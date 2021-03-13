---
title: Darbuotojų savitarnos konfigūravimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 32981812eac3c08e1409fe5470b550e421f5d6c9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113554"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="d76b3-103">Darbuotojų savitarnos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d76b3-103">Configure employee self service</span></span>

<span data-ttu-id="d76b3-104">Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="d76b3-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="d76b3-105">Išmokų plano plytelės nukreipia vartotojus į išlaidų planus, kuriems jie tinkami.</span><span class="sxs-lookup"><span data-stu-id="d76b3-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="d76b3-106">Išmokų planų plytelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="d76b3-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="d76b3-107">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d76b3-108">Pasirinkite skirtuką **Išmokų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d76b3-109">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="d76b3-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d76b3-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="d76b3-110">Field</span></span> | <span data-ttu-id="d76b3-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="d76b3-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d76b3-112">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="d76b3-112">**Tile ID**</span></span> | <span data-ttu-id="d76b3-113">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="d76b3-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d76b3-114">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-114">**Tile label text**</span></span> | <span data-ttu-id="d76b3-115">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="d76b3-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d76b3-116">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-116">**Description**</span></span> | <span data-ttu-id="d76b3-117">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-117">A description of the tile.</span></span> |
   | <span data-ttu-id="d76b3-118">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-118">**Internet address**</span></span> | <span data-ttu-id="d76b3-119">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="d76b3-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d76b3-120">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="d76b3-120">**Tile size**</span></span> | <span data-ttu-id="d76b3-121">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="d76b3-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d76b3-122">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="d76b3-122">**Target**</span></span> | <span data-ttu-id="d76b3-123">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="d76b3-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d76b3-124">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-124">**Tile background image**</span></span> | <span data-ttu-id="d76b3-125">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="d76b3-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d76b3-126">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="d76b3-126">**Start**</span></span> | <span data-ttu-id="d76b3-127">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d76b3-128">**„End“**</span><span class="sxs-lookup"><span data-stu-id="d76b3-128">**End**</span></span> | <span data-ttu-id="d76b3-129">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d76b3-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="d76b3-131">Lanksčiųjų kreditų plano plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="d76b3-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="d76b3-132">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d76b3-133">Pasirinkite skirtuką **Lanksčiųjų kreditų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d76b3-134">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="d76b3-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d76b3-135">Laukas</span><span class="sxs-lookup"><span data-stu-id="d76b3-135">Field</span></span> | <span data-ttu-id="d76b3-136">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="d76b3-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d76b3-137">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="d76b3-137">**Tile ID**</span></span> | <span data-ttu-id="d76b3-138">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="d76b3-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d76b3-139">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-139">**Tile label text**</span></span> | <span data-ttu-id="d76b3-140">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="d76b3-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="d76b3-141">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-141">**Description**</span></span> | <span data-ttu-id="d76b3-142">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-142">A description of the tile.</span></span> |
   | <span data-ttu-id="d76b3-143">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-143">**Internet address**</span></span> | <span data-ttu-id="d76b3-144">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="d76b3-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d76b3-145">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="d76b3-145">**Tile size**</span></span> | <span data-ttu-id="d76b3-146">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="d76b3-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d76b3-147">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="d76b3-147">**Target**</span></span> | <span data-ttu-id="d76b3-148">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="d76b3-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d76b3-149">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="d76b3-149">**Tile background image**</span></span> | <span data-ttu-id="d76b3-150">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="d76b3-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d76b3-151">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="d76b3-151">**Start**</span></span> | <span data-ttu-id="d76b3-152">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d76b3-153">**„End“**</span><span class="sxs-lookup"><span data-stu-id="d76b3-153">**End**</span></span> | <span data-ttu-id="d76b3-154">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="d76b3-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d76b3-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d76b3-155">Select **Save**.</span></span>
