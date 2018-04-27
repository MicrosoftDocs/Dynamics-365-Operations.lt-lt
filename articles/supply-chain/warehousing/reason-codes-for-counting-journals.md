---
title: "Atsargų skaičiavimo priežasčių kodai"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti atsargų skaičiavimo priežasčių kodus."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe01425fa236655731e6e0723f3a1e57c05035cc
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="08018-103">Atsargų skaičiavimo priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="08018-103">Reason codes for inventory counting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="08018-104">Priežasčių kodai suteikia galimybę analizuoti skaičiavimo procesą rezultatus ir visus to proceso metu įvykusius neatitikimus.</span><span class="sxs-lookup"><span data-stu-id="08018-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="08018-105">Galite nurodyti skaičiavimo priežastį, pvz., sugadintas padėklas arba atsargų koregavimas, pagal atsargų pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="08018-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="08018-106">Rekomendacija</span><span class="sxs-lookup"><span data-stu-id="08018-106">Recommendation</span></span>

<span data-ttu-id="08018-107">Prieš nustatant sistemą rekomenduojame nustatyti darbo su priežasčių kodais strategiją.</span><span class="sxs-lookup"><span data-stu-id="08018-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="08018-108">Pavyzdžiui, pabandykite atsakyti į toliau nurodytus klausimus.</span><span class="sxs-lookup"><span data-stu-id="08018-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="08018-109">Ar sandėliuose priežasčių kodai turėtų būti privalomi?</span><span class="sxs-lookup"><span data-stu-id="08018-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="08018-110">Ar kai kuriose prekėse priežasčių kodai turėtų būti privalomi, ar pasirenkami?</span><span class="sxs-lookup"><span data-stu-id="08018-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="08018-111">Kiek priežasčių kodų jums reikia?</span><span class="sxs-lookup"><span data-stu-id="08018-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="08018-112">Kaip brūkšninių kodų skaitytuvų vartotojai turėtų naudoti priežasčių kodus?</span><span class="sxs-lookup"><span data-stu-id="08018-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="08018-113">Ar priežasčių kodai turėtų būti iš anksto pasirenkami, privalomi arba neredaguojami?</span><span class="sxs-lookup"><span data-stu-id="08018-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="08018-114">Ar sandėlio darbuotojams reikalingi skirtingų tipų priežasčių kodai mobiliuosiuose skaitytuvuose?</span><span class="sxs-lookup"><span data-stu-id="08018-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="08018-115">Jei atsakymas teigiamas, galite kurti daugiau meniu elementų ir juos priskirti skirtingiems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="08018-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="08018-116">Kur taikomi priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="08018-116">Where reason codes apply</span></span>

<span data-ttu-id="08018-117">Galite kurti kelias priežasčių kodų strategijas ir kiekvienai priežasčių kodų strategijai galite priskirti dvi skaičiavimo priežasčių kodų strategijas.</span><span class="sxs-lookup"><span data-stu-id="08018-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="08018-118">Skaičiavimo priežasčių kodų strategijas galima naudoti sandėlio lygiu arba prekės lygiu.</span><span class="sxs-lookup"><span data-stu-id="08018-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="08018-119">Priežasčių kodų strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="08018-119">Set up reason code policies</span></span>

1. <span data-ttu-id="08018-120">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodų strategijos** ir sukurkite naują priežasčių kodų strategiją.</span><span class="sxs-lookup"><span data-stu-id="08018-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="08018-121">Lauke **Skaičiavimo priežasties kodo tipas** pasirinkite **Privalomas** arba **Pasirinktinis**, norėdami nurodyti, ar priežasties kodo pasirinkimas yra pasirinktinis, ar privalomas veiksmas viename iš toliau nurodytų skaičiavimo žurnalų.</span><span class="sxs-lookup"><span data-stu-id="08018-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="08018-122">Ciklo skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="08018-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="08018-123">Vietos skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="08018-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="08018-124">Ribinės reikšmės skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="08018-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="08018-125">Koregavimo taikymas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="08018-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="08018-126">Koregavimo atšaukimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="08018-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="08018-127">Žurnalo skaičiavimas (raiškusis klientas)</span><span class="sxs-lookup"><span data-stu-id="08018-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="08018-128">Taip pat galite nustatyti atskirų sandėlių ir produktų priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="08018-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="08018-129">Nustatant produktų priežasčių kodus galima nepaisyti sandėlių sąrankos.</span><span class="sxs-lookup"><span data-stu-id="08018-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="08018-130">Privalomi priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="08018-130">Mandatory reason codes</span></span>

<span data-ttu-id="08018-131">Jei sandėlių arba prekių priežasčių kodų konfigūracijoje nustatytas parametras **Privalomas**, žurnalo skaičiavimo negalima atlikti ir uždaryti, kol nepateiktas priežasties kodas.</span><span class="sxs-lookup"><span data-stu-id="08018-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="08018-132">Sandėlių priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="08018-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="08018-133">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargų paskirstymas** \> **Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="08018-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="08018-134">Skirtuko **Sandėlis** lauke **Skaičiavimo priežasčių kodų strategija** pasirinkite vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="08018-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="08018-135">**Tuščia** – nustatytas prekės parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="08018-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="08018-136">**Privalomas** – priežasties kodas yra visada privalomas skaičiuojant sandėlio žurnalus.</span><span class="sxs-lookup"><span data-stu-id="08018-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="08018-137">**Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant sandėlio žurnalus.</span><span class="sxs-lookup"><span data-stu-id="08018-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="08018-138">Produktų priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="08018-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="08018-139">Pasirinkite **Produkto informacijos valdymas** \> **Produktai** \> **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="08018-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="08018-140">Skirtuke **Produktas** pasirinkite **Skaičiavimo priežasčių kodų strategija**, tada pasirinkite vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="08018-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="08018-141">**Tuščia** – nustatytas sandėlio parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="08018-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="08018-142">**Privalomas** – priežasties kodas yra visada privalomas skaičiuojant produkto žurnalus.</span><span class="sxs-lookup"><span data-stu-id="08018-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="08018-143">Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.</span><span class="sxs-lookup"><span data-stu-id="08018-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="08018-144">**Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant produkto žurnalus.</span><span class="sxs-lookup"><span data-stu-id="08018-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="08018-145">Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.</span><span class="sxs-lookup"><span data-stu-id="08018-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="08018-146">Priežasčių kodų naudojimas skaičiavimo žurnaluose</span><span class="sxs-lookup"><span data-stu-id="08018-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="08018-147">Skaičiavimo žurnale galite įtraukti toliau nurodytų tipų skaičiavimo priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="08018-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="08018-148">Ciklo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="08018-148">Cycle Count</span></span>
- <span data-ttu-id="08018-149">Vietos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="08018-149">Spot Count</span></span>
- <span data-ttu-id="08018-150">Ribinės reikšmės skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="08018-150">Threshold Count</span></span>
- <span data-ttu-id="08018-151">Koregavimo taikymas</span><span class="sxs-lookup"><span data-stu-id="08018-151">Adjustment In</span></span>
- <span data-ttu-id="08018-152">Koregavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="08018-152">Adjustment Out</span></span>

<span data-ttu-id="08018-153">Priežasčių kodai įtraukiami į žurnalo eilutes tipo **Skaičiavimo žurnalas** skaičiavimo žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="08018-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="08018-154">Pasirinkite **Atsargų valdymas** \> **Žurnalo įrašai** \> **Prekės skaičiavimas** \> **Skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="08018-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="08018-155">Skaičiavimo žurnalo eilutės informacijos lauke **Skaičiavimo priežasties kodas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="08018-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="08018-156">Įrašytos skaičiavimo retrospektyvos peržiūra pagal priežasčių kodus</span><span class="sxs-lookup"><span data-stu-id="08018-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="08018-157">Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Skaičiavimo retrospektyva**, tada lauke **Skaičiavimo priežasties kodas** peržiūrėkite skaičiavimo retrospektyvą, kuri buvo įrašyta naudojant priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="08018-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="08018-158">Priežasties kodo naudojimas kiekiui koreguoti</span><span class="sxs-lookup"><span data-stu-id="08018-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="08018-159">Puslapyje **Turimos atsargos** pasirinkite **Koreguoti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="08018-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="08018-160">Puslapį **Turimos atsargos** galite atidaryti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="08018-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="08018-161">Pavyzdžiui, pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="08018-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="08018-162">Pasirinkite **Koreguoti kiekį**, tada lauke **Skaičiavimo priežasties kodas** pasirinkite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="08018-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="08018-163">Mobiliojo įrenginio meniu elementų priežasčių kodų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="08018-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="08018-164">Mobiliojo įrenginio meniu elemente galite konfigūruoti bet kokio tipo skaičiavimo priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="08018-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="08018-165">Mobiliojo įrenginio meniu elemento konfigūracija apima toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="08018-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="08018-166">Informacija apie tai, ar atliekant skaičiavimą priežasties kodas rodomas darbuotojui, kuriam priklauso mobilusis įrenginys.</span><span class="sxs-lookup"><span data-stu-id="08018-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="08018-167">Numatytasis priežasties kodas, rodomas mobiliojo įrenginio meniu elemente.</span><span class="sxs-lookup"><span data-stu-id="08018-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="08018-168">Informacija apie tai, ar vartotojas gali redaguoti priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="08018-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="08018-169">Priežasčių kodų nustatymas mobiliajame įrenginyje</span><span class="sxs-lookup"><span data-stu-id="08018-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="08018-170">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="08018-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="08018-171">Skirtuke **Ciklo skaičiavimas** pasirinkite **Ciklo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="08018-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="08018-172">Lauke **Numatytasis skaičiavimo priežasties kodas** nustatykite numatytąjį priežasties kodą, kuris turi būti įrašomas, kai skaičiavimas atliekamas naudojant mobiliojo įrenginio meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="08018-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="08018-173">Lauke **Rodyti skaičiavimo priežasties kodą** pasirinkite **Eilutė**, kad įrašius kiekvieną nuokrypį būtų rodomas priežasties kodas.</span><span class="sxs-lookup"><span data-stu-id="08018-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="08018-174">Taip pat galite pasirinkti **Slėpti**, jei priežasties kodas neturėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="08018-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="08018-175">Nustatykite parinkties **Redaguoti skaičiavimo priežasties kodą** reikšmę **Taip** arba **Ne**.</span><span class="sxs-lookup"><span data-stu-id="08018-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="08018-176">Jei nustatote šios parinkties reikšmę **Taip**, darbuotojas gali redaguoti priežasties kodą, kai atliekant skaičiavimą jis rodomas mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="08018-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="08018-177">Mygtuką **Ciklo skaičiavimas** galima įjungti bet kuriame mobiliojo įrenginio meniu elemente, kuriame galima atlikti skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="08018-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="08018-178">Pavyzdžiai: vietos skaičiavimo, vartotojo nurodyto darbo ir sistemos nurodyto darbo meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="08018-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="08018-179">Ciklo skaičiavimo patvirtinimai</span><span class="sxs-lookup"><span data-stu-id="08018-179">Cycle count approvals</span></span>

<span data-ttu-id="08018-180">Prieš patvirtinant skaičiavimą, vartotojas gali keisti priežasties kodą, susietą su skaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="08018-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="08018-181">Patvirtinus skaičiavimą, priežasties kodas įvedamas skaičiavimo žurnalo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="08018-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="08018-182">Ciklo skaičiavimo patvirtinimų keitimas</span><span class="sxs-lookup"><span data-stu-id="08018-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="08018-183">Pasirinkite **Sandėlio valdymas** \> **Ciklo skaičiavimas** \> **Peržiūros laukiantis ciklo skaičiavimo darbas**.</span><span class="sxs-lookup"><span data-stu-id="08018-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="08018-184">Pasirinkite **Ciklo skaičiavimas**, tada lauke **Priežasties kodas** pasirinkite naują priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="08018-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="08018-185">Procesų Koregavimo taikymas ir Koregavimo atšaukimas mobiliojo įrenginio meniu elemento keitimas</span><span class="sxs-lookup"><span data-stu-id="08018-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="08018-186">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**, tada pasirinkite **Koregavimo taikymas ir atšaukimas**.</span><span class="sxs-lookup"><span data-stu-id="08018-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="08018-187">Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="08018-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="08018-188">Lauke **Darbo kūrimo procesas** pasirinkite **Koregavimo taikymas**.</span><span class="sxs-lookup"><span data-stu-id="08018-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="08018-189">Į mobiliojo įrenginio meniu elementą bus įtraukti toliau nurodyti laukai, kai darbo kūrimo proceso metu pasirenkamas **Koregavimo taikymas** arba **Koregavimo atšaukimas**.</span><span class="sxs-lookup"><span data-stu-id="08018-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="08018-190">Numatytasis skaičiavimo priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="08018-190">Default counting reason code</span></span>
- <span data-ttu-id="08018-191">Rodyti skaičiavimo priežasties kodą</span><span class="sxs-lookup"><span data-stu-id="08018-191">Display counting reason code</span></span>
- <span data-ttu-id="08018-192">Redaguoti skaičiavimo priežasties kodą</span><span class="sxs-lookup"><span data-stu-id="08018-192">Edit counting reason code</span></span>

