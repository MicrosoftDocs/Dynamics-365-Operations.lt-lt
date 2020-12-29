---
title: Bendrojo planavimo ir funkcionalumo daugelyje vietų apžvalga
description: Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas.
author: roxanadiaconu
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2adbac35d556314b3ec9916e2b7b2706ce3528c9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433829"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="36ac9-103">Bendrojo planavimo ir funkcionalumo daugelyje vietų apžvalga</span><span class="sxs-lookup"><span data-stu-id="36ac9-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36ac9-104">Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="36ac9-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="36ac9-105">Teritorijos dimensija yra privaloma, ir galite nustatyti, kad sandėlio dimensija būtų privaloma.</span><span class="sxs-lookup"><span data-stu-id="36ac9-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="36ac9-106">Kai dimensija yra privaloma, dimensijos vertė turi būti įvesta visoms atsargų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="36ac9-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="36ac9-107">Todėl bendrojo planavimo metu yra žinoma pradinė poreikio teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="36ac9-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="36ac9-108">Teritorijos dimensija taip pat yra nuosekli, kad išskleidimo pagal žemesnį poreikį metu teritorijos vertė nepasikeistų.</span><span class="sxs-lookup"><span data-stu-id="36ac9-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="36ac9-109">Kai sandėlis nenustatytas kaip privalomas, jis gali būti nežinomas pagal pradinį poreikį.</span><span class="sxs-lookup"><span data-stu-id="36ac9-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="36ac9-110">Planavimo mechanizmas turi nustatyti, kurį sandėlį naudoti pagal prekei nustatytus parametrus, individualius sandėlius ir užsakymo eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="36ac9-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="36ac9-111">Toliau pateikiamose temose aprašoma, kaip veikia planavimo mechanizmas, kai pasirenkami skirtingi parametrai naudojamam sandėliui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="36ac9-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="36ac9-112">Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="36ac9-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="36ac9-113">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="36ac9-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="36ac9-114">Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="36ac9-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="36ac9-115">Bendrasis vietos padengimo planavimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="36ac9-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="36ac9-116">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="36ac9-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



