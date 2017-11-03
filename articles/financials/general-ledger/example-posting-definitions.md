---
title: "Registravimo aprašai"
description: "Šiame straipsnyje pateikiami pavyzdžiai, kuriais parodoma, kaip registravimo aprašai naudojami atliekant pirkimo užsakymo biudžeto rezervavimus ir biudžeto asignavimus."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1bbd9230219f11407bc7afbd59670c6287b77c02
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definition-examples"></a><span data-ttu-id="f56b2-103">Registravimo aprašų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="f56b2-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f56b2-104">Šiame straipsnyje pateikiami pavyzdžiai, kuriais parodoma, kaip registravimo aprašai naudojami atliekant pirkimo užsakymo biudžeto rezervavimus ir biudžeto asignavimus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="f56b2-105">Prieš pradėdami skaityti šią temą, turite būti susipažinę su registravimo aprašais ir operacijos registravimo aprašais.</span><span class="sxs-lookup"><span data-stu-id="f56b2-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="f56b2-106">Daugiau informacijos žr. [Registravimo aprašai](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f56b2-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="f56b2-107">Toliau pateikti pavyzdžiai gali būti nustatyti puslapyje **Registravimo aprašai**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="f56b2-108">Kiekviename pavyzdyje yra šie skyriai:</span><span class="sxs-lookup"><span data-stu-id="f56b2-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="f56b2-109">Registravimo aprašas – gretinimo kriterijai</span><span class="sxs-lookup"><span data-stu-id="f56b2-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="f56b2-110">Registravimo aprašas – sugeneruoti įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="f56b2-111">Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis</span><span class="sxs-lookup"><span data-stu-id="f56b2-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="f56b2-112">Pagal registravimo aprašą sugeneruoti DK įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="f56b2-113">Kai registravimo aprašo ir sąskaitos bei operacijos dimensijų verčių srityje **Gretinimo kriterijai** sugretinamos sąskaitos ir dimensijų vertės, pagal registravimo aprašo sritį **Sugeneruoti įrašai** sugeneruojami didžiosios knygos įrašai.</span><span class="sxs-lookup"><span data-stu-id="f56b2-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="f56b2-114">Norėdami susieti registravimo aprašą su konkrečios operacijos tipu, naudokite puslapį **Operacijos registravimo aprašai**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="f56b2-115">Susiejus registravimo aprašą su operacijos tipu ir puslapyje **DK parametrai** pasirinkus **Naudoti registravimo aprašus**, su visomis pasirinkto tipo operacijomis reikės naudoti registravimo aprašus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="f56b2-116">Pavyzdys: pirkimo užsakymo biudžeto rezervavimas</span><span class="sxs-lookup"><span data-stu-id="f56b2-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="f56b2-117">Kai puslapyje **DK parametrai** pasirinkus **Įgalinti biudžeto rezervavimo procesą** įjungiamas biudžeto rezervavimo apdorojimas, norint įrašyti sąskaitų, kurias reikia rezervuoti, biudžeto rezervavimus į didžiąją knygą reikia naudoti registravimo aprašus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="f56b2-118">Daugeliu atvejų balanse rezervuojamos visų išlaidų sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="f56b2-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="f56b2-119">Modulio **Pirkimas** biudžeto rezervavimų registravimo aprašai nustatomi puslapyje **Registravimo aprašai**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="f56b2-120">Tada puslapio **Operacijos registravimo aprašai** srityje **Pirkimas** galite pasirinkti operacijos tipą **Pirkimo užsakymas**, kad susietumėte registravimo aprašą su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="f56b2-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="f56b2-121">Visos pirkimo užsakymo rezervavimų kvitų operacijos turi būti subalansuotos (t. y. debetas turi būti lygus kreditui) kiekvienoje unikalioje kvito dimensijoje.</span><span class="sxs-lookup"><span data-stu-id="f56b2-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="f56b2-122">Registravimo aprašas – gretinimo kriterijai</span><span class="sxs-lookup"><span data-stu-id="f56b2-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="f56b2-123">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-123">Account structure</span></span>       | <span data-ttu-id="f56b2-124">Gretinti sąskaitos numerį</span><span class="sxs-lookup"><span data-stu-id="f56b2-124">Match account number</span></span> | <span data-ttu-id="f56b2-125">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="f56b2-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="f56b2-126">Sąskaitos struktūra – pelnas ir nuostolis</span><span class="sxs-lookup"><span data-stu-id="f56b2-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="f56b2-127">1</span><span class="sxs-lookup"><span data-stu-id="f56b2-127">1</span></span>        |

<span data-ttu-id="f56b2-128">* Tuščia vertė lauke **Gretinti sąskaitos numerį** reiškia, kad visos apibrėžtos sąskaitos struktūros sugretintos sąskaitos yra gretinimo taisyklių dalis.</span><span class="sxs-lookup"><span data-stu-id="f56b2-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="f56b2-129">Registravimo aprašas – sugeneruoti įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="f56b2-130">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-130">Account structure</span></span> | <span data-ttu-id="f56b2-131">Sugeneruotas sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="f56b2-131">Generated account number</span></span>                    | <span data-ttu-id="f56b2-132">Sugeneruotas debetas / kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="f56b2-133">Likutis</span><span class="sxs-lookup"><span data-stu-id="f56b2-133">Balance</span></span>           | <span data-ttu-id="f56b2-134">300143 - -(biudžeto rezervavimo sąskaita)</span><span class="sxs-lookup"><span data-stu-id="f56b2-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="f56b2-135">Tas pats</span><span class="sxs-lookup"><span data-stu-id="f56b2-135">Same</span></span>                   |
| <span data-ttu-id="f56b2-136">Likutis</span><span class="sxs-lookup"><span data-stu-id="f56b2-136">Balance</span></span>           | <span data-ttu-id="f56b2-137">300144 - -(biudžeto rezervavimo sąskaitos rezervas)</span><span class="sxs-lookup"><span data-stu-id="f56b2-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="f56b2-138">Pusiausvyros laikymas</span><span class="sxs-lookup"><span data-stu-id="f56b2-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="f56b2-139">Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis</span><span class="sxs-lookup"><span data-stu-id="f56b2-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="f56b2-140">Sąskaitų ir dimensijų vertės gaunamos iš apskaitos paskirstymų, kuriuos įvedate pirkimo užsakymo eilutėse, arba iš sąskaitų ir dimensijų, automatiškai sugeneruojamų pagal tiekėjų, prekių, kategorijų ir dimensijos šablonų numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="f56b2-141">Sąskaita + dimensijos</span><span class="sxs-lookup"><span data-stu-id="f56b2-141">Account + dimensions</span></span>           | <span data-ttu-id="f56b2-142">Debetas</span><span class="sxs-lookup"><span data-stu-id="f56b2-142">Debit</span></span>  | <span data-ttu-id="f56b2-143">Kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-143">Credit</span></span> | <span data-ttu-id="f56b2-144">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="f56b2-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="f56b2-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="f56b2-146">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="f56b2-147">Pagal registravimo aprašą sugeneruoti DK įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="f56b2-148">Sugeneruoti knygos įrašai kuriami siekiant įrašyti į biudžeto rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="f56b2-149">Sąskaita + dimensijos</span><span class="sxs-lookup"><span data-stu-id="f56b2-149">Account + dimensions</span></span>           | <span data-ttu-id="f56b2-150">Debetas</span><span class="sxs-lookup"><span data-stu-id="f56b2-150">Debit</span></span>  | <span data-ttu-id="f56b2-151">Kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-151">Credit</span></span> | <span data-ttu-id="f56b2-152">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="f56b2-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="f56b2-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="f56b2-154">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-154">250.00</span></span> |        |         |
| <span data-ttu-id="f56b2-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="f56b2-156">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-156">250.00</span></span> |         |

<span data-ttu-id="f56b2-157">Šiame pavyzdyje, bet kuri sąskaita, kuri yra srities Sąskaitos struktūra – pelnas ir nuostolis dalis, atitinka registravimo aprašo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="f56b2-158">Todėl, kai įvertinama 606500-OU\_1-OU\_3566-Training, sąskaitose, nurodytose registravimo aprašo srityje **Sugeneruoti įrašai**, sukuriami sugeneruoti įrašai.</span><span class="sxs-lookup"><span data-stu-id="f56b2-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="f56b2-159">Pavyzdys: biudžeto asignavimai</span><span class="sxs-lookup"><span data-stu-id="f56b2-159">Example: Budget appropriations</span></span>
<span data-ttu-id="f56b2-160">Įjungus biudžeto asignavimą puslapyje **DK parametrai** pasirenkant **Įgalinti biudžeto asignavimą**, biudžeto registro įrašams įrašyti DK reikia naudoti registravimo aprašus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="f56b2-161">Kai aktyvi ir įjungta biudžeto kontrolės konfigūracija, registravimo aprašus ir operacijos registravimo aprašus galima naudoti, kad būtų palaikomas asignavimų, tikslinimų, perkėlimų, projektų, ilgalaikio turto bei pasiūlos ir paklausos prognozių įrašų įrašymas į didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="f56b2-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="f56b2-162">Norėdami nustatyti biudžeto registravimo įrašų, kurių biudžeto tipas **Pradinis biudžetas** ir kurių asignavimas įjungtas, registravimo aprašą puslapyje **Registravimo aprašai** pasirinkite modulį **Biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="f56b2-163">Tada puslapio **Operacijos registravimo aprašai** srityje **Biudžetas** galite naudoti biudžeto kodus, kad susietumėte registravimo aprašą su biudžeto registro įrašais, kurių biudžeto tipas yra **Pradinis biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="f56b2-164">Kai įjungta biudžeto asignavimų ir registravimo aprašų funkcija, biudžeto registro įrašai įrašomi biudžeto kontrolės tikslais ir didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f56b2-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="f56b2-165">Registravimo aprašas – gretinimo kriterijai</span><span class="sxs-lookup"><span data-stu-id="f56b2-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="f56b2-166">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-166">Account structure</span></span>       | <span data-ttu-id="f56b2-167">Gretinti sąskaitos numerį</span><span class="sxs-lookup"><span data-stu-id="f56b2-167">Match account number</span></span> | <span data-ttu-id="f56b2-168">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="f56b2-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="f56b2-169">Sąskaitos struktūra – pelnas ir nuostolis</span><span class="sxs-lookup"><span data-stu-id="f56b2-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="f56b2-170">1</span><span class="sxs-lookup"><span data-stu-id="f56b2-170">1</span></span>        |

<span data-ttu-id="f56b2-171">* Tuščia vertė lauke **Gretinti sąskaitos numerį** reiškia, kad visos apibrėžtos sąskaitos struktūros sugretintos sąskaitos yra gretinimo taisyklių dalis.</span><span class="sxs-lookup"><span data-stu-id="f56b2-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="f56b2-172">Registravimo aprašas – sugeneruoti įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="f56b2-173">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-173">Account structure</span></span> | <span data-ttu-id="f56b2-174">Sugeneruotas sąskaitos numeris</span><span class="sxs-lookup"><span data-stu-id="f56b2-174">Generated account number</span></span>              | <span data-ttu-id="f56b2-175">Sugeneruotas debetas / kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="f56b2-176">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-176">Account structure</span></span> | <span data-ttu-id="f56b2-177">300145 - -(įvertintų įplaukų sąskaita)</span><span class="sxs-lookup"><span data-stu-id="f56b2-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="f56b2-178">Tas pats</span><span class="sxs-lookup"><span data-stu-id="f56b2-178">Same</span></span>                   |
| <span data-ttu-id="f56b2-179">Sąskaitos struktūra</span><span class="sxs-lookup"><span data-stu-id="f56b2-179">Account structure</span></span> | <span data-ttu-id="f56b2-180">300146 - -(asignavimo sąskaita)</span><span class="sxs-lookup"><span data-stu-id="f56b2-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="f56b2-181">Pusiausvyros laikymas</span><span class="sxs-lookup"><span data-stu-id="f56b2-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="f56b2-182">Operacijos su sąskaitomis, dimensijų vertėmis ir sumomis</span><span class="sxs-lookup"><span data-stu-id="f56b2-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="f56b2-183">Galite įvesti biudžeto sąskaitos įrašo sąskaitas, dimensijų vertes ir sumas į puslapį **Biudžeto registro įrašas**.</span><span class="sxs-lookup"><span data-stu-id="f56b2-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="f56b2-184">Sąskaita + dimensijos</span><span class="sxs-lookup"><span data-stu-id="f56b2-184">Account + dimensions</span></span>           | <span data-ttu-id="f56b2-185">Debetas</span><span class="sxs-lookup"><span data-stu-id="f56b2-185">Debit</span></span> | <span data-ttu-id="f56b2-186">Kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-186">Credit</span></span> | <span data-ttu-id="f56b2-187">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="f56b2-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="f56b2-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="f56b2-189">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="f56b2-190">Pagal registravimo aprašą sugeneruoti DK įrašai</span><span class="sxs-lookup"><span data-stu-id="f56b2-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="f56b2-191">Sugeneruoti didžiosios knygos įrašai sukuriami siekiant įrašyti kiekvienos dimensijos pradinį biudžetą.</span><span class="sxs-lookup"><span data-stu-id="f56b2-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="f56b2-192">Sąskaita + dimensijos</span><span class="sxs-lookup"><span data-stu-id="f56b2-192">Account + dimensions</span></span>           | <span data-ttu-id="f56b2-193">Debetas</span><span class="sxs-lookup"><span data-stu-id="f56b2-193">Debit</span></span>  | <span data-ttu-id="f56b2-194">Kreditas</span><span class="sxs-lookup"><span data-stu-id="f56b2-194">Credit</span></span> | <span data-ttu-id="f56b2-195">Komentuoti</span><span class="sxs-lookup"><span data-stu-id="f56b2-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="f56b2-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="f56b2-197">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-197">250.00</span></span> |         |
| <span data-ttu-id="f56b2-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="f56b2-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="f56b2-199">250,00</span><span class="sxs-lookup"><span data-stu-id="f56b2-199">250.00</span></span> |        |         |

<span data-ttu-id="f56b2-200">Šiame pavyzdyje, bet kuri sąskaita, kuri yra srities Sąskaitos struktūra – pelnas ir nuostolis dalis, atitinka registravimo aprašo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="f56b2-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="f56b2-201">Todėl, kai įvertinama 606400-OU\_1-OU\_3566-Training, sukuriami sugeneruoti DK įrašai.</span><span class="sxs-lookup"><span data-stu-id="f56b2-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






