## <a name="cds-released-distinct-products-to-products"></a>CDS išleisti išskirtieji produktai su produktais

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
PRODUCTNUMBER | >> | msdyn_productnumber | 
PRODUCTNAME | >> | pavadinimas | 
PRODUCTDESCRIPTION | >> | aprašas | 
ITEMNUMBER | >> | msdyn_itemnumber | 
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode | 
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol | 
SALESPRICE | >> | kaina | 
UNITCOST | >> | currentcost | 
PRODUCTTYPE | >> | producttypecode | 
SALESUNITDECIMALPRECISION | >> | quantitydecimal | 0
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight | 
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname | 
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration | 
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize | 
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle | 
