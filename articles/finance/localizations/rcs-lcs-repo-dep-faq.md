---
title: „Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nebegalioja
description: Šioje temoje pateikiama informacija „Regulatory Configuration Service“ (LCS) saugojimo atšaukimą, kuris planuojamas kaip reguliavimo konfigūracijos tarnybos „Microsoft Dynamics Lifecycle Services“ (RCS) visuotinės saugyklos kūrimo dalis.
author: JaneA07
ms.date: 10/27/2021
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
ms.openlocfilehash: 68f1ed6a6d6bb0d15a81539da7f483ad71a4d696
ms.sourcegitcommit: 477efa4cb138f41d4f68bcd82552af3473bcc3d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2021
ms.locfileid: "7715235"
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

- Naudokite RCS, norėdami sukurti ir redaguoti ER konfigūracijas ir visuotines funkcijas.
- Perstumkite konfigūracijas tiesiogiai iš RCS dizainerio į prijungtą programą, pvz. Dynamics 365 Finance aplinką, kad galėtumėte greitai atlikti ir patikrinti savo konfigūracijų pakeitimus.
- Centralizuotai išsaugokite, dalinkitės ir valdykite ER konfigūracijų ir visuotinų funkcijų gyvavimo ciklą, naudojant visuotinės saugyklos centralizuotą saugyklą.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Vienkartinių ir vykdomų veiksmų patarimų

Šiame skyriuje aprašomas veiksmų, kuriuos reikia atlikti vieną kartą, rinkinys. Joje taip pat aprašomi veiksmai, kuriuos reikia atlikti nuolat.

### <a name="one-time-action"></a>Vieną kartą veiksmas

Importuokite visas reikiamas konfigūracijas iš LCS į RCS, tada publikuokite jas iš RCS į visuotinę saugyklą. Jei LCS naudojate konkretaus projekto turto bibliotekas, kad būtų saugoma išvestinės konfigūracijos, kol LCS vis dar pasiekiamas, reikia atlikti toliau nurodytus veiksmus.

1. Jei RCS egzemplioriaus dar nėra, sutkite vieną. Daugiau informacijos žr. [RCS apžvalga](rcs-overview.md).
2. Konfigūruotame RCS egzemplioriuje užregistruokite kiekvieną LCS projektą turto bibliotekoje, kurioje įtrauktos išvestinės ER konfigūracijos, užregistruokite atitinkamą LCS saugyklą.
3. Importuokite ER konfigūracijas iš LCS saugyklų į RCS. Daugiau informacijos žr. [ER konfigūracijų importavimas iš LCS](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Jei visuotinė saugykla nėra pateikiama automatiškai, užregistruokite ją RCS.
5. Įkelti visas iškeltas konfigūracijas iš dabartinio RCS egzemplioriaus į visuotinę saugyklą. Naudokite **Konfigūravimo paketų** funkciją, kuri padės įkelti. Daugiau informacijos rasite skyriuje [RCS bendros reprodukcijos naujinimas](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Eis į priekį

Vaizdo dizainerius RCS naudokite toliau pateikiamiems tikslams:

- Išplėskite "Microsoft" pateiktus šablonus.
- Sukurkite naujas konfigūracijas, kurių reikalauja jūsų organizacija.
- Pritaikykite visuotines funkcijas, skirtas Elektroninei SF išrašymui ir Mokesčių Skaičiavimo paslaugai.

Globalizacinę saugyklą naudokite toliau pateikiamiems tikslams:

- Gauti prieigą prie Microsoft pagamintų konfigūracijų ir visuotinų funkcijų.
- Įkelkite savo sukurtas arba išplėstas konfigūracijas į visuotiną saugyklą ir bendrinkite jas su savo organizacijos Dynamics 365 programos aplinka arba su išorinėmis organizacijomis. Norėdami gauti daugiau informacijos, žr. [RCS sukurkite ER konfigūraciją ir įkelkite į visuotinį atask.](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Ar šis pakeitimas reiškia, kad LCS negalima naudoti kaip centrinės konfigūracijų saugyklos?

Taip. Funkcijos, kurios leidžia įkelti konfigūracijas į projekto turto biblioteką LCS iš programėlių ir iš „Finance and Operations“ RCS, bus nebegaliojančios. Tačiau LCS vis tiek galėsite naudoti naršyklę, norėdami įkelti konfigūracijas į projekto turto biblioteką pagal poreikį.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Deja, RCS yra pakeitimo saugykla, skirta importuoti visuotinius šablonų failus. Nežinau, kad jis naudojamas konfigūracijų saugykloms. Kuris yra teisingas?

RCS yra kūrimo ir redagavimo ER konfigūracijų dizaino tarnyba. RCS turi savo saugyklą, kuri vadinama visuotine saugykla. Ši saugykla naudojama RCS sukurtoms konfigūracijų saugykloms. Baigus naudoti LCS kaip pasenusią saugyklą, "Microsoft" konfigūracijų bendroji saugykla bus vienas šaltinis. Norėdami importuoti visas konfigūracijas, kurių reikalaujate iš LCS į RCS, turite atlikti vienkartinį veiksmą ir publikuoti jas iš RCS į visuotinę saugyklą.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Koks siūlomas būdas saugoti konfigūracijas be LCS, kad būtų galima lengvai valdyti ir perkelti "tikrinti" ir "gamybos" konfigūracijas?

RCS naudoja prisijungusio *prašymo sąvoką*. Prijungta programa sudaro ryšį tarp RCS ir visų programėlių „Finance and Operations“ egzempliorių. Kadangi RCS galima naudoti konfigūracijoje redaguoti, prijungta programa gali būti naudojama konfigūracijose tiesiogiai iš dizainerio perstumti į „Finance and Operations“ programėlių aplinkas. Todėl galite greitai pakeisti ir patikrinti savo konfigūracijas, užuot kaupę LCS projektų lygio saugyklą.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Ar yra pavyzdžių, kurie parodo nustatymą ir valdymą?

Pavyzdžių nėra, tačiau norėdami perkelti savo konfigūracijas į RCS visuotinę saugyklą galite atlikti anksčiau šioje temoje aprašytus veiksmus.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Ar RCS yra būtina sąlyga norint konfigūruoti elektronines ataskaitas?

Taip. RCS apima galimybes, kurios palaiko visuotinų funkcijų, kurias naudoja visuotinės tarnybos, nustatymą, pvz., elektroninis SF išrašymas ir Mokesčių skaičiavimo paslauga. Tačiau paslauga turi tą pačią vaizdinio dizaino funkcionalumą, kuris leidžia išplėsti arba kurti naujas ER konfigūracijas. RCS taip pat suteikia ER konfigūracijų ir viuotinų funkcijų gyvavimo ciklo valdymą.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Kuriuose regionuose gali būti įdiegta RCS?

RCS yra prieinama šiuose Azure regionuose:

- Jungtinės Valstijos
- Indija
- Prancūzija
- Europa

Daugiau informacijos apie produkto palaikymą ieškokite [Dinaminių visuotinų paslaugų apžvalga](globalization-services-overview.md). Informacijos apie geografinę pagalbą rasite, [„Dynamics 365” ir „Power Platform”: Pasiekiamumas, duomenų vieta, kalba ir lokalizavimas](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Kokia yra RCS naudojimo kaina?

RCS ir visuotinė saugykla teikiama nemokamai kaip esamų Finance and Operations programos licencijų dalis. Nėra atskirų išlaidų, susietų su RCS dizaino tarnybos naudojimu ar konfigūracijų saugojimu visuotinėje saugykloje. Šiuo metu nėra jokio konfigūracijų ar susijusių programų skaičiaus apribojimo.
