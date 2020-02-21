## <a name="currencies-to-transactioncurrencies"></a>Valiutos su transactioncurrencies

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

Šaltinio filtras: ((CURRENCYCODE != "999"))

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
nėra | >> | exchangerate | 1
