---
title: Pašalintos arba nebenaudojamos platformos funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087888"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="41a72-103">Pašalintos arba nebenaudojamos platformos funkcijos</span><span class="sxs-lookup"><span data-stu-id="41a72-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41a72-104">Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama šalinti iš „Finance and Operations“ programų platformos naujinių.</span><span class="sxs-lookup"><span data-stu-id="41a72-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="41a72-105">*Pašalinta* funkcija nebėra įtraukta į produktą.</span><span class="sxs-lookup"><span data-stu-id="41a72-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="41a72-106">*Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.</span><span class="sxs-lookup"><span data-stu-id="41a72-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="41a72-107">Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.</span><span class="sxs-lookup"><span data-stu-id="41a72-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="41a72-108">Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="41a72-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="41a72-109">Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.</span><span class="sxs-lookup"><span data-stu-id="41a72-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="41a72-110">Platformos „update 32“</span><span class="sxs-lookup"><span data-stu-id="41a72-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="41a72-111">Darbo eigos užklausos keitimo dialogo lange nebėra vartotojų pasirinkimo išplečiamojo sąrašo</span><span class="sxs-lookup"><span data-stu-id="41a72-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="41a72-112">**Nebenaudojimo / pašalinimo priežastis**</span><span class="sxs-lookup"><span data-stu-id="41a72-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="41a72-113">Dėl sąrašo galėjo kilti saugos problemų, nes keitimo užklausa galėjo būti nusiųsta nenumatytam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="41a72-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="41a72-114">Taip pat kilo tinkamumo naudoti problema, nes vartotojas buvo verčiamas nustatyti darbo eigos iniciatorių ir pasirinkti jį rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="41a72-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="41a72-115">**Pakeitė kita funkcija?**</span><span class="sxs-lookup"><span data-stu-id="41a72-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="41a72-116">Ne</span><span class="sxs-lookup"><span data-stu-id="41a72-116">No</span></span> |
| <span data-ttu-id="41a72-117">**Paveiktos produkto sritys**</span><span class="sxs-lookup"><span data-stu-id="41a72-117">**Product areas affected**</span></span>         | <span data-ttu-id="41a72-118">Darbo eiga</span><span class="sxs-lookup"><span data-stu-id="41a72-118">Workflow</span></span> |
| <span data-ttu-id="41a72-119">**Visuotinio diegimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="41a72-119">**Deployment option**</span></span>              | <span data-ttu-id="41a72-120">Visos</span><span class="sxs-lookup"><span data-stu-id="41a72-120">All</span></span> |
| <span data-ttu-id="41a72-121">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="41a72-121">**Status**</span></span>                         | <span data-ttu-id="41a72-122">Vartotojų pasirinkimo išplečiamasis sąrašas buvo pašalintas iš „Platform update 32“ keitimo užklausos dialogo lango.</span><span class="sxs-lookup"><span data-stu-id="41a72-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="41a72-123">Užklausos keitimo užklausos bus automatiškai siunčiamos iniciatoriui, kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="41a72-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="41a72-124">Norėdami gauti daugiau informacijos apie šią funkciją, žr. skyrių [Darbo eigos patvirtinimo procesų veiksmai](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="41a72-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="41a72-125">Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas</span><span class="sxs-lookup"><span data-stu-id="41a72-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="41a72-126">Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="41a72-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

