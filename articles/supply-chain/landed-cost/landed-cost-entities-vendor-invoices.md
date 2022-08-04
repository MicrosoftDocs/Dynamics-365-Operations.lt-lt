---
title: Tiekėjo SF objektai
description: Šiame straipsnyje pateikta informacija apie tiekėjo SF objektus, kurie įgalina konfigūruoti vidinių išlaidų arba išorinių išvestinių išlaidų tipų kodus.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f0371cf9862afaf3bc43a44def725c420e9aaf56
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166750"
---
# <a name="vendor-invoice-entities"></a>Tiekėjo SF objektai

[!include [banner](../includes/banner.md)]

Įkainojimo **modulis** įgalina išlaidų tipo kodus konfigūruoti vidinėms išlaidoms arba išoriškai išvestinėms išlaidoms. Jei išlaidos verslui yra išorinės, iš paslaugų teikėjo tikimasi sąskaitos faktūros. Ši SF apdorojama kaip SF žurnalas, kurį galima susieti su reisu, o SF vertė gali būti paskirstyta vienai ar daugiau reiso išlaidų.

Tiekėjo SF objektai įgalina žurnalo eilutės vertę, paskirstoma vienai ar daugiau reiso išlaidų, kurios bendrai naudoti tą patį išlaidų tipo kodą.

Išlaidas galima paskirstyti tik tada, jei yra SF žurnalo antraštė ir SF žurnalo eilutės.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Tiekėjo reiso išlaidų paskirstymai (ITMLedgerJournalCostLinesVoyagesEntity)

Tiekėjo reiso išlaidų paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti vienai ar daugiau išlaidų, kurios taikomos reiso išlaidų srityje. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesVoyagesEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |
| Reisas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Tiekėjo siuntimo konteinerio savikainos paskirstymai (ITMLedgerJournalCostLinesContainersEntity)

Tiekėjo siuntimo konteinerio savikainos paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti pagal vieną ar daugiau išlaidų, kurios taikomos siuntimo konteinerio išlaidų srityje. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesContainersEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Gabenimo konteineris | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |
| Reisas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Tiekėjo registracijos išlaidų paskirstymai (ITMLedgerJournalCostLinesFoliosEntity)

Tiekėjo registracijos išlaidų paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti vienai ar daugiau išlaidų, kurios taikomos registracijos išlaidų srityje. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesFoliosEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Registravimo lapas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Tiekėjo pirkimo užsakymo savikainos paskirstymai (ITMLedgerJournalCostLinesPurchTableEntity)

Tiekėjo pirkimo užsakymo savikainos paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti vienai ar daugiau išlaidų, kurios taikomos pirkimo užsakymo išlaidų srityje. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesPurchTableEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |
| Pirkimo užsakymas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Tiekėjo prekių savikainos paskirstymai (ITMLedgerJournalCostLinesPurchLineEntity)

Tiekėjo prekių išlaidų paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti vienai ar daugiau išlaidų, kurios taikomos prekės išlaidų srityje. Prekės išlaidų sritis padengia pirkimo užsakymo eilutės išlaidas. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesPurchLineEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |
| Pirkimo užsakymas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |
| Pirkimo užsakymo eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Tiekėjo perkėlimo užsakymo eilutės savikainos paskirstymai (ITMLedgerJournalCostLinesTransferLineEntity)

Tiekėjo perkėlimo užsakymo eilutės išlaidų paskirstymo duomenų objektas įgalina tiekėjo SF eilutę paskirstyti vienai ar daugiau išlaidų, kurios taikomos perkėlimo eilutės išlaidų srityje. Šią funkciją palaiko objektas `ITMLedgerJournalCostLinesTransferLineEntity`. Šioje lentelėje pateikiami laukai ir susiejimai, kurie sudaro šį objektą.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Paskirstyta suma | ITMLedgerJournalCostLines.Amount | Skaitinis(32, 6) | Ne | Ne |
| Išlaidų operacijos eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo eilutės numeris | ITMLedgerJournalCostLines.RefRecId | Skaitinis(32, 16) | **Taip** | Ne |
| Žurnalo numeris | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Taip** | Ne |
| Perkėlimo užsakymas | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Taip** | Ne |
| Perkėlimo užsakymo eilutės numeris | ITMLedgerJournalCostLines.CostTransRefRecId | Skaitinis(32, 16) | **Taip** | Ne |

### <a name="reference-table"></a>Nuorodų lentelė

Reiso sąnaudų eilutės tiesiogiai susiję su išlaidų operacijos įrašu. Šis įrašas apima nuorodų **lentelės ID** reikšmę. Ši vertė yra unikali kiekvienai išlaidų zonai (reisui, siuntimo konteineriui ir taip toliau). Kai konkretūs lentelės numeriai yra nurodomi duomenims, kurie kuriami naudojant duomenų objektus, objektai skaidomi remiantis nuorodos **lentelės ID vertėmis**.

Nuorodų lentelės () ir operacijos tipo (`RefTableId``TransType`) vertės yra netiesiogiai nustatytos kaip savikainos pirkimo eilutė Įkrauta arba Savikainos perkėlimo eilutės objektas.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Tiekėjo SF žurnalo eilutės (VendorInvoiceJournalLineEntity)

Prieš tai, kai žurnalo eilutės vertė gali būti priskirta vienai ar **daugiau** išlaidų modulyje Įkainota, žurnalo eilutė turi būti susieta su išlaidų sritis. Kad ši funkcija būtų efektyvi, į žurnalo **eilučių** lentelę () į žurnalo eilučių lentelę () šis modulis įtraukia keletą naujų laukų`LedgerJournalTrans`.

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Laukai, įtraukti į tiekėjo SF žurnalo eilutės objektą

Šioje lentelėje pateikiami laukai, kuriuos įkeltas **išlaidų modulis prideda** prie tiekėjo SF žurnalo eilutės objekto (`VendorInvoiceJournalLineEntity`). Šie laukai įgalina sistemą sukurti žurnalo eilutes ir prieš jas paskirstyti išlaidas.

| Vardas | Susiejimas | Duomenų tipas | Raktas | Privalomas |
|---|---|---|---|---|
| Išlaidų sritis | LedgerJournalTrans.ITMCostArea | Int | Ne | Ne |
| Išlaidų tipo kodas | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Ne | Ne |

### <a name="mainoffset-account"></a>Pagrindinė/korespondentinė sąskaita

PAGRINDINĖ/korespondentinė sąskaita SF žurnalo eilutei, susietai su įkrautos savikainos reisu, nustatoma pagal išlaidų tipo kodą. Kai išlaidų tipo kodas įtraukiamas į SF žurnalo eilutę, kodo tarpuskaitos sąskaita bus naudojama kaip pagrindinė sąskaita arba korespondentinė sąskaita, atsižvelgiant į scenarijų:

- **Vienos eilutės žurnalas** – jei nustatyta pagrindinė sąskaita (kitaip tariant, tiekėjo sąskaita) ir pateikiamas išlaidų tipo kodas, to išlaidų tipo kodo kliringo sąskaitos vertė bus įvesta į korespondentinę sąskaitą.
- **Kelių eilučių žurnalas** – jei pagrindinė sąskaita nėra nustatyta, bet pateikiamas išlaidų tipo kodas, to išlaidų tipo kodo kliringo sąskaitos vertė bus įvesta į pagrindinę sąskaitą. Žurnalo eilutė, kuri kredituoja tiekėją, nenurodo išlaidų tipo kodo.

## <a name="sequencing"></a>Seka

Pirmiausia reikia sukurti reiso įrašą dėl žurnalo ir žurnalo eilučių lentelių priklausomybės. Reiso eilutes galima kurti tik sukūrus reisą, siuntimo konteinerį ir foms.

Norint paskirstyti reiso SF, sistema turi apdoroti objektus tokia tvarka:

1. SF žurnalo antraštė (`VendInvoiceJournalHeaderEntity`)
1. SF žurnalo eilutė (`VendInvoiceJournalLineEntity`)
1. Įkainotos savikainos paskirstymai (`ITMLedgerJournalEntities`)
