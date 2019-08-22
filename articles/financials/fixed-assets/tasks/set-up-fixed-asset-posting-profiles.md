---
title: Ilgalaikio turto registravimo šablonų nustatymas
description: Šis užduočių vadovas nustatys ilgalaikio turto registravimo šablonus.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 494af854d408f0b0c02d753ff3d24eb3d6216fd9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839814"
---
# <a name="set-up-fixed-asset-posting-profiles"></a>Ilgalaikio turto registravimo šablonų nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas nustatys ilgalaikio turto registravimo šablonus.  Jis naudoja vaidmenį Buhalteris ir USMF juridinio subjekto demonstracinius duomenis.  Užduočių vadove pateikiami pagrindinio registravimo šablono pavyzdžiai, nors reikia sukurti jūsų konkretaus sąskaitų plano ir finansinių ataskaitų reikalavimų registravimo šablonus.

1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Konfigūracija > Ilgalaikio turto registravimo šablonai**.
2. Spustelėkite **Naujas**.
3. Lauke **Posting profile** surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę. Turėsite sukurti kiekvieno ilgalaikio turto operacijos tipo, kurį naudosite dirbdami su ilgalaikiu turtu, registravimo šabloną. Šis užduočių vadovas pradės nuo įsigijimo operacijos tipo.  
5. Įrankių juostoje spustelėkite **Įrašyti**.
6. Lauke **Book** įveskite arba pasirinkite reikšmę. Laukas **Groupings** leidžia registravimo šabloną apibrėžti iki lentelės (kiekvienam ilgalaikiam turtui nustatyta po vieną sąskaitą) arba grupės (kiekvienai ilgalaikio turto grupei nustatyta po vieną sąskaitą). Šiame užduočių vadove reikšmę paliksiu nustatytą į „Visi”, kad būtų taikoma visam ilgalaikiam turtui su nurodyta knyga.  
7. Lauke **Main account** nustatykite norimas reikšmes. Lauke Įsigijimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.    
8. „FastTab" skirtuko **DK sąskaitos** išplečiamajame meniu pasirinkite „Įsigijimų koregavimas“. Atlikdami įsigijimo koregavimo operacijas, naudojame tas pačias sąskaitas, kurios buvo naudojamos atliekant įsigijimo operacijas.  
9. Spustelėkite **Pridėti**.
10. Lauke **Book** įveskite arba pasirinkite reikšmę.
11. Lauke **Main account** nustatykite norimas reikšmes. Lauke Įsigijimų koregavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.    
12. „FastTab" skirtuko **DK sąskaitos** išplečiamajame meniu pasirinkite „Nusidėvėjimas“.
13. Spustelėkite **Pridėti**.
14. Lauke **Book** įveskite arba pasirinkite reikšmę.
15. Lauke **Main account** nustatykite norimas reikšmes.
16. Lauke **Offset account** nustatykite norimas reikšmes.
17. „FastTab" skirtuko **DK sąskaitos** išplečiamajame meniu pasirinkite „Nusidėvėjimo koregavimas“. Atlikdami nusidėvėjimo koregavimo operacijas, naudojame tas pačias sąskaitas, kurios buvo naudojamos atliekant nusidėvėjimo operacijas.  
18. Spustelėkite **Pridėti**.
19. Lauke **Book** įveskite arba pasirinkite reikšmę.
20. Lauke **Main account** nustatykite norimas reikšmes.
21. Lauke **Offset account** nustatykite norimas reikšmes.
22. „FastTab" skirtuko **DK sąskaitos** išplečiamajame meniu pasirinkite „Perleidimas – pardavimas“.
23. Spustelėkite **Pridėti**.
24. Lauke **Book** įveskite arba pasirinkite reikšmę.
25. Lauke **Main account** nustatykite norimas reikšmes. Lauke Likvidavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.  
26. „FastTab" skirtuko **DK sąskaitos** išplečiamajame meniu pasirinkite „Perleidimas – atliekos“. Likvidavimui parduoti ir likvidavimui nurašyti naudosime tas pačias sąskaitas.  
27. Spustelėkite **Pridėti**.
28. Lauke **Book** įveskite arba pasirinkite reikšmę.
29. Lauke **Main account** nustatykite norimas reikšmes. Lauke Likvidavimai galite įvesti korespondentinę sąskaitą arba jį palikti tuščią, kad būtų galima užpildyti atliekant konkrečią operaciją.  
30. Išplėskite **Bendra** FastTab. Turite nustatyti likvidavimo registravimo šablonus, skirtus tiek likvidavimui parduoti, tiek nurašyti.  Prasidėsime nuo likvidavimo pardavimo operacijų.  
31. Spustelėkite **Pridėti**.
32. Lauke **Book** įveskite arba pasirinkite reikšmę.
33. Lauke **Post value** pasirinkite „Įsigijimo vertė‟.
    * Įsigijimo reikšmė palies kiekvienų metų įsigijimo ir įsigijimo koregavimo reikšmes. Šių operacijų tipų sąskaitas taip pat galite apibrėžti atskirai.  
    * Galite nustatyti, kad likvidavimo procesas naudotų skirtingas sąskaitas – tai priklausytų nuo to, ar likvidavimo rezultatas – pelnas, ar – nuostolis. Pardavimo vertės tipą nustatysiu į „Visi‟, kad tos pačios sąskaitos būtų naudojamos visiems likvidavimų tipams.  
34. Lauke **Main account** nustatykite norimas reikšmes.
35. Lauke **Offset account** nustatykite norimas reikšmes.
36. Spustelėkite **Pridėti**.
37. Lauke **Book** įveskite arba pasirinkite reikšmę.
38. Lauke **Post value** pasirinkite „Nusidėvėjimas (ankstesniais metais)‟.  
38. Lauke **Main account** nustatykite norimas reikšmes.
39. Lauke **Offset account** nustatykite norimas reikšmes.
40. Spustelėkite **Pridėti**.
41. Lauke **Book** įveskite arba pasirinkite reikšmę.
42. Lauke **Post value** pasirinkite „Nusidėvėjimas (šiais metais)‟.
43. Lauke **Main account** nustatykite norimas reikšmes.
44. Lauke **Offset account** nustatykite norimas reikšmes.
45. Spustelėkite **Pridėti**.
46. Lauke **Book** įveskite arba pasirinkite reikšmę.
47. Lauke **Post value** pasirinkite „Nusidėvėjimo koregavimai (ankstesniais metais)‟.
48. Lauke **Main account** nustatykite norimas reikšmes.
49. Lauke **Offset account** nustatykite norimas reikšmes.
50. Spustelėkite **Pridėti**.
51. Lauke **Book** įveskite arba pasirinkite reikšmę.
52. Lauke **Post value** pasirinkite „Nusidėvėjimo koregavimai (šiais metais)‟.
53. Lauke **Main account** nustatykite norimas reikšmes.
54. Lauke **Offset account** nustatykite norimas reikšmes.
55. Spustelėkite **Pridėti**.
56. Lauke **Book** įveskite arba pasirinkite reikšmę.
57. Lauke **Post value** pasirinkite „Balansinė vertė‟.
58. Lauke **Main account** nustatykite norimas reikšmes.
59. Lauke **Offset account** nustatykite norimas reikšmes.
60. Lauke **Sale or scrap** pasirinkite „Nurašymas“.
61. Spustelėkite **Pridėti**.
62. Lauke **Book** įveskite arba pasirinkite reikšmę.
63. Lauke **Post value** pasirinkite „Įsigijimo vertė‟.
64. Lauke **Main account** nustatykite norimas reikšmes.
65. Lauke **Offset account** nustatykite norimas reikšmes.
66. Spustelėkite **Pridėti**.
67. Lauke **Book** įveskite arba pasirinkite reikšmę.
67. Lauke **Post value** pasirinkite „Nusidėvėjimas (ankstesniais metais)‟.  
68. Lauke **Main account** nustatykite norimas reikšmes.
69. Lauke **Offset account** nustatykite norimas reikšmes.
70. Spustelėkite **Pridėti**.
71. Lauke **Book** įveskite arba pasirinkite reikšmę.
72. Lauke **Post value** pasirinkite „Nusidėvėjimas (šiais metais)‟.
73. Lauke **Main account** nustatykite norimas reikšmes.
74. Lauke **Offset account** nustatykite norimas reikšmes.
75. Spustelėkite **Pridėti**.
76. Lauke **Book** įveskite arba pasirinkite reikšmę.
77. Lauke **Post value** pasirinkite „Nusidėvėjimo koregavimai (ankstesniais metais)‟.
78. Lauke **Main account** nustatykite norimas reikšmes.
79. Lauke **Offset account** nustatykite norimas reikšmes.
80. Spustelėkite **Pridėti**.
81. Lauke **Book** įveskite arba pasirinkite reikšmę.
82. Lauke **Post value** pasirinkite „Nusidėvėjimo koregavimai (šiais metais)‟.
83. Lauke **Main account** nustatykite norimas reikšmes.
84. Lauke **Offset account** nustatykite norimas reikšmes.
85. Spustelėkite **Pridėti**.
86. Lauke **Book** įveskite arba pasirinkite reikšmę.
87. Lauke **Post value** pasirinkite „Balansinė vertė‟.
88. Lauke **Main account** nustatykite norimas reikšmes.
89. Lauke **Offset account** nustatykite norimas reikšmes.

