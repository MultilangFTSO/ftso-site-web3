# ftso-site-web3
A business card site with minimal functionality:

- connection via Metamask (View the repo: https://gist.github.com/timothycarambat/e7e014a6fd08f33e753bcf2f9e31239e)
- Output of currency price feed from the Songbird Network blockchain based on EVM (View the repo:https://github.com/Onaxim/ftso-price-feed)
- Ability to wrap/unwrap native SGB token to WSGB and vice versa
- Ability to delegate wrapped WSGB to a choice of two FTSO providers, there are examples of two sites: ftso.thegrungies.com, evolveftso.com/delegate.html

List of all required commands is in: WNatContract is at the link in https://songbird-explorer.flare.network/address/0x02f0826ef6aD107Cfc861152B32B52fD11BaB9ED/write-contract#address-tabs

0x02f0826ef6aD107Cfc861152B32B52fD11BaB9ED → Write Contract point7. deposit → (wrap SGB to WSGB) wrap 1sgb → Write Contract point28. withdraw →(unwrap wSGB to SGB) unwrap 10in18 (100000000000000000)

contract WNat is VPToken, IWNat { using SafeMath for uint256; event Deposit(address indexed dst, uint amount); event Withdrawal(address indexed src, uint amount);

There are a few of ways to improve this code such as resolving all prices of symbols at the same time (using Promise.All). We can also be selective with which ABI items you import which could also mitigate issues such as the one with getCurrentPrice having two input parameters (by specifying only one option you will be able to call it as normal rather than by specifiyng the method name and input type).
