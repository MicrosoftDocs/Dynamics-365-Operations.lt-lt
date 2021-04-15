---
title: Konfigūracijos importavimas iš „Lifecycle Services‟
description: Šioje temoje aprašoma, kaip iš Microsoft Dynamics „Lifecycle Services” (LCS) importuoti naują elektroninių ataskaitų konfigūracijos versiją.
author: NickSelin
ms.date: 09/14/2020
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
ms.openlocfilehash: 674d0dc02b4a53e455a15a06fdb7f24ca3036ba3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752369"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="0603b-103">Konfigūracijos importavimas iš „Lifecycle Services”</span><span class="sxs-lookup"><span data-stu-id="0603b-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0603b-104">Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali importuoti naują [elektroninių ataskaitų (ER) konfigūracijos](../general-electronic-reporting.md#Configuration) versiją iš [projekto lygio turto bibliotekos](../../lifecycle-services/asset-library.md) „Microsoft Dynamics Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="0603b-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="0603b-105">Šiame pavyzdyje pasirinksite pavyzdinės įmonės pavadinimu „Litware, Inc“ pageidaujamą ER konfigūraciją ir nusiųsite į LCS. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="0603b-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="0603b-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti [Konfigūracijos įkėlimas į „Lifecycle Services”](er-upload-configuration-into-lifecycle-services.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0603b-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0603b-107">Taip pat reikia prieigos prie LCS.</span><span class="sxs-lookup"><span data-stu-id="0603b-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="0603b-108">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="0603b-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="0603b-109">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="0603b-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="0603b-110">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="0603b-110">System administrator</span></span>

2. <span data-ttu-id="0603b-111">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="0603b-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0603b-112">Pasirinkite **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="0603b-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="0603b-113">Įsitikinkite, kad dabartinis „Dynamics 365 Finance” vartotojas yra LCS projekto, kuriame yra turto biblioteka, kurią vartotojas nori [pasiekti](../../lifecycle-services/asset-library.md#asset-library-support), naudojama ER konfigūracijoms importuoti, narys.</span><span class="sxs-lookup"><span data-stu-id="0603b-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="0603b-114">Negalima pasiekti LCS projekto iš ER saugyklos, kuri nurodo domeną, kuris skiriasi nuo domeno, naudojamo „Finance”.</span><span class="sxs-lookup"><span data-stu-id="0603b-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="0603b-115">Jei bandysite, bus rodomas tuščias LCS projektų sąrašas, o jūs negalėsite importuoti ER konfigūracijų iš projekto lygio turto bibliotekos, esančios LCS.</span><span class="sxs-lookup"><span data-stu-id="0603b-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="0603b-116">Norėdami pasiekti projekto lygio turto bibliotekas iš ER saugyklos, naudojamos importuoti ER konfigūracijas, prisijunkite prie „Finance” naudodami vartotojo, priklausančio nuomotojui (domenui), kuriam sukonfigūruotas dabartinis „Finance” egzempliorius, kredencialus.</span><span class="sxs-lookup"><span data-stu-id="0603b-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="0603b-117">Duomenų modelio konfigūracijos bendrai naudojamos versijos naikinimas</span><span class="sxs-lookup"><span data-stu-id="0603b-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="0603b-118">Puslapio **Konfigūracijos** konfigūracijų medyje pasirinkite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="0603b-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="0603b-119">Sukūrėte pirmąją modelio konfigūracijos pavyzdžio versiją ir publikavote ją LCS atlikę [Konfigūracijos įkėlimas į „Lifecycle Services“](er-upload-configuration-into-lifecycle-services.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0603b-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0603b-120">Atlikdami šią procedūrą, šią ER konfigūracijos versiją panaikinsite.</span><span class="sxs-lookup"><span data-stu-id="0603b-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="0603b-121">Tada versiją importuosite iš LCS, kaip aprašyta toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="0603b-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="0603b-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0603b-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0603b-123">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="0603b-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="0603b-124">Ši būsena nurodo, kad konfigūracija publikuota LCS portale.</span><span class="sxs-lookup"><span data-stu-id="0603b-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="0603b-125">Pasirinkti **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="0603b-125">Select **Change status**.</span></span>
4. <span data-ttu-id="0603b-126">Pasirinkite **Nebenaudoti**.</span><span class="sxs-lookup"><span data-stu-id="0603b-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="0603b-127">Kad galėtumėte versiją panaikinti, jos būseną pakeiskite iš **Bendrinama** į **Nebenaudojama**.</span><span class="sxs-lookup"><span data-stu-id="0603b-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="0603b-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0603b-128">Select **OK**.</span></span>
6. <span data-ttu-id="0603b-129">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0603b-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0603b-130">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Nebenaudojama**.</span><span class="sxs-lookup"><span data-stu-id="0603b-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="0603b-131">Pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="0603b-131">Select **Delete**.</span></span>
8. <span data-ttu-id="0603b-132">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0603b-132">Select **Yes**.</span></span>

    <span data-ttu-id="0603b-133">Atkreipkite dėmesį, kad dabar galima naudoti tik 2 pasirinktos duomenų modelio konfigūracijos juodraščio versiją.</span><span class="sxs-lookup"><span data-stu-id="0603b-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="0603b-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0603b-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="0603b-135">Duomenų modelio konfigūracijos bendrai naudojamos versijos importavimas iš LCS</span><span class="sxs-lookup"><span data-stu-id="0603b-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="0603b-136">Eikite į **Organizacijos administravimas \> Darbo sritys \> Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="0603b-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="0603b-137">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Litware, Inc.”**.</span><span class="sxs-lookup"><span data-stu-id="0603b-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="0603b-138">Plytelėje **„Litware, Inc.”** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="0603b-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="0603b-139">Dabar galite atidaryti „Litware, Inc‟ konfigūracijos teikėjo saugyklų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="0603b-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="0603b-140">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="0603b-140">Select **Open**.</span></span>

    <span data-ttu-id="0603b-141">Šiame pavyzdyje pasirinkite **LCS** saugyklą ir atidarykite.</span><span class="sxs-lookup"><span data-stu-id="0603b-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="0603b-142">Turite turėti [prieigą](#accessconditions) prie LCS projekto ir turto bibliotekos, kuri pasiekiama naudojant pasirinktą ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="0603b-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="0603b-143">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0603b-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="0603b-144">Šiame pavyzdyje versijų sąraše pasirinkite pirmąją **Modelio konfigūracijos pavyzdys** versiją.</span><span class="sxs-lookup"><span data-stu-id="0603b-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="0603b-145">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="0603b-145">Select **Import**.</span></span>
7. <span data-ttu-id="0603b-146">Pasirinkite **Taip**, norėdami patvirtinti pasirinktos versijos importavimą iš LCS.</span><span class="sxs-lookup"><span data-stu-id="0603b-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="0603b-147">Informacinis pranešimas patvirtina, kad pasirinkta versija buvo sėkmingai importuota.</span><span class="sxs-lookup"><span data-stu-id="0603b-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="0603b-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0603b-148">Close the page.</span></span>
9. <span data-ttu-id="0603b-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0603b-149">Close the page.</span></span>
10. <span data-ttu-id="0603b-150">Pasirinkite **Konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="0603b-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="0603b-151">Medyje pasirinkite **Modelio konfigūracijos pavyzdys**.</span><span class="sxs-lookup"><span data-stu-id="0603b-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="0603b-152">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0603b-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0603b-153">Šiame pavyzdyje pasirinkite konfigūracijos versiją, kurios būsena – **Bendrinama**.</span><span class="sxs-lookup"><span data-stu-id="0603b-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="0603b-154">Atkreipkite dėmesį, kad dabar taip pat galima naudoti ir 1 pasirinktos duomenų modelio konfigūracijos bendrai naudojamą versiją.</span><span class="sxs-lookup"><span data-stu-id="0603b-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]