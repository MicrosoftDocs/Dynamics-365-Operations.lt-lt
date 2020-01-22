---
title: Paėmimo eilutės grupavimas
description: Šioje temoje pateikiama paėmimo eilutės grupavimo apžvalga.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906273"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="4d45b-103">Paėmimo eilutės grupavimas</span><span class="sxs-lookup"><span data-stu-id="4d45b-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d45b-104">Vykdant paėmimo eilutės grupavimą, keletą darbo eilučių, kuriose yra ta pati prekė ir vieta, galima sujungti į vieną paėmimą, kuris pateikiamas vartotojui mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="4d45b-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="4d45b-105">Todėl sandėlio darbininkai gali gauti kuo naudingesnes instrukcijas, tačiau išlaikomas ir būtinas darbo eilučių atskyrimas sistemoje (pavyzdžiui, skirtingų konteinerių ir užsakymų atveju).</span><span class="sxs-lookup"><span data-stu-id="4d45b-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="4d45b-106">Paėmimo eilutės grupavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d45b-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="4d45b-107">Mobiliojo įrenginio meniu elemento kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d45b-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="4d45b-108">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai** ir sukurkite naują meniu elementą, pavadintą **Pardavimo grupės eilutės išrinkimas – vartotojo nurodyta**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**, and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="4d45b-109">Dalyje **Mobiliojo įrenginio meniu elementai** nustatykite toliau pateikiamas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d45b-109">Under **Mobile device menu items**, set the following values:</span></span>

    - <span data-ttu-id="4d45b-110">Lauke **Meniu elemento pavadinimas** įveskite **Pardavimo paėmimas - grupės eilutė**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="4d45b-111">Lauke **Pavadinimas** įveskite **Pardavimo paėmimas - grupės eilutė**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="4d45b-112">Lauke **Režimas** pasirinkite **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="4d45b-113">Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="4d45b-114">„FastTab“ **Bendra** galite nustatyti toliau pateikiamas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d45b-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="4d45b-115">Lauke **Nukreipė** pasirinkite **Vartotojo nurodyta**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="4d45b-116">Nustatykite parinkties **Generuoti numerio lentelę** vertę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="4d45b-117">Nustatykite parinkties **Grupinis paėmimas** vertę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="4d45b-118">„FastTab“ **Darbo klasės** atlikite toliau pateikiamus veiksmus, kad sukonfigūruotumėte mobiliojo įrenginio meniu elemento tinkamas darbo klases.</span><span class="sxs-lookup"><span data-stu-id="4d45b-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="4d45b-119">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-119">Select **New**.</span></span>
    2. <span data-ttu-id="4d45b-120">Lauke **Darbo klasės ID** pasirinkite **Pardavimas** arba **PrdU paėmimas**, atsižvelgiant į sandėlį, kurį naudosite.</span><span class="sxs-lookup"><span data-stu-id="4d45b-120">In the **Work class ID** field, select **Sales** or **SO Pick**, depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="4d45b-121">Lauke **Darbo užsakymo tipas** pasirinkite **Pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="4d45b-122">Mobiliojo įrenginio meniu nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d45b-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="4d45b-123">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="4d45b-124">Įtraukite meniu elementą, kurį ką tik sukūrėte, į norimą meniu.</span><span class="sxs-lookup"><span data-stu-id="4d45b-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="4d45b-125">Darbo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="4d45b-125">Set up a work template</span></span>

1. <span data-ttu-id="4d45b-126">Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="4d45b-127">Raskite darbo šabloną, kuris turėtų būti naudojamas atliekant šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="4d45b-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="4d45b-128">Šiame pavyzdyje pasirinkite standartinį **51 Paimti į etapą** „Contoso“ darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="4d45b-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="4d45b-129">Meniu pasirinkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="4d45b-130">Skirtuke **Rūšiavimas** pasirinkite **Įtraukti**, tada nustatykite toliau pateikiamas vertes.</span><span class="sxs-lookup"><span data-stu-id="4d45b-130">On the **Sorting** tab, select **Add**, and then set the following values:</span></span>

    - <span data-ttu-id="4d45b-131">Lauke **Lentelė** pasirinkite **Laikinos darbo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="4d45b-132">Lauke **Išvestinė lentelė** pasirinkite **Laikinos darbo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="4d45b-133">Lauke **Laukas** pasirinkite **Prekės numeris**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="4d45b-134">Lauke **Ieškos kryptis** pasirinkite **Didėjimo tvarka**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="4d45b-135">Norint, kad paėmimo eilutės grupavimo funkcija veiktų, darbo eilutės turi būti surūšiuotos pagal prekės ID.</span><span class="sxs-lookup"><span data-stu-id="4d45b-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="4d45b-136">Jei eilutės, kuriose yra tos pačios prekės, nepateikiamos viena po kitos, jos nebus grupuojamos.</span><span class="sxs-lookup"><span data-stu-id="4d45b-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="4d45b-137">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="4d45b-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="4d45b-138">Paėmimo darbo kūrimas</span><span class="sxs-lookup"><span data-stu-id="4d45b-138">Create picking work</span></span>

<span data-ttu-id="4d45b-139">Kad galėtumėte nustatyti paėmimo eilutės grupavimą, turite sukurti tinkamą siuntimo darbą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="4d45b-140">Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="4d45b-141">Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="4d45b-142">Lauke **Kliento sąskaita** pasirinkite bet kurį klientą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="4d45b-143">„FastTab“ **Bendra** lauke **Sandėlis** pasirinkite **51**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="4d45b-144">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-144">Then select **OK**.</span></span>
5. <span data-ttu-id="4d45b-145">Dalyje **Pardavimo užsakymo eilutės** įtraukite toliau pateikiamas šešias eilutes.</span><span class="sxs-lookup"><span data-stu-id="4d45b-145">Under **Sales order lines**, add the following six lines:</span></span>

    - <span data-ttu-id="4d45b-146">**1 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="4d45b-147">Lauke **Kiekis** įveskite **3**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="4d45b-148">**2 eilutė.** Lauke **Prekės numeris** pasirinkite **M9201**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="4d45b-149">Lauke **Kiekis** įveskite **3**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="4d45b-150">**3 eilutė.** Lauke **Prekės numeris** pasirinkite **M9202**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="4d45b-151">Lauke **Kiekis** įveskite **2**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="4d45b-152">**4 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="4d45b-153">Lauke **Kiekis** įveskite **1**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="4d45b-154">**5 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="4d45b-155">Lauke **Kiekis** įveskite **3**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="4d45b-156">**6 eilutė.** Lauke **Prekės numeris** pasirinkite **M9202**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="4d45b-157">Lauke **Kiekis** įveskite **7**.</span><span class="sxs-lookup"><span data-stu-id="4d45b-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="4d45b-158">Toliau pateikiama kiekvienos prekės bendro kiekio suvestinė.</span><span class="sxs-lookup"><span data-stu-id="4d45b-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="4d45b-159">**Prekė M9200:** 7 vienetai</span><span class="sxs-lookup"><span data-stu-id="4d45b-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="4d45b-160">**Prekė M9201:** 3 vienetai</span><span class="sxs-lookup"><span data-stu-id="4d45b-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="4d45b-161">**Prekė M9202:** 9 vienetai</span><span class="sxs-lookup"><span data-stu-id="4d45b-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="4d45b-162">Prieš perduodami užsakymus į sandėlį, turite įsitikinti, kad paėmimo vietose pakanka atsargų visoms prekėms visuose užsakymuose pateikti.</span><span class="sxs-lookup"><span data-stu-id="4d45b-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="4d45b-163">Patikrinkite parametrą **Vietos nurodymas**, kad nustatytumėte paėmimo vietas, naudojamas pardavimo užsakymo paėmimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="4d45b-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="4d45b-164">Rezervuokite atsargas ir pateikite jas į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="4d45b-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="4d45b-165">Sukuriamas darbo ID, kuriame yra šešios eilutės.</span><span class="sxs-lookup"><span data-stu-id="4d45b-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="4d45b-166">Eilutės rūšiuojamos pagal prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="4d45b-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="4d45b-167">Mobiliojo įrenginio srauto vykdymas</span><span class="sxs-lookup"><span data-stu-id="4d45b-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="4d45b-168">Mobiliajame įrenginyje pasirinkite meniu, kuriame yra naujas mobiliojo įrenginio meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="4d45b-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="4d45b-169">Pasirinkite meniu elementą **Pardavimo paėmimas – grupės eilutė** ir inicijuokite paėmimą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="4d45b-170">Pasirinkę meniu ir įvedę darbo ID, pamatysite paėmimo veiksmą, kurį vykdant visos prekės M9200 paėmimo eilutės grupuojamos.</span><span class="sxs-lookup"><span data-stu-id="4d45b-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="4d45b-171">Gaunate nurodymą paimti prekės M9200 7 vienetus.</span><span class="sxs-lookup"><span data-stu-id="4d45b-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="4d45b-172">Patvirtinkite paėmimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="4d45b-173">Perėję į atliekamo darbo kliento ekraną, pastebėsite, kad visos trys prekės M9200 paėmimo eilutės buvo uždarytos vienu metu.</span><span class="sxs-lookup"><span data-stu-id="4d45b-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="4d45b-174">Pateikiama 4 darbo eilutė.</span><span class="sxs-lookup"><span data-stu-id="4d45b-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="4d45b-175">Patvirtinkite paėmimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-175">Confirm the pick step.</span></span>

    <span data-ttu-id="4d45b-176">Per paskutinį paėmimo veiksmą mobiliajame įrenginyje sujungiamos dvi paskutinės darbo užsakymo paėmimo eilutės.</span><span class="sxs-lookup"><span data-stu-id="4d45b-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="4d45b-177">Atlikite paėmimo veiksmą prekės M9202 9 vienetų atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="4d45b-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="4d45b-178">Patvirtinkite padėjimo veiksmą ir visas papildomas paėmimo / padėjimo poras, kad užbaigtumėte darbą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="4d45b-179">Darbo eilutes galima grupuoti tik tuo atveju, jei jos pateikiamos iš eilės.</span><span class="sxs-lookup"><span data-stu-id="4d45b-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="4d45b-180">Toliau nurodytos funkcijos nepalaikomos.</span><span class="sxs-lookup"><span data-stu-id="4d45b-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="4d45b-181">Esamo svorio prekės.</span><span class="sxs-lookup"><span data-stu-id="4d45b-181">Catch-weight items.</span></span> <span data-ttu-id="4d45b-182">Jei darbe yra esamo svorio prekių, prieš pradėdami paėmimą matote klaidos pranešimą.</span><span class="sxs-lookup"><span data-stu-id="4d45b-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="4d45b-183">Vienetų paėmimo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="4d45b-183">Piece picking.</span></span>
>    - <span data-ttu-id="4d45b-184">Darbo eilutės, kuriose nebaigtas papildymo darbas.</span><span class="sxs-lookup"><span data-stu-id="4d45b-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="4d45b-185">Viršytas paėmimo kiekis.</span><span class="sxs-lookup"><span data-stu-id="4d45b-185">Over-picking.</span></span>
