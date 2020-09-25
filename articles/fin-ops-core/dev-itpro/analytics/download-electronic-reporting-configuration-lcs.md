---
title: Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810624"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="806f1-103">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="806f1-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="806f1-104">Šioje temoje paaiškinama, kaip atsisiųsti naujausią [elektroninių ataskaitų (ER) konfigūracijų](general-electronic-reporting.md#Configuration) versiją iš [bendrai naudojamo turto bibliotekos](../lifecycle-services/asset-library.md), esančios „Microsoft Dynamics Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="806f1-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="806f1-105">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="806f1-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="806f1-106">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="806f1-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="806f1-107">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="806f1-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="806f1-108">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="806f1-108">System administrator</span></span>

2. <span data-ttu-id="806f1-109">Eikite į **Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="806f1-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="806f1-110">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="806f1-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="806f1-111">Plytelėje **Microsoft** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="806f1-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="806f1-112">[![Plytelė „Microsoft” puslapyje Lokalizavimo konfigūracijos](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="806f1-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="806f1-113">Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="806f1-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="806f1-114">Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="806f1-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="806f1-115">Pasirinkite **Įtraukti**, kad įtrauktumėte saugyklą.</span><span class="sxs-lookup"><span data-stu-id="806f1-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="806f1-116">Pasirinkite **LCS** kaip saugyklos tipą.</span><span class="sxs-lookup"><span data-stu-id="806f1-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="806f1-117">Pasirinkite **Kurti saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="806f1-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="806f1-118">Jei esate raginami pateikti autorizaciją, vykdykite ekrane pateikiamus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="806f1-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="806f1-119">Įveskite saugyklos pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="806f1-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="806f1-120">Pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="806f1-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="806f1-121">Tinklelyje pasirinkite naują tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="806f1-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="806f1-122">Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="806f1-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="806f1-123">[![Konfigūracijų saugyklų puslapis](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="806f1-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="806f1-124">Jei kyla problemų prisijungiant prie LCS saugyklos norint atsisiųsti konfigūracijas iš LCS bendrai naudojamo turto bibliotekos, galite atsisiųsti konfigūracijas iš [bendrosios saugyklos](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="806f1-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="806f1-125">Kairiojoje srityje esančiame konfigūracijų medyje pasirinkite reikiamą ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="806f1-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="806f1-126">„FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="806f1-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="806f1-127">Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš LCS į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="806f1-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="806f1-128">Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="806f1-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="806f1-129">[![Konfigūracijos saugyklos puslapis](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="806f1-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="806f1-130">Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo.</span><span class="sxs-lookup"><span data-stu-id="806f1-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="806f1-131">Galite būti informuoti apie rastas nenuoseklumo problemas.</span><span class="sxs-lookup"><span data-stu-id="806f1-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="806f1-132">Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti šias problemas.</span><span class="sxs-lookup"><span data-stu-id="806f1-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="806f1-133">Daugiau informacijos ieškokite šios temos susijusių temų sąraše.</span><span class="sxs-lookup"><span data-stu-id="806f1-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="806f1-134">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="806f1-134">Additional resources</span></span>

[<span data-ttu-id="806f1-135">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="806f1-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="806f1-136">ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="806f1-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
