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

* "I first wrote the initial draft of the Ethereum whitepaper on a cold day in San Francisco in November, as a culmination of months of thought and often frustrating work into an area that we have come to call “cryptocurrency 2.0″ ..."

Очень мило, конечно. Но, как понятно ещё из названия, статья outdated.

##### [Conference, Alpha Testnet and Ether Pre-sale Updates](https://blog.ethereum.org/2014/01/29/conference-alpha-testnet-and-ether-pre-sale-updates/)

Уже неактуальные сведения (ааа, простите, не первого февраля presale).

##### [On Transaction Fees, And The Fallacy of Market-Based Solutions](https://blog.ethereum.org/2014/02/01/on-transaction-fees-and-the-fallacy-of-market-based-solutions/)

##### [Introducing Ethereum Script 2.0](https://blog.ethereum.org/2014/02/03/introducing-ethereum-script-2-0/)

##### [More Thoughts on Scripting and Future-Compatibility](https://blog.ethereum.org/2014/02/05/more-thoughts-on-scripting-and-future-compatibility/)

##### [Cryptographic Code Obfuscation: Decentralized Autonomous Organizations Are About to Take a Huge Leap Forward](https://blog.ethereum.org/2014/02/08/cryptographic-code-obfuscation-decentralized-autonomous-organizations-are-about-to-take-a-huge-leap-forward/)

##### [Why Not Just Use X? An Instructive Example from Bitcoin](https://blog.ethereum.org/2014/02/09/why-not-just-use-x-an-instructive-example-from-bitcoin/)

##### [Important Statement regarding the Ether pre-sale](https://blog.ethereum.org/2014/02/13/important-statement-regarding-the-ether-pre-sale/)

##### [Ethereum Scalability and Decentralization Updates](https://blog.ethereum.org/2014/02/18/ethereum-scalability-and-decentralization-updates/)

##### [DAOs Are Not Scary, Part 1: Self-Enforcing Contracts And Factum Law](https://blog.ethereum.org/2014/02/24/daos-are-not-scary-part-1-self-enforcing-contracts-and-factum-law/)

##### [DAOs Are Not Scary, Part 2: Reducing Barriers](https://blog.ethereum.org/2014/03/01/daos-are-not-scary-part-2-reducing-barriers/)

##### [The Question of Mining](https://blog.ethereum.org/2014/03/20/the-question-of-mining/)

##### [The Latest EVM: “Ethereum Is A Trust-Free Closure System”](https://blog.ethereum.org/2014/03/20/the-latest-evm-ethereum-is-a-trust-free-closure-system/)

##### [SchellingCoin: A Minimal-Trust Universal Data Feed](https://blog.ethereum.org/2014/03/28/schellingcoin-a-minimal-trust-universal-data-feed/)

##### [Pyethereum and Serpent Programming Guide](https://blog.ethereum.org/2014/04/10/pyethereum-and-serpent-programming-guide/)

##### [The Issuance Model in Ethereum](https://blog.ethereum.org/2014/04/10/the-issuance-model-in-ethereum/)

##### [Decentralized Protocol Monetization and Forks](https://blog.ethereum.org/2014/04/30/decentralized-protocol-monetization-and-forks/)

##### [Serpent upgrades: More Fun Stuff](https://blog.ethereum.org/2014/05/02/serpent-upgrades-more-fun-stuff/)

##### [DAOs, DACs, DAs and More: An Incomplete Terminology Guide](https://blog.ethereum.org/2014/05/06/daos-dacs-das-and-more-an-incomplete-terminology-guide/)

##### [What is Ethereum? Project, Platform, Fuel, Stack.](https://blog.ethereum.org/2014/05/14/what-is-ethereum-project-platform-fuel-stack/)

##### [The Xbox and Ethereum’s Dual Mandate](https://blog.ethereum.org/2014/05/15/the-xbox-and-ethereums-dual-mandate/)

##### [Long-Range Attacks: The Serious Problem With Adaptive Proof of Work](https://blog.ethereum.org/2014/05/15/long-range-attacks-the-serious-problem-with-adaptive-proof-of-work/)

##### [On Long-Term Cryptocurrency Distribution Models](https://blog.ethereum.org/2014/05/24/on-long-term-cryptocurrency-distribution-models/)

##### [What If Ethereum Lived on a Treap? Or, Blockchains Charging Rent](https://blog.ethereum.org/2014/05/27/what-if-ethereum-lived-on-a-treap-or-blockchains-charging-rent/)

##### [Ethereum Project Update](https://blog.ethereum.org/2014/06/05/ethereum-project-update/)

##### [On Mining](https://blog.ethereum.org/2014/06/19/mining/)

##### [Advanced Contract Programming Example: SchellingCoin](https://blog.ethereum.org/2014/06/30/advanced-contract-programming-example-schellingcoin/)

##### [On Stake](https://blog.ethereum.org/2014/07/05/stake/)

##### [Background on the mechanics of the ether pre-sale](https://blog.ethereum.org/2014/07/09/how-to-make-a-purchase-in-the-ether-presale/)

##### [Toward a 12-second Block Time](https://blog.ethereum.org/2014/07/11/toward-a-12-second-block-time/)

##### [the ethereum project: learning to dream with open minds](https://blog.ethereum.org/2014/07/14/the-ethereum-project/)

##### [Ethereum and Oracles](https://blog.ethereum.org/2014/07/22/ethereum-and-oracles/)

##### [Launching the Ether Sale](https://blog.ethereum.org/2014/07/22/launching-the-ether-sale/)

##### [Ether Purchase Troubleshooting](https://blog.ethereum.org/2014/07/23/ether-purchase-troubleshooting/)

##### [Programming Society with Asm: Gavin Wood at Assembly 2014](https://blog.ethereum.org/2014/08/06/programming-society-with-asm-gavin-wood-at-assembly-2014/)

##### [Ether Sale: A Statistical Overview](https://blog.ethereum.org/2014/08/08/ether-sale-a-statistical-overview/)

##### [Announcement on planned withdrawal from exodus](https://blog.ethereum.org/2014/08/08/announcement-on-planned-exodus-withdrawal/)

##### [Secret Sharing and Erasure Coding: A Guide for the Aspiring Dropbox Decentralizer](https://blog.ethereum.org/2014/08/16/secret-sharing-erasure-coding-guide-aspiring-dropbox-decentralizer/)

##### [building the decentralized web 3.0](https://blog.ethereum.org/2014/08/18/building-decentralized-web/)

##### [An Introduction to Futarchy](https://blog.ethereum.org/2014/08/21/introduction-futarchy/)

##### [State of Ethereum: August Edition](https://blog.ethereum.org/2014/08/27/state-ethereum-august-edition/)

##### [Software and Bounded Rationality](https://blog.ethereum.org/2014/09/02/software-bounded-rationality/)

##### [crypto renaissance](https://blog.ethereum.org/2014/09/02/crypto-renaissance/)

##### [Scalability, Part 1: Building on Top](https://blog.ethereum.org/2014/09/17/scalability-part-1-building-top/)

##### [Slasher Ghost, and Other Developments in Proof of Stake](https://blog.ethereum.org/2014/10/03/slasher-ghost-developments-proof-stake/)

##### [Gav’s ÐΞV Update I: Where Ethereum’s at](https://blog.ethereum.org/2014/10/17/gavs-d%CE%BEv-update-ethereums/)

##### [Scalability, Part 2: Hypercubes](https://blog.ethereum.org/2014/10/21/scalability-part-2-hypercubes/)

##### [An Information-Theoretic Account of Secure Brainwallets](https://blog.ethereum.org/2014/10/23/information-theoretic-account-secure-brainwallets/)

##### [Gav’s Ethereum ÐΞV Update II](https://blog.ethereum.org/2014/11/01/gavs-ethereum-d%CE%BEv-update-ii/)

##### [Jeff’s Ethereum ÐΞV Update I](https://blog.ethereum.org/2014/11/02/jeffs-ethereum-d%CE%BEv-update/)

##### [Ethereum Community and Adoption Update – Week 1](https://blog.ethereum.org/2014/11/03/stephans-ethereum-community-adoption-update-week-1/)

##### [The Search for a Stable Cryptocurrency](https://blog.ethereum.org/2014/11/11/search-stable-cryptocurrency/)

##### [Scalability, Part 3: On Metacoin History and Multichain](https://blog.ethereum.org/2014/11/13/scalability-part-3-metacoin-history-multichain/)

##### [Gav’s Ethereum ÐΞV Update III](https://blog.ethereum.org/2014/11/18/gavs-d%CE%BEv-update-iii/)

##### [On Bitcoin Maximalism, and Currency and Platform Network Effects](https://blog.ethereum.org/2014/11/20/bitcoin-maximalism-currency-platform-network-effects/)

##### [Proof of Stake: How I Learned to Love Weak Subjectivity](https://blog.ethereum.org/2014/11/25/proof-stake-learned-love-weak-subjectivity/)

##### [From inside Ethereum ÐΞVhub Berlin](https://blog.ethereum.org/2014/12/02/inside-ethereum-d%CE%BEvhub-berlin/)

фоточкэ

##### [ÐΞVcon-0 Recap](https://blog.ethereum.org/2014/12/05/d%CE%BEvcon-0-recap/)

##### [Gav’s Ethereum ÐΞV Update IV](https://blog.ethereum.org/2014/12/15/gavs-ethereum-d%CE%BEv-update-iv/)

##### [Ethereum ÐΞV: What are we doing?](https://blog.ethereum.org/2014/12/17/ethereum-d%CE%BEv/)

##### [A call to all the bug bounty hunters out there…](https://blog.ethereum.org/2014/12/18/call-bug-bounty-hunters/)

##### [Secret Sharing DAOs: The Other Crypto 2.0](https://blog.ethereum.org/2014/12/26/secret-sharing-daos-crypto-2-0/)

##### [On Silos](https://blog.ethereum.org/2014/12/31/silos/)

##### [Jeff’s Ethereum ÐΞV Update II](https://blog.ethereum.org/2015/01/06/jeffs-ethereum-dev-update-2/)

##### [Ethereum Community Survey](https://blog.ethereum.org/2015/01/09/ethereum-community-survey/)

##### [Light Clients and Proof of Stake](https://blog.ethereum.org/2015/01/10/light-clients-proof-stake/)