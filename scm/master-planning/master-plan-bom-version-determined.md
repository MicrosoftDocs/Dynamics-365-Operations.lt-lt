---
title: "Nustatyti KS versiją"
description: "Paklausos sprogimo, metu pažymėjus elemento numatytasis užsakymo tipą, gamybos, planavimo mechanizmas nustato galioja KS versiją remiantis svetainėje."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e4f5f02dfa986669decbc8854148b5eff928c2a
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-bom-version"></a>Nustatyti KS versiją

Paklausos sprogimo, metu pažymėjus elemento numatytasis užsakymo tipą, gamybos, planavimo mechanizmas nustato galioja KS versiją remiantis svetainėje. 

Teritorijos dimensija visada žinoma ir yra nurodyta poreikio operacijoje. Tolesnis procesas naudojamas nustatyti, kokią KS versiją naudoti.

-   Jei poreikio teritorijoje yra nurodyta prekės KS versija, naudojama konkrečios teritorijos KS.
-   Jei poreikio teritorijoje konkrečios teritorijos KS versija nenustatyta, naudojama bendroji KS. Bendrajame KS teritorija nenurodoma, tad jis tinka kelioms teritorijoms. Jei yra bendroji KS, naudojama ji.
-   Jei nėra galimos naudoti bendrojo KS versijos, poreikio išskleidimas sustoja.

Tinkama KS versija, konkrečios teritorijos ar bendroji, turi atitikti nurodytus datos ir kiekio kriterijus.




