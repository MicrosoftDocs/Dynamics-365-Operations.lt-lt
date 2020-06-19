---
title: ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš konfigūravimo tarnybos bendrosios saugyklos.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421707"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="68c09-103">ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="68c09-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68c09-104">Šioje temoje paaiškinama, kaip atsisiųsti [elektroninių ataskaitų (ER) konfigūracijas](general-electronic-reporting.md#Configuration) iš konfigūravimo tarnybos bendrosios saugyklos.</span><span class="sxs-lookup"><span data-stu-id="68c09-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="68c09-105">Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365 for Finance and Operations“ – „Regulatory Services“, konfigūravimo tarnybą](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="68c09-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="68c09-106">Atidarykite konfigūracijų saugyklą</span><span class="sxs-lookup"><span data-stu-id="68c09-106">Open configurations repository</span></span>

1. <span data-ttu-id="68c09-107">Prisijunkite prie „Dynamics 365 Finance“ programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="68c09-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="68c09-108">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="68c09-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="68c09-109">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="68c09-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="68c09-110">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="68c09-110">System administrator</span></span>

2. <span data-ttu-id="68c09-111">Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="68c09-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="68c09-112">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="68c09-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="68c09-113">Plytelėje **Microsoft** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="68c09-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![Elektroninių ataskaitų darbo sritis](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="68c09-115">Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą saugyklą, kurios tipas **Bendroji**.</span><span class="sxs-lookup"><span data-stu-id="68c09-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="68c09-116">Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="68c09-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="68c09-117">Pasirinkite **Įtraukti**, kad įtrauktumėte naują saugyklą.</span><span class="sxs-lookup"><span data-stu-id="68c09-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="68c09-118">Pasirinkite saugyklos tipą **Bendroji** ir pasirinkite **Kurti saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="68c09-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="68c09-119">Paraginti vykdykite autorizavimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="68c09-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="68c09-120">Įveskite saugyklos pavadinimą bei aprašą ir pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="68c09-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="68c09-121">Tinklelyje pasirinkite naują tipo **Bendroji** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="68c09-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="68c09-122">Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="68c09-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![Konfigūracijų saugyklų puslapis](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="68c09-124">Vienos konfigūracijos importavimas</span><span class="sxs-lookup"><span data-stu-id="68c09-124">Import a single configuration</span></span>

1. <span data-ttu-id="68c09-125">Puslapyje **Konfigūracijų saugyklos**, esančiame konfigūracijos medyje, pasirinkite norimą ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="68c09-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="68c09-126">„FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="68c09-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="68c09-127">Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš bendrosios saugyklos į dabartinį „Finance“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="68c09-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68c09-128">Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame „Finance“ egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="68c09-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![Konfigūracijos saugyklos puslapis](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="68c09-130">Filtruotų konfigūracijų importavimas</span><span class="sxs-lookup"><span data-stu-id="68c09-130">Import filtered configurations</span></span>

1. <span data-ttu-id="68c09-131">Puslapyje **Konfigūracijų saugykla**, esančiame konfigūracijos medyje, išplėskite „FastTab“ **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="68c09-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="68c09-132">Tinklelyje **Žymos** pridėkite visas reikiamas žymas.</span><span class="sxs-lookup"><span data-stu-id="68c09-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="68c09-133">Lauke **Šalies / regiono taikomumas** pasirinkite reikiamus šalies / regiono kodus ir pasirinkite **Taikyti filtrą**.</span><span class="sxs-lookup"><span data-stu-id="68c09-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68c09-134">„FastTab“ **Konfigūracijos** rodomos visos konfigūracijos, kurios atitinka nurodytas pasirinkimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="68c09-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="68c09-135">„FastTab“ **Konfigūracijos** pasirinkite **Importuoti**, kad atsisiųstumėte filtruotas konfigūracijas iš bendrosios saugyklos į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="68c09-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="68c09-136">„FastTab“ **Konfigūracijos** pasirinkite **Iš naujo nustatyti filtrą**, kad būtų išvalytos nurodytos pasirinkimo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="68c09-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![Konfigūracijos saugyklos puslapis](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="68c09-138">Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo.</span><span class="sxs-lookup"><span data-stu-id="68c09-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="68c09-139">Galite būti informuoti apie rastas nenuoseklumo problemas.</span><span class="sxs-lookup"><span data-stu-id="68c09-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="68c09-140">Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti problemas.</span><span class="sxs-lookup"><span data-stu-id="68c09-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="68c09-141">Daugiau informacijos ieškokite su šia tema susijusių išteklių sąraše.</span><span class="sxs-lookup"><span data-stu-id="68c09-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="68c09-142">ER konfigūracijos gali būti sukonfigūruotos kaip priklausomos nuo kitų konfigūracijų.</span><span class="sxs-lookup"><span data-stu-id="68c09-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="68c09-143">Todėl kartu su pasirinkta konfigūracija gali būti importuotos ir kitos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="68c09-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="68c09-144">Norėdami gauti daugiau informacijos apie konfigūracijos priklausomybes, žr. [ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span><span class="sxs-lookup"><span data-stu-id="68c09-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68c09-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="68c09-145">Additional resources</span></span>

[<span data-ttu-id="68c09-146">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="68c09-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
