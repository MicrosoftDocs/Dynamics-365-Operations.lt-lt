## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Išskaitomų mokesčių kodai su msdyn_withholdingtaxcodes

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
