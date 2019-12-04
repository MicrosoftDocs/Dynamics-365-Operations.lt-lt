---
title: Bendrojo planavimo ir funkcionalumo daugelyje vietų apžvalga
description: Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0b715e0c17263519a9bb1b3780170812271d93d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813758"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="fdc0e-103">Bendrojo planavimo ir funkcionalumo daugelyje vietų apžvalga</span><span class="sxs-lookup"><span data-stu-id="fdc0e-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdc0e-104">Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="fdc0e-105">Teritorijos dimensija yra privaloma, ir galite nustatyti, kad sandėlio dimensija būtų privaloma.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="fdc0e-106">Kai dimensija yra privaloma, dimensijos vertė turi būti įvesta visoms atsargų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="fdc0e-107">Todėl bendrojo planavimo metu yra žinoma pradinė poreikio teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="fdc0e-108">Teritorijos dimensija taip pat yra nuosekli, kad išskleidimo pagal žemesnį poreikį metu teritorijos vertė nepasikeistų.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="fdc0e-109">Kai sandėlis nenustatytas kaip privalomas, jis gali būti nežinomas pagal pradinį poreikį.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="fdc0e-110">Planavimo mechanizmas turi nustatyti, kurį sandėlį naudoti pagal prekei nustatytus parametrus, individualius sandėlius ir užsakymo eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="fdc0e-111">Toliau pateikiamose temose aprašoma, kaip veikia planavimo mechanizmas, kai pasirenkami skirtingi parametrai naudojamam sandėliui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="fdc0e-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="fdc0e-112">Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="fdc0e-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fdc0e-113">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="fdc0e-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="fdc0e-114">Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="fdc0e-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="fdc0e-115">Bendrasis vietos padengimo planavimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="fdc0e-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="fdc0e-116">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="fdc0e-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



