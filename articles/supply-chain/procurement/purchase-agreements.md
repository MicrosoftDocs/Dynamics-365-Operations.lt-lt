---
title: Pirkimo sutartys
description: "Šiame straipsnyje pateikta informacija apie pirkimo sutartis. Pirkimo sutartis yra sutartis, kurią pasirašiusi organizacija įsipareigoja per tam tikrą laiką keliais pirkimo užsakymais įsigyti nurodytą kiekį arba sumą. Už šį įsipareigojimą pirkėjas gauna specialias kainas ir nuolaidas."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0506d4ed0bc1345be5d5c78c2b55a52aff5625e9
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="purchase-agreements"></a><span data-ttu-id="d10ec-105">Pirkimo sutartys</span><span class="sxs-lookup"><span data-stu-id="d10ec-105">Purchase agreements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d10ec-106">Šiame straipsnyje pateikta informacija apie pirkimo sutartis.</span><span class="sxs-lookup"><span data-stu-id="d10ec-106">This article provides information about purchase agreements.</span></span> <span data-ttu-id="d10ec-107">Pirkimo sutartis yra sutartis, kurią pasirašiusi organizacija įsipareigoja per tam tikrą laiką keliais pirkimo užsakymais įsigyti nurodytą kiekį arba sumą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-107">A purchase agreement is a contract that commits an organization to buy a specified quantity or amount by using multiple purchase orders over time.</span></span> <span data-ttu-id="d10ec-108">Už šį įsipareigojimą pirkėjas gauna specialias kainas ir nuolaidas.</span><span class="sxs-lookup"><span data-stu-id="d10ec-108">In exchange for this commitment, the buyer receives special prices and discounts.</span></span> 

<span data-ttu-id="d10ec-109">Pirkimo sutartis galima taikyti konkrečiam produktui, konkrečiai produkto piniginei vertei arba konkrečiai produkto piniginei vertei įsigijimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-109">Purchase agreements can apply to a specific quantity of a product, a specific currency amount of a product, or a specific currency amount of the products in a procurement category.</span></span> <span data-ttu-id="d10ec-110">Pardavimo sutarties kainos ir nuolaidos turi pirmenybę prieš kainas ir nuolaidas, nurodytas bet kuriose esamose prekybos sutartyse.</span><span class="sxs-lookup"><span data-stu-id="d10ec-110">The prices and discounts of the purchase agreement override the prices and discounts that are specified in any trade agreements that exist.</span></span>  

<span data-ttu-id="d10ec-111">Puslapyje **Pirkimo sutartys** galite sukurti, pritaikyti ir vykdyti tolesnius veiksmus dėl pirkimo sutarčių, sudarytų tarp jūsų organizacijos ir kliento.</span><span class="sxs-lookup"><span data-stu-id="d10ec-111">On the **Purchase agreements** page, you can create, apply, and follow up on purchase agreements that exist between your organization and your vendors.</span></span> <span data-ttu-id="d10ec-112">Pvz., sukūrę pirkimo sutartį galite užsakyti tiesiogiai iš jos.</span><span class="sxs-lookup"><span data-stu-id="d10ec-112">For example, after you create a purchase agreement, you can order directly from it.</span></span> <span data-ttu-id="d10ec-113">Kiekviena pirkimo sutartis turi galiojimo laikotarpį, kurį nustato asmuo, kuriantis pirkimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="d10ec-113">Each purchase agreement has a validity period that is defined by the person who creates the purchase agreement.</span></span> <span data-ttu-id="d10ec-114">Pageidaujama pirkinio pristatymo data turi būti šiame pirkimo sutarties galiojimo laikotarpyje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-114">The delivery date of a purchase must be within the effective dates of this validity period.</span></span>  

<span data-ttu-id="d10ec-115">Kai sukuriate pirkimo sutartį, prieš jai įsigaliojant, turite ją aktyvuoti.</span><span class="sxs-lookup"><span data-stu-id="d10ec-115">After you create a purchase agreement, you must activate it before it becomes effective.</span></span> <span data-ttu-id="d10ec-116">Norėdami suaktyvinti pirkimo sutartį, parinktį **Pažymėti sutartį kaip galiojančią** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d10ec-116">To activate a purchase agreement, set the **Mark agreement as effective** option to **Yes**.</span></span>

## <a name="commitment-types"></a><span data-ttu-id="d10ec-117">Įsipareigojimo tipai</span><span class="sxs-lookup"><span data-stu-id="d10ec-117">Commitment types</span></span>
<span data-ttu-id="d10ec-118">Kiekviena pirkimo sutarties eilutė įpareigoja ką nors pirkti.</span><span class="sxs-lookup"><span data-stu-id="d10ec-118">Each line in a purchase agreement is a commitment to buy something.</span></span> <span data-ttu-id="d10ec-119">Galite naudoti kelių pirkimo užsakymų (PU) eilutes, norėdami įvykdyti įsipareigojimą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-119">You can use lines from multiple purchase orders (POs) to fulfill the commitment.</span></span> <span data-ttu-id="d10ec-120">Yra keturi įsipareigojimų tipai:</span><span class="sxs-lookup"><span data-stu-id="d10ec-120">There are four types of commitments:</span></span>

-   <span data-ttu-id="d10ec-121">**Produkto kiekio įsipareigojimas**– įsigyjate konkretų produkto kiekį.</span><span class="sxs-lookup"><span data-stu-id="d10ec-121">**Product quantity commitment** – You purchase a specific quantity of a product.</span></span>
-   <span data-ttu-id="d10ec-122">**Produkto vertės įsipareigojimas**– įsigyjate konkrečią produkto valiutos sumą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-122">**Product value commitment** – You purchase a specific currency amount of a product.</span></span>
-   <span data-ttu-id="d10ec-123">**Produktų kategorijos vertės įsipareigojimas**– įsigyjate konkrečią valiutos sumą įsigijimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-123">**Product category value commitment** – You purchase a specific currency amount in a procurement category.</span></span> <span data-ttu-id="d10ec-124">Suma gali būti katalogo prekių arba prekių ne iš katalogo.</span><span class="sxs-lookup"><span data-stu-id="d10ec-124">The amount can be for a catalog item or a non-catalog item.</span></span>
-   <span data-ttu-id="d10ec-125">**Vertės įsipareigojimas**– įsigyjate konkrečią bet kurio produkto ar produktų bet kurioje įsigijimo kategorijoje valiutos sumą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-125">**Value commitment** – You purchase a specific currency amount of any product or products in any procurement category.</span></span>

## <a name="pricing-terms-for-purchase-agreements"></a><span data-ttu-id="d10ec-126">Pirkimo sutarčių kainodaros sąlygos</span><span class="sxs-lookup"><span data-stu-id="d10ec-126">Pricing terms for purchase agreements</span></span>
<span data-ttu-id="d10ec-127">Kainodaros sąlygos gali skirtis, atsižvelgiant į įsipareigojimo tipą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-127">Pricing terms can vary, depending on the type of commitment.</span></span> <span data-ttu-id="d10ec-128">Pirkimo sutarčių kainodaros sąlygos turi pirmenybę prieš bet kurias kitas kainodaros sąlygas, nustatytas prekybos sutartyse.</span><span class="sxs-lookup"><span data-stu-id="d10ec-128">The pricing terms from purchase agreements override any other pricing terms that are set up for trade agreements.</span></span> <span data-ttu-id="d10ec-129">Toliau pateikiamoje lentelėje aprašomi kainos laukai, kuriuos paveikia kiekvienas įsipareigojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="d10ec-129">The following table describes the price-related fields that are affected by each commitment type.</span></span> <span data-ttu-id="d10ec-130">Laukuose, kuriuose yra **Taip** užsakymo eilutę galima atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="d10ec-130">Fields that contain **Yes** can be updated on an order line.</span></span>

| <span data-ttu-id="d10ec-131">Įsipareigojimo tipas</span><span class="sxs-lookup"><span data-stu-id="d10ec-131">Commitment type</span></span>                   | <span data-ttu-id="d10ec-132">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="d10ec-132">Unit price</span></span> | <span data-ttu-id="d10ec-133">Kainos vienetas</span><span class="sxs-lookup"><span data-stu-id="d10ec-133">Price unit</span></span> | <span data-ttu-id="d10ec-134">Nuolaidos procentas</span><span class="sxs-lookup"><span data-stu-id="d10ec-134">Discount percent</span></span> | <span data-ttu-id="d10ec-135">Mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="d10ec-135">Cash discount amount</span></span> |
|-----------------------------------|------------|------------|------------------|----------------------|
| <span data-ttu-id="d10ec-136">Produkto kiekio įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="d10ec-136">Product quantity commitment</span></span>       | <span data-ttu-id="d10ec-137">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-137">Yes</span></span>        | <span data-ttu-id="d10ec-138">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-138">Yes</span></span>        | <span data-ttu-id="d10ec-139">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-139">Yes</span></span>              | <span data-ttu-id="d10ec-140">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-140">Yes</span></span>                  |
| <span data-ttu-id="d10ec-141">Produkto vertės įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="d10ec-141">Product value commitment</span></span>          |            |            | <span data-ttu-id="d10ec-142">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-142">Yes</span></span>              |                      |
| <span data-ttu-id="d10ec-143">Produkto kategorijos vertės įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="d10ec-143">Product category value commitment</span></span> |            |            | <span data-ttu-id="d10ec-144">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-144">Yes</span></span>              |                      |
| <span data-ttu-id="d10ec-145">Vertės įsipareigojimas</span><span class="sxs-lookup"><span data-stu-id="d10ec-145">Value commitment</span></span>                  |            |            | <span data-ttu-id="d10ec-146">Taip</span><span class="sxs-lookup"><span data-stu-id="d10ec-146">Yes</span></span>              |                      |

## <a name="policies-for-purchase-agreements"></a><span data-ttu-id="d10ec-147">Pirkimo sutarčių strategijos</span><span class="sxs-lookup"><span data-stu-id="d10ec-147">Policies for purchase agreements</span></span>
<span data-ttu-id="d10ec-148">Toliau nurodytos strategijos turi įtakos tam, kaip veikia ryšys tarp įsipareigojimo pirkimo sutartimi ir atitinkamos PU eilutės.</span><span class="sxs-lookup"><span data-stu-id="d10ec-148">The following policies affect the way that the link between a purchase agreement commitment and the corresponding PO lines works:</span></span>

-   <span data-ttu-id="d10ec-149">**Maksimaliai vykdoma**– bendras kiekis arba visų užsakymo eilučių suma negali viršyti susijusiame įsipareigojime nurodyto kiekio arba sumos.</span><span class="sxs-lookup"><span data-stu-id="d10ec-149">**Max is enforced** – The total quantity or amount for all order lines can't exceed the quantity or amount that is specified on the related commitment.</span></span>
-   <span data-ttu-id="d10ec-150">**Kaina ir nuolaida fiksuotos** – užsakymo eilutės kaina ir susijusio įsipareigojimo kaina turi būti tokia pati.</span><span class="sxs-lookup"><span data-stu-id="d10ec-150">**Price and discount is fixed** – The price on an order line and the price on the related commitment must be the same.</span></span> <span data-ttu-id="d10ec-151">Jei kaina užsakymo eilutėje pakeičiama, nutraukiama sąsaja su įsipareigojimu.</span><span class="sxs-lookup"><span data-stu-id="d10ec-151">If the price is changed on the order line, the link to the commitment is broken.</span></span> <span data-ttu-id="d10ec-152">Jei sąsaja su įsipareigojimu nutraukiama, užsakymo eilutė nebepridedama prie įsipareigojimo vykdymo.</span><span class="sxs-lookup"><span data-stu-id="d10ec-152">If the link is broken, the order line doesn't contribute to the fulfillment of the commitment.</span></span>
-   <span data-ttu-id="d10ec-153">**Minimali išduodama suma ir Maksimali išduodama suma** – jei suma nurodyta, gaunate pranešimą apie tai, ar galite atlikti kokius pokyčius užsakymo eilutėje, kuriuos atlikus užsakymo eilutė skirtųsi nuo susijusio įsipareigojimo.</span><span class="sxs-lookup"><span data-stu-id="d10ec-153">**Minimum release amount and Maximum release amount** – If an amount is specified, you receive a message if you make any change to an order line that causes the order line to differ from the related commitment.</span></span>

## <a name="fulfillment-calculations-for-purchase-agreements"></a><span data-ttu-id="d10ec-154">Pirkimo sutarčių įvykdymo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="d10ec-154">Fulfillment calculations for purchase agreements</span></span>
<span data-ttu-id="d10ec-155">Įvykdymo kiekiai ir sumos rodomi **Įvykdymo** skirtuke, esančiame **Eilučių informacijos** „FastTab‟, **Pirkimo sutarčių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-155">Fulfillment quantities and amounts are shown on the **Fulfillment** tab on the **Line details** FastTab of the **Purchase agreements** page.</span></span>  

<span data-ttu-id="d10ec-156">**Įvykdymo** srityje rodoma likusi suma ar kiekis, kurio reikia įsipareigojimo įvykdymui.</span><span class="sxs-lookup"><span data-stu-id="d10ec-156">The **Fulfillment** area shows the remaining amount or quantity that is required to fulfill the commitment.</span></span>  

<span data-ttu-id="d10ec-157">**Sutarties** srityje rodomas bendras kiekis arba bendra suma, kuriems yra taikoma pardavimo sutarties eilutė.</span><span class="sxs-lookup"><span data-stu-id="d10ec-157">The **Agreement** area shows the total quantity or the total amount that the sales agreement line is valid for.</span></span>  

<span data-ttu-id="d10ec-158">Naudoti PU eilutes ir SF eilutes, kurios turi įtakos skaičiuojant įvykdymą, galite eilutėse arba pirkimo sutarties antraštėje pasirinkdami **Susijusios informacijos** veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-158">You can access the PO lines and the invoice lines that contribute to the fulfillment calculation by selecting the **Related information** action on the lines or on the header of a purchase agreement.</span></span>

## <a name="confirmations-and-version-history-for-purchase-agreements"></a><span data-ttu-id="d10ec-159">Pirkimo sutarčių tvirtinimas ir versijų retrospektyva</span><span class="sxs-lookup"><span data-stu-id="d10ec-159">Confirmations and version history for purchase agreements</span></span>
<span data-ttu-id="d10ec-160">Patvirtinus pirkimo sutartį esama pirkimo sutarties versija yra saugoma retrospektyvos lentelėje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-160">When you confirm a purchase agreement, the current version of the purchase agreement is stored in a history table.</span></span> <span data-ttu-id="d10ec-161">Jei pakeisite pirkimo sutartį, galite ją patvirtinti dar kartą, norėdami saugoti kitą pirkimo sutarties versiją retrospektyvoje.</span><span class="sxs-lookup"><span data-stu-id="d10ec-161">If you change the purchase agreement, you can confirm it again to store another version of the purchase agreement in the history.</span></span> <span data-ttu-id="d10ec-162">Jei pirkimo sutarties nepatvirtinote, vis tiek galite ją naudoti, norėdami kurti PU.</span><span class="sxs-lookup"><span data-stu-id="d10ec-162">If you don't confirm a purchase agreement, you can still use it to create POs.</span></span> <span data-ttu-id="d10ec-163">Tačiau pirkimo sutarties retrospektyvos informacija nesaugoma.</span><span class="sxs-lookup"><span data-stu-id="d10ec-163">However, the history information for the purchase agreement isn't stored.</span></span> <span data-ttu-id="d10ec-164">Galite peržiūrėti arba spausdinti visas sutarties versijas.</span><span class="sxs-lookup"><span data-stu-id="d10ec-164">You can preview or print all versions of the agreement.</span></span> <span data-ttu-id="d10ec-165">Pakeitimais galite pasidalinti su tiekėju, norėdami gauti patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="d10ec-165">You can then share the revisions with your vendor to obtain approval.</span></span>

## <a name="applying-purchase-agreements-in-the-ordering-process"></a><span data-ttu-id="d10ec-166">Pirkimo sutarčių taikymas užsakymo procese</span><span class="sxs-lookup"><span data-stu-id="d10ec-166">Applying purchase agreements in the ordering process</span></span>
<span data-ttu-id="d10ec-167">Kurdami PU, jam galite taikyti pirkimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="d10ec-167">When you create a PO, you can apply a purchase agreement to it.</span></span> <span data-ttu-id="d10ec-168">Tada į PU antraštę kopijuojama informacija iš sutarties sąlygų, pvz., mokėjimo sąlygos, pristatymo sąlygos ir pristatymo adresas.</span><span class="sxs-lookup"><span data-stu-id="d10ec-168">Information from the terms for the agreement, such as the payment terms, delivery terms, and delivery address, is then copied to the header of the PO.</span></span> <span data-ttu-id="d10ec-169">Jei PU yra viena ar kelios produktų ar kategorijų eilutės, kurioms taikoma sutartis, tose eilutėse naudojamos kainos ir nuolaidos iš pirkimo sutarties.</span><span class="sxs-lookup"><span data-stu-id="d10ec-169">If the PO contains one or more lines for products or categories that are covered by the agreement, the prices and discounts from the purchase agreement are used for those lines.</span></span> <span data-ttu-id="d10ec-170">Užsakymo eilutės suma arba kiekis prisideda prie pirkimo sutarties įsipareigojimo įvykdymo.</span><span class="sxs-lookup"><span data-stu-id="d10ec-170">The amount or quantity on the order line contributes to the fulfillment of the commitment in the purchase agreement.</span></span> <span data-ttu-id="d10ec-171">Tame pačiame PU gali būti eilučių, kurios nesusijusios su pirkimo sutartimi ir eilučių, kurios susijusios su pirkimo sutarties įsipareigojimu.</span><span class="sxs-lookup"><span data-stu-id="d10ec-171">The same PO can include both lines that aren't related to a purchase agreement and lines that have a commitment for a purchase agreement.</span></span>  

<span data-ttu-id="d10ec-172">Pasirinkti pirkimo sutartį galite tik tada, kai kuriate PU.</span><span class="sxs-lookup"><span data-stu-id="d10ec-172">You can select a purchase agreement only when you're creating a PO.</span></span> <span data-ttu-id="d10ec-173">Kai PU sukurtas, pirkimo sutarties pasirinkti negalite.</span><span class="sxs-lookup"><span data-stu-id="d10ec-173">You can't select a purchase agreement after the PO has been created.</span></span>  
<span data-ttu-id="d10ec-174">Kai kuriose situacijose, kuriose PU kuriami netiesiogiai, galite valdyti, ar „Finance and Operations“ turi automatiškai ieškoti taikytinų pirkimo sutarčių.</span><span class="sxs-lookup"><span data-stu-id="d10ec-174">In some situations where POs are created indirectly, you can control whether Finance and Operations automatically searches for applicable purchase agreements.</span></span> <span data-ttu-id="d10ec-175">Pavyzdžiui, galite tai atlikti automatiškai patvirtindami suplanuotus PU arba kurdami PU pagal pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="d10ec-175">For example, you might do this when you're automatically firming planned POs or creating POs that are based on sales orders.</span></span>

## <a name="purchase-agreements-and-intercompany-trade"></a><span data-ttu-id="d10ec-176">Pirkimo sutartys ir vidinės įmonės prekyba</span><span class="sxs-lookup"><span data-stu-id="d10ec-176">Purchase agreements and intercompany trade</span></span>
<span data-ttu-id="d10ec-177">Vidinės įmonės prekybiniai ryšiai gali būti sukurti tarp tiekėjo ir kliento sąskaitų, esančių skirtinguose juridiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="d10ec-177">Intercompany trading relationships can be created between vendor accounts and customer accounts that are in different legal entities.</span></span> <span data-ttu-id="d10ec-178">Kai sukuriamas vienos iš šalių pardavimo užsakymas arba PU, sukuriama vidinės kompanijos užsakymų grandinė.</span><span class="sxs-lookup"><span data-stu-id="d10ec-178">When a sales order or PO is created for one of the parties, an intercompany order chain is created.</span></span> <span data-ttu-id="d10ec-179">Užsakymų grandinėje pardavimo užsakymas ir PU yra sukuriami atitinkamuose teisiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="d10ec-179">In the order chain, the sales order and PO are created in the appropriate legal entities.</span></span>  

<span data-ttu-id="d10ec-180">Galite kurti pirkimo sutartį arba pardavimo sutartį vienai savo vidinės įmonės prekybos pusei.</span><span class="sxs-lookup"><span data-stu-id="d10ec-180">You can create a purchase agreement or sales agreement for one of the intercompany trading parties.</span></span> <span data-ttu-id="d10ec-181">Tada galite generuoti atitinkamą pardavimo sutartį arba pirkimo sutartį kitos vidinės įmonės prekybos šalies juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="d10ec-181">You can then generate the corresponding sales agreement or purchase agreement for the other intercompany trading party in the other legal entity.</span></span>  

<span data-ttu-id="d10ec-182">Jei sukuriate vidinės įmonės PU, kuris naudoja vidinės įmonės pirkimo sutartį viename juridiniame subjekte, atitinkamas vidinės įmonės pardavimo užsakymas naudoja atitinkamos vidinės įmonės pardavimo sutartį kitame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="d10ec-182">If you create an intercompany PO that uses the intercompany purchase agreement in one legal entity, the corresponding intercompany sales order uses the corresponding intercompany sales agreement in the other legal entity.</span></span> <span data-ttu-id="d10ec-183">Pardavimo sutarties įsipareigojimų vykdymas ir pirkimo sutarčių vykdymas sinchronizuojami, kaip sinchronizuojami vidinės įmonės pardavimo užsakymas ir vidinės įmonės PU.</span><span class="sxs-lookup"><span data-stu-id="d10ec-183">The fulfillment of the sales agreement commitments and the fulfillment of the purchase agreements are synchronized, just as the intercompany sales order and the intercompany PO are synchronized.</span></span>

## <a name="financial-dimensions-on-purchase-agreements"></a><span data-ttu-id="d10ec-184">Pirkimo sutarčių finansinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="d10ec-184">Financial dimensions on purchase agreements</span></span>
<span data-ttu-id="d10ec-185">Galite nukopijuoti finansines dimensijas į dokumento antraštes arba į atskiras pirkimo sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="d10ec-185">You can copy financial dimensions to document headers or to individual lines of a purchase agreement.</span></span> <span data-ttu-id="d10ec-186">Jei pakeičiate dimensijas sutarties antraštėje arba sutarties eilutėje, pakeitimas neturi įtakos jokiems išleistiems užsakymams, tačiau jis atsispindės visuose naujuose užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="d10ec-186">If you change the dimensions in the agreement header or on the agreement line, the change doesn't affect any released orders, but it will be reflected on any new orders.</span></span>

<a name="see-also"></a><span data-ttu-id="d10ec-187">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="d10ec-187">See also</span></span>
--------

[<span data-ttu-id="d10ec-188">Kurti pirkimo sutartį (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="d10ec-188">Create a purchase agreement (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/procurement/tasks/create-purchase-agreement)

[<span data-ttu-id="d10ec-189">Kurti pirkimo leidimo užsakymą iš pirkimo sutarties (užduočių vedlys)</span><span class="sxs-lookup"><span data-stu-id="d10ec-189">Create a purchase release order from a purchase agreement (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/procurement/tasks/create-purchase-release-order-purchase-agreement)



