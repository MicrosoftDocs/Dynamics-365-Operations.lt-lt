---
title: Darbuotojų savitarnos konfigūravimas
description: Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: dbbcb10f1d14088435248c3354ac153b23e5f8d7
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229814"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="e58a8-103">Darbuotojų savitarnos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e58a8-103">Configure employee self service</span></span>

<span data-ttu-id="e58a8-104">Programoje „Microsoft Dynamics 365 Human Resources“ galite konfigūruoti aukščiausio lygio naršymo plyteles darbuotojo savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="e58a8-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="e58a8-105">Išmokų plano plytelės nukreipia vartotojus į išlaidų planus, kuriems jie tinkami.</span><span class="sxs-lookup"><span data-stu-id="e58a8-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="e58a8-106">Išmokų planų plytelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="e58a8-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="e58a8-107">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="e58a8-108">Pasirinkite skirtuką **Išmokų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="e58a8-109">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="e58a8-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e58a8-110">Laukas</span><span class="sxs-lookup"><span data-stu-id="e58a8-110">Field</span></span> | <span data-ttu-id="e58a8-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e58a8-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e58a8-112">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="e58a8-112">**Tile ID**</span></span> | <span data-ttu-id="e58a8-113">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="e58a8-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="e58a8-114">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-114">**Tile label text**</span></span> | <span data-ttu-id="e58a8-115">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="e58a8-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="e58a8-116">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-116">**Description**</span></span> | <span data-ttu-id="e58a8-117">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-117">A description of the tile.</span></span> |
   | <span data-ttu-id="e58a8-118">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-118">**Internet address**</span></span> | <span data-ttu-id="e58a8-119">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="e58a8-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="e58a8-120">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="e58a8-120">**Tile size**</span></span> | <span data-ttu-id="e58a8-121">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="e58a8-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="e58a8-122">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="e58a8-122">**Target**</span></span> | <span data-ttu-id="e58a8-123">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="e58a8-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="e58a8-124">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-124">**Tile background image**</span></span> | <span data-ttu-id="e58a8-125">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="e58a8-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="e58a8-126">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="e58a8-126">**Start**</span></span> | <span data-ttu-id="e58a8-127">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="e58a8-128">**„End“**</span><span class="sxs-lookup"><span data-stu-id="e58a8-128">**End**</span></span> | <span data-ttu-id="e58a8-129">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="e58a8-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="e58a8-131">Lanksčiųjų kreditų plano plytelės sąranka</span><span class="sxs-lookup"><span data-stu-id="e58a8-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="e58a8-132">Darbo srities **Išlaidų valdymas** dalyje **Sąranka**, pasirinkite **Darbuotojų savitarnos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="e58a8-133">Pasirinkite skirtuką **Lanksčiųjų kreditų planų plytelių sąranka**, tada pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="e58a8-134">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="e58a8-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e58a8-135">Laukas</span><span class="sxs-lookup"><span data-stu-id="e58a8-135">Field</span></span> | <span data-ttu-id="e58a8-136">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e58a8-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e58a8-137">**Plytelės ID**</span><span class="sxs-lookup"><span data-stu-id="e58a8-137">**Tile ID**</span></span> | <span data-ttu-id="e58a8-138">Unikalus plytelės identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="e58a8-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="e58a8-139">**Plytelių etiketės tekstas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-139">**Tile label text**</span></span> | <span data-ttu-id="e58a8-140">Tekstas, kuris bus rodomos ant plytelės savitarnoje.</span><span class="sxs-lookup"><span data-stu-id="e58a8-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="e58a8-141">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-141">**Description**</span></span> | <span data-ttu-id="e58a8-142">Plytelės aprašas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-142">A description of the tile.</span></span> |
   | <span data-ttu-id="e58a8-143">**Interneto adresas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-143">**Internet address**</span></span> | <span data-ttu-id="e58a8-144">Įveskite darbuotojo savitarnos puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="e58a8-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="e58a8-145">**Plytelės dydis**</span><span class="sxs-lookup"><span data-stu-id="e58a8-145">**Tile size**</span></span> | <span data-ttu-id="e58a8-146">Plytelės dydis: mažas, vidutinis arba didelis.</span><span class="sxs-lookup"><span data-stu-id="e58a8-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="e58a8-147">**Uždavinys**</span><span class="sxs-lookup"><span data-stu-id="e58a8-147">**Target**</span></span> | <span data-ttu-id="e58a8-148">Nurodoma, kur turi būti atidaromas puslapis – naujame ar esamame lange.</span><span class="sxs-lookup"><span data-stu-id="e58a8-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="e58a8-149">**Plytelės fono vaizdas**</span><span class="sxs-lookup"><span data-stu-id="e58a8-149">**Tile background image**</span></span> | <span data-ttu-id="e58a8-150">Plytelei naudojamo paveikslėlio URL (pasirinktinai).</span><span class="sxs-lookup"><span data-stu-id="e58a8-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="e58a8-151">**Pradžios**</span><span class="sxs-lookup"><span data-stu-id="e58a8-151">**Start**</span></span> | <span data-ttu-id="e58a8-152">Plytelės naudojimo pradžios data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="e58a8-153">**„End“**</span><span class="sxs-lookup"><span data-stu-id="e58a8-153">**End**</span></span> | <span data-ttu-id="e58a8-154">Plytelės naudojimo pabaigos data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="e58a8-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="e58a8-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e58a8-155">Select **Save**.</span></span>
