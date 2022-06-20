---
title: ER konkretaus domeno duomenų modelio kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti naują elektroninių ataskaitų (ER) konfigūraciją, kurioje būtų elektroninių mokėjimo dokumentų duomenų modelis.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c923ed6ec817d1f4ae6cd956c06b2156a6a61311
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908448"
---
# <a name="er-design-domain-specific-data-model"></a>ER konkretaus domeno duomenų modelio kūrimas

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį. Šis duomenų modelis vėliau bus naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.

    Pasirinkite pavyzdinės įmonės „Litware, Inc.‟ konfigūracijų teikėją Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijos teikėjo sukūrimas ir pažymėjimas aktyviu” veiksmus.  
    
2. Spustelėkite Ataskaitų konfigūracijos.

    Sukursite konfigūraciją, apimančią elektroninio mokėjimo dokumentų duomenų modelį. Šis duomenų modelis bus vėliau naudojamas kaip duomenų šaltinis, kai kursite mokėjimo dokumentų formatą.  

## <a name="create-a-new-data-model-configuration"></a>Sukurti naują duomenų modelio konfigūraciją
1. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Mokėjimai (supaprastas modelis)“.
3. Lauke „Aprašas“ įveskite „Mokėjimo modelio konfigūracija“.

    Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas. Šis teikėjas galės prižiūrėti šią konfigūraciją. Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.  

4. Spustelėkite mygtuką „Kurti konfigūraciją“, kad užbaigtumėte konfigūracijos kūrimo užduotį

## <a name="create-a-data-model"></a>Sukurti duomenų modelį
Kuriate naują pasirinktos konfigūracijos duomenų modelį. Šios konfigūracijos versijos būsena bus „Juodraštis“.  
1. Spustelėkite Konstruktorius.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Nurodyti mokėjimo procese dalyvaujančios šalies struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas” įveskite „Šalis”.
3. Spustelėkite Pridėti.
4. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
5. Lauke „Pavadinimas“ įveskite „Agentas“.
6. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
7. Spustelėkite Pridėti.
8. Lauke „Rasti” įveskite „Šalis”.
9. Spustelėkite Rasti ankstesnį.

## <a name="define-the-bank-structure-for-this-model"></a>Nurodyti šio modelio banko struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Agentas“.
3. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
4. Spustelėkite Pridėti.
5. Lauke „Aprašas“ įveskite „Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas)“.

    Šalies (skolininko / kreditoriaus) sąskaitą prižiūrinti finansų įstaiga (pvz., bankas).  

6. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
7. Lauke „Pavadinimas“ įveskite „Agentas“. 
8. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
9. Spustelėkite Pridėti.
10. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
11. Lauke „Pavadinimas“ įveskite „SWIFT“.
12. Spustelėkite Pridėti.
13. Lauke „Aprašas” įveskite „Banko identifikavimo kodas”. 
14. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
15. Lauke „Pavadinimas“ įveskite „RoutingNumber“.
16. Spustelėkite Pridėti.
17. Lauke „Aprašas” įveskite „Banko kodas”.
18. Spustelėkite Rasti ankstesnį.

## <a name="define-the-bank-account-structure-for-this-model"></a>Nurodyti šio modelio banko sąskaitos struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Pavadinimas“ įveskite „Sąskaita“. 
3. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
4. Spustelėkite Pridėti.
5. Lauke „Aprašas” įveskite „Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas”.

    Šalies sąskaitos finansų įstaigoje (pvz., banke) identifikavimas.  

6. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
7. Lauke „Pavadinimas“ suveskite „Valiuta“. 
8. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
9. Spustelėkite Pridėti.
10. Lauke „Aprašas” įveskite „Valiutos kodas”.
11. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
12. Lauke „Pavadinimas“ įveskite „Numeris“. 
13. Spustelėkite Pridėti.
14. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
15. Lauke „Pavadinimas“, įveskite „IBAN“. 
16. Spustelėkite Pridėti.
17. Lauke „Aprašas” įveskite „Tarptautinės banko sąskaitos numeris”.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Nurodyti kredito pervedimo mokėjimo tipo pranešimo struktūrą
1. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
2. Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.
3. Lauke „Pavadinimas“, įveskite „CustomerCreditTransferInitiation“.
4. Spustelėkite Pridėti.
5. Lauke „Rasti“, įveskite „CustomerCreditTransferInitiation“. 
6. Spustelėkite Rasti ankstesnį.
7. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
8. Lauke „Pavadinimas“, įveskite „MessageIdentification“. 
9. Spustelėkite Pridėti.
10. Lauke „Aprašas“ įveskite „Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą“.

    Tiesioginė nuoroda, kurią priskyrė nurodančioji šalis (ir išsiuntė kitai šaliai), kad būtų galima identifikuoti pranešimą.  

11. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
12. Lauke „Pavadinimas“, įveskite „ProcessingDateTime“.
13. Lauke „Prekės tipas“ pasirinkite „DateTime“.
14. Spustelėkite Pridėti.
15. Lauke „Aprašas“ įveskite „Mokėjimo pranešimo sukūrimo data ir laikas“. 
16. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.

    Nurodyti šio modelio mokėjimo operacijos struktūrą.  

17. Lauke „Pavadinimas“, įveskite „Mokėjimai“.
18. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
19. Spustelėkite Pridėti.
20. Lauke „Aprašas“ įveskite „Dabartinio pranešimo mokėjimo eilutės“.
21. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
22. Lauke „Pavadinimas“, įveskite „Kreditorius“. 
23. Lauke „Prekės tipas“ pasirinkite „Įrašas“.
24. Spustelėkite Pridėti.
25. Lauke „Aprašas“ įveskite „Šalis, kuriai reikia sumokėti tam tikrą pinigų sumą“. 
26. Spustelėkite Perjungti elemento nuorodą.
27. Lauke „Rasti” įveskite „Šalis”.
28. Spustelėkite Rasti kitą.
29. Spustelėkite Gerai.
30. Lauke „Rasti“ įveskite „Mokėjimai“.
31. Spustelėkite Rasti kitą.
32. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
33. Lauke „Pavadinimas“, įveskite „Skolininkas“. 
34. Spustelėkite Pridėti.
35. Lauke „Aprašas“ įveskite „Šalis, kuri (galutiniam) kreditoriui skolinga tam tikrą pinigų sumą“.
36. Spustelėkite Perjungti elemento nuorodą.
37. Lauke „Rasti” įveskite „Šalis”.
38. Spustelėkite Rasti kitą.
39. Spustelėkite Gerai.
40. Spustelėkite Rasti kitą.
41. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
42. Lauke „Pavadinimas“, įveskite „Aprašas“.
43. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
44. Spustelėkite Pridėti.
45. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
46. Lauke „Pavadinimas“ suveskite „Valiuta“.
47. Spustelėkite Pridėti.
48. Lauke „Aprašas” įveskite „Valiutos kodas”.
49. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
50. Lauke „Pavadinimas“, įveskite „TransactionDate“. 
51. Lauke „Prekės tipas“ pasirinkite „Data“.
52. Spustelėkite Pridėti.
53. Lauke „Aprašas” įveskite „Operacijos data”. 
54. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
55. Lauke „Pavadinimas“, įveskite „InstructedAmount“.  
56. Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.
57. Spustelėkite Pridėti.
58. Lauke „Aprašas“ įveskite „Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui”. Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta“.

    Pinigų suma, kurią, prieš atskaitant mokesčius, skolininkas turi perduoti kreditoriui. Suma turėtų būti išreikšta inicijuojančios šalies nurodyta valiuta.  

59. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
60. Lauke „Pavadinimas“, įveskite „End2EndID“. 
61. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
62. Spustelėkite Pridėti.
63. Lauke „Aprašas“ įveskite „Unikali inicijuojančios šalies priskirta identifikacija”. Ši identifikacija perduodama per visą tiesioginę grandinę ir lieka nepakeista“. 
64. Lauke „Pavadinimas“ įveskite „PaymentModel“.

    Pavadinimas „PaymentModel“ sutampa su iš anksto nustatytomis mokėjimo formų sąsajomis.  

65. Spustelėkite Įrašyti.
66. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
