---
title: Registracijos tinkamumo apdorojimas
description: Šiame straipsnyje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d978982213e713e362798c49aa57e6dc8b7a862
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230021"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="010d3-103">Registracijos tinkamumo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="010d3-103">Process enrollment eligibility</span></span>

<span data-ttu-id="010d3-104">Šiame straipsnyje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="010d3-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="010d3-105">Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Registracijos tinkamumo apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="010d3-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="010d3-106">Dialogo lange **Vykdyti registracijos išmokoms gauti tinkamumo apdorojimą** nurodykite šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="010d3-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="010d3-107">Laukas</span><span class="sxs-lookup"><span data-stu-id="010d3-107">Field</span></span> | <span data-ttu-id="010d3-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="010d3-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="010d3-109">**Registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="010d3-109">**Enrollment period**</span></span> | <span data-ttu-id="010d3-110">Ragistracijos tinkamumo apdorojimo registracijos laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="010d3-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="010d3-111">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="010d3-111">**Legal entity**</span></span> | <span data-ttu-id="010d3-112">Registracijos tinkamumo apdorojimo juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="010d3-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="010d3-113">**Darbininkas**</span><span class="sxs-lookup"><span data-stu-id="010d3-113">**Worker**</span></span> | <span data-ttu-id="010d3-114">Registracijos tinkamumo apdorojimo darbininkas.</span><span class="sxs-lookup"><span data-stu-id="010d3-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="010d3-115">Jei paliksite šį lauką tuščią, visų darbuotojų registracijos tinkamumas bus apdorojamas.</span><span class="sxs-lookup"><span data-stu-id="010d3-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="010d3-116">**Išmokų planas**</span><span class="sxs-lookup"><span data-stu-id="010d3-116">**Benefit plan**</span></span> | <span data-ttu-id="010d3-117">Registracijos tinkamumo apdorojimo išmokų planas.</span><span class="sxs-lookup"><span data-stu-id="010d3-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="010d3-118">Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="010d3-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="010d3-119">Įveskite proceso informaciją.</span><span class="sxs-lookup"><span data-stu-id="010d3-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="010d3-120">Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="010d3-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="010d3-121">Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="010d3-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="010d3-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="010d3-122">Select **OK**.</span></span> <span data-ttu-id="010d3-123">Procesas bus vykdomas naudojant jūsų nustatytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="010d3-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="010d3-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="010d3-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="010d3-125">Proceso rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="010d3-125">View Process Results</span></span>

<span data-ttu-id="010d3-126">Šiame straipsnyje paaiškinama, kaip peržiūrėti tinkamumo proceso rezultatus.</span><span class="sxs-lookup"><span data-stu-id="010d3-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="010d3-127">Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Proceso rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="010d3-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="010d3-128">Formoje **Proceso rezultatai** nurodyti toliau pateikti laukai.</span><span class="sxs-lookup"><span data-stu-id="010d3-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="010d3-129">Laukas</span><span class="sxs-lookup"><span data-stu-id="010d3-129">Field</span></span> | <span data-ttu-id="010d3-130">aprašymas</span><span class="sxs-lookup"><span data-stu-id="010d3-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="010d3-131">**Eigos ID**</span><span class="sxs-lookup"><span data-stu-id="010d3-131">**Process ID**</span></span> | <span data-ttu-id="010d3-132">Unikalus darbuotojo, juridinio subjekto ir proceso vykdymo derinio ID.</span><span class="sxs-lookup"><span data-stu-id="010d3-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="010d3-133">**Proceso tipas**</span><span class="sxs-lookup"><span data-stu-id="010d3-133">**Process type**</span></span> | <span data-ttu-id="010d3-134">Taip identifikuojamas procesas, kuris buvo vykdomas.</span><span class="sxs-lookup"><span data-stu-id="010d3-134">This identifies the process that was run.</span></span> <span data-ttu-id="010d3-135">Pvz.: registracija.</span><span class="sxs-lookup"><span data-stu-id="010d3-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="010d3-136">**Laiko antspaudas**</span><span class="sxs-lookup"><span data-stu-id="010d3-136">**Time stamp**</span></span> | <span data-ttu-id="010d3-137">Tinkamumo proceso vykdymo laikas.</span><span class="sxs-lookup"><span data-stu-id="010d3-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="010d3-138">**Juridinis subjektas**</span><span class="sxs-lookup"><span data-stu-id="010d3-138">**Legal entity**</span></span> | <span data-ttu-id="010d3-139">Registravimo proceso metu nurodytas juridinis subjektas.</span><span class="sxs-lookup"><span data-stu-id="010d3-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="010d3-140">**Darbuotojas**</span><span class="sxs-lookup"><span data-stu-id="010d3-140">**Worker**</span></span> | <span data-ttu-id="010d3-141">Darbuotojas, kuris buvo apdorotas.</span><span class="sxs-lookup"><span data-stu-id="010d3-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="010d3-142">\*\*Planas</span><span class="sxs-lookup"><span data-stu-id="010d3-142">\*\*Plan</span></span> | <span data-ttu-id="010d3-143">Išmokų planas, dėl kurio buvo bandyta registracija.</span><span class="sxs-lookup"><span data-stu-id="010d3-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="010d3-144">**Tinkamumo taisyklė**</span><span class="sxs-lookup"><span data-stu-id="010d3-144">**Eligibility rule**</span></span> | <span data-ttu-id="010d3-145">Apdorota tinkamumo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="010d3-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="010d3-146">Jei prieš tinkamumo vykdymą įvyko klaida, šis laukas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="010d3-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="010d3-147">Pvz.: jei darbuotojo kompensacija nebuvo nustatyta, tinkamumo procesas nebus vykdomas, o šis laukas liks tuščias.</span><span class="sxs-lookup"><span data-stu-id="010d3-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="010d3-148">**Rezultato būsena**</span><span class="sxs-lookup"><span data-stu-id="010d3-148">**Result status**</span></span> | <span data-ttu-id="010d3-149">Ji bus Tinkama arba Netinkama.</span><span class="sxs-lookup"><span data-stu-id="010d3-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="010d3-150">Rezultato būsena bus Netinkama, jei darbuotojas neatitinka tinkamumo taisyklės kriterijų, jei trūksta būtinos darbuotojo informacijos, pvz., mokėjimo dažnumo arba pastoviosios atlyginimo dalies, arba jei trūksta informacijos apie išmokų planą ir tai neleidžia darbuotojams būti užregistruotiems.</span><span class="sxs-lookup"><span data-stu-id="010d3-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="010d3-151">**Rezultato pranešimas**</span><span class="sxs-lookup"><span data-stu-id="010d3-151">**Result message**</span></span> | <span data-ttu-id="010d3-152">Nurodo, kodėl darbuotojas netinkamas išmokų planui gauti arba kad buvo išlaikyta tinkamumo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="010d3-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

