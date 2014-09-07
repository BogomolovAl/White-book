English documentation must be as clear and explicit as possible.

Here is the list of things that remained unclear to me even after careful reading. I don't think I'm a complete idiot, so these moments could probably be unclear to other respectable readers. This list is not comprehensive; it provides by far not all the insufficiently-explained moments.

## List of misprints in Ethereum White Paper

0) in [History](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#history): the link under "reusable proofs of work"  is broken, the underlying site is down for at least several weeks.

1) in [Token Systems](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#token-systems): "The key point to understand is that all a currency, or token systen, fundamentally is is a database with one operation" - several misprints here

2) in [Token Systems](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#token-systems): "A had at least X units before the transaction" instead of "X had at least X units before the transaction"

*3) in [Fees](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#fees): "is borne by third parties". Borne?

4) in [Currency and Issuance](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#currency-and-issuance): We also theorize that because coins are always lost over time due to carelessness, death, etc, and coin loss can be modeled as a percentage of the total supply per year, that the total currency supply in circulation will in fact eventually stabilize at a value equal to the annual issuance divided by the loss rate (eg. at a loss rate of 1%, once the supply reaches 30X then 0.3X will be mined and 0.3X lost every year, creating an equilibrium).

What? o_O

5) [Alternative Blockchain Application](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#alternative-blockchain-applications): broken link to namecoin.org (broken SSL-certificate); the correct address now is namecoin.info

6) Why does the attacker always have to send the money to himself when he starts mining a fork? Why couldn't he just mine the block without any transactions related to him? Just "forgetting" the transaction done in exchange for a digital good.

7) [Scripting](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#scripting): "elliptic curve signature algorithm would likely require 256 repeated multiplication rounds". Multiplication, not addition?

8) in https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Ethereum-TOC Serpent is high-level language, but in White Paper it is all way low-level.

9) [Your link to LLL on the Ethereum TOC page](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Ethereum-TOC) is broken (to be more precise, Romanian version instead).

10) [Table of contents](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#table-of-contents) should begin not with "History", but with "Introduction to Bitcoin and Existing Concepts"

11) In [Serpent](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Serpent-programming-language-operations#arithmetic) in item "Arithmetic wraps.." there's the arithmetic mistake: `x = 3 ^ (2 ^ 255)` sets x to 1, but NOT `x = 3 ^ (2 ^ 254)`. [Euler totient function](http://en.wikipedia.org/wiki/Euler%27s_totient_function) \phi (2^256) = 2^255, so if 3 in some power is equal to 1 modulo 2<sup>256</sup>, then this is 3<sup>\phi(2<sup>256</sup>)</sup> = 3<sup>2<sup>255</sup></sup>.

12) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Serpent-programming-language-operations#functions) you need to fix the third item.

13) In the very beginning of [Dagger](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Dagger): "Currently, there are three major categories.." "However, both are imperfect.."

14) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Dagger#scrypt) in the end of the paragraph the link that is not rendered nicely is, moreover, broken ;) error 404.

15) This is really important issue. Look at the last paragraph of [Ethereum State Transition Function](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#ethereum-state-transition-function). As far as I understand, the thought «If there was no contract at the receiving end of the transaction, you can just ignore the "Run the code" step» is intended. Then you say "the total transaction fee would simply be equal to the provided `GASPRICE` multiplied by the length of the transaction in bytes" (only step 3, no step 5, as far as I understand). But look at the step 3! There you multiply your transaction length by the byte-fee but not by the `GASPRICE`! They are completely different numbers.

16) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#code-execution): "While the Ethereum virtual machine is running, its full computational state can be defined by the tuple `(block_state, transaction, message, code, memory, stack, pc, gas)`, where `block_state` is the global state containing all accounts and includes balances and storage."

Really all? All accounts in the world?

17) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#blockchain-and-mining) you use the variable `GASLIMIT`, but there is no such variable; you must mean `STARTGAS`. (It's better to rename `STARTGAS` => `GASLIMIT` actually.)

18) [Here in the sixth point](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#blockchain-and-mining): "For all in in..", of course "For all `i` in"

19) on [ethereum.org](http://ethereum.org) (sic!) after you press "why": "For example, when when you deposit money.."

20) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#financial-derivatives-and-stable-value-currencies) in the last paragraph: "Unike issuers.."

21) In [this](https://github.com/ethereum/wiki/wiki/Glossary#blockchains) subsection the very last word: maintenance

22) [Here](https://github.com/ethereum/wiki/wiki/Glossary#non-blockchain): "prorgamming languages"

23) [Here](https://github.com/ethereum/wiki/wiki/Glossary#surrounding-concepts-applications-and-governance) : "Decentralized autonomous organization: decentralized organization where" instead of "Decentralized autonomous organization: decentralized organizations where"

24) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#scripting), subsubsection "Value-blindness": I do not understand piece "(eg. one UTXO of 2<sup>k</sup> for every k up to 30) and having O pick which UTXO to send to A and which to B" completely. I understand everything else in this subsubsection, but not this.

25) The last sentence of [this subsection](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#decentralized-file-storage): "If a contract is still paying out money, that provides a cryptographic proof that someone out there is still storing the piece of file." instead of "If a contract is still paying out money, that provides a cryptographic proof that someone out there is still storing the file."

26) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#decentralized-autonomous-organizations): distinquished => distinguished 

27) In [GHOST](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#modified-ghost-implementation): "Greedy Heaviest Observed Subtree", not Heavist

28) In [GHOST](https://github.com/ethereum/wiki/wiki/Glossary#ethereum-blockchain): "and mitigates the problem with fast blockchains that large miners have an advantage because they" instead of "and mitigates a problem with fast blockchains that large miners have an advantage because they"


## Minor issues

1) [Currency and Issuance](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#currency-and-issuance): "the denominations will be pre-labelled":

1: wei
10^3: lovelace 
...
10^18: ether.

And everywhere else in this text you write "Let Alice send 1000 ether to Bob.." You don't mean 1000*(10<sup>18</sup>), do you? So, I think, "1" must be ether, not wei. Anyway, 

2) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Dagger#scrypt) in the 4th item you need to close the bracket.

3) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Dagger#birthday-attack) is misprint in the last paragraph: "that is memory-hard to computer but memory-easy to verify"

4) [Here](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#a-next-generation-smart-contract-and-decentralized-application-platform): "smart property" broken/absent link.
## List of unclear moments