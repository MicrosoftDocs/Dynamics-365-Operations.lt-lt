---
title: Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį
description: Šioje temoje aprašomas baigtų produktų užbaigimo gamybos užsakyme procesas į atsargas, kai vieta valdoma pagal numerio lentelę.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211174"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="3d4e3-103">Paskelbimas, kad baigta, numerio lentelės valdomoje vietoje naudojant užduoties kortelės įrenginį</span><span class="sxs-lookup"><span data-stu-id="3d4e3-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="3d4e3-104">Procesas, vadinamas Paskelbimu, kad baigta, gamybos užsakyme baigia baigtus produktus į atsargas.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="3d4e3-105">Jei baigtas produktas yra įgalintas taikant pažangius sandėlio procesus, produktas paskelbiamas baigtu į vietą, vadinamą gamybos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="3d4e3-106">Norėdami gauti informacijos apie gamybos išeigos vietos nustatymą, žr. [Gamybos išeigos vieta](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="3d4e3-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="3d4e3-107">Jei gamybos išeigos vieta yra kontroliuojama pagal numerio lentelę, tuomet paskelbiant produktą baigtu turi būti pateikta numerio lentelė.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="3d4e3-108">Laukas **Numerio lentelė** matomas raginime **Pranešti apie eigą** puslapyje **Užduoties kortelės įrenginys**.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="3d4e3-109">Šis laukas matomas tik raginime **Pranešti apie eigą**, kai pranešama apie gamybos užsakymo paskutinę operaciją ir gamybos užsakymo prekė įgalinta vykdant sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="3d4e3-110">Yra dvi galimybės numerio lentelei pateikti.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="3d4e3-111">Vartotojas numerio lentelės lauke pasirenka esamą numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="3d4e3-112">Numerio lentelė automatiškai sugeneruojama pagal numeraciją ir pateikiama numerio lentelės lauke.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="3d4e3-113">Parinktis, norint, kad numerio lentelė būtų sugeneruota automatiškai, yra konfigūruojama pasirinkus parinktį **Generuoti numerio lentelę** puslapyje **Konfigūruoti įrenginių užduoties kortelę**.</span><span class="sxs-lookup"><span data-stu-id="3d4e3-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
