---
title: Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 4cc14860bd969048c4378b40d97a7940a8710e89
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934659"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="d9bbe-103">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="d9bbe-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9bbe-104">Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="d9bbe-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="d9bbe-105">Ši mokymo programa padės jums atsisiųsti naujausias elektroninio ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="d9bbe-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="d9bbe-106">Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="d9bbe-107">Elektroninės ataskaitos kūrėjas</span><span class="sxs-lookup"><span data-stu-id="d9bbe-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="d9bbe-108">Elektroninės ataskaitos funkcijų konsultantas</span><span class="sxs-lookup"><span data-stu-id="d9bbe-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d9bbe-109">Sistemos administratorius</span><span class="sxs-lookup"><span data-stu-id="d9bbe-109">System administrator</span></span>

2. <span data-ttu-id="d9bbe-110">Eikite į **Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-110">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="d9bbe-111">Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="d9bbe-112">Plytelėje **Microsoft** spustelėkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="d9bbe-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="d9bbe-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="d9bbe-114">Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="d9bbe-115">Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="d9bbe-116">Spustelėdami **Įtraukti** įtraukite naują saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="d9bbe-117">Pasirinkite **LCS** kaip saugyklos tipą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="d9bbe-118">Spustelėkite **Kurti saugyklą**.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="d9bbe-119">Paraginti vykdykite autorizavimo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="d9bbe-120">Įveskite saugyklos pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="d9bbe-121">Spustelėkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="d9bbe-122">Tinklelyje pasirinkite naują tipo **LCS** saugyklą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="d9bbe-123">Spustelėkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="d9bbe-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="d9bbe-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="d9bbe-125">Kairiojoje srityje esančiame konfigūracijų medyje pasirinkite reikiamą ER konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="d9bbe-126">„FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="d9bbe-127">Spustelėkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš LCS į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9bbe-128">Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame egzemplioriuje.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="d9bbe-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="d9bbe-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d9bbe-130">Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="d9bbe-131">Galite būti informuoti apie rastas nenuoseklumo problemas.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="d9bbe-132">Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti šias problemas.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="d9bbe-133">Daugiau informacijos ieškokite šios temos susijusių straipsnių sąraše.</span><span class="sxs-lookup"><span data-stu-id="d9bbe-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9bbe-134">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d9bbe-134">Additional resources</span></span>

[<span data-ttu-id="d9bbe-135">Elektroninių ataskaitų (ER) apžvalga</span><span class="sxs-lookup"><span data-stu-id="d9bbe-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
