---
title: "„Microsoft Project“ kliento integravimas"
description: "Planuoti ir tvarkyti projekto grafiką gali būti sudėtinga, todėl projektų vadovai turi naudoti įrankius, padedančius šią užduotį valdyti. Atlikus integravimą su „Microsoft Project“ klientu, galima atidaryti ir valdyti projekto darbo paskirstymo struktūrą."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4a3445417d5ae88e2ff3676962a82921a7ab475d
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="f4257-104">„Microsoft Project“ kliento integravimas</span><span class="sxs-lookup"><span data-stu-id="f4257-104">Microsoft Project client integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f4257-105">Planuoti ir tvarkyti projekto grafiką gali būti sudėtinga, todėl projektų vadovai turi naudoti įrankius, padedančius šią užduotį valdyti.</span><span class="sxs-lookup"><span data-stu-id="f4257-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="f4257-106">Atlikus integravimą su „Microsoft Project“ klientu, galima atidaryti ir valdyti projekto darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="f4257-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="f4257-107">Projekto vadovas bet kokius keitimus gali publikuoti atgal į „Finance and Operations“ projekto darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="f4257-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="f4257-108">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations“ su 2017 m. liepos mėn. naujinimu, turite įdiegti KB 4054797 ir 4055884.</span><span class="sxs-lookup"><span data-stu-id="f4257-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="f4257-109">„Microsoft Project“ kliento papildinio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f4257-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="f4257-110">Norint įjungti integravimo su „Microsoft Project“ klientu funkciją, vartotojo „Microsoft Project“ kliento programoje reikia įdiegti „Microsoft Dynamics 365“ papildinį.</span><span class="sxs-lookup"><span data-stu-id="f4257-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="f4257-111">Tai daroma atidarant **darbo sritį Projektų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f4257-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="f4257-112">•   Darbo srities skyriuje **Saitai** > **Sąranka** spustelėkite **Konfigūruoti projekto kliento papildinį**.</span><span class="sxs-lookup"><span data-stu-id="f4257-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="f4257-113">•   Paraginti spustelėkite **Atidaryti**, tada – **Paleisti**.</span><span class="sxs-lookup"><span data-stu-id="f4257-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="f4257-114">Esamo darbo paskirstymo struktūros juodraščio atidarymas ir redagavimas „Microsoft Project“ kliente</span><span class="sxs-lookup"><span data-stu-id="f4257-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="f4257-115">Jei „Finance and Operations“ projektui darbo paskirstymo struktūra jau sukurta ir ji yra juodraščio būsenos, ją galima atidaryti „Microsoft Project“ kliento programoje.</span><span class="sxs-lookup"><span data-stu-id="f4257-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="f4257-116">Norėdami ją atidaryti puslapyje **Projektas**, skirtuke **Planas** spustelėkite saitą **Atidaryti naudojant „Microsoft Project“**. Šį puslapį taip pat galima atidaryti „Microsoft Project“ kliento programoje, skirtuke **„Microsoft Dynamics 365“** spustelėjus **Atidaryti**. Sąraše pasirinkite **Juridinis subjektas** ir **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="f4257-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="f4257-117">Jei kaip naršyklę naudojate „Internet Explorer“, turėsite spustelėti **Įrašyti**, kad failą galėtumėte rankiniu būdu atidaryti iš vietos, kurioje jis atsiunčiamas.</span><span class="sxs-lookup"><span data-stu-id="f4257-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="f4257-118">Arba spustelėkite **Įrašyti ir atidaryti**, kad failą atidarytumėte „Microsoft Project“ kliente.</span><span class="sxs-lookup"><span data-stu-id="f4257-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="f4257-119">Įrašydami failą, jo nepervardykite.</span><span class="sxs-lookup"><span data-stu-id="f4257-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="f4257-120">Prieš failą redaguodami „Microsoft Project“ kliente, jį turite paimti ir užrakinti. Skirtuke **„Microsoft Dynamics 365“** spustelėkite **Paimti ir užrakinti**. Tai neleis kitiems vartotojams tuo pačiu metu darbo paskirstymo struktūros redaguoti naudojant „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f4257-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="f4257-121">Jei, baigę redaguoti darbo paskirstymo struktūrą, norite ją publikuoti, skirtuke **„Microsoft Dynamics 365“** spustelėkite **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="f4257-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="f4257-122">Jei į „Finance and Operations“ projektą jau įtraukta projekto komanda, išteklių sąrašas bus užpildytas komandos nariais.</span><span class="sxs-lookup"><span data-stu-id="f4257-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="f4257-123">Jei projekto komanda į projektą dar neįtraukta, galite pasirinkti išteklių ir komandą sukurti „Microsoft Project“ kliente – skirtuke **„Microsoft Dynamics 365“** spustelėkite mygtuką **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="f4257-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="f4257-124">Įrašymo ir atrakinimo proceso metu su „Finance and Operations“ vėl bus sinchronizuojami tolesni duomenys.</span><span class="sxs-lookup"><span data-stu-id="f4257-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="f4257-125">•   Užduoties pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f4257-125">•   Task name</span></span>

<span data-ttu-id="f4257-126">•   Pradžios data</span><span class="sxs-lookup"><span data-stu-id="f4257-126">•   Start date</span></span>

<span data-ttu-id="f4257-127">•   Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="f4257-127">•   Finish date</span></span>

<span data-ttu-id="f4257-128">•   Ankstesnė veikla</span><span class="sxs-lookup"><span data-stu-id="f4257-128">•   Predecessors</span></span>

<span data-ttu-id="f4257-129">•   Išteklių pavadinimai</span><span class="sxs-lookup"><span data-stu-id="f4257-129">•   Resource names</span></span>

<span data-ttu-id="f4257-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="f4257-130">•   Category</span></span>

<span data-ttu-id="f4257-131">•   Išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="f4257-131">•   Resource category</span></span>

<span data-ttu-id="f4257-132">•   Darbo valandos</span><span class="sxs-lookup"><span data-stu-id="f4257-132">•   Work hours</span></span>

<span data-ttu-id="f4257-133">•   Pastabos</span><span class="sxs-lookup"><span data-stu-id="f4257-133">•   Notes</span></span>

<span data-ttu-id="f4257-134">•   Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="f4257-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="f4257-135">Jei į savo „Microsoft Project“ kliento failą įtraukėte kitų stulpelių, jie nebus įrašyti ir, vėl atidarius failą, jie nebus rodomi.</span><span class="sxs-lookup"><span data-stu-id="f4257-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f4257-136">Esamo projekto darbo paskirstymo struktūros kūrimas naudojant „Microsoft Project“ klientą</span><span class="sxs-lookup"><span data-stu-id="f4257-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f4257-137">Jei norite naudodami „Microsoft Project“ klientą sukurti naują darbo paskirstymo struktūrą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4257-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="f4257-138">Atidarykite „Microsoft Project“ klientą.</span><span class="sxs-lookup"><span data-stu-id="f4257-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f4257-139">Skirtuke **„Microsoft Dynamics 365“** spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="f4257-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="f4257-140">Pasirinkite projekto **juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="f4257-141">Pasirinkite **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="f4257-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="f4257-142">Skirtuke **„Microsoft Dynamics 365“** spustelėkite **Paimti ir užrakinti**.</span><span class="sxs-lookup"><span data-stu-id="f4257-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="f4257-143">Kai būsite pasirengę ją publikuoti sprendime „Finance and Operations“, skirtuke **„Microsoft Dynamics 365“** spustelėkite **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="f4257-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="f4257-144">Esamo projekto esamos darbo paskirstymo struktūros pakeitimas naudojant „Microsoft Project“ klientą</span><span class="sxs-lookup"><span data-stu-id="f4257-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="f4257-145">Jei norite naudodami „Microsoft Project“ klientą sukurti naują darbo paskirstymo struktūrą ir pakeisti esamo projekto esamą darbo paskirstymo struktūrą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f4257-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="f4257-146">Atidarykite „Microsoft Project“ klientą.</span><span class="sxs-lookup"><span data-stu-id="f4257-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f4257-147">„Microsoft Project“ kliente sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="f4257-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f4257-148">Skirtuke **„Microsoft Dynamics 365“** spustelėkite **Įrašyti keitimus** > **Pakeisti esamą projektą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="f4257-149">Pasirinkite projekto **juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f4257-150">Pasirinkite **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="f4257-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="f4257-151">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f4257-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="f4257-152">Naujo projekto kūrimas „Microsoft Project“ kliente</span><span class="sxs-lookup"><span data-stu-id="f4257-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="f4257-153">Atidarykite „Microsoft Project“ klientą.</span><span class="sxs-lookup"><span data-stu-id="f4257-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="f4257-154">„Microsoft Project“ kliente sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="f4257-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="f4257-155">Skirtuke **„Microsoft Dynamics 365“** spustelėkite **Įrašyti keitimus** > **Įrašyti į naują projektą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="f4257-156">Pasirinkite projekto **juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="f4257-157">Jei reikia, įveskite **Projekto ID**.</span><span class="sxs-lookup"><span data-stu-id="f4257-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="f4257-158">Įveskite **Projekto pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="f4257-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="f4257-159">Pasirinkite **Projekto tipą**, **Projektų grupę** ir **Projekto sutarties ID**.</span><span class="sxs-lookup"><span data-stu-id="f4257-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="f4257-160">Taip pat naują projekto sutartį galite sukurti spustelėdami **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f4257-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="f4257-161">Pasirinkite **kalendorių**, kuris bus naudojamas su ištekliais.</span><span class="sxs-lookup"><span data-stu-id="f4257-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="f4257-162">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f4257-162">Click **OK**.</span></span>

