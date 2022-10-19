# ftso-site-web3
WNatContract 0x02f0826ef6aD107Cfc861152B32B52fD11BaB9ED → Write Contract 7. deposit → (wrap SGB to WSGB)    wrap 1sgb
                                                        → Write Contract 28. withdraw →(unwrap wSGB to SGB) unwrap 10в18 (100000000000000000)
contract WNat is VPToken, IWNat {
    using SafeMath for uint256;
    event  Deposit(address indexed dst, uint amount);
    event  Withdrawal(address indexed src, uint amount);
