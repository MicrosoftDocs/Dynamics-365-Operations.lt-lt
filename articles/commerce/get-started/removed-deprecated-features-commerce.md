---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335281"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="b21f5-103">Pašalintos arba nebenaudojamos „Dynamics 365 Commerce“ funkcijos</span><span class="sxs-lookup"><span data-stu-id="b21f5-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b21f5-104">Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b21f5-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="b21f5-105">*Pašalinta* funkcija nebėra įtraukta į produktą.</span><span class="sxs-lookup"><span data-stu-id="b21f5-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b21f5-106">*Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.</span><span class="sxs-lookup"><span data-stu-id="b21f5-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b21f5-107">Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.</span><span class="sxs-lookup"><span data-stu-id="b21f5-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="b21f5-108">Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="b21f5-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b21f5-109">Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.</span><span class="sxs-lookup"><span data-stu-id="b21f5-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="b21f5-110">Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.10 versijoje</span><span class="sxs-lookup"><span data-stu-id="b21f5-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="b21f5-111">EKA 803 operacija – paėmimas ir gavimas</span><span class="sxs-lookup"><span data-stu-id="b21f5-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b21f5-112">**Nebenaudojimo / pašalinimo priežastis**</span><span class="sxs-lookup"><span data-stu-id="b21f5-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b21f5-113">Operacijų paėmimas ir gavimas nebenaudojamas dėl naujos operacijų pertvarkos.</span><span class="sxs-lookup"><span data-stu-id="b21f5-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="b21f5-114">**Pakeitė kita funkcija?**</span><span class="sxs-lookup"><span data-stu-id="b21f5-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b21f5-115">Taip.</span><span class="sxs-lookup"><span data-stu-id="b21f5-115">Yes.</span></span> <span data-ttu-id="b21f5-116">Jie pakeičiami dviem naujomis EKA operacijomis: gaunama operacija (804) ir siunčiama operacija (805).</span><span class="sxs-lookup"><span data-stu-id="b21f5-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="b21f5-117">**Paveiktos produkto sritys**</span><span class="sxs-lookup"><span data-stu-id="b21f5-117">**Product areas affected**</span></span>         | <span data-ttu-id="b21f5-118">Elektroninio kasos aparato (EKA) programa</span><span class="sxs-lookup"><span data-stu-id="b21f5-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="b21f5-119">**Visuotinio diegimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="b21f5-119">**Deployment option**</span></span>              | <span data-ttu-id="b21f5-120">Visi / Viskas</span><span class="sxs-lookup"><span data-stu-id="b21f5-120">All</span></span> |
| <span data-ttu-id="b21f5-121">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="b21f5-121">**Status**</span></span>                         | <span data-ttu-id="b21f5-122">Nebenaudojama: nuo 10.0.10 versijos išleidimo paėmimo ir gavimo operacijos nebegaus naujų funkcijų naujinimų.</span><span class="sxs-lookup"><span data-stu-id="b21f5-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="b21f5-123">Būsimuose leidimuose bus atliktos tik kritinių operacijos klaidų pataisos.</span><span class="sxs-lookup"><span data-stu-id="b21f5-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="b21f5-124">Visi klientai skatinami pereiti prie naujų [gaunamų operacijų](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ir [siunčiamų operacijų](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), kurios ir toliau bus mūsų ilgalaikio produktų veiksmų plano dalis.</span><span class="sxs-lookup"><span data-stu-id="b21f5-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="b21f5-125">Pašalintos arba nebenaudojamos funkcijos, esančios „Commerce“ 10.0.7 versijoje</span><span class="sxs-lookup"><span data-stu-id="b21f5-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="b21f5-126">„Commerce” GetProductAvailabilities ir GetAvailableInventoryNearby API</span><span class="sxs-lookup"><span data-stu-id="b21f5-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="b21f5-127">**Nebenaudojimo / pašalinimo priežastis**</span><span class="sxs-lookup"><span data-stu-id="b21f5-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b21f5-128">Buvo sukurtos naujos optimizuotos API, kad pakeistų GetProductAvailabilities ir GetAvailableInventoryNearby API.</span><span class="sxs-lookup"><span data-stu-id="b21f5-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="b21f5-129">**Pakeitė kita funkcija?**</span><span class="sxs-lookup"><span data-stu-id="b21f5-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b21f5-130">Taip, jos pakeičiamos GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API.</span><span class="sxs-lookup"><span data-stu-id="b21f5-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="b21f5-131">**Paveiktos produkto sritys**</span><span class="sxs-lookup"><span data-stu-id="b21f5-131">**Product areas affected**</span></span>         | <span data-ttu-id="b21f5-132">„e-Commerce“ programos SDK</span><span class="sxs-lookup"><span data-stu-id="b21f5-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="b21f5-133">**Visuotinio diegimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="b21f5-133">**Deployment option**</span></span>              | <span data-ttu-id="b21f5-134">Visi / Viskas</span><span class="sxs-lookup"><span data-stu-id="b21f5-134">All</span></span> |
| <span data-ttu-id="b21f5-135">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="b21f5-135">**Status**</span></span>                         | <span data-ttu-id="b21f5-136">Nebenaudojama: nuo 10.0.7 versijos išleidimo nebebus GetProductAvailabilities ir GetAvailableInventoryNearby inžinerinių investicijų.</span><span class="sxs-lookup"><span data-stu-id="b21f5-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="b21f5-137">Organizacijos, naudojančios šias API „e-Commerce“ diegimuose, turėtų konvertuoti į naujas GetEstimatedAvailability ir GetEstimatedProductWarehouseAvailability API ir įjungti [funkciją Optimizuotas produkto pasiekiamumo skaičiavimas](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="b21f5-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b21f5-138">Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas</span><span class="sxs-lookup"><span data-stu-id="b21f5-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="b21f5-139">Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b21f5-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
