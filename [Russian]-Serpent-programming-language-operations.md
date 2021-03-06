[Russian] Serpent — высокоуровневый язык для написания контрактов. [Ссылка на англоязычный оригинал.](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Serpent-programming-language-operations)

## Арифметика

* Простые арифметические операции выполняются как обычно: `x = 20 + 7 * 5` присваивает `x` значение `55`
* Отсутствуют отрицательные числа: попытка произвести присваивание `x = 0 - 1` присваивает `x` значение `115792089237316195423570985008687907853269984665640564039457584007913129639935`
* Дробные числа также отсутствуют: `x = 7 / 4` приводит к `x` равному единице
* Если нужно закрыть глаза на то, что какие-то числа отрицательные или дробные, можно использовать `#/` и `#%`: запись `x = (0-9) #/ 3 + 5` кладёт `x` равным двойке, в то время как `y = (0-9) / 3 + 5` кладёт `y` равным `38597363079105398474523661669562635951089994888546854679819194669304376546647`
* Арифметика ломается при достижении цифры 2<sup>256</sup>: `x = 3 ^ (2 ^ 255)` приравнивает `x` к единице (это красивое следствие [теоремы Эйлера](http://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BE%D1%80%D0%B5%D0%BC%D0%B0_%D0%AD%D0%B9%D0%BB%D0%B5%D1%80%D0%B0_(%D1%82%D0%B5%D0%BE%D1%80%D0%B8%D1%8F_%D1%87%D0%B8%D1%81%D0%B5%D0%BB)))
* Для побитовых операций можно использовать `x = y | z`, `x = y & z` и `x = y xor z`

### Переменные

* Простейшие операции — как и в любом другом языке: выполнение 

```
x = 25
y = x + 5
```

приведёт к тому, что `y` будет присвоено значение `30`
* Массив из `n` (32-байтовых) величин можно инициализировать командой `x = array(n)`. Нумерация элементов массива начинается с нуля, т.е. `x[0]` вполне себе есть.
* Задать элементы массива можно командой вида `x[i] = v`. Получить элементы массива можно командой вида `v = x[i]`.
* Строку (байтовый массив) из `n` байтов можно инициализировать командой `x = bytes(n)`.
* i-ый байт в ней можно задать командой `setch(x,i,v)`. Получить значение i-ого байта можно командой `v = getch(x,i)`.
* Для быстрого задания массивов можно использовать скобки []: `x = [1,2,3]`.

Переменная с точки зрения ВМЭ-кода — это нечто, чему приписывается индекс в памяти; все переменные не только являются 32-байтовыми, но и отделены друг от друга 32 байтами. In the last example, `x` literally is the memory index of the start of the array, which is itself stored in a dynamically allocated slice of memory. Заметим, что проверка "выхода за границы" массива не производится; `array(3)[5] = 10` (попытка работать с пятым элементом массива из трёх элементов) будет приводить к непредсказуемым и зависящим от компилятора последствиям выполнения кода.

### Псевдопеременные

В Эфириум встроены следующие псевдопеременные и псевдомассивы:

* `block.prevhash` — хэш предыдущего блока
* `block.number` — номер блока
* `block.timestamp` — таймштамп блока
* `block.difficulty` — сложность нахождения блока
* `block.coinbase` — адрес майнера блока (*что имел в виду автор?*)
* `block.gaslimit` — максимальное количество газа, которое может быть потрачено в блоке(?)
* `tx.gasprice` — 
* `tx.origin` — исходный отправитель транзакции (НЕ отправитель текущего сообщения, это не одно и то же лицо в случае вложенных контрактов)
* `tx.gas` — текущее количество газа в наличии (количество оставшегося к данному моменту вычисления контракта газа)
* `msg.datasize` — длина информации в сообщении, измеряемая как число (полных?) 32-байтовых кусков
* `msg.sender` — отправитель сообщения
* `msg.value` — количество эфира, прикреплённое к сообщению
* `contract.balance` — баланс контракта
* `msg.data[i]` — i-ый 32-байтовый кусок информации в сообщении (сообщение состоит из 32-байтовых кусков)
* `contract.storage[i]` — то, что находится в хранилище контракта под индексом `i`

### Функции

* `send(to, value, gas)` — пересылает `value` единиц эфира по адресу `to`, и вычисление такого контракта обеспечено количеством газа `gas`.
* `x = msg(to, value, gas, datastart, datalen)` — пересылает сообщение по адресу `to`, используя информацию, содержащуюся под индексами `datastart ... datastart+(datalen*32)-1` (т.е. всю информацию, ибо хранится она 32-байтовыми кусками), а также пересылает туда `value` единиц эфира и `gas` единиц газа, и приравнивает `x` к первым 32 байтам результата(?).
* `msg(to, value, gas, datastart, datalen, outputstart, outputlen)` — пересылает сообщение по адресу `to`, используя информацию, содержащуюся под индексами `datastart ... datastart+(datalen*32)-1`, а также пересылает туда `value` единиц эфира и `gas` единиц газа, и записывает результат(?) в индексы `outputstart ... outputstart+(outputlen*32)-1`
* `x = create(endowment, gas, datastart, datalen)` — создаёт новый контракт и возвращает адрес контракта
* `x = sha3(v)` — возвращает SHA3 данной 32-байтовой величины
* `x = byte(y,z)` — приравнивает `x` к`z`-ому байту `y`

Покажем, как работает описанная выше функция `msg(..)`. Рассмотрим два эквивалентных примера: этот

`x = msg(0xf345747062de4d05d897d62c4696febbedcb36b8, 10^18, tx.gas - 100, [10,20,30], 3)`

и этот:

```
a = array(3)
a[0] = 10
a[1] = 20
a[2] = 30
y = array(1)
msg(0xf345747062de4d05d897d62c4696febbedcb36b8, 10^18, tx.gas - 100, a, 3, y, 1)
x = y[0]
```

### Условия и циклы

Проще всего разобраться на примерах. Вот первый пример:

```
if x > 5:
    y = 7
```

а вот второй:

```
x = 248
while x > 1:
    if (x % 2) == 0: 
        x = x / 2
    else:
        x = 3 * x + 1
```

Заметим, что запись в одну строку `if x > 5: y = 7` является ошибочной.

### Комментарии

```
x = 4 //это комментарий, и он игнорируется при компиляции кода контракта 
  // это тоже комментарий, и на этот раз вся строка посвящена ему 
  /* а такой стиль комментариев не поддерживается */
```

### Прерывающие операции

* `stop` — эта инструкция, размещённая на отдельной строке, совершает выход из цикла (как команда `break` в C++)
* `return(x)` — возвращает (32-байтовое) значение переменной x
* `return(memstart, len)` — возвращает содержимое памяти под индексами `memstart ... memstart+(32*len)-1`
* `suicide(a)` — уничтожает контракт, пересылая весь остающийся баланс на нём по адресу `a`