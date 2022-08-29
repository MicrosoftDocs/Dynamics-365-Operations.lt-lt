---
title: Darbo su planavimo optimizavimu pradžia
description: Šiame straipsnyje paaiškinama, kaip pradėti naudoti planavimo optimizavimo funkciją.
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
ms.openlocfilehash: 629a84135434ad79f8397649ee9a4a62e49751d9
ms.sourcegitcommit: 14a27b776befbc6793390f97e8fb0279c0ea18c1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/15/2022
ms.locfileid: "9295936"
---
# <a name="get-started-with-planning-optimization"></a>Darbo su planavimo optimizavimu pradžia

[!include [banner](../../includes/banner.md)]

Kaip buvo [nurodyta anksčiau](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), numatoma, kad „Planning Optimization“ pakeis esamą integruotą bendrojo planavimo mechanizmą.

Jei šiuo metu naudojate integruotą bendrojo planavimo mechanizmą, turite pradėti galvoti apie perėjimą prie „Planning Optimization“. Svarbu iš karto pradėti, nes kitu atveju jūsų operacijos gali būti paveiktos, kai atšaukiamas vykdymas (nors vykdymas šiuo metu nesuplanuotas). Primygtinai patariame baigti perkėlimą, kai tik planavimo optimizavimas palaiko jūsų reikalingas priemones, kad pradėtumėte naudotis daugelio našumo patobulinimų ir kitų naujų galimybių, kurias teikia nauja tarnyba, galimybėmis.

„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, integruotame „Supply Chain Management“. Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus. „Planning Optimization“ funkcija šiuo metu nėra įjungta „Dynamics Lifecycle Services“ (LCS) esant numatytiesiems parametrams, todėl jūs turite galimybę atlikti savo vertinimą prieš įjungiant funkciją.

> [!NOTE]
> Jums reikia prašyti išimties, kad galėtumėte nepereiti prie „Planning Optimization“, jei bendrojo planavimo procesas neapima gamybos (bendrojo planavimo sugeneruotų suplanuotų gamybos užsakymų) ir jums reikia 10.0.15 arba senesnės integruoto bendrojo planavimo mechanizmo versijos. Pradedant nuo 10.0.16 versijos, bandant paleisti integruotą bendrąjį planavimą be suplanuotų gamybos užsakymų generavimo, bus rodoma klaida. „Planning Optimization“ turi būti naudojama visiems naujiems įdiegimams, kurie negeneruoja suplanuotų gamybos užsakymų atliekant bendrąjį planavimą. Esamų aplinkų savininkai, leisdami integruotą bendrojo planavimo mechanizmą be suplanuotų gamybos užsakymų, gaus laiškus, kuriuose pateikiama informacija apie išimties procesą. Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.

Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus. Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).

## <a name="availability"></a>Prieinamumas

Planavimo optimizavimas šiuo metu yra pasiekiamas šiose "Azure" geografiniuose diagramuose: Jungtinės Valstijos, Kanada, Brazilija, Europa, Prancūzija, Jungtinė Karalystė, Australija, Azijos Ramiojo vandenynas, Japonija ir Indija. Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas. Daugiau informacijos apie "Azure" regionams ir susijusius regionus žr. ["Azure" geografiniai regionai](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.

## <a name="licensing"></a>Licencijavimas

Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.

## <a name="install-and-enable-planning-optimization"></a>„Planning Optimization“ diegimas ir įgalinimas

Norėdami naudoti „Planning Optimization”, turite įsitikinti, kad sistemoje yra visos būtinosios sąlygos, tada įgalinti jos licencijos raktą ir įdiegti „Planning Optimization” priedą, skirtą „Dynamics 365 Supply Chain Management”.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš diegiant „Planning Optimization” priedą, turi būti įgyvendintos šios būtinosios sąlygos:

- Privalote vykdyti „Supply Chain Management” su įgalinta LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinčia „Dynamics 365 Supply Chain Management” 10.0.7 arba naujesnę versiją. Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.

- Jūsų sistema turi būti nustatyta „Power Platform” integravimui. Norėdami gauti daugiau informacijos, žr.[Microsoft Power Platform integravimą su finansų ir operacijų programėle](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

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
- **Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.

Šis parametras taikomas visiems juridiniams subjektams (įmonėms). Kai kuriuose juridiniuose subjektuose negalima naudoti Planavimo optimizavimo ir įtaisytojo bendrojo planavimo kituose juridiniuose subjektuose.

> [!NOTE]
> Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.

### <a name="integration-with-the-setup"></a>Integravimas su sąranka

Jei „Planning Optimization“ yra įjungtas, pagrindinis planavimas yra atliekamas naudojant „Planning Optimization“ papildinį. Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.

## <a name="additional-resources"></a>Papildomi ištekliai

[Peržiūros sąlygos ir nuostatos.](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

