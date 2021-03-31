---
title: Atidėjimo klasteriai
description: Atidėjimo klasteriai siūlo būda paimti keletą licencijos lentelių tuo pačiu metu ir tada paimti jas atidėjimui skirtingose vietose. Jos gali būti labai naudingos mažmenos verslui, kai licencijos lentelės dažniausiai nėra pilni inventoriaus padėklai.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5552959068d109bffe32b8074666bcd63b57183a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228446"
---
# <a name="putaway-clusters"></a><span data-ttu-id="1793c-104">Atidėjimo klasteriai</span><span class="sxs-lookup"><span data-stu-id="1793c-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1793c-105">Atidėjimo klasteriai siūlo būda paimti keletą licencijos lentelių tuo pačiu metu ir tada paimti jas atidėjimui skirtingose vietose.</span><span class="sxs-lookup"><span data-stu-id="1793c-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="1793c-106">Šis procesas dažnai yra vadinamas *pieno vykdymu*.</span><span class="sxs-lookup"><span data-stu-id="1793c-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="1793c-107">Atidėjimo klasteriai gali būti labai naudingi mažmenos verslui, kai licencijos lentelės dažniausiai nėra pilni inventoriaus padėklai.</span><span class="sxs-lookup"><span data-stu-id="1793c-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="1793c-108">įjunkite klasterio atidėjimo funkciją</span><span class="sxs-lookup"><span data-stu-id="1793c-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="1793c-109">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="1793c-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1793c-110">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="1793c-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1793c-111">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="1793c-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1793c-112">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="1793c-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1793c-113">**Funkcijos pavadinimas:** *Klasterio atidėjimo funkcija*</span><span class="sxs-lookup"><span data-stu-id="1793c-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="1793c-114">Nustatymas pavyzdžio scenarijui</span><span class="sxs-lookup"><span data-stu-id="1793c-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="1793c-115">Klasterio šablonai</span><span class="sxs-lookup"><span data-stu-id="1793c-115">Cluster profiles</span></span>

<span data-ttu-id="1793c-116">Atidėjimo klasterio profilis nustato, ar prekė eis pagrindžiant vieta, kuri yra priskirta elementui gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="1793c-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="1793c-117">Jei kiti klasteriai yra reikalingi, skirtingi atidėjimo klasteriai turi būti sukurti, kurių kiekvienas turi būti mobiliam įrenginio meniu prekei.</span><span class="sxs-lookup"><span data-stu-id="1793c-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="1793c-118">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="1793c-119">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1793c-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1793c-120">Rodinyje **Antrašte**, nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="1793c-121">**Atidėjimo klasterio profilio ID:** *Klasterio atidėjimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="1793c-122">**Atidėjimo klasterio profilio ID pavadinimas:** *Klasterio atidėjimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="1793c-123">**Klasterio tipas:** *Atidėjimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="1793c-124">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="1793c-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="1793c-125">Pasirinkite **Įrašyti** tam, kad sudarytume būtinus laukelius **Bendrų** prieinamame „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="1793c-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="1793c-126">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1793c-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1793c-127">**Klasterio priskyrimo laikas:** *Gavimo metu*</span><span class="sxs-lookup"><span data-stu-id="1793c-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="1793c-128">Šis laukelis nustato, ar atidėjimo klasteris turi būti priskirtas nedelsiant, kai inventorius bus gautas arba jis turi būti rūšiuojamas vėliau.</span><span class="sxs-lookup"><span data-stu-id="1793c-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="1793c-129">**Klasterio priskyrimo taisyklė:** *Rankinė*</span><span class="sxs-lookup"><span data-stu-id="1793c-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="1793c-130">Šis laukelis nustato, ar klasterio priskyrimas turi būti nustatomas automatiškai sistemos ar rankiniu būdu vartotojo.</span><span class="sxs-lookup"><span data-stu-id="1793c-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="1793c-131">**Nurodymo kodas:** Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1793c-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="1793c-132">**Atidėjimo klasterio aptikimas:** *Gavimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="1793c-133">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="1793c-133">The following values are available:</span></span>

        - <span data-ttu-id="1793c-134">**Gavimas** – Vieta yra nedelsiant randami gavimo metu.</span><span class="sxs-lookup"><span data-stu-id="1793c-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="1793c-135">**Klasterio uždarymas** – Vieta yra randama, kai klasteris yra uždarytas.</span><span class="sxs-lookup"><span data-stu-id="1793c-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="1793c-136">**Naudotojo nukreiptas** – Vieta yra randama, kai licencijos lentelė yra paimama iš klasterio atidėjimui.</span><span class="sxs-lookup"><span data-stu-id="1793c-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="1793c-137">Tokiu atveju, nėra jokios vietos nurodytos, kai atidėjimo darbas yra sukurtas.</span><span class="sxs-lookup"><span data-stu-id="1793c-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="1793c-138">Atidėjimo metu, vartotojas gali nuskaityti licencijos lentelę ar darbo ID, kad pradėtų padėjimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="1793c-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="1793c-139">Sistema tuomet suranda padėjimo vietą dar kartą ir pasako vartotojui, kuri padėti paimtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="1793c-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="1793c-140">**Atidėjimo klasteris vartotojui:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="1793c-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="1793c-141">Šis laukelis nustato, ar kiekvienas klasteris turi būti unikalus vartotojui, kai klasteriai yra priskiriami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1793c-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="1793c-142">Jis prieinamas tik kai **Klasterio priskyrimo taisyklės** laukelis nustatytas į *Automatinis*.</span><span class="sxs-lookup"><span data-stu-id="1793c-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="1793c-143">**Vieneto apribojimas:** Palikite šį laukelį tuščią.</span><span class="sxs-lookup"><span data-stu-id="1793c-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="1793c-144">Laukelis nurodo vienetą, kuris turi gauto profilį, kad jis galiotų.</span><span class="sxs-lookup"><span data-stu-id="1793c-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="1793c-145">Jei jis paliktas tuščias, visi vienetai galioja.</span><span class="sxs-lookup"><span data-stu-id="1793c-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="1793c-146">**Darbo vieneto suskaldymas:** *Asmeninis*</span><span class="sxs-lookup"><span data-stu-id="1793c-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="1793c-147">Šis laukelis nustato, ar visas inventorius turėtų būti konsoliduotas (naudojant klasterio ID ir licencijos plokštelė) vienoje licencijos plokštelėje uždarius klasterį ir ar jis turi būti atidėtas kaip viena licencijos plokštelė ar atskiras gaunamose licencijos plokštelėse.</span><span class="sxs-lookup"><span data-stu-id="1793c-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="1793c-148">Šis laukelis yra neprieinamas, kai **Atidėjimo klasterio vietos** laukelis yra nustatytas *Gautas*.</span><span class="sxs-lookup"><span data-stu-id="1793c-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="1793c-149">**Klasteris galioja kaip valdanti licencijos plokštelė:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="1793c-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="1793c-150">Jei ši parinktis nustatyta į *Ne*, tuomet padėjimo žingsnis yra užbaigtas, klasterio ID taps valdančia licencijos plokštele ir visos prekės klasterio ID bus susietos su ta valdančia licencijos plokštele.</span><span class="sxs-lookup"><span data-stu-id="1793c-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="1793c-151">**Klasterio rūšiavimo** „FastTab“, galite nustatyti atidėjimo rūšiavimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="1793c-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="1793c-152">Pasirinkite **Naujas** įrankių juostoje, kad įtrauktumėte eilutę ir tada nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="1793c-153">**Sekos numeris:** Priimkite numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="1793c-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="1793c-154">**Laukelio pavadinimas:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="1793c-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="1793c-155">Šis laukelis nustato laukelį, kurį eilutė turi naudoti kaip rūšiavimo kriterijų.</span><span class="sxs-lookup"><span data-stu-id="1793c-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="1793c-156">**Rūšiavimas:** *Didėjantis*</span><span class="sxs-lookup"><span data-stu-id="1793c-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="1793c-157">Šis laukelis nurodo, ar rūšiavimas turi būti atliekamas didėjančia ar mažėjančia tvarka.</span><span class="sxs-lookup"><span data-stu-id="1793c-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="1793c-158">**Klasterio darbo šablono** „FastTab“, pasirinkite **Kitas** įrankių juostoje, kad įtrauktumėte eilutę ir tada nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="1793c-159">**Darbo užsakymo tipas:** *Įsigijimo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="1793c-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="1793c-160">**Darbo šablonas:** *61 PO tiesiognis*</span><span class="sxs-lookup"><span data-stu-id="1793c-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="1793c-161">Veiksmų juostoje pasirinkite **Įrašyti** ir tada pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1793c-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="1793c-162">**Klasterio atidėjimo** teksto laukelyje, **Intervalas** skirtuke pasirinkite **Įtraukti**, kad įtrauktumėte antrą liniją į užklausą.</span><span class="sxs-lookup"><span data-stu-id="1793c-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="1793c-163">Tuomet atnaujinkite užklausos eilutes kaip rodoma tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="1793c-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="1793c-164">Lentelė</span><span class="sxs-lookup"><span data-stu-id="1793c-164">Table</span></span> | <span data-ttu-id="1793c-165">Išvestinė lentelė</span><span class="sxs-lookup"><span data-stu-id="1793c-165">Derived table</span></span> | <span data-ttu-id="1793c-166">Laukas</span><span class="sxs-lookup"><span data-stu-id="1793c-166">Field</span></span> | <span data-ttu-id="1793c-167">Kriterijai</span><span class="sxs-lookup"><span data-stu-id="1793c-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="1793c-168">Darbas</span><span class="sxs-lookup"><span data-stu-id="1793c-168">Work</span></span> | <span data-ttu-id="1793c-169">Darbas</span><span class="sxs-lookup"><span data-stu-id="1793c-169">Work</span></span> | <span data-ttu-id="1793c-170">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="1793c-170">Warehouse</span></span> | <span data-ttu-id="1793c-171">*61*</span><span class="sxs-lookup"><span data-stu-id="1793c-171">*61*</span></span> |
    | <span data-ttu-id="1793c-172">Darbas</span><span class="sxs-lookup"><span data-stu-id="1793c-172">Work</span></span> | <span data-ttu-id="1793c-173">Darbas</span><span class="sxs-lookup"><span data-stu-id="1793c-173">Work</span></span> | <span data-ttu-id="1793c-174">Darbo ID</span><span class="sxs-lookup"><span data-stu-id="1793c-174">Work ID</span></span> | <span data-ttu-id="1793c-175">Palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="1793c-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="1793c-176">Pasirinkite **Gerai**, kad įrašytumėte užklausą ir uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1793c-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="1793c-177">Veiksmų juostoje pasirinkite **Įrašyti** ir užverkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1793c-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1793c-178">Laukeliai klasterio profilyje, kurie pasirodo prigęsę, kai **Sukurti klasterio ID** yra nustatyti į *Taip* yra neprieinami ir nebus laikomi galiojančiais, kai ši funkcija yra naudojama.</span><span class="sxs-lookup"><span data-stu-id="1793c-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="1793c-179">Mobiliojo įrenginio meniu elementai</span><span class="sxs-lookup"><span data-stu-id="1793c-179">Mobile device menu items</span></span>

<span data-ttu-id="1793c-180">Du nauji mobiliojo įrenginio meniu prekės yra prieinamos šiai funkcijai.</span><span class="sxs-lookup"><span data-stu-id="1793c-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="1793c-181">**Gauti ir rūšiuoti klasterį** meniu prekė yra naudojama siekiant rūšiuoti gautą inventorių į atidėjimo klasterį po gavimo.</span><span class="sxs-lookup"><span data-stu-id="1793c-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="1793c-182">**Klasterio atidėjimo** meniu prekė yra naudojama norint atidėti klasterį po jo priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="1793c-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="1793c-183">Gauti ir rūšiuoti klasterį</span><span class="sxs-lookup"><span data-stu-id="1793c-183">Receive and sort cluster</span></span>

<span data-ttu-id="1793c-184">Sukurkite naują mobiliojo įrenginio meniu prekę inventoriaus gavimui ir rūšiuokite į klasterį.</span><span class="sxs-lookup"><span data-stu-id="1793c-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="1793c-185">Ši meniu prekė sukurs išorės darbą po to, kai inventorius bus gautas, o tai rodo, kad gautas meniu prekė bus naudojama atidėjimo klasteriams.</span><span class="sxs-lookup"><span data-stu-id="1793c-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="1793c-186">**Gauti ir rūšiuoti klasterį** meniu elementas gali būti naudojamas tolesnėms gavimo meniu prekėms:</span><span class="sxs-lookup"><span data-stu-id="1793c-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="1793c-187">Gaunama pirkimo užsakymo eilutė</span><span class="sxs-lookup"><span data-stu-id="1793c-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="1793c-188">Gaunama pirkimo užsakymo prekė</span><span class="sxs-lookup"><span data-stu-id="1793c-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="1793c-189">Krovinio prekės gavimas</span><span class="sxs-lookup"><span data-stu-id="1793c-189">Load item receiving</span></span>

1. <span data-ttu-id="1793c-190">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1793c-191">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1793c-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1793c-192">Rodinyje **Antrašte**, nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="1793c-193">**Meniu prekės pavadinimas:** *Gauti ir rūšiuoti klasterį*</span><span class="sxs-lookup"><span data-stu-id="1793c-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="1793c-194">**Pavadinimas:** *Gauti ir rūšiuoti klasterį*</span><span class="sxs-lookup"><span data-stu-id="1793c-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="1793c-195">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="1793c-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="1793c-196">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="1793c-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="1793c-197">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="1793c-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="1793c-198">**Darbo sukūrimo procesas:** *Įsigijimo užsakymo prekės gavimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="1793c-199">**Generuoti numerio lentelę:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="1793c-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="1793c-200">**Priskirkite atidėjimo klasterį:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="1793c-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="1793c-201">**Priskyrimo atidėjimo klasterio** parinktis yra prieinama tik vienam žingsniui *Darbo sukūrimo proceso* veiklai gavimui.</span><span class="sxs-lookup"><span data-stu-id="1793c-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="1793c-202">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="1793c-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="1793c-203">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1793c-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="1793c-204">Klasterio atidėjimas</span><span class="sxs-lookup"><span data-stu-id="1793c-204">Cluster putaway</span></span>

<span data-ttu-id="1793c-205">Sukurkite naują mobiliojo įrenginio meniu prekę klasterio atidėjimui po jo priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="1793c-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="1793c-206">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="1793c-207">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1793c-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1793c-208">Rodinyje **Antrašte**, nustatykite tolesnes vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="1793c-209">**Meniu prekės pavadinimas:** *Klasterio atidėjimo funkcija*</span><span class="sxs-lookup"><span data-stu-id="1793c-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="1793c-210">**Pavadinimas:** *Klasterio atidėjimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="1793c-211">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="1793c-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="1793c-212">**Naudoti esamą darbą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="1793c-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="1793c-213">**Bendrų**„ FastTab“, nustatykite **Valdomas** laukelis į *Klasterio atidėjimą*.</span><span class="sxs-lookup"><span data-stu-id="1793c-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="1793c-214">Priimkite nustatytąsias vertes likusiems laukeliams.</span><span class="sxs-lookup"><span data-stu-id="1793c-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="1793c-215">**Darbo klasės** „FastTab“, nustatykite galiojančią darbo klasę šiai mobiliojo įrenginio meniu prekei:</span><span class="sxs-lookup"><span data-stu-id="1793c-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="1793c-216">**Darbo klasės ID:** *Įsigijimas*</span><span class="sxs-lookup"><span data-stu-id="1793c-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="1793c-217">**Darbo užsakymo tipas:** *Įsigijimo užsakymai*</span><span class="sxs-lookup"><span data-stu-id="1793c-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="1793c-218">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1793c-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="1793c-219">Mobiliojo įrenginio meniu</span><span class="sxs-lookup"><span data-stu-id="1793c-219">Mobile device menu</span></span>

<span data-ttu-id="1793c-220">Įtraukite meniu prekes, kurias kątik sukūrėte įvesties meniu mobiliojoje programoje.</span><span class="sxs-lookup"><span data-stu-id="1793c-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="1793c-221">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="1793c-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="1793c-222">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1793c-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="1793c-223">Meniu sąraše pasirinkite **Įvestis**.</span><span class="sxs-lookup"><span data-stu-id="1793c-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="1793c-224">**Prieinami meniu ir meniu prekių** sąraše suraskite ir pasirinkite **Gauti ir rūšiuoti klasterį**.</span><span class="sxs-lookup"><span data-stu-id="1793c-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="1793c-225">Pasirinkite dešinės rodyklės mygtuką, kad pasirinktumėte meniu prekę į **Menius struktūros** sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1793c-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="1793c-226">Naudokite rodyklės aukštyn ir žemyn mygtuką, kad perkeltumėte meniu prekę į norimą padėtį meniu.</span><span class="sxs-lookup"><span data-stu-id="1793c-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="1793c-227">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1793c-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1793c-228">Pakartokite žingsnius nuo 4 iki 7, kad įtrauktumėte likusias meniu prekes:</span><span class="sxs-lookup"><span data-stu-id="1793c-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="1793c-229">Priskirkite klasterį</span><span class="sxs-lookup"><span data-stu-id="1793c-229">Assign cluster</span></span>
    - <span data-ttu-id="1793c-230">Klasterio atidėjimas</span><span class="sxs-lookup"><span data-stu-id="1793c-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1793c-231">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="1793c-231">Example scenario</span></span>

<span data-ttu-id="1793c-232">Šis scenarijus atkartoja atidėjimo klasterio apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="1793c-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="1793c-233">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="1793c-233">Create a purchase order</span></span>

1. <span data-ttu-id="1793c-234">Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="1793c-235">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1793c-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1793c-236">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="1793c-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1793c-237">**Tiekėjo paskyra:** *1001*</span><span class="sxs-lookup"><span data-stu-id="1793c-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="1793c-238">**Sandėlis:** *61*</span><span class="sxs-lookup"><span data-stu-id="1793c-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="1793c-239">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-239">Select **OK**.</span></span>

    <span data-ttu-id="1793c-240">**Visi pirkimo užsakymai** puslapis pasirodo.</span><span class="sxs-lookup"><span data-stu-id="1793c-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="1793c-241">Puslapyje **Visi pirkimo užsakymai**, **Pirkimo užsakymo eilutės** „FastTab“, naudokite **Įtraukti eilutę** mygtuką, kad įtrauktumėte tolesnes eilutes:</span><span class="sxs-lookup"><span data-stu-id="1793c-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="1793c-242">Pirkimo užsakymo eilutė 1:</span><span class="sxs-lookup"><span data-stu-id="1793c-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="1793c-243">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1793c-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="1793c-244">**Kiekis:** *10*</span><span class="sxs-lookup"><span data-stu-id="1793c-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="1793c-245">Pirkimo užsakymo eilutė 2:</span><span class="sxs-lookup"><span data-stu-id="1793c-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="1793c-246">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1793c-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="1793c-247">**Kiekis:** *20*</span><span class="sxs-lookup"><span data-stu-id="1793c-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="1793c-248">Pirkimo užsakymo eilutė 3:</span><span class="sxs-lookup"><span data-stu-id="1793c-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="1793c-249">**Prekės numeris:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="1793c-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="1793c-250">**Kiekis:** *30*</span><span class="sxs-lookup"><span data-stu-id="1793c-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="1793c-251">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1793c-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="1793c-252">Pasižymėkite pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="1793c-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="1793c-253">Gaukite inventorių ir atidėkite iš mobiliojo įrenginio</span><span class="sxs-lookup"><span data-stu-id="1793c-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="1793c-254">Gaukite ir rūšiuokite inventorių į klasterį</span><span class="sxs-lookup"><span data-stu-id="1793c-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="1793c-255">Prisijunkite prie sandėlio programos kaip vartotojas, kuris nustatė sandėliui *61*.</span><span class="sxs-lookup"><span data-stu-id="1793c-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="1793c-256">Pagrindiniame meniu pasirinkite **Įvestis**.</span><span class="sxs-lookup"><span data-stu-id="1793c-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="1793c-257">Meniu **Įvestis** rinkitės **Gauti ir rūšiuoti klasterį**.</span><span class="sxs-lookup"><span data-stu-id="1793c-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="1793c-258">Laukelyje **Ponum** įveskite pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="1793c-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="1793c-259">Rinkitės **GERAI** (pažymėkite žymimą mygtuką).</span><span class="sxs-lookup"><span data-stu-id="1793c-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="1793c-260">Rinkitės **Prekės** laukelį ir įveskite numerį *A0001* ir tada rinkitės **GERAI**.</span><span class="sxs-lookup"><span data-stu-id="1793c-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="1793c-261">Pasirinkite **Qty** laukelį ir įveskite *10* naudodami skaičių klaviatūra ir tada rinkitės pažymėti mygtuką.</span><span class="sxs-lookup"><span data-stu-id="1793c-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="1793c-262">Užduoties puslapyje **Kiekis** rinkitės **Gerai** (pažymėkite mygtuką), kad patvirtintumėte įvestą kiekį.</span><span class="sxs-lookup"><span data-stu-id="1793c-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="1793c-263">Užduoties puslapyje **Prekė** rinkitės **Gerai** kad patvirtintumėte prekę *A0001*, kuri buvo įvesta.</span><span class="sxs-lookup"><span data-stu-id="1793c-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="1793c-264">Rinkitės **Klasterio ID** laukelį ir įveskite vertę, kad priskirtumėte ID klasteriui, kurį sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="1793c-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="1793c-265">Jūsų įvestas ID čia bus naudojamas, kai dvi likusios prekės pirkimo užsakyme bus gautos.</span><span class="sxs-lookup"><span data-stu-id="1793c-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="1793c-266">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-266">Select **OK**.</span></span>

    <span data-ttu-id="1793c-267">**Ponum** užduoties puslapis pasirodo ir rodo „Darbas baigtas“ pranešimą.</span><span class="sxs-lookup"><span data-stu-id="1793c-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="1793c-268">Prekė *A0001* dabar buvo gauta į *RECV* vietą ir priskirta klasterio ID, kurį įvedėte žingsnyje 10.</span><span class="sxs-lookup"><span data-stu-id="1793c-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="1793c-269">Pakartokite žingsnius nuo 4 iki 11, kad gautumėte likusias dvi prekes iš pirkimo užsakymo ir priskirtumėte jas klasterio ID:</span><span class="sxs-lookup"><span data-stu-id="1793c-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="1793c-270">Kiekis *20* prekei *A0002*</span><span class="sxs-lookup"><span data-stu-id="1793c-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="1793c-271">Kiekis *30* prekei *M9215*</span><span class="sxs-lookup"><span data-stu-id="1793c-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="1793c-272">Užverkite klasterį</span><span class="sxs-lookup"><span data-stu-id="1793c-272">Close the cluster</span></span>

<span data-ttu-id="1793c-273">Prieš tai, kai prekės klasteryje gali būti atidėtos, klasterį reikia užverti.</span><span class="sxs-lookup"><span data-stu-id="1793c-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="1793c-274">„Supply Chain Management“ eiktie į **Sandėlio valdymas \> Darbas \> Išvestis \> Darbo klasteriai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="1793c-275">Puslapyje **Darbo klasteriai** skyriuje **Darbo klasteris** ieškokite **Klasterio ID** laukelio klasterio ID, kurį įvedėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="1793c-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="1793c-276">Jei klsateris nerodomas, jis jau gali būti užvertas.</span><span class="sxs-lookup"><span data-stu-id="1793c-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="1793c-277">Norėdami nustatyti, ar klasteris užvertas, pasirinkite **Rodyti užvėrimo darbą** žymimą laukelį ir ieškokite klasterio ID, kurį įvedėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="1793c-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="1793c-278">Tuomet atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="1793c-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="1793c-279">Jei klasteris buvo užvertas, praleiskite likusius šios procedūros žingsnius ir judėkite toliau prie kitos procedūros, [Klasterio atidėjimas](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="1793c-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="1793c-280">Jei klasteris nebuvo užvertas, atlikite likusius šios procedūros žingsnius, kad rankinu būdu užvertumėte klasterį.</span><span class="sxs-lookup"><span data-stu-id="1793c-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="1793c-281">Tuomet judėkite prie kitos procedūros.</span><span class="sxs-lookup"><span data-stu-id="1793c-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="1793c-282">Skyriuje **Darbo klasteris** pasirinkite klasterio ID, kurį įvedėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="1793c-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="1793c-283">Veiksmų juosoje rinkitės **Užverti klasterį**.</span><span class="sxs-lookup"><span data-stu-id="1793c-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="1793c-284">Po to, kai klasteris buvo užvertas, jis neberodomas **Darbo klasteris** skyriuje (nebent **Rodyti užvertą darbą** žymimas laukelis pasirinktas).</span><span class="sxs-lookup"><span data-stu-id="1793c-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="1793c-285">Klasterio atidėjimas</span><span class="sxs-lookup"><span data-stu-id="1793c-285">Put the cluster away</span></span>

1. <span data-ttu-id="1793c-286">Prisijunkite prie sandėlio programos kaip vartotojas, kuris nustatė sandėliui *61*.</span><span class="sxs-lookup"><span data-stu-id="1793c-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="1793c-287">Pagrindiniame meniu pasirinkite **Įvestis**.</span><span class="sxs-lookup"><span data-stu-id="1793c-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="1793c-288">Meniu **įvestis** rinkitės **Klasterio atidėjimas**.</span><span class="sxs-lookup"><span data-stu-id="1793c-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="1793c-289">Rinkitės **Klasterio ID** ir įveskite klasterio ID, kurį įvedėte anksčiau užvertam klasteriui.</span><span class="sxs-lookup"><span data-stu-id="1793c-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="1793c-290">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-290">Select **OK**.</span></span>

    <span data-ttu-id="1793c-291">**Klasterio atidėjimas: Paėmimas** puslapis pasirodo.</span><span class="sxs-lookup"><span data-stu-id="1793c-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="1793c-292">Jis rodo klasterio ID, paėmimo vietą, prekes (vertė *Keletas* bus rodoma) ir bendras kiekis klasteryje, kurį reikia paimti.</span><span class="sxs-lookup"><span data-stu-id="1793c-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="1793c-293">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1793c-293">Select **OK**.</span></span>

    <span data-ttu-id="1793c-294">**Klasterio atidėjimas: Padėjimas** puslapis pasirodo.</span><span class="sxs-lookup"><span data-stu-id="1793c-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="1793c-295">**padėjimo** instrukcijos nustato klasterio ID, padėjimo vietą, prekes, bendrą kiekį ir licencijos lentelės ID prekėms, kurios buvo gautos klasteryje.</span><span class="sxs-lookup"><span data-stu-id="1793c-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="1793c-296">Turite standartines parinktis, kurios viršys arba praleis šį žingsnį.</span><span class="sxs-lookup"><span data-stu-id="1793c-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="1793c-297">![Klasterio atidėjimas: Padėjimo puslapis](media/Cluster_putaway-Put.png "Klasterio atidėjimas: Padėjimo puslapis")</span><span class="sxs-lookup"><span data-stu-id="1793c-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="1793c-298">Rinkitės **GERAI**, kad patvirtintumėte klasterio atidėjimą.</span><span class="sxs-lookup"><span data-stu-id="1793c-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="1793c-299">Rodomas pranešimas „Klasteris baigtas“.</span><span class="sxs-lookup"><span data-stu-id="1793c-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="1793c-300">Pastabos ir patarimai</span><span class="sxs-lookup"><span data-stu-id="1793c-300">Notes and tips</span></span>

<span data-ttu-id="1793c-301">Dėl atvejų, kai klasterio ID tampa valdančia licencijos plokštele pakrautam padėklui, padėjimo padėtis automatiškai suteikiama, kai nuskaitomas atitinkamas klasterio ID.</span><span class="sxs-lookup"><span data-stu-id="1793c-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="1793c-302">Negalima nuskaityti jokios tolesnės licencijos plokštelės, net jei licencijos plokštelės sukūrimas nustatytas į rankinį.</span><span class="sxs-lookup"><span data-stu-id="1793c-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]