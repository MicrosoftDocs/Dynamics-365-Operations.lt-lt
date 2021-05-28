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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Pirkimo kaupimas, kuriame yra nulinė suma, registruojamas nulinės vertės produkto gavimo kvite

KB numeris: 4612588

## <a name="symptoms"></a>Požymiai

Kai užregistruojamas gavimo dokumento vertė, kurios vertė lygi nuliui, sistema sukuria registravimą į pirkimo kaupinį, kur suma lygi 0 (nuliui).

## <a name="resolution"></a>Skiriamoji geba

Pagal numatytuosius nustatymus, kai DK registravimus sudaro *Pirkimo, kaupimo* tipas, `IsTransferredIndetail` laukelis yra visada nustatytas į *Santraukos* papildomos knygos operacijas. Todėl sistema sukuria susijusį kvito įrašą, net jei suma lygi 0 (nuliui).

Norėdami praleisti šį registravimo tipą, kai suma lygi 0 (nuliui), pratęskite `subledgerJournalizer.markDoNotTransferEntries` metodą taip, kad jis apimtų `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, kaip parodyta toliau pateiktame pavyzdyje.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
