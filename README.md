# ftso-site-web3
Сайт "визитка" с минимальным функционалом (web3 подключение кошелька, оборачивание разворачивание SGB/WSGB,делигирование двум FTSO на выбор) отображение ценовых данных на сайте, тех средних точных данных из blockchain которые отправляют FTSO.
WNatContract находится по ссылке в https://songbird-explorer.flare.network/address/0x02f0826ef6aD107Cfc861152B32B52fD11BaB9ED/write-contract#address-tabs со списком всех необходимых команд:
 0x02f0826ef6aD107Cfc861152B32B52fD11BaB9ED → Write Contract пункт 7. deposit → (wrap SGB to WSGB)    wrap 1sgb
                                                        → Write Contract пункт 28. withdraw →(unwrap wSGB to SGB) unwrap 10в18 (100000000000000000)
contract WNat is VPToken, IWNat {
    using SafeMath for uint256;
    event  Deposit(address indexed dst, uint amount);
    event  Withdrawal(address indexed src, uint amount);
