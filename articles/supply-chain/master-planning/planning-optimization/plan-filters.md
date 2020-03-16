---
title: Filtrų taikymas planui
description: Šioje temoje paaiškinama, kaip naudoti plano filtrus, kai naudojama „Planning Optimization“ funkcija.
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
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
ms.openlocfilehash: ca28953846b4f1978a453d2ab2aa9759e4f45221
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076114"
---
# <a name="apply-filters-to-a-plan"></a>Filtrų taikymas planui

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Kai naudojama „Planning Optimization“ funkcija, galite taikyti plano filtrą. **Plano filtras** bus taikomas visuomet, kai vykdomas bendrasis planavimas. **Plano filtras** yra naudingas, kai norite apriboti planą tam tikrai prekių grupei, ir įsitikinti, kad nė viena kita prekė nebūtų įtraukta į gautą bendrąjį planavimą.

Jei taikomas **Plano filtras** ir apdorojimo filtras vykdant bendrąjį planavimą, į planavimo vykdymą įtraukiamas tik šių dviejų filtrų sutapimo taškas.

**Plano filtras** pasiekiamas pasirinkus **Bendrieji planai**, kai naudojamas planavimo optimizavimas.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Plano filtras nustatytas taip, kad jį sudarytų A, B ir C prekės. Tada bendrojo planavimo vykdymai taikomi tam pačiam planui, bet taikomi skirtingi padorojimo filtrai:

- **Apdorojimo filtras, kuriame yra D prekė:** nėra suplanuotų prekių, nes nėra sutapimo taško tarp plano filtro ir padorojimo filtro.
- **Apdorojimo filtras, kuriame yra A ir D prekės:** tik A prekė įtraukiama į planavimo vykdymą, nes D prekė nėra plano filtro dalis.
- **Apdorojimo filtras, kuriame yra B prekė:** tik B prekė įtraukiama į planavimo vykdymą ir ankstesnė A prekės planavimo išvestis yra išsaugoma.
- **Apdorojimo filtras, kuriame yra visos prekės (tuščias filtras):** A, B ir C yra įtraukiamos į planavimo vykdymą, o ankstesnio prekių A ir B planavimo išvestis perrašoma.

> [!NOTE]
> Neturėtumėte nustatyti plano filtro plane, kuris yra pasirinktas kaip **Dabartinis dinaminis bendrasis planas** puslapyje **Bendrojo planavimo parametrai**. Kitu atveju dinaminio bendrojo plano funkcija bus apribota filtruotomis prekėmis. Pavyzdžiui, jei atnaujinami prekės, kuris nėra plano filtro dalis, grynieji poreikiai, nebus sugeneruota jokių rezultatų.

## <a name="related-resources"></a>Susiję ištekliai

[„Planning Optimization“ apžvalga](planning-optimization-overview.md)

[Darbo su „Planning Optimization“ pradžia](get-started.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)
