---
title: Filtrų taikymas planui
description: Šioje temoje paaiškinama, kaip naudoti plano filtrus, kai naudojama „Planning Optimization“ funkcija.
author: t-benebo
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8679844ea40dd5af74102c37ab1e7d10b0681a0f
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468390"
---
# <a name="apply-filters-to-a-plan"></a>Filtrų taikymas planui

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
> Jei bendrojo **planavimo** **parametrų** puslapyje nustatote plano, kuris bendrojo planavimo parametrų puslapyje pasirinktas kaip dabartinis dinaminis bendrasis planas, plano filtrą, tada kintamo pagrindinio plano funkcija bus apribota filtruotomis prekėmis. Pavyzdžiui, jei atnaujinami prekės, kuris nėra plano filtro dalis, grynieji poreikiai, nebus sugeneruota jokių rezultatų.

## <a name="related-resources"></a>Susiję ištekliai

[„Planning Optimization“ apžvalga](planning-optimization-overview.md)

[Darbo su „Planning Optimization“ pradžia](get-started.md)

[Planavimo optimizavimo tinkamumo analizė](planning-optimization-fit-analysis.md)

[Plano retrospektyvos ir planavimo žurnalų peržiūra](plan-history-logs.md)

[Planavimo užduoties atšaukimas](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
