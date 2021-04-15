---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šiame straipsnyje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797990"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="fc069-103">Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="fc069-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fc069-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="fc069-104">**Issue**</span></span>

- <span data-ttu-id="fc069-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="fc069-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="fc069-106">Vartotojas neturi licencijos suteikiančios teisę kurti aplinkas.</span><span class="sxs-lookup"><span data-stu-id="fc069-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="fc069-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="fc069-107">**Solution**</span></span>

<span data-ttu-id="fc069-108">Įsitikinkite, kad nuomotojo administratorius turi teisę įgyvendinti „Power Apps“ P2 teises vartotojui kuriančiam aplinką.</span><span class="sxs-lookup"><span data-stu-id="fc069-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="fc069-109">Tolesni „Microsoft Dynamics“ paslaugų planai suteikia teises kurti aplinkas:</span><span class="sxs-lookup"><span data-stu-id="fc069-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="fc069-110">Bendras produkto atsargų laikymo padalinys (SKU)</span><span class="sxs-lookup"><span data-stu-id="fc069-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="fc069-111">Power Apps P2 paslaugos planas</span><span class="sxs-lookup"><span data-stu-id="fc069-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="fc069-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="fc069-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="fc069-113">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="fc069-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="fc069-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="fc069-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="fc069-115">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="fc069-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="fc069-116">Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="fc069-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="fc069-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="fc069-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="fc069-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="fc069-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="fc069-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="fc069-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]