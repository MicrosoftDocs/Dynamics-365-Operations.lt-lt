---
title: Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį
description: Šioje temoje aprašomas baigtų produktų užbaigimo gamybos užsakyme procesas į atsargas, kai vieta valdoma pagal numerio lentelę.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572134"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį 

Procesas, vadinamas Paskelbimu, kad baigta, gamybos užsakyme baigia baigtus produktus į atsargas. Jei baigtas produktas yra įgalintas taikant pažangius sandėlio procesus, produktas paskelbiamas baigtu į vietą, vadinamą gamybos išeigos vieta. Norėdami gauti informacijos apie gamybos išeigos vietos nustatymą, žr. [Gamybos išeigos vieta](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Norėdami atlikti šią užduotį, turite pasirinkti esamą numerio lentelės numerį. Jei nustatyta, kad gamybos išeigos vieta būtų sekama pagal numerio lentelę, tuomet, kai gamybos išeigos vieta paskelbiama baigta, turi būti įtrauktas numerio lentelės numeris. Laukas **Numerio lentelė** matomas raginime **Pranešti apie eigą** puslapyje **Užduoties kortelės įrenginys**. Šis laukas matomas tik raginime **Pranešti apie eigą**, kai pranešama apie paskutinę gamybos užsakymo operaciją. Laukas rodomas tik tuo atveju, jei sandėlio valdymo procesuose yra įjungtas gamybos užsakymo elementas. 
