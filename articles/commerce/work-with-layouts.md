---
title: Darbas su esamais maketais
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793926"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="d81bf-103">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="d81bf-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d81bf-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.</span><span class="sxs-lookup"><span data-stu-id="d81bf-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d81bf-105">Prieš atlikdami šioje temoje aprašytas procedūras, būtinai perskaitykite temą [Iš anksto nustatyti ir pasirinktiniai maketai](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="d81bf-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="d81bf-106">Bendra apžvalga pateikiama temoje [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d81bf-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="d81bf-107">Naujo iš anksto nustatyto maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="d81bf-107">Create a new preset layout</span></span>

<span data-ttu-id="d81bf-108">Iš anksto nustatytą maketą galima kurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="d81bf-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="d81bf-109">Esamą pasirinktinį maketą galite įrašyti kaip naują iš anksto nustatytą maketą arba iš anksto nustatytą maketą galite kurti nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="d81bf-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="d81bf-110">Iš anksto nustatyto maketo kūrimas naudojant esamą pasirinktinį maketą</span><span class="sxs-lookup"><span data-stu-id="d81bf-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="d81bf-111">Norėdami iš anksto nustatytą maketą kurti naudodami esamą pasirinktinį maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="d81bf-112">Atidarykite esamą puslapį, kuriame šiuo metu nenaudojamas iš anksto nustatytas maketas, ir kurio modulių struktūrą norite pakartotinai naudoti kituose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="d81bf-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="d81bf-113">Norėdami patikrinti puslapį, pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="d81bf-114">Pasirinkite **Įrašyti kaip naują maketą**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-114">Select **Save as new layout**.</span></span> <span data-ttu-id="d81bf-115">Rodomas dialogo langas **Įrašyti kaip naują maketą**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="d81bf-116">Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="d81bf-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="d81bf-117">Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs.</span><span class="sxs-lookup"><span data-stu-id="d81bf-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="d81bf-118">Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.</span><span class="sxs-lookup"><span data-stu-id="d81bf-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="d81bf-119">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-119">Select **OK**.</span></span>

<span data-ttu-id="d81bf-120">Iš anksto nustatytas maketas nuo šiol bus pasiekiamas kuriant naujus puslapius arba pasirenkant kitą puslapio toje pačioje šablono hierarchijoje maketą.</span><span class="sxs-lookup"><span data-stu-id="d81bf-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="d81bf-121">Norėdami greitai peržiūrėti, ar konkretus puslapis šiuo metu yra susietas su iš anksto nustatytu maketu, puslapių sąrašo rodinyje pasirinkite puslapį ir ypatybių srityje dešinėje patikrinkite maketo metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="d81bf-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="d81bf-122">Naujo iš anksto nustatyto maketo kūrimas</span><span class="sxs-lookup"><span data-stu-id="d81bf-122">Create a new preset layout</span></span>

<span data-ttu-id="d81bf-123">Norėdami iš anksto nustatytą maketą kurti nuo pradžių, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="d81bf-124">Kairėje naršymo srityje pasirinkite **Maketai**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="d81bf-125">Pasirinkite **Naujas maketas**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-125">Select **New Layout**.</span></span> <span data-ttu-id="d81bf-126">Rodomas dialogo langas **Naujas maketas**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="d81bf-127">Pasirinkite šabloną, kurį naudosite iš anksto nustatytam maketui.</span><span class="sxs-lookup"><span data-stu-id="d81bf-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="d81bf-128">Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="d81bf-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="d81bf-129">Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs.</span><span class="sxs-lookup"><span data-stu-id="d81bf-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="d81bf-130">Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.</span><span class="sxs-lookup"><span data-stu-id="d81bf-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="d81bf-131">Pasirinkite **Gerai**, kad sukurtumėte naują iš anksto nustatytą maketą ir atidarytumėte maketų rengyklę.</span><span class="sxs-lookup"><span data-stu-id="d81bf-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="d81bf-132">Maketų rengyklėje įtraukite modulių ir juos konfigūruokite naudodami struktūros medį kairėje pusėje ir ypatybių sritį dešinėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="d81bf-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="d81bf-133">(Šis procesas panašus į šablono modulių įtraukimo ir konfigūravimo naudojant šablonų rengyklę procesą.) Modulių išdėstymas ir bet kokie užrakinti numatytieji parametrai tampa bet kokių puslapių, kuriuose naudojamas šis iš anksto nustatytas maketas, centralizuota modulių konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="d81bf-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="d81bf-134">Iš anksto nustatyto maketo modifikavimas</span><span class="sxs-lookup"><span data-stu-id="d81bf-134">Modify a preset layout</span></span>

<span data-ttu-id="d81bf-135">Norėdami modifikuoti iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="d81bf-136">Kairėje naršymo srityje pasirinkite **Maketai**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="d81bf-137">Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite modulį, kurį norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="d81bf-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="d81bf-138">Tuomet atlikite bet kuriuos iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="d81bf-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="d81bf-139">Norėdami modulį perkelti aukštyn arba žemyn jo pirminiame modulyje, pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Perkelti aukštyn** arba **Perkelti žemyn**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="d81bf-140">Norėdami pakeisti modulio numatytuosius parametrus, naudokite ypatybių sritį, kad įvestumėte numatytąsias reikšmes ir pasirinktinai jas užfiksuotumėte visuose paskesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="d81bf-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="d81bf-141">Norėdami į konteinerio modulius įtraukti naujų modulių ar fragmentų, pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį** arba **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="d81bf-142">Norėdami iš maketo pašalinti modulį, pasirinkite daugtaškio mygtuką, tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="d81bf-143">Iš anksto nustatyto maketo temos keitimas</span><span class="sxs-lookup"><span data-stu-id="d81bf-143">Change a preset layout theme</span></span>

<span data-ttu-id="d81bf-144">Paprastai nustatoma visų puslapių, kuriuose naudojamas iš anksto nustatytas maketas, numatytoji tema.</span><span class="sxs-lookup"><span data-stu-id="d81bf-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="d81bf-145">Norėdami nustatyti arba pakeisti visų antrinių puslapių, kuriuose naudojamas iš anksto nustatytas maketas, temą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="d81bf-146">Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite puslapio konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="d81bf-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="d81bf-147">(Paprastai šis modulis yra antrasis mazgas, o jo pavadinimas yra **Numatytasis puslapis**.)</span><span class="sxs-lookup"><span data-stu-id="d81bf-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="d81bf-148">Dešinėje ypatybės srityje, lauke **Tema** pasirinkite temą.</span><span class="sxs-lookup"><span data-stu-id="d81bf-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="d81bf-149">Iš anksto nustatyto maketo įrašymas, įregistravimas, peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="d81bf-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="d81bf-150">Norėdami įrašyti ir įregistruoti savo iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d81bf-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="d81bf-151">Maketo rengyklės viršuje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="d81bf-152">Įrašyti keitimai neturės įtakos tolesniems puslapiams, kol jie nebus įrašomi ir atrakinami.</span><span class="sxs-lookup"><span data-stu-id="d81bf-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="d81bf-153">Pasirinkite **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-153">Select **Finish editing**.</span></span> <span data-ttu-id="d81bf-154">Dabar jūsų keitimai yra aptinkami atsiuntimo srauto darbo eigose.</span><span class="sxs-lookup"><span data-stu-id="d81bf-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="d81bf-155">Norėdami peržiūrėti keitimus atidarykite esamą puslapį, kuriame naudojamas iš anksto nustatytas maketas, arba naudodami maketą sukurkite naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="d81bf-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="d81bf-156">Kai peržiūrėsite iš anksto nustatyto maketo keitimus, atlikite vieną iš toliau nurodytų veiksmų, kad maketas būtų publikuojamas jūsų aktyvioje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="d81bf-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="d81bf-157">Eikite į **Maketai**, pasirinkite maketą, tada pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="d81bf-158">Norėdami atidaryti maketų rengyklę pasirinkite maketo pavadinimą, tada pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="d81bf-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="d81bf-159">Publikuokite puslapį, kuris nurodo nepaskelbtą maketą.</span><span class="sxs-lookup"><span data-stu-id="d81bf-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="d81bf-160">Maketas bus publikuotas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="d81bf-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="d81bf-161">Iš anksto nustatyti maketai gali būti nurodyti keliuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="d81bf-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="d81bf-162">Kai publikuosite iš anksto nustatytą maketą, atkreipkite dėmesį, kad tai gali turėti įtakos kelių puslapių maketui.</span><span class="sxs-lookup"><span data-stu-id="d81bf-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d81bf-163">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d81bf-163">Additional resources</span></span>

[<span data-ttu-id="d81bf-164">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d81bf-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d81bf-165">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="d81bf-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
