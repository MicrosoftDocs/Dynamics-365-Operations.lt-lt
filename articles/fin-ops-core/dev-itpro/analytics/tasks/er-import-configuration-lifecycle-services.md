---
title: Konfigūracijos importavimas iš „Lifecycle Services‟
description: Šioje temoje aprašoma, kaip iš Microsoft Dynamics „Lifecycle Services” (LCS) importuoti naują elektroninių ataskaitų konfigūracijos versiją.
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270842"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="c54c9-103">Konfigūracijos importavimas iš „Lifecycle Services”</span><span class="sxs-lookup"><span data-stu-id="c54c9-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c54c9-104">Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali importuoti naują [elektroninių ataskaitų (ER) konfigūracijos](../general-electronic-reporting.md#Configuration) versiją iš [projekto lygio turto bibliotekos](../../lifecycle-services/asset-library.md) „Microsoft Dynamics Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="c54c9-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c54c9-105">LCS naudojimas kaip ER konfigūracijų saugyklos yra [nerekomenduojamas](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="c54c9-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="c54c9-106">Daugiau informacijos rasite [„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nerekomenduojama](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="c54c9-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="c54c9-107">Šiame pavyzdyje pasirinksite pavyzdinės įmonės pavadinimu „Litware, Inc“ pageidaujamą ER konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="c54c9-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="c54c9-108">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti [Konfigūracijos įkėlimas į „Lifecycle Services”](er-upload-configuration-into-lifecycle-services.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c54c9-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c54c9-109">Taip pat reikia prieigos prie LCS.</span><span class="sxs-lookup"><span data-stu-id="c54c9-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="c54c9-110">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="c54c9-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="c54c9-111">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="c54c9-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="c54c9-112">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="c54c9-112">System administrator</span></span>

2. <span data-ttu-id="c54c9-113">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="c54c9-114">Pasirinkite **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="c54c9-115">Įsitikinkite, kad dabartinis „Dynamics 365 Finance” vartotojas yra LCS projekto, kuriame yra turto biblioteka, kurią vartotojas nori [pasiekti](../../lifecycle-services/asset-library.md#asset-library-support), naudojama ER konfigūracijoms importuoti, narys.</span><span class="sxs-lookup"><span data-stu-id="c54c9-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="c54c9-116">Negalima pasiekti LCS projekto iš ER saugyklos, kuri nurodo domeną, kuris skiriasi nuo domeno, naudojamo „Finance”.</span><span class="sxs-lookup"><span data-stu-id="c54c9-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="c54c9-117">Jei bandysite, bus rodomas tuščias LCS projektų sąrašas, o jūs negalėsite importuoti ER konfigūracijų iš projekto lygio turto bibliotekos, esančios LCS.</span><span class="sxs-lookup"><span data-stu-id="c54c9-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="c54c9-118">Norėdami pasiekti projekto lygio turto bibliotekas iš ER saugyklos, naudojamos importuoti ER konfigūracijas, prisijunkite prie „Finance” naudodami vartotojo, priklausančio nuomotojui (domenui), kuriam sukonfigūruotas dabartinis „Finance” egzempliorius, kredencialus.</span><span class="sxs-lookup"><span data-stu-id="c54c9-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="c54c9-119">Duomenų modelio konfigūracijos bendrai naudojamos versijos naikinimas</span><span class="sxs-lookup"><span data-stu-id="c54c9-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="c54c9-120">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="c54c9-121">Sukūrėte pirmąją modelio konfigūracijos pavyzdžio versiją ir publikavote ją LCS atlikę [Konfigūracijos įkėlimas į „Lifecycle Services“](er-upload-configuration-into-lifecycle-services.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c54c9-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="c54c9-122">Atlikdami šią procedūrą, šią ER konfigūracijos versiją panaikinsite.</span><span class="sxs-lookup"><span data-stu-id="c54c9-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="c54c9-123">Tada versiją importuosite iš LCS, kaip aprašyta toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="c54c9-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="c54c9-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c54c9-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c54c9-125">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="c54c9-126">Ši būsena nurodo, kad konfigūracija publikuota LCS portale.</span><span class="sxs-lookup"><span data-stu-id="c54c9-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="c54c9-127">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-127">Select **Change status**.</span></span>
4. <span data-ttu-id="c54c9-128">Pasirinkite **Nebenaudoti**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="c54c9-129">Kad galėtumėte versiją panaikinti, jos būseną pakeiskite iš **Bendrinama** į **Nebenaudojama**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="c54c9-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-130">Select **OK**.</span></span>
6. <span data-ttu-id="c54c9-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c54c9-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c54c9-132">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Nebenaudojama**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="c54c9-133">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-133">Select **Delete**.</span></span>
8. <span data-ttu-id="c54c9-134">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-134">Select **Yes**.</span></span>

    <span data-ttu-id="c54c9-135">Atkreipkite dėmesį, kad dabar galima naudoti tik 2 pasirinktos duomenų modelio konfigūracijos juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="c54c9-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="c54c9-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c54c9-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="c54c9-137">Duomenų modelio konfigūracijos bendrai naudojamos versijos importavimas iš LCS</span><span class="sxs-lookup"><span data-stu-id="c54c9-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="c54c9-138">Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="c54c9-139">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Litware, Inc.”**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="c54c9-140">Plytelėje **„Litware, Inc.”** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="c54c9-141">Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="c54c9-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="c54c9-142">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-142">Select **Open**.</span></span>

    <span data-ttu-id="c54c9-143">Šiame pavyzdyje pasirinkite **LCS** saugyklą ir atidarykite.</span><span class="sxs-lookup"><span data-stu-id="c54c9-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="c54c9-144">Turite turėti [prieigą](#accessconditions) prie LCS projekto ir turto bibliotekos, kuri pasiekiama naudojant pasirinktą ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="c54c9-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="c54c9-145">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c54c9-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="c54c9-146">Šiame pavyzdyje versijų sąraše pasirinkite pirmąją **Modelio konfigūracijos pavyzdys** versiją.</span><span class="sxs-lookup"><span data-stu-id="c54c9-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="c54c9-147">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-147">Select **Import**.</span></span>
7. <span data-ttu-id="c54c9-148">Pasirinkite **Taip**, norėdami patvirtinti pasirinktos versijos importavimą iš LCS.</span><span class="sxs-lookup"><span data-stu-id="c54c9-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="c54c9-149">Informacinis pranešimas patvirtina, kad pasirinkta versija buvo sėkmingai importuota.</span><span class="sxs-lookup"><span data-stu-id="c54c9-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="c54c9-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c54c9-150">Close the page.</span></span>
9. <span data-ttu-id="c54c9-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c54c9-151">Close the page.</span></span>
10. <span data-ttu-id="c54c9-152">Pasirinkite **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="c54c9-153">Medyje pasirinkite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="c54c9-154">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c54c9-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="c54c9-155">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="c54c9-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="c54c9-156">Atkreipkite dėmesį, kad dabar taip pat galima naudoti ir 1 pasirinktos duomenų modelio konfigūracijos bendrai naudojamą versiją.</span><span class="sxs-lookup"><span data-stu-id="c54c9-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
