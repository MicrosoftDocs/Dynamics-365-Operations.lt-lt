--- 
title: "Išankstinis mokėjimas darbuotojui (Rytų Europa)"
description: "Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cc3ba589204f87b844ab4302e03105d2aa1de8d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="advance-payment-to-an-employee-eastern-europe"></a>Išankstinis mokėjimas darbuotojui (Rytų Europa)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip nustatyti ir registruoti išankstinio savininko operacijas. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje. Šią užduotį gali atlikti tik su juridiniais subjektais, kurių pagrindinis adresas yra Lenkijoje, Lietuvoje, Latvijoje, Estijoje, Čekijoje arba Vengrijoje. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-a-new-cash-account"></a>Naujo kasos kodo kūrimas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Kasos kodai.
2. Spustelėkite Naujas.
3. Lauke Grynieji pinigai įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Numeracijos grupė įveskite arba pasirinkite vertę.
6. Išplėskite skyrių Tikrinimas.
7. Lauke Valiuta įveskite arba pasirinkite vertę.
8. Lauke Neigiami grynieji pasirinkite Taip.
9. Spustelėkite Įrašyti.

## <a name="create-a-new-journal"></a>Naujo žurnalo kūrimas
1. Pasirinkite Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite Naujas.
7. Lauke Pavadinimas surinkite reikšmę.
8. Lauke „Žurnalo tipas“ pasirinkite parinktį.
9. Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.
10. Spustelėkite Įrašyti.

## <a name="create-an-advance-holder-group"></a>Išankstinių savininkų grupės kūrimas
1. Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Išankstinių savininkų grupės.
2. Spustelėkite Naujas.
3. Lauke Grupė įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.

## <a name="create-an-employee-posting-profile"></a>Darbuotojų registravimo šablono kūrimas
1. Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai > Darbuotojų registravimo šablonai.
2. Spustelėkite Naujas.
3. Lauke Registravimo šablonas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Galioja pasirinkite parinktį.
7. Lauke Suminė sąskaita nurodykite norimas reikšmes.
8. Spustelėkite Įrašyti.

## <a name="set-up-advance-holder-parameters"></a>Išankstinio savininko parametrų nustatymas
1. Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.
2. Spustelėkite skirtuką Išankstiniai savininkai.
3. Lauke Registravimo šablonas įveskite arba pasirinkite reikšmę.
4. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
5. Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.
6. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
7. Lauke Sąskaitos tipas pasirinkite parinktį.
8. Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.
9. Spustelėkite skirtuką Numeracijos.
10. Spustelėkite Įrašyti.

## <a name="set-up-a-cash-posting-profile"></a>Grynųjų registravimo šablono nustatymas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų registravimo šablonai.
2. Spustelėkite Naujas.
3. Lauke Grynųjų registravimas įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Galioja pasirinkite parinktį.
7. Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.
8. Spustelėkite Įrašyti.

## <a name="set-up-cash-and-bank-parameters"></a>Grynųjų pinigų ir banko parametrų nustatymas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.
2. Spustelėkite skirtuką Grynieji pinigai.
3. Lauke Grynieji pinigai įveskite arba pasirinkite reikšmę.
4. Lauke Grynųjų registravimas įveskite arba pasirinkite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite skirtuką Numeracijos.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Lauke Numeracijos kodas įveskite arba pasirinkite vertę.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Lauke Numeracijos kodas įveskite arba pasirinkite vertę.
11. Spustelėkite Įrašyti.

## <a name="set-up-terms-of-payment"></a>Nustatyti mokėjimo sąlygas
1. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.
2. Spustelėkite Redaguoti.
3. Lauke Iš išankstinio savininko pasirinkite Taip.
4. Spustelėkite Įrašyti.

## <a name="create-a-new-worker"></a>Naujo darbuotojo kūrimas
1. Pasirinkite Personalas > Darbuotojai > Darbuotojai.
2. Spustelėkite Naujas.
3. Lauke Vardas surinkite reikšmę.
4. Lauke Pavardė surinkite reikšmę.
5. Lauke Darbuotojo ID įveskite reikšmę.
6. Spustelėkite Samdyti naują darbuotoją.
7. Spustelėkite Įrašyti.

## <a name="set-up-a-worker-as-an-advance-holder"></a>Darbuotojo kaip išankstinio savininko nustatymas
1. Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.
2. Spustelėkite Redaguoti.
3. Lauke Grupė įveskite arba pasirinkite reikšmę.
4. Lauke Išankstinis savininkas pasirinkite Taip.
5. Spustelėkite Įrašyti.

## <a name="create-and-post-a-purchase-order-invoice"></a>Pirkimo užsakymo SF kūrimas ir registravimas
1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
4. Spustelėkite Gerai.
5. Lauke Eilutės arba antraštė pasirinkite parinktį.
6. Išplėskite skyrių Kaina ir nuolaida.
7. Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.
8. Lauke Išankstinis savininkas įveskite arba pasirinkite reikšmę.
9. Lauke Eilutės arba antraštė pasirinkite parinktį.
10. Sąraše pažymėkite pasirinktą eilutę.
11. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
12. Lauke Kiekis įveskite skaičių.
13. Lauke Vieneto kaina įveskite skaičių.
14. Spustelėkite Įrašyti.
15. Veiksmų srityje spustelėkite Pirkti.
16. Spustelėkite Patvirtinti.
17. Veiksmų srityje spustelėkite Sąskaita faktūra.
18. Spustelėkite Sąskaita faktūra.
19. Spustelėkite Numatyt. iš: gavimo dokumento kiekio, kad atidarytumėte išplečiamąjį dialogo langą.
20. Lauke Numatytasis eilučių kiekis pasirinkite parinktį.
21. Spustelėkite Gerai.
22. Lauke Numeris surinkite reikšmę.
23. Lauke Sąskaitos faktūros aprašas įveskite reikšmę.
24. Lauke SF data įveskite datą.
25. Lauke PVM registro data įveskite datą.
26. Lauke Gavimo dokumento data įveskite datą.
27. Spustelėkite Registruoti.

## <a name="balance-and-close-advance-holders-transactions"></a>Išankstinių savininkų operacijų balansavimas ir uždarymas
1. Pasirinkite Mokėtinos sumos > Nustatymas > Išankstiniai savininkai.
2. Spustelėkite Operacijos.
3. Uždarykite puslapį.
4. Spustelėkite Balansas.
5. Spustelėkite Uždaryti per banką.
6. Lauke Automatinis pasirinkite Taip.
7. Lauke Suma, skirta perkelti įveskite skaičių.
8. Spustelėkite GERAI.
9. Spustelėkite Uždaryti per kasą.
10. Lauke Automatinis pasirinkite Taip.
11. Spustelėkite GERAI.
12. Uždarykite puslapį.
13. Spustelėkite Operacijos.


