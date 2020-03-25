---
title: Darbuotojų savitarnos konfigūravimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092665"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="1700d-103">Darbuotojų savitarnos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1700d-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1700d-104">Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="1700d-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="1700d-105">Išmokų plano plytelės nukreipia vartotojus į išlaidų planus, kuriems jie turi teisę registruotis.</span><span class="sxs-lookup"><span data-stu-id="1700d-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="1700d-106">Vaidmenų centro plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="1700d-106">Set up a role center tile</span></span>

1. <span data-ttu-id="1700d-107">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1700d-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1700d-108">Pasirinkite skirtuką **Vaidmenų centro plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="1700d-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1700d-109">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="1700d-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1700d-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="1700d-110">Field</span></span> | <span data-ttu-id="1700d-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1700d-112">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="1700d-112">Tile ID</span></span> | <span data-ttu-id="1700d-113">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="1700d-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1700d-114">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="1700d-114">Tile label text</span></span> | <span data-ttu-id="1700d-115">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="1700d-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1700d-116">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-116">Description</span></span> | <span data-ttu-id="1700d-117">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="1700d-117">A description of the tile.</span></span> |
   | <span data-ttu-id="1700d-118">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="1700d-118">Internet address</span></span> | <span data-ttu-id="1700d-119">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="1700d-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1700d-120">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="1700d-120">Tile size</span></span> | <span data-ttu-id="1700d-121">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="1700d-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1700d-122">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="1700d-122">Target</span></span> | <span data-ttu-id="1700d-123">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="1700d-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1700d-124">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="1700d-124">Tile background image</span></span> | <span data-ttu-id="1700d-125">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="1700d-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1700d-126">Pradžios</span><span class="sxs-lookup"><span data-stu-id="1700d-126">Start</span></span> | <span data-ttu-id="1700d-127">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1700d-128">„End“</span><span class="sxs-lookup"><span data-stu-id="1700d-128">End</span></span> | <span data-ttu-id="1700d-129">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1700d-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1700d-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="1700d-131">Išmokų planų plytelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="1700d-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="1700d-132">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1700d-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1700d-133">Pasirinkite skirtuką **Išmokų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="1700d-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1700d-134">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="1700d-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1700d-135">Laukas</span><span class="sxs-lookup"><span data-stu-id="1700d-135">Field</span></span> | <span data-ttu-id="1700d-136">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1700d-137">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="1700d-137">Tile ID</span></span> | <span data-ttu-id="1700d-138">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="1700d-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1700d-139">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="1700d-139">Tile label text</span></span> | <span data-ttu-id="1700d-140">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="1700d-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1700d-141">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-141">Description</span></span> | <span data-ttu-id="1700d-142">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="1700d-142">A description of the tile.</span></span> |
   | <span data-ttu-id="1700d-143">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="1700d-143">Internet address</span></span> | <span data-ttu-id="1700d-144">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="1700d-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1700d-145">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="1700d-145">Tile size</span></span> | <span data-ttu-id="1700d-146">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="1700d-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1700d-147">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="1700d-147">Target</span></span> | <span data-ttu-id="1700d-148">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="1700d-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1700d-149">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="1700d-149">Tile background image</span></span> | <span data-ttu-id="1700d-150">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="1700d-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1700d-151">Pradžios</span><span class="sxs-lookup"><span data-stu-id="1700d-151">Start</span></span> | <span data-ttu-id="1700d-152">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1700d-153">„End“</span><span class="sxs-lookup"><span data-stu-id="1700d-153">End</span></span> | <span data-ttu-id="1700d-154">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1700d-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1700d-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="1700d-156">Lanksčiųjų kreditų plano plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="1700d-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="1700d-157">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1700d-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="1700d-158">Pasirinkite skirtuką **Lanksčiųjų kreditų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="1700d-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="1700d-159">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="1700d-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1700d-160">Laukas</span><span class="sxs-lookup"><span data-stu-id="1700d-160">Field</span></span> | <span data-ttu-id="1700d-161">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1700d-162">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="1700d-162">Tile ID</span></span> | <span data-ttu-id="1700d-163">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="1700d-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="1700d-164">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="1700d-164">Tile label text</span></span> | <span data-ttu-id="1700d-165">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="1700d-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="1700d-166">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1700d-166">Description</span></span> | <span data-ttu-id="1700d-167">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="1700d-167">A description of the tile.</span></span> |
   | <span data-ttu-id="1700d-168">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="1700d-168">Internet address</span></span> | <span data-ttu-id="1700d-169">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="1700d-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="1700d-170">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="1700d-170">Tile size</span></span> | <span data-ttu-id="1700d-171">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="1700d-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="1700d-172">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="1700d-172">Target</span></span> | <span data-ttu-id="1700d-173">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="1700d-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="1700d-174">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="1700d-174">Tile background image</span></span> | <span data-ttu-id="1700d-175">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="1700d-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="1700d-176">Pradžios</span><span class="sxs-lookup"><span data-stu-id="1700d-176">Start</span></span> | <span data-ttu-id="1700d-177">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="1700d-178">„End“</span><span class="sxs-lookup"><span data-stu-id="1700d-178">End</span></span> | <span data-ttu-id="1700d-179">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="1700d-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="1700d-180">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1700d-180">Select **Save**.</span></span>
