---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šiame straipsnyje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73c8910900ba6486a8e60a547b07ea0c82a6cb10
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053352"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="91230-103">Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="91230-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="91230-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="91230-104">**Issue**</span></span>

- <span data-ttu-id="91230-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="91230-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="91230-106">Vartotojas neturi licencijos suteikiančios teisę kurti aplinkas.</span><span class="sxs-lookup"><span data-stu-id="91230-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="91230-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="91230-107">**Solution**</span></span>

<span data-ttu-id="91230-108">Įsitikinkite, kad nuomotojo administratorius turi teisę įgyvendinti „Power Apps“ P2 teises vartotojui kuriančiam aplinką.</span><span class="sxs-lookup"><span data-stu-id="91230-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="91230-109">Tolesni „Microsoft Dynamics“ paslaugų planai suteikia teises kurti aplinkas:</span><span class="sxs-lookup"><span data-stu-id="91230-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="91230-110">Bendras produkto atsargų laikymo padalinys (SKU)</span><span class="sxs-lookup"><span data-stu-id="91230-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="91230-111">Power Apps P2 paslaugos planas</span><span class="sxs-lookup"><span data-stu-id="91230-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="91230-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="91230-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="91230-113">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="91230-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="91230-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="91230-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="91230-115">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="91230-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="91230-116">Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="91230-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="91230-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="91230-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="91230-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="91230-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="91230-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="91230-119">Create the environments by following the instructions in [Provision Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]