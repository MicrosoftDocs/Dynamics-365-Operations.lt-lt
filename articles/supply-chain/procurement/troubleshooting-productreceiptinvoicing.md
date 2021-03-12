---
title: Gavimo dokumentų ir sąskaitos faktūros (SF) išrašymo trikčių šalinimas
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su gavimo dokumentais ir SF išrašymu.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999058"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="3880a-103">Gavimo dokumentų ir sąskaitos faktūros (SF) išrašymo trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="3880a-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="3880a-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su gavimo dokumentais ir SF išrašymu.</span><span class="sxs-lookup"><span data-stu-id="3880a-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="3880a-105">Negaliu registruoti daugiau nei vienos pirkimo užsakymo eilutės, kuriai priklauso kategorija pagrįstos prekės, SF.</span><span class="sxs-lookup"><span data-stu-id="3880a-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="3880a-106">Kiekis yra privalomas, jei norite registruoti SF.</span><span class="sxs-lookup"><span data-stu-id="3880a-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="3880a-107">Todėl, jei visam eilutės kiekiui, kuriam SF išrašyta, yra išrašoma tik dalinė suma, ant kitos SF likusios sumos išrašyti negalėsite.</span><span class="sxs-lookup"><span data-stu-id="3880a-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="3880a-108">Pirkimo užsakymo patvirtinimo metu gaunu klaidos pranešimą „Objekto nuoroda nenustatyta”, arba parodoma išimtis „Iškvietimo paskirties vieta pranešė apie išimtį” tiekėjo SF registravimo metu.</span><span class="sxs-lookup"><span data-stu-id="3880a-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="3880a-109">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="3880a-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="3880a-110">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="3880a-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="3880a-111">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="3880a-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="3880a-112">Negaliu konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3880a-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="3880a-113">Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą, jei skirtingų gavimo dokumentų eilučių apskaitos datos skiriasi.</span><span class="sxs-lookup"><span data-stu-id="3880a-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="3880a-114">Šioje situacijoje, ankstesnėse „Microsoft Dynamics 365 Supply Chain Management” versijose, konsolidavimas buvo leistinas.</span><span class="sxs-lookup"><span data-stu-id="3880a-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="3880a-115">Tačiau ši praktika yra linkusi į klaidą.</span><span class="sxs-lookup"><span data-stu-id="3880a-115">However, the practice is prone to error.</span></span> <span data-ttu-id="3880a-116">Sukuriamų pirkimo užsakymo eilučių apskaitos data neturėtų skirtis nuo gavimo dokumento eilučių, kur buvo sukurtos šios pirkimo užsakymo eilutės, apskaitos datos.</span><span class="sxs-lookup"><span data-stu-id="3880a-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="3880a-117">(Pirkimo užsakymo eilučių apskaitos data sutampa su pirkimo užsakymo antraštės apskaitos data.) Todėl kelių gavimo dokumentų konsolidavimas į vieną pirkimo užsakymą nebeleidžiamas.</span><span class="sxs-lookup"><span data-stu-id="3880a-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="3880a-118">Apskaitos data naudojama, pvz., biudžeto lėšų rezervavimui ir biudžeto rezervavimui.</span><span class="sxs-lookup"><span data-stu-id="3880a-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="3880a-119">Todėl ji turi būti laikoma perėjimo iš gavimo dokumento į pirkimo užsakymą metu.</span><span class="sxs-lookup"><span data-stu-id="3880a-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="3880a-120">Atšaukiant gavimo dokumentus, operacijos gali būti registruojamos laikinai sustabdytoje DK sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="3880a-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3880a-121">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3880a-121">Issue description</span></span>

<span data-ttu-id="3880a-122">Jei gavimo dokumentas yra atšauktas, sistema leidžia operacijas užregistruoti laikinai sustabdytose DK sąskaitose, net jei pagrindinės sąskaitos yra sustabdytos.</span><span class="sxs-lookup"><span data-stu-id="3880a-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="3880a-123">Problemos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="3880a-123">Reproduce the issue</span></span>

<span data-ttu-id="3880a-124">Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.</span><span class="sxs-lookup"><span data-stu-id="3880a-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="3880a-125">**Mokėtinų sumų parametrai** puslapyje, skirtuke **Bendra**, įsitikinkite, kad parinktis **Gavimo dokumentą registruoti DK** nustatyta kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="3880a-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="3880a-126">Sukurkite pirkimo užsakymą ir pridėkite užsakymo eilutę, kurioje yra kiekis lygus *1000* vienam produktui.</span><span class="sxs-lookup"><span data-stu-id="3880a-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="3880a-127">Patvirtinkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3880a-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="3880a-128">Užregistruokite gavimo dokumentą ir patikrinkite kvitus.</span><span class="sxs-lookup"><span data-stu-id="3880a-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="3880a-129">Sustabdykite atitinkamas pagrindines sąskaitas, *200140* ir *140200*.</span><span class="sxs-lookup"><span data-stu-id="3880a-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="3880a-130">Atšaukite užregistruotą gavimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="3880a-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="3880a-131">Atkreipkite dėmesį, kad operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="3880a-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3880a-132">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3880a-132">Issue resolution</span></span>

<span data-ttu-id="3880a-133">Operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose, kai atšaukiami gavimo dokumentai, nes toks veikimo būdas leidžia atlikti teisingus registravimus.</span><span class="sxs-lookup"><span data-stu-id="3880a-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="3880a-134">Produkto gavimo kvito numeris sunaudotas, net jei produkto gavimo metu nesukuriamas joks fin. kvitas.</span><span class="sxs-lookup"><span data-stu-id="3880a-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="3880a-135">Jei pasirinktis **Sukaupti įsipareigojimus gavimo dokumente** prekės modelių grupei nustatyta kaip *Ne*, didžiojoje knygoje nebus vykdomi jokie registravimai.</span><span class="sxs-lookup"><span data-stu-id="3880a-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="3880a-136">Tačiau faktinis įvykis bus įrašytas papildomos knygos apskaitos tikslais, o tam įvykiui būtinas kvito numeris.</span><span class="sxs-lookup"><span data-stu-id="3880a-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="3880a-137">Šis kvito numeris yra numeris, nurodomas atsargų operacijose.</span><span class="sxs-lookup"><span data-stu-id="3880a-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="3880a-138">Rekomenduojame nustatyti pasirinktį **Sukaupti įsipareigojimus gavimo dokumente** kaip *Taip*, kaip ir aprašyta šiame tinklaraščio įraše: [Registruoti pap. išlaidas produkto gavimo metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="3880a-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="3880a-139">„Registruoti DK mokesčių sąskaitoje” parametras nėra įjungtas.</span><span class="sxs-lookup"><span data-stu-id="3880a-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3880a-140">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="3880a-140">Issue description</span></span>

<span data-ttu-id="3880a-141">Ši problema atsiranda, kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF**, esančiame **Mokėtinų sumų parametrai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3880a-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="3880a-142">Problemos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="3880a-142">Reproduce the issue</span></span>

<span data-ttu-id="3880a-143">Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.</span><span class="sxs-lookup"><span data-stu-id="3880a-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="3880a-144">Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3880a-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="3880a-145">**SF** skirtuke nustatykite pasirinktį **Registruoti DK mokesčių sąskaitoje** kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="3880a-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="3880a-146">Eikite į **Atsargų valdymas \> Sąranka \> Registravimas \> Registravimas**.</span><span class="sxs-lookup"><span data-stu-id="3880a-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="3880a-147">**Pirkimo užsakymas** skirtuke įsitikinkite, kad panaikinote visas produkto pirkimo išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="3880a-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="3880a-148">Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3880a-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="3880a-149">Sukurkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3880a-149">Create a purchase order.</span></span> <span data-ttu-id="3880a-150">**Tiekėjo sąskaita** lauke pasirinkite *1001 Acme biuro reikmenys*.</span><span class="sxs-lookup"><span data-stu-id="3880a-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="3880a-151">Pridėkite pirkimo užsakymo eilutę, kuriai nustatyti šie parametrai:</span><span class="sxs-lookup"><span data-stu-id="3880a-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="3880a-152">**Prekės numeris:** *D0011 lazerinis projektorius*</span><span class="sxs-lookup"><span data-stu-id="3880a-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="3880a-153">**Vieta:** *1*</span><span class="sxs-lookup"><span data-stu-id="3880a-153">**Site:** *1*</span></span>
    - <span data-ttu-id="3880a-154">**Sandėlis:** *11*</span><span class="sxs-lookup"><span data-stu-id="3880a-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="3880a-155">**Kiekis:** *4*</span><span class="sxs-lookup"><span data-stu-id="3880a-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="3880a-156">Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmas**, pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="3880a-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="3880a-157">Veiksmų srities skirtuke **Gauti**, grupėje **Generuoti**, pasirinkite **Gavimo dokumentas**.</span><span class="sxs-lookup"><span data-stu-id="3880a-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="3880a-158">Dialogo lange **Registruojamas gavimo dokumentas**, lauke **Gavimo dokumentas**, įveskite pasirinktinį numerį ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3880a-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="3880a-159">Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.</span><span class="sxs-lookup"><span data-stu-id="3880a-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="3880a-160">Lauke **Numeris** įveskite pasirinktinį numerį kaip SF numerį.</span><span class="sxs-lookup"><span data-stu-id="3880a-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="3880a-161">Atnaujinkite gretinimo būseną ir registruokite.</span><span class="sxs-lookup"><span data-stu-id="3880a-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="3880a-162">Atkreipkite dėmesį, kad kai generuojate SF iš pirkimo užsakymo, dabar gausite šią klaidą: „Produkto pirkimo išlaidų operacijos tipui sąskaitos numerio nėra.”</span><span class="sxs-lookup"><span data-stu-id="3880a-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3880a-163">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3880a-163">Issue resolution</span></span>

<span data-ttu-id="3880a-164">Tai priklauso nuo SF ir SF grupių parametrų nustatymų.</span><span class="sxs-lookup"><span data-stu-id="3880a-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="3880a-165">Norėdami gauti daugiau informacijos, žr. šį tinklaraščio įrašą: [Pirkimo mokesčio ir atsargų nuokrypio apskaita](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="3880a-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
