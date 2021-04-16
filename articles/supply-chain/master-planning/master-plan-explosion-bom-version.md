---
title: KS versijos išskleidimas
description: Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 367b662a43b3c3255632f20aeb821b973b04d890
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833598"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="12051-103">KS versijos išskleidimas</span><span class="sxs-lookup"><span data-stu-id="12051-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12051-104">Šiame straipsnyje paaiškinamas bendrojo planavimo scenarijus, apimantis KS versijos išskleidimą.</span><span class="sxs-lookup"><span data-stu-id="12051-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="12051-105">Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="12051-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="12051-106">Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį.</span><span class="sxs-lookup"><span data-stu-id="12051-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="12051-107">Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas.</span><span class="sxs-lookup"><span data-stu-id="12051-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="12051-108">Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku.</span><span class="sxs-lookup"><span data-stu-id="12051-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="12051-109">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="12051-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="12051-110">Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.</span><span class="sxs-lookup"><span data-stu-id="12051-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="12051-111">Teritorijos dimensija yra nuosekli.</span><span class="sxs-lookup"><span data-stu-id="12051-111">The site dimension is consistent.</span></span> <span data-ttu-id="12051-112">Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.</span><span class="sxs-lookup"><span data-stu-id="12051-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="12051-113">Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas.</span><span class="sxs-lookup"><span data-stu-id="12051-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Poreikio išplėtimas naudojantis KS versija](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="12051-115">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="12051-115">Additional resources</span></span>
--------

[<span data-ttu-id="12051-116">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="12051-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="12051-117">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="12051-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]