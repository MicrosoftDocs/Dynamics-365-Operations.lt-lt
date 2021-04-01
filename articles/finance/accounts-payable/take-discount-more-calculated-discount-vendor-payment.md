---
title: Paimkite daugiau nei apskaičiuota nuolaida pardavėjo mokėjimui
description: Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą. Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a56331f76867aeac0bad0912749d96f959513e0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235890"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="b3c13-104">Paimkite daugiau nei apskaičiuota nuolaida pardavėjo mokėjimui</span><span class="sxs-lookup"><span data-stu-id="b3c13-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3c13-105">Šiame straipsnyje apžvelgiamas scenarijus, kai paimama didesnės sumos mokėjimo nuolaida už iš pradžių sąskaitoje faktūroje nurodytą nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="b3c13-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="b3c13-106">Toks scenarijus galimas, jei organizacija susitaria su tiekėju mokėti mažesnę SF sumą.</span><span class="sxs-lookup"><span data-stu-id="b3c13-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="b3c13-107">Tiekėjas 3051 suteikia „Fabrikam“ 4 procentų mokėjimo nuolaidą, jei sąskaita faktūra apmokama per septynias dienas.</span><span class="sxs-lookup"><span data-stu-id="b3c13-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="b3c13-108">Birželio 29 d. April įveda sąskaitą faktūrą 1000,00 sumai.</span><span class="sxs-lookup"><span data-stu-id="b3c13-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="b3c13-109">Tiekėjas leidžia April pritaikyti 60,00 nuolaidą vietoj numatytosios 40,00 nuolaidos, kuri galima sąskaitai faktūrai.</span><span class="sxs-lookup"><span data-stu-id="b3c13-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="b3c13-110">April įrašo vienkartinį mokėjimą naudodama Mokėtinų sąskaitų mokėjimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b3c13-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="b3c13-111">Ji įveda mokėjimo tiekėją ir tada atidaro puslapį **Sudengti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="b3c13-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="b3c13-112">Eglė pažymi sąskaitą faktūrą ir pakeičia vertę lauke **Mokėjimo nuolaidos suma** į **60,00**.</span><span class="sxs-lookup"><span data-stu-id="b3c13-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="b3c13-113">Žymėti</span><span class="sxs-lookup"><span data-stu-id="b3c13-113">Mark</span></span>     | <span data-ttu-id="b3c13-114">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="b3c13-114">Use cash discount</span></span> | <span data-ttu-id="b3c13-115">Kvitas</span><span class="sxs-lookup"><span data-stu-id="b3c13-115">Voucher</span></span>   | <span data-ttu-id="b3c13-116">Paskyra</span><span class="sxs-lookup"><span data-stu-id="b3c13-116">Account</span></span> | <span data-ttu-id="b3c13-117">Data</span><span class="sxs-lookup"><span data-stu-id="b3c13-117">Date</span></span>      | <span data-ttu-id="b3c13-118">Terminas</span><span class="sxs-lookup"><span data-stu-id="b3c13-118">Due date</span></span>  | <span data-ttu-id="b3c13-119">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="b3c13-119">Invoice</span></span> | <span data-ttu-id="b3c13-120">Suma operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="b3c13-120">Amount in transaction currency</span></span> | <span data-ttu-id="b3c13-121">Valiuta</span><span class="sxs-lookup"><span data-stu-id="b3c13-121">Currency</span></span> | <span data-ttu-id="b3c13-122">Sudengtina suma</span><span class="sxs-lookup"><span data-stu-id="b3c13-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="b3c13-123">Pasirinkta</span><span class="sxs-lookup"><span data-stu-id="b3c13-123">Selected</span></span> | <span data-ttu-id="b3c13-124">Įprastas</span><span class="sxs-lookup"><span data-stu-id="b3c13-124">Normal</span></span>            | <span data-ttu-id="b3c13-125">SF-10040</span><span class="sxs-lookup"><span data-stu-id="b3c13-125">Inv-10040</span></span> | <span data-ttu-id="b3c13-126">3051</span><span class="sxs-lookup"><span data-stu-id="b3c13-126">3051</span></span>    | <span data-ttu-id="b3c13-127">2015-06-29</span><span class="sxs-lookup"><span data-stu-id="b3c13-127">6/29/2015</span></span> | <span data-ttu-id="b3c13-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="b3c13-128">7/29/2015</span></span> | <span data-ttu-id="b3c13-129">10040</span><span class="sxs-lookup"><span data-stu-id="b3c13-129">10040</span></span>   | <span data-ttu-id="b3c13-130">1000,00</span><span class="sxs-lookup"><span data-stu-id="b3c13-130">1,000.00</span></span>                       | <span data-ttu-id="b3c13-131">USD</span><span class="sxs-lookup"><span data-stu-id="b3c13-131">USD</span></span>      | <span data-ttu-id="b3c13-132">940,00</span><span class="sxs-lookup"><span data-stu-id="b3c13-132">940.00</span></span>           |

<span data-ttu-id="b3c13-133">Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje.</span><span class="sxs-lookup"><span data-stu-id="b3c13-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="b3c13-134">Mokėjimo nuolaidos data</span><span class="sxs-lookup"><span data-stu-id="b3c13-134">Cash discount date</span></span>           | <span data-ttu-id="b3c13-135">2015-07-12</span><span class="sxs-lookup"><span data-stu-id="b3c13-135">7/12/2015</span></span> |
| <span data-ttu-id="b3c13-136">Mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="b3c13-136">Cash discount amount</span></span>         | <span data-ttu-id="b3c13-137">60,00</span><span class="sxs-lookup"><span data-stu-id="b3c13-137">60.00</span></span>     |
| <span data-ttu-id="b3c13-138">Naudokite mokėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="b3c13-138">Use cash discount</span></span>            | <span data-ttu-id="b3c13-139">Įprastas</span><span class="sxs-lookup"><span data-stu-id="b3c13-139">Normal</span></span>    |
| <span data-ttu-id="b3c13-140">Pritaikyta mokėjimo nuolaida</span><span class="sxs-lookup"><span data-stu-id="b3c13-140">Cash discount taken</span></span>          | <span data-ttu-id="b3c13-141">0,00</span><span class="sxs-lookup"><span data-stu-id="b3c13-141">0.00</span></span>      |
| <span data-ttu-id="b3c13-142">Taikytinos mokėjimo nuolaidos suma</span><span class="sxs-lookup"><span data-stu-id="b3c13-142">Cash discount amount to take</span></span> | <span data-ttu-id="b3c13-143">60,00</span><span class="sxs-lookup"><span data-stu-id="b3c13-143">60.00</span></span>     |

<span data-ttu-id="b3c13-144">April užregistruoja mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="b3c13-144">April posts the payment journal.</span></span> <span data-ttu-id="b3c13-145">Sąskaita faktūra yra visiškai sudengta naudojant 940.00 mokėjimą ir 60,00 nuolaida.</span><span class="sxs-lookup"><span data-stu-id="b3c13-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]