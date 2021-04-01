---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3df2d99ef10f909cedef16167fb8d5a0024683b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210952"
---
# <a name="work-with-fragments"></a><span data-ttu-id="70d65-103">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="70d65-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="70d65-104">Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="70d65-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="70d65-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="70d65-105">Overview</span></span>

<span data-ttu-id="70d65-106">Fragmentai leidžia centralizuotai kurti modulių konfigūracijas, kurias reikia pakartotinai naudoti jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="70d65-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="70d65-107">Pavyzdžiui, antraštės, poraštės ir reklamos juostos dažnai sukonfigūruojamos kaip fragmentai, nes jos yra bendrai naudojamos daug puslapių.</span><span class="sxs-lookup"><span data-stu-id="70d65-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="70d65-108">Fragmentus galima laikyti miniatiūriniais tinklalapiais, kuriuos galima įtraukti į kitus svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="70d65-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="70d65-109">Fragmentai turi savo ciklą.</span><span class="sxs-lookup"><span data-stu-id="70d65-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="70d65-110">Kitaip tariant, jie kuriami, nurodomi, atnaujinami ir naikinami kaip nepriklausomi kūrimo įrankių objektai.</span><span class="sxs-lookup"><span data-stu-id="70d65-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="70d65-111">Sukonfigūruotus fragmentus galima naudoti ten, kur svetainės struktūroje galima naudoti modulius.</span><span class="sxs-lookup"><span data-stu-id="70d65-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="70d65-112">Fragmentai gali būti nurodomi puslapiuose, maketuose, šablonuose ir kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="70d65-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="70d65-113">Fragmentai gali būti įdedami kituose fragmentuose iki septynių lygių gylio.</span><span class="sxs-lookup"><span data-stu-id="70d65-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="70d65-114">Pavyzdžiui, jei norite reklamuoti sezoninį įvykį daugelyje savo svetainės puslapių, galite naudoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="70d65-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="70d65-115">Pirmas naujo fragmento kūrimo veiksmas – modulio tipo, nuo kurio norite pradėti, pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="70d65-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="70d65-116">Pavyzdžiui, galite kurti fragmentą naudodami pagrindinės reklamos juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="70d65-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="70d65-117">Fragmentus galima kurti naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="70d65-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="70d65-118">Tada pagrindinės reklamos juostos fragmentą galite konfigūruoti su konkrečiu reklaminiu turiniu.</span><span class="sxs-lookup"><span data-stu-id="70d65-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="70d65-119">Jei reikia, taip pat galite jį lokalizuoti.</span><span class="sxs-lookup"><span data-stu-id="70d65-119">You can also localize it as you require.</span></span> <span data-ttu-id="70d65-120">Tada naujas atskiras pagrindinės reklamos juostos fragmentas gali būti naudojamas visoje svetainėje kaip iš anksto sukonfigūruotas modulis.</span><span class="sxs-lookup"><span data-stu-id="70d65-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="70d65-121">Jį galite lengvai įtraukti į šablonus, konkrečius puslapius ar kitus fragmentus, kuriuose yra pagrindinės reklamos juostos modulių.</span><span class="sxs-lookup"><span data-stu-id="70d65-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="70d65-122">Visos vietos, į kurias įtrauktas fragmentas, yra nuorodos jūsų sukurtą centrinį pagrindinės reklamos juostos fragmentą.</span><span class="sxs-lookup"><span data-stu-id="70d65-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="70d65-123">Jeigu publikuosite fragmento keitimus, tie pakeitimai bus iš karto rodomi visose vietose, kuriose fragmentas yra nurodytas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="70d65-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="70d65-124">Todėl fragmentai – galingas ir veiksmingas būdas pakartotinai naudoti ir centralizuotai valdyti modulių konfigūracijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="70d65-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="70d65-125">Veiksmingai juos naudodami galite smarkiai padidinti lankstumą ir padėti sumažinti išlaidas, susijusias su svetainės turinio valdymu.</span><span class="sxs-lookup"><span data-stu-id="70d65-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="70d65-126">Toliau pateiktame paveikslėlyje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="70d65-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="70d65-128">Fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="70d65-128">Create a fragment</span></span>

<span data-ttu-id="70d65-129">Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="70d65-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="70d65-130">Esamos modulio konfigūracijos įrašymas kaip fragmento</span><span class="sxs-lookup"><span data-stu-id="70d65-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="70d65-131">Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="70d65-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70d65-132">Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="70d65-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="70d65-133">Struktūros srities kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite anksčiau konfigūruotą modulį.</span><span class="sxs-lookup"><span data-stu-id="70d65-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="70d65-134">Struktūros srityje arba pasirinkto modulio įrankių juostoje vizualinėje puslapio daryklėje pasirinkite daugtaškį (**...**), esantį šalia modulio pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="70d65-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="70d65-135">Pasirinkite **Bendrinti kaip fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="70d65-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="70d65-136">Dialogo lange **Įrašyti kaip fragmentą** įveskite fragmento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="70d65-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="70d65-137">Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="70d65-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="70d65-138">Kurti naują fragmentą</span><span class="sxs-lookup"><span data-stu-id="70d65-138">Create a new fragment</span></span>

<span data-ttu-id="70d65-139">Norėdami sukurti naują fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="70d65-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70d65-140">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="70d65-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="70d65-141">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="70d65-141">Select **New**.</span></span> <span data-ttu-id="70d65-142">Pasirodys dialogo langas **Naujas fragmentas**, kuriame rodomi visi galimi modulių tipai.</span><span class="sxs-lookup"><span data-stu-id="70d65-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="70d65-143">Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="70d65-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="70d65-144">Pasirinkite fragmento modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="70d65-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="70d65-145">Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="70d65-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="70d65-146">Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas</span><span class="sxs-lookup"><span data-stu-id="70d65-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="70d65-147">Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.</span><span class="sxs-lookup"><span data-stu-id="70d65-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="70d65-148">Fragmento įtraukimas</span><span class="sxs-lookup"><span data-stu-id="70d65-148">Add a fragment</span></span>

<span data-ttu-id="70d65-149">Norėdami įtraukti fragmentą „Commerce” svetainių daryklės puslapį, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="70d65-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70d65-150">Struktūros juostoje kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite konteinerį arba vietą, kur būtų galima įtraukti antrinius modulius.</span><span class="sxs-lookup"><span data-stu-id="70d65-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="70d65-151">Pasirinkite daugtaškį (**...**) šalia talpyklos ar vietos pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="70d65-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="70d65-152">Arba, jei naudojate vizualinę puslapio daryklę, pasirinkite pliuso simbolį (**+**).</span><span class="sxs-lookup"><span data-stu-id="70d65-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="70d65-153">Pasirinkite **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="70d65-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="70d65-154">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="70d65-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="70d65-155">Dialogo lange **Pasirinkti fragmentą** ieškokite ir pasirinkite fragmentą, kurį norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="70d65-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="70d65-156">Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="70d65-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="70d65-157">Pasirinkite fragmentą, kurį norite įtraukti į konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="70d65-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="70d65-158">Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.</span><span class="sxs-lookup"><span data-stu-id="70d65-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="70d65-159">Fragmento šalinimas</span><span class="sxs-lookup"><span data-stu-id="70d65-159">Remove a fragment</span></span>

<span data-ttu-id="70d65-160">Norėdami pašalinti fragmentą iš „Commerce” svetainių daryklės puslapio vietos ar konteinerio, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="70d65-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70d65-161">Išorinėje jusotoje lairėje, pasirinkite elipsę (**...**) šalia šalinamo fragmento pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį.</span><span class="sxs-lookup"><span data-stu-id="70d65-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="70d65-162">Arba galite pasirinkite fragmentą vizualinėje puslapio daryklėje ir pasirinkti šiukšlių dėžės simbolį fragmento įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="70d65-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="70d65-163">Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="70d65-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="70d65-164">Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą.</span><span class="sxs-lookup"><span data-stu-id="70d65-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="70d65-165">Svetainėje fragmentas **nepanaikinamas**.</span><span class="sxs-lookup"><span data-stu-id="70d65-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="70d65-166">Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI).</span><span class="sxs-lookup"><span data-stu-id="70d65-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="70d65-167">Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="70d65-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="70d65-168">Fragmento redagavimas</span><span class="sxs-lookup"><span data-stu-id="70d65-168">Edit a fragment</span></span>

<span data-ttu-id="70d65-169">Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI.</span><span class="sxs-lookup"><span data-stu-id="70d65-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="70d65-170">Toks apribojimas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="70d65-170">This restriction is by design.</span></span> <span data-ttu-id="70d65-171">Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="70d65-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="70d65-172">Norėdami redaguoti fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="70d65-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="70d65-173">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="70d65-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="70d65-174">Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="70d65-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="70d65-175">Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą.</span><span class="sxs-lookup"><span data-stu-id="70d65-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="70d65-176">Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="70d65-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="70d65-177">Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="70d65-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70d65-178">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="70d65-178">Additional resources</span></span>

[<span data-ttu-id="70d65-179">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="70d65-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="70d65-180">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="70d65-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="70d65-181">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="70d65-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="70d65-182">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="70d65-182">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]