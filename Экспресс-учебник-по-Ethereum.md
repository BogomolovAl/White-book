(Если вы не понимаете, куда попали, вам [сюда](https://github.com/snordenstorm/wiki/wiki/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2-%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B2%D0%B0%D0%BB%D1%8E%D1%82%D1%8B).)
Здесь я пытаюсь построить что-то вроде университетского спецкурса про Ethereum. Официальная документация расположена преимущественно по адресу [github.com/ethereum/wiki/wiki](https://github.com/ethereum/wiki/wiki). Некоторые другие места Сети, где могут быть материалы про Ethereum:
* [ethereum.org](http://ethereum.org/)
* [official Twitter](https://twitter.com/ethereumproject)
* [official youtube](http://www.youtube.com/user/ethereumproject)
* bitcointalk

В качестве нулевого этапа погружения в бездну Эфириума рекомендовал бы вдохновившие меня когда-то популярные статьи: [первая](http://bitnovosti.com/2014/03/05/dacs/), [вторая](http://bitnovosti.com/2014/03/01/etherium-next-generation-crypto/). 

Первым же этапом погружения в бездну должно стать чтение [White Paper](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper) (Манифеста). (Ниже я привожу выжимку из него — краткое содержание.) В рамках [второго этапа](https://github.com/snordenstorm/wiki/wiki/%D0%AD%D0%BA%D1%81%D0%BF%D1%80%D0%B5%D1%81%D1%81-%D1%83%D1%87%D0%B5%D0%B1%D0%BD%D0%B8%D0%BA-%D0%BF%D0%BE-Ethereum#%D0%A7%D0%B5%D0%B3%D0%BE-%D0%BD%D0%B5-%D1%85%D0%B2%D0%B0%D1%82%D0%B0%D0%B5%D1%82-%D0%B2-%D0%93%D0%BB%D0%BE%D1%81%D1%81%D0%B0%D1%80%D0%B8%D0%B8) пробежимся по всем понятиям, возникающим в Эфириум, и кратко опишем, что они примерно делают и зачем нужны.

### Краткое содержание [White Paper](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper)

* [Введение в биткойн и существующие концепции](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B2-%D0%B1%D0%B8%D1%82%D0%BA%D0%BE%D0%B9%D0%BD-%D0%B8-%D1%81%D1%83%D1%89%D0%B5%D1%81%D1%82%D0%B2%D1%83%D1%8E%D1%89%D0%B8%D0%B5-%D0%BA%D0%BE%D0%BD%D1%86%D0%B5%D0%BF%D1%86%D0%B8%D0%B8)
  - [История](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%98%D1%81%D1%82%D0%BE%D1%80%D0%B8%D1%8F)
  - [Биткойн как система изменения состояний](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%91%D0%B8%D1%82%D0%BA%D0%BE%D0%B9%D0%BD-%D0%BA%D0%B0%D0%BA-%D1%81%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F-%D1%81%D0%BE%D1%81%D1%82%D0%BE%D1%8F%D0%BD%D0%B8%D0%B9)
  - [Майнинг](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%9C%D0%B0%D0%B9%D0%BD%D0%B8%D0%BD%D0%B3)
  - [Деревья Мёркла](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%94%D0%B5%D1%80%D0%B5%D0%B2%D1%8C%D1%8F-%D0%9C%D1%91%D1%80%D0%BA%D0%BB%D0%B0)
  - [Альтернативные приложения блокчейна](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%90%D0%BB%D1%8C%D1%82%D0%B5%D1%80%D0%BD%D0%B0%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D0%B5-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B1%D0%BB%D0%BE%D0%BA%D1%87%D0%B5%D0%B9%D0%BD%D0%B0)
  - [Написание сценариев (скриптов)](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%9D%D0%B0%D0%BF%D0%B8%D1%81%D0%B0%D0%BD%D0%B8%D0%B5-%D1%81%D1%86%D0%B5%D0%BD%D0%B0%D1%80%D0%B8%D0%B5%D0%B2-%D1%81%D0%BA%D1%80%D0%B8%D0%BF%D1%82%D0%BE%D0%B2)
* [Эфириум](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%AD%D1%84%D0%B8%D1%80%D0%B8%D1%83%D0%BC)
  - [Эфириум-аккаунты](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%AD%D1%84%D0%B8%D1%80%D0%B8%D1%83%D0%BC-%D0%B0%D0%BA%D0%BA%D0%B0%D1%83%D0%BD%D1%82%D1%8B)
  - [Сообщения и транзакции](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A1%D0%BE%D0%BE%D0%B1%D1%89%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B8-%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B8)
  - [Функция изменения состояния в Эфириум](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A4%D1%83%D0%BD%D0%BA%D1%86%D0%B8%D1%8F-%D0%B8%D0%B7%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F-%D1%81%D0%BE%D1%81%D1%82%D0%BE%D1%8F%D0%BD%D0%B8%D1%8F-%D0%B2-%D0%AD%D1%84%D0%B8%D1%80%D0%B8%D1%83%D0%BC)
  - [Выполнение кода](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%92%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA%D0%BE%D0%B4%D0%B0)
  - [Блокчейн и майнинг](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%91%D0%BB%D0%BE%D0%BA%D1%87%D0%B5%D0%B9%D0%BD-%D0%B8-%D0%BC%D0%B0%D0%B9%D0%BD%D0%B8%D0%BD%D0%B3)
* [Приложения](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%9F%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
  - [Система жетонов](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D0%B0-%D0%B6%D0%B5%D1%82%D0%BE%D0%BD%D0%BE%D0%B2)
  - [Финансовые деривативы и валюты](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A4%D0%B8%D0%BD%D0%B0%D0%BD%D1%81%D0%BE%D0%B2%D1%8B%D0%B5-%D0%B4%D0%B5%D1%80%D0%B8%D0%B2%D0%B0%D1%82%D0%B8%D0%B2%D1%8B-%D0%B8-%D0%B2%D0%B0%D0%BB%D1%8E%D1%82%D1%8B)
  - [Системы идентификации и репутации](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A1%D0%B8%D1%81%D1%82%D0%B5%D0%BC%D1%8B-%D0%B8%D0%B4%D0%B5%D0%BD%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8-%D0%B8-%D1%80%D0%B5%D0%BF%D1%83%D1%82%D0%B0%D1%86%D0%B8%D0%B8)
  - [Децентрализованное хранение файлов](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%94%D0%B5%D1%86%D0%B5%D0%BD%D1%82%D1%80%D0%B0%D0%BB%D0%B8%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D0%BE%D0%B5-%D1%85%D1%80%D0%B0%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D1%84%D0%B0%D0%B9%D0%BB%D0%BE%D0%B2)
  - [Децентрализованные автономные организации](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%94%D0%B5%D1%86%D0%B5%D0%BD%D1%82%D1%80%D0%B0%D0%BB%D0%B8%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%BD%D1%8B%D0%B5-%D0%B0%D0%B2%D1%82%D0%BE%D0%BD%D0%BE%D0%BC%D0%BD%D1%8B%D0%B5-%D0%BE%D1%80%D0%B3%D0%B0%D0%BD%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D0%B8)
  - [Дальнейшие приложения](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%94%D0%B0%D0%BB%D1%8C%D0%BD%D0%B5%D0%B9%D1%88%D0%B8%D0%B5-%D0%BF%D1%80%D0%B8%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
* [Размышления и разное](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A0%D0%B0%D0%B7%D0%BC%D1%8B%D1%88%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F-%D0%B8-%D1%80%D0%B0%D0%B7%D0%BD%D0%BE%D0%B5)
  - [Реализация modified GHOST](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A0%D0%B5%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-modified-ghost)
  - [Комиссии](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%9A%D0%BE%D0%BC%D0%B8%D1%81%D1%81%D0%B8%D0%B8)
  - [Вычисление и Тьюринг-полнота](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%92%D1%8B%D1%87%D0%B8%D1%81%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%A2%D1%8C%D1%8E%D1%80%D0%B8%D0%BD%D0%B3-%D0%BF%D0%BE%D0%BB%D0%BD%D0%BE%D1%82%D0%B0)
  - [Валюта и выпуск](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%92%D0%B0%D0%BB%D1%8E%D1%82%D0%B0-%D0%B8-%D0%B2%D1%8B%D0%BF%D1%83%D1%81%D0%BA)
  - [Централизация майнинга](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%A6%D0%B5%D0%BD%D1%82%D1%80%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%BC%D0%B0%D0%B9%D0%BD%D0%B8%D0%BD%D0%B3%D0%B0)
  - [Масштабируемость](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%9C%D0%B0%D1%81%D1%88%D1%82%D0%B0%D0%B1%D0%B8%D1%80%D1%83%D0%B5%D0%BC%D0%BE%D1%81%D1%82%D1%8C)
* [Заключение](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%97%D0%B0%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%BD%D0%B8%D0%B5)
* [Заметки и дальнейшее чтение](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-White-Paper#%D0%97%D0%B0%D0%BC%D0%B5%D1%82%D0%BA%D0%B8-%D0%B8-%D0%B4%D0%B0%D0%BB%D1%8C%D0%BD%D0%B5%D0%B9%D1%88%D0%B5%D0%B5-%D1%87%D1%82%D0%B5%D0%BD%D0%B8%D0%B5)

### Чего не хватает в [Глоссарии](https://github.com/snordenstorm/wiki/wiki/%5BRussian%5D-Glossary)

Глоссарий, как и всегда — словарик, объясняющий все связанные с нашей темой термины. Скорее всего, нужный Вам термин есть там. Поскольку глоссарий несовершенен, ниже предполагается объяснять всё, что в нём упущено. 

* RLP
* Patricia Tree
* Wire protocol
* Light client protocol
* Serpent

### Further reading

* [yellow paper](http://gavwood.com/Paper.pdf) (осторожно, это хардкор)