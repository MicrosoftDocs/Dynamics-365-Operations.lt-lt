---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698101"
---
# <a name="work-with-fragments"></a><span data-ttu-id="be901-103">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="be901-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="be901-104">Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="be901-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="be901-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="be901-105">Overview</span></span>

<span data-ttu-id="be901-106">Fragmentai leidžia centralizuotai kurti modulių konfigūracijas, kurias reikia pakartotinai naudoti jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="be901-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="be901-107">Pavyzdžiui, antraštės, poraštės ir reklamos juostos dažnai sukonfigūruojamos kaip fragmentai, nes jos yra bendrai naudojamos daug puslapių.</span><span class="sxs-lookup"><span data-stu-id="be901-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="be901-108">Fragmentus galima laikyti miniatiūriniais tinklalapiais, kuriuos galima įtraukti į kitus svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="be901-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="be901-109">Fragmentai turi savo ciklą.</span><span class="sxs-lookup"><span data-stu-id="be901-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="be901-110">Kitaip tariant, jie kuriami, nurodomi, atnaujinami ir naikinami kaip nepriklausomi kūrimo įrankių objektai.</span><span class="sxs-lookup"><span data-stu-id="be901-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="be901-111">Sukonfigūruotus fragmentus galima naudoti ten, kur svetainės struktūroje galima naudoti modulius.</span><span class="sxs-lookup"><span data-stu-id="be901-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="be901-112">Fragmentai gali būti nurodomi puslapiuose, maketuose, šablonuose ir kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="be901-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="be901-113">Fragmentai gali būti įdedami kituose fragmentuose iki septynių lygių gylio.</span><span class="sxs-lookup"><span data-stu-id="be901-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="be901-114">Pavyzdžiui, jei norite reklamuoti sezoninį įvykį daugelyje savo svetainės puslapių, galite naudoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="be901-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="be901-115">Pirmas naujo fragmento kūrimo veiksmas – modulio tipo, nuo kurio norite pradėti, pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="be901-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="be901-116">Pavyzdžiui, galite kurti fragmentą naudodami pagrindinės reklamos juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="be901-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="be901-117">Fragmentus galima kurti naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="be901-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="be901-118">Tada pagrindinės reklamos juostos fragmentą galite konfigūruoti su konkrečiu reklaminiu turiniu.</span><span class="sxs-lookup"><span data-stu-id="be901-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="be901-119">Jei reikia, taip pat galite jį lokalizuoti.</span><span class="sxs-lookup"><span data-stu-id="be901-119">You can also localize it as you require.</span></span> <span data-ttu-id="be901-120">Tada naujas atskiras pagrindinės reklamos juostos fragmentas gali būti naudojamas visoje svetainėje kaip iš anksto sukonfigūruotas modulis.</span><span class="sxs-lookup"><span data-stu-id="be901-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="be901-121">Jį galite lengvai įtraukti į šablonus, konkrečius puslapius ar kitus fragmentus, kuriuose yra pagrindinės reklamos juostos modulių.</span><span class="sxs-lookup"><span data-stu-id="be901-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="be901-122">Visos vietos, į kurias įtrauktas fragmentas, yra nuorodos jūsų sukurtą centrinį pagrindinės reklamos juostos fragmentą.</span><span class="sxs-lookup"><span data-stu-id="be901-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="be901-123">Jeigu publikuosite fragmento keitimus, tie pakeitimai bus iš karto rodomi visose vietose, kuriose fragmentas yra nurodytas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="be901-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="be901-124">Todėl fragmentai – galingas ir veiksmingas būdas pakartotinai naudoti ir centralizuotai valdyti modulių konfigūracijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="be901-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="be901-125">Veiksmingai juos naudodami galite smarkiai padidinti lankstumą ir padėti sumažinti išlaidas, susijusias su svetainės turinio valdymu.</span><span class="sxs-lookup"><span data-stu-id="be901-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="be901-126">Toliau pateiktame paveikslėlyje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="be901-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="be901-128">Fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="be901-128">Create a fragment</span></span>

<span data-ttu-id="be901-129">Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="be901-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="be901-130">Naujo fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="be901-130">Create a new fragment</span></span>

<span data-ttu-id="be901-131">Norėdami sukurti naują fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be901-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="be901-132">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="be901-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="be901-133">Pasirinkite **Naujas puslapio fragmentas**.</span><span class="sxs-lookup"><span data-stu-id="be901-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="be901-134">Pasirodys dialogo langas, kuriame rodomi visi galimi modulių tipai.</span><span class="sxs-lookup"><span data-stu-id="be901-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="be901-135">Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="be901-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="be901-136">Pasirinkite fragmento modulio tipą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="be901-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="be901-137">Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="be901-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="be901-138">Esamos modulio konfigūracijos įrašymas kaip fragmento</span><span class="sxs-lookup"><span data-stu-id="be901-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="be901-139">Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be901-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="be901-140">Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="be901-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="be901-141">Struktūros srityje kairėje šalia modulio pavadinimo pasirinkite daugtaškio mygtuką (**...**), tada pasirinkite **Įrašyti kaip fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="be901-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="be901-142">Atsiranda dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="be901-142">A dialog box appears.</span></span>
1. <span data-ttu-id="be901-143">Įveskite fragmento pavadinimą ir metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="be901-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="be901-144">Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="be901-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="be901-145">Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas</span><span class="sxs-lookup"><span data-stu-id="be901-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="be901-146">Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.</span><span class="sxs-lookup"><span data-stu-id="be901-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="be901-147">Fragmento įtraukimas</span><span class="sxs-lookup"><span data-stu-id="be901-147">Add a fragment</span></span>

<span data-ttu-id="be901-148">Norėdami į puslapį įtraukti fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be901-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="be901-149">Struktūros srityje kairėje pasirinkite konteinerį arba vietą, į kuriuos galima įtraukti antrinių modulių.</span><span class="sxs-lookup"><span data-stu-id="be901-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="be901-150">Šalia konteinerio arba vietos pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="be901-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="be901-151">Atsiranda dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="be901-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="be901-152">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="be901-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="be901-153">Dialogo lange raskite ir pasirinkite fragmentą, kurį norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="be901-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="be901-154">Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="be901-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="be901-155">Pasirinkite **Gerai**, kad pasirinktą fragmentą įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="be901-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="be901-156">Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.</span><span class="sxs-lookup"><span data-stu-id="be901-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="be901-157">Fragmento šalinimas</span><span class="sxs-lookup"><span data-stu-id="be901-157">Remove a fragment</span></span>

<span data-ttu-id="be901-158">Norėdami fragmentą pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be901-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="be901-159">Struktūros srityje kairėje šalia fragmento, kurį norite pašalinti, pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite šiukšliadėžės mygtuką.</span><span class="sxs-lookup"><span data-stu-id="be901-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="be901-160">Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="be901-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="be901-161">Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą.</span><span class="sxs-lookup"><span data-stu-id="be901-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="be901-162">Svetainėje fragmentas **nepanaikinamas**.</span><span class="sxs-lookup"><span data-stu-id="be901-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="be901-163">Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI).</span><span class="sxs-lookup"><span data-stu-id="be901-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="be901-164">Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="be901-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="be901-165">Fragmento redagavimas</span><span class="sxs-lookup"><span data-stu-id="be901-165">Edit a fragment</span></span>

<span data-ttu-id="be901-166">Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI.</span><span class="sxs-lookup"><span data-stu-id="be901-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="be901-167">Toks apribojimas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="be901-167">This restriction is by design.</span></span> <span data-ttu-id="be901-168">Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="be901-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="be901-169">Norėdami redaguoti fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="be901-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="be901-170">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="be901-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="be901-171">Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="be901-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="be901-172">Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą.</span><span class="sxs-lookup"><span data-stu-id="be901-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="be901-173">Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="be901-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="be901-174">Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="be901-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be901-175">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="be901-175">Additional resources</span></span>

[<span data-ttu-id="be901-176">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="be901-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="be901-177">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="be901-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="be901-178">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="be901-178">Work with preset layouts</span></span>](work-with-layouts.md)
