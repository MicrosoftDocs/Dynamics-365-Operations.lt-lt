---
title: "Sudengiamas dalinis kliento mokėjimas ir visas paskutinis mokėjimas prieš nuolaidos datą"
description: "Šiame straipsnyje pateikiami scenarijai, kuriais parodoma, kaip įrašyti dalinius kliento mokėjimus ir mokėjimo nuolaidos laikotarpiu taikyti mokėjimo nuolaidą."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 655cc2b67eabac99460c00a2ddab059335fd74f8
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Sudengiamas dalinis kliento mokėjimas ir visas paskutinis mokėjimas prieš nuolaidos datą

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami scenarijai, kuriais parodoma, kaip įrašyti dalinius kliento mokėjimus ir mokėjimo nuolaidos laikotarpiu taikyti mokėjimo nuolaidą.

Fabrikam parduoda prekes 4028 klientui. Fabrikam siūlo 1 procento mokėjimo nuolaidą, jei sąskaita faktūra apmokama per 14 dienų. SF turi būti apmokėtos per 30 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Sudengimo parametrus rasite puslapyje **Gautinų sumų parametrai**.

## <a name="customer-invoice"></a>Kliento SF
Birželio 25 d. Eglė 4028 klientui įveda ir užregistruoja sąskaitą faktūrą 1 000,00 sumai. Arnas gali šią operaciją peržiūrėti puslapyje **Kliento operacijos**.

| Kvitas   | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10010 | PVM sąskaita faktūra          | 2015-06-25 | 10010   | 1000,00                             |                                       | 1000,00 | USD      |

Puslapyje **Klientas** arba **Kliento operacijos** Arnie gali atidaryti puslapį **Sudengti operacijas** norėdamas peržiūrėti sąskaitai faktūrai galimas mokėjimo nuolaidų datas ir sumas. Terminas yra liepos 25 d., o 10.00 mokėjimo nuolaida galima, jei sąskaita faktūra apmokama iki liepos 9 d.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 990,00           |

Nuolaidos informacija rodoma pažymėtos sąskaitos faktūros puslapio **Sudengti operacijas** apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 10,00     |

Arnie spusteli skirtuką **Mokėjimo nuolaida** ir peržiūri nuolaidos sumą.

| Mokėjimo nuolaidos data | Mokėjimo nuolaidos suma | Suma operacijos valiuta |
|--------------------|----------------------|--------------------------------|
| 2015-07-09           | 10,00                | 990,00                         |
| 2015-07-25          | 0,00                 | 1000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Dalinis mokėjimas naudojant puslapį Įvesti kliento mokėjimus
4028 klientas siunčia 500,00 mokėjimą liepos 1 d. Norėdama įvesti šį mokėjimą, Eglė nespusteli **Eilutės**. Vietoj to, jis įrašo mokėjimą sukūręs naują mokėjimų žurnalą ir tada atidaro puslapį **Įvesti kliento mokėjimus**. Jis įveda mokėjimo informaciją ir pažymi sąskaitą faktūrą, kurią įvedė. Kai Arnie įveda **500,00** kaip sumą, jis taip pat įveda **500,00** tinklelio lauke **Mokėtina suma**. Kadangi „Fabrikam“ leidžia mokėjimo nuolaidą ir daliniams mokėjimams, jis mato, kad 5,05 dalinio mokėjimo nuolaida taip pat bus taikoma. Ši nuolaida apskaičiuojama taip: 500,00 ÷ 0,99 x 0,01 = 5,05. (Šiame skaičiavime 500,00 padalinti iš 0,99, nes taikoma 1 % nuolaida. Todėl klientas apmoka 99 procentus sąskaitos faktūros. Tada rezultatas padauginamas iš nuolaidos procento, tai yra, iš 1 procento arba 0,01. Jei klientas gauna visą 10,00 nuolaidą, suma, kuri turi būti sudengta, bus 990,00.) Nuolaidos informacija rodoma tinklelyje, puslapio **Įvesti kliento mokėjimus** apačioje.

| Taikytinos mokėjimo nuolaidos suma | Pritaikyta mokėjimo nuolaida | Mokėtina suma |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Dalinis mokėjimas naudojant žurnalo eilutes
Vietoj to, kad atidarytų puslapį **Įvesti kliento mokėjimus** mokėjimo žurnale, Arnie gali spustelėti **Eilutės** ir įvesti mokėjimą. Rodomas mokėjimo žurnalas, kur Eglė gali įvesti eilutę 4028 klientui. Tada Arnas atidaro puslapį **Sudengti operacijas**, kad galėtų pažymėti sudengtiną SF. Arnie pažymi sąskaitą faktūrą ir pakeičia lauko **Sudengtina suma** vertę į **500,00**. Vėlgi, jis mato, kad lauko **Mokėjimo nuolaidos suma** vertė yra **10,00** visai sąskaitai faktūrai, o lauko **Taikytinos mokėjimo nuolaidos suma** vertė yra **5,05**. Todėl šios sąskaitos faktūros suma, kurią Arnie sudengia, yra 505,05.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 500,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 5,05      |

Jei klientas nori sudengti lygiai pusę sąskaitos faktūros, klientas pateikia 495,00 mokėjimą. Šiuo atveju Arnie įveda **495,00** lauke **Sudengtina suma**. Mokėjimo nuolaida 5,00 bus taip pat taikoma, todėl bendroji sudengtina suma yra 500,00.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 495,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 0,00      |
| Taikytinos mokėjimo nuolaidos suma | 5,00      |

Arnie uždaro puslapį **Sudengti operacijas**. Žurnale sukuriama mokėjimo eilutė 495,00 sumai ir tada Arnie užregistruoja žurnalą. Tada jis gali peržiūrėti kliento operacijas puslapyje **Kliento operacijos**. Šiame puslapyje Arnie mato, kad sąskaitos faktūros balansas yra 500,00. Jis taip pat mato 495,00 mokėjimą ir 5,00 nuolaidą.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10010  | PVM sąskaita faktūra          | 2015-06-25 | 10010   | 1000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Mokėjimas         | 2015-07-01  |         |                                      | 495,00                                | 0,00    | USD      |
| NUOL-10010 |  Mokėjimo nuolaida   | 2015-07-01  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Likusios sumos mokėjimas
Klientas 4028 sumoka likusią 495,00 sumą liepos 8 d., kuri patenka į mokėjimo nuolaidos laikotarpį. Arnie sukuria mokėjimo žurnalą liepos 8 d. ir pažymi operaciją sudengti. Jis mato, kad suma, kurią reikia sudengti, yra 495,00. Lauko **Įvertinta mokėjimo nuolaida** vertė yra **5,00**, nes anksčiau buvo pritaikyta 5,00 nuolaida.

|                         |        |
|-------------------------|--------|
| Pažymėta bendroji suma            | 495,00 |
| Įvertinta mokėjimo nuolaida | 5,00   |

Informacija apie pažymėtą operaciją rodoma puslapio **Sudengti atviras operacijas** tinklelyje.

| Žymėti     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Suma operacijos valiuta | Valiuta | Sudengtina suma |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Pasirinkta | Įprastas            | LFSF-10010 | 4028    | 2015-06-25 | 2015-07-25 | 10010   | 1000,00                       | USD      | 495,00           |

Nuolaidos informacija rodoma puslapio **Sudengti atidarytas operacijas**apačioje.

|                              |           |
|------------------------------|-----------|
| Mokėjimo nuolaidos data           | 2015-07-09 |
| Mokėjimo nuolaidos suma         | 10,00     |
| Naudokite mokėjimo nuolaidą            | Įprastas    |
| Pritaikyta mokėjimo nuolaida          | 5,00      |
| Taikytinos mokėjimo nuolaidos suma | 5,00      |

Arnie užregistruoja šį mokėjimo žurnalą ir peržiūri kliento operacijas puslapyje **Kliento operacijos**. Dabar sąskaitos faktūros balansas yra 0,00 ir Arnie mato du mokėjimus ir dvi mokėjimo nuolaidas.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| LFSF-10010  | PVM sąskaita faktūra          | 2015-06-25 | 10010   | 1000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Mokėjimas          | 2015-07-01  |         |                                      | 495,00                                | 0,00    | USD      |
| NUOL-10010 | Mokėjimo nuolaida    | 2015-07-01  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Mokėjimas          | 2015-07-08  |         |                                      | 495,00                                | 0,00    | USD      |
| NUOL-10011 | Mokėjimo nuolaida    | 2015-07-08  |         |                                      | 5,00                                  | 0,00    | USD      |






