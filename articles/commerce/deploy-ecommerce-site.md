---
title: Talpinkite naują e-komercijos nuomotoją
description: Šiame skyriuje aprašoma, kaip talpinti naują „Dynamics 365 Commerce“ e-komercijos svetainę naudojant „Microsoft Dynamics  Lifecycle Services“ (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801954"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Talpinkite naują e-komercijos nuomotoją

[!include [banner](includes/banner.md)]

Šiame skyriuje aprašoma, kaip talpinti naują „Dynamics 365 Commerce“ e-komercijos svetainę naudojant „Microsoft Dynamics  Lifecycle Services“ (LCS).

„Microsoft Dynamics“ „Lifecycle Services“ (LCS) yra debesiu pagrįsta bendradarbiavimo darbo sritis, kurią partneriai ir klientai gali naudoti savo projektams ir aplinkoms tvarkyti, peržiūrėti naujausią informaciją apie „Microsoft Dynamics“ produktus ir funkcijas bei kurti, sekti ir naršyti palaikymo incidentus. E-komercijos valdymo funkcijos yra integruotos į LCS.

Norėdami sužinoti daugiau apie LCS, žr. [„Lifecycle Services“ vartotojo vadovą](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Pradėta

Prieš tai kai pradėsite e-komerciją, turite pradėti projektą, aplinką ir Retail Cloud Scale Unit (RCSU). Norėdami atlikti LCS inicijavimą, turite turėti teises, skirtas projekto savininko arba aplinkos administratoriaus vaidmeniui. Palaikomos gamybos ir smėlio dėžės aplinkos topologijos.

Daugiau informacijos apie aplinkas ieškokite [aplinkos planavime](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Daugiau informacijos apie RCSU, žr. [„Retail Cloud Scale Unit“ inicijavimas](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Pradėkite e-komerciją

Naudokite šią procedūrą siekiant pradėti e-komercijos funkciją esančioje aplinkoje.

Prieš pradėdami įsitikinkite, kad turite tokią reikalingą informaciją:

- RSCU, kuris bus naudojamas.
- „Microsoft Azure Active Directory“ saugos grupė, kuri bus naudojama e-komercijos sistemos administratorių.
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
    - Redagavimo profilio strategijos ID.

> [!NOTE]
> Šią informaciją galima įtraukti vėliau, naudojant paslaugos užklausą.

Jums surinkus reikiamą informaciją, atlikite šiuos žingsnius, kad pradėtumėte e-komerciją.

1. Prisijunkite prie [LCS](https://lcs.dynamics.com).
1. Atidarykite projektą, kuriame yra aplinka, kurioje norite pradėti e-komerciją.
1. Skyriuje **Aplinkos** pasirinkite aplinką.
1. Dalyje **Aplinkos funkcijos** pasirinkite saitą **„Retail“ valdymas**.
1. Skirtuke **El. prekyba** pasirinkite **Sąranka**. Atsiranda dialogo langas, kuriame reikia įvesti informaciją, reikalingą kuriant.
1. Įveskite reikiamą informaciją ir pereikite prie tolesnio puslapio.
1. Kitame puslapyje įveskite reikiamą informaciją ir pateikite formą. Jūs grąžinami į skirtuką **El. prekyba**, kur turėtumėte matyti, kad inicijavimas pradėtas.
1. Norėdami peržiūrėti inicijavimo būseną, **atnaujinkite** arba grįžkite į skirtuką **El. prekyba**.
    
Kai e-komercija yra pradėta iš LCS, sistemos suteikia keletą komponentų, kurie yra būtini e-komercijai ir susieja juos su aplinka. Pasibaigus parengimui, skirtukas **El. prekyba** puslapyje **„Retail“ valdymas** atnaujinamas, kad atsispindėtų parengimą. Puslapyje pateikiami naujausi tinkinimo diegimai ir bet kurių kitų vykdomų diegimų būsena. Ji taip pat apima nuorodas į e-komercijos saitą ir komercijos saito kūrimo įrankį, kuriame saitai yra leidžiami.

## <a name="access-commerce-site-builder"></a>Prieiga prie komercijos saito kūrimo įrankio

Norėdami patekti į komercijos saito kūrimo įrankį, eikite į **e-komercijos** skirtuką  **Mažmeninis valdymas** puslapį LCS ir pasirinkite **e-komercijos saito valdymo įrankio** nuorodą. Svetainių daryklės nukreipimo puslapyje rodomas nuomotojo lygio rodinys. Šiame puslapyje galite atlikti tolesnius veiksmus.

- Modifikuoti nuomotojo lygio parametrus.
- Pereiti į bet kurią sukurtą svetainę, kurią turite teisę peržiūrėti. 
- Naudotis peržiūros funkcijomis, pvz., priežiūra ir ataskaitų pateikimu.
- Sukurkite naują svetainę. Dėl daugiau informacijos apie tai, kaip sukurti naują saitą, žr. [Sukurkite e-komercijos svetainę](create-ecommerce-site.md) . 

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Sukurkite e-komercijos saitą](create-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[robots.txt failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
