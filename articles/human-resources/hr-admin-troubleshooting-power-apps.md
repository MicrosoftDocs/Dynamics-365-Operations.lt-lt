---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šiame straipsnyje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431066"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="63b54-103">Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="63b54-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="63b54-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="63b54-104">**Issue**</span></span>

- <span data-ttu-id="63b54-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="63b54-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="63b54-106">Licencija, suteikianti vartotojams teisę atlikti aplinkos kūrimo veiksmą, nėra tiesiogiai priskirta vartotojui, kuris atlieka šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="63b54-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="63b54-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="63b54-107">**Solution**</span></span>

<span data-ttu-id="63b54-108">Įsitikinkite, kad nuomotojo administratorius tiesiogiai priskyrė tinkamą Power Apps P2 licenciją vartotojui, kuris atliks aplinkos kūrimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="63b54-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="63b54-109">Štai „Microsoft Dynamics“ paslaugų teikimo planai, kurie suteikia tokią teisę.</span><span class="sxs-lookup"><span data-stu-id="63b54-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="63b54-110">Viso produkto sandėliavimo vienetas (SKU)</span><span class="sxs-lookup"><span data-stu-id="63b54-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="63b54-111">Power Apps P2 paslaugos planas</span><span class="sxs-lookup"><span data-stu-id="63b54-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="63b54-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="63b54-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="63b54-113">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="63b54-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="63b54-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="63b54-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="63b54-115">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="63b54-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="63b54-116">Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="63b54-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="63b54-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="63b54-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="63b54-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="63b54-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="63b54-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Human Resources“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="63b54-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
