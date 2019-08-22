---
title: Operacijų perkėlimas į Intrastat
description: Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat.
author: Anasyash
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 919c3cd755458f46a9f083415aa196c703fcf338
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852527"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Naujo prekės kodo kūrimas ir esamo naujinimas
1. Pasirinkite **Moduliai > Produkto informacijos valdymas > Nustatymas > Kategorijos ir atributai > Kategorijų hierarchijos**.
2. Sąraše raskite arba pasirinkite **Intrastat commodity codes.** įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Medyje pasirinkite „įrašas‟. Pavyzdžiui, pasirinkit **Intrastat\Speaker**.  
5. Spustelėkite **Redaguoti**.
6. Išplėskite fastTab **Foreign trade** dalįf
7. Lauke **Additional units** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **pcs**.  
8. Lauke **Weight not applicable** pasirinkite **Yes**.
9. Medyje pasirinkite **Intrastat**.
10. Spustelėkite **New category node**.
11. Lauke **Name** įveskite prekės pavadinimą. Pavyzdžiui, įveskit **Other commodity**.  
12. Lauke **Code**įveskite prekės kodą. Pavyzdžiui, įveskit **995 00 00**.  
13. Lauke „Patogus pavadinimas“ įveskite reikšmę. Pavyzdžiui, įveskite **Other**.  
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Prekės kodo priskyrimas produktų hierarchijai ir išleistam produktui
1. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką **sales** reikšme **sales **.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Medyje išplėskit **a category node**. Pavyzdžiui, išplėskit **Sales hierarchy\Home audio**.  
4. Medyje pasirinkite **the category to assign to the commodity code**. Pavyzdžiui, pasirinkite **Pardavimo hierarchija \ Namų garso sistema \ Garsiakalbiai.  
5. Išplėskite fastTab **Commodity codes** dalį.
6. Spustelėkite **Pridėti**.
7. Lauke **Select hierarchy** pasirinkite **Intrastat**.
8. Sąraše raskite ir pasirinkite prekės kodą. Pavyzdžiui, pasirinkit **920 20 34 Speaker**.  
9. Spustelėkite rodyklę, kad pasirinktumėte tiekėją.
10. Spustelėkite **Gerai**.
11. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
12. Sąraše pasirinkite išleistą produktą, kurį priskirsite prekės kodui. Pavyzdžiui, pasirinkite **D0001**.  
13. Spustelėkite **Redaguoti**.
14. Išplėskite fastTab **Foreign trade** dalįf
15. Lauke **Commodity** įveskite prekės kodą. Pavyzdžiui, pasirinkite reikšmę **920 20 34 Speaker**.    
16. Lauke **Charges percentage** įveskite skaičių. Pavyzdžiui, įveskite **3**.  
17. Lauke **Country/region** įveskite arba pasirinkite kilmės šalį arba regioną. Pavyzdžiui, pasirinkite **AUT**.  
18. Išplėskite dalį **Manage inventory**.
19. Lauke **Net weight**įveskite svorį kilogramais. Pavyzdžiui, įveskite **2.5**.  
20. Spustelėkite **Įrašyti**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastat operacijų kodų ir užsienio prekybos parametrų nustatymas
1. Naršymo srityje eikite į **Moduliai > Mokestis > Konfigūracija > Užsienio prekyba > Operacijų kodai.**
2. Spustelėkite **Naujas**.
3. Lauke **Transaction code**įveskite reikšmę. Pavyzdžiui, kaip operacijos kodą, naudojamą kaip grąžinimas, įveskite **21**.  
4. Lauke **Name** įveskite operacijos kodo pavadinimą. Pvz., įveskite **Return**.  
5. Lauke **Statistical amount**pasirinkite parinktį. Pavyzdžiui, pasirinkite **Empty** – tai nurodo, kad skelbtina operacijų su operacijos kodu **21** statistinė reikšmė visada bus nulis.  
6. Naršymo srityje eikite į **Moduliai > Mokestis > Konfigūracija > Užsienio prekyba > Užsienio prekybos parametrai**.
7. Lauke **Transaction code** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **11**.  
8. Lauke **Credit note** įveskite arba pasirinkite reikšmę. Ši reikšmė taip pat nurodo fizinį grąžinimą. Fizinio grąžinimo kredito pažyma bus perkelta į Intrastat žurnalą su priešinga kryptimi. Pavyzdžiui, gavimo grąžinimas persiunčiamas kaip išsiuntimas.   Priešingu atveju kredito pažyma laikoma taisymu ir persiunčiama su ta pačia kryptimi ir priešingu ženklu. Pavyzdžiui, gavimo taisymas persiunčiamas kaip gavimas su neigiama suma, o aktyvi vėliavėlė nustatoma į **Correction**.  
9. Išplėskite **Transfer** FastTab.
10. Lauke **Items with commodity code** pasirinkite **Yes**. Pasirinkite šią parinktį, kad perkeltumėte tik operacijas su priskirtu prekės kodu. Operacijos be prekės kodo į Intrastat perkeltos nebus.  
11. Lauke **Transfer when meeting criterion for** pasirinkite parinktį. Pavyzdžiui, pasirinkite **One of the selected**.  
12. Išplėskite **Commodity code hierarchy** dalį.
13. Spustelėkite skirtuką **Country/region properties**.
14. Spustelėkite **Naujas**.
15. Lauke **Country/region** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite reikšmę **FRA**.  
16. Lauke **Intrastat code** įveskite šalies ISO kodą.  Pavyzdžiui, įveskite **FR**.  
17. Lauke **Country/region type** pasirinkite **EU**.
18. Spustelėkite skirtuką Numeracijos.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Pristatymo būdų ir išlaidų įtraukimo į Intrastat taisyklių nustatymas
1. Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Konfigūracija > Paskirstymas > Pristatymo režimai**.
2. Sąraše raskite ir pasirinkite norimą įrašą. Pavyzdžiui, pasirinkite **20 Air**.  
3. Išplėskite fastTab **Foreign trade** dalįf
4. Spustelėkite **Redaguoti**.
5. Lauke **Transport**įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **02**.  
6. Pasirinkit **Modules > Accounts receivable > Charges setup > Charges code**.
7. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Išlaidų kodas reikšme **freight**.
8. Išplėskite fastTab **Foreign trade** dalįf
9. Spustelėkite **Redaguoti**.
10. Lauke **Intrastat invoice value** pasirinkite **Yes**. Suma bus perkelta į lauką **Invoice charges** ir susumuota su suma, perkelta į lauką SF suma. Jei keitimų sumą reikia perkelti į lauką **Statistical charges** ir **Statistical amount**, lauke **Intrastat statistical value** pasirinkite **Yes**.  

## <a name="sell-products-for-eu-customers"></a>Produktų pardavimas ES klientams
1. Valdymo skiltyje eikite į **Moduliai >Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Customer account** pasirinkite ES klientą. Pavyzdžiui, pasirinkite **DE-012 Litware Retail**.  
4. Išplėskite **Delivery** FastTab.
5. Lauke **Mode of delivery** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **20 Air**.  
6. Spustelėkite **Gerai**.
7. Pasirinkite pirmąją pardavimo užsakymo eilučių eilutę.
8. Lauke **Item number** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **D001**.  
9. Išplėskite FastTab **Line details**.
10. Spustelėkite skirtuką **Užsienio prekyba**. Transportas automatiškai užpildomas pasirinktu pristatymo būdu.  
11. Lauke **Port** įveskite arba pasirinkite reikšmę.
12. Spustelėkite **Financials**. Pagal parametrus ši suma bus įtraukta į **Intrastat invoice value**.  
13. Spustelėkite **Maintain charges**.
14. Lauke **Charges code** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **FREIGHT**.  
15. Pažymėkite žymės langelį **Keep**.
16. Lauke **Išlaidų vertė** įveskite skaičių. Pavyzdžiui, įveskite **10**.  
17. Spustelėkite **Įrašyti**.
18. Uždarykite puslapį.
19. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
20. Spustelėkite **Sąskaita faktūra**.
21. Išplėskite skyrių **Parameters**.
22. Lauke **Quantity** pasirinkite **All**.
23. Išplėskite **Setup** FastTab.
24. Lauke **SF data** įveskite datą. Pavyzdžiui, įveskit **2015-01-31**.  
25. Spustelėkite **Gerai**.
26. Spustelėkite **Gerai**.
27. Uždarykite puslapį.
28. Spustelėkite **Naujas**.
29. Lauke **Customer account** pasirinkite ES klientą. Pavyzdžiui, pasirinkite **DE-013 Trey Wholesales**.
30. Spustelėkite **Gerai**.
31. Lauke **Item number** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **D0001**.  
32. Spustelėkite **Įrašyti**.
33. Spustelėkite **Sąskaita faktūra**.
34. Lauke **SF data** įveskite datą. Pavyzdžiui, įveskite datą **2015-01-31**.  
35. Spustelėkite **Gerai**.
36. Spustelėkite **Gerai**.

## <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat
1. Naršymo srityje eikite į **Moduliai > Mokestis > Deklaracijos > Užsienio prekyba > Intrastat**.
2. Spustelėkite **Transfer**.
3. Lauke **Customer invoice** pasirinkite **Yes**.
4. Spustelėkite **Filtras**.
5. Sąraše pažymėkite eilutę su **Date**.
6. Lauke **Criteria**surinkite reikšmę. Pavyzdžiui, įveskite 2015 m. sausio laikotarpio filtrą (tiksli reikšmė priklauso nuo jūsų datos formato): 2015-01-01..2015-01-31  
7. Spustelėkite **Gerai**.
8. Spustelėkite **Gerai**.
9. Sąraše raskite ir pasirinkite perkeltą įrašą.
10. Spustelėkite skirtuką **Bendra**.
    
Peržiūrėkite perkeltus duomenis – paskirties / išsiuntimo šalį / regioną, kilmės šalį, svorį, kiekį, kiekį papildomais vienetais, prekę, operacijos kodą, SF sumas ir statistines sumas. Jei reikia, duomenis galite modifikuoti.  

