---
title: Atšaukimo registravimas žurnale
description: Šioje temoje aprašomos galimybės, leidžiančios atšaukti kvitus iš kvitų operacijų sąrašo arba iš finansinių žurnalų.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d18b71c1fc7f3f0c39172bd9edf19b4e60a2bf8
ms.sourcegitcommit: cfaad79bcb1460ee0e7ad5a2c596f9199e14c53a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/08/2020
ms.locfileid: "2944433"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="f2561-103">Atšaukimo registravimas žurnale</span><span class="sxs-lookup"><span data-stu-id="f2561-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2561-104">Šioje temoje aprašomos „Microsoft Dynamics 365 Finance“ galimybės, leidžiančios atšaukti visą žurnalą arba atšaukti vieną ar keletą kvitų iš kvitų operacijų sąrašo, neatsižvelgiant į jų kilmę.</span><span class="sxs-lookup"><span data-stu-id="f2561-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="f2561-105">Žurnalų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f2561-105">Reversing journals</span></span>

<span data-ttu-id="f2561-106">Galite atšaukti atskiras žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="f2561-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="f2561-107">Registruodami atšaukimą žurnale, taip pat galite atšaukti visą finansinį žurnalą.</span><span class="sxs-lookup"><span data-stu-id="f2561-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="f2561-108">Atšaukite žurnalą, atlikę toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f2561-108">To reverse a journal:</span></span> 

- <span data-ttu-id="f2561-109">Atidarykite finansinį žurnalą ir filtruokite paskelbtus žurnalus.</span><span class="sxs-lookup"><span data-stu-id="f2561-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="f2561-110">Pasirinkite puslapio viršuje esantį meniu **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="f2561-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="f2561-111">Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą</span><span class="sxs-lookup"><span data-stu-id="f2561-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="f2561-112">Pasirinkite **Taip**, jei norite, kad būtų naudojamos esamos operacijų datos, arba **Ne**, kad įvestumėte naują.</span><span class="sxs-lookup"><span data-stu-id="f2561-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="f2561-113">Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs turite įvesti naują atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="f2561-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="f2561-114">Jei pasirinksite **Ne**, įveskite atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="f2561-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="f2561-115">Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="f2561-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="f2561-116">Paspauskite mygtuką **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="f2561-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="f2561-117">Operacijos bus atšauktos.</span><span class="sxs-lookup"><span data-stu-id="f2561-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="f2561-118">Jei kvito eilučių skaičius viršija 100, atšaukimo procesas bus vykdomas naudojant paketinį procesą.</span><span class="sxs-lookup"><span data-stu-id="f2561-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="f2561-119">Rezultatus galite peržiūrėti peržiūrėdami paketinės užduoties komentarus.</span><span class="sxs-lookup"><span data-stu-id="f2561-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="f2561-120">Visos operacijos, kurių negalima atšaukti, bus įtrauktos į paketinės užduoties retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="f2561-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="f2561-121">Jei kvito eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="f2561-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="f2561-122">Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, kartu su priežastimis, dėl kurių nepavyko atšaukti.</span><span class="sxs-lookup"><span data-stu-id="f2561-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="f2561-123">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f2561-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="f2561-124">Kvitų atšaukimas kvitų operacijų sąraše.</span><span class="sxs-lookup"><span data-stu-id="f2561-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="f2561-125">Kvitus taip pat galite atšaukti **Kvitų operacijų sąraše** visose papildomose knygose.</span><span class="sxs-lookup"><span data-stu-id="f2561-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="f2561-126">Be to, vienu metu galite atšaukti keletą kvitų.</span><span class="sxs-lookup"><span data-stu-id="f2561-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="f2561-127">Norėdami atšaukti vieną ar daugiau kvitų, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f2561-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="f2561-128">Pasirinkite puslapio viršuje esantį meniu **Atšaukti**</span><span class="sxs-lookup"><span data-stu-id="f2561-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="f2561-129">Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių kiekį.</span><span class="sxs-lookup"><span data-stu-id="f2561-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="f2561-130">Pasirinkite **Taip**, jei norite, kad būtų naudojamos esamos operacijų datos, arba **Ne**, kad įvestumėte naują.</span><span class="sxs-lookup"><span data-stu-id="f2561-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="f2561-131">Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs turite įvesti naują operacijos datą, kad ją atšauktumėte.</span><span class="sxs-lookup"><span data-stu-id="f2561-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="f2561-132">Jei pasirinksite **Ne**, įveskite atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="f2561-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="f2561-133">Įveskite komentarą, kad aprašytumėte atšaukimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="f2561-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="f2561-134">Paspauskite mygtuką **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="f2561-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="f2561-135">Operacijos bus atšauktos.</span><span class="sxs-lookup"><span data-stu-id="f2561-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="f2561-136">Jei kvito eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą.</span><span class="sxs-lookup"><span data-stu-id="f2561-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="f2561-137">Rezultatus galite peržiūrėti peržiūrėdami paketinės užduoties komentarus.</span><span class="sxs-lookup"><span data-stu-id="f2561-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="f2561-138">Visos operacijos, kurių negalima atšaukti, bus įtrauktos į paketinės užduoties retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="f2561-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="f2561-139">Jei kvito eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="f2561-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="f2561-140">Rezultatai bus rodomi dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, kartu su priežastimis.</span><span class="sxs-lookup"><span data-stu-id="f2561-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="f2561-141">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="f2561-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="f2561-142">Operacijas galima atšaukti tik tuo atveju, jei jos atitinka atšaukimui taikomas verslo taisykles.</span><span class="sxs-lookup"><span data-stu-id="f2561-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="f2561-143">Tiekėjo mokėjimų negalima atšaukti naudojant šioje temoje aprašytą funkciją.</span><span class="sxs-lookup"><span data-stu-id="f2561-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="f2561-144">Tiekėjo mokėjimai turi būti atšaukiami atliekant veiksmus, aprašytus [Tiekėjo mokėjimo atšaukimas](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="f2561-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

