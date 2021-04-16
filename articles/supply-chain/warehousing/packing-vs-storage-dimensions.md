---
title: Skirtingų pakavimo ir saugojimo dimensijų nustatymas
description: Šioje temoje aprašoma, kaip nurodyti, kuriam procesui (pakavimui, saugojimui ar įdėtajam pakavimui) naudojama kiekviena nurodyta dimensija.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e997f8bccde7856303d8b3c6407143598ccc6030
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818925"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="9b502-103">Skirtingų pakavimo ir saugojimo dimensijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="9b502-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b502-104">Kai kurios prekės yra supakuotos arba saugomos taip, kad jums gali reikėti sekti kiekvieno iš kelių skirtingų procesų faktines dimensijas atskirai.</span><span class="sxs-lookup"><span data-stu-id="9b502-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="9b502-105">Funkcija *Produkto pakavimo dimensijos* leidžia jums nustatyti vieną ar kelis kiekvieno produkto dimensijų tipus.</span><span class="sxs-lookup"><span data-stu-id="9b502-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="9b502-106">Kiekvienas dimensijos tipas pateikia faktinių matavimų (svorio, pločio, gylio ir aukščio) rinkinį ir nustato procesą, kuriame taikomos šių faktinių matavimų vertės.</span><span class="sxs-lookup"><span data-stu-id="9b502-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="9b502-107">Kai ši funkcija yra įgalinta, jūsų sistema palaiko šiuos dimensijų tipus:</span><span class="sxs-lookup"><span data-stu-id="9b502-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="9b502-108">*Saugojimas* – saugojimo dimensijos naudojamos kartu su vietos tūrio metrikomis, siekiant nustatyti, kiek kiekvienos prekės vienetų galima saugoti įvairiose sandėlio vietose.</span><span class="sxs-lookup"><span data-stu-id="9b502-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="9b502-109">*Pakavimas* – pakavimo dimensijos naudojamos krovimo į konteineriu ir rankinio pakavimo proceso metu, siekiant nustatyti, kiek kiekvienos prekės vienetų tilptų į įvairiems konteinerių tipus.</span><span class="sxs-lookup"><span data-stu-id="9b502-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="9b502-110">*Įdėtasis pakavimas* – įdėtojo pakavimo dimensijos naudojamos, kai pakavimo procese yra keli lygiai.</span><span class="sxs-lookup"><span data-stu-id="9b502-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="9b502-111">*Saugojimo* dimensijos palaikomos net tada, kai funkcija *Produkto pakavimo dimensijos* nėra įgalinta.</span><span class="sxs-lookup"><span data-stu-id="9b502-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="9b502-112">Jas nustatote naudodami **Faktinės dimensijos** „Supply Chain Management” puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b502-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="9b502-113">Šios dimensijos naudojamos visuose procesuose, kuriuose nenurodytos pakavimo ir įdėtojo pakavimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="9b502-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="9b502-114">*Pakavimo* ir *Įdėtojo pakavimo* dimensijos yra nustatomos naudojant **Faktinės produkto dimensijos** puslapį, kuris įtraukiamas įgalinus *Produkto pakavimo dimensijų* funkciją.</span><span class="sxs-lookup"><span data-stu-id="9b502-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="9b502-115">Šioje temoje pateikiamas scenarijus, iliustruojantis šios funkcijos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="9b502-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="9b502-116">Produkto pakavimo dimensijų funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="9b502-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="9b502-117">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="9b502-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9b502-118">Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="9b502-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9b502-119">Ten ši funkcija pateikiama taip:</span><span class="sxs-lookup"><span data-stu-id="9b502-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9b502-120">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="9b502-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9b502-121">**Funkcijos pavadinimas:** *Produkto pakavimo dimensijos*</span><span class="sxs-lookup"><span data-stu-id="9b502-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9b502-122">Pavyzdinis scenarijus</span><span class="sxs-lookup"><span data-stu-id="9b502-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="9b502-123">Scenarijaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="9b502-123">Set up the scenario</span></span>

<span data-ttu-id="9b502-124">Prieš vykdydami pavyzdinį scenarijų, turite paruošti savo sistemą, kaip aprašyta šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="9b502-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="9b502-125">Demonstracinių duomenų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="9b502-125">Enable demo data</span></span>

<span data-ttu-id="9b502-126">Norėdami dirbti pagal šį scenarijų, naudodami čia nurodytus demonstracinius įrašus ir vertes, turite būti sistemoje su įdiegtais standartiniais [demonstraciniais duomenimis](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9b502-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="9b502-127">Be to, prieš pradedant turite pasirinkti *„USMF”* juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="9b502-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="9b502-128">Produkto faktinės dimensijos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9b502-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="9b502-129">Įtraukite naują produkto faktinę dimensiją, atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="9b502-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="9b502-130">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="9b502-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9b502-131">Pasirinkite produktą su **Prekės numeriu** *„A0001”*.</span><span class="sxs-lookup"><span data-stu-id="9b502-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="9b502-132">Veiksmų srityje atidarykite **Inventoriaus valdymo** skirtuką ir iš **Sandėlio** grupės, pasirinkite **Faktinės produkto dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="9b502-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="9b502-133">Atidaromas **Faktinės produkto dimensijos** puslapis.</span><span class="sxs-lookup"><span data-stu-id="9b502-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="9b502-134">Veiksmų srityje pasirinkite **Naujas** norėdami įtraukti naują dimensiją į tinklelį su šiais parametrais:</span><span class="sxs-lookup"><span data-stu-id="9b502-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="9b502-135">**Faktinės dimensijos tipas** - *Pakavimas*</span><span class="sxs-lookup"><span data-stu-id="9b502-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="9b502-136">**Faktinis vienetas** - *vnt*</span><span class="sxs-lookup"><span data-stu-id="9b502-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="9b502-137">**Svoris** - *4'*</span><span class="sxs-lookup"><span data-stu-id="9b502-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="9b502-138">**Svorio vienetas** - *kg'*</span><span class="sxs-lookup"><span data-stu-id="9b502-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="9b502-139">**Gylis** - *3'*</span><span class="sxs-lookup"><span data-stu-id="9b502-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="9b502-140">**Aukštis** - *4'*</span><span class="sxs-lookup"><span data-stu-id="9b502-140">**Height** - *4*</span></span>
    - <span data-ttu-id="9b502-141">**Plotis** - *3'*</span><span class="sxs-lookup"><span data-stu-id="9b502-141">**Width** - *3*</span></span>
    - <span data-ttu-id="9b502-142">**Ilgis** - *cm'*</span><span class="sxs-lookup"><span data-stu-id="9b502-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="9b502-143">**Tūrio vienetas** - *cm3'*</span><span class="sxs-lookup"><span data-stu-id="9b502-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="9b502-144">Laukas **Tūris** apskaičiuojamas automatiškai pagal jūsų **Gylio**, **Aukščio** ir **Pločio** parametrus.</span><span class="sxs-lookup"><span data-stu-id="9b502-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="9b502-145">Naujo konteinerio tipo kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b502-145">Create a new container type</span></span>

<span data-ttu-id="9b502-146">Eikite į **Sandėlio valdymas \> Sąranka \> Konteineris \> Konteinerių tipai** ir sukurkite naują įrašą su šiais parametrais:</span><span class="sxs-lookup"><span data-stu-id="9b502-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="9b502-147">**Konteinerio tipo kodas** - *Trumpa dėžė*</span><span class="sxs-lookup"><span data-stu-id="9b502-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="9b502-148">**Aprašymas** - *Trumpa dėžė*</span><span class="sxs-lookup"><span data-stu-id="9b502-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="9b502-149">**Didžiausias grynasis svoris** - *50'*</span><span class="sxs-lookup"><span data-stu-id="9b502-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="9b502-150">**Tūris** - *144'*</span><span class="sxs-lookup"><span data-stu-id="9b502-150">**Volume** - *144*</span></span>
- <span data-ttu-id="9b502-151">**Ilgis** - *6'*</span><span class="sxs-lookup"><span data-stu-id="9b502-151">**Length** - *6*</span></span>
- <span data-ttu-id="9b502-152">**Plotis** - *6'*</span><span class="sxs-lookup"><span data-stu-id="9b502-152">**Width** - *6*</span></span>
- <span data-ttu-id="9b502-153">**Aukštis** - *4'*</span><span class="sxs-lookup"><span data-stu-id="9b502-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="9b502-154">Konteinerių grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b502-154">Create a container group</span></span>

<span data-ttu-id="9b502-155">Eikite į **Sandėlio valdymas \> Sąranka \> Konteineris \> Konteinerių grupės** ir sukurkite naują įrašą su šiais parametrais:</span><span class="sxs-lookup"><span data-stu-id="9b502-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="9b502-156">**Konteinerių grupės ID** - *Trumpa dėžė*</span><span class="sxs-lookup"><span data-stu-id="9b502-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="9b502-157">**Aprašymas** - *Trumpa dėžė*</span><span class="sxs-lookup"><span data-stu-id="9b502-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="9b502-158">Įtraukite naują eilutę į **Išsamios informacijos** skyrių.</span><span class="sxs-lookup"><span data-stu-id="9b502-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="9b502-159">Nustatykite **Konteinerio tipą** į *Trumpa dėžė*.</span><span class="sxs-lookup"><span data-stu-id="9b502-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="9b502-160">Konteinerio kūrimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="9b502-160">Set up a container build template</span></span>

<span data-ttu-id="9b502-161">Eikite į **Sandėlio valdymas \> Sąranka \> Konteineriai \> Konteinerių kūrimo šablonai** ir pasirinkite **Dėžės**.</span><span class="sxs-lookup"><span data-stu-id="9b502-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="9b502-162">Pakeiskite **Konteinerių grupės ID** į *Trumpa dėžė*.</span><span class="sxs-lookup"><span data-stu-id="9b502-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="9b502-163">Scenarijaus vykdymas</span><span class="sxs-lookup"><span data-stu-id="9b502-163">Run the scenario</span></span>

<span data-ttu-id="9b502-164">Parengę sistemą, kaip aprašyta ankstesniame skyriuje, esate pasiruošę vykdyti scenarijų, kaip aprašyta kitame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="9b502-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="9b502-165">Pardavimo užsakymo ir siuntos kūrimas</span><span class="sxs-lookup"><span data-stu-id="9b502-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="9b502-166">Šio proceso metu jūs sukursite siuntą pagal prekės *Pakavimo* dimensijas su aukščiu mažesniu nei 3.</span><span class="sxs-lookup"><span data-stu-id="9b502-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="9b502-167">Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="9b502-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9b502-168">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9b502-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9b502-169">Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:</span><span class="sxs-lookup"><span data-stu-id="9b502-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9b502-170">**Kliento sąskaita:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9b502-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9b502-171">**Sandėlis:** *63*</span><span class="sxs-lookup"><span data-stu-id="9b502-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="9b502-172">Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.</span><span class="sxs-lookup"><span data-stu-id="9b502-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="9b502-173">Naujas pardavimo užsakymas yra atidarytas.</span><span class="sxs-lookup"><span data-stu-id="9b502-173">The new sales order is opened.</span></span> <span data-ttu-id="9b502-174">Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="9b502-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="9b502-175">Šioje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="9b502-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="9b502-176">**Prekės numeris:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9b502-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="9b502-177">**Kiekis:** *5*</span><span class="sxs-lookup"><span data-stu-id="9b502-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="9b502-178">**Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.</span><span class="sxs-lookup"><span data-stu-id="9b502-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="9b502-179">**Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="9b502-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="9b502-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9b502-180">Close the page.</span></span>
1. <span data-ttu-id="9b502-181">Veiksmų srityje atidarykite skirtuką **Sandėlis** ir pasirinkite **Išleisti į sandėlį** sandėlio darbo užduočiai sukurti.</span><span class="sxs-lookup"><span data-stu-id="9b502-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="9b502-182">„FastTab” **Pardavimų užsakymų eilutės** pasirinkite **Sandėlis \> Siuntimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="9b502-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="9b502-183">Veiksmų srityje atidarykite skirtuką **Transportavimas** ir pasirinkite **Rodyti konteinerius**.</span><span class="sxs-lookup"><span data-stu-id="9b502-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="9b502-184">Patvirtinkite, kad prekė buvo sudėta į du *Trumpos dėžės* konteinerius.</span><span class="sxs-lookup"><span data-stu-id="9b502-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="9b502-185">Prekės patalpinimas į saugyklą</span><span class="sxs-lookup"><span data-stu-id="9b502-185">Place an item into storage</span></span>

1. <span data-ttu-id="9b502-186">Atidarykite mobilųjį įrenginį, prisijunkite prie 63 sandėlio ir eikite į **Atsargos \> Koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="9b502-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="9b502-187">Įveskite **Vieta** = *TRUMPA-01*.</span><span class="sxs-lookup"><span data-stu-id="9b502-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="9b502-188">Sukurkite naują numerio lentelę su **Preke** = *„A0001”* ir **Kiekiu** = *1 vnt*.</span><span class="sxs-lookup"><span data-stu-id="9b502-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="9b502-189">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9b502-189">Select **OK**.</span></span> <span data-ttu-id="9b502-190">Gausite klaidą „Vieta TRUMPA-01 nepavyko, nes prekė „A0001” neatitinka nurodytų vietos dimensijų.”</span><span class="sxs-lookup"><span data-stu-id="9b502-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="9b502-191">Taip nutinka dėl to, kad produkto *Saugojimo* tipo dimensijos yra didesnės nei vietos profilyje nurodytos dimensijos.</span><span class="sxs-lookup"><span data-stu-id="9b502-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]