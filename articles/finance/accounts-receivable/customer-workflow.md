---
title: Kliento darbo eiga
description: Šiame straipsnyje pateikiama informacijos apie kliento darbo eigą. Galite keisti konkrečius kliento laukus ir, naudodami šią darbo eigą, tuos keitimus siųsti tvirtinti, prieš juos įtraukiant prie kliento.
author: abruer
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 883e77b5480a52201673e58a641c7180009a129c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864431"
---
# <a name="customer-workflow"></a>Kliento darbo eiga

[!include [banner](../includes/banner.md)]

Į 8.0.4 versiją įtraukta klientų darbo eiga. Galite keisti konkrečius kliento laukus ir, naudodami šią darbo eigą, tuos keitimus siųsti tvirtinti, prieš juos įtraukiant prie kliento.

## <a name="set-up-the-customer-workflow"></a>Kliento darbo eigos nustatymas

Kad galėtumėte naudoti kliento darbo eigos funkciją, turite ją įjungti.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
2. Norėdami įjungti šią funkciją, skirtuko **Bendra** „FastTab“ konteineryje **Klientų tvirtinimas** parinktį **Įjungti klientų tvirtinimus** nustatykite kaip **Taip**.
3. Lauke **Duomenų objektų veikimo būdas** pasirinkite vieną iš tolesnių veikimo būdų, kurį turi naudoti duomenų objektai, kai importuojami duomenys.

    - **Leisti keisti netvirtinant** – objektas kliento įrašą gali atnaujinti jo neapdorodamas darbo eigoje.
    - **Atmesti keitimus** – kliento įrašo keisti negalima. Įjungtų darbo eigos laukų importuoti nepavyks.
    - **Kurti keitimo pasiūlymus** – bus pakeisti visi laukai, išskyrus įjungtus darbo eigos laukus. Naujosios tų laukų reikšmės prie kliento bus įtrauktos kaip siūlomi keitimai, o darbo eiga bus pradėta automatiškai.

4. Tada kliento laukų sąraše prie kiekvieno lauko, kurį reikia patvirtinti, kad būtų galima atlikti keitimus, pažymėkite žymės langelį **Įjungti**.
5. Eikite į **Gautinos sumos \> Sąranka \> Gautinų sumų darbo eigos**.
6. Pasirinkite **Nauja**.
7. Pasirinkite **Siūlomų kliento keitimų darbo eiga**. 
8. Darbo eigą nustatykite taip, kad ji atitiktų jūsų tvirtinimo procesą. Darbo eigos **Siūlomo kliento keitimo darbo eigos tvirtinimas** tvirtinimo elementas keitimus pritaikys klientui.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Kliento informacijos keitimas ir keitimų teikimas į darbo eigą

Kai keičiate įjungtą darbo eigos lauką, pasirodo puslapis **Siūlomi keitimai**. Šiame puslapyje rodoma pradinė lauko reikšmė ir jūsų įvesta nauja reikšmė. Jūsų pakeistame lauke grąžinama pradinė jo reikšmė. Puslapyje būsenos pranešimas jums praneša, kad jūsų keitimai nepateikti.

Jums kaskart keičiant įjungtą darbo eigos lauką, jis įtraukiamas į siūlomų keitimų sąrašą. Norėdami atmesti siūlomą lauko reikšmę, naudokite prie sąraše esančio lauko esantį mygtuką **Atmesti**. Norėdami atmesti visus keitimus, naudokite puslapio apačioje esantį mygtuką **Atmesti visus keitimus**. Norėdami uždaryti puslapį, pasirinkite **Gerai**.

Kai turite bent vieną siūlomą keitimą, veiksmų srityje atsiranda du papildomi meniu: **Siūlomi keitimai** ir **Darbo eiga**.

1. Pasirinkdami **Siūlomi keitimai**, galite atidaryti puslapį **Siūlomi keitimai** ir peržiūrėti savo keitimus.
2. Pasirinkite **Darbo eiga \> Pateikti**, kad keitimus pateiktumėte į darbo eigą.

    Puslapio būsena pakeičiama į **Patvirtinimo laukiantys keitimai**.

Ši darbo eiga vykdoma pagal standartinį programos darbo eigų procesą. Tvirtintojas nukreipiamas į puslapį **Klientas**, kurio puslapyje **Siūlomi keitimai** jis gali peržiūrėti keitimus ir, pasirinkdamas **Darbo eiga \> Patvirtinti**, patvirtinti darbo eigą. Viską patvirtinus, laukai yra atnaujinami jūsų pasiūlytomis reikšmėmis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
