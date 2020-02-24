---
title: Darbuotojų savitarnos konfigūravimas
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009949"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="22faa-102">Darbuotojų savitarnos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="22faa-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="22faa-103">Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="22faa-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="22faa-104">Išmokų plano plytelės nukreipia vartotojus į išlaidų planus, kuriems jie turi teisę registruotis.</span><span class="sxs-lookup"><span data-stu-id="22faa-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="22faa-105">Vaidmenų centro plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="22faa-105">Set up a role center tile</span></span>

1. <span data-ttu-id="22faa-106">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="22faa-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="22faa-107">Pasirinkite skirtuką **Vaidmenų centro plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="22faa-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="22faa-108">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="22faa-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="22faa-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="22faa-109">Field</span></span> | <span data-ttu-id="22faa-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="22faa-111">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="22faa-111">Tile ID</span></span> | <span data-ttu-id="22faa-112">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="22faa-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="22faa-113">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="22faa-113">Tile label text</span></span> | <span data-ttu-id="22faa-114">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="22faa-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="22faa-115">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-115">Description</span></span> | <span data-ttu-id="22faa-116">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="22faa-116">A description of the tile.</span></span> |
   | <span data-ttu-id="22faa-117">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="22faa-117">Internet address</span></span> | <span data-ttu-id="22faa-118">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="22faa-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="22faa-119">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="22faa-119">Tile size</span></span> | <span data-ttu-id="22faa-120">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="22faa-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="22faa-121">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="22faa-121">Target</span></span> | <span data-ttu-id="22faa-122">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="22faa-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="22faa-123">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="22faa-123">Tile background image</span></span> | <span data-ttu-id="22faa-124">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="22faa-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="22faa-125">Pradžios</span><span class="sxs-lookup"><span data-stu-id="22faa-125">Start</span></span> | <span data-ttu-id="22faa-126">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="22faa-127">„End“</span><span class="sxs-lookup"><span data-stu-id="22faa-127">End</span></span> | <span data-ttu-id="22faa-128">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="22faa-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="22faa-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="22faa-130">Išmokų planų plytelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="22faa-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="22faa-131">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="22faa-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="22faa-132">Pasirinkite skirtuką **Išmokų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="22faa-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="22faa-133">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="22faa-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="22faa-134">Laukas</span><span class="sxs-lookup"><span data-stu-id="22faa-134">Field</span></span> | <span data-ttu-id="22faa-135">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="22faa-136">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="22faa-136">Tile ID</span></span> | <span data-ttu-id="22faa-137">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="22faa-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="22faa-138">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="22faa-138">Tile label text</span></span> | <span data-ttu-id="22faa-139">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="22faa-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="22faa-140">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-140">Description</span></span> | <span data-ttu-id="22faa-141">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="22faa-141">A description of the tile.</span></span> |
   | <span data-ttu-id="22faa-142">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="22faa-142">Internet address</span></span> | <span data-ttu-id="22faa-143">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="22faa-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="22faa-144">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="22faa-144">Tile size</span></span> | <span data-ttu-id="22faa-145">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="22faa-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="22faa-146">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="22faa-146">Target</span></span> | <span data-ttu-id="22faa-147">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="22faa-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="22faa-148">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="22faa-148">Tile background image</span></span> | <span data-ttu-id="22faa-149">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="22faa-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="22faa-150">Pradžios</span><span class="sxs-lookup"><span data-stu-id="22faa-150">Start</span></span> | <span data-ttu-id="22faa-151">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="22faa-152">„End“</span><span class="sxs-lookup"><span data-stu-id="22faa-152">End</span></span> | <span data-ttu-id="22faa-153">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="22faa-154">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="22faa-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="22faa-155">Lanksčiųjų kreditų plano plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="22faa-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="22faa-156">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="22faa-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="22faa-157">Pasirinkite skirtuką **Lanksčiųjų kreditų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="22faa-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="22faa-158">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="22faa-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="22faa-159">Laukas</span><span class="sxs-lookup"><span data-stu-id="22faa-159">Field</span></span> | <span data-ttu-id="22faa-160">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="22faa-161">Plytelės ID</span><span class="sxs-lookup"><span data-stu-id="22faa-161">Tile ID</span></span> | <span data-ttu-id="22faa-162">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="22faa-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="22faa-163">Plytelių etiketės tekstas</span><span class="sxs-lookup"><span data-stu-id="22faa-163">Tile label text</span></span> | <span data-ttu-id="22faa-164">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="22faa-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="22faa-165">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="22faa-165">Description</span></span> | <span data-ttu-id="22faa-166">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="22faa-166">A description of the tile.</span></span> |
   | <span data-ttu-id="22faa-167">Interneto adresas</span><span class="sxs-lookup"><span data-stu-id="22faa-167">Internet address</span></span> | <span data-ttu-id="22faa-168">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="22faa-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="22faa-169">Plytelės dydis</span><span class="sxs-lookup"><span data-stu-id="22faa-169">Tile size</span></span> | <span data-ttu-id="22faa-170">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="22faa-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="22faa-171">Uždavinys</span><span class="sxs-lookup"><span data-stu-id="22faa-171">Target</span></span> | <span data-ttu-id="22faa-172">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="22faa-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="22faa-173">Plytelės fono vaizdas</span><span class="sxs-lookup"><span data-stu-id="22faa-173">Tile background image</span></span> | <span data-ttu-id="22faa-174">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="22faa-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="22faa-175">Pradžios</span><span class="sxs-lookup"><span data-stu-id="22faa-175">Start</span></span> | <span data-ttu-id="22faa-176">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="22faa-177">„End“</span><span class="sxs-lookup"><span data-stu-id="22faa-177">End</span></span> | <span data-ttu-id="22faa-178">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="22faa-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="22faa-179">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="22faa-179">Select **Save**.</span></span>
