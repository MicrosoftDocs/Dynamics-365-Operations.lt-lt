---
title: Darbo su „Planning Optimization“ pradžia
description: Šioje temoje aiškinama, kaip pradėti naudoti „Planning Optimization“ funkciją.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971469"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Darbo su „Planning Optimization“ pradžia

„Planning Optimization“ funkcija šiuo metu nepalaiko visų funkcijų, kurias galima naudoti planavimo mechanizme, kuris įdiegtas „Microsoft"Dynamics 365 Supply Chain Management“. Todėl svarbu, kad įvertintumėte, ar funkcijų rinkinys, kurį šiuo metu galima naudoti „Planning Optimization“, atitiks jūsų reikalavimus. „Planning Optimization“ funkcija pagal numatytuosius parametrus nėra įjungta „Dynamics Lifecycle Services“ (LCS). Todėl prieš ją įjungdami turite galimybę atlikti savo vertinimą.

Galiausiai, „Planning Optimization“ pakeis dabartinį įdiegtą „Supply Chain Management“ planavimo mechanizmą.

Prieš įjungiant „Planning Optimization“, primygtinai rekomenduojame įvertinti „Planning Optimization“ tinkamumo analizės rezultatus. Daugiau informacijos žr. [„Planning Optimization“ tinkamumo analizė](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Licencijavimas

Jei galite vykdyti bendrąjį planavimą naudodami esamą licenciją, jums nereikia įsigyti papildomos licencijos, kad galėtumėte pradėti naudoti „Planning Optimization“.

### <a name="install-the-add-in"></a>Papildinio įdiegimas

Norėdami naudoti „Planning Optimization“, įdiekite „Planning Optimization“ papildinį, skirtą „Dynamics 365 Supply Chain Management“. Galite pasiekti papildinį savo LCS projekte ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“ vartotojo sąsajoje (UI).

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

## <a name="related-resources"></a>Susiję ištekliai

[Peržiūros sąlygos ir nuostatos.](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
