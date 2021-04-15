---
title: Darbas su moduliais
description: Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801366"
---
# <a name="work-with-modules"></a><span data-ttu-id="9eac7-103">Darbas su moduliais</span><span class="sxs-lookup"><span data-stu-id="9eac7-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9eac7-104">Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9eac7-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9eac7-105">Moduliai yra loginiai kūrimo blokai, kurie sudaro puslapio struktūrą, o jų paskirtis ir taikymo sritys yra įvairios.</span><span class="sxs-lookup"><span data-stu-id="9eac7-105">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="9eac7-106">Kai kurie moduliai yra aukšto lygio konteineriai, o jų vienintelė paskirtis – laikyti ir organizuoti kitus modulius (antrinius modulius).</span><span class="sxs-lookup"><span data-stu-id="9eac7-106">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="9eac7-107">Kitų modulių, pvz., paprasto vaizdų išdėstymo modulio, paskirtis yra labai konkreti.</span><span class="sxs-lookup"><span data-stu-id="9eac7-107">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="9eac7-108">Kiti moduliai, pvz., karuselės modulis, patenka tarp šių dviejų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="9eac7-108">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="9eac7-109">Pagal numatytuosius nustatymus jūsų „Dynamics 365 Commerce“ svetainėje yra modulių biblioteka, kuri leidžia įgyvendinti pagrindinius el. prekybos scenarijus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-109">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="9eac7-110">Tiesiog naudodami šiuos modulius greičiausiai galėsite sukurti visapusišką el. prekybos svetainę.</span><span class="sxs-lookup"><span data-stu-id="9eac7-110">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="9eac7-111">Tačiau galbūt norėsite šiuos modulius tinkinti arba kurti naujus pasirinktinius modulius konkretiems poreikiams.</span><span class="sxs-lookup"><span data-stu-id="9eac7-111">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="9eac7-112">Jei norite kurti pasirinktinius modulius, galite naudoti modulių kūrimo programinės įrangos kūrimo rinkinį (SDK), kuris padės sukurti pasirinktinių modulių biblioteką.</span><span class="sxs-lookup"><span data-stu-id="9eac7-112">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="9eac7-113">Konteinerio moduliai ir vietos</span><span class="sxs-lookup"><span data-stu-id="9eac7-113">Container modules and slots</span></span>

<span data-ttu-id="9eac7-114">Kaip minėta anksčiau, kai kurie moduliai yra skirti laikyti antrinius modulius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-114">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="9eac7-115">Šie moduliai vadinami *konteineriais* ir leidžia naudoti įdėtųjų modulių hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="9eac7-115">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="9eac7-116">Konteinerio moduliai apima *vietas*.</span><span class="sxs-lookup"><span data-stu-id="9eac7-116">Container modules include *slots*.</span></span> <span data-ttu-id="9eac7-117">Vietos naudojamos antrinių modulių maketui ir paskirčiai konteineryje tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="9eac7-117">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="9eac7-118">Pavyzdys – pagrindinis puslapio konteinerio modulis (bet kurio puslapio aukščiausio lygio modulis), kuriame nustatytos kelios svarbios vietos.</span><span class="sxs-lookup"><span data-stu-id="9eac7-118">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="9eac7-119">Antraštės vieta</span><span class="sxs-lookup"><span data-stu-id="9eac7-119">A header slot</span></span>
- <span data-ttu-id="9eac7-120">Papildomos antraštės vieta</span><span class="sxs-lookup"><span data-stu-id="9eac7-120">A sub-header slot</span></span>
- <span data-ttu-id="9eac7-121">Pagrindinė vieta</span><span class="sxs-lookup"><span data-stu-id="9eac7-121">A main slot</span></span>
- <span data-ttu-id="9eac7-122">Poraštės vieta</span><span class="sxs-lookup"><span data-stu-id="9eac7-122">A footer slot</span></span>
- <span data-ttu-id="9eac7-123">Papildomos poraštės vieta</span><span class="sxs-lookup"><span data-stu-id="9eac7-123">A sub-footer slot</span></span>

<span data-ttu-id="9eac7-124">Modulio kūrėjas apibrėžia šias vietas ir nustato, kuriuos antrinius modulius ir kiek antrinių modulių galima tiesiogiai įdėti jų viduje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-124">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="9eac7-125">Pavyzdžiui, antraštės vieta gali palaikyti tik vieną tipo **Antraštės modulis** modulį, o pagrindinės dalies vieta gali palaikyti neribotą skaičių bet kokio tipo modulių (išskyrus kitus puslapio konteinerio modulius).</span><span class="sxs-lookup"><span data-stu-id="9eac7-125">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="9eac7-126">Naudodami kūrimo įrankius puslapių autoriai neprivalo iš anksto žinoti, kuriuos modulius galima įdėti į kiekvieną vietą arba kurių modulių įdėti negalima.</span><span class="sxs-lookup"><span data-stu-id="9eac7-126">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="9eac7-127">Kai puslapių autoriai pasirenka vietą ir bando pasirinkti modulį, kurį nori į šią vietą įtraukti, jie matys modulio tipų, kurie toje vietoje palaikomi, filtruotą rodinį.</span><span class="sxs-lookup"><span data-stu-id="9eac7-127">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="9eac7-128">Turinio moduliai</span><span class="sxs-lookup"><span data-stu-id="9eac7-128">Content modules</span></span>

<span data-ttu-id="9eac7-129">Turinio moduliuose yra turinio ir medijos elementų, pvz., teksto (pvz., antraščių, pastraipų ir saitų) arba turto nuorodų (pavyzdžiui, vaizdų, vaizdo įrašų ir PDF failų).</span><span class="sxs-lookup"><span data-stu-id="9eac7-129">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="9eac7-130">Įprasto turinio modulio tipai apima turinio bloką, teksto bloką ir skatinančios reklamjuostės modulius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-130">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="9eac7-131">Šių trijų tipų moduliuose gali būti teksto arba medijos, ir jiems nereikia jokių antrinių modulių, kad kokią nors informaciją būtų galima padaryti matoma puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-131">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="9eac7-132">Dauguma įprastų, kasdienių puslapių ir turinio kūrimo užduočių apima turinio modulius, visų pirma todėl, kad šie moduliai apibrėžia faktinį turinį, kuris generuojamas jų pirminio konteinerio moduliuose.</span><span class="sxs-lookup"><span data-stu-id="9eac7-132">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="9eac7-133">Yra daug turinio modulių ir jie paprastai yra paskutinės dalys, kurias įtrauksite į puslapio įdėtųjų modulių hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="9eac7-133">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="9eac7-134">Toliau pateiktoje iliustracijoje parodyta, kaip moduliai yra įdėti į pirminio konteinerio modulio vietas.</span><span class="sxs-lookup"><span data-stu-id="9eac7-134">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Modulių įdėjimas](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="9eac7-136">Modulių įtraukimas arba pašalinimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-136">Add or remove modules</span></span>

<span data-ttu-id="9eac7-137">Tolesnėse procedūrose aprašoma, kaip įtraukti modulių arba juos pašalinti.</span><span class="sxs-lookup"><span data-stu-id="9eac7-137">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="9eac7-138">Modulio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-138">Add a module</span></span>

<span data-ttu-id="9eac7-139">Norėdami modulį įtraukti į vietą arba konteinerį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-139">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-140">Išorinėje juostoje kairėje arba tiesiai pagrindinėje drobėje pasirinkite talpyklą ar vietą, į kurią galima įtraukti vaiko modulį.</span><span class="sxs-lookup"><span data-stu-id="9eac7-140">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9eac7-141">Modulių dizaino įrankyje nustatytas modulių, kuriuos galima įtraukti į konkrečią modulio vietą, tipų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9eac7-141">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="9eac7-142">Šablono autoriai tuomet gali išdirbti leidžiamas modulio parinktis tam, kad padėtų užtikrinti nuoseklų ieškos variklio optimizavimą (SEO) ir leidžiamą efektyvumą puslapiams, kurie yra sukurti pagal specialų šabloną.</span><span class="sxs-lookup"><span data-stu-id="9eac7-142">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="9eac7-143">Įtraukdami modulį į vietą,**Modulio įtraukimas** teksto laukelis automatiškai filtruojamas taip, kad rodytų tik pasirinktoje talpykloje ar vietoje palaikomus modulius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-143">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="9eac7-144">Šis leidžiamų modulių sąrašas yra sudaromas puslapio šablone arba talpyklos modulio apraše.</span><span class="sxs-lookup"><span data-stu-id="9eac7-144">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="9eac7-145">Jei naudojate išorės juostą, pasirinkite elipsę (**...**) šalia modulio pavadinimo ir tuomet pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-145">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="9eac7-146">Jei naudojate valdiklius tiesiogiai drobėje, pasirinkite pliuso simbolį (**+**) tuščioje vietoje ar šalia prie šiuo metu pasirinkto modulio ir tuomet pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-146">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9eac7-147">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti modulį** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="9eac7-147">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="9eac7-148">**Įtraukti modulį** teksto laukelyje pasirinkite modulį įtraukimui į jūsų puslapį.</span><span class="sxs-lookup"><span data-stu-id="9eac7-148">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="9eac7-149">**Turinio blokavimas** yra geras modulio tipas pradedantiems su juo dirbti.</span><span class="sxs-lookup"><span data-stu-id="9eac7-149">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="9eac7-150">Pasirinkite **Gerai**, kad pasirinktą modulį įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-150">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="9eac7-151">Modulio šalinimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-151">Remove a module</span></span>

<span data-ttu-id="9eac7-152">Norėdami modulį pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-152">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-153">Išorinėje kairinėje juostoje pasirinkite elipsę (**...**) šalia šalinamo modulio pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį.</span><span class="sxs-lookup"><span data-stu-id="9eac7-153">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="9eac7-154">Kitu atveju, pagrindinėje drobėje galite pasirinkti fragmentą šiukšlių dėžės simbolį pasirinkto modulio įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-154">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="9eac7-155">Kai esate paskatinti patvirtinti, ar norite pašalinti modulį, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-155">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="9eac7-156">Perkelkite modulį į naują padėtį</span><span class="sxs-lookup"><span data-stu-id="9eac7-156">Move a module to a new position</span></span>

<span data-ttu-id="9eac7-157">Modulio perkėlimui į naują padėtį puslapyje, naudokite bet kurį iš tolesnių metodų.</span><span class="sxs-lookup"><span data-stu-id="9eac7-157">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="9eac7-158">Perkelkite modulį naudodami išorės juostą</span><span class="sxs-lookup"><span data-stu-id="9eac7-158">Move a module using the outline pane</span></span>

<span data-ttu-id="9eac7-159">Modulio perkėlimui naudojant išorės juostą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-159">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-160">Pasirinkite ir laikykite norimą perkelti modulį išorės juostoje, tada tempkite modulį į naują padėtį išorėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-160">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="9eac7-161">Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas.</span><span class="sxs-lookup"><span data-stu-id="9eac7-161">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="9eac7-162">Atleiskite modulį jo numetimui į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="9eac7-162">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="9eac7-163">Kelkite modulį tiesiai drobėje</span><span class="sxs-lookup"><span data-stu-id="9eac7-163">Move a module directly within the canvas</span></span>

<span data-ttu-id="9eac7-164">Modulio perkėlimui tiesiai drobėje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-164">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-165">Pasirinkite modulį, kurį norite kelti drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-165">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="9eac7-166">Pasirinkite vieną iš į viršų ar apačią rodančių rodyklių simbolių modulio įrankių juostoje ir tuomet tempkite rodyklę į naują padėtį puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-166">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="9eac7-167">Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas.</span><span class="sxs-lookup"><span data-stu-id="9eac7-167">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="9eac7-168">Jei modulis negali būti judinamas aukštyn ar žemyn, rodyklės simbolis bus papilkėjęs.</span><span class="sxs-lookup"><span data-stu-id="9eac7-168">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="9eac7-169">Atleiskite modulį jo numetimui į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="9eac7-169">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="9eac7-170">Perkelkite modulį naudodami elipsės meniu</span><span class="sxs-lookup"><span data-stu-id="9eac7-170">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="9eac7-171">Modulio perkėlimui naudojant elipsės meniu, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-171">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-172">Pasirinkite modulį išorėje ar drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-172">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="9eac7-173">Pasirinkite elipsę (**...**) šalia modulio pavadinimo išorės juostoje arba modulio įrankių juostoje drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-173">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="9eac7-174">Jei modulis gali būti judinamas aukštyn ar žemyne konteineryje ar vietoje, matysime parinktis **Judinti aukštyn** ar **Judinti žemyn**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-174">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="9eac7-175">Pasirinkite norimą judesio parinktį modulio judinimui aukštyn ar žemyn pagal jo gimines.</span><span class="sxs-lookup"><span data-stu-id="9eac7-175">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="9eac7-176">Modulių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-176">Configure modules</span></span>

<span data-ttu-id="9eac7-177">Tolesnėse procedūrose aprašoma, kaip konfigūruoti turinio ir konteinerio modulius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-177">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="9eac7-178">Turinio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-178">Configure a content module</span></span>

<span data-ttu-id="9eac7-179">Norėdami konfigūruoti turinio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-179">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-180">Išorės juostoje kairėje, išplėskite medį ir pasirinkite bet kurį turinio modulį (pavyzdžiui, **Turinio blokavimą**).</span><span class="sxs-lookup"><span data-stu-id="9eac7-180">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="9eac7-181">Kitu atveju, galite pasirinkti modulį pagrindinėje drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-181">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="9eac7-182">Modulio parametrų juostoje dešinėje, įveskite parametrus bet kuriems norimo modulio valdikliams.</span><span class="sxs-lookup"><span data-stu-id="9eac7-182">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="9eac7-183">Komandų juostoje, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-183">On the command bar, select **Save**.</span></span> <span data-ttu-id="9eac7-184">Tai padarius, taip pat bus atnaujinta peržiūros drobė.</span><span class="sxs-lookup"><span data-stu-id="9eac7-184">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="9eac7-185">Redaguokite modulio teksto parametrus</span><span class="sxs-lookup"><span data-stu-id="9eac7-185">Edit module text properties</span></span>

<span data-ttu-id="9eac7-186">Tik skaitymui neskirti modulio teksto parametrai gali būti tiesiai redaguojami drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-186">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="9eac7-187">Modulio teksto parametrų redagavimui, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-187">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-188">Pasirinkite teksto valdiklį drobėje, tuomet padėkite savo rodyklę ten, kur norite redaguoti tekstą.</span><span class="sxs-lookup"><span data-stu-id="9eac7-188">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="9eac7-189">Įveskite teksto turinį.</span><span class="sxs-lookup"><span data-stu-id="9eac7-189">Enter your text content.</span></span>
1. <span data-ttu-id="9eac7-190">Pasirinkite bet kur už teksto turinio ribų tam, kad tęstumėte kito turinio redagavimą.</span><span class="sxs-lookup"><span data-stu-id="9eac7-190">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="9eac7-191">Eilutės paveikslėlio pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-191">Inline image selection</span></span>

<span data-ttu-id="9eac7-192">Tik skaitymui neskirti modulio paveikslėliai parametrai gali būti tiesiai keičiami drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-192">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="9eac7-193">Tam, kad pasirinktumėte naują modulio turinio paveikslėlį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="9eac7-193">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-194">Dukart spustelėję drobėje ant paveikslėlio.</span><span class="sxs-lookup"><span data-stu-id="9eac7-194">In the canvas, double-click the image.</span></span> <span data-ttu-id="9eac7-195">Tai atidarys medijos pasirinkimo langą.</span><span class="sxs-lookup"><span data-stu-id="9eac7-195">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="9eac7-196">Suraskite ir pasirinkite naują jūsų norimą naudoti paveikslėlį ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-196">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="9eac7-197">Naujas paveikslėlis dabar bus rodomas drobėje.</span><span class="sxs-lookup"><span data-stu-id="9eac7-197">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="9eac7-198">Konteinerio modulio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9eac7-198">Configure a container module</span></span>

<span data-ttu-id="9eac7-199">Norėdami konfigūruoti konteinerio modulį puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-199">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="9eac7-200">Savo puslapyje pasirinkite konteinerio modulį (pavyzdžiui, karuselės arba nepastovaus konteinerio modulį).</span><span class="sxs-lookup"><span data-stu-id="9eac7-200">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="9eac7-201">Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9eac7-201">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="9eac7-202">Struktūros srityje kairėje šalia konteinerio arba bet kokių konteineryje esančių vietų pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9eac7-202">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="9eac7-203">Tada į pasirinktą konteinerį įtraukite antrinių modulių.</span><span class="sxs-lookup"><span data-stu-id="9eac7-203">Then, add child modules to the selected container.</span></span> <span data-ttu-id="9eac7-204">Daugiau informacijos žr. ankstesniame šios temos skyriuje [Darbas su moduliais](#add-a-module).</span><span class="sxs-lookup"><span data-stu-id="9eac7-204">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="9eac7-205">Jei pirminiame konteineryje yra keli tos pačios kilmės antriniai moduliai, galite pakeisti jų rodymo pirminiame konteineryje tvarką.</span><span class="sxs-lookup"><span data-stu-id="9eac7-205">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="9eac7-206">Pasirinkite modulio daugtaškio mygtuką, tada naudokite rodyklės aukštyn arba rodyklės žemyn mygtukus.</span><span class="sxs-lookup"><span data-stu-id="9eac7-206">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9eac7-207">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9eac7-207">Additional resources</span></span>

[<span data-ttu-id="9eac7-208">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9eac7-208">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9eac7-209">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="9eac7-209">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9eac7-210">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="9eac7-210">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9eac7-211">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="9eac7-211">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="9eac7-212">Konteinerio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="9eac7-212">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="9eac7-213">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="9eac7-213">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
