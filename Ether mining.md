#### Что происходит

Цель данной работы состоит в том, чтобы в условиях ASIC-resistant монеты, которой, как ожидается, будет [Эфириум](https://github.com/snordenstorm/wiki/wiki/My-Ethereum-Homepage), понять наиболее грамотную тактику для её майнинга в первые месяцы работы сети. Упрощая, неплохо бы понять, что выгоднее — арендовать 100 VPS или купить 100 процессоров на авито. Текущие соображения по поводу того, как будет устроен алгоритм хеширования в Эфириум, выложены разработчиками [здесь](https://forum.ethereum.org/discussion/197/mining-faq-live-updates/p1).

Алгоритмы хеширования, которые нам кажутся хорошим приближением к тому, что будет в Эфириум и которые мы потому рассматриваем — Wild Keccak, Scrypt-N, Cryptonight, X11 (в порядке убывания удачности приближения). Будем добывать соответствующие им монеты: Boolberry, Vertcoin, Bytecoin, Darkcoin. 

#### Оглавление

* [VPS mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#vps-mining)
* [Amazon AWS Cloud Computing mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#amazon-aws-cloud-computing-mining)
* [Normal CPU mining](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#normal-cpu-mining)
* [Сравнение и выводы](https://github.com/snordenstorm/wiki/wiki/Ether-CPU-mining#%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

#### VPS mining

VPS я искал [здесь](https://poiskvps.ru/).

#### Amazon AWS Cloud Computing mining

#### Normal CPU mining

**Vertcoin**: мой дохлый домашний ноутбук, купленный ровно 5 лет назад, [выдаёт 2 khash/s](https://dl.dropboxusercontent.com/u/14533127/experiment/Vertcoin/vertcoin_my.png) <br>
**Darkcoin**:  32-bit mining is not supported as a means to protect the network against botnets.

#### Сравнение и выводы

* Процессоры можно перепродать, VPS — нет.
* Кроме того, любая CPU-монета рано или поздно превращается в GPU-монету. ПК, которыми ты физически владеешь, можно начинить GPU-майнерами; VPS — нет. Может быть, сейчас стоит закупиться GPU по копеечным ценам?