---
title: Vietos produkto dimensijos maišymas
description: Šioje temoje pateikiama informacija apie vietos produkto dimensijos maišymą. Ši vietos profilio funkcija padeda pagerinti vietos valdymą, kai produkto variantai arba produktai, turintys dimensijas, yra naudojami pvz., mados industrijoje. Ji leidžia Jums nuspręsti, ar konfigūracijas, spalvas, stilius ir dydžius galima maišyti tam tikram vietos profiliui, taip pat ar vieną iš šių dimensijų arba jų derinį galima įtraukti į tą pačią vietą.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004607"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="9b968-105">Vietos produkto dimensijos maišymas</span><span class="sxs-lookup"><span data-stu-id="9b968-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b968-106">Vietos produkto dimensijos maišymas yra vietos profilio funkcija, padedanti pagerinti vietos valdymą, kai produkto variantai arba produktai, turintys dimensijas, yra naudojami pvz., mados industrijoje.</span><span class="sxs-lookup"><span data-stu-id="9b968-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="9b968-107">Ji leidžia Jums nuspręsti, ar konfigūracijas, spalvas, stilius ir dydžius galima maišyti tam tikram vietos profiliui, taip pat ar vieną iš šių dimensijų arba jų derinį galima įtraukti į tą pačią vietą.</span><span class="sxs-lookup"><span data-stu-id="9b968-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="9b968-108">Vietos produkto dimensijos maišymo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="9b968-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="9b968-109">Norėdami naudoti vietos produkto dimensijos maišymą, ši funkcija turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="9b968-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="9b968-110">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="9b968-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9b968-111">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="9b968-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9b968-112">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="9b968-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9b968-113">**Funkcijos pavadinimas:** *Vietos produkto dimensijos maišymas*</span><span class="sxs-lookup"><span data-stu-id="9b968-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="9b968-114">Sąranka</span><span class="sxs-lookup"><span data-stu-id="9b968-114">Setup</span></span>

<span data-ttu-id="9b968-115">Su kiekviena sandėlio vieta turi būti susietas vietos profilis, nurodantis vietos ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9b968-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="9b968-116">Todėl visos vietos, kuriose naudojamas tas pats vietos profilis, galės leisti produkto dimensijos maišymą, kai jis bus nustatytas.</span><span class="sxs-lookup"><span data-stu-id="9b968-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="9b968-117">Vietos profilių konfigūravimas produkto dimensijai maišyti</span><span class="sxs-lookup"><span data-stu-id="9b968-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="9b968-118">Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlys \> Vietos profiliai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="9b968-119">Iš vietų profilių sąrašo pasirinkite **KROVINYS**.</span><span class="sxs-lookup"><span data-stu-id="9b968-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="9b968-120">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9b968-121">„FastTab“ skirtuke **Bendra** nustatykite **Įjungti konkretų vietos produkto dimensijos maišymą** parinktį į *Taip*.</span><span class="sxs-lookup"><span data-stu-id="9b968-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9b968-122">Šią parinktį galite nustatyti į *Taip* tik jeigu parinktis **Leisti mišrias prekes** yra nustatyta į *ne*.</span><span class="sxs-lookup"><span data-stu-id="9b968-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="9b968-123">„FastTab“ skirtuke **Leidžiamų produktų dimensijos maišymas** parinktį **Dydis** nustatykite į *taip*.</span><span class="sxs-lookup"><span data-stu-id="9b968-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="9b968-124">Šioje temoje pateiktu atveju, maišymas gali būti atliekamas tik tiems produktams, kurių **Dydžių** dimensijos skiriasi.</span><span class="sxs-lookup"><span data-stu-id="9b968-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="9b968-125">Tačiau galimos ir kitos parinktis.</span><span class="sxs-lookup"><span data-stu-id="9b968-125">However, other options are also available.</span></span>
1. <span data-ttu-id="9b968-126">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="9b968-127">Bendrųjų produktų ir produktų variantų sukūrimas</span><span class="sxs-lookup"><span data-stu-id="9b968-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="9b968-128">Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="9b968-129">Veiksmų srityje pasirinkite **Nauja** bendrajam produktui sukurti.</span><span class="sxs-lookup"><span data-stu-id="9b968-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="9b968-130">Dialogo lange **Naujas produktas** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="9b968-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b968-131">**Produkto tipas:** *Prekė*</span><span class="sxs-lookup"><span data-stu-id="9b968-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="9b968-132">**Produkto potipis:** *Bendrasis produktas*</span><span class="sxs-lookup"><span data-stu-id="9b968-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="9b968-133">**Produkto numeris:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="9b968-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="9b968-134">**Produkto pavadinimas:** *B0001 Dydis*</span><span class="sxs-lookup"><span data-stu-id="9b968-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="9b968-135">**Produkto dimensijos grupė:** *Dydis*</span><span class="sxs-lookup"><span data-stu-id="9b968-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="9b968-136">**Konfigūravimo technologija:** *Iš anksto nustatytas variantas*</span><span class="sxs-lookup"><span data-stu-id="9b968-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="9b968-137">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-137">Select **OK**.</span></span>
1. <span data-ttu-id="9b968-138">Puslapio **Produkto informacija** „FastTab“ skirtuke **Bendra** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="9b968-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="9b968-139">**Generuoti variantus automatiškai** *Taip*</span><span class="sxs-lookup"><span data-stu-id="9b968-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="9b968-140">**Dydžio grupė:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="9b968-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="9b968-141">Norėdami peržiūrėti iš anksto nustatytus variantus, veiksmų srityje pasirinkite **Produkto variantai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="9b968-142">Puslapis **Produkto variantai** atsidarys ir parodys dydžių grupės konfigūravimo variantų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9b968-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="9b968-143">Produktų išleidimas į USMF įmonę</span><span class="sxs-lookup"><span data-stu-id="9b968-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="9b968-144">Veiksmų srityje pasirinkite **Produkto variantai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="9b968-145">Puslapyje **Pasirinkti išleidžiamus produktus** patikrinkite, ar produkto numeris *B0001* yra sąraše, o tada pasirinkite **kitas**.</span><span class="sxs-lookup"><span data-stu-id="9b968-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="9b968-146">Pasirinkite **Toliau** norėdami patvirtinti išleidžiamus produkto variantus.</span><span class="sxs-lookup"><span data-stu-id="9b968-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="9b968-147">Puslapyje **Pasirinkite išleidimo įmones** pasirinkite *USMF* ir **Toliau** parinkčiai patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9b968-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="9b968-148">Puslapyje **Patvirtinti pasirinkimą** pasirinkite **Baigti** išleidimui užbaigti.</span><span class="sxs-lookup"><span data-stu-id="9b968-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="9b968-149">Jūs gausite pranešimą "Operacija atlikta".</span><span class="sxs-lookup"><span data-stu-id="9b968-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="9b968-150">Išleisto produkto USMF įmonėje atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="9b968-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="9b968-151">Įsitikinkite, kad esate prisijungęs prie **USMF** įmonės.</span><span class="sxs-lookup"><span data-stu-id="9b968-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="9b968-152">Pasirinkite **Produkto informacijos valdymas \> Produktai \> Išleisti produktai** pabaigti kurti išleistam produktui.</span><span class="sxs-lookup"><span data-stu-id="9b968-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="9b968-153">Raskite ir pasirinkite prekės numerį *B0001* puslapiui **Išleisto produkto informacija** atidaryti.</span><span class="sxs-lookup"><span data-stu-id="9b968-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="9b968-154">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9b968-155">Įsitikinkite, kad „FastTab“ skirtuko **Bendra** laukas **Prekių modelių grupė** nustatytas į *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="9b968-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="9b968-156">Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Dimensijų grupės**.</span><span class="sxs-lookup"><span data-stu-id="9b968-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="9b968-157">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9b968-157">Set the following values:</span></span>

    - <span data-ttu-id="9b968-158">**Saugojimo dimensijos grupė:** *Sandėlis*</span><span class="sxs-lookup"><span data-stu-id="9b968-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="9b968-159">**Sekimo dimensijos grupė:** *Nėra*</span><span class="sxs-lookup"><span data-stu-id="9b968-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="9b968-160">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-160">Select **OK**.</span></span>
1. <span data-ttu-id="9b968-161">Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Rezervavimo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="9b968-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="9b968-162">Nustatykite **Rezervavimo hierarchijos** lauką į *Numatytasis* ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="9b968-163">Atkreipkite dėmesį, kad jūsų pasirinkimai skyriaus **Administravimas** „FastTab“ skirtuke **Bendra** buvo atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="9b968-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="9b968-164">„FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite *10*.</span><span class="sxs-lookup"><span data-stu-id="9b968-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="9b968-165">„FastTab“ skirtuko **Tvarkyti išlaidas** lauke **Prekių grupė** įveskite *Audio*.</span><span class="sxs-lookup"><span data-stu-id="9b968-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="9b968-166">„FastTab“ skirtuko **Pirkimas** lauke **Kaina** įveskite *10*.</span><span class="sxs-lookup"><span data-stu-id="9b968-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="9b968-167">„FastTab“ skirtuko **Sandėlys** lauke **Vienetų sekų grupės ID** įveskite *EA*.</span><span class="sxs-lookup"><span data-stu-id="9b968-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="9b968-168">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="9b968-169">Vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b968-169">Create a location directive</span></span>

1. <span data-ttu-id="9b968-170">Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="9b968-171">Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Pirkimo užsakymai*.</span><span class="sxs-lookup"><span data-stu-id="9b968-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="9b968-172">Iš sąrašo pasirinkite vietos nurodymą pavadinimu *24 Tiesioginis PU*.</span><span class="sxs-lookup"><span data-stu-id="9b968-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="9b968-173">„FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="9b968-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="9b968-174">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9b968-175">**Sekos numeris:** *1*</span><span class="sxs-lookup"><span data-stu-id="9b968-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="9b968-176">Nauja eilutė turi būti priekyje anksčiau sukurtos eilutės.</span><span class="sxs-lookup"><span data-stu-id="9b968-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="9b968-177">Norėdami atlikti pakeitimą, naudokite įrankių juostoje esančius mygtukus **Perkelti aukštyn** ir **Perkelti žemyn** arba pakeiskite esamos eilutės **Sekos numerio** reikšmę į *2*.</span><span class="sxs-lookup"><span data-stu-id="9b968-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="9b968-178">**Pavadinimas:** *Pridėti į BULK vietos profilį*</span><span class="sxs-lookup"><span data-stu-id="9b968-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="9b968-179">**Fiksuotos vietos naudojimas:** *Fiksuotos ir nefiksuotos vietos*</span><span class="sxs-lookup"><span data-stu-id="9b968-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="9b968-180">**Leisti neigiamas atsargas:** *Išvalyti šį žymės langelį (=Ne)*</span><span class="sxs-lookup"><span data-stu-id="9b968-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="9b968-181">**Paketas įjungtas:** *Išvalykite šį žymės langelį (=Ne)*</span><span class="sxs-lookup"><span data-stu-id="9b968-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="9b968-182">**Strategija:** *Nėra*</span><span class="sxs-lookup"><span data-stu-id="9b968-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="9b968-183">Kol renkamasi nauja eilutė, virš tinklelio pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="9b968-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="9b968-184">Dialogo lango **Diapazonas** skirtuke pasirinkite **Pridėti** eilutei pridėti į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="9b968-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="9b968-185">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9b968-186">**Lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="9b968-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="9b968-187">**Išvestinė lentelė:** *Vietos*</span><span class="sxs-lookup"><span data-stu-id="9b968-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="9b968-188">**Laukas:** *Vietos profilio ID*</span><span class="sxs-lookup"><span data-stu-id="9b968-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="9b968-189">**Kriterijai:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="9b968-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="9b968-190">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-190">Select **OK**.</span></span>
1. <span data-ttu-id="9b968-191">Veiksmų srities puslapyje **Vietos nurodymai** pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="9b968-192">Jei skirtuko **Vietos nurodymai**„FastTab“ lauke **Strategija** pasirinkta vietos strategija yra *Konsolidavimas* nustatymo **Leidžiamų produktų dimensijos maišymas** **Vietos profiliuose** nebus paisoma, o prekės bus pridėtos į tą pačią vietą, net jei šis veiksmas neleidžiamas pagal nustatymą.</span><span class="sxs-lookup"><span data-stu-id="9b968-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="9b968-193">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b968-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="9b968-194">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="9b968-195">Veiksmų srityje pasirinkite **Nauja** meniu elemento, naudojamo rūšiavimui, sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="9b968-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="9b968-196">Antraštėje nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="9b968-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="9b968-197">**Meniu elemento pavadinimas:** *PU eilutės gavimas*</span><span class="sxs-lookup"><span data-stu-id="9b968-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="9b968-198">**Pavadinimas:** *PU eilutės gavimas*</span><span class="sxs-lookup"><span data-stu-id="9b968-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="9b968-199">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="9b968-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="9b968-200">**Naudoti sukurtą darbą:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="9b968-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="9b968-201">„FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="9b968-202">**Darbo sukūrimo procesas:** *Pirkimo užsakymo eilutės gavimas ir paėmimas*</span><span class="sxs-lookup"><span data-stu-id="9b968-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="9b968-203">**Generuoti numerio lentelę:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="9b968-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="9b968-204">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="9b968-205">Mobiliojo įrenginio meniu konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9b968-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="9b968-206">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="9b968-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="9b968-207">Iš meniu sąrašo pasirinkite **Gaunama**.</span><span class="sxs-lookup"><span data-stu-id="9b968-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="9b968-208">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9b968-209">Iš **Galimų meniu ir meniu elementų** sąrašo suraskite ir pasirinkite **PU eilutės gavimo** meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="9b968-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="9b968-210">Pasirinkti dešiniosios rodyklės mygtuką **PU eilutės gavimo** meniu elementui perkelti į **Meniu struktūros** sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9b968-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="9b968-211">Tokiu būdu prie pasirinkto meniu pridėsite naują meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="9b968-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="9b968-212">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="9b968-213">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="9b968-213">Scenario</span></span>

<span data-ttu-id="9b968-214">Šis parodomasis scenarijus parodo, kaip du skirtingi produkto variantai gali būti pridėdami į tą pačią vietą, tuo atveju, kai vietos profilis neleidžia maišyti prekių, bet *Vietos produkto dimensijos maišymo* funkcija yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="9b968-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="9b968-215">Šiuo atveju kaip kriterijų naudosite **Dydžio** variantą.</span><span class="sxs-lookup"><span data-stu-id="9b968-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="9b968-216">Prieš pradėdami įsitikinkite, kad *24* sandėlyje yra tuščių vietų, naudojančių *BULK* vietos profilį.</span><span class="sxs-lookup"><span data-stu-id="9b968-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="9b968-217">Pirkimo užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b968-217">Create a purchase order</span></span>

<span data-ttu-id="9b968-218">Jūs sukursite pirkimo užsakymas, turintį tris eilutes: dvi eilutės yra to pačio produkto numerio, tačiau skirtingų **Dydžio** variantų, o trečia eilutė yra skirta skirtingiems produktams, kuriuose nėra variantų.</span><span class="sxs-lookup"><span data-stu-id="9b968-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="9b968-219">Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="9b968-220">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9b968-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b968-221">Dialogo lange **Sukurti pirkimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="9b968-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b968-222">**Tiekėjo paskyra:** *1001*</span><span class="sxs-lookup"><span data-stu-id="9b968-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="9b968-223">**Sandėlis:** *24*</span><span class="sxs-lookup"><span data-stu-id="9b968-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="9b968-224">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b968-224">Select **OK**.</span></span>
1. <span data-ttu-id="9b968-225">Sukuriamas pirkimo užsakymas, o nauja eilutė yra įtraukiama į **Pirkimo užsakymo eilutės** „FastTab“ skirtuką.</span><span class="sxs-lookup"><span data-stu-id="9b968-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="9b968-226">Pasižymėkite pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="9b968-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="9b968-227">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9b968-228">**Prekės numeris:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="9b968-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="9b968-229">**Dydis** *L*</span><span class="sxs-lookup"><span data-stu-id="9b968-229">**Size** *L*</span></span>
    - <span data-ttu-id="9b968-230">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="9b968-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="9b968-231">Pasirinkite **Pridėti eilutę** antram pirkimo užsakymui pridėti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="9b968-232">**Prekės numeris:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="9b968-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="9b968-233">**Dydis** *XL*</span><span class="sxs-lookup"><span data-stu-id="9b968-233">**Size** *XL*</span></span>
    - <span data-ttu-id="9b968-234">**Kiekis:** *2*</span><span class="sxs-lookup"><span data-stu-id="9b968-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="9b968-235">Pasirinkite **Pridėti eilutę** trečiam pirkimo užsakymui pridėti ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b968-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="9b968-236">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9b968-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="9b968-237">**Kiekis:** *1*</span><span class="sxs-lookup"><span data-stu-id="9b968-237">**Quantity:** *1*</span></span>

<span data-ttu-id="9b968-238">1. Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9b968-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="9b968-239">Pirkimo užsakymo eilutės gavimas „Warehousing“ programoje</span><span class="sxs-lookup"><span data-stu-id="9b968-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="9b968-240">Prisijunkite prie „Warehousing“ programos kaip vartotojas, įgalintas sandėliui *24*.</span><span class="sxs-lookup"><span data-stu-id="9b968-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="9b968-241">Pasirinkite **Gaunama** meniu.</span><span class="sxs-lookup"><span data-stu-id="9b968-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="9b968-242">Pasirinkite: **PU eilutės gavimas**.</span><span class="sxs-lookup"><span data-stu-id="9b968-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="9b968-243">Pasirinkite lauką **PU numeris** ir įveskite pirkimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="9b968-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="9b968-244">Patvirtinkite savo įrašą pasirinkdami mygtuką patvirtinti (✔) puslapio apačioje.</span><span class="sxs-lookup"><span data-stu-id="9b968-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="9b968-245">Įveskite eilutės numerį iš gaunamo pirkimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="9b968-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="9b968-246">Pasirinkite lauką **Eilutės numeris** ir naudodami skaičių klaviatūrą, įveskite *1*.</span><span class="sxs-lookup"><span data-stu-id="9b968-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="9b968-247">Patvirtinkite savo įrašą.</span><span class="sxs-lookup"><span data-stu-id="9b968-247">Confirm your entry.</span></span>
1. <span data-ttu-id="9b968-248">Įvesti gaunamą kiekį.</span><span class="sxs-lookup"><span data-stu-id="9b968-248">Enter the quantity to receive.</span></span> <span data-ttu-id="9b968-249">Pasirinkite pliuso ženklo (**+**) mygtuką du kartus, kad padidintumėte vertę lauke **Kiekis** į *2*.</span><span class="sxs-lookup"><span data-stu-id="9b968-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="9b968-250">Užregistruokite savo įrašą pasirinkdami mygtuką (✔) puslapio apačioje ir patvirtinkite savo įrašą pasirinkdami mygtuką (✔) dar kartą.</span><span class="sxs-lookup"><span data-stu-id="9b968-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="9b968-251">Peržiūrėkite informaciją **Pirkimo užsakymus: Paėmimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9b968-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="9b968-252">Šiame puslapyje rodomas darbas, sukurtas prekių paėmimui (1 darbas).</span><span class="sxs-lookup"><span data-stu-id="9b968-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="9b968-253">Bus rodoma neseniai užbaigtos **PU eilutės gavimo** užduoties vieta, kurioje bus padėta gaunama prekė, numerio lentelė, prekė, dydis ir kiekis.</span><span class="sxs-lookup"><span data-stu-id="9b968-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="9b968-254">Paėmimo darbo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="9b968-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="9b968-255">Pakartokite 4-11 žingsnius 2 pirkimo užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="9b968-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="9b968-256">Tačiau 8 žingsnyje nustatykite kiekį į *1*.</span><span class="sxs-lookup"><span data-stu-id="9b968-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="9b968-257">Naujas paėmimo darbas (2 darbas) yra sukuriamas toje pačioje vietoje kaip 1 darbas.</span><span class="sxs-lookup"><span data-stu-id="9b968-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="9b968-258">Pakartokite 4-11 žingsnius dar sykį 2 pirkimo užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="9b968-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="9b968-259">8 žingsnyje nustatykite likusį kiekį į *1*.</span><span class="sxs-lookup"><span data-stu-id="9b968-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="9b968-260">Naujas paėmimo darbas (3 darbas) yra sukuriamas toje pačioje vietoje kaip 1 darbas ir 2 darbas.</span><span class="sxs-lookup"><span data-stu-id="9b968-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="9b968-261">Taip atsitinka, nes yra naudojama *Konsolidavimo* vietos nurodymo strategija, o „FastTab“ skirtuko **Leidžiamo produkto dimensijos maišymas**, esančio *Krovinys* **Vietos profiliai**, nustatymas leidžia vietoje maišyti **Dydžio** variantą.</span><span class="sxs-lookup"><span data-stu-id="9b968-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="9b968-262">Pakartokite 4-11 žingsnius 3 pirkimo užsakymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="9b968-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="9b968-263">8 žingsnyje nustatykite kiekį į *1,* skirtą prekės numeriui *A0001*.</span><span class="sxs-lookup"><span data-stu-id="9b968-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="9b968-264">Naujas paėmimo darbas (4 darbas) sukuriamas skirtingai vietai, nei ta, kuri yra naudojama 1 ir 2 pirkimo užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="9b968-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="9b968-265">Taip atsitinka, nes vietos profilis neleidžia maišyti produktų, bet leidžia maišyti tos pačio bendrojo produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="9b968-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="9b968-266">Puslapio viršuje pasirinkite meniu mygtuką (kartais jis vadinamas Hamburger arba Hamburger mygtuku) ir tada pasirinkite **Atšaukti,** kad išeitumėte iš **PU eilutės gavimo**.</span><span class="sxs-lookup"><span data-stu-id="9b968-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="9b968-267">Galite pakartoti šį scenarijų, bet šį kartą nustatykite *KROVINYS* **Vietos profiliai** „FastTab“ skirtuko **Leisti produkto dimensijos maišymą** **Dydį** - *Ne*, kad nebūtų galima maišyti nė vienos produkto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="9b968-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="9b968-268">Tokiu atveju, kai gausite pirkimo užsakymą, kiekvienas produkto variantas bus įtrauktas į naują vietą.</span><span class="sxs-lookup"><span data-stu-id="9b968-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>