---
title: Operacijų perkėlimas į Intrastat
description: Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat.
author: AdamTrukawka
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines
- Intrastat, SysQueryForm, DeliveryReason, DeliveryTerms, DestinationCode
ms.openlocfilehash: 5bcb20423b9187df99c0c3078175f4a7d85d78a3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283757"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat

[!include [banner](../../includes/banner.md)]

Šia procedūra parodoma, kaip nustatyti Intrastat parametrus ir perkelti operacijas į Intrastat. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Naujo prekės kodo kūrimas ir esamo naujinimas
1. Pasirinkite **Moduliai > Produkto informacijos valdymas > Nustatymas > Kategorijos ir atributai > Kategorijų hierarchijos**.
2. Sąraše raskite arba pasirinkite įrašą **Intrastat prekių kodai**.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Medyje pasirinkite „įrašas“. Pavyzdžiui, pasirinkite **Intrastat \ Garsiakalbis**.  
5. Spustelėkite **Redaguoti**.
6. Išplėskite „FastTab“ skirtuką **Užsienio prekyba**.
7. Lauke **Papildomi vienetai** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **vnt.**  
8. Lauke **Svoris netaikomas** pasirinkite **Taip**.
9. Medyje pasirinkite **Intrastat**.
10. Spustelėkite **Naujas kategorijos mazgas**.
11. Lauke **Pavadinimas** įveskite prekės pavadinimą. Pavyzdžiui, įveskite **Kita prekė**.  
12. Lauke **Kodas** įveskite prekės kodą. Pavyzdžiui, įveskite **995 00 00**.  
13. Lauke „Patogus pavadinimas“ įveskite reikšmę. Pavyzdžiui, įveskite **Kiti**.  
14. Spustelėkite **Įrašyti**.
15. Uždarykite puslapį.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Prekės kodo priskyrimas produktų hierarchijai ir išleistam produktui
1. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pavyzdžiui, filtruokite lauką **Pavadinimas**, kurio reikšmė **pardavimas**.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Medyje išplėskite **kategorijos mazgas**. Pavyzdžiui, išplėskite **Pardavimo hierarchija \ Namų garso sistema**.  
4. Medyje pasirinkite **prekės kodui priskirtina kategorija**. Pavyzdžiui, pasirinkite **Pardavimo hierarchija \ Namų garso sistema \ Garsiakalbiai.  
5. Išplėskite „FastTab“ skirtuką **Prekių kodai**.
6. Spustelėkite **Pridėti**.
7. Lauke **Pasirinkti hierarchiją** pasirinkite **Intrastat**.
8. Sąraše raskite ir pasirinkite prekės kodą. Pavyzdžiui, pasirinkite **920 20 34 \ Garsiakalbis**.  
9. Spustelėkite rodyklę, kad pasirinktumėte tiekėją.
10. Spustelėkite **Gerai**.
11. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
12. Sąraše pasirinkite išleistą produktą, kurį priskirsite prekės kodui. Pavyzdžiui, pasirinkite **D0001**.  
13. Spustelėkite **Redaguoti**.
14. Išplėskite fastTab **Užsienio prekyba** dalįf
15. Lauke **Prekė** įveskite prekės kodą. Pavyzdžiui, pasirinkite reikšmę **920 20 34 \ Garsiakalbis**.    
16. Lauke **Išlaidos procentais** įveskite skaičių. Pavyzdžiui, įveskite **3**.  
17. Lauke **Šalis / regionas** įveskite arba pasirinkite kilmės šalį arba regioną. Pavyzdžiui, pasirinkite **AUT**.  
18. Išplėskite „FastTab“ skirtuką **Valdyti atsargas**.
19. Lauke **Grynasis svoris** įveskite svorį kilogramais. Pavyzdžiui, įveskite **2,5**.  
20. Spustelėkite **Įrašyti**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastat operacijų kodų ir užsienio prekybos parametrų nustatymas
1. Naršymo srityje eikite į **Moduliai > Mokestis > Konfigūracija > Užsienio prekyba > Operacijų kodai.**
2. Spustelėkite **Naujas**.
3. Lauke **Operacijos kodas** įveskite reikšmę. Pavyzdžiui, kaip operacijos kodą, naudojamą kaip grąžinimas, įveskite **21**.  
4. Lauke **Pavadinimas** įveskite operacijos kodo pavadinimą. Pavyzdžiui, įveskite **Grąžinti**.  
5. Lauke **Statistinė suma** pasirinkite parinktį. Pavyzdžiui, pasirinkite **Tuščia** – tai nurodo, kad skelbtina operacijų su operacijos kodu **21** statistinė reikšmė visada bus nulis.  
6. Naršymo srityje eikite į **Moduliai > Mokestis > Konfigūracija > Užsienio prekyba > Užsienio prekybos parametrai**.
7. Lauke **Operacijos kodas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **11**.  
8. Lauke **Kredito pažyma** įveskite arba pasirinkite reikšmę. Ši reikšmė taip pat nurodo fizinį grąžinimą. Fizinio grąžinimo kredito pažyma bus perkelta į Intrastat žurnalą su priešinga kryptimi. Pavyzdžiui, gavimo grąžinimas persiunčiamas kaip išsiuntimas.   Priešingu atveju kredito pažyma laikoma taisymu ir persiunčiama su ta pačia kryptimi ir priešingu ženklu. Pavyzdžiui, gavimo taisymas persiunčiamas kaip gavimas su neigiama suma, o aktyvi vėliavėlė nustatoma į **Koregavimas**.  
9. Išplėskite „FastTab“ skirtuką **Perkelti**.
10. Lauke **Prekės su prekės kodu** pasirinkite **Taip**. Pasirinkite šią parinktį, kad perkeltumėte tik operacijas su priskirtu prekės kodu. Operacijos be prekės kodo į Intrastat perkeltos nebus.  
11. Lauke **Perduoti, kai atitinka kriterijai** pasirinkite parinktį. Pavyzdžiui, pasirinkite **Vienas iš pasirinktų**.  
12. Išplėskite sekciją **Prekių kodų hierarchija**.
13. Spustelėkite skirtuką **Šalies / regiono ypatybės**.
14. Spustelėkite **Naujas**.
15. Lauke **Šalis / regionas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite reikšmę **FRA**.  
16. Lauke **Intrastat kodas** įveskite šalies ISO kodą.  Pavyzdžiui, įveskite **FR**.  
17. Lauke **Šalies / regiono tipas** pasirinkite **EU**.
18. Spustelėkite skirtuką Numeracijos.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Pristatymo būdų ir išlaidų įtraukimo į Intrastat taisyklių nustatymas
1. Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Konfigūracija > Paskirstymas > Pristatymo režimai**.
2. Sąraše raskite ir pasirinkite norimą įrašą. Pavyzdžiui, pasirinkite **20 Air**.  
3. Išplėskite fastTab **Užsienio prekyba** dalįf
4. Spustelėkite **Redaguoti**.
5. Lauke **Transportas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **02**.  
6. Pasirinkite **Moduliai > Gautinos sumos > Išlaidų sąranka > Išlaidų kodas**.
7. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Išlaidų kodas reikšme **transportavimas**.
8. Išplėskite fastTab **Užsienio prekyba** dalįf
9. Spustelėkite **Redaguoti**.
10. Lauke **Intrastat sąskaitos faktūros vertė** pasirinkite **Taip**. Suma bus perkelta į lauką **SF išlaidos** ir susumuota su suma, perkelta į lauką SF suma. Jei keitimų sumą reikia perkelti į lauką **Statistinės išlaidos** ir **Statistinė suma**, lauke **Intrastat statistinė vertė** pasirinkite **Taip**.  

## <a name="sell-products-for-eu-customers"></a>Produktų pardavimas ES klientams
1. Valdymo skiltyje eikite į **Moduliai >Gautinos sumos > Užsakymai > Visi pardavimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Kliento sąskaita** pasirinkite ES klientą. Pavyzdžiui, pasirinkite **DE-012 Litware Retail**.  
4. Išplėskite „FastTab“ skirtuką **Pristatymas**.
5. Lauke **Pristatymo būdas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **20 Air**.  
6. Spustelėkite **Gerai**.
7. Pasirinkite pirmąją pardavimo užsakymo eilučių eilutę.
8. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **D001**.  
9. Išplėskite FastTab **Eilutės informacija**.
10. Spustelėkite skirtuką **Užsienio prekyba**. Transportas automatiškai užpildomas pasirinktu pristatymo būdu.  
11. Lauke **Uostas** įveskite arba pasirinkite reikšmę.
12. Spustelėkite **Finansai**. Pagal parametrus ši suma bus įtraukta į **Intrastat sąskaitos faktūros vertė**.  
13. Spustelėkite **Prižiūrėti išlaidas**.
14. Lauke **Išlaidų kodas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **TRANSPORTAVIMAS**.  
15. Pažymėkite žymės langelį **Išsaugoti**.
16. Lauke **Išlaidų vertė** įveskite skaičių. Pavyzdžiui, įveskite **10**.  
17. Spustelėkite **Įrašyti**.
18. Uždarykite puslapį.
19. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
20. Spustelėkite **Sąskaita faktūra**.
21. Išplėskite skyrių **Parametrai**.
22. Lauke **Kiekis** pasirinkite **Visi**.
23. Išplėskite „FastTab“ skirtuką **Sąranka**.
24. Lauke **SF data** įveskite datą. Pavyzdžiui, įveskite **2015-01-31**.  
25. Spustelėkite **Gerai**.
26. Spustelėkite **Gerai**.
27. Uždarykite puslapį.
28. Spustelėkite **Naujas**.
29. Lauke **Kliento sąskaita** pasirinkite ES klientą. Pavyzdžiui, pasirinkite **DE-013 „Trey“ didmeninė prekyba**.
30. Spustelėkite **Gerai**.
31. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Pavyzdžiui, pasirinkite **D0001**.  
32. Spustelėkite **Įrašyti**.
33. Spustelėkite **Sąskaita faktūra**.
34. Lauke **SF data** įveskite datą. Pavyzdžiui, įveskite datą **2015-01-31**.  
35. Spustelėkite **Gerai**.
36. Spustelėkite **Gerai**.

## <a name="transfer-transactions-to-the-intrastat"></a>Operacijų perkėlimas į Intrastat
1. Naršymo srityje eikite į **Moduliai > Mokestis > Deklaracijos > Užsienio prekyba > Intrastat**.
2. Spustelėkite **Perkelti**.
3. Lauke **Kliento SF** pasirinkite **Taip**.
4. Spustelėkite **Filtras**.
5. Sąraše pažymėkite eilutę su **Data**.
6. Lauke **Kriterijai** surinkite reikšmę. Pavyzdžiui, įveskite 2015 m. sausio laikotarpio filtrą (tiksli reikšmė priklauso nuo jūsų datos formato): 2015-01-01..2015-01-31  
7. Spustelėkite **Gerai**.
8. Spustelėkite **Gerai**.
9. Sąraše raskite ir pasirinkite perkeltą įrašą.
10. Spustelėkite skirtuką **Bendra**.
    
Peržiūrėkite perkeltus duomenis – paskirties / išsiuntimo šalį / regioną, kilmės šalį, svorį, kiekį, kiekį papildomais vienetais, prekę, operacijos kodą, SF sumas ir statistines sumas. Jei reikia, duomenis galite modifikuoti.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
