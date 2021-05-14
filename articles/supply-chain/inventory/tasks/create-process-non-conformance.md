---
title: Neatitikimo kūrimas ir apdorojimas
description: Šioje temoje aprašoma, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956211"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="06550-103">Neatitikimo kūrimas ir apdorojimas</span><span class="sxs-lookup"><span data-stu-id="06550-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06550-104">Šioje temoje aprašoma, kaip vykdyti neatitikimo valdymą remiantis esamu kokybės užsakymu.</span><span class="sxs-lookup"><span data-stu-id="06550-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="06550-105">Paprastai neatitikties valdymą atliko kokybės klerkas.</span><span class="sxs-lookup"><span data-stu-id="06550-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="06550-106">Jei būtina, turite turėti prieinamą kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="06550-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="06550-107">(Daugiau informacijos apie tai, kaip kurti ir dirbti su kokybės užsakymais rasite [Stebėkite prekių kokybę](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="06550-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="06550-108">Kad vartotojas galėtų apdoroti neatitikties patvirtinimą, darbuotojas turi būti jam priskirtas vartotojų **puslapio** lauke **Asmuo**.</span><span class="sxs-lookup"><span data-stu-id="06550-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="06550-109">Be to, prieš vartotojui naudojant dokumentų pastabas jų vartotojo pasirinktyse turi būti nustatyta parinktis **Įgalinti** dokumentų *tvarkymą*.</span><span class="sxs-lookup"><span data-stu-id="06550-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="06550-110">Neatitikties kūrimas</span><span class="sxs-lookup"><span data-stu-id="06550-110">Create a nonconformance</span></span>

<span data-ttu-id="06550-111">Norėdami sukurti neatitiktis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="06550-112">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-113">Veiksmų juostoje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="06550-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="06550-114">Dialogo lange Kurti neatitikčių žymėjimą lauke Problemos tipas **pasirinkite** problemos **, kuri** buvo rasta tikrinimo proceso metu, tipą.</span><span class="sxs-lookup"><span data-stu-id="06550-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="06550-115">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="06550-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="06550-116">Neatitikties tvirtinimas ar atmetimas</span><span class="sxs-lookup"><span data-stu-id="06550-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="06550-117">Norėdami patvirtinti arba atmesti neatitiktis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="06550-118">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-119">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-120">Pataisymus galite įtraukti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-121">Veiksmų srityje pasirinkite **Funkcijos \> Tvirtinti neatitiktis** norėdami patvirtinti neatitiktis ar **Funkcijos \> Atsisakyti neatitikčių** norėdami jas atmesti.</span><span class="sxs-lookup"><span data-stu-id="06550-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="06550-122">Patvirtintas neatitiktis galima susieti su [susijusiomis](../quality-operations.md) operacijomis.</span><span class="sxs-lookup"><span data-stu-id="06550-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="06550-123">Tokiu būdu galite įrašyti darbą, įvertinimą, o taisymą – kaip neatitikties tvarkymo dalį.</span><span class="sxs-lookup"><span data-stu-id="06550-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="06550-124">Jus paragins patvirtinti savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="06550-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="06550-125">Pasirinkite **Taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="06550-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="06550-126">Prie neatitikimų pridėkite operacijas ir kitą informaciją</span><span class="sxs-lookup"><span data-stu-id="06550-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="06550-127">Sukūrę neatitiką, galite pradėti pridėti susijusias operacijas ir nurodyti papildomą informaciją apie tas operacijas.</span><span class="sxs-lookup"><span data-stu-id="06550-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="06550-128">Susijusias operacijas galite įtraukti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="06550-129">Be pagrindinės informacijos, operacijai galite pridėti ir toliau nurodytą informaciją:</span><span class="sxs-lookup"><span data-stu-id="06550-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="06550-130">**Prekės** – galite sukurti prekių, suvartotų atlikti koregavimą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="06550-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="06550-131">Pavyzdžiui, prekės gali būti produktai, kurių reikia norint remontuoti įrangą arba ingredientus, reikalingus baigtam produktui perkurti.</span><span class="sxs-lookup"><span data-stu-id="06550-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="06550-132">**Kokybės išlaidos** – galite sukurti išlaidų, kurios patirtos arba išrašomos iš išorinių šaltinių, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="06550-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="06550-133">**Tabelis** – galite sukurti laiko, kurį kiekvienas darbuotojas praleidžia operacijoje, žurnalą.</span><span class="sxs-lookup"><span data-stu-id="06550-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="06550-134">Likę nustatymai yra neprivalomi.</span><span class="sxs-lookup"><span data-stu-id="06550-134">The remaining settings are optional.</span></span> <span data-ttu-id="06550-135">Susumuojamos kiekvienos prekės išlaidos, kokybės išlaidos ir tabelis bei rodomas operacijoje.</span><span class="sxs-lookup"><span data-stu-id="06550-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="06550-136">Operacijos lauko Išlaidos **tiesiogiai** redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="06550-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="06550-137">Kurti neatitikties operaciją</span><span class="sxs-lookup"><span data-stu-id="06550-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="06550-138">Norėdami sukurti neatitikčių operaciją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="06550-139">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-140">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-141">Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-142">Veiksmų srityje spustelėkite **Susijusios operacijos**.</span><span class="sxs-lookup"><span data-stu-id="06550-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="06550-143">Puslapyje **Susijusios operacijos** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="06550-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="06550-144">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="06550-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="06550-145">**Operacija** – pasirinkite operacijos, kuri bus atliekama neatitikti, kodą.</span><span class="sxs-lookup"><span data-stu-id="06550-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="06550-146">**Priežastis** – įveskite išsamų aprašymą, paaiškinaį, kodėl operacija reikalinga.</span><span class="sxs-lookup"><span data-stu-id="06550-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="06550-147">**Pardavimo užsakymas – jei pasirinktas operacijos kodas yra susijęs su pardavimo užsakymo tipu, pasirinkite pardavimo užsakymą, su** kurį susiesite operaciją.</span><span class="sxs-lookup"><span data-stu-id="06550-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="06550-148">**Pirkimo užsakymas – jei pasirinktas operacijos kodas yra susijęs su pirkimo užsakymo tipu, pasirinkite pirkimo užsakymą, su** kurį susiesite operaciją.</span><span class="sxs-lookup"><span data-stu-id="06550-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="06550-149">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="06550-150">Prekių įtraukimas į operaciją</span><span class="sxs-lookup"><span data-stu-id="06550-150">Add items to an operation</span></span>

<span data-ttu-id="06550-151">Norėdami į operaciją įtraukti prekes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="06550-152">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-153">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-154">Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-155">Veiksmų srityje spustelėkite **Susijusios operacijos**.</span><span class="sxs-lookup"><span data-stu-id="06550-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="06550-156">Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti prekes.</span><span class="sxs-lookup"><span data-stu-id="06550-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="06550-157">Veiksmų srityje pasirinkite **Prekės**.</span><span class="sxs-lookup"><span data-stu-id="06550-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="06550-158">Puslapyje **Susijusios operacijos** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="06550-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="06550-159">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="06550-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="06550-160">**Prekės numeris** – pasirinkite produktą, kuris bus suvartotas kaip pasirinktos operacijos dalis.</span><span class="sxs-lookup"><span data-stu-id="06550-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="06550-161">**Kiekis** – įveskite suvartotų prekių skaičių.</span><span class="sxs-lookup"><span data-stu-id="06550-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-162">Prekės išlaidas galite peržiūrėti skirtuko **Bendra** lauke **Išlaidos**. Išlaidos, kurios rodomos, yra iš išlaidų, kurios yra nustatytos **išleisto produkto** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="06550-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="06550-163">Išlaidų negalima tiesiogiai atnaujinti puslapyje Susijusios **operacijos** elementas.</span><span class="sxs-lookup"><span data-stu-id="06550-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="06550-164">Visų prekių, kurios pridėtos puslapyje Susijusios operacijos elementai, išlaidos automatiškai pridėtos prie **lauko Išlaidos puslapyje** **Susijusios** **operacijos**.</span><span class="sxs-lookup"><span data-stu-id="06550-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="06550-165">Pakartokite ankstesnį veiksmą su kiekviena papildoma preke, kurią turite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="06550-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="06550-166">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="06550-167">Į operaciją įtraukti kokybės išlaidas</span><span class="sxs-lookup"><span data-stu-id="06550-167">Add quality charges to an operation</span></span>

<span data-ttu-id="06550-168">Norėdami įtraukti kokybės keitimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="06550-169">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-170">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-171">Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-172">Veiksmų srityje spustelėkite **Susijusios operacijos**.</span><span class="sxs-lookup"><span data-stu-id="06550-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="06550-173">Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti kokybės keitimus.</span><span class="sxs-lookup"><span data-stu-id="06550-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="06550-174">Veiksmų srityje pasirinkite **Kokybės keitimai**.</span><span class="sxs-lookup"><span data-stu-id="06550-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="06550-175">Puslapyje **Susiję operacijų keitimai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="06550-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="06550-176">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="06550-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="06550-177">**Kodo mokesčiai** – Pasirinkite kokybės grupę, kurią norite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="06550-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="06550-178">**Aprašas** – įveskite išsamų keitimo aprašą.</span><span class="sxs-lookup"><span data-stu-id="06550-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="06550-179">**Vertės mokesčiai** – Įvesti taikytiną mokesčio sumą.</span><span class="sxs-lookup"><span data-stu-id="06550-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="06550-180">Pakartokite ankstesnį veiksmą su kiekvienu papildomu mokesčiu, kurią turite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="06550-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="06550-181">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="06550-182">Lauke Išlaidų vertė automatiškai sumuojamos visos kokybės išlaidos ir pridedama prie visų kitų sumų  **lauke** **Išlaidos** **puslapyje Susijusios** operacijos.</span><span class="sxs-lookup"><span data-stu-id="06550-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="06550-183">Sukurkite operacijos tabelį</span><span class="sxs-lookup"><span data-stu-id="06550-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="06550-184">Norėdami įtraukti tabelį į operaciją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="06550-185">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-186">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-187">Susijusias operacijas galite įtraukti ar naujinti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-188">Veiksmų srityje spustelėkite **Susijusios operacijos**.</span><span class="sxs-lookup"><span data-stu-id="06550-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="06550-189">Puslapyje **Susijusios operacijos** pasirinkite operaciją, į kurią norite įtraukti tabelį.</span><span class="sxs-lookup"><span data-stu-id="06550-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="06550-190">Veiksmų srityje pasirinkite **Tabelis**.</span><span class="sxs-lookup"><span data-stu-id="06550-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="06550-191">Puslapyje **Susiję operacijų tabeliai** veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="06550-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="06550-192">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="06550-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="06550-193">**Data** – nurodykite datą, kada darbas buvo atliktas.</span><span class="sxs-lookup"><span data-stu-id="06550-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="06550-194">Pagal numatytą laukelį, nustatoma esama data.</span><span class="sxs-lookup"><span data-stu-id="06550-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="06550-195">**Darbuotojas** – Pasirinkite darbuotoją, kuris nedirbo.</span><span class="sxs-lookup"><span data-stu-id="06550-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="06550-196">Pagal numatytuosius nustatymus šis laukas nustatomas darbuotojui, kuris priskirtas dabartiniam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="06550-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="06550-197">**Operacijos valandos** – įveskite valandų skaičių, kuris buvo valandų skaičius, pagal kurį buvo dirbama su pasirinkta operacija.</span><span class="sxs-lookup"><span data-stu-id="06550-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="06550-198">**Išrašyta SF – pažymėkite šį žymės langelį, jei SF** klientams arba tiekėjui išrašoma sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="06550-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-199">Galite peržiūrėti išlaidas lauke **Išlaidos** skirtuke **Bendra**. Išlaidos apskaičiuojamos naudojant tarifą, kurį nurodote **atsargų valdymo parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="06550-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="06550-200">Pakartokite ankstesnį veiksmą su kiekvienu papildomu tabeliu, kurį turite įtraukti.</span><span class="sxs-lookup"><span data-stu-id="06550-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="06550-201">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="06550-202">Lauke Išlaidų vertė automatiškai sumuojamos visi kokybės kaštai ir pridedama prie visų kitų tabelių eilučių  **Kaštai** **Išlaidos** **puslapyje Susijusios** operacijos.</span><span class="sxs-lookup"><span data-stu-id="06550-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="06550-203">Taisymo pridėjimas prie neatitikties</span><span class="sxs-lookup"><span data-stu-id="06550-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="06550-204">Norėdami įtraukti taisymą į neatitiktis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="06550-205">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-206">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-207">Pataisymus galite įtraukti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-208">Veiksmų srityje pasirinkite **Taisymai**.</span><span class="sxs-lookup"><span data-stu-id="06550-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="06550-209">Puslapyje **Taisymai** tam, kad įtrauktumėte eilutę tinklelyje **Peržiūros** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="06550-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="06550-210">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="06550-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="06550-211">**Diagnostika** – pasirinkite diagnozės tipą, kuris identifikuoja kuriamo pataisos tipą.</span><span class="sxs-lookup"><span data-stu-id="06550-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="06550-212">**Darbuotojas** – Pasirinkite už taisymus atsakingą asmenį.</span><span class="sxs-lookup"><span data-stu-id="06550-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="06550-213">**Koregavimo prioritetas – pasirinkite pasirinktį, norėdami nurodyti, kaip turi būti taisymo prioritetas** (*Žemas*, *Įprastas* arba *Aukštas*).</span><span class="sxs-lookup"><span data-stu-id="06550-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="06550-214">**Pareikalauta data** – įveskite datą, kada pareikalauta baudos veiksmo.</span><span class="sxs-lookup"><span data-stu-id="06550-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="06550-215">**Suplanuota** data – įveskite datą, kada tikimasi atlikti pataisymą.</span><span class="sxs-lookup"><span data-stu-id="06550-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="06550-216">**Trumpalaikis sprendimas** – pasirinkite šį žymės langelį, jei koreguojamuoju veiksmu neatitiktis taisoma tik trumpą laiką.</span><span class="sxs-lookup"><span data-stu-id="06550-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="06550-217">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="06550-218">Žymėti taisymą kaip užbaigtą</span><span class="sxs-lookup"><span data-stu-id="06550-218">Mark a correction as completed</span></span>

<span data-ttu-id="06550-219">Norėdami pažymėti neatitikties taisymą kaip baigtą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="06550-220">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-221">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06550-222">Pataisymus galite įtraukti tik į patvirtintas neatitiktis.</span><span class="sxs-lookup"><span data-stu-id="06550-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="06550-223">Veiksmų srityje pasirinkite **Taisymai**.</span><span class="sxs-lookup"><span data-stu-id="06550-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="06550-224">Skirtuko **Taisymų** puslapyje tinklelyje pasirinkite taisymą, kurį norite pažymėti kaip užbaigtą.</span><span class="sxs-lookup"><span data-stu-id="06550-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="06550-225">Veiksmų srityje spustelėkite **Žymėjimas baigtas**.</span><span class="sxs-lookup"><span data-stu-id="06550-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="06550-226">Jus paragins patvirtinti savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="06550-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="06550-227">Norėdami tęsti **Rinkitės** GERAI.</span><span class="sxs-lookup"><span data-stu-id="06550-227">Select **OK** to continue.</span></span> <span data-ttu-id="06550-228">Lauke **Baigimo data** ir laikas nustatyti dabartiniai data ir laikas, ir **pažymėtas žymės langelis** Baigta.</span><span class="sxs-lookup"><span data-stu-id="06550-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="06550-229">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="06550-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="06550-230">Atidarykite baigtą taisymą iš naujo</span><span class="sxs-lookup"><span data-stu-id="06550-230">Reopen a completed correction</span></span>

<span data-ttu-id="06550-231">Norėdami atidaryti iš naujo baigtą taisymą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="06550-232">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-233">Sąraše raskite ir pasirinkite neatitiktis, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="06550-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="06550-234">Veiksmų juostoje pasirinkite **Taisymai**.</span><span class="sxs-lookup"><span data-stu-id="06550-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="06550-235">Skirtuko **Taisymų** puslapyje tinklelyje pasirinkite taisymą, kurį norite atidaryti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="06550-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="06550-236">Veiksmų srityje pasirinkite **Atidaryti iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="06550-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="06550-237">Jus paragins patvirtinti savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="06550-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="06550-238">Norėdami tęsti **Rinkitės** GERAI.</span><span class="sxs-lookup"><span data-stu-id="06550-238">Select **OK** to continue.</span></span> <span data-ttu-id="06550-239">Vertė išvalo lauką **Užbaigimo data ir** laikas, o žymės **langelis Baigtas** išvalomas.</span><span class="sxs-lookup"><span data-stu-id="06550-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="06550-240">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="06550-240">Close the page.</span></span>

<span data-ttu-id="06550-241">Dabar galite atlikti papildomus pataisymų redagavimus ar atnaujinimus.</span><span class="sxs-lookup"><span data-stu-id="06550-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="06550-242">Baigę pataisymą galite žymėti kaip užbaigtą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="06550-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="06550-243">Neatitikties uždarymas</span><span class="sxs-lookup"><span data-stu-id="06550-243">Close a nonconformance</span></span>

<span data-ttu-id="06550-244">Norėdami uždaryti neatitiktis, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="06550-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="06550-245">Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="06550-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="06550-246">Tinklelyje pasirinkite kokybės užsakymą.</span><span class="sxs-lookup"><span data-stu-id="06550-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="06550-247">Veiksmų srityje pasirinkite **Užklausos \> Neatitiktys**.</span><span class="sxs-lookup"><span data-stu-id="06550-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="06550-248">Neatitikties **puslapyje** tinklelyje pasirinkite tikslinę neatitikčių tikslą.</span><span class="sxs-lookup"><span data-stu-id="06550-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="06550-249">Veiksmų srityje pasirinkite **Funkcijos \> Uždaryti neatitiktis**.</span><span class="sxs-lookup"><span data-stu-id="06550-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="06550-250">Jus paragins patvirtinti savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="06550-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="06550-251">Pasirinkite **Taip** tam, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="06550-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="06550-252">Uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="06550-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06550-253">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="06550-253">Additional resources</span></span>

- [<span data-ttu-id="06550-254">Kokybės valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="06550-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="06550-255">Įjungti kiekio ir neatitikties valdymą</span><span class="sxs-lookup"><span data-stu-id="06550-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="06550-256">Darbuotojai, atsakingi už neatitikties tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="06550-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="06550-257">Neatitikimų sulaikymo zonos</span><span class="sxs-lookup"><span data-stu-id="06550-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="06550-258">Neatitikimų diagnostikos tipai</span><span class="sxs-lookup"><span data-stu-id="06550-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="06550-259">Neatitikimų kokybės mokesčiai</span><span class="sxs-lookup"><span data-stu-id="06550-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="06550-260">Neatitikties operacijos</span><span class="sxs-lookup"><span data-stu-id="06550-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="06550-261">Sandėlio procesų kokybės valdymas</span><span class="sxs-lookup"><span data-stu-id="06550-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
