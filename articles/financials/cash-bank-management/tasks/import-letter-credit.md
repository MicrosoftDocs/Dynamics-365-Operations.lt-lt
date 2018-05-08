--- 
title: "Importuoti akredityvą"
description: "Ši procedūra padeda importuoti akredityvą."
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 02be2627186a149a05eaccfa3e5906a9fe1d74dd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-letter-of-credit"></a>Importuoti akredityvą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda importuoti akredityvą. Prieš atliekant šią procedūrą reikia nustatyti: banko priemones, registravimo šablonus, banko priemonės sutartį ir tiekėjo banko informaciją.

Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Kurti pirkimo užsakymą su akredityvu
1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite skyrių Bendra.
7. Lauke Teritorija įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
11. Lauke „Apskaitos data“ įveskite datą.
12. Lauke Pristatymo data įveskite datą.
    * Pastaba: turi būti pasirinkta lauko „Banko dokumento tipas“ reikšmė „Akredityvas“.  
13. Spustelėkite GERAI.
14. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Išplėskite skyrių Eilutės informacija.
18. Spustelėkite skirtuką Pristatymas.
19. Lauke Pristatymo data įveskite datą.
20. Lauke Patvirtinta pristatymo data įveskite datą.
21. Lauke Vieneto kaina įveskite skaičių.
    * Nurodykite akredityvo informaciją.  
22. Veiksmų srityje spustelėkite Valdyti.
23. Spustelėkite Akredityvo / importo rinkinys.
24. Lauke Prašymo data įveskite datą ir laiką.
    * Patikrinkite, ar lauko „Banko sąskaita“ reikšmė yra numatytoji aktyvi banko sąskaita, pagrįsta taikymo data.  
25. Lauke Banko dokumento numeris įveskite reikšmę.
26. Lauke Gavimo data įveskite datą ir laiką.
27. Išplėskite skyrių Banko dokumentas.
28. Lauke Galiojimo data įveskite datą ir laiką.
29. Išplėskite sekciją Banko informacija.
30. Lauke Konsultavimo bankas įveskite arba pasirinkite reikšmę.
31. Sąraše spustelėkite saitą pasirinktoje eilutėje.
32. Spustelėkite Įrašyti.
33. Spustelėkite Surasti pirkimo užsakymo siuntas.
34. Uždarykite puslapį.
35. Veiksmų srityje spustelėkite Pirkti.
36. Spustelėkite Patvirtinti.
37. Veiksmų srityje spustelėkite Valdyti.
38. Spustelėkite Akredityvo / importo rinkinys.
39. Spustelėkite „Apdoroti“.
40. Spustelėkite Patvirtinti.
    * Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą.  Šiame pavyzdyje pirkimo suma = 500,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9500,00.  
41. Uždarykite puslapį.
42. Lauke Vieneto kaina įveskite skaičių.
43. Spustelėkite Įrašyti.
44. Veiksmų srityje spustelėkite Pirkti.
45. Spustelėkite Patvirtinti.
    * Keiskite akredityvą dėl pakeistos vieneto kainos.  
46. Veiksmų srityje spustelėkite Valdyti.
47. Spustelėkite Akredityvo / importo rinkinys.
    * Keiskite akredityvą dėl pakeistos pirkimo vieneto kainos.  
48. Spustelėkite „Apdoroti“.
49. Spustelėkite Keisti.
50. Spustelėkite Šalinti.
51. Spustelėkite Taip.
52. Spustelėkite Surasti pirkimo užsakymo siuntas.
53. Spustelėkite „Apdoroti“.
54. Spustelėkite Patvirtinti.
    * Patikrinkite, ar priemonės balansas sumažina pirkimo užsakymo sumą.  Šiame pavyzdyje pakeista pirkimo suma = 600,00, o priemonės limitas = 10000,00, todėl priemonės balansas = 9400,00.  
55. Uždarykite puslapį.

## <a name="post-packing-slip"></a>Registruoti važtaraštį
1. Veiksmų srityje spustelėkite Gauti.
2. Spustelėkite Produkto gavimo kvitas.
3. Lauke „PurchParmTable_Num“ įveskite reikšmę.
    * Pasirinkite siuntos numerį, sukurtą remiantis akredityvu.  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Produkto gavimo kvito data įveskite datą.
6. Spustelėkite GERAI.
7. Uždarykite puslapį.
8. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status"></a>Tikrinti importo akredityvo būseną
1. Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite importo akredityvo būseną.  
4. Uždarykite puslapį.
5. Uždarykite puslapį.

## <a name="post-purchase-invoice"></a>Registruoti pirkimo SF
1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.
    * Pasirinkite pirkimo užsakymą, sukurtą naudojant akredityvą.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Veiksmų srityje spustelėkite Sąskaita faktūra.
5. Spustelėkite Sąskaita faktūra.
6. Lauke Numeris surinkite reikšmę.
7. Lauke Siuntos numeris įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Įveskite datą lauke Sąskaitos faktūros data.
10. Spustelėkite Naujinti gretinimo būseną.
11. Spustelėkite Registruoti.
12. Uždarykite puslapį.
13. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status"></a>Tikrinti importo akredityvo būseną
1. Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite 2 importo akredityvą.  
    * Tikrinti: siuntos būsena = banko paslaugos, kurių SF išrašytos, informacija  
4. Spustelėkite Peržiūrėti.
5. Spustelėkite Spausdinti prašymą.
6. Spustelėkite GERAI.
    * Patikrinkite, ar spausdinamas akredityvo prašymas.  
7. Uždarykite puslapį.
8. Uždarykite puslapį.
9. Uždarykite puslapį.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Registruoti sukurtos pirkimo SF su akredityvu tiekėjo mokėjimų žurnalą
1. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėkite Eilutės.
6. Lauke Data įveskite datą.
7. Lauke Sąskaita nustatykite norimas reikšmes.
8. Spustelėkite „Sudengti operacijas“.
9. Išplėskite sekciją Bendrosios sumos.
10. Lauke Rodyti pasirinkite parinktį.
    * Patikrinkite, ar atnaujinti laukai Banko dokumento numeris ir Siuntos numeris.  
11. Pažymėkite žymės langelį Žymėti.
12. Spustelėkite GERAI.
13. Spustelėkite skirtuką Mokėjimas.
    * Patikrinkite, ar atnaujinti laukai Banko dokumento numeris ir Siuntos numeris.  
14. Spustelėkite Registruoti.
15. Uždarykite puslapį.
16. Uždarykite puslapį.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Tikrinti importo akredityvo būseną po SF apmokėjimo
1. Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Importo akredityvas ir importo rinkinys.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite importo akredityvo būseną.   
4. Uždarykite puslapį.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Tikrinti banko priemonės limito ir naudojimo ataskaitą
1. Eikite į Grynųjų pinigų ir banko valdymas > Užklausos ir ataskaitos > Akredityvai arba garantiniai raštai > Banko priemonių ir naudojimo ataskaita.
2. Išplėskite dalį Įtrauktini įrašai.
3. Spustelėkite Filtras.
    * Lauke Kriterijai nurodykite reikiamą banko sąskaitą.  
4. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite GERAI.
7. Spustelėkite GERAI.
    * Patikrinkite ataskaitą, kurioje išvardytos operacijos.  
    * Patikrinkite, ar ataskaitoje išvardijamos operacijos su banko dokumento numeriu, priemonės limitu, panaudota suma ir priemonės balanso suma.  
8. Uždarykite puslapį.


