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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8c633e09103c45aff5614270a94a3bfe4fc5e20
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="4ca9b-103">KS versijos išskleidimas</span><span class="sxs-lookup"><span data-stu-id="4ca9b-103">Explosion of a BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4ca9b-104">Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="4ca9b-105">Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="4ca9b-106">Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="4ca9b-107">Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="4ca9b-108">Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="4ca9b-109">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="4ca9b-110">Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="4ca9b-111">Teritorijos dimensija yra nuosekli.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-111">The site dimension is consistent.</span></span> <span data-ttu-id="4ca9b-112">Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="4ca9b-113">Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas.</span><span class="sxs-lookup"><span data-stu-id="4ca9b-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Poreikio išplėtimas naudojantis KS versija](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="4ca9b-115">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="4ca9b-115">See also</span></span>
--------

[<span data-ttu-id="4ca9b-116">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="4ca9b-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="4ca9b-117">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="4ca9b-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




