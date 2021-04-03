---
title: Suplanuotas prekių skirstymas
description: Šioje temoje aprašoma Išplėstinis suplanuoto prekių skirstymas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis. Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 722b004e607cb2e6b7de292d92b67b18c2024696
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556271"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="4d5b5-104">Suplanuotas prekių skirstymas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d5b5-105">Šioje temoje aprašomas išplėstini suplanuotas prekių skirstymą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="4d5b5-106">Išplėstinis suplanuoto prekių skirstymas yra sandėlio procesas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="4d5b5-107">Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="4d5b5-108">Suplanuoto prekių skirstymo darbuotojai gali praleisti gaunamų atsargų padėjimus ir siunčiamų prekių paėmimus, jau pažymėti siunčiamam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="4d5b5-109">Todėl kartai, kuomet atsargos yra paimamos yra minimalizuoti, jei įmanoma.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="4d5b5-110">Taip pat dėl mažesnės sąveikos su sistema, laiko ir vietos taupymas sandėlio darbo aukšte yra padidinami.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="4d5b5-111">Prieš paleidžiant suplanuotą prekių skirstymą, vartotojas turi konfigūruoti naują prekių skirstymo šabloną, kur nurodytas tiekimo šaltinis ir kiti prekių skirstymo reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="4d5b5-112">Kadangi siuntimo užsakymas sukuriamas, eilutė turi būti pažymėta pagal gavimo užsakymą, kuriame yra ta prekė.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="4d5b5-113">Gaunamo užsakymo gavimo metu, prekių skirstymo nustatymas automatiškai identifikuoja prekių skirstymo poreikius ir sukuria reikiamo kiekio perkėlimo darbą, pagrįstą vietos nurodymo nustatymu.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5b5-114">Atsargų operacijos yra **ne** registruojamos atšaukus prekių skirstymo darbą, net jei šios galimybės nustatymas yra įjungtas sandėlio valdymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="4d5b5-115">Įjungti suplanuoto prekių skirstymo funkcijas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="4d5b5-116">Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir toliau pateikiama tvarka įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="4d5b5-117">*Suplanuotas prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="4d5b5-118">*Prekių skirstymo šablonai su vietovės nurodymais*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="4d5b5-119">Sąranka</span><span class="sxs-lookup"><span data-stu-id="4d5b5-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="4d5b5-120">Pakartotinai generuoti krovinio registravimo metodus</span><span class="sxs-lookup"><span data-stu-id="4d5b5-120">Regenerate load posting methods</span></span>

<span data-ttu-id="4d5b5-121">Suplanuotas prekių skirstymas yra įgyvendinamas kaip krovinio registravimo metodas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="4d5b5-122">Įjungę funkciją, turite pakartotinai generuoti metodus.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="4d5b5-123">Eikite į **Sandėlio valdymas \> Nustatymas \> Krovinio registravimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="4d5b5-124">Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="4d5b5-125">Baigus pakartotinį generavimą , turėtumėte matyti metodą, kurio **Metodo pavadinimas** yra *Planuoti prekių skirstymą*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="4d5b5-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="4d5b5-127">Sukurkite prekių skirstymo šabloną</span><span class="sxs-lookup"><span data-stu-id="4d5b5-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="4d5b5-128">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Prekių skirstymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="4d5b5-129">Veiksmų srityje pasirinkite **Nauja** šablonui sukurti.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="4d5b5-130">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-131">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="4d5b5-132">Šis laukas nurodo tvarką, kuria yra vertinami šablonai.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="4d5b5-133">**Prekių skirstymo šablono ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="4d5b5-134">**Aprašas:** *Sandėlis 51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="4d5b5-135">**Paklausos išleidimo strategija:** *Prieš tiekimo kvitą*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="4d5b5-136">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d5b5-137">„FastTab“ nustatymas **Planavimas** kontroliuoja, kaip veikia šablonas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="4d5b5-138">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-138">Set the following values:</span></span>

    - <span data-ttu-id="4d5b5-139">**Paklausos reikalavimai:** *Nėra*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="4d5b5-140">Šiame lauke apibrėžiami atsargų paklausos reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="4d5b5-141">Jei paklausa turi būti susieta su tiekimu prieš išleidimą, pasirinkite *Žymėjimas*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="4d5b5-142">Jei paklausa turi būti užsakymas, rezervuotas pagal tiekimą prieš išleidžiant, pasirinkite *Užsakymo rezervavimas*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="4d5b5-143">**Vietos tipas:** *Siuntimo vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="4d5b5-144">Šiame lauke nurodoma, ar prekių skirstymas turi naudoti surinkimo/krovinio vietas iš siuntimo, ar reikia naudoti vietos nurodymus, kad būtų galima rasti surinkimo/krovinio vietas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="4d5b5-145">**Darbo šablonas** – Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="4d5b5-146">Šiame lauke apibrėžiamas darbo šablonas, kurį reikia naudoti, kai sukuriamas prekių skirstymo darbas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="4d5b5-147">**Iš naujo patikrinti tiekimo kvitą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="4d5b5-148">Ši pasirinktis nurodo, ar turi būti iš naujo patikrinta pasiūla gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="4d5b5-149">Jei ši pasirinktis nustatyta kaip *Taip,* tikrinamas ir maksimalus laiko langą, ir galiojimo dienų intervalas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="4d5b5-150">**Nurodymo kodas:** palikite šį lauką tuščią</span><span class="sxs-lookup"><span data-stu-id="4d5b5-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="4d5b5-151">Ši parinktis įgalina sistemą naudoti vietos nurodymus, kad padėtų nustatyti geriausią vietą, į kurią bus perkeliamos prekių skirstymo atsargos.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="4d5b5-152">Galite ją nustatyti, priskirdami nurodymo kodą kiekvienam susijusiam prekių skirstymo šablonui.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="4d5b5-153">Kiekvienas nurodymo kodas identifikuoja unikalų vietos nurodymą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="4d5b5-154">**Patikrinti laiko langą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="4d5b5-155">Ši pasirinktis nurodo, ar maksimalaus laiko langas turi būti įvertintas, kai pasirinktas tiekimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="4d5b5-156">Jei ši pasirinktis nustatyta kaip *Taip*, laukai, susiję su maksimalaus ir minimalaus laiko langais, bus prieinami.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="4d5b5-157">**Maksimalus laiko langais:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="4d5b5-158">Šis laukas apibrėžia maksimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="4d5b5-159">**Maksimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="4d5b5-160">**Minimalus laiko langas:** *0*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="4d5b5-161">Šis laukas apibrėžia minimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="4d5b5-162">**Minimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="4d5b5-163">**Galiojimo dienų diapazpnas:** *0*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="4d5b5-164">*„Pirmas baigia galioti, pirmas išeina“ (FEFO) kriterijus:* Šis laukas apibrėžia maksimalų galiojimo datos pirmojo termino pabaigos skaičių tarp paketo, kuris yra sandėlyje ir šiuo metu gaunamo paketo.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="4d5b5-165">„FastTab“ skirtuke **Tiekimo šaltiniai** turite nurodyti tiekimo tipus, kurie galioja šiam šablonui.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="4d5b5-166">Pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4d5b5-167">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d5b5-168">**Tiekimo šaltinis:** *Pirkimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="4d5b5-169">Darbo klasės kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-169">Create a work class</span></span>

1. <span data-ttu-id="4d5b5-170">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="4d5b5-171">Veiksmų srityje pasirinkite **Nauja** darbo klasės krovinio grupės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="4d5b5-172">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-172">Set the following values:</span></span>

    - <span data-ttu-id="4d5b5-173">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="4d5b5-174">**Aprašas:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="4d5b5-175">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="4d5b5-176">Darbo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-176">Create a work template</span></span>

1. <span data-ttu-id="4d5b5-177">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4d5b5-178">Lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="4d5b5-179">Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="4d5b5-180">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-181">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d5b5-182">**Darbo šablonas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="4d5b5-183">**Darbo šablono aprašas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="4d5b5-184">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="4d5b5-185">„FastTab” skirtuke **Išsami darbo šablono informacija** pasirinkite **Nauja** norėdami sukurti naują tinklelio eilutę.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d5b5-186">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-187">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="4d5b5-188">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="4d5b5-189">Pasirinkite **Nauja** kitai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="4d5b5-190">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4d5b5-191">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="4d5b5-192">Pasirinkite **Įrašyti** ir patvirtinkite, kad pasirinktas žymės langelis **Galiojantis** žymės langelis *51 prekių skirstymo* šablonui.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5b5-193">Darbo klasės ir darbų tipų *Paėmimas* ir *Padėjimas* ID turi sutapti.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="4d5b5-194">Vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-194">Create location directives</span></span>

1. <span data-ttu-id="4d5b5-195">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4d5b5-196">Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="4d5b5-197">Veiksmų srityje pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="4d5b5-198">**SEekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4d5b5-199">**Pavadinimas:** *51 prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="4d5b5-200">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="4d5b5-201">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-201">**Site:** *5*</span></span>
    - <span data-ttu-id="4d5b5-202">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d5b5-203">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="4d5b5-204">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d5b5-205">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-206">**Pradinis kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="4d5b5-207">**Galutinis kiekis:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="4d5b5-208">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="4d5b5-209">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d5b5-210">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-211">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="4d5b5-212">**Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="4d5b5-213">Pasirinkite **Įrašyti,** jei norite, kad atsirastų **Redaguoti užklausą** mygtukas **Vietos nurdymo veiksmų** įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="4d5b5-214">Norėdami atidaryti užklausų rengyklę, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="4d5b5-215">Skirtuke **Diapazonas** įsitikinkite, kad sukonfigūruotos šios dvi eilutės:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="4d5b5-216">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-216">Line 1:</span></span>

        - <span data-ttu-id="4d5b5-217">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="4d5b5-218">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="4d5b5-219">**Laukas:** *Sandėlis*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="4d5b5-220">**Kriterijai:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="4d5b5-221">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-221">Line 2:</span></span>

        - <span data-ttu-id="4d5b5-222">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="4d5b5-223">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="4d5b5-224">**Laukas:** *Vieta*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="4d5b5-225">**Kriterijai:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="4d5b5-226">Pasirinkite **Gerai** ir uždarykite užklausos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="4d5b5-227">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="4d5b5-228">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4d5b5-229">Kairiojoje srityje esančiame meniu elementų sąraše pasirinkite **Pirkimo padėjimas**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="4d5b5-230">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-230">Select **Edit**.</span></span>
1. <span data-ttu-id="4d5b5-231">„FastTab“ skirtuke **Darbo klasės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4d5b5-232">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-233">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="4d5b5-234">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="4d5b5-235">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="4d5b5-236">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="4d5b5-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="4d5b5-237">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-237">Create a purchase order</span></span>

<span data-ttu-id="4d5b5-238">Norėdami sukurti pirkimo užsakymą kaip tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="4d5b5-239">Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="4d5b5-240">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4d5b5-241">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-242">**Tiekėjo paskyra:** *104*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="4d5b5-243">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d5b5-244">Pasirinkite **Gerai** ir pasižymėkite užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="4d5b5-245">Nauja eilutė pridedama į „FastTab” skirtuką **Pirkimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="4d5b5-246">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-247">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4d5b5-248">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="4d5b5-249">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="4d5b5-249">Create a sales order</span></span>

<span data-ttu-id="4d5b5-250">Norėdami sukurti pardavimo užsakymą kaip paklausos tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="4d5b5-251">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4d5b5-252">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4d5b5-253">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-254">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="4d5b5-255">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="4d5b5-256">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-256">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-257">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4d5b5-258">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d5b5-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d5b5-259">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4d5b5-260">**Kiekis:** *3*</span><span class="sxs-lookup"><span data-stu-id="4d5b5-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="4d5b5-261">Suplanuoto prekių skirstymo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-261">Create planned cross-docking</span></span>

<span data-ttu-id="4d5b5-262">Atlikite šiuos veiksmus, norėdami sukurti suplanuotą prekių skirstymo iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="4d5b5-263">Puslapyje **Pardavimo užsakymo išsami informacija** Jūsų sukurtam pardavimo užsakymui veiksmų srities **Sandėlio** skirtuko grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4d5b5-264">Išleidimo į sandėlio veiksmas sukuria pardavimo užsakymo siuntos ir krovinio eilutę pardavimo užsakymas ir bando paskirstyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="4d5b5-265">Jūs gausite informacinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-265">You receive an informational message.</span></span> <span data-ttu-id="4d5b5-266">Taip pat gausite tokį įspėjamąjį pranešimą: „Bangai XXXX nebuvo sukurtas joks darbas“.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="4d5b5-267">Dėl išsamesnės informacijos žr. darbo kūrimo retrospektyvos žurnale.“</span><span class="sxs-lookup"><span data-stu-id="4d5b5-267">See the work creation history log for details."</span></span> <span data-ttu-id="4d5b5-268">Taip nutinka, nes sandėlyje nėra atsargų.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="4d5b5-269">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Sandėlis** pasirinkite **Išsami siuntimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="4d5b5-270">Pasirodys puslapis **Išsami siuntimo informacija** ir parodys pardavimo užsakymui sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="4d5b5-271">„FastTab“ skirtuke **Krovinio eilutės** atkreipkite dėmesį, kad **Suplanuoto prekių skirstymo kiekio** laukas nustatytas kaip *3*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="4d5b5-272">Kadangi sandėlyje nėra pasiekiamų atsargų, bet tinkamas tiekimo šaltinis bus gautas per laiko langą, nurodytą prekių skirstymo šablone, kuriame buvo sukurtas prekių skirstymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="4d5b5-273">„FastTab“ skirtuke **Krovinio eilutės** pasirinkite **Suplanuotas prekių skirstymas** peržiūrėti išsamią sukurto prekių skirstymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="4d5b5-274">Prekių skirstymo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4d5b5-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="4d5b5-275">Pirkimo užsakymas „Warehousing“ programėlėje</span><span class="sxs-lookup"><span data-stu-id="4d5b5-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="4d5b5-276">Sistema gaus 5 kiekį iš pirkimo užsakymo į gavimo vietą ir sukurs du darbo vienetus.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="4d5b5-277">Pirmoji sukurta darbo ID yra **Darbo užsakymo tipo** *Prekių skirstymo* reikšmė, susieta su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="4d5b5-278">Ji turi 3 kiekį ir yra nukreipta į galutinę siuntimo vietą, kad ją būtų galima išsiųsti nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="4d5b5-279">Antroji sukurta darbo ID yra **Darbo užsakymo tipo** *Pirkimo užsakymas* reikšmė, susieta su pirkimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="4d5b5-280">Jos likęs kiekis yra 2, jis nebuvo perkrautas ir nukreiptas į padėjimo į saugyklą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="4d5b5-281">Prisijunkite kaip mobiliojo įrenginio vartotojas sandėlyje *51*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="4d5b5-282">Eikite į **Gavimas \> Pirkimo gavimą**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="4d5b5-283">Lauke **PU numeris** įveskite savo pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="4d5b5-284">Lauke **Kiekis** įveskite *5*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="4d5b5-285">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-285">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-286">Kitame puslapyje nustatykite lauką **Prekė** į *A0001*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="4d5b5-287">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-287">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-288">Kitame puslapyje patvirtinkite **PU numerio**, **Prekės** ir **Kiekio** reikšmes pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="4d5b5-289">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4d5b5-290">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="4d5b5-291">Atsargų padėjimas prekių skirstyme ir krovinyje</span><span class="sxs-lookup"><span data-stu-id="4d5b5-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="4d5b5-292">Šiuo metu abejos darbo ID turi vienodas tikslines numerio lentelės.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="4d5b5-293">Norėdami atlikti kitus veiksmus, turite gauti darbo ID ir tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="4d5b5-294">Tai galite sužinoti iš išsamios pirkimo ir pardavimo užsakymų eilučių darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="4d5b5-295">Taip pat galite pereiti prie **Sandėlio valdymas \> Darbas \> Išsami darbo informacija** ir filtruoti darbą, kurio **Sandėlio** reikšmė yra *51*.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="4d5b5-296">Mobiliajame įrenginyje eikite į **Gavimas \> Pirkimo padėjimas** ir įveskite tikslinę darbo numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="4d5b5-297">Lauke **ID** įveskite tikslinės numerio lentelės ID iš darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="4d5b5-298">Prekių skirstymo paėmimo puslapyje pateikiama paėmimo vieta (*RECV*), tikslinė numerio lentelė (*numerio lentelė*), prekė (*A0001*) ir kiekis (*3*).</span><span class="sxs-lookup"><span data-stu-id="4d5b5-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="4d5b5-299">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-299">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-300">Lauke **Tikslinė LP** įveskite tikslinės numerio lentelės ID, kuri turi būti įtraukta (perskirstyta) į siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="4d5b5-301">Galite pasirinkti bet kurį savo pasirinktą numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="4d5b5-302">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-302">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-303">Kito puslapio lauke **ID** įveskite tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="4d5b5-304">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-304">Select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-305">Patvirtinkite paėmimo darbą, kad būtų galima paimti likusį 2 kiekį ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="4d5b5-306">Kitame puslapyje pasirinkite **Atlikta** užbaigti paėmimo procesą ir pradėti padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="4d5b5-307">Mobiliųjų įrenginių programėlė pateikia Jums vietą ir numerio lentelę, į kurias galima įtraukti prekę.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="4d5b5-308">Patvirtinkite krovinio **Padėjimo** saugyklą pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="4d5b5-309">Kitame puslapyje patvirtinkite prekių skirstymo **Padėjimą** pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="4d5b5-310">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4d5b5-311">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="4d5b5-312">Toliau pateiktoje iliustracijoje rodoma, kaip atliktas prekių skirstymas gali atrodyti „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="4d5b5-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4d5b5-313">![Atliktas prekių skirstymas](media/PlannedCrossDockingWork.png "Atliktas prekių skirstymas")</span><span class="sxs-lookup"><span data-stu-id="4d5b5-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]