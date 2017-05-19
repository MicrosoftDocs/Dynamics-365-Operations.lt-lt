---
title: "Sudenkite dalinį kliento mokėjimą, kuriam taikomos kredito pažymų nuolaidos"
description: "Šiame straipsnyje apžvelgiamas scenarijus, kai mokėjimo nuolaida taikoma kredito pažymai, kai mokėjimo nuolaida taip pat buvo taikoma pradinei SF."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 39056251c868c5683ed64a2e18168ed45bc27d61
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Sudenkite dalinį kliento mokėjimą, kuriam taikomos kredito pažymų nuolaidos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamas scenarijus, kai mokėjimo nuolaida taikoma kredito pažymai, kai mokėjimo nuolaida taip pat buvo taikoma pradinei SF. 

„Fabrikam“ klientams leidžia mokėjimo nuolaidas taikyti daliniams mokėjimams ir kredito pažymoms (kredito pažymoms). Mokėjimo nuolaidą galima taikyti kredito pažymai, kai kredito pažyma išduodama SF, kuriai klientas pritaikė mokėjimo nuolaidą. Galite ne teikti visos sumos kreditą, o kliento balansą kredituoti sumai, į kurią kliento pritaikytas mokėjimo nuolaidos procentas neįtrauktas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoice-and-credit-note"></a>SF ir kredito pažyma
4035 klientas turi 1 000,00 SF ir 100,00 kredito pažymą. Kiekvienam dokumentui taikoma 1 procento nuolaida, jei jis sudengiamas per 14 dienų. Arnas gali šią informaciją peržiūrėti puslapyje **Kliento operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra  | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10050  | PVM sąskaita faktūra          | 2015-06-28 | 10050    | 1000,00                             |                                       | 1000,00 | USD      |
| CCRN-10050 | Kredito pažyma      | 2015-06-28 | CR-10050 |                                      | 100,00                                | -100.00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Kredito pažymos sudengimas naudojant SF
Puslapyje **Kliento operacijos** Arnas atidaro puslapį **Sudengti operacijas**. Naudodamas puslapį **Sudengti operacijas** jis gali sudengti SF ir kredito pažymą. Vykdydamas sudengimo procesą jis peržiūri mokėjimo nuolaidos datas ir sumas. Jis pažymi du dokumentus ir spusteli **Registruoti**, kad sudengtų operacijas. Kredito pažymoje taikoma –1,00 nuolaida, nes „Fabrikam“ leidžia nuolaidas kredito pažymose.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas    | Paskyra | Data      | Terminas  | PVM sąskaita faktūra  | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10050  | 4035    | 2015-06-28 | 2015-07-28 | 10050    | 1000,00                       | USD      | 990,00           |
| Pasirinkta | Įprastas            | CCRN-10050 | 4035    | 2015-06-28 | 2015-07-28 | CR-10050 | -100.00                        | USD      | –99,00           |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-12 |
| Mokėjimo nuolaidos suma         | –1,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | –1,00     |

Bus sudengiama 100,00 suma, įskaitant 99,00 mokėjimą ir 1,00 nuolaidą.




