---
title: "Bendrasis planavimas ir kelių teritorijų funkcija"
description: "Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04f61141497570577520fe9146fbd1464f31062e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="c4c06-103">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="c4c06-103">Master planning and multisite functionality</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4c06-104">Atliekant bendrąjį planavimą, atsižvelgiama į teritorijos ir sandėlio atsargų dimensijas.</span><span class="sxs-lookup"><span data-stu-id="c4c06-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="c4c06-105">Teritorijos dimensija yra privaloma, ir galite nustatyti, kad sandėlio dimensija būtų privaloma.</span><span class="sxs-lookup"><span data-stu-id="c4c06-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="c4c06-106">Kai dimensija yra privaloma, dimensijos vertė turi būti įvesta visoms atsargų operacijoms.</span><span class="sxs-lookup"><span data-stu-id="c4c06-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="c4c06-107">Todėl bendrojo planavimo metu yra žinoma pradinė poreikio teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="c4c06-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="c4c06-108">Teritorijos dimensija taip pat yra nuosekli, kad išskleidimo pagal žemesnį poreikį metu teritorijos vertė nepasikeistų.</span><span class="sxs-lookup"><span data-stu-id="c4c06-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="c4c06-109">Kai sandėlis nenustatytas kaip privalomas, jis gali būti nežinomas pagal pradinį poreikį.</span><span class="sxs-lookup"><span data-stu-id="c4c06-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="c4c06-110">Planavimo mechanizmas turi nustatyti, kurį sandėlį naudoti pagal prekei nustatytus parametrus, individualius sandėlius ir užsakymo eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="c4c06-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="c4c06-111">Toliau pateikiamose temose aprašoma, kaip veikia planavimo mechanizmas, kai pasirenkami skirtingi parametrai naudojamam sandėliui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="c4c06-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="c4c06-112">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="c4c06-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c4c06-113">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="c4c06-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c4c06-114">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="c4c06-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c4c06-115">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="c4c06-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c4c06-116">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="c4c06-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



