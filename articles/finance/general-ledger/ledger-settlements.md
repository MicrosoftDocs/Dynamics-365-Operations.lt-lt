---
title: DK sudengimai
description: Šioje temoje paaiškinama, kaip, naudojantis DK sudengimų puslapiu, sudengti DK operacijas ir atšaukti sudengimus.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: d41a69bed3d1340736cc7df35aa3ded032d4d79d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445905"
---
# <a name="ledger-settlements"></a>DK sudengimai

[!include [banner](../includes/banner.md)]

DK sudengimai leidžia suderinti DK debeto ir kredito operacijas ir pažymėti jas kaip sudengtas. Tokiu būdu galite būti tikri, kad susijusios operacijos panaikintos. Atšaukti sudengimus galite ir tada, kai jie atlikti per klaidą.

## <a name="enable-advanced-ledger-settlements"></a>Išplėstinių didžiosios knygos sudengimų įgalinimas

Išplėstinių DK sudengimų puslapyje siūloma papildomų operacijų filtravimo ir pasirinkimo galimybių. Norėdami įgalinti išplėstinių DK sudengimų puslapį, atlikite šiuos veiksmus.

1. Paspauskite **Didžioji knyga** \> **DK nustatymas** \> **DK parametrai**. 
2. Skirtuke **DK sudengimai** nustatę funkcijos **Išplėstinis DK sudengimas** parinktį **Taip** įjunkite išplėstinio DK sudengimo funkciją. Dalyje **Periodinės užduotys** pasirinkus **DK sudengimai** bus naudojamas išplėstiniams sudengimams skirtas puslapis **DK sudengimai**. 
3. Turite įvesti kiekvieno sąskaitų plano DK sudengimams naudojamų sąskaitų sąrašą. Šis sąrašas naudojamas puslapyje **DK sudengimai** rodomam operacijų sąrašui filtruoti. Sąraše **Sąskaitų planas** pasirinkite sąskaitų planą, paskui, paspaudę **Nauja**, į sąrašą įtraukite naujų sąskaitų.

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a>Operacijų sudengimas naudojantis išplėstinių DK sudengimų puslapiu

Norėdami sudengti DK operacijas, atlikite toliau nurodytus veiksmus.

1. Paspauskite **Didžioji knyga** \> **Periodinės užduotys** \> **DK sudengimai**.
2. Nustatyti puslapio viršuje esančius filtrus:

    - Pasirinkite datos intervalą arba pasirinkite **Datos intervalo kodas**, kad datos intervalas būtų užpildomas automatiškai.
    - Pakeiskite registravimo sluoksnį, pagal tai, ko jums reikia.
    - Norėdami, kad DK sąskaita ir dimensijos būtų rodomos atskirai, pasirinkite finansinių dimensijų rinkinį.

3. Pasirinkite **Rodyti operacijas**, kad būtų rodomos visos jūsų nustatytus filtrus atitinkančios operacijos ir nustatant ankstesniame skyriuje pateiktą sąskaitų plano sąrašą nurodytų sąskaitų sąrašas. Pakeitus bet kurį filtrą arba dimensijų rinkinius, būtina dar kartą pasirinkti **Rodyti operacijas**.
4. Pasirinkite vieną ar kelias eilutes, kurias ketinate sudengti. Puslapio viršuje esančio lauko **Pasirinkta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pasirinktų eilučių sumos.
5. Pasirinkę operacijas, paspauskite **Žymėti pasirinktas**. Kiekvienos pasirinktos operacijos stulpelyje **Pažymėta** rodoma žymės varnelė. Be to, virš tinklelio esančio lauko **Pažymėta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pžymėtų eilučių sumos.
6. Kai **Pažymėta suma** vertė yra **0** (nulis), pasirinkite **Sudengti pažymėtas operacijas**. Pažymėtų operacijų būsena atnaujinama į **Sudengta**.

## <a name="make-transactions-easier-to-find"></a>Lengvesnė operacijų paieška

Puslapyje **DK sudengimai** pateikiama galimybių, kuriomis naudojantis paprasčiau pastebėti operacijas, kurias reikia sudengti.

- Naudojantis mygtuku **Panaikinti žymėjimus** išvalomi visų pažymėtų eilučių laukai **Pažymėta**.
- Naudodamiesi filtru **Pažymėta** galite filtruoti operacijas, pagal tai, ar jų laukas **Pažymėta** pažymėtas, ar ne.
- Naudodamiesi filtru **Būsena** galite filtruoti operacijas, pagal tai, ar jų būsena **Sudengta**, ar **Nesudengta**.
- Naudodamiesi mygtuku **Rūšiuoti pagal absoliučią sumą** galite rūšiuoti sumas pagal absoliučią vertę, kad galėtumėte sugrupuoti tos pačios sumos debetus ir kreditus.

## <a name="reverse-a-settlement"></a>Sudengimo atšaukimas

Galite atšaukti per klaida atliktą sudengimą.

1. Atlikite nuo 1 iki 3 skyriaus „Operacijų sudengimas naudojantis išplėstinių DK sudengimų puslapiu“ veiksmus, kad būtų rodomos ieškomos operacijos.
2. Filtre **Būsena** pasirinkite **Sudengta**.
3. Pasirinkite vieną ar kelias eilutes, kurias ketinate atkurti. Puslapio viršuje esančio lauko **Pasirinkta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pasirinktų eilučių sumos.
4. Pasirinkę operacijas, paspauskite **Žymėti pasirinktas**. Kiekvienos pasirinktos operacijos stulpelyje **Pažymėta** rodoma žymės varnelė. Be to, puslapio viršuje esančio lauko **Pažymėta suma** vertė didėja arba mažėja, priklausomai nuo bendros jūsų pažymėtų eilučių sumos.
5. Kai **Pažymėta suma** vertė yra **0** (nulis), pasirinkite **Atšaukti pažymėtas operacijas**. Pažymėtų operacijų būsena atnaujinama į **Nesudengta**.

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a>Į operacijų sąrašą įtrauktų sąskaitų sąrašo atnaujinimas

Paspauskite **DK sudengimo sąskaitos**, kad būtų atidarytas dialogo langas, kuriame galėsite redaguoti į operacijų sąrašą įtrauktas sąskaitas. Norėdami į sąrašą įtraukti naujų sąskaitų, paspauskite **Nauja**. Šis sąrašas naudojamas puslapyje **DK sudengimai** rodomam operacijų sąrašui filtruoti.
