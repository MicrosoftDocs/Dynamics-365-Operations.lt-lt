---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šiame straipsnyje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113557"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="f3791-103">Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="f3791-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="f3791-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="f3791-104">**Issue**</span></span>

- <span data-ttu-id="f3791-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="f3791-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="f3791-106">Vartotojas neturi licencijos suteikiančios teisę kurti aplinkas.</span><span class="sxs-lookup"><span data-stu-id="f3791-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="f3791-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="f3791-107">**Solution**</span></span>

<span data-ttu-id="f3791-108">Įsitikinkite, kad nuomotojo administratorius turi teisę įgyvendinti „Power Apps“ P2 teises vartotojui kuriančiam aplinką.</span><span class="sxs-lookup"><span data-stu-id="f3791-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="f3791-109">Tolesni „Microsoft Dynamics“ paslaugų planai suteikia teises kurti aplinkas:</span><span class="sxs-lookup"><span data-stu-id="f3791-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="f3791-110">Bendras produkto atsargų laikymo padalinys (SKU)</span><span class="sxs-lookup"><span data-stu-id="f3791-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="f3791-111">Power Apps P2 paslaugos planas</span><span class="sxs-lookup"><span data-stu-id="f3791-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="f3791-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="f3791-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="f3791-113">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="f3791-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="f3791-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="f3791-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="f3791-115">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="f3791-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="f3791-116">Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="f3791-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="f3791-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="f3791-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="f3791-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="f3791-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="f3791-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="f3791-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
