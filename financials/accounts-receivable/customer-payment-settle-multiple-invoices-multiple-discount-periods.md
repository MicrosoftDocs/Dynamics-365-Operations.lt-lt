---
title: "Naudoti kliento mokėjimą keletą sąskaitų, kurie apima kelis nuolaida laikotarpiai"
description: "Šiame straipsnyje parodoma, kaip sumokamos kelios SF, kai kiekvienai SF gali būti pritaikyta mokėjimo nuolaida. Šio straipsnio scenarijais pabrėžiama, kaip taikomos mokėjimo nuolaidos skiriasi pagal tai, kada atliekamas mokėjimas."
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
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 6fd78a587d70ec371861084ac9f76b439c821a8f
ms.lasthandoff: 03/31/2017


---

# <a name="use-a-customer-payment-to-settle-multiple-invoices-that-span-multiple-discount-periods"></a>Naudoti kliento mokėjimą keletą sąskaitų, kurie apima kelis nuolaida laikotarpiai

Šiame straipsnyje parodoma, kaip sumokamos kelios SF, kai kiekvienai SF gali būti pritaikyta mokėjimo nuolaida. Šio straipsnio scenarijais pabrėžiama, kaip taikomos mokėjimo nuolaidos skiriasi pagal tai, kada atliekamas mokėjimas.

Fabrikam parduoda prekes klientui 4032. Fabrikam siūlo 1 proc nuolaida, jei sąskaita yra apmokėta per 14 dienų. „Fabrikam“ taip pat siūlo dalinių mokėjimų mokėjimo nuolaidas. Settement parametrai yra ant to **sudaro gautinų sumų parametrai** puslapis.

## <a name="invoices"></a>SF
4032 klientas turi tris sąskaitas faktūras, kurių bendra suma 3000,00:

-   SF FTI-10040 1000,00, buvo įrašytas gegužės 15. Šioje sąskaitoje-faktūroje turi teisę gauti 1 proc. nuolaida, jei ji mokama per 14 dienų.
-   SF FTI-10041 1000,00, buvo įvestas birželio 25. Šioje sąskaitoje-faktūroje turi teisę gauti 1 proc. nuolaida, jei ji mokama per 14 dienų.
-   SF FTI-10042 1000,00, buvo įvestas birželio 25. Šioje sąskaitoje-faktūroje turi teisę gauti 2 procentų nuolaida, jei ji mokama penkias dienas ir 1 proc nuolaida, jei ji mokama per 14 dienų.

## <a name="settle-all-invoices-on-june-29"></a>Sudengti visas sąskaitas faktūras birželio 29 d.
Jei Arnas sukuria mokėjimų žurnalą, kad visiškai sudengtų šias sąskaitas faktūras birželio 29 d., mokėjimas yra 2970,00. Visa nuolaidos suma 30,00. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes:

-   Sąskaitos faktūros LFSF-10040 mokėjimas 1000,00. Mokėjimo nuolaida nepritaikyta.
-   Sąskaitos faktūros LFSF-10041 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida.
-   Sąskaitos faktūros LFSF-10042 mokėjimas 980,00. Pritaikyta 2 procentų, arba 20,00, mokėjimo nuolaida.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Pasirinkta                 | Įprastas            | LFSF-10040 | 4032    | 2015-05-15 | 2015-06-15 | 10040   | 1000,00                             |                                       | USD      | 1000,00         |
| Pasirinkta                 | Įprastas            | LFSF-10041 | 4032    | 2015-06-25 | 2015-07-25 | 10041   | 1000,00                             |                                       | USD      | 990,00           |
| Pasirinkta ir paryškinta | Įprastas            | LFSF-10042 | 4032    | 2015-06-25 | 2015-07-25 | 10042   | 1000,00                             |                                       | USD      | 980,00           |

Užregistravus mokėjimą kliento balansas yra 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Sudengti visas sąskaitas faktūras liepos 1 d.
Jei Arnas sukuria mokėjimų žurnalą, kad visiškai sudengtų šias sąskaitas faktūras liepos 1 d., mokėjimas yra 2980,00. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes:

-   Sąskaitos faktūros LFSF-10040 mokėjimas 1000,00. Mokėjimo nuolaida nepritaikyta.
-   Sąskaitos faktūros LFSF-10041 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida.
-   Sąskaitos faktūros LFSF-10042 mokėjimas 990,00. Pritaikyta 1 procento, arba 10,00, mokėjimo nuolaida. Nors liepos 1 d. yra po laikotarpio, kai galima pritaikyti 2 procentų nuolaidą, šiuo laikotarpiu vis dar galima pritaikyti 1 procento nuolaidą.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Pasirinkta                 | Įprastas            | LFSF-10040 | 4032    | 2015-05-15 | 2015-06-15 | 10040   | 1000,00                             |                                       | USD      | 1000,00         |
| Pasirinkta                 | Įprastas            | LFSF-10041 | 4032    | 2015-06-25 | 2015-07-25 | 10041   | 1000,00                             |                                       | USD      | 990,00           |
| Pasirinkta ir paryškinta | Įprastas            | LFSF-10042 | 4032    | 2015-06-25 | 2015-07-25 | 10042   | 1000,00                             |                                       | USD      | 990,00           |

## <a name="partial-settlement-on-june-29"></a>Dalinis sudengimas birželio 29 d.
4032 klientas gali sumokėti dalinę sumą, pvz., pusę kiekvienos sąskaitos faktūros. Arnas sukuria 4032 kliento mokėjimą, tada atsidaro puslapį **Sudengti operacijas**. Puslapyje **Sudengti operacijas** Arnas pažymi visas tris sudengtinas sąskaitos faktūros eilutes. Kiekvienoje eilutėje jis įveda sudengtiną sumą pagal kliento pateiktas instrukcijas. Kai Arnas pasirenka eilutę, jis mato tos eilutės nuolaidos sumą ir pritaikytos mokėjimo nuolaidos sumą. Kadangi klientas moka už pusę sąskaitos faktūros, Arnas mato, kad LFSF-10042 lauko **Mokėjimo nuolaidos suma** vertė yra **20,00**, bet vertė lauke **Pritaikyta mokėjimo nuolaida** yra **10,00**. Mokėjimo suma yra 1485,00.

| Žymėti                     | Naudokite mokėjimo nuolaidą | Kvitas   | Paskyra | Data      | Terminas  | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Valiuta | Sudengtina suma |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Pasirinkta                 | Įprastas            | LFSF-10040 | 4032    | 2015-05-15 | 2015-06-15 | 10040   | 1000,00                             |                                       | USD      | 500,00           |
| Pasirinkta                 | Įprastas            | LFSF-10041 | 4032    | 2015-06-25 | 2015-07-25 | 10041   | 1000,00                             |                                       | USD      | 495,00           |
| Pasirinkta ir paryškinta | Įprastas            | LFSF-10042 | 4032    | 2015-06-25 | 2015-07-25 | 10042   | 1000,00                             |                                       | USD      | 490,00           |

Jūratė galite patys įvesti mokėjimo suma 1,485.00, kol jis atidaro su **atsiskaitymams** puslapis. Jei Arnie rankiniu būdu patenka mokėjimo sumą ir tada pažymi visas tris operacijas, bet jis nėra nustatyti vertę, **sudengtina suma** lauko kiekvienam sandoriui, jis gauna tokį pranešimą, kai jis baigia puslapio:

> Pažymėtų operacijų bendra suma skiriasi nuo  žurnalo sumos. Ar pakeisti žurnalo sumą?

Jei Arnas nori, kad mokėjimo suma būtų tik 1485,00, jis spustelėja **Ne** ir tada registruoja žurnalą. Operacijos sudengiamos tokiu būdu:

1.  Sąskaitos faktūros LFSF-10040 suma 1000,00 yra visiškai sudengiama, nes ji buvo įvesta gegužės 15 d. ir yra seniausia sąskaita faktūra. Mokėjimo nuolaida nepritaikyta. Likusi mokėjimo operacijos suma yra 485,00.
2.  Sąskaita faktūra LFSF-10041 visiškai nesudengiama. Sąskaitos faktūros LFSF-10041 ir LFSF-10042 buvo įvestos tą pačią dieną. Tačiau sąskaitai faktūrai LFSF-10041 galima pritaikyti 1 procento nuolaidą, o sąskaitai faktūrai LFSF-10042 – 2 procentų nuolaidą. Kadangi didesnę nuolaidą galima pritaikyti sąskaitai faktūrai LFSF-10042, likusi 485,00 suma sudengia sąskaitą faktūrą LFSF-10042.
3.  Sąskaita faktūra LFSF-10042 sudengiama likusiais 485,00. „Fabrikam“ siūlo dalines nuolaidas. Šiuo atveju nuolaida yra 9,90 (= 485,00 ÷ 0,98 x 0,02). Suma (485,00) yra padalinama iš 0,98, nes pritaikyta 2 procentų nuolaida (todėl klientas apmoka 98 proc. sąskaitos faktūros). Tada rezultatas padauginamas iš nuolaidos procento, arba 2 procentų. 485,00 mokėjimas plius 9,90 nuolaida lygu 494,90. Pradinės sąskaitos faktūros suma buvo 1000,00. Todėl operacijos balansas yra 505,10 (= 1000,00 – 494,90).

Arnas peržiūri šią operaciją puslapyje **Kliento operacijos**.

| Kvitas    | Operacijos tipas | Data      | PVM sąskaita faktūra | Operacijos valiutos debeto suma | Operacijos valiutos kredito suma | Likutis  | Valiuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| LFSF-10040  | PVM sąskaita faktūra          | 2015-05-15 | 10040   | 1000,00                             |                                       | 0,00     | USD      |
| LFSF-10041  | PVM sąskaita faktūra          | 2015-06-25 | 10041   | 1000,00                             |                                       | 1000,00 | USD      |
| LFSF-10042  | PVM sąskaita faktūra          | 2015-06-25 | 10042   | 1000,00                             |                                       | 505,10   | USD      |
| ARP-10040  | Mokėjimas          | 2015-06-29 |         |                                      | 1485,00                              | 0,00     | USD      |
| NUOL-10040 | Mokėjimo nuolaida    | 2015-06-29 |         |                                      | 9,90                                  | 0,00     | USD      |




