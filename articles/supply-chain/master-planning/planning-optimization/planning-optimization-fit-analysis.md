---
title: Planavimo optimizavimo tinkamumo analizė
description: Šioje temoje paaiškinama, kaip patikrinti dabartinę sąranką ir duomenis, atsižvelgiant į „Planning Optimization“ funkcijos galimybes.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
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
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208759"
---
# <a name="planning-optimization-fit-analysis"></a>Planavimo optimizavimo tinkamumo analizė

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Norėdami pamatyti, kaip suderinama dabartinė sąranka ir duomenys „Planning Optimization“, eikite į **Bendrasis planavimas** \> **Sąranka** \> **„Planning Optimization“ tinkamumo analizė** ir pasirinkite **Atlikti analizę**. Jei atlikus analizę randama neatitikimų, jie pateikiami tame pačiame puslapyje. (Analizė gali užtrukti kelias minutes.)

> [!NOTE]
> Jei randama neatitikimų, vis tiek galite naudoti „Planning Optimization“ funkciją. Tinkamumo analizės rezultatai rodo tik tas vietas, kuriose planavimo paslauga neatsižvelgs į dabartinę sąranką. Kitaip tariant, rodomos vietos, kuriose gali būti nepaisoma kai kurių procesų arba jie gali būti nepalaikomi.

## <a name="analysis-results-example-1"></a>Analizės rezultatai: 1 pavyzdys

- **Funkcija:** gamyba
- **Problema:** prekės, kurių KS lygis didesnis nei nulis: 56
- **Paaiškinimas:** tinkamumo analizė rado 56 prekes, kurios turi komplektavimo specifikacijos (KS) nustatymus gamybai. Kadangi dabartinė „Planning Optimization“ versija nepalaiko gamybos, „Planning Optimization“ sugeneruos suplanuotus pirkimo užsakymus, ne suplanuotus gamybos užsakymus. Taip pat bus rodomas įspėjimas, kuriame išvardijamos paveiktos prekės.

### <a name="analysis-results-example-2"></a>Analizės rezultatai: 2 pavyzdys

- **Funkcija:** veiksmai
- **Išdavimas:** padengimo grupės su įjungtu veiksmų skaičiavimu: 6
- **Paaiškinimas:** tinkamumo analizė rado šešias padengimo grupes, kuriose veiksmų skaičiavimas įjungtas. Kadangi dabartinė „Planning Optimization“ versija nepalaiko veiksmų, bendrojo planavimo metu jokie veiksmai nebus generuojami.

## <a name="related-resources"></a>Susiję ištekliai

[Planavimo optimizavimo apžvalga](planning-optimization-overview.md)

[Darbo su „Planning Optimization“ pradžia](get-started.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Filtrų taikymas planui](plan-filters.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
