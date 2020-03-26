---
title: Naujo el. prekybos nuomotojo diegimas
description: Šioje temoje aprašoma, kaip įdiegti naują el. prekybos nuomininką naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).
author: psimolin
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d5cf2804c44e81ad135a3248d38c228148b530cc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096683"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Naujo el. prekybos nuomotojo diegimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip įdiegti naują el. prekybos svetainę naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).

## <a name="overview"></a>Peržiūrėti

„Microsoft Dynamics“ „Lifecycle Services“ (LCS) yra debesiu pagrįsta bendradarbiavimo darbo sritis, kurią partneriai ir klientai gali naudoti savo projektams ir aplinkoms tvarkyti, peržiūrėti naujausią informaciją apie „Microsoft Dynamics“ produktus ir funkcijas bei kurti, sekti ir naršyti palaikymo incidentus. El. prekybos valdymo funkcijos integruotos į LCS.

Norėdami sužinoti daugiau apie LCS, žr. [„Lifecycle Services“ vartotojo vadovą](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Darbo pradžia

Kad galėtumėte paleisti el. prekybą, turite paleisti projektą, aplinką ir „Retail Cloud Scale Unit“ (RCSU). Norėdami atlikti LCS inicijavimą, turite turėti teises, skirtas projekto savininko arba aplinkos administratoriaus vaidmeniui. Palaikomos gamybos ir smėlio dėžės aplinkos topologijos.

Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Daugiau informacijos apie RCSU, žr. [„Retail Cloud Scale Unit“ inicijavimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>El. prekybos inicijavimas

Naudokite šią procedūrą paleisti el. prekybos funkciją esamoje aplinkoje.

Prieš pradėdami įsitikinkite, kad turite tokią reikalingą informaciją:

- RSCU, kuris bus naudojamas.
- „Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama el. prekybos sistemos administratoriams.
- „Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama įvertinimų ir apžvalgų moderatoriams.
- Domenai, kurie bus susieti su aplinka.

Be to, galite rinkti tokią pasirinktinę informaciją:

- „Azure AD“ verslo ir vartotojų (B2C) informaciją:

    - Nuomotojo pavadinimas.
    - Kliento ID.
    - Prisijungimo pasirinktinis domenas.
    - Atsakymo URL.
    - Registracijos prisijungimo strategijos ID.
    - Slaptažodžio nustatymo iš naujo strategijos ID.
    - Redagagavimo profilio strategijos ID.

[!NOTE]
Šią informaciją galima įtraukti vėliau, naudojant paslaugos užklausą.

Surinkę reikiamą informaciją, atlikite šiuos veiksmus, norėdami paleisti el. prekybą.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com).
1. Atidarykite projektą, kuriame yra aplinka, kurioje norima paleisti el. prekybą.
1. Skyriuje **Aplinkos** pasirinkite aplinką.
1. Dalyje **Aplinkos funkcijos** pasirinkite saitą **„Retail“ valdymas**.
1. Skirtuke **El. prekyba** pasirinkite **Sąranka**. Atsiranda dialogo langas, kuriame reikia įvesti informaciją, reikalingą kuriant.
1. Įveskite reikiamą informaciją ir pereikite prie tolesnio puslapio.
1. Kitame puslapyje įveskite reikiamą informaciją ir pateikite formą. Jūs grąžinami į skirtuką **El. prekyba**, kur turėtumėte matyti, kad inicijavimas pradėtas.
1. Norėdami peržiūrėti inicijavimo būseną, **atnaujinkite** arba grįžkite į skirtuką **El. prekyba**.
    
Paleidus el. prekybą iš LCS, sistema sukuria keletą komponentų, kurie būtini el. prekybai ir susieja juos su aplinka. Pasibaigus parengimui, skirtukas **El. prekyba** puslapyje **„Retail“ valdymas** atnaujinamas, kad atsispindėtų parengimą. Puslapyje pateikiami naujausi tinkinimo diegimai ir bet kurių kitų vykdomų diegimų būsena. Jame taip pat yra saitų į El. prekybos svetainę ir El. prekybos svetainių daryklę, kurioje kuriamos svetainės.

## <a name="access-site-builder"></a>Prieiga prie svetainių daryklės

Norėdami pasiekti svetainių daryklę, eikite į skirtuką **El. prekyba** LCS puslapyje **„Retail“ valdymas** ir pasirinkite saitą **El. prekybos svetainių valdymo įrankis**. Svetainių daryklės nukreipimo puslapyje rodomas nuomotojo lygio rodinys. Šiame puslapyje galite atlikti tolesnius veiksmus.

- Modifikuoti nuomotojo lygio parametrus.
- Pereiti į bet kurią sukurtą svetainę, kurią turite teisę peržiūrėti. 
- Naudotis peržiūros funkcijomis, pvz., priežiūra ir ataskaitų pateikimu.
- Sukurkite naują svetainę. Daugiau informacijos apie tai, kaip sukurti naują svetainę, žr. [El. prekybos svetainės kūrimas](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[El. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Interneto parduotuvės kanalo integravimas](online-stores.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
