---
title: Darbo su bendruoju planavimu pradžia
description: Šiame straipsnyje paaiškinama, kaip pradėti naudoti bendrojo planavimo funkciją Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780308"
---
# <a name="get-started-with-master-planning"></a>Darbo su bendruoju planavimu pradžia

[!include [banner](../../includes/banner.md)]

Bendrąjį planavimą tiekimo grandinės valdymo metu teikia išorinė tarnyba, vadinama planavimo optimizavimo papildiniu Dynamics 365 Supply Chain Management. Šioje temoje paaiškinama, kaip gauti ir nustatyti šią paslaugą.

## <a name="availability"></a>Esamumas

Planavimo optimizavimas šiuo metu yra pasiekiamas šiose "Azure" geografiniuose diagramuose: Jungtinės Valstijos, Kanada, Brazilija, Europa, Prancūzija, Jungtinė Karalystė, Norvegija, Šveicarija, Australijos Ramiojo vandenynas, Japonija ir Indija. Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas. Daugiau informacijos apie "Azure" regionams ir susijusius regionus žr. ["Azure" geografiniai regionai](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.

## <a name="licensing"></a>Licencijavimas

Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.

## <a name="install-and-enable-planning-optimization"></a>„Planning Optimization“ diegimas ir įgalinimas

Norėdami naudoti „Planning Optimization”, turite įsitikinti, kad sistemoje yra visos būtinosios sąlygos, tada įgalinti jos licencijos raktą ir įdiegti „Planning Optimization” priedą, skirtą „Dynamics 365 Supply Chain Management”.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš diegiant „Planning Optimization” priedą, turi būti įgyvendintos šios būtinosios sąlygos:

- Privalote vykdyti „Supply Chain Management” su įgalinta LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinčia „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją. Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.

- Jūsų sistema turi būti nustatyta „Power Platform” integravimui. Norėdami gauti daugiau informacijos, žr. [Microsoft Power Platform integravimą su finansų ir operacijų programėle](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>„Planning Optimization“ licencijos įgalinimas

Norėdami naudoti „Planning Optimization”, turite įgalinti jo konfigūracijos raktą. Norėdami tai padaryti:

1. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Skirtuke **Konfigūracijos raktai** pasirinkite žymės langelį **Planavimo optimizavimas**.
1. Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="install-the-planning-optimization-add-in"></a>„Planning Optimization“ priedo diegimas

Turite įdiegti papildinį savo LCS projekte ir tada įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje.

Norėdami įdiegti „Planning Optimization“ priedą:

1. Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.
1. Eikite į **Išsami informacija**.
1. Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.
1. Pasirinkite **Diegti naują papildinį**.
1. Pasirinkite **Planavimo optimizavimas**.
1. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.
1. Pasirinkti **Diegti**.
1. „FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad planavimo optimizavimas yra diegiamas.
1. Po kelių minučių būsena **Diegiama** turėtų pasikeisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį). Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.

Pagrindinis „Planning Optimization“ papildinio diegimo tikslas yra susieti paslaugas ir aplinką. Dėl to, privalote įdiegti papildinį atskirai kiekvienoje aplinkoje, kurioje naudosite „Planning Optimization“ nepriklausomai nuo bet kokio kodo perkelto tarp aplinkų.

## <a name="integrate-planning-optimization-with-your-system"></a>„Planning Optimization” integravimas su jūsų sistema

Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.

### <a name="connection-status"></a>Ryšio būsena

Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną. Lentelėje pateiktos galimės reikšmės.

| Ryšio būsena | Aprašymas | Ar galima naudoti „Planning Optimization“? |
|---|---|---|
| Prisijungta | Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“. | Taip |
| Įjungiamas ryšys | Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga. | Ne |
| Atsijungta | Nėra ryšio su „Planning Optimization“ paslauga. Ryšį galima įjungti iš LCS, kaip anksčiau aprašyta šiame straipsnyje. | Ne |
| Išjungiamas ryšys | Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga. | Ne |
| Gavimo būsena | Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos. | Ne |

### <a name="the-use-planning-optimization-option"></a>„Planning Optimization“ parinkties naudojimas

Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:

- **Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.
- **Ne** – bendrasis planavimas naudojamas pasenusiam bendrojo planavimo moduliui.

Šis parametras taikomas visiems juridiniams subjektams (įmonėms). Negalima kai kuriuose juridiniuose subjektuose naudoti planavimo optimizavimo ir kitų juridinių subjektų pasenusio bendrojo planavimo modulio.

> [!NOTE]
> Jei esamos planavimo paketinės užduotys **, kurios buvo sukurtos pasenusiam bendrojo planavimo moduliui, suaktyvinami, kai nustatyta parinktis Naudoti planavimo optimizavimą** **kaip Taip**, šių užduočių atlikti nepavyks.

### <a name="integration-with-the-setup"></a>Integravimas su sąranka

Jei „Planning Optimization“ yra įjungtas, pagrindinis planavimas yra atliekamas naudojant „Planning Optimization“ papildinį. Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
