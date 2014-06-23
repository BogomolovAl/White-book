English documentation must be as clear and explicit as possible.

Here is the list of things that remained unclear to me even after ... reading. I don't think I'm a complete idiot, so these moments could probably be unclear to other respectable readers.

## List of misprints in Ethereum White Paper

0) in [History](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#history): the link under "reusable proofs of work"  is broken, the underlying site is down for at least several weeks.

1) in [Token Systems](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#token-systems): "The key point to understand is that all a currency, or token systen, fundamentally is is a database with one operation" - several misprints here

2) in [Token Systems](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#token-systems): "A had at least X units before the transaction" instead of "X had at least X units before the transaction"

*3) in [Fees](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#fees): "is borne by third parties". Borne?

4) in [Currency and Issuance](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#currency-and-issuance): We also theorize that because coins are always lost over time due to carelessness, death, etc, and coin loss can be modeled as a percentage of the total supply per year, that the total currency supply in circulation will in fact eventually stabilize at a value equal to the annual issuance divided by the loss rate (eg. at a loss rate of 1%, once the supply reaches 30X then 0.3X will be mined and 0.3X lost every year, creating an equilibrium).

What? o_O

5) [Alternative Blockchain Application](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#alternative-blockchain-applications): broken link to namecoin.org (broken SSL-certificate); the correct address now is namecoin.info

6) [Scripting](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#scripting): "and returns 1 if the verification is successful and 0 otherwise". I thought "return 1" means "return error"? 

7) [Scripting](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#scripting): "elliptic curve signature algorithm would likely require 256 repeated multiplication rounds". Multiplication, not addition?

8) in https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Ethereum-TOC Serpent is high-level language, but in White Paper it is all way low-level.

9) [Your link to LLL on the Ethereum TOC page](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Ethereum-TOC) is broken (to be more precise, Romanian version instead).

10) [Table of contents](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#table-of-contents) should begin not with "History", but with "Introduction to Bitcoin and Existing Concepts"

11) In [Serpent](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-Serpent-programming-language-operations#arithmetic) in item "Arithmetic wraps.." there's the arithmetic mistake: `x = 3 ^ (2 ^ 255)` sets x to 1, but NOT `x = 3 ^ (2 ^ 254)`. [Euler totient function](http://en.wikipedia.org/wiki/Euler%27s_totient_function) \phi (2^256) = 2^255, so if 3 in some power is equal to 1 modulo 2<sup>256</sup>, then this is 3<sup>\phi(2<sup>256</sup>)</sup> = 3<sup>2<sup>255</sup></sup>.

## Minor issues

1) [Currency and Issuance](https://github.com/ethereum/wiki/wiki/%5BEnglish%5D-White-Paper#currency-and-issuance): "the denominations will be pre-labelled":

1: wei
10^3: lovelace 
...
10^18: ether.

And everywhere else in this text you write "Let Alice send 1000 ether to Bob.." You don't mean 1000*(10<sup>18</sup>), do you? So, I think, "1" must be ether, not wei. Anyway, 

## List of unclear moments