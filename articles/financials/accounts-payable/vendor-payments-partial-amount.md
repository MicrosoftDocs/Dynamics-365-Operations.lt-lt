---
title: "Tiekėjo dalinės sumos mokėjimai"
description: "Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma. Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti. Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4cc8e2864343b5e9fee8eaf058a51360d15e425a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="30822-105">Tiekėjo dalinės sumos mokėjimai</span><span class="sxs-lookup"><span data-stu-id="30822-105">Vendor payments for a partial amount</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="30822-106">Kartais tiekėjui galite atlikti mokėjimą, kuris yra mažesnis nei sąskaitos faktūros suma.</span><span class="sxs-lookup"><span data-stu-id="30822-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="30822-107">Šiame straipsnyje aprašomos įvairios parinktys šiai situacijai spręsti.</span><span class="sxs-lookup"><span data-stu-id="30822-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="30822-108">Jums prieinamos parinktys priklauso nuo jūsų verslo poreikių ir konfigūracijų.</span><span class="sxs-lookup"><span data-stu-id="30822-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="30822-109">Mokėjimo nuolaidos sumos</span><span class="sxs-lookup"><span data-stu-id="30822-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="30822-110">Tiekėjas gali jums suteikti mokėjimo nuolaidą apmokant SF iki termino pabaigos.</span><span class="sxs-lookup"><span data-stu-id="30822-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="30822-111">Pavyzdžiui, įvedate sąskaitą faktūrą 100,00 sumai, kurioje nurodyta 2 % mokėjimo nuolaida, jei SF apmokama per 10 dienų.</span><span class="sxs-lookup"><span data-stu-id="30822-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="30822-112">Galutinis terminas yra 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="30822-112">The due date terms are 30 days.</span></span> <span data-ttu-id="30822-113">Jei mokėjimo pasiūlyme sąskaitos faktūros pasirinkimo kriterijumi laikoma mokėjimo nuolaida, o pasiūlymas bus įvykdytas mokėjimo nuolaidos dieną ar prieš ją, bus pasirinkta apmokėti pagal šią sąskaitą faktūrą ir bus sukurta 98,00 siekianti mokėjimo suma.</span><span class="sxs-lookup"><span data-stu-id="30822-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="30822-114">Galima pritaikyti mokėjimo nuolaidą ir neautomatiškai sukurtam vienkartiniam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="30822-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="30822-115">Daliniai mokėjimai taikant mokėjimo nuolaidas</span><span class="sxs-lookup"><span data-stu-id="30822-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="30822-116">Kai atliekate dalinį mokėjimą, galite planuoti atlikti papildomą dalinį mokėjimą, kad visiškai sudengtumėte SF.</span><span class="sxs-lookup"><span data-stu-id="30822-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="30822-117">Norėdami daliniam mokėjimui taikyti mokėjimo nuolaidą, puslapyje **Mokėtinų sumų parametrai** turite nustatyti parinkties **Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="30822-117">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments **option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="30822-118">Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo.</span><span class="sxs-lookup"><span data-stu-id="30822-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="30822-119">Užregistruota 100,00 sumos sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="30822-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="30822-120">Jei per 10 dienų sumokėsite 49,00, mokėjimų žurnale įvedate 49,00 siekiantį debetą.</span><span class="sxs-lookup"><span data-stu-id="30822-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="30822-121">Kai sudengsite dalinį mokėjimą puslapyje **Sudengti atidarytas operacijas**, lauke **Taikytina mokėjimo nuolaidos suma** bus rodoma **1,00**.</span><span class="sxs-lookup"><span data-stu-id="30822-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="30822-122">Pastaba. Jei įvesite dalinį mokėjimą ir lauke **Sudengtina suma** paliksite visą sąskaitos faktūros sumą, laukas **Taikytina mokėjimo nuolaidos suma** bus perskaičiuotas automatiškai, kai registruosite operacijas.</span><span class="sxs-lookup"><span data-stu-id="30822-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="30822-123">Kredito pažymos su mokėjimo nuolaidomis</span><span class="sxs-lookup"><span data-stu-id="30822-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="30822-124">Galite grąžinti kai kurias prekes, įtrauktas į SF, ir gauti kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="30822-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="30822-125">Jei mokėjimo nuolaida pritaikyta originaliai SF, galite atimti nuolaidos vertę ir gauti teisingos sumos grąžinimą.</span><span class="sxs-lookup"><span data-stu-id="30822-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="30822-126">Jei puslapyje **Mokėtinų sumų parametrai** nustatyta parinkties **Skaičiuoti kredito pažymų mokėjimo nuolaidas** reikšmė **Taip**, automatiškai apskaičiuojama kredito pažymos nuolaida.</span><span class="sxs-lookup"><span data-stu-id="30822-126">If the **Calculate cash discounts for credit notes **option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="30822-127">Pavyzdžiui, galite gauti 2 % mokėjimo nuolaidą, jei SF apmokama per 10 dienų nuo jo išdavimo.</span><span class="sxs-lookup"><span data-stu-id="30822-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="30822-128">Užregistruota 100,00 sumos SF.</span><span class="sxs-lookup"><span data-stu-id="30822-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="30822-129">Jei grąžinsite prekes ir gausite kredito pažymą, pagal kredito pažymą galėsite įvesti visą pradinės SF 100,00 siekiančią sumą bei kredito pažymoje taip pat nustatytą 2 % mokėjimo nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="30822-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="30822-130">Peržiūrint kredito pažymą puslapyje **Sudengti operacijas**, lauke **Sudengtina suma** bus rodoma **98,00**, o lauke **Mokėjimo nuolaidos suma** bus rodoma **–2,00**.</span><span class="sxs-lookup"><span data-stu-id="30822-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="30822-131">Nuolaidos suma registruojama mokėjimo nuolaidos sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="30822-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="30822-132">Permokėjimo / neprimokėjimo sumos</span><span class="sxs-lookup"><span data-stu-id="30822-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="30822-133">Galite atlikti dalinį mokėjimą, kai suma, kurią vis dar reikia sudengti, yra labai maža.</span><span class="sxs-lookup"><span data-stu-id="30822-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="30822-134">Pvz., tiekėjo SF suma yra 1 000,00 ir jūs sumokate 999,90.</span><span class="sxs-lookup"><span data-stu-id="30822-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="30822-135">Jei likusi suma yra mažesnė už sumą, kuri nurodyta prie permokėjimų arba neprimokėjimų puslapyje **Mokėtinų sumų parametrai**, skirtumas automatiškai užregistruojamas permokėjimų / neprimokėjimų DK sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="30822-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="30822-136">Daugiau informacijos žr. [Tiekėjo mokėjimų apžvalga](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="30822-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>
