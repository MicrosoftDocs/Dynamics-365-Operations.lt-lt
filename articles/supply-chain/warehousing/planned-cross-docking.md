---
title: Suplanuotas prekių skirstymas
description: Šioje temoje aprašoma Išplėstinis suplanuoto prekių skirstymas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis. Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911253"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="ea8d6-104">Suplanuotas prekių skirstymas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea8d6-105">Šioje temoje aprašomas išplėstini suplanuotas prekių skirstymą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="ea8d6-106">Išplėstinis suplanuoto prekių skirstymas yra sandėlio procesas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="ea8d6-107">Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="ea8d6-108">Suplanuoto prekių skirstymo darbuotojai gali praleisti gaunamų atsargų padėjimus ir siunčiamų prekių paėmimus, jau pažymėti siunčiamam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="ea8d6-109">Todėl atsargų paėmimo kartai yra sumažinti, jei įmanoma.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="ea8d6-110">Taip pat dėl mažesnės sąveikos su sistema, laiko ir vietos taupymas sandėlio darbo aukšte yra padidinami.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="ea8d6-111">Norėdami vykdyti prekių skirstymą, turite sukonfigūruoti naują prekių skirstymo šabloną, kuriame nurodytas tiekimo šaltinis ir kiti prekių skirstymo reikalavimų rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="ea8d6-112">Kadangi siuntimo užsakymas sukuriamas, eilutė turi būti pažymėta pagal gavimo užsakymą, kuriame yra ta prekė.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="ea8d6-113">Nurodymo kodą galite pasirinkti prekių skirstymo šablone, panašiai kaip nustatote papildymo ir pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="ea8d6-114">Gaunamo užsakymo gavimo metu, prekių skirstymo nustatymas automatiškai identifikuoja prekių skirstymo poreikius ir sukuria reikiamo kiekio perkėlimo darbą, pagrįstą vietos nurodymo nustatymu.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="ea8d6-115">Atsargų operacijos yra *ne* registruojamos atšaukus prekių skirstymo darbą, net jei šios galimybės nustatymas yra įjungtas sandėlio valdymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="ea8d6-116">Įjungti suplanuoto prekių skirstymo funkcijas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="ea8d6-117">Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir toliau pateikiama tvarka įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="ea8d6-118">*Suplanuotas prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="ea8d6-119">*Prekių skirstymo šablonai su vietovės nurodymais*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="ea8d6-120">Ši funkcija įgalina prekių skirstymo šablone nurodyti lauką **Nurodymo kodas**, panašiai kaip nustatote papildymo šablonus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="ea8d6-121">Šios funkcijos įgalinimas neleidžia jums įtraukti nurodymo kodo į prekių skirstymo šablono eilutes, paskutinei *Įdėti* eilutei.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="ea8d6-122">Taip užtikrinama, kad prieš atsižvelgiant į darbo šablonus, galutinė įdėjimo vieta gali būti nustatyta darbo kūrimo metu.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="ea8d6-123">Sąranka</span><span class="sxs-lookup"><span data-stu-id="ea8d6-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="ea8d6-124">Pakartotinai generuoti krovinio registravimo metodus</span><span class="sxs-lookup"><span data-stu-id="ea8d6-124">Regenerate load posting methods</span></span>

<span data-ttu-id="ea8d6-125">Suplanuotas prekių skirstymas yra įgyvendinamas kaip krovinio registravimo metodas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="ea8d6-126">Įjungę funkciją, turite pakartotinai generuoti metodus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="ea8d6-127">Eikite į **Sandėlio valdymas \> Nustatymas \> Krovinio registravimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="ea8d6-128">Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="ea8d6-129">Baigus pakartotinį generavimą , turėtumėte matyti metodą, kurio **Metodo pavadinimas** yra *Planuoti prekių skirstymą*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="ea8d6-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="ea8d6-131">Sukurkite prekių skirstymo šabloną</span><span class="sxs-lookup"><span data-stu-id="ea8d6-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="ea8d6-132">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Prekių skirstymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="ea8d6-133">Veiksmų srityje pasirinkite **Nauja** šablonui sukurti.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="ea8d6-134">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-135">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="ea8d6-136">Šis laukas nurodo tvarką, kuria yra vertinami šablonai.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="ea8d6-137">**Prekių skirstymo šablono ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="ea8d6-138">**Aprašas:** *Sandėlis 51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="ea8d6-139">**Paklausos išleidimo strategija:** *Prieš tiekimo kvitą*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="ea8d6-140">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ea8d6-141">„FastTab“ nustatymas **Planavimas** kontroliuoja, kaip veikia šablonas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="ea8d6-142">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-142">Set the following values:</span></span>

    - <span data-ttu-id="ea8d6-143">**Paklausos reikalavimai:** *Nėra*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="ea8d6-144">Šiame lauke apibrėžiami atsargų paklausos reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="ea8d6-145">Jei paklausa turi būti susieta su tiekimu prieš išleidimą, pasirinkite *Žymėjimas*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="ea8d6-146">Jei paklausa turi būti užsakymas, rezervuotas pagal tiekimą prieš išleidžiant, pasirinkite *Užsakymo rezervavimas*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="ea8d6-147">**Vietos tipas:** *Siuntimo vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="ea8d6-148">Šiame lauke nurodoma, ar prekių skirstymas turi naudoti surinkimo/krovinio vietas iš siuntimo, ar reikia naudoti vietos nurodymus, kad būtų galima rasti surinkimo/krovinio vietas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="ea8d6-149">**Darbo šablonas** – Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="ea8d6-150">Šiame lauke apibrėžiamas darbo šablonas, kurį reikia naudoti, kai sukuriamas prekių skirstymo darbas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="ea8d6-151">**Iš naujo patikrinti tiekimo kvitą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="ea8d6-152">Ši pasirinktis nurodo, ar turi būti iš naujo patikrinta pasiūla gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="ea8d6-153">Jei ši pasirinktis nustatyta kaip *Taip,* tikrinamas ir maksimalus laiko langą, ir galiojimo dienų intervalas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="ea8d6-154">**Nurodymo kodas:** Palikite šį lauką tuščią</span><span class="sxs-lookup"><span data-stu-id="ea8d6-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="ea8d6-155">Šią parinktį įgalina funkcija *Prekių skirstymo šablonai su vietos nurodymais*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="ea8d6-156">Sistema naudoja vietos nurodymus, kad padėtų nustatyti geriausią vietą, į kurią bus perkeliamos prekių skirstymo atsargos.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="ea8d6-157">Galite ją nustatyti, priskirdami nurodymo kodą kiekvienam susijusiam prekių skirstymo šablonui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="ea8d6-158">Jei nurodymo kodas yra nustatytas, sistema ieškos vietos nurodymų pagal nurodymo kodą, kai darbas bus sugeneruotas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="ea8d6-159">Tokiu būdu galite apriboti vietos nurodymus, naudojamus konkrečiam prekių skirstymo šablonui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="ea8d6-160">**Patikrinti laiko langą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="ea8d6-161">Ši pasirinktis nurodo, ar maksimalaus laiko langas turi būti įvertintas, kai pasirinktas tiekimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="ea8d6-162">Jei ši pasirinktis nustatyta kaip *Taip*, laukai, susiję su maksimalaus ir minimalaus laiko langais, bus prieinami.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="ea8d6-163">**Maksimalus laiko langais:** *5*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="ea8d6-164">Šis laukas apibrėžia maksimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="ea8d6-165">**Maksimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="ea8d6-166">**Minimalus laiko langas:** *0*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="ea8d6-167">Šis laukas apibrėžia minimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="ea8d6-168">**Minimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="ea8d6-169">**Galiojimo dienų diapazonas:** *0*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="ea8d6-170">*„Pirmas baigia galioti, pirmas išeina“ (FEFO) kriterijus:* Šis laukas apibrėžia maksimalų galiojimo datos pirmojo termino pabaigos skaičių tarp paketo, kuris yra sandėlyje ir šiuo metu gaunamo paketo.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="ea8d6-171">„FastTab“ skirtuke **Tiekimo šaltiniai** turite nurodyti tiekimo tipus, kurie galioja šiam šablonui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="ea8d6-172">Pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="ea8d6-173">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ea8d6-174">**Tiekimo šaltinis:** *Pirkimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="ea8d6-175">Darbo klasės kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-175">Create a work class</span></span>

1. <span data-ttu-id="ea8d6-176">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="ea8d6-177">Veiksmų srityje pasirinkite **Nauja** darbo klasės krovinio grupės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="ea8d6-178">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-178">Set the following values:</span></span>

    - <span data-ttu-id="ea8d6-179">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="ea8d6-180">**Aprašas:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="ea8d6-181">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="ea8d6-182">Darbo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-182">Create a work template</span></span>

1. <span data-ttu-id="ea8d6-183">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="ea8d6-184">Lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="ea8d6-185">Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="ea8d6-186">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-187">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ea8d6-188">**Darbo šablonas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="ea8d6-189">**Darbo šablono aprašas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="ea8d6-190">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="ea8d6-191">„FastTab” skirtuke **Išsami darbo šablono informacija** pasirinkite **Nauja** norėdami sukurti naują tinklelio eilutę.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ea8d6-192">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-193">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="ea8d6-194">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="ea8d6-195">Pasirinkite **Nauja** kitai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="ea8d6-196">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="ea8d6-197">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="ea8d6-198">Pasirinkite **Įrašyti** ir patvirtinkite, kad pasirinktas žymės langelis **Galiojantis** žymės langelis *51 prekių skirstymo* šablonui.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="ea8d6-199">Darbo klasės ir darbų tipų *Paėmimas* ir *Padėjimas* ID turi sutapti.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="ea8d6-200">Vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-200">Create location directives</span></span>

1. <span data-ttu-id="ea8d6-201">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ea8d6-202">Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="ea8d6-203">Veiksmų srityje pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="ea8d6-204">**SEekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ea8d6-205">**Pavadinimas:** *51 prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="ea8d6-206">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="ea8d6-207">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-207">**Site:** *5*</span></span>
    - <span data-ttu-id="ea8d6-208">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ea8d6-209">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="ea8d6-210">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ea8d6-211">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-212">**Pradinis kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="ea8d6-213">**Galutinis kiekis:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="ea8d6-214">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="ea8d6-215">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ea8d6-216">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-217">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="ea8d6-218">**Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="ea8d6-219">Pasirinkite **Įrašyti,** jei norite, kad atsirastų **Redaguoti užklausą** mygtukas **Vietos nurodymo veiksmų** įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="ea8d6-220">Norėdami atidaryti užklausų rengyklę, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="ea8d6-221">Skirtuke **Diapazonas** įsitikinkite, kad sukonfigūruotos šios dvi eilutės:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="ea8d6-222">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-222">Line 1:</span></span>

        - <span data-ttu-id="ea8d6-223">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="ea8d6-224">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="ea8d6-225">**Laukas:** *Sandėlis*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="ea8d6-226">**Kriterijai:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="ea8d6-227">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-227">Line 2:</span></span>

        - <span data-ttu-id="ea8d6-228">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="ea8d6-229">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="ea8d6-230">**Laukas:** *Vieta*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="ea8d6-231">**Kriterijai:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="ea8d6-232">Pasirinkite **Gerai** ir uždarykite užklausos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="ea8d6-233">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="ea8d6-234">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ea8d6-235">Kairiojoje srityje esančiame meniu elementų sąraše pasirinkite **Pirkimo padėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="ea8d6-236">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-236">Select **Edit**.</span></span>
1. <span data-ttu-id="ea8d6-237">„FastTab“ skirtuke **Darbo klasės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ea8d6-238">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-239">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="ea8d6-240">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="ea8d6-241">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="ea8d6-242">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="ea8d6-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="ea8d6-243">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-243">Create a purchase order</span></span>

<span data-ttu-id="ea8d6-244">Norėdami sukurti pirkimo užsakymą kaip tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="ea8d6-245">Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ea8d6-246">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ea8d6-247">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-248">**Tiekėjo paskyra:** *104*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="ea8d6-249">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ea8d6-250">Pasirinkite **Gerai** ir pasižymėkite užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="ea8d6-251">Nauja eilutė pridedama į „FastTab” skirtuką **Pirkimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="ea8d6-252">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-253">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ea8d6-254">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="ea8d6-255">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="ea8d6-255">Create a sales order</span></span>

<span data-ttu-id="ea8d6-256">Norėdami sukurti pardavimo užsakymą kaip paklausos tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="ea8d6-257">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ea8d6-258">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ea8d6-259">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-260">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="ea8d6-261">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="ea8d6-262">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-262">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-263">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ea8d6-264">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="ea8d6-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="ea8d6-265">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="ea8d6-266">**Kiekis:** *3*</span><span class="sxs-lookup"><span data-stu-id="ea8d6-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="ea8d6-267">Suplanuoto prekių skirstymo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-267">Create planned cross-docking</span></span>

<span data-ttu-id="ea8d6-268">Atlikite šiuos veiksmus, norėdami sukurti suplanuotą prekių skirstymo iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="ea8d6-269">Puslapyje **Pardavimo užsakymo išsami informacija** Jūsų sukurtam pardavimo užsakymui veiksmų srities **Sandėlio** skirtuko grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ea8d6-270">Išleidimo į sandėlio veiksmas sukuria pardavimo užsakymo siuntos ir krovinio eilutę pardavimo užsakymas ir bando paskirstyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="ea8d6-271">Jūs gausite informacinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-271">You receive an informational message.</span></span> <span data-ttu-id="ea8d6-272">Taip pat gausite tokį įspėjamąjį pranešimą: „Bangai XXXX nebuvo sukurtas joks darbas“.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="ea8d6-273">Dėl išsamesnės informacijos žr. darbo kūrimo retrospektyvos žurnale.“</span><span class="sxs-lookup"><span data-stu-id="ea8d6-273">See the work creation history log for details."</span></span> <span data-ttu-id="ea8d6-274">Taip nutinka, nes sandėlyje nėra atsargų.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="ea8d6-275">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Sandėlis** pasirinkite **Išsami siuntimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="ea8d6-276">Pasirodys puslapis **Išsami siuntimo informacija** ir parodys pardavimo užsakymui sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="ea8d6-277">„FastTab“ skirtuke **Krovinio eilutės** atkreipkite dėmesį, kad **Suplanuoto prekių skirstymo kiekio** laukas nustatytas kaip *3*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="ea8d6-278">Kadangi sandėlyje nėra pasiekiamų atsargų, bet tinkamas tiekimo šaltinis bus gautas per laiko langą, nurodytą prekių skirstymo šablone, kuriame buvo sukurtas prekių skirstymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="ea8d6-279">„FastTab“ skirtuke **Krovinio eilutės** pasirinkite **Suplanuotas prekių skirstymas** peržiūrėti išsamią sukurto prekių skirstymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="ea8d6-280">Prekių skirstymo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="ea8d6-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="ea8d6-281">Pirkimo užsakymas „Warehousing“ programėlėje</span><span class="sxs-lookup"><span data-stu-id="ea8d6-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="ea8d6-282">Sistema gaus 5 kiekį iš pirkimo užsakymo į gavimo vietą ir sukurs du darbo vienetus.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="ea8d6-283">Pirmoji sukurta darbo ID yra **Darbo užsakymo tipo** *Prekių skirstymo* reikšmė, susieta su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="ea8d6-284">Ji turi 3 kiekį ir yra nukreipta į galutinę siuntimo vietą, kad ją būtų galima išsiųsti nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="ea8d6-285">Antroji sukurta darbo ID yra **Darbo užsakymo tipo** *Pirkimo užsakymas* reikšmė, susieta su pirkimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="ea8d6-286">Jos likęs kiekis yra 2, jis nebuvo perkrautas ir nukreiptas į padėjimo į saugyklą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="ea8d6-287">Prisijunkite kaip mobiliojo įrenginio vartotojas sandėlyje *51*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="ea8d6-288">Eikite į **Gavimas \> Pirkimo gavimą**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="ea8d6-289">Lauke **PU numeris** įveskite savo pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="ea8d6-290">Lauke **Kiekis** įveskite *5*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="ea8d6-291">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-291">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-292">Kitame puslapyje nustatykite lauką **Prekė** į *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="ea8d6-293">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-293">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-294">Kitame puslapyje patvirtinkite **PU numerio**, **Prekės** ir **Kiekio** reikšmes pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="ea8d6-295">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="ea8d6-296">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="ea8d6-297">Atsargų padėjimas prekių skirstyme ir krovinyje</span><span class="sxs-lookup"><span data-stu-id="ea8d6-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="ea8d6-298">Šiuo metu abejos darbo ID turi vienodas tikslines numerio lentelės.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="ea8d6-299">Norėdami atlikti kitus veiksmus, turite gauti darbo ID ir tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="ea8d6-300">Tai galite sužinoti iš išsamios pirkimo ir pardavimo užsakymų eilučių darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="ea8d6-301">Taip pat galite pereiti prie **Sandėlio valdymas \> Darbas \> Išsami darbo informacija** ir filtruoti darbą, kurio **Sandėlio** reikšmė yra *51*.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="ea8d6-302">Mobiliajame įrenginyje eikite į **Gavimas \> Pirkimo padėjimas** ir įveskite tikslinę darbo numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="ea8d6-303">Lauke **ID** įveskite tikslinės numerio lentelės ID iš darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="ea8d6-304">Prekių skirstymo paėmimo puslapyje pateikiama paėmimo vieta (*RECV*), tikslinė numerio lentelė (*numerio lentelė*), prekė (*A0001*) ir kiekis (*3*).</span><span class="sxs-lookup"><span data-stu-id="ea8d6-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="ea8d6-305">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-305">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-306">Lauke **Tikslinė LP** įveskite tikslinės numerio lentelės ID, kuri turi būti įtraukta (perskirstyta) į siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="ea8d6-307">Galite pasirinkti bet kurį savo pasirinktą numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="ea8d6-308">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-308">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-309">Kito puslapio lauke **ID** įveskite tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="ea8d6-310">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-310">Select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-311">Patvirtinkite paėmimo darbą, kad būtų galima paimti likusį 2 kiekį ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="ea8d6-312">Kitame puslapyje pasirinkite **Atlikta** užbaigti paėmimo procesą ir pradėti padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="ea8d6-313">Mobiliųjų įrenginių programėlė pateikia Jums vietą ir numerio lentelę, į kurias galima įtraukti prekę.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="ea8d6-314">Patvirtinkite krovinio **Padėjimo** saugyklą pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="ea8d6-315">Kitame puslapyje patvirtinkite prekių skirstymo **Padėjimą** pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="ea8d6-316">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="ea8d6-317">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="ea8d6-318">Toliau pateiktoje iliustracijoje rodoma, kaip atliktas prekių skirstymas gali atrodyti „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="ea8d6-319">![Atliktas prekių skirstymas](media/PlannedCrossDockingWork.png "Atliktas prekių skirstymas")</span><span class="sxs-lookup"><span data-stu-id="ea8d6-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]