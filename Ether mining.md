#### Что происходит

Цель данной работы состоит в том, чтобы в условиях ASIC-resistant монеты, которой, как ожидается, будет [Эфириум](https://github.com/snordenstorm/wiki/wiki/My-Ethereum-Homepage), понять наиболее грамотную тактику для её майнинга в первые месяцы работы сети. Упрощая, неплохо бы понять, что выгоднее — арендовать 100 VPS или купить 100 процессоров на авито. Текущие соображения по поводу того, как будет устроен алгоритм хеширования в Эфириум, выложены разработчиками [здесь](https://forum.ethereum.org/discussion/197/mining-faq-live-updates/p1).

Алгоритмы хеширования, которые нам кажутся хорошим приближением к тому, что будет в Эфириум и которые мы потому рассматриваем — Wild Keccak, Scrypt-N, Cryptonight, X11 (в порядке убывания удачности приближения). Будем добывать соответствующие им монеты: Boolberry, Vertcoin, Bytecoin, Darkcoin. 

#### Оглавление

* [VPS mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#vps-mining)
* [Amazon AWS Cloud Computing mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#amazon-aws-cloud-computing-mining)
* [Normal CPU mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#normal-cpu-mining)
* [Сравнение и выводы](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

#### Общая инструкция о том, как майнить в пуле, для тех, кто никогда этого не делал

[(О том, что такое майнинг-пулы и почему без них никак.)](https://github.com/snordenstorm/wiki/wiki/%D0%9C%D0%B0%D0%B9%D0%BD%D0%B8%D0%BD%D0%B3-%D0%B1%D0%B8%D1%82%D0%BA%D0%BE%D0%B9%D0%BD%D0%BE%D0%B2#%D0%A7%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-%D0%BC%D0%B0%D0%B9%D0%BD%D0%B8%D0%BD%D0%B3-%D0%BF%D1%83%D0%BB%D1%8B)

* Набираешь в гугле, например, "vertcoin pool"
* Переходишь по ссылке, попадаешь на [vtcweb.poolz.net](http://vtcweb.poolz.net/). Большинство пулов слеплено по одному шаблону и выглядит примерно как этот. 
* Если пул нравится (допустим, мне [vtcweb.poolz.net](http://vtcweb.poolz.net/) понравился) — регистрируешься.
* "Account created, please login." Login.
* Жмёшь на "My Workers", добавляешь нового нажатием "Add New Workers". Появится новая строчка: пусть я сделал так, что в моём случае в поле "Worker Login" будет написано "snordenstorm.user0", в поле "Worker Password" — "password0".
* Жмёшь на "Getting Started"
* Скачиваешь майнер. CGMiner, SGMiner — это всё майнеры для видеокарт, нам такое не надо. Нам нужен какой-нибудь CPU miner.
* Открываешь терминал или командную строку.
* Далее (под Windows) с помощью команд `cd` и `cd ..` переходишь в папку, содержащую программу-майнер (обычно она называется minerd.exe) и набираешь там следующее (для того, чтобы майнить на [конкретно этом](http://vtcweb.poolz.net/index.php?page=gettingstarted) пуле):

```
minerd.exe -a scrypt -o stratum+tcp://vtc.poolz.net:3333 -u snordenstorm.user0 -p password0
```
* И это всё! 

*Выглядеть получившееся будет примерно так. Появление yay!!! означает, что пул принял ваши вычисления и выплатит вам полагающуюся за них долю, появление booooo — что, с точки зрения пула, вы отсылаете ему какой-то бред/уже не релевантные данные. LONGPOLL detected new block — индикатор того, что какой-либо из участников сети только что нашёл новый блок, и все мы отправляемся майнить следующий.*
![pooled_mining](https://dl.dropboxusercontent.com/u/14533127/paperfor/pooled_mining.png)


#### Откуда качать майнеры

**Boolberry**: <br>
**Vertcoin**: [отсюда](https://bitcointalk.org/index.php?topic=55038.msg654850#msg654850)<br>
**Bytecoin**: <br>
**Darkcoin**: [вот](http://wiki.darkcoin.eu/wiki/Mining_Darkcoin#Mining_Programs); 32-bit mining is not supported as a means to protect the network against botnets.

#### VPS mining

<!--VPS я искал [здесь](https://poiskvps.ru/). -->

#### Amazon AWS Cloud Computing mining

#### Normal CPU mining

**Vertcoin**: мой дохлый домашний ноутбук, купленный ровно 5 лет назад, [выдаёт 2 khash/s](https://dl.dropboxusercontent.com/u/14533127/experiment/Vertcoin/vertcoin_my.png); университетский ПК выдаёт 7 khash/s, университетский 64-разрядный ПК выдаёт 15 khash/s <br>
**Darkcoin**:  

#### Сравнение и выводы

* Процессоры можно перепродать, VPS — нет.
* Кроме того, любая CPU-монета рано или поздно превращается в GPU-монету. ПК, которыми ты физически владеешь, можно начинить GPU-майнерами; VPS — нет. Может быть, сейчас стоит закупиться GPU по копеечным ценам?