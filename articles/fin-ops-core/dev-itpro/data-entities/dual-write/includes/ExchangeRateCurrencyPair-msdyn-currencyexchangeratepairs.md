## <a name="exchange-rate-currency-pair-to-msdyn_currencyexchangeratepairs"></a>Valiutos kurso valiutų pora su msdyn_currencyexchangeratepairs

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
EXCHANGERATEDISPLAYFACTOR | >< | msdyn_displayfactor | 
EXCHANGERATETYPENAME | = | msdyn_currencyexchangeratetypeid.msdyn_name | 
FROMCURRENCYCODE | = | msdyn_fromtransactioncurrencyid.isocurrencycode | 
TOCURRENCYCODE | = | msdyn_totransactioncurrencyid.isocurrencycode | 
