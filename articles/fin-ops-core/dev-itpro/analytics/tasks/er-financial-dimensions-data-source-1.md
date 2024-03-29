---
title: ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)
description: Šiame straipsnyje aprašoma, kaip sukonfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (1 dalis)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
ms.openlocfilehash: 053b9cf9ea6b2845bef5d95e901c1c90fac964be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290851"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>ER naudoti finansines dimensijas kaip duomenų šaltinį (1 dalis – Duomenų modelio kūrimas)

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratorius arba elektroninių ataskaitų kūrėjas gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.


## <a name="create-a-new-data-model"></a>Naujo duomenų modelio kūrimas
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad „Litware, Inc.“ yra pasiekiamas ir pažymėtas kaip aktyvus.  
2. Spustelėkite Ataskaitų konfigūracijos.
3. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
4. Lauke Pavadinimas įveskite Finansinių dimensijų modelio pavyzdys.
5. Spustelėkite Sukurti konfigūraciją.
6. Spustelėkite Konstruktorius.
7. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
8. Lauke Pavadinimas įveskite Įrašas.
9. Spustelėkite Pridėti.
10. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
11. Lauke „Pavadinimas“ įveskite „Įmonė“.
12. Spustelėkite Pridėti.
    * Įtrauksime mūsų modelį į naują įrašų sąrašą. Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų parametrai. Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos parametrą.  
13. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
14. Lauke Pavadinimas įveskite Dimensijos parametras.
15. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
16. Spustelėkite Pridėti.
17. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
18. Lauke Pavadinimas įveskite Kodas.
19. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
20. Spustelėkite Pridėti.
21. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
22. Lauke „Pavadinimas“ įveskite „Agentas“.
23. Spustelėkite Pridėti.
24. Medyje pasirinkite Įrašas.
25. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
26. Lauke Pavadinimas įveskite Žurnalas.
27. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
28. Spustelėkite Pridėti.
29. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
30. Lauke Pavadinimas įveskite Paketas.
31. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
32. Spustelėkite Pridėti.
33. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
34. Lauke Pavadinimas įveskite Operacija.
35. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
36. Spustelėkite Pridėti.
37. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
38. Lauke Pavadinimas įveskite Data.
39. Lauke „Prekės tipas“ pasirinkite „Data“.
40. Spustelėkite Pridėti.
41. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
42. Lauke Pavadinimas įveskite Debetas.
43. Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.
44. Spustelėkite Pridėti.
45. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
46. Lauke Pavadinimas įveskite Kreditas.
47. Spustelėkite Pridėti.
48. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
49. Lauke „Pavadinimas“ suveskite „Valiuta“.
50. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
51. Spustelėkite Pridėti.
52. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
53. Lauke Pavadinimas įveskite Kvitas.
54. Spustelėkite Pridėti.
55. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
56. Lauke Pavadinimas įveskite Dimensijų duomenys.
57. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
58. Spustelėkite Pridėti.
    * Įtraukėme mūsų modelį į naują įrašų sąrašą. Šiame sąraše bus parodyti (jei ER ataskaitose šis modelis naudojamas kaip duomenų šaltinis) pasirinktų finansinių dimensijų reikšmės. Kiekviena finansinė dimensija bus šiame sąraše pateikta kaip įrašas su atitinkamais laukais, nurodančiais dimensijos reikšmes. Dimensijos pavadinimas taip pat bus pateiktas šiame įraše yra laukas, kurį, jei reikia, galima naudoti norint pasirinkti.  
59. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
60. Lauke Pavadinimas įveskite Kodas.
61. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
62. Spustelėkite Pridėti.
63. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
64. Lauke „Pavadinimas“, įveskite „Aprašas“.
65. Spustelėkite Pridėti.
66. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
67. Lauke „Pavadinimas“ įveskite „Agentas“.
68. Spustelėkite Pridėti.
69. Spustelėkite Įrašyti.
70. Uždarykite puslapį.

![ER duomenų modelio dizaino įrankio puslapis.](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
