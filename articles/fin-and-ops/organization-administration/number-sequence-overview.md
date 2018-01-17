---
title: Numeravimai
description: "Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e978519a86e32d4440b7c0562c4c5069c001ce81
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="number-sequences"></a><span data-ttu-id="b35c8-103">Numeravimai</span><span class="sxs-lookup"><span data-stu-id="b35c8-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b35c8-104">Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti.</span><span class="sxs-lookup"><span data-stu-id="b35c8-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="b35c8-105">Pagrindinių duomenų įrašas arba operacijų įrašas, kuriam reikia identifikatoriaus, vadinamas *nuoroda*.</span><span class="sxs-lookup"><span data-stu-id="b35c8-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="b35c8-106">Kad galėtumėte kurti naujus įrašus kaip nuorodas, turite nustatyti numeraciją ir susieti ją su nuoroda.</span><span class="sxs-lookup"><span data-stu-id="b35c8-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="b35c8-107">Rekomenduojame naudoti puslapius dalyje **Organizacijos administravimas**, kad nustatytumėte numeracijas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="b35c8-108">Jei reikalingi konkretaus modulio parametrai, galite naudoti parametrų puslapį modulyje, kad nurodytumėte numeracijas to modulio nuorodoms.</span><span class="sxs-lookup"><span data-stu-id="b35c8-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="b35c8-109">Pvz., dalyje **Gautinos sumos** ir **Mokėtinos sumos** galite nustatyti numeracijos grupes, kad priskirtumėte konkrečias numeracijas konkretiems klientams arba tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="b35c8-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="b35c8-110">Kai nustatote numeraciją, turite nustatyti aprėptį, kur apibūdina, kokia organizacija naudoja numeraciją.</span><span class="sxs-lookup"><span data-stu-id="b35c8-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="b35c8-111">Aprėptis gali būti **Bendrai naudojama**, **Įmonės**, **Juridinio subjekto** arba **Valdymo vieneto**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="b35c8-112">**Juridinio subjekto** ir **Įmonės** aprėptys gali būt sujungtos su **Ataskaitiniu kalendoriniu laikotarpiu**, kad būtų kuriamos dar konkretesnės numeracijos.</span><span class="sxs-lookup"><span data-stu-id="b35c8-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="b35c8-113">Numeracijų formatus sudaro segmentai.</span><span class="sxs-lookup"><span data-stu-id="b35c8-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="b35c8-114">Numeracijos, kurių aprėptis yra kita nei **Bendrai naudojama**, gali apimti segmentus, kurie atitinka aprėptį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="b35c8-115">Pvz., numeracijoje, kurios apimtis **Juridinio subjekto**, gali būti juridinio subjekto segmentas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="b35c8-116">Įtraukdami aprėpties segmentą į numeracijos formatą, galite nustatyti konkretaus įrašo aprėptį pagal jo numerį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="b35c8-117">Be segmentų, atitinkančių aprėptis, numeracijų formatai gali apimti **Pastoviuosius** ir **Raidinius-skaitinius segmentus**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="b35c8-118">**Pastovusis** segmentas apima raidžių, skaitmenų arba simbolių, kurie nesikeičia, rinkinį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="b35c8-119">**Raidinis-skaitinis** segmentas apima raidžių ir skaitmenų rinkinį, kuris didinamas kaskart panaudojus skaičių.</span><span class="sxs-lookup"><span data-stu-id="b35c8-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="b35c8-120">Naudokite skaičiaus ženklą (\#) norėdami nurodyti didėjančius skaičius ir ampersandus (&) norėdami nurodyti didėjančias raides.</span><span class="sxs-lookup"><span data-stu-id="b35c8-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="b35c8-121">Pvz., pagal formatą \#\#\#\#\#\_2017 sukuriamos sekos 00001\_2017, 00002\_2017 ir t.t.</span><span class="sxs-lookup"><span data-stu-id="b35c8-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="b35c8-122">Numeracijos pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="b35c8-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="b35c8-123">Toliau pateiktuose pavyzdžiuose parodyta, kaip naudoti segmentus kuriant numeracijų formatus.</span><span class="sxs-lookup"><span data-stu-id="b35c8-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="b35c8-124">Konkrečiai pavyzdžiai parodo aprėpties segmentų poveikį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="b35c8-125">Išlaidų ataskaitos numeriai</span><span class="sxs-lookup"><span data-stu-id="b35c8-125">Expense report numbers</span></span>

<span data-ttu-id="b35c8-126">Tolesniame pavyzdyje išlaidų ataskaitos numeriai nustatyti juridiniam subjektui, kuris pavadintas **CS**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="b35c8-127">**Sritis:** kelionės ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="b35c8-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="b35c8-128">**Nuoroda:** išlaidų ataskaitos numeris.</span><span class="sxs-lookup"><span data-stu-id="b35c8-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="b35c8-129">**Aprėptis:** juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="b35c8-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="b35c8-130">**Juridinis subjektas:** CS</span><span class="sxs-lookup"><span data-stu-id="b35c8-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="b35c8-131">Segmentai</span><span class="sxs-lookup"><span data-stu-id="b35c8-131">Segments</span></span>  | <span data-ttu-id="b35c8-132">Segmento tipas</span><span class="sxs-lookup"><span data-stu-id="b35c8-132">Segment type</span></span> | <span data-ttu-id="b35c8-133">Vertė</span><span class="sxs-lookup"><span data-stu-id="b35c8-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="b35c8-134">1 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-134">Segment 1</span></span> | <span data-ttu-id="b35c8-135">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="b35c8-135">Legal entity</span></span> | <span data-ttu-id="b35c8-136">CS</span><span class="sxs-lookup"><span data-stu-id="b35c8-136">CS</span></span>        |
| <span data-ttu-id="b35c8-137">2 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-137">Segment 2</span></span> | <span data-ttu-id="b35c8-138">Pastovus</span><span class="sxs-lookup"><span data-stu-id="b35c8-138">Constant</span></span>     | <span data-ttu-id="b35c8-139">-IŠLAIDOS-</span><span class="sxs-lookup"><span data-stu-id="b35c8-139">-EXPENSE-</span></span> |
| <span data-ttu-id="b35c8-140">3 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-140">Segment 3</span></span> | <span data-ttu-id="b35c8-141">Raidinis ir skaitinis</span><span class="sxs-lookup"><span data-stu-id="b35c8-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="b35c8-142">**Suformatuoto numerio pavyzdys**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="b35c8-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="b35c8-143">Galite nustatyti panašų numeracijos formatą kitiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="b35c8-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="b35c8-144">Pvz., jei pakeisite tik juridinio subjekto, pavadinimu **RW**, segmento vertę, suformatuotas numeris bus RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="b35c8-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="b35c8-145">Taip pat galite pakeisti visą kitų juridinių subjektų numeracijų formatą.</span><span class="sxs-lookup"><span data-stu-id="b35c8-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="b35c8-146">Pvz., galite praleisti juridinio subjekto aprėpties segmentą, kad sukurtumėte formatuotą numerį, pvz., Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="b35c8-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="b35c8-147">Pardavimo užsakymo numeriai</span><span class="sxs-lookup"><span data-stu-id="b35c8-147">Sales order numbers</span></span>

<span data-ttu-id="b35c8-148">Tolesniame pavyzdyje pardavimo užsakymo numeriai nustatyti įmonės ID **CEU**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="b35c8-149">**Sritis:** pardavimas</span><span class="sxs-lookup"><span data-stu-id="b35c8-149">**Area:** Sales</span></span> 
- <span data-ttu-id="b35c8-150">**Nuoroda:** pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="b35c8-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="b35c8-151">**Aprėptis:** įmonė</span><span class="sxs-lookup"><span data-stu-id="b35c8-151">**Scope:** Company</span></span> 
- <span data-ttu-id="b35c8-152">**Įmonė:** CEU</span><span class="sxs-lookup"><span data-stu-id="b35c8-152">**Company:** CEU</span></span>

| <span data-ttu-id="b35c8-153">Segmentai</span><span class="sxs-lookup"><span data-stu-id="b35c8-153">Segments</span></span>  | <span data-ttu-id="b35c8-154">Segmento tipas</span><span class="sxs-lookup"><span data-stu-id="b35c8-154">Segment type</span></span> | <span data-ttu-id="b35c8-155">Vertė</span><span class="sxs-lookup"><span data-stu-id="b35c8-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="b35c8-156">1 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-156">Segment 1</span></span> | <span data-ttu-id="b35c8-157">Pastovus</span><span class="sxs-lookup"><span data-stu-id="b35c8-157">Constant</span></span>     | <span data-ttu-id="b35c8-158">SO-</span><span class="sxs-lookup"><span data-stu-id="b35c8-158">SO-</span></span>      |
| <span data-ttu-id="b35c8-159">2 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-159">Segment 2</span></span> | <span data-ttu-id="b35c8-160">Raidinis ir skaitinis</span><span class="sxs-lookup"><span data-stu-id="b35c8-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="b35c8-161">**Suformatuoto numerio pavyzdys**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="b35c8-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="b35c8-162">Nors aprėpties segmentas neįtrauktas į formatą, iš naujo pradedama kiekvieno įmonės ID numeracija.</span><span class="sxs-lookup"><span data-stu-id="b35c8-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="b35c8-163">Jei naudojate tą patį formatą visiems įmonėms ID, tie patys numeriai naudojami kiekvienoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b35c8-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="b35c8-164">Pvz., pardavimo užsakymo numeris SO-0029 naudojamas kiekvienoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b35c8-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="b35c8-165">Taip pat galite pakeisti visą kitų įmonės ID numeracijų formatą.</span><span class="sxs-lookup"><span data-stu-id="b35c8-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="b35c8-166">Pirkimo paraiškos numeriai</span><span class="sxs-lookup"><span data-stu-id="b35c8-166">Purchase requisition numbers</span></span>

<span data-ttu-id="b35c8-167">Tolesniame pavyzdyje pirkimo paraiškos numeriai taikomi visoje organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="b35c8-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="b35c8-168">**Sritis:** pirkimas</span><span class="sxs-lookup"><span data-stu-id="b35c8-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="b35c8-169">**Nuoroda:** pirkimo paraiška</span><span class="sxs-lookup"><span data-stu-id="b35c8-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="b35c8-170">**Aprėptis:** bendrai naudojama</span><span class="sxs-lookup"><span data-stu-id="b35c8-170">**Scope:** Shared</span></span>

| <span data-ttu-id="b35c8-171">Segmentai</span><span class="sxs-lookup"><span data-stu-id="b35c8-171">Segments</span></span>  | <span data-ttu-id="b35c8-172">Segmento tipas</span><span class="sxs-lookup"><span data-stu-id="b35c8-172">Segment type</span></span> | <span data-ttu-id="b35c8-173">Vertė</span><span class="sxs-lookup"><span data-stu-id="b35c8-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="b35c8-174">1 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-174">Segment 1</span></span> | <span data-ttu-id="b35c8-175">Pastovus</span><span class="sxs-lookup"><span data-stu-id="b35c8-175">Constant</span></span>     | <span data-ttu-id="b35c8-176">Reik.</span><span class="sxs-lookup"><span data-stu-id="b35c8-176">Req</span></span>      |
| <span data-ttu-id="b35c8-177">2 segmentas</span><span class="sxs-lookup"><span data-stu-id="b35c8-177">Segment 2</span></span> | <span data-ttu-id="b35c8-178">Raidinis ir skaitinis</span><span class="sxs-lookup"><span data-stu-id="b35c8-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="b35c8-179">**Suformatuoto numerio pavyzdys**: Req0052</span><span class="sxs-lookup"><span data-stu-id="b35c8-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="b35c8-180">Kadangi aprėptis yra **Bendrai naudojama**, numeracijos formatas naudojamas visoje organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="b35c8-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="b35c8-181">Negalite nustatyti kitokių numeracijų formatų skirtingoms organizacijos dalims.</span><span class="sxs-lookup"><span data-stu-id="b35c8-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="b35c8-182">Numeracijų našumo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="b35c8-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="b35c8-183">Apsvarstykite toliau nurodytą informaciją apie tai, kaip numeracijų konfigūracija gali paveikti sistemos našumą, prieš nustatydami numeracijas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="b35c8-184">Tęstinės ir netęstinės numeracijos</span><span class="sxs-lookup"><span data-stu-id="b35c8-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="b35c8-185">Numeracijos gali būti tęstinės arba netęstinės.</span><span class="sxs-lookup"><span data-stu-id="b35c8-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="b35c8-186">Tęstinėje numeracijoje nepraleidžiami jokie skaičiai, bet skaičiai gali būti naudojami ne paeiliui.</span><span class="sxs-lookup"><span data-stu-id="b35c8-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="b35c8-187">Skaičiai iš netęstinės numeracijos naudojami paeiliui, bet numeracijoje gali būti praleisti skaičiai.</span><span class="sxs-lookup"><span data-stu-id="b35c8-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="b35c8-188">Pvz., jei naudotojas atšaukia operaciją, numeris sugeneruojamas, bet nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="b35c8-189">Tęstinėje numeracijoje skaičiai pakartotinai panaudojami vėliau.</span><span class="sxs-lookup"><span data-stu-id="b35c8-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="b35c8-190">Netęstinėje numeracijoje skaičius nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="b35c8-191">Tęstinės numeracijos paprastai reikalingos išoriniams dokumentams, pvz., pirkimo užsakymams, pardavimo užsakymams ir SF.</span><span class="sxs-lookup"><span data-stu-id="b35c8-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="b35c8-192">Tačiau tęstinės numeracijos gali turėti neigiamos įtakos sistemos atsako laikui, nes sistema turi pareikalauti skaičiaus iš duomenų bazės kaskart, kai sukuriamas naujas dokumentas arba įrašas.</span><span class="sxs-lookup"><span data-stu-id="b35c8-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="b35c8-193">Jei naudojate netęstinę numeraciją, **Numeracijų** puslapio **Našumo** „FastTab‟ galite įgalinti **Išankstinį paskirstymą**.</span><span class="sxs-lookup"><span data-stu-id="b35c8-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="b35c8-194">Kai nurodote iš anksto priskiriamų numerių kiekį, sistema parenka tuos numerius ir saugo atmintyje.</span><span class="sxs-lookup"><span data-stu-id="b35c8-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="b35c8-195">Naujų numerių prašoma iš duomenų bazės tik panaudojus iš anksto priskirtą kiekį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="b35c8-196">Rekomenduojame naudoti netęstines numeracijas, kad užtikrintumėte geresnį našumą, nebent taikomi reglamento reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="b35c8-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="b35c8-197">Automatinis numeracijų valymas</span><span class="sxs-lookup"><span data-stu-id="b35c8-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="b35c8-198">Nutrūkus maitinimui, įvykus klaidai arba kitai netikėtai trikčiai, sistema negali perskirstyti tęstinių numeracijų skaičių automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b35c8-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="b35c8-199">Galite vykdyti valymo procesą rankiniu būdu arba automatiškai atkurti prarastus numerius.</span><span class="sxs-lookup"><span data-stu-id="b35c8-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="b35c8-200">Atidžiai apsvarstykite serverio naudojimą, kai planuojate valymo procesą.</span><span class="sxs-lookup"><span data-stu-id="b35c8-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="b35c8-201">Rekomenduojame ne piko valandomis atlikti valymą kaip paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b35c8-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






