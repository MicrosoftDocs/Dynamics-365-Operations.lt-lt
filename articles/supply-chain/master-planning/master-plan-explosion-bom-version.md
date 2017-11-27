---
title: "KS versijos išskleidimas"
description: "Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="df4bd-103">KS versijos išskleidimas</span><span class="sxs-lookup"><span data-stu-id="df4bd-103">Explosion of a BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="df4bd-104">Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.</span><span class="sxs-lookup"><span data-stu-id="df4bd-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="df4bd-105">Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="df4bd-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="df4bd-106">Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį.</span><span class="sxs-lookup"><span data-stu-id="df4bd-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="df4bd-107">Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas.</span><span class="sxs-lookup"><span data-stu-id="df4bd-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="df4bd-108">Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku.</span><span class="sxs-lookup"><span data-stu-id="df4bd-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="df4bd-109">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="df4bd-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="df4bd-110">Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.</span><span class="sxs-lookup"><span data-stu-id="df4bd-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="df4bd-111">Teritorijos dimensija yra nuosekli.</span><span class="sxs-lookup"><span data-stu-id="df4bd-111">The site dimension is consistent.</span></span> <span data-ttu-id="df4bd-112">Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.</span><span class="sxs-lookup"><span data-stu-id="df4bd-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="df4bd-113">Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas.</span><span class="sxs-lookup"><span data-stu-id="df4bd-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Poreikio išplėtimas naudojantis KS versija](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="df4bd-115">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="df4bd-115">See also</span></span>
--------

[<span data-ttu-id="df4bd-116">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="df4bd-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="df4bd-117">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="df4bd-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




