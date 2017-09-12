---
title: "Darbo eigos kūrimas"
description: "Šioje temoje paaiškinama, kaip sukurti darbo eigą."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, UnifiedOperations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4d57e47fe7f38a43ecfdfbdd701d7e6a7d7800d6
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="create-a-workflow"></a><span data-ttu-id="ef54b-103">Darbo eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-103">Create a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ef54b-104">Šioje temoje paaiškinama, kaip sukurti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-104">This topics explains how to create a workflow.</span></span>

<a name="open-the-workflow-editor"></a><span data-ttu-id="ef54b-105">Darbo eigos rengyklės atidarymas</span><span class="sxs-lookup"><span data-stu-id="ef54b-105">Open the workflow editor</span></span>
------------------------

<span data-ttu-id="ef54b-106">„Microsoft Dynamics 365 for Finance and Operations“ modulis, kuriame dirbate, nustato galimus kurti darbo eigos tipus.</span><span class="sxs-lookup"><span data-stu-id="ef54b-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="ef54b-107">Atlikite šiuos veiksmus, kad pasirinktumėte darbo eigos, kurią norite kurti, tipą ir atidarytumėte darbo eigos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="ef54b-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1.  <span data-ttu-id="ef54b-108">Atidarykite modulį, kuriame norite sukurti naują darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="ef54b-109">Pavyzdžiui, jei norite sukurti pirkimo paraiškų darbo eigą, eikite į modulį, spustelėkite **Paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2.  <span data-ttu-id="ef54b-110">Spustelėkite **Sąranka** &gt; **\[Modulio pavadinimas\] darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3.  <span data-ttu-id="ef54b-111">Sąrašo puslapio, kuris pasirodo, veiksmų srityje spustelėkite skirtuką **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4.  <span data-ttu-id="ef54b-112">Puslapyje **Darbo eigos kūrimas** pasirinkite norimos kurti darbo eigos tipą ir tada spustelėkite **Kurti darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="ef54b-113">Atidaroma darbo eigos rengyklė.</span><span class="sxs-lookup"><span data-stu-id="ef54b-113">The workflow editor appears.</span></span> <span data-ttu-id="ef54b-114">Dabar galite naudoti toliau nurodytas procedūras, kad sumodeliuotumėte darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="ef54b-115">Darbo eigos elementų nuvilkimas į kūrimo sritį</span><span class="sxs-lookup"><span data-stu-id="ef54b-115">Drag workflow elements onto the canvas</span></span>
<span data-ttu-id="ef54b-116">Darbo eigos rengyklės srityje **Darbo eigos elementai** pateikti elementai, kuriuos galite įtraukti į savo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="ef54b-117">Norėdami įtraukti elementus į darbo eigą, nuvilkite juos į drobę.</span><span class="sxs-lookup"><span data-stu-id="ef54b-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="ef54b-118">Elementų sujungimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-118">Connect the elements</span></span>
<span data-ttu-id="ef54b-119">Norėdami vieną darbo eigos elementą sujungti su kitu, laikykite žymiklį ant elemento, kol atsiras jungties taškai.</span><span class="sxs-lookup"><span data-stu-id="ef54b-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="ef54b-120">Spustelėkite sujungimo tašką ir vilkite jį prie kito elemento.</span><span class="sxs-lookup"><span data-stu-id="ef54b-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="ef54b-121">Būtinai sujunkite visus elementus.</span><span class="sxs-lookup"><span data-stu-id="ef54b-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="ef54b-122">Darbo eigos ypatybių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-122">Configure the properties of the workflow</span></span>
<span data-ttu-id="ef54b-123">Atlikite toliau nurodytus veiksmus, kad sukonfigūruotumėte darbo eigos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="ef54b-123">Follow these steps to configure the properties of the workflow.</span></span>

1.  <span data-ttu-id="ef54b-124">Spustelėkite kūrimo sritį, kad įsitikintumėte, jog nepasirinktas joks darbo eigos elementas.</span><span class="sxs-lookup"><span data-stu-id="ef54b-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2.  <span data-ttu-id="ef54b-125">Spustelėkite **Ypatybės**, kad atidarytumėte darbo eigos puslapį **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3.  <span data-ttu-id="ef54b-126">Naudokite procedūras, pateiktas temoje [Darbo eigos ypatybių konfigūravimas](configure-workflow-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ef54b-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="ef54b-127">Darbo eigos elementų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-127">Configure the elements of the workflow</span></span>
<span data-ttu-id="ef54b-128">Sukonfigūruokite kiekvieną elementą, kurį nuvilkote į kūrimo sritį.</span><span class="sxs-lookup"><span data-stu-id="ef54b-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="ef54b-129">Daugiau informacijos, kaip konfigūruoti kiekvieną darbo eigos elementą, žr. tolesnes temas.</span><span class="sxs-lookup"><span data-stu-id="ef54b-129">For information about how to configure each workflow element, see the following topics:</span></span>

-   [<span data-ttu-id="ef54b-130">Neautomatizuotos užduoties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
-   [<span data-ttu-id="ef54b-131">Automatizuotos užduoties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
-   [<span data-ttu-id="ef54b-132">Patvirtinimo proceso konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
-   [<span data-ttu-id="ef54b-133">Patvirtinimo veiksmo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
-   [<span data-ttu-id="ef54b-134">Neautomatizuoto sprendimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
-   [<span data-ttu-id="ef54b-135">Sąlyginio sprendimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
-   [<span data-ttu-id="ef54b-136">Lygiagrečios veiklos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
-   [<span data-ttu-id="ef54b-137">Lygiagrečios šakos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
-   [<span data-ttu-id="ef54b-138">Eilutės elemento darbo eigos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="ef54b-139">Visų klaidų ir perspėjimų sprendimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-139">Resolve any errors or warnings</span></span>
<span data-ttu-id="ef54b-140">Srityje **Klaidos ir perspėjimai**, esančioje darbo eigos rengyklės apačioje, rodomi sugeneruoti pranešimai apie darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="ef54b-141">Norėdami rasti elementą, kuriame įvyko klaida arba buvo sugeneruotas perspėjimas, dukart spustelėkite klaidos arba perspėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ef54b-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="ef54b-142">Norint suaktyvinti darbo eigą, prieš tai reikia išspręsti visas klaidas ir perspėjimus.</span><span class="sxs-lookup"><span data-stu-id="ef54b-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="ef54b-143">Darbo eigos įrašymas ir suaktyvinimas</span><span class="sxs-lookup"><span data-stu-id="ef54b-143">Save and activate the workflow</span></span>
<span data-ttu-id="ef54b-144">Kai būsite pasirengę įrašyti ir suaktyvinti darbo eigą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ef54b-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="ef54b-145">Spustelėkite **Įrašyti ir uždaryti**, kad uždarytumėte darbo eigos rengyklę ir atidarytumėte puslapį **Įrašyti darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2.  <span data-ttu-id="ef54b-146">Įveskite komentarus apie atliktus darbo eigos pakeitimus, o tada spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3.  <span data-ttu-id="ef54b-147">Jei visos klaidos ir perspėjimai išspręsti, bus rodomas puslapis **Darbo eigos aktyvinimas**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="ef54b-148">Pasirinkite vieną iš toliau pateiktų pasirinkčių:</span><span class="sxs-lookup"><span data-stu-id="ef54b-148">Select one of the following options:</span></span>
    -   <span data-ttu-id="ef54b-149">Norėdami aktyvinti šią darbo eigos versiją, spustelėkite **Aktyvinti naują versiją**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="ef54b-150">Kai darbo eiga aktyvi, vartotojai galės pateikti dokumentus apdoroti.</span><span class="sxs-lookup"><span data-stu-id="ef54b-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    -   <span data-ttu-id="ef54b-151">Jei šios versijos aktyvinti nenorite, spustelėkite **Neaktyvinti naujos versijos**.</span><span class="sxs-lookup"><span data-stu-id="ef54b-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="ef54b-152">Darbo eigą galite suaktyvinti vėliau.</span><span class="sxs-lookup"><span data-stu-id="ef54b-152">You can activate the workflow later.</span></span>






