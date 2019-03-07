---
title: Nepavyksta sukurti aplinkos „PowerApps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft PowerApps“ administravimo centre.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305529"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="2027a-103">Nepavyksta sukurti aplinkos „PowerApps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="2027a-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2027a-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="2027a-104">**Issue**</span></span>

- <span data-ttu-id="2027a-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft PowerApps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="2027a-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="2027a-106">Licencija, suteikianti vartotojams teisę atlikti aplinkos kūrimo veiksmą, nėra tiesiogiai priskirta vartotojui, kuris atlieka šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="2027a-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="2027a-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="2027a-107">**Solution**</span></span>

<span data-ttu-id="2027a-108">Įsitikinkite, kad nuomotojo administratorius tiesiogiai priskyrė tinkamą „PowerApps“ P2 licenciją vartotojui, kuris atliks aplinkos kūrimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="2027a-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="2027a-109">Štai „Microsoft Dynamics“ paslaugų teikimo planai, kurie suteikia tokią teisę.</span><span class="sxs-lookup"><span data-stu-id="2027a-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="2027a-110">Viso produkto sandėliavimo vienetas (SKU)</span><span class="sxs-lookup"><span data-stu-id="2027a-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="2027a-111">„PowerApps“ P2 paslaugų teikimo planas</span><span class="sxs-lookup"><span data-stu-id="2027a-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="2027a-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="2027a-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="2027a-113">„PowerApps“, skirtos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="2027a-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="2027a-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="2027a-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="2027a-115">„PowerApps“, skirtos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="2027a-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="2027a-116">Atkreipkite dėmesį, kad įvairūs „Microsoft Office“ SKU taip pat suteikia teisę kartu naudoti atskiro „PowerApps“ 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="2027a-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="2027a-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="2027a-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="2027a-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="2027a-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="2027a-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Talent“ parengimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="2027a-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
