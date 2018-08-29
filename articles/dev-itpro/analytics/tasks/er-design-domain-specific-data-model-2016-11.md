--- 
title: "Konkretaus domeno duomenų modelio kūrimas"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c59bdea789c4eafd2443a5d1cf802768259858c6
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-domain-specific-data-models"></a>Konkretaus domeno duomenų modelio kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį. Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.



Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Pasirinkite pavyzdinės įmonės „Litware, Inc.‟ konfigūracijų teikėją. Jei nematote šio konfigūracijų teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijų teikėjo sukūrimas ir jo pažymėjimas kaip aktyvaus" veiksmus.  
2. Spustelėkite Ataskaitų konfigūracijos.
    * Sukursite konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį. Šis duomenų modelis bus vėliau naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.  

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Mokėjimai (supaprastas modelis)“.
    * Mokėjimai (supaprastintas modelis)  
3. Lauke „Aprašas“ įveskite „Mokėjimo modelio konfigūracija“.
    * Mokėjimo modelio konfigūracija  
    * Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas. Šis teikėjas galės prižiūrėti šią konfigūraciją. Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.  
4. Spustelėkite mygtuką „Kurti konfigūraciją“, kad užbaigtumėte konfigūracijos kūrimo užduotį

## <a name="create-a-data-model"></a>Sukurti duomenų modelį
    * Kuriate naują pasirinktos konfigūracijos duomenų modelį. Šios konfigūracijos versijos būsena bus „Juodraštis“.  
1. Spustelėkite Konstruktorius.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Nurodyti mokėjimo procese dalyvaujančios šalies struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas” įveskite „Šalis”.
    * Įrašas  
3. Spustelėkite Pridėti.
4. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
5. Lauke „Pavadinimas“ įveskite „Agentas“.
    * Vardas  
6. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
7. Spustelėkite Pridėti.
8. Lauke „Rasti” įveskite „Šalis”.
    * Įrašas  
9. Spustelėkite Rasti ankstesnį.

## <a name="define-the-bank-structure-for-this-model"></a>Nurodyti šio modelio banko struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Agentas“.
    * Agentas  
3. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
4. Spustelėkite Pridėti.
5. Lauke „Aprašas“ įveskite „Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas)“.
    * Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas).  
6. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
7. Lauke „Pavadinimas“ įveskite „Agentas“.
    * Vardas  
8. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
9. Spustelėkite Pridėti.
10. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
11. Lauke „Pavadinimas“ įveskite „SWIFT“.
    * SWIFT  
12. Spustelėkite Pridėti.
13. Lauke „Aprašas” įveskite „Banko identifikavimo kodas”.
    * Banko identifikavimo kodas  
14. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
15. Lauke „Pavadinimas“ įveskite „RoutingNumber“.
    * RoutingNumber  
16. Spustelėkite Pridėti.
17. Lauke „Aprašas” įveskite „Banko kodas”.
    * Įmonės kodas  
18. Spustelėkite Rasti ankstesnį.

## <a name="define-the-bank-account-structure-for-this-model"></a>Nurodyti šio modelio banko sąskaitos struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Sąskaita“.
    * Paskyra  
3. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
4. Spustelėkite Pridėti.
5. Lauke „Aprašas” įveskite „Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas”.
    * Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas.  
6. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
7. Lauke „Pavadinimas“ suveskite „Valiuta“.
    * Valiuta  
8. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
9. Spustelėkite Pridėti.
10. Lauke „Aprašas” įveskite „Valiutos kodas”.
    * Valiutos kodas  
11. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
12. Lauke „Pavadinimas“ įveskite „Numeris“.
    * Skaičius  
13. Spustelėkite Pridėti.
14. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
15. Lauke „Pavadinimas“, įveskite „IBAN“.
    * IBAN  
16. Spustelėkite Pridėti.
17. Lauke „Aprašas” įveskite „Tarptautinės banko sąskaitos numeris”.
    * Tarptautinės banko sąskaitos numeris  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Nurodyti kredito pervedimo mokėjimo tipo pranešimo struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.
3. Lauke „Pavadinimas“, įveskite „CustomerCreditTransferInitiation“.
    * CustomerCreditTransferInitiation  
4. Spustelėkite Pridėti.
5. Lauke „Rasti“, įveskite „CustomerCreditTransferInitiation“.
    * CustomerCreditTransferInitiation  
6. Spustelėkite Rasti ankstesnį.
7. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
8. Lauke „Pavadinimas“, įveskite „MessageIdentification“.
    * MessageIdentification  
9. Spustelėkite Pridėti.
10. Lauke „Aprašas“ įveskite „Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą“.
    * Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą.  
11. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
12. Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.
    * ProcessingDateTime  
13. Lauke „Prekės tipas“ pasirinkite „DateTime“.
14. Spustelėkite Pridėti.
15. Lauke „Aprašas“ įveskite „Mokėjimo pranešimo sukūrimo data ir laikas“.
    * Mokėjimo pranešimo sukūrimo data ir laikas.  
16. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
    * Nurodyti šio modelio mokėjimo operacijos struktūrą.  
17. Lauke „Pavadinimas“, įveskite „Mokėjimai“.
    * Mokėjimai  
18. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
19. Spustelėkite Pridėti.
20. Lauke „Aprašas“ įveskite „Dabartinio pranešimo mokėjimo eilutės“.
    * Dabartinio pranešimo mokėjimo eilutės  
21. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
22. Lauke „Pavadinimas“, įveskite „Kreditorius“.
    * Gavėjas  
23. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
24. Spustelėkite Pridėti.
25. Lauke „Aprašas“ įveskite „Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą“.
    * Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą.  
26. Spustelėkite Perjungti elemento nuorodą.
27. Lauke „Rasti” įveskite „Šalis”.
    * Įrašas  
28. Spustelėkite Rasti kitą.
29. Spustelėkite GERAI.
30. Lauke „Rasti“ įveskite „Mokėjimai“.
    * Mokėjimai  
31. Spustelėkite Rasti kitą.
32. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
33. Lauke „Pavadinimas“, įveskite „Skolininkas“.
    * Debitorius  
34. Spustelėkite Pridėti.
35. Lauke „Aprašas“ įveskite „Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą“.
    * Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą.  
36. Spustelėkite Perjungti elemento nuorodą.
37. Lauke „Rasti” įveskite „Šalis”.
    * Įrašas  
38. Spustelėkite Rasti kitą.
39. Spustelėkite GERAI.
40. Spustelėkite Rasti kitą.
41. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
42. Lauke „Pavadinimas“, įveskite „Aprašas“.
    * aprašymas  
43. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
44. Spustelėkite Pridėti.
45. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
46. Lauke „Pavadinimas“ suveskite „Valiuta“.
    * Valiuta  
47. Spustelėkite Pridėti.
48. Lauke „Aprašas” įveskite „Valiutos kodas”.
    * Valiutos kodas  
49. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
50. Lauke „Pavadinimas“, įveskite „TransactionDate“.
    * TransactionDate  
51. Lauke „Prekės tipas“ pasirinkite „Data“.
52. Spustelėkite Pridėti.
53. Lauke „Aprašas” įveskite „Operacijos data”.
    * Operacijos data  
54. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
55. Lauke „Pavadinimas“, įveskite „InstructedAmount“.
    * InstructedAmount  
56. Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.
57. Spustelėkite Pridėti.
58. Lauke „Aprašas“ įveskite „Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui”. Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta“.
    * Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui. Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta.  
59. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
60. Lauke „Pavadinimas“, įveskite „End2EndID“.
    * „End2EndID“  
61. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
62. Spustelėkite Pridėti.
63. Lauke „Aprašas“ įveskite „Unikali inicijuojančios šalies priskirta identifikacija”. Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista“.
    * Unikali inicijuojančios šalies priskirta identifikacija. Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista.  
64. Lauke „Pavadinimas“ įveskite „PaymentModel“.
    * Pavadinimas „PaymentModel“ sutampa su iš anksto nustatytomis mokėjimo formų sąsajomis.  
65. Spustelėkite Įrašyti.
66. Uždarykite puslapį.


