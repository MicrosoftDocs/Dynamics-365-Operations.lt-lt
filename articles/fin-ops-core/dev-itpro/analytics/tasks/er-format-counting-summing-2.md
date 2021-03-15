---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (2 dalis – Skaičiavimų konfigūravimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (2 dalis)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093002"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (2 dalis – Skaičiavimų konfigūravimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (1 dalis. Formato kūrimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Formato konfigūracijos kūrimas, norint įtraukti skaičiavimo ir sumavimo informaciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išplėskite „Intrastat“ modelis.
4. Medyje pasirinkite Intrastat model\Intrastat (DE).
    * Tarkime, kad norite tinkinti formatą, kurį teikia „Microsoft“, „Intrastat“ ataskaitos gale įtraukdami eilutes su suvestinės informacija. Tai galite atlikti, savo „Intrastat“ konfigūracijos egzempliorių išvesdami iš „Microsoft“ egzemplioriaus, kad galėtumėte atlikti keitimus.  
5. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
6. Lauke Naujas įveskite Kildinti iš pavadinimo: „Intrastat“ (DE), „Microsoft“.
7. Lauke Pavadinimas įveskite Intrastat (DE) be skaičiavimo ir sumavimo.
8. Spustelėkite Sukurti konfigūraciją.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Šios ataskaitos konfigūravimas, norint skaičiavimo ir sumavimo veiksmus atlikti pagal išvesties informaciją
1. Spustelėkite Konstruktorius.
2. Lauke Rinkti išeigos informaciją pasirinkite Taip.
    * Pažymėjus šią žymą, vykdymo metu bus suaktyvintas „Intrastat“ failo generavimo išvesties informacijos rinkimo procesas.  
    * Turite atlikti skirtingų „Intrastat“ krypčių skaičiavimus, todėl skirtąjį modelių išvardijimą turite įtraukti į šios formato konfigūracijos duomenų šaltinių sąrašą.  
3. Spustelėkite skirtuką „Susiejimas“.
4. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
5. Medyje pasirinkite Data model\Enumeration.
6. Lauke Pavadinimas įveskite Kryptis.
7. Lauke Modelių išvardijimas įveskite arba pasirinkite reikšmę.
    * Pasirinkite reikšmę Kryptis.  
8. Spustelėkite GERAI.
9. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
10. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
11. Lauke Pavadinimas įveskite $BlockName.
12. Spustelėkite „Redaguoti formulę“.
13. Lauke Formulė įveskite blokas.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.
16. Spustelėkite GERAI.
17. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
18. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
19. Lauke Pavadinimas įveskite $RecName.
20. Spustelėkite „Redaguoti formulę“.
21. Lauke Formulė įveskite įrašas.
22. Spustelėkite Įrašyti.
23. Uždarykite puslapį.
24. Spustelėkite GERAI.
25. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
26. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
27. Lauke Pavadinimas įveskite $InvName.
28. Spustelėkite „Redaguoti formulę“.
29. Lauke Formulė įveskite InvoicedAmountEUR.
30. Spustelėkite Įrašyti.
31. Uždarykite puslapį.
32. Spustelėkite GERAI.
33. Medyje pasirinkite Intrastat\Data.
34. Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti
35. Spustelėkite „Įtraukti duomenų šaltinį“.
    * $BlockName  
36. Spustelėkite Įrašyti.
37. Uždarykite puslapį.
38. Spustelėkite lauko Surinktų duomenų rakto reikšmė mygtuką Redaguoti.
39. Lauke Formulė įveskite IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Spustelėkite Įrašyti.
41. Uždarykite puslapį.
    * Suskaičiuokite šios sekos eilutes. Rezultatai, pavadinimu „blokas“, bus atskirai naudojami skirtingoms kryptims. Reikšmė „Importuoti“ bus naudojama visoms „Intrastat“ gavimų operacijoms. Reikšmė „Eksportuoti“ bus naudojama visoms „Intrastat“ išsiuntimų operacijoms. Tai gali būti laikoma virtualia „Excel“ skaičiuokle. Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“.  
42. Medyje išplėskite dalį Intrastat\Data: Sequence.
43. Medyje pasirinkite Intrastat\Data: Sequence\Arrivals?.
44. Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.
    * Suskaičiuokite šios sekos eilutes. Rezultatai bus išsaugoti naudojant pavadinimą „įrašas“.  
45. Medyje pasirinkite $RecName.
46. Spustelėkite „Įtraukti duomenų šaltinį“.
47. Spustelėkite Įrašyti.
48. Uždarykite puslapį.
49. Spustelėkite lauko „Surinktų duomenų rakto reikšmė“ mygtuką Redaguoti
50. Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.
51. Spustelėkite Įrašyti.
52. Uždarykite puslapį.
    * Suskaičiuokite šios sekos eilutes. Rezultatai, pavadinimu „įrašas“, bus atskirai naudojami skirtingiems prekių kodams. Tai gali būti laikoma virtualia „Excel“ skaičiuokle. Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“, o antrasis blokas, pavadinimu „įrašas“, užpildytas prekės kodo reikšme.  
53. Medyje pasirinkite Intrastat\Data: Sequence\Dispatches?.
54. Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti
55. Medyje pasirinkite $RecName.
56. Spustelėkite „Įtraukti duomenų šaltinį“.
57. Spustelėkite Įrašyti.
58. Uždarykite puslapį.
59. Spustelėkite lauko „Surinktų duomenų rakto reikšmė“ mygtuką Redaguoti.
60. Lauke Formulė įveskite Intrastat.CommodityRecord.CommodityCode.
61. Spustelėkite Įrašyti.
62. Uždarykite puslapį.
63. Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?.
64. Medyje išplėskite dalį Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord.
65. Spustelėkite skirtuką Formatas.
66. Medyje pasirinkite Intrastat\Data\Dispatches\Record\Invoice amount EUR.
67. Spustelėkite skirtuką „Susiejimas“.
68. Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.
69. Medyje pasirinkite $InvName.
70. Spustelėkite „Įtraukti duomenų šaltinį“.
71. Spustelėkite Įrašyti.
72. Uždarykite puslapį.
    * Susumuokite šios sekos eilučių SF sumos reikšmes. Rezultatai, pavadinimu „InvoicedAmountEUR“, bus naudojami skirtingoms „Intrastat“ kryptims ir prekių kodams. Tai gali būti laikoma virtualiai sukurtu elementu „Excel“ skaičiuoklėje. Kiekvienos operacijos eilutė, kurios pirmasis stulpelis yra „blokas“, užpildytas atitinkamomis reikšmėmis „Importuoti“ ir „Eksportuoti“. Antrasis blokas, pavadinimu „įrašas“, užpildomas prekės kodo reikšme, o trečiasis stulpelis, pavadinimu „InvoicedAmountEUR“, užpildomas SF sumos reikšme.  
73. Medyje išplėskite dalį Intrastat\Data\Arrivals?.
74. Medyje išplėskite dalį Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord.
75. Spustelėkite skirtuką Formatas.
76. Medyje pasirinkite Intrastat\Data\Arrivals\Record\Invoice amount EUR.
77. Spustelėkite skirtuką „Susiejimas“.
78. Spustelėkite lauko „Surinktų duomenų rakto pavadinimas“ mygtuką Redaguoti.
79. Medyje pasirinkite $InvName.
80. Spustelėkite „Įtraukti duomenų šaltinį“.
81. Spustelėkite Įrašyti.
82. Uždarykite puslapį.
83. Spustelėkite Įrašyti.
84. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]