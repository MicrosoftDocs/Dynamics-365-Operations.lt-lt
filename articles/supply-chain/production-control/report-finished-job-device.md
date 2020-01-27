---
title: Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį
description: Šioje temoje aprašomas baigtų produktų užbaigimo gamybos užsakyme procesas į atsargas, kai vieta valdoma pagal numerio lentelę.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935127"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį 

Procesas, vadinamas Paskelbimu, kad baigta, gamybos užsakyme baigia baigtus produktus į atsargas. Jei baigtas produktas yra įgalintas taikant pažangius sandėlio procesus, produktas paskelbiamas baigtu į vietą, vadinamą gamybos išeigos vieta. Norėdami gauti informacijos apie gamybos išeigos vietos nustatymą, žr. [Gamybos išeigos vieta](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Jei gamybos išeigos vieta yra kontroliuojama pagal numerio lentelę, tuomet paskelbiant produktą baigtu turi būti pateikta numerio lentelė. Laukas **Numerio lentelė** matomas raginime **Pranešti apie eigą** puslapyje **Užduoties kortelės įrenginys**. Šis laukas matomas tik raginime **Pranešti apie eigą**, kai pranešama apie gamybos užsakymo paskutinę operaciją ir gamybos užsakymo prekė įgalinta vykdant sandėlio valdymo procesus. 

Yra dvi galimybės numerio lentelei pateikti.
- Vartotojas numerio lentelės lauke pasirenka esamą numerio lentelę.
- Numerio lentelė automatiškai sugeneruojama pagal numeraciją ir pateikiama numerio lentelės lauke.

Parinktis, norint, kad numerio lentelė būtų sugeneruota automatiškai, yra konfigūruojama pasirinkus parinktį **Generuoti numerio lentelę** puslapyje **Konfigūruoti įrenginių užduoties kortelę**.
