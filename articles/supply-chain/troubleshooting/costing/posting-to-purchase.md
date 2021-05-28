---
title: Pirkimo kaupimas, kuriame yra nulinė suma, registruojamas nulinės vertės produkto gavimo kvite
description: Kai užregistruojamas gavimo dokumento vertė, kurios vertė lygi nuliui, sistema sukuria registravimą į pirkimo kaupinį, kur suma lygi 0 (nuliui).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026761"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="1f297-103">Pirkimo kaupimas, kuriame yra nulinė suma, registruojamas nulinės vertės produkto gavimo kvite</span><span class="sxs-lookup"><span data-stu-id="1f297-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="1f297-104">KB numeris: 4612588</span><span class="sxs-lookup"><span data-stu-id="1f297-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="1f297-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="1f297-105">Symptoms</span></span>

<span data-ttu-id="1f297-106">Kai užregistruojamas gavimo dokumento vertė, kurios vertė lygi nuliui, sistema sukuria registravimą į pirkimo kaupinį, kur suma lygi 0 (nuliui).</span><span class="sxs-lookup"><span data-stu-id="1f297-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="1f297-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="1f297-107">Resolution</span></span>

<span data-ttu-id="1f297-108">Pagal numatytuosius nustatymus, kai DK registravimus sudaro *Pirkimo, kaupimo* tipas, `IsTransferredIndetail` laukelis yra visada nustatytas į *Santraukos* papildomos knygos operacijas.</span><span class="sxs-lookup"><span data-stu-id="1f297-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="1f297-109">Todėl sistema sukuria susijusį kvito įrašą, net jei suma lygi 0 (nuliui).</span><span class="sxs-lookup"><span data-stu-id="1f297-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="1f297-110">Norėdami praleisti šį registravimo tipą, kai suma lygi 0 (nuliui), pratęskite `subledgerJournalizer.markDoNotTransferEntries` metodą taip, kad jis apimtų `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, kaip parodyta toliau pateiktame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="1f297-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
