---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 49025d0aa0f6a627b816a43dd4260449942b400c
ms.sourcegitcommit: ae04c7cb48f7ecafe71bbe77a0f97715e6290991
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973481"
---
# <a name="get-started-with-planning-optimization"></a>Darbo su planavimo optimizavimu pradžia

[!include [banner](../../includes/banner.md)]

Kaip buvo [nurodyta anksčiau](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), numatoma, kad „Planning Optimization“ pakeis esamą integruotą bendrojo planavimo mechanizmą.

Jei šiuo metu naudojate integruotą bendrojo planavimo mechanizmą, turite pradėti galvoti apie perėjimą prie „Planning Optimization“. Svarbu iš karto pradėti perėjimo procesą, nes tai gali turėti jūsų darbui, kai senesnė versija taps nebenaudojama. Tam, kad išvengtumėte problemų, kai senesnė versija taps nebenaudojama, primygtinai rekomenduojame baigti perėjimą iki 2020 m. gruodžio 1 d. 

„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, integruotame „Supply Chain Management“. Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus. „Planning Optimization“ funkcija šiuo metu nėra įjungta „Dynamics Lifecycle Services“ (LCS) esant numatytiesiems parametrams, todėl jūs turite galimybę atlikti savo vertinimą prieš įjungiant funkciją.

> [!NOTE]
> Jums reikia prašyti išimties, kad galėtumėte nepereiti prie „Planning Optimization“, jei bendrojo planavimo procesas neapima gamybos (bendrojo planavimo sugeneruotų suplanuotų gamybos užsakymų) ir jums reikia 10.0.15 arba senesnės integruoto bendrojo planavimo mechanizmo versijos. Pradedant nuo 10.0.16 versijos, bandant paleisti integruotą bendrąjį planavimą be suplanuotų gamybos užsakymų generavimo, bus rodoma klaida. „Planning Optimization“ turi būti naudojama visiems naujiems įdiegimams, kurie negeneruoja suplanuotų gamybos užsakymų atliekant bendrąjį planavimą. Esamų aplinkų savininkai, leisdami integruotą bendrojo planavimo mechanizmą be suplanuotų gamybos užsakymų, gaus laiškus, kuriuose pateikiama informacija apie išimties procesą. Rekomenduojame kartu su partneriu įvertinti ir planuoti perėjimą prie „Planning Optimization“.

Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus. Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Prieinamumas
Šiuo metu planavimo optimizavimas pasiekiamas tolesniuose „Azure” regionuose: Jungtinės Valstijos, Kanada, Europa, Jungtinė Karalystė ir Australija. Jei bandote įdiegti papildinį kitame geografiniame regione, LCS rodys pranešimą, nurodantį, kad šis regionas nepalaikomas.

Turėkite omenyje, kad planavimo optimizavimas nepalaiko vietinių visuotinių „Dynamics 365 Supply Chain Management” diegimų.

### <a name="licensing"></a>Licencijavimas

Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.

### <a name="install-the-add-in"></a>Papildinio įdiegimas

Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“. Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).

> [!NOTE]
> Planavimo optimizavimo reikalavimas yra su įgalintais LCS plačiai pasiekiama 2 ar aukštesnės pakopos aplinka (ne „OneBox” aplinka), turinti „Dynamics 365 Supply Chain Management” versiją 10.0.7 arba naujesnę versiją. Jei bandote įdiegti papildinį „OneBox” aplinkoje, diegimas nebus užbaigtas ir jį reikės atšaukti.

1. Prisijunkite prie LCS ir atsidarykite pageidaujamą aplinką.
1. Eikite į **Išsami informacija**.
1. Slinkite žemyn iki „FastTab“ **Aplinkos papildiniai**.
1. Pasirinkite **Diegti naują papildinį**.
1. Pasirinkite **Planning Optimization**.
1. Vadovaukitės diegimo vadovu ir sutikite su sąlygomis ir nuostatomis.
1. Pasirinkti **Diegti**.
1. „FastTab“ **Aplinkos papildiniai** turėtumėte matyti, kad diegiamas planavimo optimizavimas.
1. Po kelių minučių būsena **Diegiama** turėtų pakisti į **Įdiegta** (jums gali prireikti atnaujinti puslapį). Baigus diegti galite aktyvinti planavimo optimizavimą programoje „Dynamics 365 Supply Chain Management“.

### <a name="planning-optimization-integration"></a>„Planning Optimization“ integravimas

Norėdami sukonfigūruoti, ar planavimo optimizavimo papildinys turi būti naudojamas bendrajam planavimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Planavimo optimizavimo parametrai**.

#### <a name="connection-status"></a>Ryšio būsena

Ryšio būsena rodo dabartinę ryšio tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos būseną. Lentelėje pateiktos galimės reikšmės.

| Ryšio būsena | Aprašymas | Ar galima naudoti „Planning Optimization“? |
|---|---|---|
| Prisijungta | Jungtis nustatyta tarp „Planning Optimization“ paslaugos ir „Supply Chain Management“. | Taip |
| Įjungiamas ryšys | Šiuo metu apdorojama užklausa, ar įjungti ryšį su „Planning Optimization“ paslauga. | Ne |
| Atsijungta | Nėra ryšio su „Planning Optimization“ paslauga. Ryšį galima įjungti iš LCS, kaip pirmiau aprašyta šioje temoje. | Ne |
| Išjungiamas ryšys | Šiuo metu apdorojama užklausa, ar išjungti ryšį su „Planning Optimization“ paslauga. | Ne |
| Gavimo būsena | Sistema laukia būsenos informacijos iš „Planning Optimization“ paslaugos. | Ne |

#### <a name="the-use-planning-optimization-option"></a>„Planning Optimization“ parinkties naudojimas

Parinkties **Naudoti „Planning Optimization“** parametras apibrėžia, kuris planavimo mechanizmas naudojamas pagrindiniam planavimui:

- **Taip** – „Planning Optimization“ funkcija naudojama bendrajam planavimui.
- **Ne** – įdiegtas „Supply Chain Management“ planavimo mechanizmas naudojamas bendrajam planavimui.

> [!NOTE]
> Jei esamos paketinės užduotys, kurios buvo sukurtos įdiegtam „Supply Chain Management“ planavimo mechanizmui, yra suaktyvinamos, kai parinktis **Naudoti „Planning Optimization“** nustatyta į **Taip**, šių užduočių nepavyks atlikti.

### <a name="integration-with-the-setup"></a>Integravimas su sąranka

Jei „Planning Optimization“ peržiūra įjungta, bendrasis planavimas atliekamas naudojant „Planning Optimization“ papildinį. Šiuo atveju, bus paveikti bendrojo planavimo rezultatai ir funkcijos.

## <a name="additional-resources"></a>Papildomi ištekliai

[Peržiūros sąlygos ir nuostatos.](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
