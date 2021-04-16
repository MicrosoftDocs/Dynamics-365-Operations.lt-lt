---
title: Darbas su fragmentais
description: Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793950"
---
# <a name="work-with-fragments"></a><span data-ttu-id="4d809-103">Darbas su fragmentais</span><span class="sxs-lookup"><span data-stu-id="4d809-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d809-104">Šioje temoje aprašoma, kodėl, kada ir kaip naudoti fragmentus programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="4d809-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4d809-105">Fragmentai leidžia centralizuotai kurti modulių konfigūracijas, kurias reikia pakartotinai naudoti jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="4d809-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="4d809-106">Pavyzdžiui, antraštės, poraštės ir reklamos juostos dažnai sukonfigūruojamos kaip fragmentai, nes jos yra bendrai naudojamos daug puslapių.</span><span class="sxs-lookup"><span data-stu-id="4d809-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="4d809-107">Fragmentus galima laikyti miniatiūriniais tinklalapiais, kuriuos galima įtraukti į kitus svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="4d809-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="4d809-108">Fragmentai turi savo ciklą.</span><span class="sxs-lookup"><span data-stu-id="4d809-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="4d809-109">Kitaip tariant, jie kuriami, nurodomi, atnaujinami ir naikinami kaip nepriklausomi kūrimo įrankių objektai.</span><span class="sxs-lookup"><span data-stu-id="4d809-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="4d809-110">Sukonfigūruotus fragmentus galima naudoti ten, kur svetainės struktūroje galima naudoti modulius.</span><span class="sxs-lookup"><span data-stu-id="4d809-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="4d809-111">Fragmentai gali būti nurodomi puslapiuose, maketuose, šablonuose ir kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="4d809-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="4d809-112">Fragmentai gali būti įdedami kituose fragmentuose iki septynių lygių gylio.</span><span class="sxs-lookup"><span data-stu-id="4d809-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="4d809-113">Pavyzdžiui, jei norite reklamuoti sezoninį įvykį daugelyje savo svetainės puslapių, galite naudoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="4d809-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="4d809-114">Pirmas naujo fragmento kūrimo veiksmas – modulio tipo, nuo kurio norite pradėti, pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="4d809-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="4d809-115">Pavyzdžiui, galite kurti fragmentą naudodami pagrindinės reklamos juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="4d809-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="4d809-116">Fragmentus galima kurti naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="4d809-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="4d809-117">Tada pagrindinės reklamos juostos fragmentą galite konfigūruoti su konkrečiu reklaminiu turiniu.</span><span class="sxs-lookup"><span data-stu-id="4d809-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="4d809-118">Jei reikia, taip pat galite jį lokalizuoti.</span><span class="sxs-lookup"><span data-stu-id="4d809-118">You can also localize it as you require.</span></span> <span data-ttu-id="4d809-119">Tada naujas atskiras pagrindinės reklamos juostos fragmentas gali būti naudojamas visoje svetainėje kaip iš anksto sukonfigūruotas modulis.</span><span class="sxs-lookup"><span data-stu-id="4d809-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="4d809-120">Jį galite lengvai įtraukti į šablonus, konkrečius puslapius ar kitus fragmentus, kuriuose yra pagrindinės reklamos juostos modulių.</span><span class="sxs-lookup"><span data-stu-id="4d809-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="4d809-121">Visos vietos, į kurias įtrauktas fragmentas, yra nuorodos jūsų sukurtą centrinį pagrindinės reklamos juostos fragmentą.</span><span class="sxs-lookup"><span data-stu-id="4d809-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="4d809-122">Jeigu publikuosite fragmento keitimus, tie pakeitimai bus iš karto rodomi visose vietose, kuriose fragmentas yra nurodytas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="4d809-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="4d809-123">Todėl fragmentai – galingas ir veiksmingas būdas pakartotinai naudoti ir centralizuotai valdyti modulių konfigūracijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="4d809-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="4d809-124">Veiksmingai juos naudodami galite smarkiai padidinti lankstumą ir padėti sumažinti išlaidas, susijusias su svetainės turinio valdymu.</span><span class="sxs-lookup"><span data-stu-id="4d809-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="4d809-125">Toliau pateiktame paveikslėlyje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="4d809-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Iliustracija, kurioje rodoma, kaip fragmentai gali būti naudojami bendrai naudojamų modulių konfigūracijų kūrimui centralizuoti visoje el. prekybos svetainėje](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="4d809-127">Fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d809-127">Create a fragment</span></span>

<span data-ttu-id="4d809-128">Galite sukurti naują fragmentą arba kaip fragmentą įrašyti esamą modulio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="4d809-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="4d809-129">Esamos modulio konfigūracijos įrašymas kaip fragmento</span><span class="sxs-lookup"><span data-stu-id="4d809-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="4d809-130">Norėdami anksčiau sukonfigūruotą modulį konvertuoti į daugkartinio naudojimo fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d809-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d809-131">Atidarykite puslapį arba šabloną, kuriame yra modulis, kurį norite konvertuoti į fragmentą.</span><span class="sxs-lookup"><span data-stu-id="4d809-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="4d809-132">Struktūros srities kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite anksčiau konfigūruotą modulį.</span><span class="sxs-lookup"><span data-stu-id="4d809-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="4d809-133">Struktūros srityje arba pasirinkto modulio įrankių juostoje vizualinėje puslapio daryklėje pasirinkite daugtaškį (**...**), esantį šalia modulio pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="4d809-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="4d809-134">Pasirinkite **Bendrinti kaip fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="4d809-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="4d809-135">Dialogo lange **Įrašyti kaip fragmentą** įveskite fragmento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4d809-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="4d809-136">Pasirinkite **Gerai**, kad modulių konfigūraciją įrašytumėte kaip fragmentą, kurį galima įtraukti į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="4d809-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="4d809-137">Kurti naują fragmentą</span><span class="sxs-lookup"><span data-stu-id="4d809-137">Create a new fragment</span></span>

<span data-ttu-id="4d809-138">Norėdami sukurti naują fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d809-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d809-139">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="4d809-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="4d809-140">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d809-140">Select **New**.</span></span> <span data-ttu-id="4d809-141">Pasirodys dialogo langas **Naujas fragmentas**, kuriame rodomi visi galimi modulių tipai.</span><span class="sxs-lookup"><span data-stu-id="4d809-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="4d809-142">Kaip minėta anksčiau, fragmentai gali būti kuriami naudojant bet kokį modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="4d809-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="4d809-143">Pasirinkite fragmento modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="4d809-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="4d809-144">Pasirinkdami bendrąjį konteinerio modulio tipą, gausite daugiausiai lankstumo, kai vėliau reikės atnaujinti ir konfigūruoti fragmentą.</span><span class="sxs-lookup"><span data-stu-id="4d809-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="4d809-145">Puslapio fragmentų įtraukimas, pašalinimas arba redagavimas</span><span class="sxs-lookup"><span data-stu-id="4d809-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="4d809-146">Tolesnėse procedūrose aprašoma, kaip įtraukti fragmentų, juos pašalinti ir redaguoti.</span><span class="sxs-lookup"><span data-stu-id="4d809-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="4d809-147">Fragmento įtraukimas</span><span class="sxs-lookup"><span data-stu-id="4d809-147">Add a fragment</span></span>

<span data-ttu-id="4d809-148">Norėdami įtraukti fragmentą „Commerce” svetainių daryklės puslapį, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d809-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d809-149">Struktūros juostoje kairėje arba tiesiai vizualinėje puslapio daryklėje pasirinkite konteinerį arba vietą, kur būtų galima įtraukti antrinius modulius.</span><span class="sxs-lookup"><span data-stu-id="4d809-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="4d809-150">Pasirinkite daugtaškį (**...**) šalia talpyklos ar vietos pavadinimo.</span><span class="sxs-lookup"><span data-stu-id="4d809-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="4d809-151">Arba, jei naudojate vizualinę puslapio daryklę, pasirinkite pliuso simbolį (**+**).</span><span class="sxs-lookup"><span data-stu-id="4d809-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="4d809-152">Pasirinkite **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="4d809-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="4d809-153">Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti fragmentą** nepasiekiama.</span><span class="sxs-lookup"><span data-stu-id="4d809-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="4d809-154">Dialogo lange **Pasirinkti fragmentą** ieškokite ir pasirinkite fragmentą, kurį norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="4d809-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="4d809-155">Jei sąraše nėra pasiekiamų fragmentų, pirmiausia gali reikėti sukurti fragmentą naudojant pasirinkto konteinerio ar vietos palaikomą modulio tipą.</span><span class="sxs-lookup"><span data-stu-id="4d809-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="4d809-156">Pasirinkite fragmentą, kurį norite įtraukti į konteinerį arba vietą jūsų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="4d809-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="4d809-157">Konteineryje arba vietoje leidžiami moduliai nustatomi puslapio šablone arba pačių modulių aprašuose.</span><span class="sxs-lookup"><span data-stu-id="4d809-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="4d809-158">Fragmento šalinimas</span><span class="sxs-lookup"><span data-stu-id="4d809-158">Remove a fragment</span></span>

<span data-ttu-id="4d809-159">Norėdami pašalinti fragmentą iš „Commerce” svetainių daryklės puslapio vietos ar konteinerio, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d809-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d809-160">Išorinėje kairinėje juostoje pasirinkite elipsę (**...**) šalia šalinamo fragmento pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį.</span><span class="sxs-lookup"><span data-stu-id="4d809-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="4d809-161">Arba galite pasirinkite fragmentą vizualinėje puslapio daryklėje ir pasirinkti šiukšlių dėžės simbolį fragmento įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="4d809-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="4d809-162">Kai būsite paraginti patvirtinti, kad norite pašalinti fragmentą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d809-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="4d809-163">Kai pašalinate fragmentą iš puslapio, iš šio puslapio tik pašalinate nuorodą į tą fragmentą.</span><span class="sxs-lookup"><span data-stu-id="4d809-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="4d809-164">Svetainėje fragmentas **nepanaikinamas**.</span><span class="sxs-lookup"><span data-stu-id="4d809-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="4d809-165">Norint panaikinti fragmentus iš svetainės, reikia naudoti fragmento inspektoriaus vartotojo sąsają (UI).</span><span class="sxs-lookup"><span data-stu-id="4d809-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="4d809-166">Panaikinti fragmentus iš svetainės galite tik tuo atveju, jei jie nėra nurodyti jokiuose puslapiuose, šablonuose ar kituose fragmentuose.</span><span class="sxs-lookup"><span data-stu-id="4d809-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="4d809-167">Fragmento redagavimas</span><span class="sxs-lookup"><span data-stu-id="4d809-167">Edit a fragment</span></span>

<span data-ttu-id="4d809-168">Norint redaguoti fragmentus reikia naudoti fragmentų rengyklės UI.</span><span class="sxs-lookup"><span data-stu-id="4d809-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="4d809-169">Toks apribojimas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="4d809-169">This restriction is by design.</span></span> <span data-ttu-id="4d809-170">Jis padeda užtikrinti, kad autoriai konkretaus puslapio modulių redagavimo proceso nesupainios su fragmentų, kurie gali būti bendrai naudojami daug puslapių, redagavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="4d809-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="4d809-171">Norėdami redaguoti fragmentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d809-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d809-172">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="4d809-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="4d809-173">Dalyje **Fragmentai** pasirinkite fragmentą, kurį norite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="4d809-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="4d809-174">Pagal poreikius redaguokite fragmento modulio ypatybes ir struktūrą.</span><span class="sxs-lookup"><span data-stu-id="4d809-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="4d809-175">Šis procesas panašus į modulių, kurie redaguojami puslapio rengyklės rodinyje, redagavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="4d809-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="4d809-176">Fragmentą taip pat galite redaguoti pasirinkę jį puslapyje, šablone arba pirminiame fragmente, o tada dešinėje pusėje esančioje ypatybių srityje pasirinkę **Redaguoti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="4d809-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d809-177">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4d809-177">Additional resources</span></span>

[<span data-ttu-id="4d809-178">Šablonų ir maketų apžvalga</span><span class="sxs-lookup"><span data-stu-id="4d809-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4d809-179">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="4d809-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4d809-180">Darbas su esamais maketais</span><span class="sxs-lookup"><span data-stu-id="4d809-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4d809-181">Darbas su publikavimo grupėmis</span><span class="sxs-lookup"><span data-stu-id="4d809-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
