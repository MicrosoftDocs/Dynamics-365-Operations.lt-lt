---
title: Tiekėjo darbo eiga
description: Keiskite tiekėjo informaciją ir naudokite darbo eigą, kad ją patvirtintumėte.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8f4fc24153842b2a108b13835e56e70177d7b53842cb15ea17f172da21ddc10d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777173"
---
# <a name="vendor-workflow"></a>Tiekėjo darbo eiga

[!include [banner](../includes/banner.md)]

Kai naudojama tiekėjo darbo eiga, konkrečių laukų pakeitimai siunčiami į darbo eigą patvirtinti prieš įtraukiant juos į tiekėją.

## <a name="set-up-the-vendor-workflow"></a>Tiekėjo darbo eigos nustatymas

Norėdami naudoti darbo eigos funkciją, turite ją įjungti.

1. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
2. Skirtuko **Bendra** „FastTab“ **Tiekėjo patvirtinimas** nustatykite parinktį **Įjungti tiekėjo patvirtinimą** į **Taip**.
3. Lauke **Duomenų objekto veikimo būdas** pasirinkite veikimo būdą, kuris turi būti naudojamas importuojant duomenis.

    - **Leisti keisti be patvirtinimo** – duomenų objektas gali atnaujinti tiekėjo įrašą neapdorodamas jo darbo eigoje.
    - **Atmesti pakeitimus** – tiekėjo įrašo keisti negalima. Nepavyks importuoti laukų, kurių darbo eiga įjungta.
    - **Kurti pakeitimų pasiūlymus** – bus pakeisti visi laukai, išskyrus laukus, kurių darbo eiga įjungta. Naujos tų laukų reikšmės bus įtrauktos į tiekėją kaip siūlomi pakeitimai, o darbo eiga bus paleista automatiškai.

4. Tiekėjo laukų sąraše pasirinkite žymės langelį **Įjungti**, pateiktą prie kiekvieno lauko, kuris turi būti patvirtintas prieš atliekant keitimus.
5. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų darbo eigos**.
6. Pasirinkite **Naujas**.
7. Pasirinkite **Tiekėjo siūlomų pakeitimų darbo eiga**. 
8. Nustatykite darbo eigą, kad ji atitiktų jūsų patvirtinimo procesą. Darbo eigos patvirtinimo elementas **Darbo eigos patvirtinimas dėl tiekėjo siūlomo pakeitimo** pritaikys pakeitimus tiekėjui.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Tiekėjo informacijos keitimas ir pakeitimų pateikimas į darbo eigą

Pakeitus lauką, kurio darbo eiga įjungta, rodomas puslapis **Siūlomi pakeitimai**. Šiame puslapyje rodoma pradinė lauko reikšmė ir jūsų įvesta nauja reikšmė. Nustatoma pradinė pakeisto lauko reikšmė. Būsenos pranešimas taip pat nurodo, kad pakeitimai nebuvo pateikti. 

Kiekvieną kartą pakeitus lauką, kurio darbo eiga įjungta, tas laukas įtraukiamas į sąrašą puslapyje **Siūlomi pakeitimai**. Norėdami atmesti siūlomą lauko reikšmę, naudokite mygtuką **Atmesti**, pateiktą šalia lauko sąraše. Norėdami atmesti visus keitimus, naudokite mygtuką **Atmesti visus keitimus** puslapio apačioje. Pasirinkite **Gerai** ir uždarykite puslapį.

Kai pateikiamas bent vienas siūlomas pakeitimas, veiksmų srityje rodomi du papildomi skirtukai: **Siūlomi pakeitimai** ir **Darbo eigos**.

1. Pasirinkite **Siūlomi pakeitimai**, kad atidarytumėte puslapį **Siūlomi pakeitimai** ir peržiūrėtumėte savo pakeitimus.
2. Pasirinkite **Darbo eiga \> Pateikti**, kad pateiktumėte pakeitimus į darbo eigą.

    Puslapio būsena pakeičiama į **Patvirtinimo laukiantys keitimai**.

Ši darbo eiga vykdoma pagal standartinį darbo eigų procesą. Tvirtintojas nukreipiamas į puslapį **Tiekėjas**, kuriame galima peržiūrėti pakeitimus puslapyje **Siūlomi pakeitimai**, pasirinkti **Darbo eiga \> Patvirtinti** ir patvirtinti darbo eigą. Viską patvirtinus, laukai yra atnaujinami jūsų pasiūlytomis reikšmėmis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]