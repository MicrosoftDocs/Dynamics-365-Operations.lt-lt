---
title: Atsargų skaičiavimo priežasčių kodai
description: Šioje temoje aprašoma, kaip nustatyti ir taikyti atsargų skaičiavimo priežasčių kodus.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: a6b8a686b6aee6b52b3f43caf8acae9f371f8804
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838207"
---
# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="a368c-103">Atsargų skaičiavimo priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="a368c-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a368c-104">Priežasčių kodai suteikia galimybę analizuoti skaičiavimo procesą rezultatus ir visus to proceso metu įvykusius neatitikimus.</span><span class="sxs-lookup"><span data-stu-id="a368c-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="a368c-105">Galite nurodyti skaičiavimo priežastį, pvz., sugadintas padėklas arba atsargų koregavimas, pagal atsargų pavyzdžius.</span><span class="sxs-lookup"><span data-stu-id="a368c-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="a368c-106">Rekomendacija</span><span class="sxs-lookup"><span data-stu-id="a368c-106">Recommendation</span></span>

<span data-ttu-id="a368c-107">Prieš nustatant sistemą rekomenduojame nustatyti darbo su priežasčių kodais strategiją.</span><span class="sxs-lookup"><span data-stu-id="a368c-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="a368c-108">Pavyzdžiui, pabandykite atsakyti į toliau nurodytus klausimus.</span><span class="sxs-lookup"><span data-stu-id="a368c-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="a368c-109">Ar sandėliuose priežasčių kodai turėtų būti privalomi?</span><span class="sxs-lookup"><span data-stu-id="a368c-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="a368c-110">Ar kai kuriose prekėse priežasčių kodai turėtų būti privalomi, ar pasirenkami?</span><span class="sxs-lookup"><span data-stu-id="a368c-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="a368c-111">Kiek priežasčių kodų jums reikia?</span><span class="sxs-lookup"><span data-stu-id="a368c-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="a368c-112">Kaip brūkšninių kodų skaitytuvų vartotojai turėtų naudoti priežasčių kodus?</span><span class="sxs-lookup"><span data-stu-id="a368c-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="a368c-113">Ar priežasčių kodai turėtų būti iš anksto pasirenkami, privalomi arba neredaguojami?</span><span class="sxs-lookup"><span data-stu-id="a368c-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="a368c-114">Ar sandėlio darbuotojams reikalingi skirtingų tipų priežasčių kodai mobiliuosiuose skaitytuvuose?</span><span class="sxs-lookup"><span data-stu-id="a368c-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="a368c-115">Jei atsakymas teigiamas, galite kurti daugiau meniu elementų ir juos priskirti skirtingiems žmonėms.</span><span class="sxs-lookup"><span data-stu-id="a368c-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="a368c-116">Kur taikomi priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="a368c-116">Where reason codes apply</span></span>

<span data-ttu-id="a368c-117">Galite kurti kelias priežasčių kodų strategijas ir kiekvienai priežasčių kodų strategijai galite priskirti dvi skaičiavimo priežasčių kodų strategijas.</span><span class="sxs-lookup"><span data-stu-id="a368c-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="a368c-118">Skaičiavimo priežasčių kodų strategijas galima naudoti sandėlio lygiu arba prekės lygiu.</span><span class="sxs-lookup"><span data-stu-id="a368c-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="a368c-119">Priežasčių kodų strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a368c-119">Set up reason code policies</span></span>

1. <span data-ttu-id="a368c-120">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargos** \> **Skaičiavimo priežasčių kodų strategijos** ir sukurkite naują priežasčių kodų strategiją.</span><span class="sxs-lookup"><span data-stu-id="a368c-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="a368c-121">Lauke **Skaičiavimo priežasties kodo tipas** pasirinkite **Privalomas** arba **Pasirinktinis**, norėdami nurodyti, ar priežasties kodo pasirinkimas yra pasirinktinis, ar privalomas veiksmas viename iš toliau nurodytų skaičiavimo žurnalų.</span><span class="sxs-lookup"><span data-stu-id="a368c-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="a368c-122">Ciklo skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="a368c-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="a368c-123">Vietos skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="a368c-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="a368c-124">Ribinės reikšmės skaičiavimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="a368c-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="a368c-125">Koregavimo taikymas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="a368c-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="a368c-126">Koregavimo atšaukimas (mobilusis įrenginys)</span><span class="sxs-lookup"><span data-stu-id="a368c-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="a368c-127">Žurnalo skaičiavimas (raiškusis klientas)</span><span class="sxs-lookup"><span data-stu-id="a368c-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="a368c-128">Taip pat galite nustatyti atskirų sandėlių ir produktų priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="a368c-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="a368c-129">Nustatant produktų priežasčių kodus galima nepaisyti sandėlių sąrankos.</span><span class="sxs-lookup"><span data-stu-id="a368c-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="a368c-130">Privalomi priežasčių kodai</span><span class="sxs-lookup"><span data-stu-id="a368c-130">Mandatory reason codes</span></span>

<span data-ttu-id="a368c-131">Jei sandėlių arba prekių priežasčių kodų konfigūracijoje nustatytas parametras **Privalomas**, žurnalo skaičiavimo negalima atlikti ir uždaryti, kol nepateiktas priežasties kodas.</span><span class="sxs-lookup"><span data-stu-id="a368c-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="a368c-132">Sandėlių priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a368c-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="a368c-133">Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Atsargų paskirstymas** \> **Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="a368c-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="a368c-134">Skirtuko **Sandėlis** lauke **Skaičiavimo priežasčių kodų strategija** pasirinkite vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="a368c-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="a368c-135">**Tuščia** – nustatytas prekės parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="a368c-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="a368c-136">**Privalomas** – priežasties kodas yra visada privalomas skaičiuojant sandėlio žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a368c-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="a368c-137">**Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant sandėlio žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a368c-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="a368c-138">Produktų priežasčių kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a368c-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="a368c-139">Pasirinkite **Produkto informacijos valdymas** \> **Produktai** \> **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="a368c-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="a368c-140">Skirtuke **Produktas** pasirinkite **Skaičiavimo priežasčių kodų strategija**, tada pasirinkite vieną iš toliau nurodytų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="a368c-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="a368c-141">**Tuščia** – nustatytas sandėlio parametras naudojamas nustatant, ar produkto žurnalų skaičiavimas yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="a368c-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="a368c-142">**Privalomas** – priežasties kodas yra visada privalomas skaičiuojant produkto žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a368c-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="a368c-143">Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.</span><span class="sxs-lookup"><span data-stu-id="a368c-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="a368c-144">**Pasirinktinis** – priežasties kodas nėra privalomas skaičiuojant produkto žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a368c-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="a368c-145">Šis parametras perrašo bet kokį priežasties kodo parametrą sandėlio lygiu.</span><span class="sxs-lookup"><span data-stu-id="a368c-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="a368c-146">Priežasčių kodų naudojimas skaičiavimo žurnaluose</span><span class="sxs-lookup"><span data-stu-id="a368c-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="a368c-147">Skaičiavimo žurnale galite įtraukti toliau nurodytų tipų skaičiavimo priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="a368c-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="a368c-148">Ciklo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a368c-148">Cycle Count</span></span>
- <span data-ttu-id="a368c-149">Vietos skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a368c-149">Spot Count</span></span>
- <span data-ttu-id="a368c-150">Ribinės reikšmės skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a368c-150">Threshold Count</span></span>
- <span data-ttu-id="a368c-151">Koregavimo taikymas</span><span class="sxs-lookup"><span data-stu-id="a368c-151">Adjustment In</span></span>
- <span data-ttu-id="a368c-152">Koregavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a368c-152">Adjustment Out</span></span>

<span data-ttu-id="a368c-153">Priežasčių kodai įtraukiami į žurnalo eilutes tipo **Skaičiavimo žurnalas** skaičiavimo žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="a368c-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="a368c-154">Pasirinkite **Atsargų valdymas** \> **Žurnalo įrašai** \> **Prekės skaičiavimas** \> **Skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="a368c-155">Skaičiavimo žurnalo eilutės informacijos lauke **Skaičiavimo priežasties kodas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a368c-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="a368c-156">Įrašytos skaičiavimo retrospektyvos peržiūra pagal priežasčių kodus</span><span class="sxs-lookup"><span data-stu-id="a368c-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="a368c-157">Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Skaičiavimo retrospektyva**, tada lauke **Skaičiavimo priežasties kodas** peržiūrėkite skaičiavimo retrospektyvą, kuri buvo įrašyta naudojant priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="a368c-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="a368c-158">Priežasties kodo naudojimas kiekiui koreguoti</span><span class="sxs-lookup"><span data-stu-id="a368c-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="a368c-159">Puslapyje **Turimos atsargos** pasirinkite **Koreguoti kiekį**.</span><span class="sxs-lookup"><span data-stu-id="a368c-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="a368c-160">Puslapį **Turimos atsargos** galite atidaryti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="a368c-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="a368c-161">Pavyzdžiui, pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Turimos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="a368c-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="a368c-162">Pasirinkite **Koreguoti kiekį**, tada lauke **Skaičiavimo priežasties kodas** pasirinkite priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="a368c-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="a368c-163">Mobiliojo įrenginio meniu elementų priežasčių kodų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a368c-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="a368c-164">Mobiliojo įrenginio meniu elemente galite konfigūruoti bet kokio tipo skaičiavimo priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="a368c-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="a368c-165">Mobiliojo įrenginio meniu elemento konfigūracija apima toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="a368c-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="a368c-166">Informacija apie tai, ar atliekant skaičiavimą priežasties kodas rodomas darbuotojui, kuriam priklauso mobilusis įrenginys.</span><span class="sxs-lookup"><span data-stu-id="a368c-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="a368c-167">Numatytasis priežasties kodas, rodomas mobiliojo įrenginio meniu elemente.</span><span class="sxs-lookup"><span data-stu-id="a368c-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="a368c-168">Informacija apie tai, ar vartotojas gali redaguoti priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="a368c-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="a368c-169">Priežasčių kodų nustatymas mobiliajame įrenginyje</span><span class="sxs-lookup"><span data-stu-id="a368c-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="a368c-170">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="a368c-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="a368c-171">Skirtuke **Ciklo skaičiavimas** pasirinkite **Ciklo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="a368c-172">Lauke **Numatytasis skaičiavimo priežasties kodas** nustatykite numatytąjį priežasties kodą, kuris turi būti įrašomas, kai skaičiavimas atliekamas naudojant mobiliojo įrenginio meniu elementą.</span><span class="sxs-lookup"><span data-stu-id="a368c-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="a368c-173">Lauke **Rodyti skaičiavimo priežasties kodą** pasirinkite **Eilutė**, kad įrašius kiekvieną nuokrypį būtų rodomas priežasties kodas.</span><span class="sxs-lookup"><span data-stu-id="a368c-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="a368c-174">Taip pat galite pasirinkti **Slėpti**, jei priežasties kodas neturėtų būti rodomas.</span><span class="sxs-lookup"><span data-stu-id="a368c-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="a368c-175">Nustatykite parinkties **Redaguoti skaičiavimo priežasties kodą** reikšmę **Taip** arba **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a368c-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="a368c-176">Jei nustatote šios parinkties reikšmę **Taip**, darbuotojas gali redaguoti priežasties kodą, kai atliekant skaičiavimą jis rodomas mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="a368c-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="a368c-177">Mygtuką **Ciklo skaičiavimas** galima įjungti bet kuriame mobiliojo įrenginio meniu elemente, kuriame galima atlikti skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a368c-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="a368c-178">Pavyzdžiai: vietos skaičiavimo, vartotojo nurodyto darbo ir sistemos nurodyto darbo meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="a368c-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="a368c-179">Ciklo skaičiavimo patvirtinimai</span><span class="sxs-lookup"><span data-stu-id="a368c-179">Cycle count approvals</span></span>

<span data-ttu-id="a368c-180">Prieš patvirtinant skaičiavimą, vartotojas gali keisti priežasties kodą, susietą su skaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="a368c-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="a368c-181">Patvirtinus skaičiavimą, priežasties kodas įvedamas skaičiavimo žurnalo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="a368c-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="a368c-182">Ciklo skaičiavimo patvirtinimų keitimas</span><span class="sxs-lookup"><span data-stu-id="a368c-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="a368c-183">Pasirinkite **Sandėlio valdymas** \> **Ciklo skaičiavimas** \> **Peržiūros laukiantis ciklo skaičiavimo darbas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="a368c-184">Pasirinkite **Ciklo skaičiavimas**, tada lauke **Priežasties kodas** pasirinkite naują priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="a368c-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="a368c-185">Procesų Koregavimo taikymas ir Koregavimo atšaukimas mobiliojo įrenginio meniu elemento keitimas</span><span class="sxs-lookup"><span data-stu-id="a368c-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="a368c-186">Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**, tada pasirinkite **Koregavimo taikymas ir atšaukimas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="a368c-187">Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a368c-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="a368c-188">Lauke **Darbo kūrimo procesas** pasirinkite **Koregavimo taikymas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="a368c-189">Į mobiliojo įrenginio meniu elementą bus įtraukti toliau nurodyti laukai, kai darbo kūrimo proceso metu pasirenkamas **Koregavimo taikymas** arba **Koregavimo atšaukimas**.</span><span class="sxs-lookup"><span data-stu-id="a368c-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="a368c-190">Numatytasis skaičiavimo priežasties kodas</span><span class="sxs-lookup"><span data-stu-id="a368c-190">Default counting reason code</span></span>
- <span data-ttu-id="a368c-191">Rodyti skaičiavimo priežasties kodą</span><span class="sxs-lookup"><span data-stu-id="a368c-191">Display counting reason code</span></span>
- <span data-ttu-id="a368c-192">Redaguoti skaičiavimo priežasties kodą</span><span class="sxs-lookup"><span data-stu-id="a368c-192">Edit counting reason code</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]