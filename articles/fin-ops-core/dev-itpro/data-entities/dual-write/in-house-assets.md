---
title: Vidaus paslaugų turtas
description: Šioje temoje aprašoma, kaip galite naudoti „Microsoft Dynamics 365 Field Service“, kad būtų galima aptarnauti kliento turtą ir turtą įmonėje.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d4d681b2362c90b69007ea44c01c886f96cc1db1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568083"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="3f1f9-103">Vidaus paslaugų turtas</span><span class="sxs-lookup"><span data-stu-id="3f1f9-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3f1f9-104">„Microsoft Dynamics 365 Field Service“ sukurta klientų turtui aptarnauti.</span><span class="sxs-lookup"><span data-stu-id="3f1f9-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="3f1f9-105">Dynamics 365 Supply Chain Management turto valdymas yra skirtas valdyti vidaus turtą.</span><span class="sxs-lookup"><span data-stu-id="3f1f9-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="3f1f9-106">Integravę šias dvi programėles, galite naudoti „Field Service“, kad aptarnautumėte tiek kliento, tiek vidaus turtą.</span><span class="sxs-lookup"><span data-stu-id="3f1f9-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="3f1f9-107">Taip pat galite klasifikuoti turtą, pagrįstą funkcine vieta ar hierarchija, ir sekti aptarnavimą išsamesniu lygiu.</span><span class="sxs-lookup"><span data-stu-id="3f1f9-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="3f1f9-108">Daugiau informacijos rasite [Dynamics 365 Field Service ir „Supply Chain Management“ integravimas](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="3f1f9-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="3f1f9-109">Šablonai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-109">Templates</span></span>

<span data-ttu-id="3f1f9-110">Vidinį turtą sudaro pagrindinių lentelių schemų, veikiančių kartu, kai duomenys yra naudojami interaktyviai, rinkinys, kaip parodyta tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="3f1f9-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="3f1f9-111">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="3f1f9-111">Finance and Operations apps</span></span> | <span data-ttu-id="3f1f9-112">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="3f1f9-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3f1f9-113">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3f1f9-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="3f1f9-114">Turto valdymo turto ciklo modeliai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="3f1f9-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="3f1f9-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="3f1f9-116">Turto valdymo turto ciklo modelių būsenos</span><span class="sxs-lookup"><span data-stu-id="3f1f9-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="3f1f9-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="3f1f9-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="3f1f9-118">Turto valdymo turtas</span><span class="sxs-lookup"><span data-stu-id="3f1f9-118">Asset management assets</span></span> | <span data-ttu-id="3f1f9-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="3f1f9-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="3f1f9-120">Turto valdymo turto tipai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-120">Asset management asset types</span></span> | <span data-ttu-id="3f1f9-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="3f1f9-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="3f1f9-122">Turto valdymo funkcinių vietų ciklo modeliai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="3f1f9-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="3f1f9-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="3f1f9-124">Turto valdymo funkcinių vietų ciklo būsenos</span><span class="sxs-lookup"><span data-stu-id="3f1f9-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="3f1f9-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="3f1f9-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="3f1f9-126">Turto valdymo funkcinės vietos</span><span class="sxs-lookup"><span data-stu-id="3f1f9-126">Asset management functional locations</span></span> | <span data-ttu-id="3f1f9-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="3f1f9-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="3f1f9-128">Turto valdymo funkcinių vietų tipai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-128">Asset management functional location types</span></span> | <span data-ttu-id="3f1f9-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="3f1f9-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="3f1f9-130">Turto valdymo gamintojai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-130">Asset management manufacturers</span></span> | <span data-ttu-id="3f1f9-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="3f1f9-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="3f1f9-132">Turto valdymo modeliai</span><span class="sxs-lookup"><span data-stu-id="3f1f9-132">Asset management models</span></span> | <span data-ttu-id="3f1f9-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="3f1f9-133">msdyn\_models</span></span> | |
| <span data-ttu-id="3f1f9-134">Turto valdymo garantija</span><span class="sxs-lookup"><span data-stu-id="3f1f9-134">Asset management warranty</span></span> | <span data-ttu-id="3f1f9-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="3f1f9-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]