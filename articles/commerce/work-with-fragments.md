---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026045"
---
# <a name="work-with-fragments"></a><span data-ttu-id="c8c42-103">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="c8c42-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="c8c42-104">Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c8c42-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8c42-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c8c42-105">Overview</span></span>

<span data-ttu-id="c8c42-106">Fragmentai leidžia centralizuotai kurti modulių konfigūracijas, kurias reikia pakartotinai naudoti jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="c8c42-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="c8c42-107">Pavyzdžiui, antraštės, poraštės ir reklamos juostos dažnai sukonfigūruojamos kaip fragmentai, nes jos yra bendrai naudojamos daug puslapių.</span><span class="sxs-lookup"><span data-stu-id="c8c42-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="c8c42-108">Fragmentus galima laikyti miniatiūriniais tinklalapiais, kuriuos galima įtraukti į kitus svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="c8c42-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="c8c42-109">Fragmentai turi savo ciklą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="c8c42-110">Kitaip tariant, jie kuriami, nurodomi, atnaujinami ir naikinami kaip nepriklausomi kūrimo įrankių objektai.</span><span class="sxs-lookup"><span data-stu-id="c8c42-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="c8c42-111">Sukonfigūruotus fragmentus galima naudoti ten, kur svetainės struktūroje galima naudoti modulius.</span><span class="sxs-lookup"><span data-stu-id="c8c42-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="c8c42-112">Fragmentai gali būti nurodomi puslapiuose, maketuose, šablonuose ir kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="c8c42-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c42-113">Fragmentai gali būti įdedami kituose fragmentuose iki septynių lygių gylio.</span><span class="sxs-lookup"><span data-stu-id="c8c42-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="c8c42-114">Pavyzdžiui, jei norite reklamuoti sezoninį įvykį daugelyje savo svetainės puslapių, galite naudoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="c8c42-115">Pirmas naujo fragmento kūrimo veiksmas – modulio tipo, nuo kurio norite pradėti, pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="c8c42-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="c8c42-116">Pavyzdžiui, galite kurti fragmentą naudodami pagrindinės reklamos juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="c8c42-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c42-117">Fragmentus galima kurti naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="c8c42-118">Tada pagrindinės reklamos juostos fragmentą galite konfigūruoti su konkrečiu reklaminiu turiniu.</span><span class="sxs-lookup"><span data-stu-id="c8c42-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="c8c42-119">Jei reikia, taip pat galite jį lokalizuoti.</span><span class="sxs-lookup"><span data-stu-id="c8c42-119">You can also localize it as you require.</span></span> <span data-ttu-id="c8c42-120">Tada naujas atskiras pagrindinės reklamos juostos fragmentas gali būti naudojamas visoje svetainėje kaip iš anksto sukonfigūruotas modulis.</span><span class="sxs-lookup"><span data-stu-id="c8c42-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="c8c42-121">Jį galite lengvai įtraukti į šablonus, konkrečius puslapius ar kitus fragmentus, kuriuose yra pagrindinės reklamos juostos modulių.</span><span class="sxs-lookup"><span data-stu-id="c8c42-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="c8c42-122">Visos vietos, į kurias įtrauktas fragmentas, yra nuorodos jūsų sukurtą centrinį pagrindinės reklamos juostos fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="c8c42-123">Jeigu publikuosite fragmento keitimus, tie pakeitimai bus iš karto rodomi visose vietose, kuriose fragmentas yra nurodytas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="c8c42-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="c8c42-124">Todėl fragmentai – galingas ir veiksmingas būdas pakartotinai naudoti ir centralizuotai valdyti modulių konfigūracijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="c8c42-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="c8c42-125">Veiksmingai juos naudodami galite smarkiai padidinti lankstumą ir padėti sumažinti išlaidas, susijusias su svetainės turinio valdymu.</span><span class="sxs-lookup"><span data-stu-id="c8c42-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="c8c42-126">Toliau pateiktame paveikslėlyje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="c8c42-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="c8c42-128">Fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-128">Create a fragment</span></span>

<span data-ttu-id="c8c42-129">Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="c8c42-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="c8c42-130">Esamos modulio konfigūracijos įrašymas kaip fragmento</span><span class="sxs-lookup"><span data-stu-id="c8c42-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="c8c42-131">Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8c42-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="c8c42-132">Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="c8c42-133">Struktūros srityje kairėje šalia modulio pavadinimo pasirinkite daugtaškio mygtuką (**...**).</span><span class="sxs-lookup"><span data-stu-id="c8c42-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="c8c42-134">Pasirinkite **Bendrinti kaip fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="c8c42-135">Atsiranda dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="c8c42-135">A dialog box appears.</span></span> <span data-ttu-id="c8c42-136">Įveskite fragmento pavadinimą ir metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="c8c42-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="c8c42-137">Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="c8c42-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="c8c42-138">Toliau pateiktame paveiksle parodyta, kaip modulio konfigūraciją įrašyti kaip fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Ekrano vaizdas, kuriame parodyta, kaip modulio konfigūraciją įrašyti kaip fragmentą](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="c8c42-140">Naujo fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-140">Create a new fragment</span></span>

<span data-ttu-id="c8c42-141">Norėdami sukurti naują fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8c42-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="c8c42-142">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c8c42-143">Pasirinkite **Naujas puslapio fragmentas**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="c8c42-144">Pasirodys dialogo langas, kuriame rodomi visi galimi modulių tipai.</span><span class="sxs-lookup"><span data-stu-id="c8c42-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="c8c42-145">Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="c8c42-146">Pasirinkite fragmento modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="c8c42-147">Toliau pateiktame paveikslėlyje parodyta, kur kurti naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-147">The following image shows where to create a new fragment.</span></span>

![Ekrano vaizdas, kuriame parodyta, kur kurti naują fragmentą](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="c8c42-149">Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="c8c42-150">Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="c8c42-151">Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c8c42-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="c8c42-152">Fragmento įtraukimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-152">Add a fragment</span></span>

<span data-ttu-id="c8c42-153">Norėdami į puslapį įtraukti fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8c42-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="c8c42-154">Struktūros srityje kairėje pasirinkite konteinerį arba vietą, į kuriuos galima įtraukti antrinių modulių.</span><span class="sxs-lookup"><span data-stu-id="c8c42-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="c8c42-155">Šalia konteinerio arba vietos pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="c8c42-156">Atsiranda dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="c8c42-156">A dialog box appears.</span></span>

    ![Ekrano vaizdas, kuriame parodyta, kaip įtraukti esamą fragmentą į vietą arba konteinerį](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="c8c42-158">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="c8c42-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="c8c42-159">Dialogo lange raskite ir pasirinkite fragmentą, kurį norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="c8c42-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="c8c42-160">Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="c8c42-161">Pasirinkite fragmentą, kurį norite įtraukti į konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c8c42-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Ekrano vaizdas, kuriame parodytas fragmentų parinkiklio modalusis langas](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="c8c42-163">Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.</span><span class="sxs-lookup"><span data-stu-id="c8c42-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="c8c42-164">Fragmento šalinimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-164">Remove a fragment</span></span>

<span data-ttu-id="c8c42-165">Norėdami fragmentą pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8c42-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="c8c42-166">Struktūros srityje kairėje šalia fragmento, kurį norite pašalinti, pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite šiukšliadėžės mygtuką.</span><span class="sxs-lookup"><span data-stu-id="c8c42-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="c8c42-167">Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c42-168">Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="c8c42-169">Svetainėje fragmentas **nepanaikinamas**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="c8c42-170">Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI).</span><span class="sxs-lookup"><span data-stu-id="c8c42-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="c8c42-171">Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="c8c42-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="c8c42-172">Fragmento redagavimas</span><span class="sxs-lookup"><span data-stu-id="c8c42-172">Edit a fragment</span></span>

<span data-ttu-id="c8c42-173">Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI.</span><span class="sxs-lookup"><span data-stu-id="c8c42-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="c8c42-174">Toks apribojimas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="c8c42-174">This restriction is by design.</span></span> <span data-ttu-id="c8c42-175">Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="c8c42-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="c8c42-176">Norėdami redaguoti fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8c42-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="c8c42-177">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="c8c42-178">Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c8c42-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="c8c42-179">Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="c8c42-180">Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="c8c42-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="c8c42-181">Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="c8c42-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8c42-182">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c8c42-182">Additional resources</span></span>

[<span data-ttu-id="c8c42-183">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c8c42-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="c8c42-184">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="c8c42-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="c8c42-185">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="c8c42-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="c8c42-186">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="c8c42-186">Work with publish groups</span></span>](publish-groups.md)
