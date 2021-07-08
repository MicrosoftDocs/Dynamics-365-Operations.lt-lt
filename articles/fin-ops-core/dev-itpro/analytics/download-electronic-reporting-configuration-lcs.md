---
title: Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271188"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="b2c23-103">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="b2c23-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2c23-104">Šioje temoje paaiškinama, kaip atsisiųsti naujausią [elektroninių ataskaitų (ER) konfigūracijų](general-electronic-reporting.md#Configuration) versiją iš [bendrai naudojamo turto bibliotekos](../lifecycle-services/asset-library.md), esančios „Microsoft Dynamics Lifecycle Services” (LCS).</span><span class="sxs-lookup"><span data-stu-id="b2c23-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2c23-105">LCS naudojimas kaip ER konfigūracijų saugyklos yra [nerekomenduojamas](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="b2c23-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="b2c23-106">Daugiau informacijos rasite [„Regulatory Configuration Service“ (RCS) – „Lifecycle Services“ (LCS) saugykla nerekomenduojama](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="b2c23-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="b2c23-107">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="b2c23-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="b2c23-108">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="b2c23-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="b2c23-109">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="b2c23-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="b2c23-110">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="b2c23-110">System administrator</span></span>

2. <span data-ttu-id="b2c23-111">Eikite į **Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b2c23-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="b2c23-112">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b2c23-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="b2c23-113">Plytelėje **Microsoft** pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="b2c23-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="b2c23-114">[![Plytelė „Microsoft” puslapyje Lokalizavimo konfigūracijos](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="b2c23-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="b2c23-115">Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="b2c23-116">Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b2c23-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="b2c23-117">Pasirinkite **Įtraukti**, kad įtrauktumėte saugyklą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="b2c23-118">Pasirinkite **LCS** kaip saugyklos tipą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="b2c23-119">Pasirinkite **Kurti saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="b2c23-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="b2c23-120">Jei esate raginami pateikti autorizaciją, vykdykite ekrane pateikiamus nurodymus.</span><span class="sxs-lookup"><span data-stu-id="b2c23-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="b2c23-121">Įveskite saugyklos pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="b2c23-122">Pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="b2c23-123">Tinklelyje pasirinkite naują tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="b2c23-124">Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="b2c23-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="b2c23-125">[![Konfigūracijų saugyklų puslapis](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="b2c23-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="b2c23-126">Jei kyla problemų prisijungiant prie LCS saugyklos norint atsisiųsti konfigūracijas iš LCS bendrai naudojamo turto bibliotekos, galite atsisiųsti konfigūracijas iš [bendrosios saugyklos](er-download-configurations-global-repo.md).</span><span class="sxs-lookup"><span data-stu-id="b2c23-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="b2c23-127">Kairiojoje srityje esančiame konfigūracijų medyje pasirinkite reikiamą ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b2c23-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="b2c23-128">„FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="b2c23-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="b2c23-129">Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš LCS į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="b2c23-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2c23-130">Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="b2c23-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="b2c23-131">[![Konfigūracijos saugyklos puslapis](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="b2c23-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b2c23-132">Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo.</span><span class="sxs-lookup"><span data-stu-id="b2c23-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="b2c23-133">Galite būti informuoti apie rastas nenuoseklumo problemas.</span><span class="sxs-lookup"><span data-stu-id="b2c23-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="b2c23-134">Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti šias problemas.</span><span class="sxs-lookup"><span data-stu-id="b2c23-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="b2c23-135">Daugiau informacijos ieškokite šios temos susijusių temų sąraše.</span><span class="sxs-lookup"><span data-stu-id="b2c23-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2c23-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b2c23-136">Additional resources</span></span>

[<span data-ttu-id="b2c23-137">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="b2c23-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="b2c23-138">ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos</span><span class="sxs-lookup"><span data-stu-id="b2c23-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
