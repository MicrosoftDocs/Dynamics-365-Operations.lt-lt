---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis – Skaičiavimų naudojimas išvesčiai kurti)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (3 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749002"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (3 dalis – Skaičiavimų naudojimas išvesčiai kurti)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (2 dalis. Skaičiavimų konfigūravimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Šios ataskaitos konfigūravimas, norint naudoti skaičiavimo ir sumavimo informaciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išplėskite „Intrastat“ modelis.
4. Medyje išplėskite dalį Intrastat model\Intrastat (DE).
5. Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. Spustelėkite Konstruktorius.
7. Spustelėkite skirtuką „Susiejimas“.
8. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
    * Įtraukite naują duomenų šaltinį, norėdami gauti išsaugotų blokų sąrašą.  
9. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
10. Lauke Pavadinimas įveskite $BlocksList.
    * $BlocksList  
11. Spustelėkite „Redaguoti formulę“.
12. Medyje pasirinkite Data collection functions\COLLECTEDLIST.
13. Spustelėkite „Įtraukti funkciją“.
14. Spustelėkite „Įtraukti duomenų šaltinį“.
15. Lauke Formulė įveskite COLLECTEDLIST('$BlockName', .
    * COLLECTEDLIST('$BlockName',  
16. Lauke Formulė įveskite COLLECTEDLIST('$BlockName', "*").
    * COLLECTEDLIST('$BlockName', "*")  
17. Spustelėkite Įrašyti.
    * Simbolis „*“ nurodo, kad visi blokai bus įtraukti į šio įrašo sąrašą.  
18. Uždarykite puslapį.
19. Spustelėkite GERAI.
20. Spustelėkite skirtuką Formatas.
21. Medyje pasirinkite Intrastat\Data.
22. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
23. Medyje pasirinkite Text\Sequence.
24. Lauke Pavadinimas, įveskite Bendrosios sumos pagal blokus.
    * Bendrosios sumos pagal blokus  
25. Lauke Specialieji simboliai pasirinkite Nauja eilutė – „Windows“ (CR LF).
26. Spustelėkite Gerai.
27. Medyje pasirinkite Intrastat\Data\Totals by blocks.
28. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
29. Medyje pasirinkite „Tekstas \ Eilutė‟.
30. Lauke Pavadinimas įveskite Bloko kodas.
    * Bloko kodas  
31. Spustelėkite GERAI.
32. Spustelėkite Įtraukti eilutę.
33. Lauke Pavadinimas įveskite Eilučių skaičiavimas.
    * Eilučių skaičiavimas  
34. Spustelėkite GERAI.
35. Spustelėkite Įtraukti eilutę.
36. Lauke Pavadinimas įveskite Bendroji suma.
    * Bendra suma  
37. Spustelėkite GERAI.
38. Spustelėkite skirtuką „Susiejimas“.
39. Medyje pasirinkite $BlocksList.
40. Spustelėkite Susieti.
    * Kurkite kiekvieno išsaugoto bloko suvestinės eilutę.  
41. Spustelėkite skirtuką Formatas.
42. Medyje pasirinkite Intrastat\Data\Totals by blocks\Block code.
43. Spustelėkite skirtuką „Susiejimas“.
44. Spustelėkite „Redaguoti formulę“.
45. Lauke Formulė įveskite '"Block id: " & '.
    * "Block id: " &  
46. Medyje išplėskite dalį $BlocksList.
47. Medyje pasirinkite $BlocksList\Value.
48. Spustelėkite „Įtraukti duomenų šaltinį“.
49. Spustelėkite Įrašyti.
50. Uždarykite puslapį.
51. Spustelėkite skirtuką Formatas.
52. Medyje pasirinkite Intrastat\Data\Totals by blocks\Lines counting.
53. Spustelėkite skirtuką „Susiejimas“.
54. Spustelėkite „Redaguoti formulę“.
    * Kurkite kiekvieno šioje ataskaitoje pateikto bloko eilučių skaičiaus išvestį.  
55. Lauke Formulė įveskite '"Number of lines in this block: " & '.
    * "Number of lines in this block: " &  
56. Lauke Formulė įveskite '"Number of lines in this block: " & TEXT('.
    * "Number of lines in this block: " & TEXT(  
57. Medyje pasirinkite Data collection functions\COUNTIFS.
58. Spustelėkite „Įtraukti funkciją“.
59. Spustelėkite „Įtraukti duomenų šaltinį“.
60. Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',  
61. Medyje išplėskite dalį $BlocksList.
62. Medyje pasirinkite $BlocksList\Value.
63. Spustelėkite „Įtraukti duomenų šaltinį“.
64. Lauke Formulė įveskite '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Medyje pasirinkite $RecName.
66. Spustelėkite „Įtraukti duomenų šaltinį“.
67. Lauke Formulė įveskite "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Spustelėkite Įrašyti.
69. Uždarykite puslapį.
70. Spustelėkite skirtuką Formatas.
71. Medyje pasirinkite Intrastat\Data\Totals by blocks\Total amount.
72. Spustelėkite skirtuką „Susiejimas“.
73. Spustelėkite „Redaguoti formulę“.
    * Kurkite išvestį, kuri bus kiekvieno šioje ataskaitoje pateikto bloko bendroji SF suma.  
74. Lauke Formulė įveskite "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Spustelėkite Įrašyti.
76. Uždarykite puslapį.
77. Spustelėkite Įrašyti.
78. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]