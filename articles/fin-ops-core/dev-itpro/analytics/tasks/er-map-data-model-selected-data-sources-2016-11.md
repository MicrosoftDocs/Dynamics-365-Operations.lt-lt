---
title: ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais
description: Šiame straipsnyje aprašoma, kaip susieti elektroninės ataskaitos (ER) duomenų modelį su pasirinktais Microsoft Dynamics 365 finansų duomenų šaltiniais.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
ms.openlocfilehash: 7d4dcc9b4e4e1128c8d1abee93b2f7affe711643
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290191"
---
# <a name="er-map-data-model-to-selected-data-sources"></a>ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali susieti elektroninių ataskaitų (ER) duomenų modelį su pasirinktais duomenų šaltiniais. Vėliau šis modelio susiejimas bus naudojamas kaip duomenų šaltinis formato konfigūracijoje, kuri bus naudojama elektroninio mokėjimo dokumentams valdyti. Šiame pavyzdyje susiesite pavyzdinės įmonės „Litware, Inc“ duomenų modelį su duomenų šaltiniais. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Pasirinkti modelio susiejimo duomenų šaltinius“ veiksmus.


## <a name="open-er-configurations-tree"></a>Atidaryti ER konfigūracijos medį
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite „Konfigūracijos“.

## <a name="select-created-model-mapping"></a>Pasirinkti sukurto modelio susiejimą
1. Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.
    * Įsitikinkite, kad modelio konfigūracija „Mokėjimai (supaprastintas modelis)“ buvo sukurta iš anksto. Priešingu atveju tuoj pat sustabdykite ir grįžkite užbaigę užduočių vadovą „Naujos konfigūracijos naudojant pasirinkto domeno duomenų modelį kūrimas”.  
2. Spustelėkite „Modelių kūrimo įrankis“.
3. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
4. Pasirinkite įrašą „Kredito pervedimo susiejimas“.
    * Kreditų pervedimų susiejimas  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Susieti sukurtus duomenų šaltinius su duomenų modelio elementais
1. Spustelėkite Konstruktorius.
2. Medyje pasirinkite „Apdorojimo data ir laikas (ProcessingDateTime)“.
3. Medyje pasirinkite „Apdorojimo data (ProcessingDateTime)“.
4. Spustelėkite Susieti.
5. Medyje pasirinkite „Mokėjimo pranešimo identifikacija (MessageIdentification)“.
6. Medyje išplėskite „Operacijos“.
7. Medyje pasirinkite „Operacijos \ Žurnalo numeris (JournalNum)“.
8. Spustelėkite Susieti.
9. Medyje pasirinkite „Mokėjimai“.
10. Medyje pasirinkite „Operacijos“.
11. Spustelėkite Susieti.
12. Medyje išplėskite „Mokėjimai = Operacijos“.
13. Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius‟.
14. Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita‟.
15. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ Valiutos kodas (Valiuta)“.
16. Medyje išplėskite „Operacijos \ vendBankAccountInTransactionCompany()“.
17. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Valiuta (CurrencyCode)“.
18. Spustelėkite Susieti.
19. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ IBAN kodas (IBAN)“.
20. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ IBAN (BankIBAN)“.
21. Spustelėkite Susieti.
22. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Sąskaita \ Numeris“.
23. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Banko sąskaitos numeris (AccountNum).
24. Spustelėkite Susieti.
25. Medyje išplėskite „Mokėjimai = Operacijos \ Kreditorius \ Agentas“.
26. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ Pavadinimas“.
27. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Pavadinimas“.
28. Spustelėkite Susieti.
29. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ Banko numeris (RoutingNumber)“.
30. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ Banko numeris (RegistrationNum)“.
31. Spustelėkite Susieti.
32. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Agentas \ SWIFT kodas (SWIFT)“.
33. Medyje pasirinkite „Operacijos \ vendBankAccountInTransactionCompany() \ SWIFT kodas (SWIFTNo)“.
34. Spustelėkite Susieti.
35. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Pavadinimas“.
36. Medyje išplėskite „Operacijos \ findVendTable()“.
37. Medyje pasirinkite „Operacijos \ findVendTable()\name()“.
38. Spustelėkite Susieti.
39. Medyje pasirinkite „Mokėjimai = Operacijos \ Kreditorius \ Valiutos kodas (Valiuta)“.
40. Medyje išplėskite Transactions\>Relations.
41. Medyje išplėskite Transactions\>Relations\Currency table(Currency).
42. Medyje pasirinkite Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).
43. Spustelėkite Susieti.
44. Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas“.
45. Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita‟.
46. Medyje pasirinkite „Mokėjimai = Operacijos \ Debitorius \ Sąskaita \ Valiutos kodas (Valiuta)“.
47. Medyje pasirinkite „Banko sąskaita (BankAccount)“.
48. Medyje išplėskite „Banko sąskaita (BankAccount)“.
49. Medyje pasirinkite „Banko sąskaita (BankAccount) \ Valiuta (CurrencyCode)“.
50. Spustelėkite Susieti.
51. Medyje pasirinkite „Banko sąskaita (BankAccount) \ IBAN“.
52. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita \ IBAN kodas (IBAN)“.
53. Spustelėkite Susieti.
54. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Sąskaita \ Numeris“.
55. Medyje pasirinkite „Banko sąskaitą (BankAccount) \ Bank sąskaitos numeris (AccountNum)“.
56. Spustelėkite Susieti.
57. Medyje išplėskite „Mokėjimai = Operacijos \ Skolininkas \ Agentas‟.
58. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ Pavadinimas“.
59. Medyje pasirinkite „Banko sąskaita (BankAccount) \ Pavadinimas“.
60. Spustelėkite Susieti.
61. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ Banko numeris (RoutingNumber)“.
62. Medyje pasirinkite „Banko sąskaitą (BankAccount) \ Bank numeris (RegistrationNum)“.
63. Spustelėkite Susieti.
64. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Agentas \ SWIFT kodas (SWIFT)“.
65. Medyje pasirinkite „Banko sąskaita (BankAccount) \ SWIFT kodas (SWIFTNo)“.
66. Spustelėkite Susieti.
67. Medyje pasirinkite „Mokėjimai = Operacijos \ Skolininkas \ Pavadinimas“.
68. Medyje pasirinkite „Įmonės informacija (Įmonė)“.
69. Medyje išplėskite „Įmonės informacija (Įmonė)“.
70. Medyje pasirinkite „Įmonės informacija (Įmonė) \ Pavadinimas“.
71. Spustelėkite Susieti.
72. Medyje pasirinkite „Mokėjimai = Operacijos \ Aprašas“.
73. Medyje pasirinkite „Operacijos \ Aprašas (Txt)“.
74. Spustelėkite Susieti.
75. Medyje pasirinkite „Mokėjimai = Operacijos \ Tiesioginės identifikacijos kodas (End2EndID)“.
76. Medyje pasirinkite Transactions\$EndToEndID.
77. Spustelėkite Susieti.
78. Medyje pasirinkite „Mokėjimai = Operacijos \ Nurodyta suma (InstructedAmount)“.
79. Medyje pasirinkite „Transactions\$Amount“.
80. Spustelėkite Susieti.
81. Medyje pasirinkite „Mokėjimai = Operacijos \ Operacijos data (TransactionDate)“.
82. Medyje pasirinkite „Operacijos \ Data (TransDate)“.
83. Spustelėkite Susieti.

## <a name="validate-created-mapping"></a>Tikrinti sukurtą susiejimą
1. Spustelėkite Tikrinti.
    * Norėdami įsitikinti, kad visi susiejimai veikia gerai, patikrinkite naują susiejimą.  
2. Spustelėdami rodyklę išplėskite arba sutraukite sekciją Klaidų sąrašas.
3. Spustelėkite Įrašyti.
4. Uždarykite puslapį.
5. Uždarykite puslapį.
6. Uždarykite puslapį.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Pakeisti esamos modelio konfigūracijos versijos būseną
1. Spustelėkite keisti būseną.
    * Pakeiskite sukurtos modelio konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti kuriant mokėjimo formatus.  
2. Spustelėkite Baigti.
    * Pasirinkite Baigti.  
3. Lauke Aprašas įveskite reikšmę.
    * Pavyzdžiui, „1 versija“.  
4. Spustelėkite GERAI.
5. Pasirinkite baigtą esamos konfigūracijos versiją.
    * Atkreipkite dėmesį, kad sukurta konfigūracija įrašoma kaip 1 baigta versija.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
