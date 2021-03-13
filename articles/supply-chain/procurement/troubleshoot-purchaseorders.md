---
title: Pirkimo užsakymų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pirkimo užsakymais.
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
ms.openlocfilehash: 7b65c23fc7ac04fc30c0001bee9541a475026018
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007496"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="05c3e-103">Pirkimo užsakymų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="05c3e-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="05c3e-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="05c3e-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="05c3e-105">Veiksmą galima baigti tik tada, kai eilutės numeris yra visiškai paskirstytas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="05c3e-106">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="05c3e-107">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="05c3e-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="05c3e-108">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="05c3e-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="05c3e-109">Kai pirkimo užsakymai importuojami naudojant duomenų valdymą, pirkimo užsakymo eilučių numeriai neatitinka sistemos parametruose nurodyto padidėjimo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-110">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-110">Issue description</span></span>

<span data-ttu-id="05c3e-111">Numatyta, kad automatiškai sugeneruoti pirkimo užsakymo eilučių, kurios importuojamos per *Pirkimo užsakymo eilučių V2* duomenų objektą, numeriai nenaudoja sistemos parametruose nurodyto sistemos eilutės numerio padidėjimo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="05c3e-112">Jei kuriate pirkimo užsakymą rankiniu būdu ir pridedate eilutes per vartotojo sąsają (UI), eilučių numeriai yra padidinami tinkamai.</span><span class="sxs-lookup"><span data-stu-id="05c3e-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="05c3e-113">Tačiau jei naudojate duomenų valdymo sistemą (DMF), jie nėra padidinami tinkamai.</span><span class="sxs-lookup"><span data-stu-id="05c3e-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="05c3e-114">Ši problema kyla dėl to, kad importuojant eilutes per DMF, jei eilučių numeriai dar nėra priskirti importuotam subjektui, sistema naudoja DMF metodą jiems priskirti.</span><span class="sxs-lookup"><span data-stu-id="05c3e-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="05c3e-115">Šis metodas visada padidina eilučių numerius vienu skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="05c3e-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="05c3e-116">Problemos sprendimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-116">Issue workaround</span></span>

<span data-ttu-id="05c3e-117">Įsitikinkite, kad norimų eilučių numeriai jau yra pateikti duomenų subjekto eilutės numerio laukuose, kai importuojate pirkimo užsakymų eilutes.</span><span class="sxs-lookup"><span data-stu-id="05c3e-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="05c3e-118">Šiuo atveju DMF neperrašys eilučių numerių.</span><span class="sxs-lookup"><span data-stu-id="05c3e-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="05c3e-119">Numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="05c3e-120">Jei naudojate mokėtojo kodą, kuris skiriasi nuo kliento kodo, numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo sukūrus pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="05c3e-121">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-121">This behavior is by design.</span></span> <span data-ttu-id="05c3e-122">Numatytosios mokesčių grupės vertės, mokėjimo nuolaidos ir kita kainos informacija yra paremtos kliento, o ne mokėtojo kodu.</span><span class="sxs-lookup"><span data-stu-id="05c3e-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="05c3e-123">Pirkimo užsakymo patvirtinimo metu gaunu klaidos pranešimą „Objekto nuoroda nenustatyta”, arba parodoma išimtis „Iškvietimo paskirties vieta pranešė apie išimtį” tiekėjo SF registravimo metu.</span><span class="sxs-lookup"><span data-stu-id="05c3e-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="05c3e-124">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="05c3e-125">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="05c3e-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="05c3e-126">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="05c3e-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="05c3e-127">Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.</span><span class="sxs-lookup"><span data-stu-id="05c3e-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-128">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-128">Issue description</span></span>

<span data-ttu-id="05c3e-129">Jūs gaunate šią klaidą: „Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.”</span><span class="sxs-lookup"><span data-stu-id="05c3e-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05c3e-130">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-130">Issue resolution</span></span>

<span data-ttu-id="05c3e-131">Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="05c3e-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="05c3e-132">Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="05c3e-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="05c3e-133">Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="05c3e-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="05c3e-134">Ar galima rodyti tik savo sukurtus pirkimo užsakymus?</span><span class="sxs-lookup"><span data-stu-id="05c3e-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="05c3e-135">Šiuo metu ši funkcija negalima.</span><span class="sxs-lookup"><span data-stu-id="05c3e-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="05c3e-136">Ar galiu rezervuoti atsargas ir sukurti operacijas su užregistruotomis atsargomis pirkimo užsakyme?</span><span class="sxs-lookup"><span data-stu-id="05c3e-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-137">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-137">Issue description</span></span>

<span data-ttu-id="05c3e-138">Net kai pirkimo užsakymo prekių būsena yra *Registruota*, jūs vis tiek galite rezervuoti atsargas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="05c3e-139">Kitaip tariant, galite sukurti operacijas su užregistruotomis atsargomis.</span><span class="sxs-lookup"><span data-stu-id="05c3e-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="05c3e-140">Problemos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-140">Reproduce the issue</span></span>

<span data-ttu-id="05c3e-141">Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="05c3e-142">Sukurkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-142">Create a purchase order.</span></span>
2. <span data-ttu-id="05c3e-143">Užregistruokite pirkimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="05c3e-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="05c3e-144">Atkreipkite dėmesį, kad galite generuoti rezervavimus arba operacijas su užregistruotomis atsargomis.</span><span class="sxs-lookup"><span data-stu-id="05c3e-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05c3e-145">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-145">Issue resolution</span></span>

<span data-ttu-id="05c3e-146">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-146">This behavior is by design.</span></span> <span data-ttu-id="05c3e-147">Tikimasi, kad užregistruotos prekės faktiškai atvyko į sandėlį arba į atsargas ir todėl jas galima rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="05c3e-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="05c3e-148">Pirkimo užsakymai neatspindi juridinio subjekto kalbos nustatymų.</span><span class="sxs-lookup"><span data-stu-id="05c3e-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-149">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-149">Issue description</span></span>

<span data-ttu-id="05c3e-150">Produkto pavadinimas pirkimo užsakyme rodomas sistemos kalba, o ne kalba, nustatyta juridiniam subjektui, kuriame buvo sukurtas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="05c3e-151">Problemos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-151">Reproduce the issue</span></span>

<span data-ttu-id="05c3e-152">Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="05c3e-153">Nustatykite sistemos kalbą į *EN-US* (JAV anglų kalba).</span><span class="sxs-lookup"><span data-stu-id="05c3e-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="05c3e-154">Įsitikinkite, kad egzistuoja produktas, kuriame *EN-US* ir *DE* (vokiečių) kalbos yra palaikomos produkto pavadinimo vertimams.</span><span class="sxs-lookup"><span data-stu-id="05c3e-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="05c3e-155">Pakeisti juridinio subjekto kalbą į *DE*.</span><span class="sxs-lookup"><span data-stu-id="05c3e-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="05c3e-156">Juridiniame subjekte, kuriame *DE* yra nustatyta kaip kalba, sukurkite pirkimo užsakymą, kuriame yra produktas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="05c3e-157">Atkreipkite dėmesį, kad produkto pavadinimas vis dar rodomas JAV anglų kalba (sistemos kalba).</span><span class="sxs-lookup"><span data-stu-id="05c3e-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05c3e-158">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-158">Issue resolution</span></span>

<span data-ttu-id="05c3e-159">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-159">This behavior is by design.</span></span> <span data-ttu-id="05c3e-160">Pirkimo užsakymuose produktas visada rodomas sistemos kalba.</span><span class="sxs-lookup"><span data-stu-id="05c3e-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="05c3e-161">Pirkimo užsakymo kalba yra naudojama, kai kuriamas patvirtinimo žurnalas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="05c3e-162">Patvirtintų tiekėjų sąrašas pagal produkto objektą neleidžia pakeisti įsigaliojimo datos.</span><span class="sxs-lookup"><span data-stu-id="05c3e-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-163">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-163">Issue description</span></span>

<span data-ttu-id="05c3e-164">Produktas turi patvirtintą tiekėją, kurio įsigaliojimo data, pavyzdžiui, yra 2018 m. sausio mėn. 11 d. (*11/01/2018*) ir galiojimo data yra *Niekada*.</span><span class="sxs-lookup"><span data-stu-id="05c3e-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="05c3e-165">Jeigu bandysite pakeisti įsigaliojimo datą iki 2018 m. sausio mėn 10 d. (*10/01/2018*) arba 2018 m. sausio mėn. 12 d., (*12/01/2018*), gausite šią klaidą:</span><span class="sxs-lookup"><span data-stu-id="05c3e-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="05c3e-166">Negalima sukurti įrašo patvirtintame tiekėjų sąraše (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="05c3e-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="05c3e-167">Vertė „Galiojimas” turi būti didesnė arba lygi vertei „Įsigaliojimas”.</span><span class="sxs-lookup"><span data-stu-id="05c3e-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05c3e-168">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-168">Issue resolution</span></span>

<span data-ttu-id="05c3e-169">Galite pratęsti tik tokį laikotarpį, kuriam tiekėjas yra patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="05c3e-170">Galioja šios taisyklės:</span><span class="sxs-lookup"><span data-stu-id="05c3e-170">The following rules apply:</span></span>

- <span data-ttu-id="05c3e-171">Norėdami pakeisti įsigaliojimo datą taip, kad ji būtų ankstesnė nei bet kuris esamas faktinis prekės tiekėjo įrašas (laikotarpiai), naujo laikotarpio galiojimo pabaigos data turi būti ankstesnė už visas esamų įrašų galiojimo datas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="05c3e-172">Norėdami pakeisti galiojimo datą taip, kad ji būtų vėlesnė nei bet kuris iš esamų laikotarpių, galiojimo data turi būti vėlesnė nei vėliausia data iš esamų įrašų.</span><span class="sxs-lookup"><span data-stu-id="05c3e-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="05c3e-173">Norėdami sumažinti bendrą laikotarpį, kuriam tiekėjas buvo patvirtintas, turite panaikinti arba modifikuoti esamus įrašus.</span><span class="sxs-lookup"><span data-stu-id="05c3e-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="05c3e-174">Taip pat galite naudoti jungiklį **Sutrumpinti** importavimo metu.</span><span class="sxs-lookup"><span data-stu-id="05c3e-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="05c3e-175">Šis jungiklis panaikina visus esamus įrašus, esančius patvirtintų tiekėjų pagal prekę lentelėje.</span><span class="sxs-lookup"><span data-stu-id="05c3e-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="05c3e-176">Scenarijaus pavyzdyje, kuris aprašytas problemos aprašyme, kur įrašo įsigaliojimo data yra *11/01/2018* ir galiojimo pabaigos data yra *Niekada* galite importuoti naują įrašą, kurio įsigaliojimo data yra *10/01/2018* ir galiojimo pabaigos data yra *Niekada*.</span><span class="sxs-lookup"><span data-stu-id="05c3e-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="05c3e-177">Tačiau negalite sutrumpinti laikotarpio taip, kad įsigaliojimo data būtų atnaujinta į *12/01/2018* per duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="05c3e-178">Turite atlikti šį keitimą per vartotojo sąsają.</span><span class="sxs-lookup"><span data-stu-id="05c3e-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="05c3e-179">Pakeitus pristatymo adresą pirkimo užsakymo antraštėje, pristatymo pavadinimas nėra sinchronizuojamas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="05c3e-180">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="05c3e-180">Issue description</span></span>

<span data-ttu-id="05c3e-181">Pirkimo užsakymo antraštėje esantis adresas atnaujinamas į adresą, kuris nėra pristatymo adresas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="05c3e-182">Nors adresas yra atnaujinamas pirkimo užsakyme, pristatymo pavadinimas nėra atnaujinamas pagal atnaujintą adresą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="05c3e-183">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="05c3e-183">Issue resolution</span></span>

<span data-ttu-id="05c3e-184">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-184">This behavior is by design.</span></span> <span data-ttu-id="05c3e-185">Pasirinktas adresas turi būti klasifikuojamas kaip pristatymo adresas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="05c3e-186">Kitu atveju pristatymo pavadinimas nėra atnaujinamas pagal pasirinktą adresą.</span><span class="sxs-lookup"><span data-stu-id="05c3e-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="05c3e-187">Ar galima rasti vartotoją, kuris atšaukė pirkimo užsakymą?</span><span class="sxs-lookup"><span data-stu-id="05c3e-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="05c3e-188">Ši informacija sekama tik tada, kai pirkimo užsakymui taikomas pakeitimų valdymas.</span><span class="sxs-lookup"><span data-stu-id="05c3e-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="05c3e-189">Jei naudojate keitimų valdymą, galite matyti, kas pateikė pakeitimą (atšaukimą) ir kas jį patvirtino.</span><span class="sxs-lookup"><span data-stu-id="05c3e-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
