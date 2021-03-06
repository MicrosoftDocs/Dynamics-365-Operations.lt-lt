---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. rugsėjo 10 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462034"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. rugsėjo 10 d.)

**8.1.138.0 versija**

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent: Core HR“ funkcijos.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Leiskite nedarbo laiko užklausose naudoti konkretų dienos laiką (pusdieniai)

Jei atostogos ir neatvykimas nustatomas taip, kad nedarbo laiko pateikiamas dienomis, dabar galite įjungti pusės dienos apibrėžtį. Tada, kai vartotojai pateikia nedarbo laiko užklausas, jie gali nurodyti, ar jie teikia užklausą dėl pirmosios, ar dėl antrosios dienos pusės.

Pagal numatytuosius parametrus ši parinktis yra išjungta. Tam, kad darbuotojai galėtų kreiptis dėl pirmosios arba antrosios dienos pusės, turite įjungti šią parinktį personalo parametrų srityje **Atostogos ir neatvykimas**.

Šios funkcijos saugos teisė yra Tvarkyti personalo parametrus.

## <a name="validation-of-leave-and-absence-entries"></a>Atostogų ir neatvykimo įrašų tikrinimas

Atsižvelgiant į tai, kaip sukonfigūruotos atostogos, darbuotojai, kurie bando teikti užklausą dėl nedarbo laiko, kuris ilgesnis už jų darbo dieną, gaus įspėjamąjį pranešimą. Kitaip tariant, jie įspėjami, jei jie bando pateikti ilgesnio nei bet kuri visa darbo diena nedarbo laiko užklausą.

Šis tikrinimas yra visada įjungtas. Kai tik darbuotojai viršija nurodytą darbo dienos ribą, teikdami nedarbo laiko užklausą jie gauna įspėjimą.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Darbo eigų sąlyginių sakinių papildomi laukai

Papildomi laukai įtraukti į sąlyginius sakinius ir vietos rezervavimo ženklus keliose „Core HR“ darbo eigose.

Toliau nurodyti lauki įtraukti į kompensacijos, atleidimo ir perkėlimo darbo eigas.

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Pozicija
- Sąjunga
- Skyrius
- PositionType
- CompLocation
- Pareigos
- Darbas
- JobType
- JobFamily
- JobFunction

Toliau nurodyti lauki įtraukti į pareigų darbo eigą

- Pozicija
- Sąjunga
- Skyrius
- PositionType
- CompLocation
- Pareigos
- Darbas
- JobType
- JobFamily
- JobFunction

Sąlyginių sakinių ir vietos rezervavimo ženklų laukai pasiekiami visiems vartotojams, kurie turi teisę konfigūruoti pirmiau minėtas darbo eigas.

## <a name="navigation-to-attract-from-personnel-management"></a>„Attract“ atidarymas personalo valdymo srities

Jei „Attract“ nenustatyta, personalo valdymo sritis **Samdytini kandidatai** nurodo vartotojams pradėti „Attract“, o ne parodo pranešimą „Turinio, kurį būtų galima pateikti, nerasta.“

## <a name="other-changes"></a>Kiti pakeitimai

Šiame leidime įtraukti keli papildomi klaidų ištaisymai.

- Kai pasamdomas rangovas, skirtukas **Kompensacija** nebus rodomas užklausos / veiksmo puslapyje.
- Atleidimo užklausos proceso metu negalima tęsti tol, kol visuose būtinuose laukuose bus duomenų.
- Rikiavimo tvarkos ir datos rodymo problemos personalo valdymo analizėje išspręstos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]