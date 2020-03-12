---
title: „Planning Optimization“ apžvalga
description: Šioje temoje pateikiama „Planning Optimization“ funkcijos apžvalga.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076160"
---
# <a name="planning-optimization-overview"></a>„Planning Optimization“ apžvalga

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

„Planning Optimization“ papildinys, skirtas „Microsoft Dynamics 365 Supply Chain Management“, leidžia, kad pagrindinių duomenų skaičiavimas vyktų ne „Dynamics 365 Supply Chain Management“ ir susijusioje SQL duomenų bazėje. „Planning Optimization“ funkcijos privalumai yra geresnis veikimas ir minimalus poveikis SQL duomenų bazei pagrindinių planavimų vykdymų metu. Greitą planavimo vykdymą galima atlikti netgi darbo valandomis, kad planuotojai galėtų nedelsiant reaguoti į poreikį ir parametrų keitimus.

Norėdami naudoti „Planning Optimization“, turite įdiegti „Planning Optimization“ papildinį iš savo projekto, esančio „Microsoft Dynamics Lifecycle Services“ (LCS), ir įjungti „Planning Optimization“ funkciją „Supply Chain Management“. Daugiau informacijos žr. [Darbo su „Planning Optimization“ pradžia](get-started.md).

Toliau pateiktame paveiksle parodyta, kaip veikia „Planning Optimization“ funkcija darbo valandomis.

![„Planning Optimization“ vykdymo darbo valandomis privalumas](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Geresnis efektyvumas

„Planning Optimization“ gali būti naudojama scenarijuose, kuriuose yra ilgai vykdomų bendrųjų planų. Jis konkrečiai sukurtas itin greitiems skaičiavimams, kuriuose yra daug duomenų. Kadangi jis yra sukurtas kaip aukšto mastelio multinuomotojų paslauga, keli egzemplioriai vienu metu gali dirbti kartu, kad apskaičiuotų planą. Be to, planavimo paslauga pašalina bendrojo planavimo įkėlimą iš sistemos ir dirba su duomenų srautu, kuris sumažina serverio apkrovą.

„Planning Optimization“ funkcija gali padėti pasiekti toliau nurodytus tikslus.

- Pagerinti planavimo efektyvumą per trumpesnį vykdymo laiką.
- Sumažinti poveikį kitiems procesams bendrojo planavimo vykdymo metu.
- Dažniau atlikti planavimo vykdymus. (Neriboja dienos vykdymų skaičius.)
- Užtikrinti, kad būsimas verslo augimas neperaugs planavimo sistemos.

## <a name="architecture-and-data-flow"></a>Architektūra ir duomenų srautai

Kai „Planning Optimization“ papildinys įdiegtas iš LCS, sukuriamas saugus ryšys su „Planning Optimization“ paslauga. Paslauga yra toje pačioje duomenų centro šalyje ar regione kaip ir susijęs „Supply Chain Management“ egzempliorius. Nustačius „Planning Optimization“, vykdant bendrąjį planavimą, pagrindiniai duomenys ir operacijų duomenys siunčiami iš „Supply Chain Management“ į „Planning Optimization“ tarnybą.

Jei išdiegiamas „Planning Optimization“ papildinys, pašalinami visi susiję „Planning Optimization“ paslaugos duomenys.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Aukšto lygio duomenų srautas, skirtas regeneravimo vykdymui

1. „Supply Chain Management“ klientas siunčia signalą, kad pateiktų užklausą dėl planavimo vykdymo iš „Planning Optimization“.
2. „Planning Optimization“ prašo reikiamų duomenų per integruotą jungtį.
3. SQL duomenų bazė siunčia prašomą informaciją apie nustatymus, pagrindinius ir operacijų duomenis į „Planning Optimization“ per jungtį. Jungtis verčia informaciją tarp „Supply Chain Management“ ir „Planning Optimization“ paslaugos.
4. „Planning Optimization“ paslauga atmintyje turi su planavimu susijusių duomenų ir atlieka reikalingus skaičiavimus.
5. Planavimo rezultatas per jungtį siunčiamas į „Supply Chain Management“ duomenų bazę. Rezultatuose pateikiama informacija, pvz., suplanuoti užsakymai ir iškvietimo informacija. „Planning Optimization“ siunčia signalą į „Supply Chain Management“, kad nurodytų, jog planavimo vykdymas baigtas. Jis taip pat siunčia visus susijusius pranešimus ir įspėjimus.

Tolesnėje iliustracijoje pavaizduotas duomenų srautas.

![Duomenų srautas, skirtas regeneravimo vykdymui](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Susiję ištekliai

[Darbo su „Planning Optimization“ pradžia](get-started.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
