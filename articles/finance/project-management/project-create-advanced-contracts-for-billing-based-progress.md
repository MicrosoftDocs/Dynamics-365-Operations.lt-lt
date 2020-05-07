---
title: Išplėstinių atsiskaitymo pagal eigą sutarčių kūrimas
description: Šioje temoje paaiškinama, kaip kurti projekto sutartis, kad būtų galima generuoti klientų SF, atsižvelgiant į užbaigto darbo procentinę dalį.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282839"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="7a4ec-103">Išplėstinių atsiskaitymo pagal eigą sutarčių kūrimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a4ec-104">Šioje temoje paaiškinama, kaip kurti projekto sutartis, kad būtų galima kurti klientų SF, atsižvelgiant į užbaigto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="7a4ec-105">Automatiškai apskaičiuojamos projekte nustatyto darbo biudžeto kategorijų SF sumos.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="7a4ec-106">SF išrašymo laikas nustatomas derinant projekto sutartį su klientu.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="7a4ec-107">Naudokite šioje temoje aprašytas procedūras, norėdami nustatyti sutartį, susijusį projektą ir atsiskaitymo taisykles, apskaičiuojančias projekte numatyto darbo biudžeto kategorijų SF sumas.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="7a4ec-108">Sukūrę sutartį ir projektą, galite nustatyti išsamią projekto informaciją.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="7a4ec-109">Pvz., galite nustatyti veiklą ir priskirti darbuotojus projektui.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="7a4ec-110">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7a4ec-110">Example</span></span>

<span data-ttu-id="7a4ec-111">Jūsų organizacija yra programinę įrangą kurianti įmonė.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-111">Your organization is a software development firm.</span></span> <span data-ttu-id="7a4ec-112">Jūs sutinkate klientui sukurti darbo užmokesčio apskaitos paketą už 20 000 JAV dolerių (USD).</span><span class="sxs-lookup"><span data-stu-id="7a4ec-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="7a4ec-113">Jūsų organizacija susitaria išrašyti klientui SF, kai bus atlikta tam tikra projekto dalis.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="7a4ec-114">Galite nustatyti tolesnes darbo projekto kategorijas, kad galėtumėte jas naudoti atsiskaitymo procese.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="7a4ec-115">Konsultavimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-115">Consulting</span></span>
- <span data-ttu-id="7a4ec-116">Dizainas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-116">Design</span></span>
- <span data-ttu-id="7a4ec-117">Diegimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-117">Installation</span></span>

<span data-ttu-id="7a4ec-118">Taip pat galite nustatyti atsiskaitymo taisykles, kad SF sumos būtų automatiškai apskaičiuojamos pagal tai, kiek atlikta kiekvienos kategorijos projekto darbo.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="7a4ec-119">Biudžeto vadybininkas sukuria biudžetą pagal projekto kategorijas.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="7a4ec-120">Atlikto darbo kiekis automatiškai apskaičiuojamas procentais pagal faktinio darbo kiekį, palyginti su biudžeto sumomis.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a4ec-121">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="7a4ec-121">Prerequisites</span></span>

<span data-ttu-id="7a4ec-122">Prieš kurdami projektą, naudojantį atsiskaitymo taisykles, turite nustatyti atsiskaitymo taisyklių numeracijas ir mokesčių žurnalą, naudojamą registruoti sąskaitų pateikimo eigą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="7a4ec-123">Eikite į **Projektų valdymas ir apskaita** \> **Nustatymas** \> **Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="7a4ec-124">Puslapyje **Projekto valdymo ir apskaitos parametrai**, skirtuke **Numeracijos**, nustatykite numeraciją, kurią norite naudoti, kai kuriamos atsiskaitymo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="7a4ec-125">Eikite į **Projektų valdymas ir apskaita** \> **Žurnalai** \> **Mokestis**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="7a4ec-126">Puslapyje **Mokesčių žurnalas** pasirinkite **Naujas** ir įveskite žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="7a4ec-127">Sukurkite sutartį dėl sąskaitų pateikimo eigos.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-127">Create a contract for progress billings</span></span>

<span data-ttu-id="7a4ec-128">Naudodami šią procedūrą sukurkite projekto sutartį, skirtą fiksuotos kainos projektui.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="7a4ec-129">Galite sukurti projekto SF, kai įvykdyta nurodyta dalis projekto darbų (procentais).</span><span class="sxs-lookup"><span data-stu-id="7a4ec-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="7a4ec-130">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projekto sutartys**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="7a4ec-131">Puslapyje **Projekto sutartys** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="7a4ec-132">Dialogo lange **Nauja projekto sutartis** nustatykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="7a4ec-133">**Vardas ir (arba) pavardė**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-133">**Name**</span></span>
    - <span data-ttu-id="7a4ec-134">**Lėšų skyrimo tipas**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-134">**Funding type**</span></span>
    - <span data-ttu-id="7a4ec-135">**Lėšų skyrimo šaltinis**</span><span class="sxs-lookup"><span data-stu-id="7a4ec-135">**Funding source**</span></span>
    - <span data-ttu-id="7a4ec-136">**Pardavimo valiuta** – pagal numatytuosius parametrus ši valiuta naudojama kliento SF, kurios susietos si projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="7a4ec-137">Tačiau galite keisti konkrečios kliento SF pardavimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="7a4ec-138">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-138">Select **OK**.</span></span> <span data-ttu-id="7a4ec-139">Informacija nukopijuojama į puslapio **Projekto sutartys** antraštę.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="7a4ec-140">Puslapyje **Projekto sutartys** įveskite likusią reikiamą projekto informaciją.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="7a4ec-141">Sąskaitų pateikimo eigos projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-141">Create a project for progress billings</span></span>

<span data-ttu-id="7a4ec-142">Atlikite šiuos veiksmus kurdami projektą ir visus subprojektus, susietus su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="7a4ec-143">Pasirinkite **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="7a4ec-144">Puslapyje **Visi projektai** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="7a4ec-145">Dialogo lango **Naujas projektas** lauke **Projekto tipas** pasirinkite **Laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="7a4ec-146">Pasirinkite projektų grupę.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-146">Select a project group.</span></span> <span data-ttu-id="7a4ec-147">Projektų grupė nustato grupei priskirtų projektų registravimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="7a4ec-148">Pasirinkite **Kurti projektą**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-148">Select **Create project**.</span></span>
6. <span data-ttu-id="7a4ec-149">Sukūrę projektą, nustatykite projekto etapą **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="7a4ec-150">Projekto biudžeto kūrimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-150">Create a budget for a project</span></span>

<span data-ttu-id="7a4ec-151">Biudžeto kategorijos naudojamos siekiant automatiškai apskaičiuoti SF sumas pagal tai, kiek atlikta kiekvienos kategorijos darbų.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="7a4ec-152">Atlikite tolesnius veiksmus, norėdami sukurti įvertintų savikainų biudžeto kategorijas.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="7a4ec-153">Pasirinkite **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="7a4ec-154">Puslapyje **Visi projektai** pasirinkite ir atidarykite norimą projektą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="7a4ec-155">Puslapio **Projektai** veiksmų srityje, skirtuke **Planuoti**, grupėje **Biudžetas**, pasirinkite **Projekto biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="7a4ec-156">Puslapyje **Projekto biudžetas** įveskite kiekvienos projekto kategorijos įvertintą savikainą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="7a4ec-157">Sąskaitų pateikimo eigai skirtų atsiskaitymo taisyklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="7a4ec-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="7a4ec-158">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projekto sutartys**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="7a4ec-159">Puslapyje **Projekto sutartys** pasirinkite ir atidarykite projekto sutartį.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="7a4ec-160">Projekto sutarties puslapyje, „FastTab” **Atsiskaitymo taisyklės**, pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="7a4ec-161">Puslapyje **Atsiskaitymo taisyklė**, lauke **Eilutės tipas**, pasirinkite **Eiga**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="7a4ec-162">„FastTab” **Atsiskaitymo taisyklės eilutės informacija**, lauke **Sutarties vertė**, įveskite bendrąją sutarties vertę.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="7a4ec-163">Lauke **Kategorija** pasirinkite kategoriją, kurioje turi būti užregistruota mokesčio operacija.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="7a4ec-164">Lauke **Projektas** pasirinkite projektą arba užduotį, kurioje naudojama ši atsiskaitymo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="7a4ec-165">Pasirinktinai: atsiskaitymo taisyklę priskirkite papildomiems projektams.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="7a4ec-166">„FastTab” **Projektas** skyriuje **Galimi projektai** pasirinkite projektą, tada pasirinkite rodyklės dešinėn mygtuką, kad įtrauktumėte projektą į skyrių **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="7a4ec-167">Pasirinktinai: apskaičiuokite procentinę sumą, kuri klientui išskaitoma iš mokėjimų sąskaitoje-faktūroje.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="7a4ec-168">„FastTab” **Mokėjimo užlaikymo sąlygos** pasirinkite lėšų skyrimo šaltinį, tada lauke **Užlaikymo procentinis dydis** įveskite užlaikymo procentą.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="7a4ec-169">Kartokite šiuos veiksmus norėdami sukurti papildomas projekto sutarties atsiskaitymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="7a4ec-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
