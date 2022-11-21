---
title: Importuoti akredityvą
description: Ši procedūra padeda importuoti akredityvą.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07748c2dc41f6411add1d54589652baa7fc3fbb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779444"
---
# <a name="import-letter-of-credit"></a>Importuoti akredityvą

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda importuoti akredityvą. Prieš atliekant šią procedūrą reikia nustatyti: banko priemones, registravimo šablonus, banko priemonės sutartį ir tiekėjo banko informaciją.

Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Kurti pirkimo užsakymą su akredityvu
1. Pereikite į mokėtinų **sumų > pirkimo užsakymų > visi pirkimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite skyrių **Bendra**.
7. Lauke **Teritorija** įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke **Sandėlis** įveskite arba pasirinkite reikšmę.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Lauke **Apskaitos data** įveskite datą.
12. Lauke **Pristatymo data** įveskite datą.
    * Pastaba: banko dokumento **tipo laukas turi** būti **akredityvo**.  
13. Spustelėkite **Gerai**.
14. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Išplėskite skyrių **Eilutės informacija** section.
18. Spustelėkite skirtuką **Pristatymas**.
19. Lauke **Pristatymo data** įveskite datą.
20. Lauke **Patvirtinta pristatymo data** įveskite datą.
21. Lauke **Vieneto kaina** įveskite skaičių.
    * Nurodykite akredityvo informaciją.  
22. Veiksmų srityje spustelėkite **Valdyti**.
23. Spustelėkite akredityvo **/ importo rinkinį**.
24. **Programos datos lauke** įveskite datą ir laiką.
    * Patikrinkite, ar **laukas** Banko kodas turi numatytąją aktyvią banko sąskaitą, pagrįstą prašymo data.  
25. Lauke Banko **dokumento numeris** įveskite vertę.
26. **Lauke Gavimo data** įveskite datą ir laiką.
27. Išplėskite banko **dokumento** skyrių.
28. Lauke Galiojimo **data** įveskite datą ir laiką.
29. Išplėskite skyrių **Banko** informacija.
30. **Lauke Konsultavimo bankas** įveskite arba pasirinkite vertę.
31. Sąraše spustelėkite saitą pasirinktoje eilutėje.
32. Spustelėkite **Įrašyti**.
33. Spustelėkite **Surasti pirkimo užsakymo siuntas**.
34. Uždarykite puslapį.
35. Veiksmų srityje spustelėkite **Pirkti**.
36. Spustelėkite **Patvirtinti**.
37. Veiksmų srityje spustelėkite **Valdyti**.
38. Spustelėkite akredityvo **/ importo rinkinį**.
39. Spustelėkite **Apdoroti**.
40. Spustelėkite **Patvirtinti**.
    * Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą. Šiame pavyzdyje pirkimo suma = 500,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9500,00.  
41. Uždarykite puslapį.
42. Lauke **Vieneto kaina** įveskite skaičių.
43. Spustelėkite **Įrašyti**.
44. Veiksmų srityje spustelėkite **Pirkti**.
45. Spustelėkite **Patvirtinti**.
    * Keiskite akredityvą dėl pakeistos vieneto kainos.  
46. Veiksmų srityje spustelėkite **Valdyti**.
47. Spustelėkite akredityvo **/ importo rinkinį**.
    * Keiskite akredityvą dėl pakeistos pirkimo vieneto kainos.  
48. Spustelėkite **Apdoroti**.
49. Spustelėkite **Pakeisti**.
50. Spustelėkite **Pašalinti**.
51. Spustelėkite **Taip**.
52. Spustelėkite **Surasti pirkimo užsakymo siuntas**.
53. Spustelėkite **Apdoroti**.
54. Spustelėkite **Patvirtinti**.
    * Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą. Šiame pavyzdyje pakeista pirkimo suma = 600,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9400,00.  
55. Uždarykite puslapį.

## <a name="post-packing-slip"></a>Registruoti važtaraštį
1. Veiksmų srityje spustelėkite **Gauti**.
2. Spustelėkite **Produkto gavimo kvitas**.
3. **Į PurchParmTable_Num** įveskite vertę.
    * Pasirinkite siuntos numerį, sukurtą remiantis akredityvu.  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. **Gavimo dokumento datos** lauke įveskite datą.
6. Spustelėkite **Gerai**.
7. Uždarykite puslapį.
8. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status"></a>Tikrinti importo akredityvo būseną
1. Eikite į **grynųjų pinigų ir banko valdymo > akredityvo > importo akredityvo ir importo rinkinį**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite importo akredityvo būseną.     
4. Uždarykite puslapį.
5. Uždarykite puslapį.

## <a name="post-purchase-invoice"></a>Registruoti pirkimo SF
1. Pereikite į mokėtinų **sumų > pirkimo užsakymų > visi pirkimo užsakymai**.
    * Pasirinkite pirkimo užsakymą, sukurtą naudojant akredityvą.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Veiksmų srityje spustelėkite **Sąskaita faktūra**.
5. Spustelėkite **Sąskaita faktūra**.
6. Lauke **Numeris** įveskite vertę.
7. Į lauką **Siuntos** numeris įveskite arba pasirinkite vertę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke **SF data** įveskite datą.
10. Spustelėkite **Naujinti gretinimo būseną**.
11. Spustelėkite **Registruoti**.
12. Uždarykite puslapį.
13. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Patikrinkite importo akredityvo ir spausdinimo būseną.

1. Eikite į **grynųjų pinigų ir banko valdymo > akredityvo > importo akredityvo ir importo rinkinį**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite 2 importo akredityvą.  
    * Tikrinti: siuntos **būsenos, kurioms** = **išrašyta SF** banko priemonės informacija  
4. Spustelėkite **Rodyti**.
5. Spustelėkite **Spausdinti prašymą**.
6. Spustelėkite **Gerai**.
    * Patikrinkite, ar spausdinamas akredityvo prašymas.  
7. Uždarykite puslapį.
8. Uždarykite puslapį.
9. Uždarykite puslapį.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Registruoti sukurtos pirkimo SF su akredityvu tiekėjo mokėjimų žurnalą
1. Pasirinkite **Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite **Eilutės**.
6. Lauke **Data** įveskite datą.
7. Lauke **Sąskaita** nustatykite norimas reikšmes.
8. Spustelėkite Sudengti **operacijas**.
9. Išplėskite sekciją Bendrosios sumos.
10. **Lauke Rodyti** pasirinkite pasirinktį.
    * Patikrinkite, ar **atnaujinti laukai** Banko **dokumento numeris** ir Siuntos numeris.  
11. Pažymėkite žymės langelį **Žymėti**.
12. Spustelėkite **Gerai**.
13. Spustelėkite skirtuką Mokėjimas.
    * Patikrinkite, ar **atnaujinti laukai** Banko **dokumento numeris** ir Siuntos numeris.  
14. Spustelėkite **Registruoti**.
15. Uždarykite puslapį.
16. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Tikrinti importo akredityvo būseną po SF apmokėjimo
1. Eikite į **grynųjų pinigų ir banko valdymo > akredityvo > importo akredityvo ir importo rinkinį**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite importo akredityvo būseną.   
4. Uždarykite puslapį.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Tikrinti banko priemonės limito ir naudojimo ataskaitą
1. Eikite **į grynųjų pinigų ir banko valdymo > užklausas ir ataskaitas, > akredityvo arba garantinio > ir naudingumo ataskaitą**.
2. Išplėskite dalį Įtrauktini įrašai.
3. Spustelėkite **Filtras**.
    * Nurodykite **kriterijų** lauką su reikalinga banko sąskaita.  
4. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Gerai**.
7. Spustelėkite **Gerai**.
    * Patikrinkite ataskaitą, kurioje išvardytos operacijos.  
    * Patikrinkite, ar ataskaitoje išvardijamos operacijos su banko dokumento numeriu, priemonės limitu, panaudota suma ir priemonės balanso suma.  
8. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
