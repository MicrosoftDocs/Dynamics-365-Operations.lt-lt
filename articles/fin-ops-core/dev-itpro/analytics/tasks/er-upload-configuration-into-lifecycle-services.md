---
title: Konfigūracijos nusiuntimas į „Lifecycle Services‟
description: Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali sukurti naują elektroninių ataskaitų (ER) konfigūraciją ir ją nusiųsti į „Microsoft Dynamics Lifecycle Services‟ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ebafb52882fd33f4f0ef140c5d23d3288af97a2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684168"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="912a3-103">Konfigūracijos nusiuntimas į „Lifecycle Services‟</span><span class="sxs-lookup"><span data-stu-id="912a3-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="912a3-104">Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali sukurti naują [elektroninių ataskaitų (ER) konfigūraciją](../general-electronic-reporting.md#Configuration) ir ją nusiųsti į [projekto lygio turto biblioteką](../../lifecycle-services/asset-library.md) „Microsoft Dynamics Lifecycle Services‟ (LCS).</span><span class="sxs-lookup"><span data-stu-id="912a3-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="912a3-105">Šiame pavyzdyje sukursite pavyzdinės įmonės pavadinimu „Litware, Inc“ konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="912a3-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="912a3-106">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="912a3-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="912a3-107">Taip pat reikia prieigos prie LCS.</span><span class="sxs-lookup"><span data-stu-id="912a3-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="912a3-108">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="912a3-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="912a3-109">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="912a3-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="912a3-110">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="912a3-110">System administrator</span></span>

2. <span data-ttu-id="912a3-111">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="912a3-112">Pasirinkite **„Litware, Inc.‟** ir nustatykite į **Aktyvi**.</span><span class="sxs-lookup"><span data-stu-id="912a3-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="912a3-113">Pasirinkite **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="912a3-114">Įsitikinkite, kad dabartinis „Dynamics 365 Finance” vartotojas yra LCS projekto, kuriame yra [turto biblioteka](../../lifecycle-services/asset-library.md#asset-library-support), naudojama ER konfigūracijoms importuoti, narys.</span><span class="sxs-lookup"><span data-stu-id="912a3-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="912a3-115">Negalima pasiekti LCS projekto iš ER saugyklos, kuri nurodo domeną, kuris skiriasi nuo domeno, naudojamo „Finance”.</span><span class="sxs-lookup"><span data-stu-id="912a3-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="912a3-116">Jei bandysite, bus rodomas tuščias LCS projektų sąrašas, o jūs negalėsite importuoti ER konfigūracijų iš projekto lygio turto bibliotekos, esančios LCS.</span><span class="sxs-lookup"><span data-stu-id="912a3-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="912a3-117">Norėdami pasiekti projekto lygio turto bibliotekas iš ER saugyklos, naudojamos importuoti ER konfigūracijas, prisijunkite prie „Finance” naudodami vartotojo, priklausančio nuomotojui (domenui), kuriam sukonfigūruotas dabartinis „Finance” egzempliorius, kredencialus.</span><span class="sxs-lookup"><span data-stu-id="912a3-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="912a3-118">Sukurti naują duomenų modelio konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="912a3-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="912a3-119">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="912a3-120">Puslapyje **Konfigūracijos** pasirinkite **Kurti konfigūraciją**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="912a3-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="912a3-121">Šiame pavyzdyje sukursite konfigūraciją, apimančią elektroninių dokumentų duomenų modelio pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="912a3-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="912a3-122">Ši duomenų modelio konfigūracija vėliau bus nusiųsta į LCS.</span><span class="sxs-lookup"><span data-stu-id="912a3-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="912a3-123">Lauke **Pavadinimas** įveskite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="912a3-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="912a3-124">Lauke **Aprašas** įveskite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="912a3-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="912a3-125">Pasirinkite **Kurti konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="912a3-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="912a3-126">Pasirinkite **Modelio dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="912a3-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="912a3-127">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="912a3-127">Select **New**.</span></span>
8. <span data-ttu-id="912a3-128">Lauke **Pavadinimas** įveskite **Įvesties taškas**.</span><span class="sxs-lookup"><span data-stu-id="912a3-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="912a3-129">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-129">Select **Add**.</span></span>
10. <span data-ttu-id="912a3-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-130">Select **Save**.</span></span>
11. <span data-ttu-id="912a3-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="912a3-131">Close the page.</span></span>
12. <span data-ttu-id="912a3-132">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="912a3-132">Select **Change status**.</span></span>
13. <span data-ttu-id="912a3-133">Pasirinkite **Baigti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-133">Select **Complete**.</span></span>
14. <span data-ttu-id="912a3-134">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="912a3-134">Select **OK**.</span></span>
15. <span data-ttu-id="912a3-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="912a3-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="912a3-136">Naujos saugyklos registravimas</span><span class="sxs-lookup"><span data-stu-id="912a3-136">Register a new repository</span></span>

1. <span data-ttu-id="912a3-137">Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="912a3-138">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Litware, Inc.”**.</span><span class="sxs-lookup"><span data-stu-id="912a3-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="912a3-139">Plytelėje **„Litware, Inc.”** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="912a3-140">Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="912a3-141">Pažymėkite **Įtraukti**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="912a3-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="912a3-142">Dabar galite įtraukti naują saugyklą.</span><span class="sxs-lookup"><span data-stu-id="912a3-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="912a3-143">Lauke **Konfigūracijų saugykla** pasirinkite **LCS**.</span><span class="sxs-lookup"><span data-stu-id="912a3-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="912a3-144">Pasirinkite **Kurti saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="912a3-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="912a3-145">Lauke **Projektas** įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="912a3-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="912a3-146">Šiame pavyzdyje pasirinkite norimą LCS projektą.</span><span class="sxs-lookup"><span data-stu-id="912a3-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="912a3-147">Turite turėti [prieigą](#accessconditions) prie projekto.</span><span class="sxs-lookup"><span data-stu-id="912a3-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="912a3-148">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="912a3-148">Select **OK**.</span></span>

    <span data-ttu-id="912a3-149">Baikite naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="912a3-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="912a3-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="912a3-151">Šiame pavyzdyje pasirinkite **LCS** saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="912a3-152">Atkreipkite dėmesį, kad registruotą saugyklą pažymėjo dabartinis teikėjas.</span><span class="sxs-lookup"><span data-stu-id="912a3-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="912a3-153">Kitaip tariant, perkelti į šią saugyklą ir vėliau nusiųsti į pasirinktą LCS projektą galima tik tam tiekėjui priklausančias konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="912a3-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="912a3-154">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-154">Select **Open**.</span></span>

    <span data-ttu-id="912a3-155">Atidarę saugyklą galėsite peržiūrėti ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="912a3-156">Jei pasirinktas projektas dar nenaudotas bendrinant ER konfigūracijas, sąrašas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="912a3-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="912a3-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="912a3-157">Close the page.</span></span>
12. <span data-ttu-id="912a3-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="912a3-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="912a3-159">Konfigūracijos nusiuntimas į LCS</span><span class="sxs-lookup"><span data-stu-id="912a3-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="912a3-160">Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="912a3-161">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="912a3-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="912a3-162">Turite pasirinkti sukurtą, jau baigtą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="912a3-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="912a3-163">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="912a3-164">Šiame pavyzdyje pasirinkite pasirinktos konfigūracijos versiją, kurios būsena – **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="912a3-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="912a3-165">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="912a3-165">Select **Change status**.</span></span>
5. <span data-ttu-id="912a3-166">Pasirinkite **Bendrinti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-166">Select **Share**.</span></span>

    <span data-ttu-id="912a3-167">Konfigūracijos būsena pasikeičia iš **Baigta** į **Bendrinama**, kai konfigūracija publikuojama LCS.</span><span class="sxs-lookup"><span data-stu-id="912a3-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="912a3-168">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="912a3-168">Select **OK**.</span></span>
7. <span data-ttu-id="912a3-169">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="912a3-170">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="912a3-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="912a3-171">Atkreipkite dėmesį, kad pasirinktos versijos būsena pasikeitė iš **Baigta** į **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="912a3-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="912a3-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="912a3-172">Close the page.</span></span>
9. <span data-ttu-id="912a3-173">Pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="912a3-173">Select **Repositories**.</span></span>

    <span data-ttu-id="912a3-174">Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="912a3-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="912a3-175">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="912a3-175">Select **Open**.</span></span>

    <span data-ttu-id="912a3-176">Šiame pavyzdyje pasirinkite **LCS** saugyklą ir atidarykite.</span><span class="sxs-lookup"><span data-stu-id="912a3-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="912a3-177">Atkreipkite dėmesį, kad pasirinkta konfigūracija rodoma kaip pasirinkto LCS projekto turtas.</span><span class="sxs-lookup"><span data-stu-id="912a3-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="912a3-178">Atidarykite LCS nuėję į <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="912a3-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="912a3-179">Atidarykite projektą, kuris buvo naudojamas anksčiau saugyklos registracijai.</span><span class="sxs-lookup"><span data-stu-id="912a3-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="912a3-180">Atidarykite projekto turto biblioteką.</span><span class="sxs-lookup"><span data-stu-id="912a3-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="912a3-181">Pasirinkite turto tipą **GER konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="912a3-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="912a3-182">Turi būti nurodyta ER konfigūracija, kurią nusiuntėte.</span><span class="sxs-lookup"><span data-stu-id="912a3-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="912a3-183">Atkreipkite dėmesį, kad, jei tiekėjai turi prieigą prie šio LCS projekto, nusiųstąją LCS konfigūraciją galima importuoti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="912a3-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
