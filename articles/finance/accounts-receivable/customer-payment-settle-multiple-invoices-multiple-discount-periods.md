---
title: Naudokite vieną mokėjimą, kad sudarytumėte sąskaitas, kuriose yra keli skirtingi nuolaidų laikotarpiai
description: Šiame straipsnyje parodoma, kaip sumokamos kelios SF, kai kiekvienai SF gali būti pritaikyta mokėjimo nuolaida. Šio straipsnio scenarijais pabrėžiama, kaip taikomos mokėjimo nuolaidos skiriasi pagal tai, kada atliekamas mokėjimas.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bf321a5b0511295f2500f10cdffa9ff6f043bff
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780270"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Naudokite vieną mokėjimą, kad sudarytumėte sąskaitas, kuriose yra keli skirtingi nuolaidų laikotarpiai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje parodoma, kaip sumokamos kelios SF, kai kiekvienai SF gali būti pritaikyta mokėjimo nuolaida. Šio straipsnio scenarijais pabrėžiama, kaip taikomos mokėjimo nuolaidos skiriasi pagal tai, kada atliekamas mokėjimas.

Fabrikam parduoda prekes 4032 klientui. Fabrikam siūlo 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="invoices"></a>SF
4032 klientas turi tris sąskaitas faktūras, kurių bendra suma 3000,00:

-   Sąskaita faktūra LFSF-10040, kurios suma 1000,00, buvo įvesta gegužės 15 d. Šiai sąskaitai faktūrai galima pritaikyti 1 procento mokėjimo nuolaidą, jei ji sumokama per 14 dienų.
-   Sąskaita faktūra LFSF-10041, kurios suma 1000,00, buvo įvesta birželio 25 d. Šiai sąskaitai faktūrai galima pritaikyti 1 procento mokėjimo nuolaidą, jei ji sumokama per 14 dienų.
-   Sąskaita faktūra LFSF-10042, kurios suma 1000,00, buvo įvesta birželio 25 d. Šiai sąskaitai faktūrai galima pritaikyti 2 procentų mokėjimo nuolaidą, jei ji apmokama per penkias dienas ir 1 procento nuolaidą, jei ji apmokama per 14 dienų.

## <a name="settle-all-invoices-on-june-29"></a>Sudengti visas sąskaitas faktūras birželio 29 d.
Jei Arnas sukuria mokėjimų žurnalą, kad visiškai sudengtų šias sąskaitas faktūras birželio 29 d., mokėjimas yra 2970,00. Visa nuolaidos suma 30,00. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes:

-   Sąskaitos faktūros LFSF-10040 mokėjimas 1000,00. Mokėjimo nuolaida nepritaikyta.
-   Sąskaitos faktūros LFSF-10041 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida.
-   Sąskaitos faktūros LFSF-10042 mokėjimas 980,00. Pritaikyta 2 procentų, arba 20,00, mokėjimo nuolaida.

| Žymėti | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data   | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|------|----------|-----------|---------|-----------|-----------|---------|---------------------|---------------------|----------|------------------|
| Pasirinkta     | Normalus      | LFSF-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00  |                    | USD      | 1,000.00         |
| Pasirinkta     | Normalus      | LFSF-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |                    | USD      | 990.00           |
| Pasirinkta ir paryškinta | Normalus      | LFSF-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00    |              | USD      | 980.00           |

Užregistravus mokėjimą kliento balansas yra 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Sudengti visas sąskaitas faktūras liepos 1 d.
Jei Arnas sukuria mokėjimų žurnalą, kad visiškai sudengtų šias sąskaitas faktūras liepos 1 d., mokėjimas yra 2980,00. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes:

-   Sąskaitos faktūros LFSF-10040 mokėjimas 1000,00. Mokėjimo nuolaida nepritaikyta.
-   Sąskaitos faktūros LFSF-10041 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida.
-   Sąskaitos faktūros LFSF-10042 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida. Nors liepos 1 d. yra po laikotarpio, kai galima pritaikyti 2 procentų nuolaidą, šiuo laikotarpiu vis dar galima pritaikyti 1 procento nuolaidą.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|----------|---------|-----------|---------|-----------|-----------|---------|--------------------|------------------|----------|------------------|
| Pasirinkta         | Normalus            | LFSF-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00         |                | USD      | 1,000.00         |
| Pasirinkta                 | Normalus            | LFSF-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00  |               | USD      | 990.00           |
| Pasirinkta ir paryškinta | Normalus            | LFSF-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00  |             | USD      | 990.00           |

## <a name="partial-settlement-on-june-29"></a>Dalinis sudengimas birželio 29 d.
4032 klientas gali sumokėti dalinę sumą, pvz., pusę kiekvienos sąskaitos faktūros. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes. Kiekvienoje eilutėje Arnas įveda sudengtiną sumą pagal kliento pateiktas instrukcijas. Kai Arnas pasirenka eilutę, Arnas mato tos eilutės nuolaidos sumą ir pritaikytos mokėjimo nuolaidos sumą. Kadangi klientas moka už pusę sąskaitos faktūros, Arnas mato, kad LFSF-10042 lauko **Mokėjimo nuolaidos suma** vertė yra **20,00**, bet vertė lauke **Pritaikyta mokėjimo nuolaida** yra **10,00**. Mokėjimo suma yra 1485,00.

| Žymėti   | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|-------------|-------------------|-----------|---------|-----------|-----------|---------|-----------|------------------|----------|------------------|
| Pasirinkta   | Normalus       | LFSF-10040 | 4032    | 5/15/2020 | 6/15/2020 | 10040   | 1,000.00        |               | USD      | 500.00           |
| Pasirinkta                 | Normalus            | LFSF-10041 | 4032    | 6/25/2020 | 7/25/2020 | 10041   | 1,000.00     |     | USD      | 495,00           |
| Pasirinkta ir paryškinta | Normalus            | LFSF-10042 | 4032    | 6/25/2020 | 7/25/2020 | 10042   | 1,000.00     |         | USD      | 490,00           |

Arnas taip pat gali rankiniu būdu įvesti mokėjimo sumą 1 485,00 prieš atidarydamas puslapį **Sudengti operacijas**. Jei Arnas rankiniu būdu įveda mokėjimo sumą ir tada pažymi visas tris operacijas, bet nepakoreguoja kiekvienos operacijos lauko **Sudengtina suma** vertės, uždarius puslapį pateikiamas tolesnis pranešimas:

> Pažymėtų operacijų bendra suma skiriasi nuo žurnalo sumos. Ar pakeisti žurnalo sumą?

Jei Arnas nori, kad mokėjimo suma būtų tik 1485,00, Arnas spustelėja **Ne** ir tada registruoja žurnalą. Operacijos sudengiamos tokiu būdu:

1.  Sąskaitos faktūros LFSF-10040 suma 1000,00 yra visiškai sudengiama, nes ji buvo įvesta gegužės 15 d. ir yra seniausia sąskaita faktūra. Mokėjimo nuolaida nepritaikyta. Likusi mokėjimo operacijos suma yra 485,00.
2.  Sąskaita faktūra LFSF-10041 visiškai nesudengiama. Sąskaitos faktūros LFSF-10041 ir LFSF-10042 buvo įvestos tą pačią dieną. Tačiau sąskaitai faktūrai LFSF-10041 galima pritaikyti 1 procento nuolaidą, o sąskaitai faktūrai LFSF-10042 – 2 procentų nuolaidą. Kadangi didesnę nuolaidą galima pritaikyti sąskaitai faktūrai LFSF-10042, likusi 485,00 suma sudengia sąskaitą faktūrą LFSF-10042.
3.  Sąskaita faktūra LFSF-10042 sudengiama likusiais 485,00. „Fabrikam“ siūlo dalines nuolaidas. Šiuo atveju nuolaida yra 9,90 (= 485,00 ÷ 0,98 x 0,02). Suma (485,00) yra padalinama iš 0,98, nes pritaikyta 2 procentų nuolaida (todėl klientas apmoka 98 proc. sąskaitos faktūros). Tada rezultatas padauginamas iš nuolaidos procento, arba 2 procentų. 485,00 mokėjimas plius 9,90 nuolaida lygu 494,90. Pradinės sąskaitos faktūros suma buvo 1000,00. Todėl operacijos balansas yra 505,10 (= 1000,00 – 494,90).

Arnas peržiūri šią operaciją puslapyje **Kliento operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10040  | Sąskaita faktūra          | 5/15/2020 | 10040   | 1,000.00                             |                                       | 0,00     | USD      |
| LFSF-10041  | Sąskaita faktūra          | 6/25/2020 | 10041   | 1,000.00                             |                                       | 1,000.00 | USD      |
| LFSF-10042  | Sąskaita faktūra          | 6/25/2020 | 10042   | 1,000.00                             |                                       | 505,10   | USD      |
| ARP-10040  | Mokėjimas          | 6/29/2020 |         |                                      | 1485,00                              | 0,00     | USD      |
| NUOL-10040 | Mokėjimo nuolaida    | 6/29/2020 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
