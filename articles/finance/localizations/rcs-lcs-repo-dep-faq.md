---
title: „Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nebegalioja
description: Šioje temoje pateikiama informacija „Regulatory Configuration Service“ (LCS) saugojimo atšaukimą, kuris planuojamas kaip reguliavimo konfigūracijos tarnybos „Microsoft Dynamics Lifecycle Services“ (RCS) visuotinės saugyklos kūrimo dalis.
author: JaneA07
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: abaeb34db1d209fa8e5cc83a98c333f42e91f2d2
ms.sourcegitcommit: 7cda434becd198c1cd405e001289777ae7a24fe1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6127924"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nebegalioja

[!include [banner](../includes/banner.md)]

Galiojimo laiko tarnybų (LCS) naudojimas kaip elektroninių ataskaitų (ER) konfigūracijų saugyklos saugykla „Microsoft Dynamics Lifecycle Services“ yra pasenusi. Šis pasikeitimas bus atlikti šiais pakeitimais:

- „Microsoft" pagamintos konfigūracijos, nebebus publikuojamos LCS bendrai naudojamų „Microsoft Dynamics 365“ bendrintų turtų bibliotekoje. Todėl jos bus publikuojamos tik naudojant RCS visuotinę saugyklą. Tačiau konfigūracijos „Dynamics AX 2012“ toliau bus publikuojamos bendrintoje turto bibliotekoje LCS iki palaikymo gyvavimo ciklas AX 2012 baigsis.
- Funkcijos, kurios leidžia įkelti konfigūracijas į projekto turto biblioteką LCS iš programėlių ir iš „Finance and Operations“ RCS, bus neaktyvintos. Tačiau LCS vis tiek galėsite naudoti naršyklę, norėdami įkelti konfigūracijas į projekto turto biblioteką. Todėl vis tiek galėsite įtraukti konfigūracijas į LCS, kad jas būtų galima įtraukti į sprendimų paketus.
- Importuoti konfigūracijas iš LCS, kurios tam tikrą laiką bus ir toliau galimos ir palaikomos programėlėse, ir „Finance and Operations“ RCS. Nepaisant to, funkcija galiausiai nebegalios. (Tiksli nurašyta data bus vėlesnė.)

## <a name="deprecation-notice"></a>Pranešimas apie nebegaliojimą

LCS naudojimas kaip saugykla buvo naudojamas kaip [pašalintos arba pasenusios funkcijos – „Dynamics 365 Finance“ LCS pranešimai dėl pasenusios funkcijos](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Suplanuota pasenusi data yra 2022 m. balandžio 1 d.

## <a name="key-features"></a>Pagrindinės funkcijos

- Konfigūracijai kurti ir redaguoti galite naudoti RCS. Tada galite tiesiogiai šias konfigūracijas stumti iš dizainerio į prijungtą programą. Todėl galite greitai keisti ir tikrinti savo konfigūracijas.
- Visuotinė saugykla yra centralizuota visų ER konfigūracijų saugykla.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Vienkartinių ir vykdomų veiksmų patarimų

Šiame skyriuje aprašomas veiksmų, kuriuos reikia atlikti vieną kartą, rinkinys. Joje taip pat aprašomi veiksmai, kuriuos reikia atlikti nuolat.

### <a name="one-time-action"></a>Vieną kartą veiksmas

Importuokite visas reikiamas konfigūracijas iš LCS į RCS, tada publikuokite jas iš RCS į visuotinę saugyklą. Jei LCS naudojate konkretaus projekto turto bibliotekas, kad būtų saugoma išvestinės konfigūracijos, kol LCS vis dar pasiekiamas, reikia atlikti toliau nurodytus veiksmus.

1. Jei RCS egzemplioriaus dar nėra, sutkite vieną. Daugiau informacijos žr. [RCS apžvalga](rcs-overview.md).
2. Konfigūruotame RCS egzemplioriuje užregistruokite kiekvieną LCS projektą turto bibliotekoje, kurioje įtrauktos išvestinės ER konfigūracijos, užregistruokite atitinkamą LCS saugyklą.
3. Importuokite ER konfigūracijas iš LCS saugyklų į RCS. Daugiau informacijos žr. [ER konfigūracijų importavimas iš LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Jei visuotinė saugykla nėra pateikiama automatiškai, užregistruokite ją RCS.
5. Įkelti visas iškeltas konfigūracijas iš dabartinio RCS egzemplioriaus į visuotinę saugyklą. Naudodami **konfigūracijos paketus vartotojas gali įkelti visas konfigūracijas į GR vienoje operacijos priemonėje, kad padėtų** įkelti. Daugiau informacijos rasite skyriuje [RCS bendros reprodukcijos naujinimas](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Eis į priekį

Norėdami sukurti visas naujas konfigūracijas, naudokite vaizdo dizainerius RCS. Tada naujinkite bendros saugyklos konfigūravimus talpinimui. Norėdami gauti daugiau informacijos, žr. [RCS sukurkite ER konfigūraciją ir įkelkite į visuotinį atask.](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Ar šis pakeitimas reiškia, kad LCS negalima naudoti kaip centrinės konfigūracijų saugyklos?

Taip. Funkcijos, kurios leidžia įkelti konfigūracijas į projekto turto biblioteką LCS iš programėlių ir iš „Finance and Operations“ RCS, bus nebegaliojančios. Tačiau LCS vis tiek galėsite naudoti naršyklę, norėdami įkelti konfigūracijas į projekto turto biblioteką pagal poreikį.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Deja, RCS yra pakeitimo saugykla, skirta importuoti visuotinius šablonų failus. Nežinau, kad jis naudojamas konfigūracijų saugykloms. Kuris yra teisingas?

RCS yra kūrimo ir redagavimo ER konfigūracijų dizaino tarnyba. RCS turi savo saugyklą, kuri vadinama visuotine saugykla. Ši saugykla naudojama RCS sukurtoms konfigūracijų saugykloms. Baigus naudoti LCS kaip pasenusią saugyklą, "Microsoft" konfigūracijų bendroji saugykla bus vienas šaltinis. Norėdami importuoti visas konfigūracijas, kurių reikalaujate iš LCS į RCS, turite atlikti vienkartinį veiksmą ir publikuoti jas iš RCS į visuotinę saugyklą.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Koks siūlomas būdas saugoti konfigūracijas be LCS, kad būtų galima lengvai valdyti ir perkelti "tikrinti" ir "gamybos" konfigūracijas?

RCS naudoja prisijungusio *prašymo sąvoką*. Prijungta programa sudaro ryšį tarp RCS ir visų programėlių „Finance and Operations“ egzempliorių. Kadangi RCS galima naudoti konfigūracijoje redaguoti, prijungta programa gali būti naudojama konfigūracijose tiesiogiai iš dizainerio perstumti į „Finance and Operations“ programėlių aplinkas. Todėl galite greitai pakeisti ir patikrinti savo konfigūracijas, užuot kaupę LCS projektų lygio saugyklą.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Ar yra pavyzdžių, kurie parodo nustatymą ir valdymą?

Pavyzdžių nėra, tačiau norėdami perkelti savo konfigūracijas į RCS visuotinę saugyklą galite atlikti anksčiau šioje temoje aprašytus veiksmus.
