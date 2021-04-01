---
title: Darbo telkinio keitimas
description: Šiame skyriuje paaiškinama, kaip galite naudoti darbo telkinio keitimo mygtuką darbo elementams tam, kad pakeistumėte esančios užduoties darbo telkinį.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233060"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="4d0cb-103">Darbo telkinio keitimas</span><span class="sxs-lookup"><span data-stu-id="4d0cb-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d0cb-104">Galite naudoti darbo telkinius užduočių suskirstymui į grupes.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="4d0cb-105">Pavyzdžiui, galite sukurti darbo telkinį tam, kad klasifikuotumėte darbus, kurie pasirodo konkrečioje sandėlio vietoje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="4d0cb-106">*Darbo telkinio keitimas darbui* funkcija įtraukiama į **Darbo telkinio keitimo** mygtuką darbo elementų veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="4d0cb-107">Dėl to, sandėlio vadovai gali lengvai keisti esančios užduoties darbo telkinį.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="4d0cb-108">Ši savybė leidžia vadovams greitai reaguoti į pokyčius ant sandėlio parduotuvės grindų ir padeda jiems pagerinti jų galimybes prisitaikyti prie besikeičiančių situacijų ir poreikio perduoti darbą kitam darbo baseinui.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="4d0cb-109">Įjunkite darbo baseino keitimus darbo savybėse</span><span class="sxs-lookup"><span data-stu-id="4d0cb-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="4d0cb-110">Prieš pradėdami nustatyti ar naudoti šią savybę, privalote įsitikinti, kad ji yra prieinama jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="4d0cb-111">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4d0cb-112">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4d0cb-113">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4d0cb-114">**Savybės pavadinimas:** *Keisti darbo baseiną darbe*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="4d0cb-115">Nustatykite darbo baseino keitimus darbo savybėse</span><span class="sxs-lookup"><span data-stu-id="4d0cb-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="4d0cb-116">Šios savybės naudojimui, privalote turėti nustatytus keletą darbo baseinų.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="4d0cb-117">Galite taip pat nustatyti savo darbo šablonus taip, kad jie automatiškai priskirtų baseiną.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="4d0cb-118">Jei norite dirbti su pavyzdiniu scenarijumi, pateiktu šioje temoje, nustatykite sistemą, kaip aprašyta šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="4d0cb-119">Darbo baseinų nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d0cb-119">Set up work pools</span></span>

<span data-ttu-id="4d0cb-120">Darbo baseinai leidžia jums tvarkyti darbo elementus pagal tipą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="4d0cb-121">Darbui su *Darbo baseino keitimu savo darbe* funkcija, privalote turėti mažiausiai du prieinamus darbo baseinus.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="4d0cb-122">Darbo baseinų peržiūrai ir įtraukimui, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="4d0cb-123">Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbas \> Darbo baseinai**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="4d0cb-124">Jei dirbate su demo duomenimis iš **USMF** bendrovės ir dirbsite vėliau su pavyzdiniu scenarijume šioje temoje, įtraukite du darbo baseinus, kurie turi šiuos nustatymus:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="4d0cb-125">Darbo baseinas 1:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-125">Work pool 1:</span></span>

        - <span data-ttu-id="4d0cb-126">**Darbo baseino identifikavimo kodas:** *Tinklo parduotuvė*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="4d0cb-127">**Aprašas:** *Tinklo parduotuvė*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="4d0cb-128">Darbo baseinas 2:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-128">Work pool 2:</span></span>

        - <span data-ttu-id="4d0cb-129">**Darbo baseino identifikavimo kodas:** *Skambučių centras*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="4d0cb-130">**Aprašas:** *Skambučių centras*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="4d0cb-131">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="4d0cb-132">Nustatyti darbo šablonus</span><span class="sxs-lookup"><span data-stu-id="4d0cb-132">Set up work templates</span></span>

<span data-ttu-id="4d0cb-133">Kiekvienam iš savo darbo šablonų galite nustatyti kokį norite nustatytąjį darbo baseiną.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="4d0cb-134">Kiekvienam atitinkamam šablonui, priskiriate darbo baseiną **Darbo baseino identifikavimo kodo** stulpelyje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="4d0cb-135">Šiuo atveju, visi darbo elementai sukurti naudojant duotą šabloną automatiškai paveldės priskirtą darbo baseiną.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="4d0cb-136">Jei dirbate su demo duomenimis iš **USMF** bendrovės ir dirbsite vėliau su pavyzdiniu scenarijume šioje temoje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="4d0cb-137">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4d0cb-138">Veiksmų juostoje pasirinkite **Redaguoti** tam, kad lange įjungtumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="4d0cb-139">Redaguokite šabloną nustatydami šias vertes:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="4d0cb-140">**Darbo šablonas:** *62 Paėmima pakavimui*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="4d0cb-141">**Darbo baseino identifikavimo kodas:** *Tinklo parduotuvė*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="4d0cb-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4d0cb-143">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="4d0cb-143">Example scenario</span></span>

<span data-ttu-id="4d0cb-144">Šis scenarijus rodo, kaip keisti esančio darbo elemento apdorojimo srautą keičiant jo darbo baseiną.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="4d0cb-145">Jis naudoja demo duomenis **USMF** bendrovėje ir nustatymus, kurie buvo pasiūlyti anksčiau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="4d0cb-146">Sukuria prekybos užsakymą ir išleidžia jį į sandėlį</span><span class="sxs-lookup"><span data-stu-id="4d0cb-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="4d0cb-147">Patvirtinkite, kad yra pakankamai turimo inventoriaus elementams *A0001* ir *A0002* sandėlyje *62*.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="4d0cb-148">Eikite į **Inventoriaus valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas** ir redaguokite čia rodomus filtrus:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="4d0cb-149">**Sandėlis** vertė prasideda su *62*.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="4d0cb-150">**Elemento numerio** vertė yra *A001* arba *A002*.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="4d0cb-151">Demo duomenys turi turėti 10 vienetų kiekvieniems duomenims.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="4d0cb-152">Vėliau, privalote sukurti prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="4d0cb-153">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4d0cb-154">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4d0cb-155">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4d0cb-156">**Kliento sąskaita:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="4d0cb-157">**Sandėlis:** *62*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="4d0cb-158">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="4d0cb-159">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-159">The new sales order is opened.</span></span> <span data-ttu-id="4d0cb-160">Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4d0cb-161">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d0cb-162">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4d0cb-163">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4d0cb-164">Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="4d0cb-165">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="4d0cb-166">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-166">Close the page.</span></span>
1. <span data-ttu-id="4d0cb-167">**Prekybos užsakymo linijos** „FastTab“, pasirinkite **Įtraukti liniją** kitos linijos į savo prekybos užsakymą įtraukimui.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="4d0cb-168">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4d0cb-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="4d0cb-169">**Prekės numeris:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="4d0cb-170">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="4d0cb-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4d0cb-171">Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="4d0cb-172">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="4d0cb-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-173">Close the page.</span></span>
1. <span data-ttu-id="4d0cb-174">Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="4d0cb-175">Gausite informacinį pranešimą, kuriame rodomas bangos identifikavimo kodas ir siuntimo identifikavimo kodas, kurie buvo sukurti po išleidimo.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="4d0cb-176">Užsirašykite bangos identifikavimo kodą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="4d0cb-177">Peržiūrėkite siunčiamą bangą</span><span class="sxs-lookup"><span data-stu-id="4d0cb-177">Review the outbound wave</span></span>

1. <span data-ttu-id="4d0cb-178">Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="4d0cb-179">Tinklelyje ieškokite bangos identifikavimo kodo, kuris buvo sukurtas iš prekybos užsakymo išleidimo.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="4d0cb-180">Pasirinkite bangos identifikavimo kodą informacijos peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="4d0cb-181">**Bangos linijos** „FastTab“, įsitikinkite, kad siuntimo identifikavimo kodas yra rodomas prekybos užsakyme.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="4d0cb-182">Jei **Bangos apdorojimas išleidimui į sandėlį** parinktis yra nustatyta ties *Ne* siuntimo bangos šablono nustatymu, privalote ranka apdoroti bangą pasirinkdami **Apdoroti** **Bangos** skirtuke veiksmų juostoje tam, kad sukurtumėte darbą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="4d0cb-183">Įsitikinkite, kad banga buvo apdorota.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="4d0cb-184">Šis apdorojimas sukuria reikiamą darbą.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="4d0cb-185">Peržiūrėkite darbo informaciją ir pakeiskite darbo baseiną</span><span class="sxs-lookup"><span data-stu-id="4d0cb-185">View work details and change the work pool</span></span>

<span data-ttu-id="4d0cb-186">Galite naudoti **Darbo informacijos** puslapį tam, kad peržiūrėtumėte sukurtą darbą ir valdytumėte darbo baseiną.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="4d0cb-187">Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4d0cb-188">Pasirinkite darbo, kurį kątik sukūrėte, eilutę.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="4d0cb-189">**Užsakymo numerio** stulpelis rodys prekybos užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="4d0cb-190">**Darbo baseino identifikavimo kodo** laukelis bus nustatytas į darbo baseino identifikavimo kodą, kuris buvo nustatytas darbo šablone.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="4d0cb-191">Jei nematote **darbo baseino identifikavimo kodo** laukelio, įtraukite stulpelį į tinklelį ir vėliau perkraukite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="4d0cb-192">Tam, kad pakeistumėte darbo baseiną susietą su darbo identifikavimo kodu, veiksmų juostoje **Darbo** skirtuke pasirinkite **Keisti darbo baseino identifikavimo kodą**.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="4d0cb-193">**Keisti darbo baseiną** teksto laukelyje, **Parametrų** „FastTab“, **Darbo baseino identifikavimo kodo** laukelyje, pasirinkite *Skambučių centras*.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="4d0cb-194">Pasirinkite **OK** keitimo pritaikymui.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="4d0cb-195">Atkreipkite dėmesį, kad **Darbo baseino identifikavimo kodo** laukelis dabar buvo pakeistas į *Skambučio centrą*.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d0cb-196">Kai **Darbo baseino keitimo** laukelis pasirodo, **Darbo baseino identifikavimo kodo** laukelis gali būti paliktas tusčias iš anksto.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="4d0cb-197">Jei laukelis yra tuščias, kai pasirenkate **OK** keitimų pritaikymui, tuomet visai pašalinsite darbo baseiną iš darbo.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="4d0cb-198">Kartu su darbo baseinų keitimu, galite naudoti šią procedūrą darbo baseino įtraukimui į bet kurį darbo elementą, kuris jo neturi arba darbo baseino pašalinimui iš bet kurio darbo elemento, kuris jį turi.</span><span class="sxs-lookup"><span data-stu-id="4d0cb-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]