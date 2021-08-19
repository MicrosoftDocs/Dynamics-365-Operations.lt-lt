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
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722180"
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
