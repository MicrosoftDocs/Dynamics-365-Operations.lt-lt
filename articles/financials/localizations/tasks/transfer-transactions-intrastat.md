---
title: Operacijų perkėlimas į Intrastat
description: Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13cc9dc2119ad3dc85d580e92edee7bb9ef2075c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559324"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Naujo prekės kodo kūrimas ir esamo naujinimas
1. Pasirinkite Produkto informacijos valdymas > Nustatymas > Kategorijos ir atributai > Kategorijų hierarchijos.
2. Sąraše raskite arba pasirinkite įrašą Intrastat prekių kodai.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Medyje pasirinkite „įrašas‟.
    * Pavyzdžiui, pasirinkite Intrastat \ Garsiakalbis.  
5. Spustelėkite Redaguoti.
6. Išplėskite dalį Užsienio prekyba.
7. Lauke Papildomi vienetai įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite „vnt.‟.  
8. Lauke Svoris netaikomas pasirinkite Taip.
9. Medyje pasirinkite Intrastat.
10. Spustelėkite „Naujas kategorijos mazgas“.
11. Lauke Pavadinimas įveskite prekės pavadinimą.
    * Pavyzdžiui, įveskite „Kita prekė‟.  
12. Lauke Kodas įveskite prekės kodą.
    * Pavyzdžiui, įveskite „995 00 00‟.  
13. Lauke „Patogus pavadinimas“ įveskite reikšmę.
    * Pavyzdžiui, įveskite „Kita‟.  
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Prekės kodo priskyrimas produktų hierarchijai ir išleistam produktui
1. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Pavadinimas reikšme „pardavimas“.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Medyje išplėskite „kategorijos mazgas‟.
    * Pavyzdžiui, išplėskite Pardavimo hierarchija \ Namų garso sistema.  
4. Medyje pasirinkite „prekės kodui priskirtina kategorija‟.
    * Pavyzdžiui, pasirinkite Pardavimo hierarchija \ Namų garso sistema \ Garsiakalbiai.  
5. Išplėskite dalį Prekių kodai.
6. Spustelėkite Pridėti.
7. Lauke Pasirinkti hierarchiją pasirinkite „Intrastat‟.
8. Sąraše raskite ir pasirinkite prekės kodą.
    * Pavyzdžiui, pasirinkite 920 20 34 \ Garsiakalbis.  
9. Spustelėkite Pasirinkti kodus.
10. Spustelėkite GERAI.
11. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
12. Sąraše pasirinkite išleistą produktą, kurį priskirsite prekės kodui.
    * Pavyzdžiui, pasirinkite D0001.  
13. Spustelėkite Redaguoti.
14. Išplėskite dalį Užsienio prekyba.
15. Lauke Prekė įveskite prekės kodą.
    * Pavyzdžiui, pasirinkite reikšmę 920 20 34 Garsiakalbis.    
16. Lauke Išlaidų procentas įveskite skaičių.
    * Pvz., įveskite „3‟.  
17. Lauke Šalis / regionas įveskite arba pasirinkite kilmės šalį arba regioną.
    * Pavyzdžiui, pasirinkite AUT.  
18. Išplėskite dalį Valdyti atsargas.
19. Lauke Grynasis svoris įveskite svorį kilogramais.
    * Pvz., įveskite „2,5‟.  
20. Spustelėkite Įrašyti.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastat operacijų kodų ir užsienio prekybos parametrų nustatymas
1. Pasirinkite Mokesčiai > Nustatymas > Užsienio prekyba > Operacijų kodai.
2. Spustelėkite Naujas.
3. Lauke Operacijos kodas įveskite reikšmę.
    * Pavyzdžiui, kaip operacijos kodą, naudojamą kaip grąžinimas, įveskite „21‟.  
4. Lauke Pavadinimas įveskite operacijos kodo pavadinimą.
    * Pvz., įveskite „Grąžinimas‟.  
5. Lauke Statistinė suma pasirinkite parinktį.
    * Pavyzdžiui, pasirinkite Tuščia – tai nurodo, kad skelbtina operacijų su operacijos kodu „21‟ statistinė reikšmė visada bus nulis.  
6. Pasirinkite Mokesčiai > Nustatymai > Užsienio prekyba > Užsienio prekybos parametrai.
7. Lauke Operacijos kodas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite 11.  
8. Lauke Kredito pažyma įveskite arba pasirinkite reikšmę.
    * Ši reikšmė taip pat nurodo fizinį grąžinimą. Fizinio grąžinimo kredito pažyma bus perkelta į Intrastat žurnalą su priešinga kryptimi. Pavyzdžiui, gavimo grąžinimas persiunčiamas kaip išsiuntimas.   Priešingu atveju kredito pažyma laikoma taisymu ir persiunčiama su ta pačia kryptimi ir priešingu ženklu. Pavyzdžiui, gavimo taisymas persiunčiamas kaip gavimas su neigiama suma, o aktyvi vėliavėlė nustatoma į „Taisymas“.  
9. Išplėskite dalį Perkėlimas.
10. Lauke Prekės su prekės kodu pasirinkite Taip.
    * Pasirinkite šią parinktį, kad perkeltumėte tik operacijas su priskirtu prekės kodu. Operacijos be prekės kodo į Intrastat perkeltos nebus.  
11. Lauke Perduoti, kai atitinka kriterijai pasirinkite parinktį.
    * Pavyzdžiui, pasirinkite Vienas iš pasirinktų.  
12. Išplėskite dalį Prekių kodų hierarchija.
13. Spustelėkite skirtuką Šalies / regiono ypatybės.
14. Spustelėkite Naujas.
15. Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite reikšmę FRA.  
16. Lauke Intrastat kodas įveskite šalies ISO kodą.
    * Pavyzdžiui, įveskite „FR‟.  
17. Lauke Šalies / regiono tipas pasirinkite „ES“.
18. Spustelėkite skirtuką Numeracijos.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Pristatymo būdų ir išlaidų įtraukimo į Intrastat taisyklių nustatymas
1. Pasirinkite Pardavimas ir rinkodara > Nustatymas > Platinimas > Pristatymo būdai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pavyzdžiui, pasirinkite 20 Air.  
3. Išplėskite dalį Užsienio prekyba.
4. Spustelėkite Redaguoti.
5. Lauke Transportavimas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite 02.  
6. Pasirinkite Gautinos sumos > Išlaidų nustatymas > Išlaidų kodas.
7. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Išlaidų kodas reikšme „transportavimas‟.
8. Išplėskite dalį Užsienio prekyba.
9. Spustelėkite Redaguoti.
10. Lauke Intrastat sąskaitos faktūros vertė pasirinkite Taip.
    * Suma bus perkelta į lauką SF išlaidos ir susumuota su suma, perkelta į lauką SF suma.    Jei keitimų sumą reikia perkelti į lauką Statistinės išlaidos ir susumuoti su statistine suma, lauke Intrastat statistinė reikšmė pasirinkite Taip.  

## <a name="sell-products-for-eu-customers"></a>Produktų pardavimas ES klientams
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita pasirinkite ES klientą.
    * Pavyzdžiui, pasirinkite DE-012 „Litware Retail‟.  
4. Išplėskite dalį Pristatymas.
5. Lauke Pristatymo būdas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite 20 Air.  
6. Spustelėkite GERAI.
7. Perkelkite žymeklį ant pirmosios pardavimo užsakymo eilučių eilutės.
8. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite D001.  
9. Išplėskite skyrių Eilutės informacija.
10. Spustelėkite skirtuką Užsienio prekyba.
    * Transportavimas užpildomas automatiškai pagal pasirinktą pristatymo būdą.  
11. Lauke Uostas įveskite arba pasirinkite reikšmę.
12. Spustelėkite Finansai.
    * Pagal parametrus ši suma bus įtraukta į Intrastat sąskaitos faktūros vertę.  
13. Spustelėkite Prižiūrėti išlaidas.
14. Lauke Išlaidų kodas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite TRANSPORTAVIMAS.  
15. Pažymėkite žymės langelį Laikyti.
16. Lauke Išlaidų vertė įveskite skaičių.
    * Pvz., įveskite „10‟.  
17. Spustelėkite Įrašyti.
18. Uždarykite puslapį.
19. Veiksmų srityje spustelėkite Sąskaita faktūra.
20. Spustelėkite Sąskaita faktūra.
21. Išplėskite skyrių Parametrai.
22. Lauke Kiekis pasirinkite Visi.
23. Išplėskite skyrių Nustatymas.
24. Įveskite datą lauke Sąskaitos faktūros data.
    * Pavyzdžiui, įveskite „2015-01-31‟.  
25. Spustelėkite GERAI.
26. Spustelėkite GERAI.
27. Uždarykite puslapį.
28. Spustelėkite Naujas.
29. Lauke Kliento sąskaita pasirinkite ES klientą.
    * Pavyzdžiui, pasirinkite DE-013 „Trey‟ didmeninė prekyba  
30. Spustelėkite GERAI.
31. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite D0001.  
32. Spustelėkite Įrašyti.
33. Spustelėkite Sąskaita faktūra.
34. Įveskite datą lauke Sąskaitos faktūros data.
    * Pavyzdžiui, įveskite datą „2015-01-31‟.  
35. Spustelėkite GERAI.
36. Spustelėkite GERAI.

## <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat
1. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
2. Spustelėkite Perkelti.
3. Lauke Kliento SF pasirinkite Taip.
4. Spustelėkite Filtras.
5. Sąraše pažymėkite eilutę su Data.
6. Lauke Kriterijai surinkite reikšmę.
    * Pavyzdžiui, įveskite 2015 m. sausio laikotarpio filtrą (tiksli reikšmė priklauso nuo jūsų datos formato): 2015-01-01..2015-01-31  
7. Spustelėkite GERAI.
8. Spustelėkite GERAI.
9. Sąraše raskite ir pasirinkite perkeltą įrašą.
10. Spustelėkite skirtuką Bendra.
    * Peržiūrėkite perkeltus duomenis – paskirties / išsiuntimo šalį / regioną, kilmės šalį, svorį, kiekį, kiekį papildomais vienetais, prekę, operacijos kodą, SF sumas ir statistines sumas.   Jei reikia, duomenis galite modifikuoti.  

