---
title: "Sudenkite dalinį tiekėjo mokėjimą, kuriam taikomos tiekėjo kredito pažymų nuolaidos"
description: "Šiame straipsnyje žingsnis po žingsnio pateiktas scenarijus, kuriame su sąskaita faktūra sudengiama kredito pažyma."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 849cffa64eaf777f9f4c9243dab41b00fa59ad79
ms.lasthandoff: 03/31/2017


---

# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-vendor-credit-notes"></a>Sudenkite dalinį tiekėjo mokėjimą, kuriam taikomos tiekėjo kredito pažymų nuolaidos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje žingsnis po žingsnio pateiktas scenarijus, kuriame su sąskaita faktūra sudengiama kredito pažyma.

„Fabrikam‟ tiekėjai kredito pažymoms suteikia mokėjimo nuolaidų. 3050 tiekėjas leidžia „Fabrikam“ gauti 1 procento mokėjimo nuolaidą, jei SF apmokama per 14 dienų.

## <a name="invoice-and-credit-memo"></a>SF ir kredito pažyma
Birželio 29 d. Eglė 3050 tiekėjui sukuria sąskaitą faktūrą 1 000,00 sumai. Liepos 2 d. ji sukuria kredito pažymą 200,00 sumai. Iš **Tiekėjų** puslapio April atidaro puslapį **Sudengti operacijas**. Naudodama puslapį **Sudengti operacijas** ji gali pažymėti kredito pažymą ir SF sudengti. Kredito pažymoje apskaičiuojama nuolaida – 2,00. Todėl bendra kredito pažymos vertė sumažinama iki 198,00.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta                 | Įprastas            | SF-10070 | 3050    | 2015-06-29 | 2015-07-29 | 10070   | –1 000,00                      | USD      | –990,00          |
| Pasirinkta ir paryškinta | Įprastas            | CR-10070  | 3050    | 2015-07-02  | 2015-07-29 |         | 200,00                         | USD      | 198,00           |

Kredito pažymos nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas** apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-13 |
| Mokėjimo nuolaidos suma         | 2,00      |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 2,00      |

April spusteli **Registruoti**. Tada ji peržiūri baigtą sudengimą. April mato, kad buvo pritaikyta 198,00 kredito pažymos ir gauta 2,00 nuolaida. Todėl bendroji suma yra 200,00.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra  | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Pasirinkta ir paryškinta | Įprastas            | SF-10070 | 3050    | 2015-06-29 | 2015-07-29 | 10070    | –1 000,00                      | USD      | –200,00          |
| Pasirinkta                 | Įprastas            | CR-10070  | 3050    | 2015-07-02  | 2015-07-29 | CR-10070 | 200,00                         | USD      | 198,00           |

**Tiekėjų operacijų** puslapyje peržiūrėti tiekėjų operacijas April gali **Visų tiekėjų** puslapyje pasirinkdama tiekėją ir veiksmų srityje spustelėdama **Operacijos**. Šiame puslapyje April mato, kad SF balansas yra –800,00. Ji taip pat mato kredito pažymą 198,00 sumai ir 2,00 nuolaidą.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| SF-10070  | PVM sąskaita faktūra          | 2015-06-29 | 10070   |                                      | 1000,00                              | –800,00 | USD      |
| SF-10071  |                  | 2015-07-02  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| NUOL-10071 |  Mokėjimo nuolaida   | 2015-07-02  |         | 2,00                                 |                                       | 0,00    | USD      |
| NUOL-10071 |  Mokėjimo nuolaida   | 2015-07-02  |         |                                      | 2,00                                  | 0,00    | USD      |






