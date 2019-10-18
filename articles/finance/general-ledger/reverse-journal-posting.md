---
title: Atšaukimo registravimas žurnale
description: Šioje temoje aprašomos galimybės, leidžiančios atšaukti kvitus iš kvitų operacijų sąrašo arba iš finansinių žurnalų.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248590"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="cc89f-103">Atšaukimo registravimas žurnale</span><span class="sxs-lookup"><span data-stu-id="cc89f-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc89f-104">Šioje temoje aprašomos „Microsoft“ „Dynamics 365 Finance“ galimybės, leidžiančios atšaukti visą žurnalą arba atšaukti vieną ar keletą kvitų iš kvitų operacijų sąrašo, neatsižvelgiant į jų kilmę.</span><span class="sxs-lookup"><span data-stu-id="cc89f-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="cc89f-105">Žurnalų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="cc89f-105">Reversing journals</span></span>

<span data-ttu-id="cc89f-106">Galite atšaukti atskiras žurnalo eilutes.</span><span class="sxs-lookup"><span data-stu-id="cc89f-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="cc89f-107">Registruodami atšaukimą žurnale, taip pat galite atšaukti visą finansinį žurnalą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="cc89f-108">Atšaukite žurnalą, atlikę toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc89f-108">To reverse a journal:</span></span> 
- <span data-ttu-id="cc89f-109">Atidarykite finansinį žurnalą ir filtruokite užregistruotus žurnalus</span><span class="sxs-lookup"><span data-stu-id="cc89f-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="cc89f-110">Spustelėkite puslapio viršuje esantį meniu Atšaukti</span><span class="sxs-lookup"><span data-stu-id="cc89f-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="cc89f-111">Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą</span><span class="sxs-lookup"><span data-stu-id="cc89f-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="cc89f-112">Pasirinkite Taip, jei norite, kad būtų naudojamos esamos operacijų datos, arba Ne, kad įvestumėte naują.</span><span class="sxs-lookup"><span data-stu-id="cc89f-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="cc89f-113">Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs norite įvesti naują atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="cc89f-114">Jei pasirinkote Ne, įveskite atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="cc89f-115">Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją</span><span class="sxs-lookup"><span data-stu-id="cc89f-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="cc89f-116">Spustelėkite mygtuką Atšaukti</span><span class="sxs-lookup"><span data-stu-id="cc89f-116">Click the Reverse button</span></span>

<span data-ttu-id="cc89f-117">Operacijos bus atšauktos.</span><span class="sxs-lookup"><span data-stu-id="cc89f-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="cc89f-118">Jei kvitų eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="cc89f-119">Galite peržiūrėti atšaukimo rezultatus peržiūrėję įvykdytos paketinės užduoties komentarus.</span><span class="sxs-lookup"><span data-stu-id="cc89f-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="cc89f-120">Visos klaidos bus įtrauktos į paketinių užduočių retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="cc89f-121">Jei kvitų eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="cc89f-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="cc89f-122">Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, ir priežastys, dėl kurių nepavyko atšaukti.</span><span class="sxs-lookup"><span data-stu-id="cc89f-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="cc89f-123">Spustelėję Gerai, užverkite dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="cc89f-124">Kvitų atšaukimas kvitų operacijų sąraše.</span><span class="sxs-lookup"><span data-stu-id="cc89f-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="cc89f-125">Kvitus taip pat galite atšaukti **Kvitų operacijų sąraše** visose papildomose knygose.</span><span class="sxs-lookup"><span data-stu-id="cc89f-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="cc89f-126">Be to, vienu metu galite atšaukti keletą kvitų.</span><span class="sxs-lookup"><span data-stu-id="cc89f-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="cc89f-127">Norėdami atšaukti vieną ar daugiau kvitų, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc89f-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="cc89f-128">Spustelėkite puslapio viršuje esantį meniu Atšaukti</span><span class="sxs-lookup"><span data-stu-id="cc89f-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="cc89f-129">Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą</span><span class="sxs-lookup"><span data-stu-id="cc89f-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="cc89f-130">Pasirinkite Taip, jei norite, kad būtų naudojamos esamos operacijų datos, arba Ne, kad įvestumėte naują.</span><span class="sxs-lookup"><span data-stu-id="cc89f-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="cc89f-131">Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs norite įvesti naują atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="cc89f-132">Jei pasirinkote Ne, įveskite atšaukimo operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="cc89f-133">Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją</span><span class="sxs-lookup"><span data-stu-id="cc89f-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="cc89f-134">Spustelėkite mygtuką Atšaukti</span><span class="sxs-lookup"><span data-stu-id="cc89f-134">Click the Reverse button</span></span>

<span data-ttu-id="cc89f-135">Operacijos bus atšauktos.</span><span class="sxs-lookup"><span data-stu-id="cc89f-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="cc89f-136">Jei kvitų eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="cc89f-137">Galite peržiūrėti atšaukimo rezultatus peržiūrėję įvykdytos paketinės užduoties komentarus.</span><span class="sxs-lookup"><span data-stu-id="cc89f-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="cc89f-138">Visos klaidos bus įtrauktos į paketinių užduočių retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="cc89f-139">Jei kvitų eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="cc89f-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="cc89f-140">Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, ir priežastys, dėl kurių nepavyko atšaukti.</span><span class="sxs-lookup"><span data-stu-id="cc89f-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="cc89f-141">Spustelėję Gerai, užverkite dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="cc89f-141">Click on Ok to close the dialog.</span></span>

