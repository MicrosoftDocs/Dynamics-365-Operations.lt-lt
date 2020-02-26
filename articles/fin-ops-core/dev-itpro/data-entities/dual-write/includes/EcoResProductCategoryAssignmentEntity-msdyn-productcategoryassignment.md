## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Produktų kategorijų priskyrimai su msdyn_productcategoryassignments

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
