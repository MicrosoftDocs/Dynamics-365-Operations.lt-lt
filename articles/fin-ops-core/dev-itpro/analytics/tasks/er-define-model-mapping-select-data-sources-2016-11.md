---
title: ER modelio susiejimų nustatymas ir jų duomenų šaltinių pasirinkimas
description: Tolesniais veiksmais paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali pažymėti elektroninių ataskaitų duomenų modelio duomenų šaltinius.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6287fa95b7ce7341e99d1b1a6b972db68a30398
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142176"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>ER modelio susiejimų nustatymas ir jų duomenų šaltinių pasirinkimas

[!include [banner](../../includes/banner.md)]

Tolesniais veiksmais paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali pažymėti elektroninių ataskaitų (ER) duomenų modelio duomenų šaltinius. Duomenų šaltiniai bus susieti su atskirais pasirinkto duomenų modelio komponentais kūrimo metu ir automatiškai įves verslo duomenis į tą duomenų modelį vykdymo metu. Šiame pavyzdyje pasirinksite esamo duomenų modelio, sukurto pavyzdinei įmonei „Litware, Inc.“, duomenų šaltinius. Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Kurti naują duomenų modelį“ veiksmus.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Atidaryti elektroninių ataskaitų konfigūracijų medį
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.

## <a name="insert-a-new-model-mapping"></a>Įterpti naują modelio susiejimą
1. Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.
2. Spustelėkite Konstruktorius.
3. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
4. Spustelėkite Naujas.
    * Taip sukursite naują įrašą, kuris susies duomenų modelį su duomenų šaltiniais. Šiame pavyzdyje susiesite duomenų modelį su norimo mokėjimo tipo (kredito pervedimas) duomenų šaltiniais.     Galima sukurti daugiau nei vieną konkretaus duomenų modelio susiejimą. Pvz., galite sukurti skirtingų tipų mokėjimų, pvz., tiesioginio debeto arba kredito pervedimų, susiejimą. Šiame pavyzdyje sukursite kredito pervedimų susiejimą.  
5. Lauke „Pavadinimas“ įveskite „CT susiejimas“.
    * Kreditų pervedimų susiejimas  
6. Lauke „Aprašas“ įveskite „Mokėjimo modelio CT susiejimas“.
    * Kreditų pervedimų mokėjimo modelio susiejimas  
7. Lauke „Aprašas“ įveskite „CustomerCreditTransferInitiation“.
    * CustomerCreditTransferInitiation  
8. ResolveChanges – aprašas.
9. Spustelėkite Įrašyti.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Nurodyti reikiamus esamo modelio susiejimo duomenų šaltinius
1. Spustelėkite Konstruktorius.
2. Medyje pasirinkite Dynamics 365 for Operations\Table records.
3. Spustelėkite „Įtraukti šaknį“.
    * Įveskite šį duomenų šaltinį, kad pasiektumėte mokėjimo operacijas.  
4. Lauke „Pavadinimas“, įveskite „Operacijos“.
    * Operacijos  
5. Lauke „Žyma“ įveskite „Operacijos“.
    * Operacijos  
6. Lauke „Žinynas“ įveskite „Didžiosios knygos žurnalo eilutės“.
    * Didžiosios knygos žurnalo eilutės  
7. Lauke „Prašyti užklausos“ pasirinkite „Taip“.
    * Pasirinkite „Taip“.  
8. Lauke „Lentelė“, įveskite „LedgerJournalTrans“.
    * LedgerJournalTable  
9. Spustelėkite GERAI.
    * Pasirinkite lentelę „LedgerJournalTrans“ kaip esamo duomenų modelio duomenų šaltinį.  
10. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
11. Spustelėkite Pridėti.
    * Spustelėkite „Įtraukti“, kad įtrauktumėte naują apskaičiuotą lauką.  
12. Lauke „Pavadinimas“ įveskite „$EndToEndID“.
    * $EndToEndID  
13. Spustelėkite „Redaguoti formulę“.
14. Medyje pasirinkite „Eilutė \ SUJUNGTI“.
15. Spustelėkite „Įtraukti funkciją“.
16. Medyje išplėskite „Operacijos“.
17. Medyje pasirinkite „Operacijos \ Kvitas“.
18. Spustelėkite „Įtraukti duomenų šaltinį“.
19. Lauke „Formulė“ įveskite „CONCATENATE(Transactions.Voucher, "-", “.
    * Įveskite [, "–",] formulės pabaigoje.  
20. Medyje pasirinkite „Eilutė \ TEKSTAS“.
21. Spustelėkite „Įtraukti funkciją“.
22. Medyje pasirinkite „Operacijos \ Įrašo ID (RecId)“.
23. Spustelėkite „Įtraukti duomenų šaltinį“.
24. Lauke „Formulė“ įveskite „CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))“.
    * Įveskite [))] formulės pabaigoje.  
25. Spustelėkite Įrašyti.
    * Įsitikinkite, ar neaptikta sukurtos formulės klaidų. Peržiūrėkite skirtuką KLAIDOS, esantį po formulės redaktorius valdikliu.  
26. Uždarykite puslapį.
27. Spustelėkite GERAI.
    * Įtraukite apskaičiuotą lauką į šį duomenų šaltinį.  
28. Spustelėkite Pridėti.
    * Spustelėkite „Įtraukti“, kad įtrauktumėte naują apskaičiuotą lauką.  
29. Lauke „Pavadinimas“ įveskite „$Suma“.
    * $Suma  
30. Spustelėkite „Redaguoti formulę“.
31. Medyje išplėskite „Operacijos“.
32. Medyje pasirinkite „Operacijos \ Debetas (AmountCurDebit)“.
33. Spustelėkite „Įtraukti duomenų šaltinį“.
34. Lauke „Formulė“ įveskite „Transactions.AmountCurDebit - ”.
    * Įveskite [ - ] formulės pabaigoje.  
35. Medyje pasirinkite „Operacijos \ Kreditas (AmountCurCredit)“.
36. Spustelėkite „Įtraukti duomenų šaltinį“.
37. Spustelėkite Įrašyti.
38. Uždarykite puslapį.
39. Spustelėkite GERAI.
    * Tai įtrauks apskaičiuotą lauką „$Suma“ į pasirinktą esamo duomenų modelio duomenų šaltinį.  
40. Medyje pasirinkite „Transactions\$Amount“.
41. Medyje išplėskite „Operacijos“.
42. Medyje išplėskite arba sutraukite „Transactions\$Amount”.
43. Medyje išplėskite arba sutraukite „Operacijos”.
44. Medyje pasirinkite Dynamics 365 for Operations\Table records.
45. Spustelėkite „Įtraukti šaknį“.
    * Įveskite šį duomenų šaltinį, kad pasiektumėte įmonės banko sąskaitos informaciją.  
46. Lauke „Pavadinimas“ įveskite „BankAccount“.
    * BankAccount  
47. Lauke „Žyma“ įveskite „Banko sąskaita“.
    * Banko kodas  
48. Lauke „Žinynas“ įveskite „Banko sąskaita“.
    * Banko kodas  
49. Lauke „Prašyti užklausos“ pasirinkite „Taip“.
    * Pasirinkite „Taip“.  
50. Lauke „Lentelė“, įveskite „BankAccountTable“.
    * BankAccountTable  
51. Spustelėkite GERAI.
    * Pasirinkite lentelę „BankAccountTable“ kaip esamo duomenų modelio duomenų šaltinį.  
52. Spustelėkite „Įtraukti šaknį“.
    * Įveskite šį duomenų šaltinį, kad pasiektumėte įmonės rekvizitus.  
53. Lauke „Pavadinimas“ įveskite „Įmonė“.
    * Įmonė  
54. Lauke „Žyma“ įveskite reikšmę.
    * Informacija apie įmonę  
55. Lauke „Žinynas“ įveskite „Įmonės informacija“.
    * Informacija apie įmonę  
56. Lauke „Prašyti užklausos“ pasirinkite „Taip“.
    * Pasirinkite „Taip“.  
57. Lauke „Lentelė“, įveskite „CompanyInfo“.
    * CompanyInfo  
58. Spustelėkite GERAI.
    * Pasirinkite lentelę „CompanyInfo“ kaip esamo duomenų modelio duomenų šaltinį.  
59. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
60. Spustelėkite „Įtraukti šaknį“.
    * Įtraukite apskaičiuotą lauką kaip naują duomenų šaltinį.  
61. Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.
    * ProcessingDateTime  
62. Lauke Žyma įveskite „Apdorojimo data ir laikas“.
    * Apdorojimo data ir laikas  
63. Spustelėkite „Redaguoti formulę“.
64. Medyje pasirinkite „Data / laikas \ SESSIONNOW”.
65. Spustelėkite „Įtraukti funkciją“.
66. Spustelėkite Įrašyti.
67. Uždarykite puslapį.
68. Spustelėkite GERAI.
    * Įtraukite apskaičiuotą lauką „ProcessingDateTime“ kaip esamo duomenų modelio duomenų šaltinį.  
69. Spustelėkite Įrašyti.
70. Uždarykite puslapį.
71. Uždarykite puslapį.
72. Uždarykite puslapį.

