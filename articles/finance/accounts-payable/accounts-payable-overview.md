---
title: Mokėtinos sumos sąskaitos faktūros apžvalgos konfigūravimas
description: Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas modulyje Mokėtinos sumos. Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable, DeliveryReason, DeliveryTerms, DestinationCode
audience: Application User
ms.reviewer: roschlom
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff2da881bb77bf7db2c443f3556b4255cd81e3d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972185"
---
# <a name="configure-accounts-payable-overview"></a><span data-ttu-id="f3b1a-104">Mokėtinos sumos sąskaitos faktūros apžvalgos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f3b1a-104">Configure Accounts payable overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3b1a-105">Šiame straipsnyje aprašomi puslapiai, kuriuos naudojate norėdami nustatyti pagrindines ir laisvai pasirenkamas funkcijas modulyje Mokėtinos sumos.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable.</span></span> <span data-ttu-id="f3b1a-106">Jame taip pat aprašomi nustatymo veiksmai, kuriuos turite atlikti prieš pradėdami nustatyti Mokėtinas sumas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="f3b1a-107">Būtinosios Mokėtinų sumų sąrankos sąlygos</span><span class="sxs-lookup"><span data-stu-id="f3b1a-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="f3b1a-108">Prieš nustatydami Mokėtinas sumas, turite atlikti toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="f3b1a-109">Didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-109">In General ledger:</span></span>
    -   <span data-ttu-id="f3b1a-110">Jei planuojate naudoti mokėjimų žurnalus, juos nustatykite.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="f3b1a-111">Jei planuojate vykdyti valiutos kurso koregavimus, puslapyje Valiutos nustatykite valiutų kodus, puslapyje Valiutų kursų tipai nustatykite valiutų kursų tipus, o Valiutų kursų puslapyje nustatykite valiutų kursus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="f3b1a-112">Grynųjų pinigų ir banko valdymo modulyje nustatykite banko sąskaitas, kurias norite naudoti su mokėjimo būdais.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="f3b1a-113">Mokėtinų sumų sąrankos puslapiai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="f3b1a-114">Norėdami nustatyti pagrindines kiekvieno juridinio subjekto Mokėtinų sumų funkcijas, naudokite toliau nurodytus puslapius.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="f3b1a-115">Puslapiai išvardyti rekomenduojama sąrankos tvarka.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="f3b1a-116">Norėdami palengvinti sąrankos procesą, galite kurti šablonus iš pirmųjų sukurtų įrašų.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="f3b1a-117">Šablone reikšmės paprastai įvedamos keliuose laukuose, kad būtų atspindimos savybės, kurias organizacija nori pritaikyti tam tikram klientų tipui.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="f3b1a-118">Mokėjimo sąlygų puslapyje apibrėžkite mokėjimo sąlygas, kurias norite priskirti pardavimo užsakymams, pirkimo užsakymams, klientams ir tiekėjams, ir kurios apibrėžia SF terminus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="f3b1a-119">Daugiau informacijos žr. [Nustatyti tiekėjo mokėjimo mokesčius](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="f3b1a-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="f3b1a-120">Puslapyje Mokėjimo metodai – tiekėjai kurkite ir prižiūrėkite informaciją apie tai, kaip organizacija moka savo tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="f3b1a-121">Tiekėjų grupių puslapyje kurkite ir prižiūrėkite tiekėjų grupes su tokiais pat svarbiais registravimo, sudengimo ir mokėjimo, ataskaitų kūrimo bei prognozavimo parametrais.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="f3b1a-122">Tiekėjų registravimo profilių puslapyje apibrėžkite, kaip tiekėjų operacijos registruojamos į DK.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="f3b1a-123">Mokėtinų sumų parametrų puslapyje nustatykite numatytąsias nuostatas, taikomas, jei nenurodoma konkretesnė nuostata, įvairių funkcijų parametrai ir įvairios Mokėtinų sumų numeracijos.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="f3b1a-124">Formų sąrankos puslapyje apibrėžkite įvairių dokumentų, susijusių su tiekėjais ir kuriuos naudoja organizacija gavimams iš tiekėjų sekti ir mokėjimų tiekėjams nurodyti srauto priežastis, formatą.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="f3b1a-125">Tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų sąskaitas bei mokesčių institucijas, kurioms jūsų organizacija teikia PVM ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="f3b1a-126">Pasirinktiniai mokėtinų sumų sąrankos puslapiai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="f3b1a-127">Be pagrindinių funkcijų, Mokėtinos sumos turi kitų funkcijų, kurias galite nustatyti.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="f3b1a-128">Papildomi sąrankos puslapiai sisteminami pagal funkcijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="f3b1a-129">**Strategijos**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-129">**Policies**</span></span>
-   <span data-ttu-id="f3b1a-130">Tiekėjo SF strategijos puslapyje nustatykite tiekėjo SF strategijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="f3b1a-131">**SF gretinimas**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-131">**Invoice matching**</span></span>

-   <span data-ttu-id="f3b1a-132">SF sumų leistinų nuokrypių puslapyje nustatykite leistinus SF sumų nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="f3b1a-133">Puslapyje Gretinimo strategija nustatykite dvišalio ir trišalio gretinimo strategijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="f3b1a-134">Puslapyje Leistini kainų nuokrypiai nustatykite leistinus vieneto kainų nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="f3b1a-135">Leistinų prekių kainų nuokrypių grupių puslapyje nustatykite leistinų prekių kainų nuokrypių grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="f3b1a-136">Leistinų tiekėjo kainų nuokrypių grupių puslapyje nustatykite leistinų tiekėjo kainų nuokrypių grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="f3b1a-137">Puslapyje Leistini išlaidų nuokrypiai nustatykite leistinus išlaidų nuokrypius.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="f3b1a-138">**Darbo eiga**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-138">**Workflow**</span></span>

-   <span data-ttu-id="f3b1a-139">Mokėtinų sumų darbo eigų puslapyje nustatykite žurnalų patvirtinimo ir pirkimo paraiškų darbo eigų konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="f3b1a-140">**Priežastys**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-140">**Reasons**</span></span>

-   <span data-ttu-id="f3b1a-141">Tiekėjo priežasčių puslapyje nustatykite priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="f3b1a-142">**Mokesčiai**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-142">**Charges**</span></span>

-   <span data-ttu-id="f3b1a-143">Puslapyje Išlaidų kodas nustatykite išlaidų kodus, naudojamus pirkimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="f3b1a-144">Puslapyje Tiekėjo išlaidų grupė kurkite ir prižiūrėkite tiekėjų išlaidų grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="f3b1a-145">Prekių išlaidų grupių puslapyje kurkite ir prižiūrėkite prekių išlaidų grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="f3b1a-146">Automatinių išlaidų puslapyje apibrėžkite išlaidas, kurios yra automatiškai priskiriamos užsakymams.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="f3b1a-147">**Papildomos prekės**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-147">**Supplementary items**</span></span>

-   <span data-ttu-id="f3b1a-148">Papildomų prekių grupių – tiekėjų puslapyje kurkite ir prižiūrėkite tiekėjų papildomų prekių grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="f3b1a-149">Papildomų prekių grupių – atsargų puslapyje kurkite ir prižiūrėkite prekių papildomų prekių grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="f3b1a-150">**Paskirstymas**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-150">**Distribution**</span></span>

-   <span data-ttu-id="f3b1a-151">Pristatymo sąlygų puslapyje kurkite ir prižiūrėkite prekės perdavimo iš pardavėjo pirkėjui sąlygas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="f3b1a-152">Pristatymo būdų puslapyje kurkite ir prižiūrėkite transportavimo būdus, naudojamus pristatant užsakymą iš pardavėjo pirkėjui.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="f3b1a-153">Paskirties kodų puslapyje kurkite ir prižiūrėkite pristatymo vietų identifikatorius ir aprašus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="f3b1a-154">**Formos**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-154">**Forms**</span></span>

-   <span data-ttu-id="f3b1a-155">Formų pastabų puslapyje sukurkite standartinį tekstą, rodomą įvairiuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="f3b1a-156">Formų rūšiavimo parametrų puslapyje nustatykite paraiškų, gavimų sąrašų, važtaraščių ir sąskaitų faktūrų rūšiavimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="f3b1a-157">Spausdinimo valdymo sąrankos puslapyje nustatykite puslapių originalų ir kopijų spausdinimo valdymo informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="f3b1a-158">**Mokėjimai**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-158">**Payments**</span></span>

-   <span data-ttu-id="f3b1a-159">Mokėjimo nuolaidų puslapyje nustatykite ir prižiūrėkite mokėjimo nuolaidų gavimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="f3b1a-160">Mokėjimo nuolaidų kodai susiejami su tiekėjais ir taikomi pirkimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="f3b1a-161">Mokėjimų grafikų puslapyje nustatykite mokėjimų grafikus, kurie naudojami valdant įmokų mokėjimus tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="f3b1a-162">Mokėjimo dienų puslapyje apibrėžkite mokėjimo dienas, naudojamas terminams skaičiuoti, ir nurodykite konkrečios savaitės ar mėnesio dienos mokėjimo dienas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="f3b1a-163">Mokėjimo mokesčio puslapyje kurkite ir prižiūrėkite su tiekėjais susietus mokėjimų mokesčius.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="f3b1a-164">Mokėjimo instrukcijos puslapyje kurkite ir prižiūrėkite mokėjimų instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="f3b1a-165">**Statistika**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-165">**Statistics**</span></span>

-   <span data-ttu-id="f3b1a-166">Skirstymo pagal terminus laikotarpių apibrėžčių puslapyje nustatykite naudotojo apibrėžtus intervalus, kurie naudojami analizuoti tiekėjų sąskaitų paskirstymui pagal mokėjimo terminus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="f3b1a-167">Verslo šakos puslapyje kurkite verslo šakų (LOB) kodus, priskiriamus tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="f3b1a-168">**Mokesčiai 1099**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-168">**Tax 1099**</span></span>

-   <span data-ttu-id="f3b1a-169">Puslapyje **1099 laukai** patikrinkite ir atnaujinkite minimalias sumas, apie kurias reikia pranešti JAV mokesčių inspekcijai (IRS) pagal naujausius jos reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="f3b1a-170">**Papildoma kitų modulių sąranka**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="f3b1a-171">**Organizacijos administravimas**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-171">**Organization administration**</span></span>

-   <span data-ttu-id="f3b1a-172">Numeracijų puslapyje nustatykite SF numerių numeracijų grupes.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="f3b1a-173">Toliau nurodytuose puslapiuose nustatykite adreso informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="f3b1a-174">Adreso sąranka</span><span class="sxs-lookup"><span data-stu-id="f3b1a-174">Address setup</span></span>
    -   <span data-ttu-id="f3b1a-175">NAF kodai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-175">NAF codes</span></span>
    -   <span data-ttu-id="f3b1a-176">Importuoti pašto indeksus</span><span class="sxs-lookup"><span data-stu-id="f3b1a-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="f3b1a-177">**DK**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-177">**General ledger**</span></span>

-   <span data-ttu-id="f3b1a-178">Finansinių dimensijų puslapyje nustatykite finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="f3b1a-179">Toliau nurodytuose puslapiuose nustatykite mokesčių informaciją.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="f3b1a-180">PVM kodai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-180">Sales tax codes</span></span>
    -   <span data-ttu-id="f3b1a-181">PVM grupės</span><span class="sxs-lookup"><span data-stu-id="f3b1a-181">Sales tax groups</span></span>
    -   <span data-ttu-id="f3b1a-182">Prekės PVM grupės</span><span class="sxs-lookup"><span data-stu-id="f3b1a-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="f3b1a-183">Sąskaitų grupė</span><span class="sxs-lookup"><span data-stu-id="f3b1a-183">Account group</span></span>
    -   <span data-ttu-id="f3b1a-184">Neapmokestinimo PVM kodai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="f3b1a-185">PVM jurisdikcijos</span><span class="sxs-lookup"><span data-stu-id="f3b1a-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="f3b1a-186">PVM rinkėjai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="f3b1a-187">PVM sudengimo laikotarpiai</span><span class="sxs-lookup"><span data-stu-id="f3b1a-187">Sales tax settlement periods</span></span>

<span data-ttu-id="f3b1a-188">**Grynųjų pinigų ir banko valdymas**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="f3b1a-189">Mokėjimų paskirčių kodų puslapyje nustatykite centrinio banko paskirties kodą.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





