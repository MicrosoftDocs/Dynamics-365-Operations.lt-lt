---
title: Atšaukti užduotį, kuri buvo sukurta naudojant pasenusią bendrojo planavimo sistemą
description: Šiame straipsnyje paaiškinama, kaip atšaukti aktyvią planavimo užduotį, kuri naudoja pasenusią bendrojo planavimo sistemą.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740883"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Atšaukti užduotį, kuri buvo sukurta naudojant pasenusią bendrojo planavimo sistemą

[!include [banner](../includes/banner.md)]

Yra kelios pasirinktys atšaukti užduotį, kuri buvo sukurta naudojant pasenusią bendrojo planavimo sistemą. Pavyzdžiui, atšaukti bendrojo planavimo užduotį galbūt norėsite tada, jei ji buvo pradėta per klaidą arba jei ji vykdoma ilgiau, nei tikėtasi, ir norite ją baigti.

Geriausias būdas atšaukti planavimo užduotį yra naudoti puslapį **Nebaigti planavimo procesai**. Alternatyvias parinktis, esančias puslapiuose **Paketinės užduotys** ir **Patobulintos paketinės užduotys**, reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.

## <a name="preferred-cancel-option"></a>Pageidaujama atšaukimo parinktis

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Atšaukti bendrojo planavimo užduotį neužbaigto planavimo procesų puslapyje

1. Nueikite į **Bendrasis planavimas > Užklausos ir ataskaitos > Bendrasis planavimas > Nebaigti planavimo procesai**.
2. Pasirinkite eilutę, kurioje yra norimas atšaukti planavimo procesas.
3. Pasirinkite **Atšaukti**.

## <a name="additional-cancel-options"></a>Papildomos atšaukimo parinktys

Jas reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Bendrojo planavimo užduoties panaikinimas puslapyje **Paketinės užduotys**

1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Pasirinkite eilutę, kurioje yra norima panaikinti planavimo užduotis.
3. Pasirinkite **Naikinti**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Bendrojo planavimo užduoties nutraukimas puslapyje **Patobulintos paketinės užduotys**

1. Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.
2. Jei sąraše užduoties ID nerodomas, spustelėkite **Perjungti į patobulintą formą**, kitu atveju pereikite prie kito veiksmo.
3. Paketinę užduotį atidarykite. Pasirinkite paketinės **užduoties, kurioje yra norimos pabaigti užduotys, ID**.
4. Dalyje **Paketinės užduotys** pasirinkite užduotis, kurias norite baigti.
5. Pasirinkite **Keisti būseną**, pasirinkite **Atšaukti** ir spustelėkite **Gerai**.
6. „FastTab“ konteineryje **Paketinės užduotys** spustelėkite **Nutraukti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]