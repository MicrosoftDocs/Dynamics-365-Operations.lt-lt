---
title: Bendrojo planavimo užduoties atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti aktyvią planavimo užduotį, kurios metu naudojama integruota planavimo funkcija.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
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
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: c04e2b2c0e5d7f28ea688578b3e1d7a1e1d9f6d3
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117453"
---
# <a name="cancel-a-master-planning-job"></a>Bendrojo planavimo užduoties atšaukimas

[!include [banner](../includes/banner.md)]

Naudojant „Microsoft Dynamics 365 Supply Chain Management“, atšaukti bendrojo planavimo užduotį galima keliais būdais. Pavyzdžiui, atšaukti bendrojo planavimo užduotį galbūt norėsite tada, jei ji buvo pradėta per klaidą arba jei ji vykdoma ilgiau, nei tikėtasi, ir norite ją baigti. Geriausias būdas atšaukti planavimo užduotį yra naudoti puslapį **Nebaigti planavimo procesai**. Alternatyvias parinktis, esančias puslapiuose **Paketinės užduotys** ir **Patobulintos paketinės užduotys**, reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.

## <a name="preferred-cancel-option"></a>Pageidaujama atšaukimo parinktis
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Bendrojo planavimo užduoties atšaukimas puslapyje **Nebaigti planavimo procesai**
1. Nueikite į **Bendrasis planavimas > Užklausos ir ataskaitos > Bendrasis planavimas > Nebaigti planavimo procesai**.
2. Pasirinkite eilutę, kurioje yra norimas atšaukti planavimo procesas.
3. Spustelėkite **Atšaukti**.

## <a name="additional-cancel-options"></a>Papildomos atšaukimo parinktys
Jas reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Bendrojo planavimo užduoties panaikinimas puslapyje **Paketinės užduotys**
1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Pasirinkite eilutę, kurioje yra norima panaikinti planavimo užduotis.
3. Spustelėkite **Naikinti**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Bendrojo planavimo užduoties nutraukimas puslapyje **Patobulintos paketinės užduotys**
1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Jei sąraše užduoties ID nerodomas, spustelėkite **Perjungti į patobulintą formą**, kitu atveju pereikite prie kito veiksmo.
3. Paketinę užduotį atidarykite. Spustelėkite paketinės užduoties, kurios elementus norite baigti, **ID**.
4. Dalyje **Paketinės užduotys** pasirinkite užduotis, kurias norite baigti.
5. „FastTab“ konteineryje **Paketinės užduotys** spustelėkite **Nutraukti**.
