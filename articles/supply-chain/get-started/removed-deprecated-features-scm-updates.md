---
title: Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos
description: Šioje temoje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Supply Chain Management“.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331253"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="b7b76-103">Pašalintos arba nebenaudojamos „Dynamics 365 Supply Chain Management“ funkcijos</span><span class="sxs-lookup"><span data-stu-id="b7b76-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b76-104">Ši tema bus atnaujinta, kai naujai pašalintos arba nebenaudojamos funkcijos bus užfiksuotos „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b7b76-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="b7b76-105">*Pašalinta* funkcija nebėra įtraukta į produktą.</span><span class="sxs-lookup"><span data-stu-id="b7b76-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="b7b76-106">*Nebenaudojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.</span><span class="sxs-lookup"><span data-stu-id="b7b76-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="b7b76-107">Šis sąrašas skirtas suteikti jums informacijos apie pašalintas ir nebenaudojamas funkcijas, kad galėtumėte geriau planuoti savo darbą.</span><span class="sxs-lookup"><span data-stu-id="b7b76-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="b7b76-108">Išsamios informacijos apie „Finance and Operations“ programų objektus rasite skyriuje [Techninės informacijos ataskaitos](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="b7b76-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="b7b76-109">Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš „Finance and Operations“ programų versijų.</span><span class="sxs-lookup"><span data-stu-id="b7b76-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="b7b76-110">Pašalintos arba nebenaudojamos funkcijos, esančios „Supply Chain Management“ 10.0.11 versijoje</span><span class="sxs-lookup"><span data-stu-id="b7b76-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="b7b76-111">Įtaisytojo „Supply Chain Management“ bendrojo planavimo mechanizmo naudojimas paskirstymo scenarijuose</span><span class="sxs-lookup"><span data-stu-id="b7b76-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="b7b76-112">**Nebenaudojimo / pašalinimo priežastis**</span><span class="sxs-lookup"><span data-stu-id="b7b76-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="b7b76-113">Siekiant padidinti našumą ir sumažinti SQL duomenų bazės apkrovą bendrojo planavimo vykdymų metu, įtaisytasis „Supply Chain Management” bendrojo planavimo mechanizmas yra pakeičiamas planavimo optimizavimu.</span><span class="sxs-lookup"><span data-stu-id="b7b76-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="b7b76-114">Planavimo optimizavimas leidžia greitai planuoti vykdymus, kuriuos galima atlikti netgi darbo valandomis.</span><span class="sxs-lookup"><span data-stu-id="b7b76-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="b7b76-115">Dėl to planuotojai iš karto reaguoja į poreikio arba planavimo parametrų pasikeitimus.</span><span class="sxs-lookup"><span data-stu-id="b7b76-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="b7b76-116">**Pakeitė kita funkcija?**</span><span class="sxs-lookup"><span data-stu-id="b7b76-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="b7b76-117">Taip, planavimo optimizavimas pakeis dabartinį įtaisytąjį „Supply Chain Management“ bendrojo planavimo mechanizmą.</span><span class="sxs-lookup"><span data-stu-id="b7b76-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="b7b76-118">**Paveiktos produkto sritys**</span><span class="sxs-lookup"><span data-stu-id="b7b76-118">**Product areas affected**</span></span>         | <span data-ttu-id="b7b76-119">„Supply Chain Management” – bendrasis planavimas</span><span class="sxs-lookup"><span data-stu-id="b7b76-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="b7b76-120">**Visuotinio diegimo parinktis**</span><span class="sxs-lookup"><span data-stu-id="b7b76-120">**Deployment option**</span></span>              | <span data-ttu-id="b7b76-121">Tik debesyje.</span><span class="sxs-lookup"><span data-stu-id="b7b76-121">Cloud only.</span></span> <span data-ttu-id="b7b76-122">Planavimo optimizavimas nepalaikomas vietiniuose visuotiniuose diegimuose.</span><span class="sxs-lookup"><span data-stu-id="b7b76-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="b7b76-123">**Būsena**</span><span class="sxs-lookup"><span data-stu-id="b7b76-123">**Status**</span></span>                         | <span data-ttu-id="b7b76-124">Nebenaudojama.</span><span class="sxs-lookup"><span data-stu-id="b7b76-124">Deprecated.</span></span> <span data-ttu-id="b7b76-125">Nuo 2021 m. balandžio mėn. paskirstymo scenarijai nebebus palaikomi su įtaisytuoju „Dynamics 365 Supply Chain Management” bendrojo planavimo mechanizmu.</span><span class="sxs-lookup"><span data-stu-id="b7b76-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="b7b76-126">Paskirstymo scenarijuose klientai turi naudoti bendrojo planavimo skaičiavimo planavimo optimizavimą.</span><span class="sxs-lookup"><span data-stu-id="b7b76-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="b7b76-127">Daugiau informacijos žr. [Planavimo optimizavimo dokumentacija](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="b7b76-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="b7b76-128">Klientai, turintys vietinius visuotinius „Dynamics 365 Supply Chain Management” diegimus, po 2021 m. balandžio mėn. gali toliau naudoti „Supply Chain Management” bendrojo planavimo mechanizmą paskirstymo scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="b7b76-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="b7b76-129">Tačiau daugiau funkcijų patobulinimų nebus teikiama.</span><span class="sxs-lookup"><span data-stu-id="b7b76-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="b7b76-130">Ankstesni pranešimai apie pašalintas arba nebenaudojamas funkcijas</span><span class="sxs-lookup"><span data-stu-id="b7b76-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="b7b76-131">Norėdami sužinoti daugiau apie funkcijas, kurios buvo pašalintos arba nebenaudojamos ankstesniuose leidimuose, žr. skyrių [Ankstesniuose leidimuose pašalintos arba nebenaudojamos funkcijos](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="b7b76-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
