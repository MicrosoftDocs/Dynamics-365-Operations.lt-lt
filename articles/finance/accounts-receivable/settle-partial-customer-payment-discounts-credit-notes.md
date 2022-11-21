---
title: Sudenkite dalinį kliento mokėjimą, kuriam taikomos kredito pažymų nuolaidos
description: Šiame straipsnyje apžvelgiamas scenarijus, kai mokėjimo nuolaida taikoma kredito pažymai, kai mokėjimo nuolaida taip pat buvo taikoma pradinei SF.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f64b9b9cd4fa65d17ba30fb87a688411becd5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780246"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>Sudenkite dalinį kliento mokėjimą, kuriam taikomos kredito pažymų nuolaidos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas scenarijus, kai mokėjimo nuolaida taikoma kredito pažymai, kai mokėjimo nuolaida taip pat buvo taikoma pradinei SF. 

„Fabrikam“ klientams leidžia mokėjimo nuolaidas taikyti daliniams mokėjimams ir kredito pažymoms (kredito pažymoms). Mokėjimo nuolaidą galima taikyti kredito pažymai, kai kredito pažyma išduodama SF, kuriai klientas pritaikė mokėjimo nuolaidą. Galite ne teikti visos sumos kreditą, o kliento balansą kredituoti sumai, į kurią kliento pritaikytas mokėjimo nuolaidos procentas neįtrauktas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoice-and-credit-note"></a>SF ir kredito pažyma
4035 klientas turi 1 000,00 SF ir 100,00 kredito pažymą. Kiekvienam dokumentui taikoma 1 procento nuolaida, jei jis sudengiamas per 14 dienų. Arnas gali šią informaciją peržiūrėti puslapyje **Kliento operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra  | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10050  | Sąskaita faktūra          | 6/28/2020 | 10050    | 1,000.00                             |                                       | 1,000.00 | USD      |
| CCRN-10050 | Kredito sąskaita      | 6/28/2020 | CR-10050 |                                      | 100.00                                | -100.00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>Kredito pažymos sudengimas naudojant SF
Puslapyje **Kliento operacijos** Arnas atidaro puslapį **Sudengti operacijas**. Naudodamas puslapį **Sudengti operacijas** Arnis gali sudengti SF ir kredito pažymą. Vykdydamas sudengimo procesą Arnis peržiūri mokėjimo nuolaidos datas ir sumas. Arnis pažymi du dokumentus ir spusteli **Registruoti**, kad sudengtų operacijas. Kredito pažymoje taikoma –1,00 nuolaida, nes „Fabrikam“ leidžia nuolaidas kredito pažymose.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas    | Paskyra | Data      | Terminas  | PVM sąskaita faktūra  | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Pasirinkta | Normalus            | LFSF-10050  | 4035    | 6/28/2020 | 7/28/2020 | 10050    | 1,000.00                       | USD      | 990.00           |
| Pasirinkta | Normalus            | CCRN-10050 | 4035    | 6/28/2020 | 7/28/2020 | CR-10050 | -100.00                        | USD      | –99,00           |

Nuolaidos informacija rodoma puslapio **Sudengti operacijas** apačioje.

- **Mokėjimo nuolaidos data**: 2020-12-7 
- **Mokėjimo nuolaidos suma**: -1,00     
- **Naudokite mokėjimo nuolaidą**: įprasta    
- **Pritaikyta mokėjimo nuolaida**: 0,00      
- **Taikytinos mokėjimo nuolaidos suma**: -1,00     

Bus sudengiama 100,00 suma, įskaitant 99,00 mokėjimą ir 1,00 nuolaidą.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
