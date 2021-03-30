---
title: KS versijos išskleidimas
description: Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220853"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="80bea-103">KS versijos išskleidimas</span><span class="sxs-lookup"><span data-stu-id="80bea-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80bea-104">Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.</span><span class="sxs-lookup"><span data-stu-id="80bea-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="80bea-105">Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="80bea-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="80bea-106">Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį.</span><span class="sxs-lookup"><span data-stu-id="80bea-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="80bea-107">Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas.</span><span class="sxs-lookup"><span data-stu-id="80bea-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="80bea-108">Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku.</span><span class="sxs-lookup"><span data-stu-id="80bea-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="80bea-109">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="80bea-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="80bea-110">Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.</span><span class="sxs-lookup"><span data-stu-id="80bea-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="80bea-111">Teritorijos dimensija yra nuosekli.</span><span class="sxs-lookup"><span data-stu-id="80bea-111">The site dimension is consistent.</span></span> <span data-ttu-id="80bea-112">Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.</span><span class="sxs-lookup"><span data-stu-id="80bea-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="80bea-113">Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas.</span><span class="sxs-lookup"><span data-stu-id="80bea-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Poreikio išplėtimas naudojantis KS versija](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="80bea-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="80bea-115">Additional resources</span></span>
--------

[<span data-ttu-id="80bea-116">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="80bea-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="80bea-117">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="80bea-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]