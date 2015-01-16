Данные заметки - попытка привести полное изложение блога [blog.ethereum.org](https://blog.ethereum.org/). Мы идём в обратном порядке (от 31 декабря 2013 к более современным постам).

##### [Bootstrapping A Decentralized Autonomous Corporation: Part I](https://blog.ethereum.org/2013/12/31/bootstrapping-a-decentralized-autonomous-corporation-part-i/)

* У корпораций, как правило, существует mission statement (у большинства он заключается в том, чтобы делать деньги для держателей акций, но - не только). Его изложением занимается совет директоров. На самом деле его можно изложить в виде кода; тогда отпадёт необходимость в совете директоров.
* Очевидно, такой код не должен храниться на какой-то одной машине => distributed computing
* 501-of-1000 multisignature addresses - отстой. Почему? Во-первых, потому что это 501 ЭЦП в транзакции => 501*70 байт = 35 Кб - размер одной транзакции. (Текущий биткойн-клиент не принимает транзакции размером более 10 Кб.) Во-вторых, если корпорация хочет разместить нефинансовые данные, Биткойн бесполезен.
* secure multiparty computation норм

##### [Bootstrapping An Autonomous Decentralized Corporation, Part 2: Interacting With the World](https://blog.ethereum.org/2013/12/31/bootstrapping-an-autonomous-decentralized-corporation-part-2-interacting-with-the-world/)

* Ок, мы поняли, что возможны такие децентрализованные корпорации, которые будут думать и поддерживать свой Биткойн-баланс и слать биткойн-транзакции. Но как они с миром-то вокруг будут взаимодействовать?
* Например, как они будут следить за событиями в мире вокруг? Например, как они будут догадываться до того, чего хотят люди и какие доступны для них ресурсы?
* Данные бывают самопроверяемые и не обладающие этим свойством. В этом смысле Биткойн - интересный случай: правильно подписанные транзакции в Биткойн полностью самопроверяемы (если цифровая подпись проходит через алгоритм проверки цифровой подписи, транзакция валидна).
* Время, например, не самопроверяемо, однако в Биткойн "принцип причинности" реализован известно как: неважно, что произошло первым, важно, что попало в блокчейн большинства первым. Обобщая: можно сбацать примерно такой же механизм для определения верного значения той или иной величины (при котором на мнения тех, кто идёт против "mainstream view", забивают - SchellingCoin-стайл). С помощью такой штуки можно было бы узнавать стоимость 1 BTC и изменять скорость выпуска так, чтобы стабилизировать цену. 
* Но нихуя! Активным майнерам выгодно задирать цену. Причём даже нельзя быть честным и продолжать получать честные деньги с майнинга. Чем выше стоимость 1 BTC, тем больше денег печатается => декларируемая стоимость 1 BTC всё выше и выше => ... => hyperinflation.
* В случае PoS будет всё то же самое, только активным майнерам будет выгодно занижать цену.

...

##### [Bootstrapping a Decentralized Autonomous Corporation, Part 3: Identity Corp](https://blog.ethereum.org/2013/12/31/bootstrapping-a-decentralized-autonomous-corporation-part-3-identity-corp/)

##### [Slasher: A Punitive Proof-of-Stake Algorithm](https://blog.ethereum.org/2014/01/15/slasher-a-punitive-proof-of-stake-algorithm/)

*

##### [Ethereum: Now Going Public](https://blog.ethereum.org/2014/01/23/ethereum-now-going-public/)

##### [Conference, Alpha Testnet and Ether Pre-sale Updates](https://blog.ethereum.org/2014/01/29/conference-alpha-testnet-and-ether-pre-sale-updates/)

##### [On Transaction Fees, And The Fallacy of Market-Based Solutions](https://blog.ethereum.org/2014/02/01/on-transaction-fees-and-the-fallacy-of-market-based-solutions/)

##### [Introducing Ethereum Script 2.0](https://blog.ethereum.org/2014/02/03/introducing-ethereum-script-2-0/)

##### [More Thoughts on Scripting and Future-Compatibility](https://blog.ethereum.org/2014/02/05/more-thoughts-on-scripting-and-future-compatibility/)

##### [Cryptographic Code Obfuscation: Decentralized Autonomous Organizations Are About to Take a Huge Leap Forward](https://blog.ethereum.org/2014/02/08/cryptographic-code-obfuscation-decentralized-autonomous-organizations-are-about-to-take-a-huge-leap-forward/)