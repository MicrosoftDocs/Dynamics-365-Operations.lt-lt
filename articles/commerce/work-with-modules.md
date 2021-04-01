---
title: Darbas su moduliais
description: Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210904"
---
# <a name="work-with-modules"></a><span data-ttu-id="a76ca-103">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="a76ca-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a76ca-104">Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="a76ca-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a76ca-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="a76ca-105">Overview</span></span>

<span data-ttu-id="a76ca-106">Moduliai yra loginiai kūrimo blokai, kurie sudaro puslapio struktūrą, o jų paskirtis ir taikymo sritys yra įvairios.</span><span class="sxs-lookup"><span data-stu-id="a76ca-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="a76ca-107">Kai kurie moduliai yra aukšto lygio konteineriai, o jų vienintelė paskirtis – laikyti ir organizuoti kitus modulius (antrinius modulius).</span><span class="sxs-lookup"><span data-stu-id="a76ca-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="a76ca-108">Kitų modulių, pvz., paprasto vaizdų išdėstymo modulio, paskirtis yra labai konkreti.</span><span class="sxs-lookup"><span data-stu-id="a76ca-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="a76ca-109">Kiti moduliai, pvz., karuselės modulis, patenka tarp šių dviejų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="a76ca-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="a76ca-110">Pagal numatytuosius nustatymus jūsų „Dynamics 365 Commerce“ svetainėje yra modulių biblioteka, kuri leidžia įgyvendinti pagrindinius el. prekybos scenarijus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="a76ca-111">Tiesiog naudodami šiuos modulius greičiausiai galėsite sukurti visapusišką el. prekybos svetainę.</span><span class="sxs-lookup"><span data-stu-id="a76ca-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="a76ca-112">Tačiau galbūt norėsite šiuos modulius tinkinti arba kurti naujus pasirinktinius modulius konkretiems poreikiams.</span><span class="sxs-lookup"><span data-stu-id="a76ca-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="a76ca-113">Jei norite kurti pasirinktinius modulius, galite naudoti modulių kūrimo programinės įrangos kūrimo rinkinį (SDK), kuris padės sukurti pasirinktinių modulių biblioteką.</span><span class="sxs-lookup"><span data-stu-id="a76ca-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="a76ca-114">Konteinerio moduliai ir vietos</span><span class="sxs-lookup"><span data-stu-id="a76ca-114">Container modules and slots</span></span>

<span data-ttu-id="a76ca-115">Kaip minėta anksčiau, kai kurie moduliai yra skirti laikyti antrinius modulius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="a76ca-116">Šie moduliai vadinami *konteineriais* ir leidžia naudoti įdėtųjų modulių hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="a76ca-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="a76ca-117">Konteinerio moduliai apima *vietas*.</span><span class="sxs-lookup"><span data-stu-id="a76ca-117">Container modules include *slots*.</span></span> <span data-ttu-id="a76ca-118">Vietos naudojamos antrinių modulių maketui ir paskirčiai konteineryje tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="a76ca-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="a76ca-119">Pavyzdys – pagrindinis puslapio konteinerio modulis (bet kurio puslapio aukščiausio lygio modulis), kuriame nustatytos kelios svarbios vietos.</span><span class="sxs-lookup"><span data-stu-id="a76ca-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="a76ca-120">Antraštės vieta</span><span class="sxs-lookup"><span data-stu-id="a76ca-120">A header slot</span></span>
- <span data-ttu-id="a76ca-121">Papildomos antraštės vieta</span><span class="sxs-lookup"><span data-stu-id="a76ca-121">A sub-header slot</span></span>
- <span data-ttu-id="a76ca-122">Pagrindinė vieta</span><span class="sxs-lookup"><span data-stu-id="a76ca-122">A main slot</span></span>
- <span data-ttu-id="a76ca-123">Poraštės vieta</span><span class="sxs-lookup"><span data-stu-id="a76ca-123">A footer slot</span></span>
- <span data-ttu-id="a76ca-124">Papildomos poraštės vieta</span><span class="sxs-lookup"><span data-stu-id="a76ca-124">A sub-footer slot</span></span>

<span data-ttu-id="a76ca-125">Modulio kūrėjas apibrėžia šias vietas ir nustato, kuriuos antrinius modulius ir kiek antrinių modulių galima tiesiogiai įdėti jų viduje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="a76ca-126">Pavyzdžiui, antraštės vieta gali palaikyti tik vieną tipo **Antraštės modulis** modulį, o pagrindinės dalies vieta gali palaikyti neribotą skaičių bet kokio tipo modulių (išskyrus kitus puslapio konteinerio modulius).</span><span class="sxs-lookup"><span data-stu-id="a76ca-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="a76ca-127">Naudodami kūrimo įrankius puslapių autoriai neprivalo iš anksto žinoti, kuriuos modulius galima įdėti į kiekvieną vietą arba kurių modulių įdėti negalima.</span><span class="sxs-lookup"><span data-stu-id="a76ca-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="a76ca-128">Kai puslapių autoriai pasirenka vietą ir bando pasirinkti modulį, kurį nori į šią vietą įtraukti, jie matys modulio tipų, kurie toje vietoje palaikomi, filtruotą rodinį.</span><span class="sxs-lookup"><span data-stu-id="a76ca-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="a76ca-129">Turinio moduliai</span><span class="sxs-lookup"><span data-stu-id="a76ca-129">Content modules</span></span>

<span data-ttu-id="a76ca-130">Turinio moduliuose yra turinio ir medijos elementų, pvz., teksto (pvz., antraščių, pastraipų ir saitų) arba turto nuorodų (pavyzdžiui, vaizdų, vaizdo įrašų ir PDF failų).</span><span class="sxs-lookup"><span data-stu-id="a76ca-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="a76ca-131">Įprasto turinio modulio tipai apima turinio bloką, teksto bloką ir skatinančios reklamjuostės modulius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="a76ca-132">Šių trijų tipų moduliuose gali būti teksto arba medijos, ir jiems nereikia jokių antrinių modulių, kad kokią nors informaciją būtų galima padaryti matoma puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="a76ca-133">Dauguma įprastų, kasdienių puslapių ir turinio kūrimo užduočių apima turinio modulius, visų pirma todėl, kad šie moduliai apibrėžia faktinį turinį, kuris generuojamas jų pirminio konteinerio moduliuose.</span><span class="sxs-lookup"><span data-stu-id="a76ca-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="a76ca-134">Yra daug turinio modulių ir jie paprastai yra paskutinės dalys, kurias įtrauksite į puslapio įdėtųjų modulių hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="a76ca-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="a76ca-135">Toliau pateiktoje iliustracijoje parodyta, kaip moduliai yra įdėti į pirminio konteinerio modulio vietas.</span><span class="sxs-lookup"><span data-stu-id="a76ca-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Modulių įdėjimas](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="a76ca-137">Modulių įtraukimas arba pašalinimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-137">Add or remove modules</span></span>

<span data-ttu-id="a76ca-138">Tolesnėse procedūrose aprašoma, kaip įtraukti modulių arba juos pašalinti</span><span class="sxs-lookup"><span data-stu-id="a76ca-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="a76ca-139">Modulio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-139">Add a module</span></span>

<span data-ttu-id="a76ca-140">Norėdami modulį įtraukti į vietą arba konteinerį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-141">Išorinėje juostoje kairėje arba tiesiai pagrindinėje drobėje pasirinkite talpyklą ar vietą, į kurią galima įtraukti vaiko modulį.</span><span class="sxs-lookup"><span data-stu-id="a76ca-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a76ca-142">Modulių dizaino įrankyje nustatytas modulių, kuriuos galima įtraukti į konkrečią modulio vietą, tipų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="a76ca-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="a76ca-143">Šablono autoriai tuomet gali išdirbti leidžiamas modulio parinktis tam, kad padėtų užtikrinti nuoseklų ieškos variklio optimizavimą (SEO) ir leidžiamą efektyvumą puslapiams, kurie yra sukurti pagal specialų šabloną.</span><span class="sxs-lookup"><span data-stu-id="a76ca-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="a76ca-144">Įtraukdami modulį į vietą,**Modulio įtraukimas** teksto laukelis automatiškai filtruojamas taip, kad rodytų tik pasirinktoje talpykloje ar vietoje palaikomus modulius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="a76ca-145">Šis leidžiamų modulių sąrašas yra sudaromas puslapio šablone arba talpyklos modulio apraše.</span><span class="sxs-lookup"><span data-stu-id="a76ca-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="a76ca-146">Jei naudojate išorės juostą, pasirinkite elipsę (**...**) šalia modulio pavadinimo ir tuomet pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="a76ca-147">Jei naudojate valdiklius tiesiogiai drobėje, pasirinkite pliuso simbolį (**+**) tuščioje vietoje ar adjacente prie šiuo metu pasirinkto modulio ir tuomet pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a76ca-148">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti modulį** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="a76ca-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="a76ca-149">**Įtraukti modulį** teksto laukelyje pasirinkite modulį įtraukimui į jūsų puslapį.</span><span class="sxs-lookup"><span data-stu-id="a76ca-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="a76ca-150">**Turinio blokavimas** yra geras modulio tipas pradedantiems su juo dirbti.</span><span class="sxs-lookup"><span data-stu-id="a76ca-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="a76ca-151">Pasirinkite **Gerai**, kad pasirinktą modulį įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="a76ca-152">Modulio šalinimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-152">Remove a module</span></span>

<span data-ttu-id="a76ca-153">Norėdami modulį pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-154">Išorinėje jusotoje lairėje, pasirinkite elipsę (**...**) šalia šalinamo modulio pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį.</span><span class="sxs-lookup"><span data-stu-id="a76ca-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="a76ca-155">Kitu atveju, pagrindinėje drobėje galite pasirinkti fragmentą šiukšlių dėžės simbolį pasirinkto modulio įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="a76ca-156">Kai esate paskatinti patvirtinti, ar norite pašalinti modulį, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="a76ca-157">Perkelkite modulį į naują padėtį</span><span class="sxs-lookup"><span data-stu-id="a76ca-157">Move a module to a new position</span></span>

<span data-ttu-id="a76ca-158">Modulio perkėlimui į naują padėtį puslapyje, naudokite bet kurį iš tolesnių metodų.</span><span class="sxs-lookup"><span data-stu-id="a76ca-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="a76ca-159">Perkelkite modulį naudodami išorės juostą</span><span class="sxs-lookup"><span data-stu-id="a76ca-159">Move a module using the outline pane</span></span>

<span data-ttu-id="a76ca-160">Modulio perkėlimui naudojant išorės juostą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-161">Pasirinkite ir laikykite norimą perkelti modulį išorės juostoje, tada tempkite modulį į naują padėtį išorėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="a76ca-162">Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas.</span><span class="sxs-lookup"><span data-stu-id="a76ca-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="a76ca-163">Atleiskite modulį jo numetimui į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="a76ca-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="a76ca-164">Kelkite modulį tiesiai drobėje</span><span class="sxs-lookup"><span data-stu-id="a76ca-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="a76ca-165">Modulio perkėlimui tiesiai drobėje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-166">Pasirinkite modulį, kurį norite kelti drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="a76ca-167">Pasirinkite vieną iš į viršų ar apačią rodančių rodyklių simbolių modulio įrankių juostoje ir tuomet tempkite rodyklę į naują padėtį puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="a76ca-168">Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas.</span><span class="sxs-lookup"><span data-stu-id="a76ca-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="a76ca-169">Jei modulis negali būti judinamas aukštyn ar žemyn, rodyklės simbolis bus papilkėjęs.</span><span class="sxs-lookup"><span data-stu-id="a76ca-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="a76ca-170">Atleiskite modulį jo numetimui į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="a76ca-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="a76ca-171">Perkelkite modulį naudodami elipsės meniu</span><span class="sxs-lookup"><span data-stu-id="a76ca-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="a76ca-172">Modulio perkėlimui naudojant elipsės meniu, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-173">Pasirinkite modulį išorėje ar drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="a76ca-174">Pasirinkite elipsę (**...**) šalia modulio pavadinimo išorės juostoje arba modulio įrankių juostoje drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="a76ca-175">Jei modulis gali būti judinamas aukštyn ar žemyne konteineryje ar vietoje, matysime parinktis **Judinti aukštyn** ar **Judinti žemyn**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="a76ca-176">Pasirinkite norimą judesio parinktį modulio judinimui aukštyn ar žemyn pagal jo gimines.</span><span class="sxs-lookup"><span data-stu-id="a76ca-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="a76ca-177">Modulių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-177">Configure modules</span></span>

<span data-ttu-id="a76ca-178">Tolesnėse procedūrose aprašoma, kaip konfigūruoti turinio ir konteinerio modulius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="a76ca-179">Turinio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-179">Configure a content module</span></span>

<span data-ttu-id="a76ca-180">Norėdami konfigūruoti turinio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-181">Išorės juostoje kairėje, išplėskite medį ir pasirinkite bet kurį turinio modulį (pavyzdžiui, **Turinio blokavimą**).</span><span class="sxs-lookup"><span data-stu-id="a76ca-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="a76ca-182">Kitu atveju, galite pasirinkti modulį pagrindinėje drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="a76ca-183">Modulio parametrų juostoje dešinėje, įveskite parametrus bet kuriems norimo modulio valdikliams.</span><span class="sxs-lookup"><span data-stu-id="a76ca-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="a76ca-184">Komandų juostoje, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="a76ca-185">Tai padarius, taip pat bus atnaujinta peržiūros drobė.</span><span class="sxs-lookup"><span data-stu-id="a76ca-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="a76ca-186">Redaguokite modulio teksto parametrus</span><span class="sxs-lookup"><span data-stu-id="a76ca-186">Edit module text properties</span></span>

<span data-ttu-id="a76ca-187">Tik skaitymui neskirti modulio teksto parametrai gali būti tiesiai redaguojami drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="a76ca-188">Modulio teksto parametrų redagavimui, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-189">Pasirinkite teksto valdiklį drobėje, tuomet padėkite savo rodyklę ten, kur norite redaguoti tekstą.</span><span class="sxs-lookup"><span data-stu-id="a76ca-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="a76ca-190">Įveskite teksto turinį.</span><span class="sxs-lookup"><span data-stu-id="a76ca-190">Enter your text content.</span></span>
1. <span data-ttu-id="a76ca-191">Pasirinkite bet kur už teksto turinio ribų tam, kad tęstumėte kito turinio redagavimą.</span><span class="sxs-lookup"><span data-stu-id="a76ca-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="a76ca-192">Eilutės paveikslėlio pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-192">Inline image selection</span></span>

<span data-ttu-id="a76ca-193">Tik skaitymui neskirti modulio paveikslėliai parametrai gali būti tiesiai keičiami drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="a76ca-194">Tam, kad pasirinktumėte naują modulio turinio paveikslėlį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="a76ca-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-195">Dukart spustelėję drobėje ant paveikslėlio.</span><span class="sxs-lookup"><span data-stu-id="a76ca-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="a76ca-196">Tai atidarys medijos pasirinkimo langą.</span><span class="sxs-lookup"><span data-stu-id="a76ca-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="a76ca-197">Suraskite ir pasirinkite naują jūsų norimą naudoti paveikslėlį ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="a76ca-198">Naujas paveikslėlis dabar bus rodomas drobėje.</span><span class="sxs-lookup"><span data-stu-id="a76ca-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="a76ca-199">Konteinerio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a76ca-199">Configure a container module</span></span>

<span data-ttu-id="a76ca-200">Norėdami konfigūruoti konteinerio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="a76ca-201">Savo puslapyje pasirinkite konteinerio modulį (pavyzdžiui, karuselės arba nepastovaus konteinerio modulį).</span><span class="sxs-lookup"><span data-stu-id="a76ca-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="a76ca-202">Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.</span><span class="sxs-lookup"><span data-stu-id="a76ca-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="a76ca-203">Struktūros srityje kairėje šalia konteinerio arba bet kokių konteineryje esančių vietų pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="a76ca-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="a76ca-204">Tada į pasirinktą konteinerį įtraukite antrinių modulių.</span><span class="sxs-lookup"><span data-stu-id="a76ca-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="a76ca-205">Daugiau informacijos žr. ankstesniame šios temos skyriuje [Darbas su moduliais](#add-a-module).</span><span class="sxs-lookup"><span data-stu-id="a76ca-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="a76ca-206">Jei pirminiame konteineryje yra keli tos pačios kilmės antriniai moduliai, galite pakeisti jų rodymo pirminiame konteineryje tvarką.</span><span class="sxs-lookup"><span data-stu-id="a76ca-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="a76ca-207">Pasirinkite modulio daugtaškio mygtuką, tada naudokite rodyklės aukštyn arba rodyklės žemyn mygtukus.</span><span class="sxs-lookup"><span data-stu-id="a76ca-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a76ca-208">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a76ca-208">Additional resources</span></span>

[<span data-ttu-id="a76ca-209">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a76ca-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="a76ca-210">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="a76ca-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="a76ca-211">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="a76ca-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="a76ca-212">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="a76ca-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="a76ca-213">Konteinerio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="a76ca-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="a76ca-214">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="a76ca-214">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]