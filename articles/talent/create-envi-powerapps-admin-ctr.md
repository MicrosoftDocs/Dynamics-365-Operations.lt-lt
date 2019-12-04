---
title: Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre
description: Šioje temoje paaiškinama, ką daryti, jei administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773224"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="32942-103">Nepavyksta sukurti aplinkos „Power Apps“ administravimo centre</span><span class="sxs-lookup"><span data-stu-id="32942-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32942-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="32942-104">**Issue**</span></span>

- <span data-ttu-id="32942-105">Nuomotojo arba aplinkos administratorius negali sukurti aplinkos „Microsoft Power Apps“ administravimo centre.</span><span class="sxs-lookup"><span data-stu-id="32942-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="32942-106">Licencija, suteikianti vartotojams teisę atlikti aplinkos kūrimo veiksmą, nėra tiesiogiai priskirta vartotojui, kuris atlieka šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="32942-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="32942-107">**Sprendimas**</span><span class="sxs-lookup"><span data-stu-id="32942-107">**Solution**</span></span>

<span data-ttu-id="32942-108">Įsitikinkite, kad nuomotojo administratorius tiesiogiai priskyrė tinkamą Power Apps P2 licenciją vartotojui, kuris atliks aplinkos kūrimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="32942-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="32942-109">Štai „Microsoft Dynamics“ paslaugų teikimo planai, kurie suteikia tokią teisę.</span><span class="sxs-lookup"><span data-stu-id="32942-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="32942-110">Viso produkto sandėliavimo vienetas (SKU)</span><span class="sxs-lookup"><span data-stu-id="32942-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="32942-111">Power Apps P2 paslaugos planas</span><span class="sxs-lookup"><span data-stu-id="32942-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="32942-112">„Microsoft Dynamics 365 for Operations“</span><span class="sxs-lookup"><span data-stu-id="32942-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="32942-113">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="32942-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="32942-114">„Microsoft Dynamics 365“ planas „Enterprise Edition“</span><span class="sxs-lookup"><span data-stu-id="32942-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="32942-115">Power Apps, skirta „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="32942-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="32942-116">Atkreipkite dėmesį, kad įvairūs Microsoft Office SKU taip pat suteikia teisę kartu naudoti atskiro Power Apps 2 plano SKU.</span><span class="sxs-lookup"><span data-stu-id="32942-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="32942-117">Svarbiausia tai, kad turi būti vienas iš šių SKU.</span><span class="sxs-lookup"><span data-stu-id="32942-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="32942-118">Eikite į [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span><span class="sxs-lookup"><span data-stu-id="32942-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="32942-119">Kurkite aplinkas vykdydami instrukcijas, pateiktas [„Talent“ parengimas](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="32942-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
