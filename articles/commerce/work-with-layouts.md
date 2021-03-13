---
title: Darbas su esamais maketais
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 57dc0de64ce7536cf70c1f277d5212c3b8dd7480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009598"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="e7e95-103">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="e7e95-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e7e95-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.</span><span class="sxs-lookup"><span data-stu-id="e7e95-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7e95-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="e7e95-105">Overview</span></span>

<span data-ttu-id="e7e95-106">Prieš atlikdami šioje temoje aprašytas procedūras, būtinai perskaitykite temą [Iš anksto nustatyti ir pasirinktiniai maketai](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="e7e95-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="e7e95-107">Bendra apžvalga pateikiama temoje [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7e95-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="e7e95-108">Naujo iš anksto nustatyto maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e95-108">Create a new preset layout</span></span>

<span data-ttu-id="e7e95-109">Iš anksto nustatytą maketą galima kurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="e7e95-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="e7e95-110">Esamą pasirinktinį maketą galite įrašyti kaip naują iš anksto nustatytą maketą arba iš anksto nustatytą maketą galite kurti nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="e7e95-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="e7e95-111">Iš anksto nustatyto maketo kūrimas naudojant esamą pasirinktinį maketą</span><span class="sxs-lookup"><span data-stu-id="e7e95-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="e7e95-112">Norėdami iš anksto nustatytą maketą kurti naudodami esamą pasirinktinį maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e95-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="e7e95-113">Atidarykite esamą puslapį, kuriame šiuo metu nenaudojamas iš anksto nustatytas maketas, ir kurio modulių struktūrą norite pakartotinai naudoti kituose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="e7e95-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="e7e95-114">Norėdami patikrinti puslapį, pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="e7e95-115">Pasirinkite **Įrašyti kaip naują maketą**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-115">Select **Save as new layout**.</span></span> <span data-ttu-id="e7e95-116">Rodomas dialogo langas **Įrašyti kaip naują maketą**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="e7e95-117">Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="e7e95-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="e7e95-118">Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs.</span><span class="sxs-lookup"><span data-stu-id="e7e95-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="e7e95-119">Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.</span><span class="sxs-lookup"><span data-stu-id="e7e95-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="e7e95-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-120">Select **OK**.</span></span>

<span data-ttu-id="e7e95-121">Iš anksto nustatytas maketas nuo šiol bus pasiekiamas kuriant naujus puslapius arba pasirenkant kitą puslapio toje pačioje šablono hierarchijoje maketą.</span><span class="sxs-lookup"><span data-stu-id="e7e95-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="e7e95-122">Norėdami greitai peržiūrėti, ar konkretus puslapis šiuo metu yra susietas su iš anksto nustatytu maketu, puslapių sąrašo rodinyje pasirinkite puslapį ir ypatybių srityje dešinėje patikrinkite maketo metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="e7e95-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="e7e95-123">Naujo iš anksto nustatyto maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e95-123">Create a new preset layout</span></span>

<span data-ttu-id="e7e95-124">Norėdami iš anksto nustatytą maketą kurti nuo pradžių, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e95-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="e7e95-125">Kairėje naršymo srityje pasirinkite **Maketai**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="e7e95-126">Pasirinkite **Naujas maketas**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-126">Select **New Layout**.</span></span> <span data-ttu-id="e7e95-127">Rodomas dialogo langas **Naujas maketas**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="e7e95-128">Pasirinkite šabloną, kurį naudosite iš anksto nustatytam maketui.</span><span class="sxs-lookup"><span data-stu-id="e7e95-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="e7e95-129">Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="e7e95-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="e7e95-130">Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs.</span><span class="sxs-lookup"><span data-stu-id="e7e95-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="e7e95-131">Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.</span><span class="sxs-lookup"><span data-stu-id="e7e95-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="e7e95-132">Pasirinkite **Gerai**, kad sukurtumėte naują iš anksto nustatytą maketą ir atidarytumėte maketų rengyklę.</span><span class="sxs-lookup"><span data-stu-id="e7e95-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="e7e95-133">Maketų rengyklėje įtraukite modulių ir juos konfigūruokite naudodami struktūros medį kairėje pusėje ir ypatybių sritį dešinėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="e7e95-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="e7e95-134">(Šis procesas panašus į šablono modulių įtraukimo ir konfigūravimo naudojant šablonų rengyklę procesą.) Modulių išdėstymas ir bet kokie užrakinti numatytieji parametrai tampa bet kokių puslapių, kuriuose naudojamas šis iš anksto nustatytas maketas, centralizuota modulių konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="e7e95-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="e7e95-135">Iš anksto nustatyto maketo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="e7e95-135">Modify a preset layout</span></span>

<span data-ttu-id="e7e95-136">Norėdami modifikuoti iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e95-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7e95-137">Kairėje naršymo srityje pasirinkite **Maketai**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="e7e95-138">Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite modulį, kurį norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="e7e95-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="e7e95-139">Tuomet atlikite bet kuriuos iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="e7e95-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="e7e95-140">Norėdami modulį perkelti aukštyn arba žemyn jo pirminiame modulyje, pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Perkelti aukštyn** arba **Perkelti žemyn**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="e7e95-141">Norėdami pakeisti modulio numatytuosius parametrus, naudokite ypatybių sritį, kad įvestumėte numatytąsias reikšmes ir pasirinktinai jas užfiksuotumėte visuose paskesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="e7e95-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="e7e95-142">Norėdami į konteinerio modulius įtraukti naujų modulių ar fragmentų, pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį** arba **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="e7e95-143">Norėdami iš maketo pašalinti modulį, pasirinkite daugtaškio mygtuką, tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="e7e95-144">Iš anksto nustatyto maketo temos keitimas</span><span class="sxs-lookup"><span data-stu-id="e7e95-144">Change a preset layout theme</span></span>

<span data-ttu-id="e7e95-145">Paprastai nustatoma visų puslapių, kuriuose naudojamas iš anksto nustatytas maketas, numatytoji tema.</span><span class="sxs-lookup"><span data-stu-id="e7e95-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="e7e95-146">Norėdami nustatyti arba pakeisti visų antrinių puslapių, kuriuose naudojamas iš anksto nustatytas maketas, temą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e95-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7e95-147">Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite puslapio konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="e7e95-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="e7e95-148">(Paprastai šis modulis yra antrasis mazgas, o jo pavadinimas yra **Numatytasis puslapis**.)</span><span class="sxs-lookup"><span data-stu-id="e7e95-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="e7e95-149">Dešinėje ypatybės srityje, lauke **Tema** pasirinkite temą.</span><span class="sxs-lookup"><span data-stu-id="e7e95-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="e7e95-150">Iš anksto nustatyto maketo įrašymas, įregistravimas, peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="e7e95-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="e7e95-151">Norėdami įrašyti ir įregistruoti savo iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e95-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="e7e95-152">Maketo rengyklės viršuje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="e7e95-153">Įrašyti keitimai neturės įtakos tolesniems puslapiams, kol jie nebus įrašomi ir atrakinami.</span><span class="sxs-lookup"><span data-stu-id="e7e95-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="e7e95-154">Pasirinkite **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-154">Select **Finish editing**.</span></span> <span data-ttu-id="e7e95-155">Dabar jūsų keitimai yra aptinkami atsiuntimo srauto darbo eigose.</span><span class="sxs-lookup"><span data-stu-id="e7e95-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="e7e95-156">Norėdami peržiūrėti keitimus atidarykite esamą puslapį, kuriame naudojamas iš anksto nustatytas maketas, arba naudodami maketą sukurkite naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="e7e95-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="e7e95-157">Kai peržiūrėsite iš anksto nustatyto maketo keitimus, atlikite vieną iš toliau nurodytų veiksmų, kad maketas būtų publikuojamas jūsų aktyvioje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="e7e95-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="e7e95-158">Eikite į **Maketai**, pasirinkite maketą, tada pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="e7e95-159">Norėdami atidaryti maketų rengyklę pasirinkite maketo pavadinimą, tada pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="e7e95-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="e7e95-160">Publikuokite puslapį, kuris nurodo nepaskelbtą maketą.</span><span class="sxs-lookup"><span data-stu-id="e7e95-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="e7e95-161">Maketas bus publikuotas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e7e95-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="e7e95-162">Iš anksto nustatyti maketai gali būti nurodyti keliuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="e7e95-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="e7e95-163">Kai publikuosite iš anksto nustatytą maketą, atkreipkite dėmesį, kad tai gali turėti įtakos kelių puslapių maketui.</span><span class="sxs-lookup"><span data-stu-id="e7e95-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7e95-164">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e7e95-164">Additional resources</span></span>

[<span data-ttu-id="e7e95-165">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="e7e95-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e7e95-166">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="e7e95-166">Work with templates</span></span>](work-with-templates.md)
