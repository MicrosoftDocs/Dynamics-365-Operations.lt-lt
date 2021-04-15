---
title: Darbuotojų savitarnos konfigūravimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797940"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="74efe-103">Darbuotojų savitarnos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="74efe-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="74efe-104">Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="74efe-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="74efe-105">Išmokų plano plytelės nukreipia vartotojus į išlaidų planus, kuriems jie tinkami.</span><span class="sxs-lookup"><span data-stu-id="74efe-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="74efe-106">Išmokų planų plytelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="74efe-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="74efe-107">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="74efe-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="74efe-108">Pasirinkite skirtuką **Išmokų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="74efe-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="74efe-109">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="74efe-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="74efe-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="74efe-110">Field</span></span> | <span data-ttu-id="74efe-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="74efe-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="74efe-112">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="74efe-112">**Tile ID**</span></span> | <span data-ttu-id="74efe-113">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="74efe-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="74efe-114">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="74efe-114">**Tile label text**</span></span> | <span data-ttu-id="74efe-115">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="74efe-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="74efe-116">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="74efe-116">**Description**</span></span> | <span data-ttu-id="74efe-117">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="74efe-117">A description of the tile.</span></span> |
   | <span data-ttu-id="74efe-118">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="74efe-118">**Internet address**</span></span> | <span data-ttu-id="74efe-119">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="74efe-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="74efe-120">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="74efe-120">**Tile size**</span></span> | <span data-ttu-id="74efe-121">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="74efe-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="74efe-122">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="74efe-122">**Target**</span></span> | <span data-ttu-id="74efe-123">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="74efe-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="74efe-124">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="74efe-124">**Tile background image**</span></span> | <span data-ttu-id="74efe-125">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="74efe-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="74efe-126">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="74efe-126">**Start**</span></span> | <span data-ttu-id="74efe-127">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="74efe-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="74efe-128">**„End“**</span><span class="sxs-lookup"><span data-stu-id="74efe-128">**End**</span></span> | <span data-ttu-id="74efe-129">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="74efe-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="74efe-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="74efe-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="74efe-131">Lanksčiųjų kreditų plano plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="74efe-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="74efe-132">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="74efe-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="74efe-133">Pasirinkite skirtuką **Lanksčiųjų kreditų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="74efe-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="74efe-134">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="74efe-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="74efe-135">Laukas</span><span class="sxs-lookup"><span data-stu-id="74efe-135">Field</span></span> | <span data-ttu-id="74efe-136">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="74efe-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="74efe-137">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="74efe-137">**Tile ID**</span></span> | <span data-ttu-id="74efe-138">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="74efe-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="74efe-139">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="74efe-139">**Tile label text**</span></span> | <span data-ttu-id="74efe-140">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="74efe-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="74efe-141">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="74efe-141">**Description**</span></span> | <span data-ttu-id="74efe-142">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="74efe-142">A description of the tile.</span></span> |
   | <span data-ttu-id="74efe-143">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="74efe-143">**Internet address**</span></span> | <span data-ttu-id="74efe-144">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="74efe-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="74efe-145">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="74efe-145">**Tile size**</span></span> | <span data-ttu-id="74efe-146">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="74efe-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="74efe-147">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="74efe-147">**Target**</span></span> | <span data-ttu-id="74efe-148">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="74efe-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="74efe-149">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="74efe-149">**Tile background image**</span></span> | <span data-ttu-id="74efe-150">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="74efe-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="74efe-151">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="74efe-151">**Start**</span></span> | <span data-ttu-id="74efe-152">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="74efe-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="74efe-153">**„End“**</span><span class="sxs-lookup"><span data-stu-id="74efe-153">**End**</span></span> | <span data-ttu-id="74efe-154">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="74efe-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="74efe-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="74efe-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]