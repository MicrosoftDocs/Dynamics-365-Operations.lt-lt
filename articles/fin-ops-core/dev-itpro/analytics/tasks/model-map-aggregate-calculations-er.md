---
title: Modelio susiejimo konfigūracijų naudojimas agreguotiems skaičiavimams duomenų bazės lygiu
description: Naudojant šią procedūrą pateikiama informacija apie tai, kaip sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0912b620fc70f8ed33e336da9ecefacd1f4e376e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143182"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Modelio susiejimo konfigūracijų naudojimas agreguotiems skaičiavimams duomenų bazės lygiu

[!include [banner](../../includes/banner.md)]

Naudojant šią procedūrą pateikiama informacija apie tai, kaip sukurti naują elektroninių ataskaitų (ER) modelio susiejimo konfigūraciją ir, siekiant efektyviai sutelkti skaičiavimus, naudoti integruotas ER funkcijas. Šioje procedūroje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. 

Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas. Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.

 Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „ER pagerina agreguotų skaičiavimų efektyvumą juos atliekant duomenų bazės lygmeniu (1 dalis. Konfigūracijų parengimas)“ veiksmus.

1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat“ modelis.
3. Medyje pasirinkite „Intrastat model\Intrastat sample mapping“ (Intrastat modelis\Intrastat pavyzdinis susiejimas).
4. Spustelėkite Konstruktorius.
5. Spustelėkite Konstruktorius.
6. Medyje pasirinkite Dynamics 365 for Operations\Table records.
7. Spustelėkite „Įtraukti šaknį“.
    * Įtraukite naują duomenų šaltinį, apimantį norimus grupuoti įrašus.  
8. Lauke „Pavadinimas“, įveskite „Operacijos“.
    * Operacijos  
9. Lauke Lentelė, įveskite „Intrastat“.
    * Intrastat  
10. Spustelėkite GERAI.
11. Medyje pasirinkite Funkcijos\Grupuoti pagal.
    * Šis duomenų šaltinio tipas naudojamas norint vykdymo metu į grupės įrašus įtraukti naują duomenų šaltinį ir apskaičiuoti reikiamus telkimus.  
12. Spustelėkite „Įtraukti šaknį“.
13. Lauke Pavadinimas įveskite „TransactionsGroups“ (operacijų grupės).
    * TransactionsGroups  
14. Spustelėkite Redaguoti grupę pagal.
15. Medyje pasirinkite „Operacijos“.
    * Pasirinkite „Įrašų sąrašas“ tipo, kuris žymi duomenis, kuriuos norite grupuoti, pridėtus duomenų šaltinius.  
16. Spustelėkite Įtraukti lauką į.
17. Spustelėkite Ką grupuoti.
18. Medyje išplėskite „Operacijos“.
19. Medyje pasirinkite „Operacijos\Kryptis“.
20. Spustelėkite Įtraukti lauką į.
21. Spustelėkite Sugrupuoti laukai.
    * Pasirinkę lauką nurodykite grupavimo lygį. Pagal šią pasirinktį, duomenų šaltinis vykdymo metu grąžina tiek operacijų grupių, kiek yra Intrastat lentelėje sutinkamų krypčių kodų.  
22. Medyje pasirinkite „Operacijos\SF suma(MSTSuma)“.
    * Pasirinkite lauką, kad galėtumėte nurodyti telkimo skaičiavimo šaltinį.  
23. Spustelėkite Įtraukti lauką į.
24. Spustelėkite Telkimo laukai.
25. Sąraše pažymėkite pasirinktą eilutę.
26. Lauke Metodas pasirinkite „Sum“ (suma).
    * Pasirinkite telkimo tipą.  
27. Lauke Pavadinimas įveskite „SumOfAmountMST“ (bendroji MST suma).
    * Nurodykite šio telkimo pavadinimą sukonfigūruotame duomenų šaltinyje.  
28. Spustelėkite Įrašyti.
    * Atkreipkite dėmesį, kad lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo metu SQL duomenų bazėje.  
29. Uždarykite puslapį.
30. Spustelėkite GERAI.
31. Medyje išplėskite „Totals“ (bendrosios sumos).
32. Medyje išplėskite „TransactionsGroups“ (operacijų grupės).
33. Medyje išplėskite „OperacijųGrupės\susietos“.
34. Medyje pasirinkite „OperacijųGrupės\susietos\BendrojiMSTsuma“.
35. Medyje pasirinkite „Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')“.
36. Spustelėkite Susieti.
    * Pagal šį parametrą, šis duomenų šaltinis skaičiuos kiekvienos operacijų grupės lauko „AmountMST“ verčių sumą. Šis telkimo skaičiavimas bus pasiekiamas kaip elementas TransactionsGroups.aggregated.TotalAmount.  
37. Medyje išplėskite „TransactionsGroups“ (operacijų grupės).
38. Medyje pasirinkite „TransactionsGroups“ (operacijų grupės).
39. Spustelėkite Redaguoti.
40. Spustelėkite Redaguoti grupę pagal.
41. Medyje išplėskite „Operacijos“.
42. Medyje pasirinkite „Operacijos\SF suma(MSTSuma)“.
43. Spustelėkite Įtraukti lauką į.
44. Spustelėkite Telkimo laukai.
45. Sąraše pažymėkite pasirinktą eilutę.
46. Lauke Metodas pasirinkite „Max“ (maksimalus).
47. Lauke Pavadinimas įveskite „MaxOfAmountMST“ (maksimali MST suma).
48. Spustelėkite Įrašyti.
    * Šiuo metu GROUPBY duomenų šaltinių vykdymas gali būti konvertuotas į SQL duomenų bazės lygį taikant tam tikrus apribojimus. Galima atlikti tipo „Įrašų sąrašas“ duomenų šaltinių arba kaip išraiška pateikiamų duomenų šaltinių konvertavimą naudojant funkciją FILTRAS. Tai taip pat galima atlikti, kai sukonfigūruotas tik vienas vieno grupavimo įrašų lauko telkimas.  
    * Atkreipkite dėmesį, kad, nors sukonfigūruotas daugiau nei vienas lauko AmountMST telkimas, lauke „Vykdymas“ vis tiek nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku SQL duomenų bazėje. Taip yra todėl, kad su duomenų modelio elementu susietas tik vienas telkimas, kuris bus naudojamas vykdymo laiku norint ištraukti duomenis iš šio duomenų šaltinio.  
49. Uždarykite puslapį.
50. Spustelėkite GERAI.
51. Medyje išplėskite „TransactionsGroups“ (operacijų grupės).
52. Medyje išplėskite „OperacijųGrupės\susietos“.
53. Medyje pasirinkite „TransactionsGroups\aggregated\MaxOfAmountMST“ (operacijų grupės\susietos\maksimali MST suma).
54. Medyje pasirinkite „Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')“.
55. Spustelėkite Susieti.
56. Medyje išplėskite „TransactionsGroups“ (operacijų grupės).
57. Medyje pasirinkite „TransactionsGroups“ (operacijų grupės).
58. Spustelėkite Redaguoti.
59. Spustelėkite Redaguoti grupę pagal.
    * Atkreipkite dėmesį, lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku atmintyje, nes abu to paties lauko telkimai susieti su duomenų modelio elementais.   
60. Pažymėkite arba atžymėkite visas sąrašo eilutes.
61. Spustelėkite Naikinti.
62. Spustelėkite Taip.
63. Spustelėkite Naikinti.
64. Spustelėkite Taip.
65. Spustelėkite Įtraukti lauką į.
66. Spustelėkite Ką grupuoti.
67. Medyje išplėskite „Commodity record(Intrastat)“.
68. Spustelėkite Įrašyti.
    * Atkreipkite dėmesį, kad lauke „Vykdymas“ nurodoma, kad šis grupavimas bus atliekamas vykdymo laiku atmintyje, nors nėra nurodytų telkimų, o pasirinktas tipo „Lentelės įrašai“ duomenų šaltinis paremtas ta pačia „Intrastat“ lentele. Taip yra todėl, kad duomenų šaltinyje yra keletas apskaičiuotų laukų, kurie dar negali būti konvertuoti į SQL duomenų bazės lygį.  

