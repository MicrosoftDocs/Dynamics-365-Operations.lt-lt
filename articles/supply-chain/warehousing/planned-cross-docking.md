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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433993"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="902a3-104">Suplanuotas prekių skirstymas</span><span class="sxs-lookup"><span data-stu-id="902a3-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="902a3-105">Šioje temoje aprašomas išplėstini suplanuotas prekių skirstymą.</span><span class="sxs-lookup"><span data-stu-id="902a3-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="902a3-106">Išplėstinis suplanuoto prekių skirstymas yra sandėlio procesas, kai atsargų kiekis, reikalingas užsakymui yra nukreipiamas tiesiai iš gavimo arba sukuriama į teisinga pakrovimo rampa arba išdėstymo sritis.</span><span class="sxs-lookup"><span data-stu-id="902a3-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="902a3-107">Visos likusios atsargos iš gavimo šaltinių yra nukreipiamos į teisingą saugojimo vietą naudojant įprastą padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="902a3-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="902a3-108">Suplanuoto prekių skirstymo darbuotojai gali praleisti gaunamų atsargų padėjimus ir siunčiamų prekių paėmimus, jau pažymėti siunčiamam užsakymui.</span><span class="sxs-lookup"><span data-stu-id="902a3-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="902a3-109">Todėl kartai, kuomet atsargos yra paimamos yra minimalizuoti, jei įmanoma.</span><span class="sxs-lookup"><span data-stu-id="902a3-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="902a3-110">Taip pat dėl mažesnės sąveikos su sistema, laiko ir vietos taupymas sandėlio darbo aukšte yra padidinami.</span><span class="sxs-lookup"><span data-stu-id="902a3-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="902a3-111">Prieš paleidžiant suplanuotą prekių skirstymą, vartotojas turi konfigūruoti naują prekių skirstymo šabloną, kur nurodytas tiekimo šaltinis ir kiti prekių skirstymo reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="902a3-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="902a3-112">Kadangi siuntimo užsakymas sukuriamas, eilutė turi būti pažymėta pagal gavimo užsakymą, kuriame yra ta prekė.</span><span class="sxs-lookup"><span data-stu-id="902a3-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="902a3-113">Gaunamo užsakymo gavimo metu, prekių skirstymo nustatymas automatiškai identifikuoja prekių skirstymo poreikius ir sukuria reikiamo kiekio perkėlimo darbą, pagrįstą vietos nurodymo nustatymu.</span><span class="sxs-lookup"><span data-stu-id="902a3-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="902a3-114">Atsargų operacijos yra **ne** registruojamos atšaukus prekių skirstymo darbą, net jei šios galimybės nustatymas yra įjungtas sandėlio valdymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="902a3-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="902a3-115">Įjungti suplanuoto prekių skirstymo funkciją</span><span class="sxs-lookup"><span data-stu-id="902a3-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="902a3-116">Norėdami naudoti išplėstinę prekių skirstymo funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="902a3-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="902a3-117">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="902a3-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="902a3-118">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="902a3-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="902a3-119">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="902a3-120">**Funkcijos pavadinimas:** *Suplanuotas prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="902a3-121">Sąranka</span><span class="sxs-lookup"><span data-stu-id="902a3-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="902a3-122">Pakartotinai generuoti krovinio registravimo metodus</span><span class="sxs-lookup"><span data-stu-id="902a3-122">Regenerate load posting methods</span></span>

<span data-ttu-id="902a3-123">Suplanuotas prekių skirstymas yra įgyvendinamas kaip krovinio registravimo metodas.</span><span class="sxs-lookup"><span data-stu-id="902a3-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="902a3-124">Įjungę funkciją, turite pakartotinai generuoti metodus.</span><span class="sxs-lookup"><span data-stu-id="902a3-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="902a3-125">Eikite į **Sandėlio valdymas \> Nustatymas \> Krovinio registravimo metodai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="902a3-126">Veiksmų srityje spustelėkite **Pakartotinai generuoti metodus**.</span><span class="sxs-lookup"><span data-stu-id="902a3-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="902a3-127">Baigus pakartotinį generavimą , turėtumėte matyti metodą, kurio **Metodo pavadinimas** yra *Planuoti prekių skirstymą*.</span><span class="sxs-lookup"><span data-stu-id="902a3-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="902a3-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="902a3-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="902a3-129">Sukurkite prekių skirstymo šabloną</span><span class="sxs-lookup"><span data-stu-id="902a3-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="902a3-130">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Prekių skirstymo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="902a3-131">Veiksmų srityje pasirinkite **Nauja** šablonui sukurti.</span><span class="sxs-lookup"><span data-stu-id="902a3-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="902a3-132">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="902a3-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="902a3-133">**Seka:** *1*</span><span class="sxs-lookup"><span data-stu-id="902a3-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="902a3-134">Šis laukas nurodo tvarką, kuria yra vertinami šablonai.</span><span class="sxs-lookup"><span data-stu-id="902a3-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="902a3-135">**Prekių skirstymo šablono ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="902a3-136">**Aprašas:** *Sandėlis 51*</span><span class="sxs-lookup"><span data-stu-id="902a3-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="902a3-137">**Paklausos išleidimo strategija:** *Prieš tiekimo kvitą*</span><span class="sxs-lookup"><span data-stu-id="902a3-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="902a3-138">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="902a3-139">„FastTab“ nustatymas **Planavimas** kontroliuoja, kaip veikia šablonas.</span><span class="sxs-lookup"><span data-stu-id="902a3-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="902a3-140">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="902a3-140">Set the following values:</span></span>

    - <span data-ttu-id="902a3-141">**Paklausos reikalavimai:** *Nėra*</span><span class="sxs-lookup"><span data-stu-id="902a3-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="902a3-142">Šiame lauke apibrėžiami atsargų paklausos reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="902a3-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="902a3-143">Jei paklausa turi būti susieta su tiekimu prieš išleidimą, pasirinkite *Žymėjimas*.</span><span class="sxs-lookup"><span data-stu-id="902a3-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="902a3-144">Jei paklausa turi būti užsakymas, rezervuotas pagal tiekimą prieš išleidžiant, pasirinkite *Užsakymo rezervavimas*.</span><span class="sxs-lookup"><span data-stu-id="902a3-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="902a3-145">**Vietos tipas:** *Siuntimo vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="902a3-146">Šiame lauke nurodoma, ar prekių skirstymas turi naudoti surinkimo/krovinio vietas iš siuntimo, ar reikia naudoti vietos nurodymus, kad būtų galima rasti surinkimo/krovinio vietas.</span><span class="sxs-lookup"><span data-stu-id="902a3-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="902a3-147">**Darbo šablonas** – Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="902a3-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="902a3-148">Šiame lauke apibrėžiamas darbo šablonas, kurį reikia naudoti, kai sukuriamas prekių skirstymo darbas.</span><span class="sxs-lookup"><span data-stu-id="902a3-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="902a3-149">**Iš naujo patikrinti tiekimo kvitą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="902a3-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="902a3-150">Ši pasirinktis nurodo, ar turi būti iš naujo patikrinta pasiūla gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="902a3-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="902a3-151">Jei ši pasirinktis nustatyta kaip *Taip,* tikrinamas ir maksimalus laiko langą, ir galiojimo dienų intervalas.</span><span class="sxs-lookup"><span data-stu-id="902a3-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="902a3-152">**Patikrinti laiko langą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="902a3-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="902a3-153">Ši pasirinktis nurodo, ar maksimalaus laiko langas turi būti įvertintas, kai pasirinktas tiekimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="902a3-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="902a3-154">Jei ši pasirinktis nustatyta kaip *Taip*, laukai, susiję su maksimalaus ir minimalaus laiko langais, bus prieinami.</span><span class="sxs-lookup"><span data-stu-id="902a3-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="902a3-155">**Maksimalus laiko langais:** *5*</span><span class="sxs-lookup"><span data-stu-id="902a3-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="902a3-156">Šis laukas apibrėžia maksimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="902a3-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="902a3-157">**Maksimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="902a3-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="902a3-158">**Minimalus laiko langas:** *0*</span><span class="sxs-lookup"><span data-stu-id="902a3-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="902a3-159">Šis laukas apibrėžia minimalų leidžiamą laikotarpį tarp tiekiamų prekių atvykimo ir reikiamų prekių išvykimo.</span><span class="sxs-lookup"><span data-stu-id="902a3-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="902a3-160">**Minimalaus laiko lango vienetas:** *Dienos*</span><span class="sxs-lookup"><span data-stu-id="902a3-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="902a3-161">**Galiojimo dienų diapazpnas:** *0*</span><span class="sxs-lookup"><span data-stu-id="902a3-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="902a3-162">*„Pirmas baigia galioti, pirmas išeina“ (FEFO) kriterijus:* Šis laukas apibrėžia maksimalų galiojimo datos pirmojo termino pabaigos skaičių tarp paketo, kuris yra sandėlyje ir šiuo metu gaunamo paketo.</span><span class="sxs-lookup"><span data-stu-id="902a3-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="902a3-163">„FastTab“ skirtuke **Tiekimo šaltiniai** turite nurodyti tiekimo tipus, kurie galioja šiam šablonui.</span><span class="sxs-lookup"><span data-stu-id="902a3-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="902a3-164">Pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="902a3-165">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="902a3-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="902a3-166">**Tiekimo šaltinis:** *Pirkimo užsakymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="902a3-167">Darbo klasės kūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-167">Create a work class</span></span>

1. <span data-ttu-id="902a3-168">Eikite į **Sandėlio valdymas \> Nustatymas \> Darbas \> Darbo klasės**.</span><span class="sxs-lookup"><span data-stu-id="902a3-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="902a3-169">Veiksmų srityje pasirinkite **Nauja** darbo klasės krovinio grupės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="902a3-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="902a3-170">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="902a3-170">Set the following values:</span></span>

    - <span data-ttu-id="902a3-171">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="902a3-172">**Aprašas:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="902a3-173">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="902a3-174">Darbo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-174">Create a work template</span></span>

1. <span data-ttu-id="902a3-175">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="902a3-176">Lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="902a3-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="902a3-177">Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="902a3-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="902a3-178">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="902a3-179">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="902a3-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="902a3-180">**Darbo šablonas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="902a3-181">**Darbo šablono aprašas** *51 Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="902a3-182">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Darbo šablono išsami informacija** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="902a3-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="902a3-183">„FastTab” skirtuke **Išsami darbo šablono informacija** pasirinkite **Nauja** norėdami sukurti naują tinklelio eilutę.</span><span class="sxs-lookup"><span data-stu-id="902a3-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="902a3-184">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="902a3-185">**Darbo tipas:** *Paėmimas*</span><span class="sxs-lookup"><span data-stu-id="902a3-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="902a3-186">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="902a3-187">Pasirinkite **Nauja** kitai eilutei įtraukti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="902a3-188">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="902a3-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="902a3-189">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="902a3-190">Pasirinkite **Įrašyti** ir patvirtinkite, kad pasirinktas žymės langelis **Galiojantis** žymės langelis *51 prekių skirstymo* šablonui.</span><span class="sxs-lookup"><span data-stu-id="902a3-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="902a3-191">Darbo klasės ir darbų tipų *Paėmimas* ir *Padėjimas* ID turi sutapti.</span><span class="sxs-lookup"><span data-stu-id="902a3-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="902a3-192">Vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-192">Create location directives</span></span>

1. <span data-ttu-id="902a3-193">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="902a3-194">Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į *Prekių skirstymas*.</span><span class="sxs-lookup"><span data-stu-id="902a3-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="902a3-195">Veiksmų srityje pasirinkite **Nauja** ir tada nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="902a3-196">**SEekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="902a3-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="902a3-197">**Pavadinimas:** *51 prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="902a3-198">**Darbo tipas:** *Padėjimas*</span><span class="sxs-lookup"><span data-stu-id="902a3-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="902a3-199">**Vieta:** *5*</span><span class="sxs-lookup"><span data-stu-id="902a3-199">**Site:** *5*</span></span>
    - <span data-ttu-id="902a3-200">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="902a3-201">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="902a3-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="902a3-202">„FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="902a3-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="902a3-203">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="902a3-204">**Pradinis kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="902a3-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="902a3-205">**Galutinis kiekis:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="902a3-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="902a3-206">Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="902a3-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="902a3-207">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="902a3-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="902a3-208">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="902a3-209">**Pavadinimas:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="902a3-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="902a3-210">**Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="902a3-211">Pasirinkite **Įrašyti,** jei norite, kad atsirastų **Redaguoti užklausą** mygtukas **Vietos nurdymo veiksmų** įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="902a3-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="902a3-212">Norėdami atidaryti užklausų rengyklę, pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="902a3-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="902a3-213">Skirtuke **Diapazonas** įsitikinkite, kad sukonfigūruotos šios dvi eilutės:</span><span class="sxs-lookup"><span data-stu-id="902a3-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="902a3-214">Eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="902a3-214">Line 1:</span></span>

        - <span data-ttu-id="902a3-215">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="902a3-216">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="902a3-217">**Laukas:** *Sandėlis*</span><span class="sxs-lookup"><span data-stu-id="902a3-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="902a3-218">**Kriterijai:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="902a3-219">Eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="902a3-219">Line 2:</span></span>

        - <span data-ttu-id="902a3-220">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="902a3-221">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="902a3-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="902a3-222">**Laukas:** *Vieta*</span><span class="sxs-lookup"><span data-stu-id="902a3-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="902a3-223">**Kriterijai:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="902a3-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="902a3-224">Pasirinkite **Gerai** ir uždarykite užklausos rengyklę.</span><span class="sxs-lookup"><span data-stu-id="902a3-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="902a3-225">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="902a3-226">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="902a3-227">Kairiojoje srityje esančiame meniu elementų sąraše pasirinkite **Pirkimo padėjimas**.</span><span class="sxs-lookup"><span data-stu-id="902a3-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="902a3-228">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="902a3-228">Select **Edit**.</span></span>
1. <span data-ttu-id="902a3-229">„FastTab“ skirtuke **Darbo klasės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="902a3-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="902a3-230">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="902a3-231">**Darbo klasės ID:** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="902a3-232">**Darbo užsakymo tipas** *Prekių skirstymas*</span><span class="sxs-lookup"><span data-stu-id="902a3-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="902a3-233">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="902a3-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="902a3-234">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="902a3-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="902a3-235">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-235">Create a purchase order</span></span>

<span data-ttu-id="902a3-236">Norėdami sukurti pirkimo užsakymą kaip tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="902a3-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="902a3-237">Eikite į **Pirkimas ir tiekėjų parinkimas \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="902a3-238">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="902a3-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="902a3-239">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="902a3-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="902a3-240">**Tiekėjo paskyra:** *104*</span><span class="sxs-lookup"><span data-stu-id="902a3-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="902a3-241">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="902a3-242">Pasirinkite **Gerai** ir pasižymėkite užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="902a3-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="902a3-243">Nauja eilutė pridedama į „FastTab” skirtuką **Pirkimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="902a3-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="902a3-244">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="902a3-245">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="902a3-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="902a3-246">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="902a3-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="902a3-247">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="902a3-247">Create a sales order</span></span>

<span data-ttu-id="902a3-248">Norėdami sukurti pardavimo užsakymą kaip paklausos tiekimo šaltinį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="902a3-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="902a3-249">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="902a3-250">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="902a3-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="902a3-251">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="902a3-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="902a3-252">**Kliento sąskaita:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="902a3-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="902a3-253">**Sandėlis:** *51*</span><span class="sxs-lookup"><span data-stu-id="902a3-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="902a3-254">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-254">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-255">Nauja eilutė pridedama į „FastTab” skirtuką **Pardavimo užsakymo eilutės**.</span><span class="sxs-lookup"><span data-stu-id="902a3-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="902a3-256">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="902a3-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="902a3-257">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="902a3-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="902a3-258">**Kiekis:** *3*</span><span class="sxs-lookup"><span data-stu-id="902a3-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="902a3-259">Suplanuoto prekių skirstymo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="902a3-259">Create planned cross-docking</span></span>

<span data-ttu-id="902a3-260">Atlikite šiuos veiksmus, norėdami sukurti suplanuotą prekių skirstymo iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="902a3-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="902a3-261">Puslapyje **Pardavimo užsakymo išsami informacija** Jūsų sukurtam pardavimo užsakymui veiksmų srities **Sandėlio** skirtuko grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="902a3-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="902a3-262">Išleidimo į sandėlio veiksmas sukuria pardavimo užsakymo siuntos ir krovinio eilutę pardavimo užsakymas ir bando paskirstyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="902a3-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="902a3-263">Jūs gausite informacinį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="902a3-263">You receive an informational message.</span></span> <span data-ttu-id="902a3-264">Taip pat gausite tokį įspėjamąjį pranešimą: „Bangai XXXX nebuvo sukurtas joks darbas“.</span><span class="sxs-lookup"><span data-stu-id="902a3-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="902a3-265">Dėl išsamesnės informacijos žr. darbo kūrimo retrospektyvos žurnale.“</span><span class="sxs-lookup"><span data-stu-id="902a3-265">See the work creation history log for details."</span></span> <span data-ttu-id="902a3-266">Taip nutinka, nes sandėlyje nėra atsargų.</span><span class="sxs-lookup"><span data-stu-id="902a3-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="902a3-267">„FastTab“ skirtuke **Pardavimo užsakymo eilutės** meniu **Sandėlis** pasirinkite **Išsami siuntimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="902a3-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="902a3-268">Pasirodys puslapis **Išsami siuntimo informacija** ir parodys pardavimo užsakymui sukurtą darbą.</span><span class="sxs-lookup"><span data-stu-id="902a3-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="902a3-269">„FastTab“ skirtuke **Krovinio eilutės** atkreipkite dėmesį, kad **Suplanuoto prekių skirstymo kiekio** laukas nustatytas kaip *3*.</span><span class="sxs-lookup"><span data-stu-id="902a3-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="902a3-270">Kadangi sandėlyje nėra pasiekiamų atsargų, bet tinkamas tiekimo šaltinis bus gautas per laiko langą, nurodytą prekių skirstymo šablone, kuriame buvo sukurtas prekių skirstymo kiekis.</span><span class="sxs-lookup"><span data-stu-id="902a3-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="902a3-271">„FastTab“ skirtuke **Krovinio eilutės** pasirinkite **Suplanuotas prekių skirstymas** peržiūrėti išsamią sukurto prekių skirstymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="902a3-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="902a3-272">Prekių skirstymo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="902a3-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="902a3-273">Pirkimo užsakymas „Warehousing“ programėlėje</span><span class="sxs-lookup"><span data-stu-id="902a3-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="902a3-274">Sistema gaus 5 kiekį iš pirkimo užsakymo į gavimo vietą ir sukurs du darbo vienetus.</span><span class="sxs-lookup"><span data-stu-id="902a3-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="902a3-275">Pirmoji sukurta darbo ID yra **Darbo užsakymo tipo** *Prekių skirstymo* reikšmė, susieta su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="902a3-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="902a3-276">Ji turi 3 kiekį ir yra nukreipta į galutinę siuntimo vietą, kad ją būtų galima išsiųsti nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="902a3-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="902a3-277">Antroji sukurta darbo ID yra **Darbo užsakymo tipo** *Pirkimo užsakymas* reikšmė, susieta su pirkimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="902a3-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="902a3-278">Jos likęs kiekis yra 2, jis nebuvo perkrautas ir nukreiptas į padėjimo į saugyklą.</span><span class="sxs-lookup"><span data-stu-id="902a3-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="902a3-279">Prisijunkite kaip mobiliojo įrenginio vartotojas sandėlyje *51*.</span><span class="sxs-lookup"><span data-stu-id="902a3-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="902a3-280">Eikite į **Gavimas \> Pirkimo gavimą**.</span><span class="sxs-lookup"><span data-stu-id="902a3-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="902a3-281">Lauke **PU numeris** įveskite savo pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="902a3-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="902a3-282">Lauke **Kiekis** įveskite *5*.</span><span class="sxs-lookup"><span data-stu-id="902a3-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="902a3-283">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-283">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-284">Kitame puslapyje nustatykite lauką **Prekė** į *A0001*.</span><span class="sxs-lookup"><span data-stu-id="902a3-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="902a3-285">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-285">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-286">Kitame puslapyje patvirtinkite **PU numerio**, **Prekės** ir **Kiekio** reikšmes pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="902a3-287">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="902a3-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="902a3-288">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="902a3-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="902a3-289">Atsargų padėjimas prekių skirstyme ir krovinyje</span><span class="sxs-lookup"><span data-stu-id="902a3-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="902a3-290">Šiuo metu abejos darbo ID turi vienodas tikslines numerio lentelės.</span><span class="sxs-lookup"><span data-stu-id="902a3-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="902a3-291">Norėdami atlikti kitus veiksmus, turite gauti darbo ID ir tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="902a3-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="902a3-292">Tai galite sužinoti iš išsamios pirkimo ir pardavimo užsakymų eilučių darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="902a3-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="902a3-293">Taip pat galite pereiti prie **Sandėlio valdymas \> Darbas \> Išsami darbo informacija** ir filtruoti darbą, kurio **Sandėlio** reikšmė yra *51*.</span><span class="sxs-lookup"><span data-stu-id="902a3-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="902a3-294">Mobiliajame įrenginyje eikite į **Gavimas \> Pirkimo padėjimas** ir įveskite tikslinę darbo numerio lentelę.</span><span class="sxs-lookup"><span data-stu-id="902a3-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="902a3-295">Lauke **ID** įveskite tikslinės numerio lentelės ID iš darbo informacijos.</span><span class="sxs-lookup"><span data-stu-id="902a3-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="902a3-296">Prekių skirstymo paėmimo puslapyje pateikiama paėmimo vieta (*RECV*), tikslinė numerio lentelė (*numerio lentelė*), prekė (*A0001*) ir kiekis (*3*).</span><span class="sxs-lookup"><span data-stu-id="902a3-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="902a3-297">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-297">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-298">Lauke **Tikslinė LP** įveskite tikslinės numerio lentelės ID, kuri turi būti įtraukta (perskirstyta) į siuntimo vietą.</span><span class="sxs-lookup"><span data-stu-id="902a3-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="902a3-299">Galite pasirinkti bet kurį savo pasirinktą numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="902a3-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="902a3-300">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-300">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-301">Kito puslapio lauke **ID** įveskite tikslinės numerio lentelės ID.</span><span class="sxs-lookup"><span data-stu-id="902a3-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="902a3-302">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-302">Select **OK**.</span></span>
1. <span data-ttu-id="902a3-303">Patvirtinkite paėmimo darbą, kad būtų galima paimti likusį 2 kiekį ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="902a3-304">Kitame puslapyje pasirinkite **Atlikta** užbaigti paėmimo procesą ir pradėti padėjimo procesą.</span><span class="sxs-lookup"><span data-stu-id="902a3-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="902a3-305">Mobiliųjų įrenginių programėlė pateikia Jums vietą ir numerio lentelę, į kurias galima įtraukti prekę.</span><span class="sxs-lookup"><span data-stu-id="902a3-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="902a3-306">Patvirtinkite krovinio **Padėjimo** saugyklą pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="902a3-307">Kitame puslapyje patvirtinkite prekių skirstymo **Padėjimą** pasirinkdami **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="902a3-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="902a3-308">Gaunate Pabaigtas darbas pranešimą.</span><span class="sxs-lookup"><span data-stu-id="902a3-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="902a3-309">Pasirinkti **Atšaukti** norėdami atsijungti.</span><span class="sxs-lookup"><span data-stu-id="902a3-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="902a3-310">Toliau pateiktoje iliustracijoje rodoma, kaip atliktas prekių skirstymas gali atrodyti „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="902a3-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="902a3-311">![Atliktas prekių skirstymas](media/PlannedCrossDockingWork.png "Atliktas prekių skirstymas")</span><span class="sxs-lookup"><span data-stu-id="902a3-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
