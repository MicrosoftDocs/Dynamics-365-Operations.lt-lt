---
title: "Sudengimo peržiūra"
description: "Šiame straipsnyje pateikta bendra informacija apie sudengimo procesą. Jame aprašomi galimų sudengti operacijų tipai, tai, kada ir kaip operacijas galima sudengti bei sudengimo proceso rezultatai."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4d45db11c1d5bf7a58f9117fca75679ddfababf5
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="settlement-overview"></a>Sudengimo peržiūra

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta bendra informacija apie sudengimo procesą. Jame aprašomi galimų sudengti operacijų tipai, tai, kada ir kaip operacijas galima sudengti bei sudengimo proceso rezultatai.

Atliekant sudengimą vieno dokumento operacijos sudengiamos su kito dokumento operacijomis, kad būtų padidintas arba sumažintas kiekvieno dokumento balansas. Pvz., mokėjimas gali būti taikomas sąskaitai faktūrai. Įvairių tipų operacijos kaskart gali būti sudengtos skirtingais būdais. Atliekant sudengimą gali būti sugeneruota naujų operacijų.

## <a name="what-transactions-can-be-settled"></a>Kokioms operacijoms galima taikyti sudengimą
Mokėtinų ir gautinų sumų sudengimas gali būti atliekamas su bet kurio tipo operacijomis, kurios turi įtakos tiekėjo arba kliento balansui, pvz., SF, mokėjimai, kredito pažymos ir mokesčių operacijos. Bet kurio tipo operaciją galima sudengti pagal bet kurį kitą operacijos tipą. Pavyzdžiui, galite sudengti mokėjimą su SF, kredito pažymą su SF, SF su SF ir mokėjimą su mokėjimu. Galima sudengti mokėjimus su operacijomis, atliekamomis to paties arba kito juridinio subjekto. Organizacijose, kuriose naudojamas centralizuoto mokėjimo modelis, [centralizuoti mokėjimai](set-up-centralized-payments.md) gali padėti racionalizuoti mokėjimo procesą.

## <a name="when-to-settle-transactions"></a>Kada taikomas operacijų sudengimas
Operacijas galima sudengti mokėjimų įvedimo metu. Pavyzdžiui, atliekant mokėjimą tiekėjui, paprastai pasirenkama apmokėti SF. Pasirinkdami sąskaitas faktūras, jas pažymite sudengti pagal mokėjimą. Kai darbuotojai, atsakingi už Gaunamų sumų mokėjimus, užregistruoja kliento mokėjimą, jie gali pažymėti reikiamas sudengti sąskaitas faktūras remiantis kliento mokėjimo informacija. Puslapyje **Sudengti operacijas** galima pažymėti reikiamas sudengti operacijas. Šio puslapio negalima atidaryti, jei atitinkama SF arba mokėjimas nėra užregistruoti. Užregistravus operaciją užregistruojamas ir sudengimas. Operacijos taip pat gali būti sudengtos jas užregistravus. Galite įvesti ir registruoti kliento mokėjimą neatlikdami sudengimo su jokiomis SF. Tačiau gali prireikti pirmiausia patikrinti, ar mokėjimas sudengtas su tinkama SF. Puslapį **Sudengti operacijas** galima atidaryti iš puslapio **Visi klientai** arba **Visi tiekėjai** arba iš bet kurio kliento ar teikėjo puslapio **Operacijos**. Be to, galite rezervuoti užregistruotus išankstinius mokėjimus pagal tam tikrą SF sudengimui su pirkimo ar pardavimo užsakymais atlikti. Tokiu atveju, mokėjimas turės atvirą balansą, tačiau negalės būti sudengtas pagal kitą sąskaitą faktūrą. Mokėjimas bus automatiškai sudengtas su ta sąskaita faktūra, kuri sukuriama pagal pirkimo arba pardavimo užsakymą.

## <a name="how-to-settle-transactions"></a>Kaip taikomas operacijų sudengimas
Operacijas galima sudengti rankiniu būdu, automatiškai arba derinant bu būdus. Sudengimo būdo pasirinkimas priklauso nuo verslo proceso, kuris gali būti vykdomas nustatant sudengimo mokėtinų sumų parametrus ir gautinų sumų parametrus. Galite kurti tiekėjo mokėjimus ir kliento tiesioginio debeto mokėjimus naudodami mokėjimo pasiūlymą, kuris naudojamas apmokėtinoms SF pasirinkti. Mokėjimo pasiūlymas inicijuojamas rankiniu būdu, tada „Microsoft Dynamics 365 for Finance and Operations“ automatiškai pažymi pasirinktas sąskaitas faktūras sudengimui atlikti, kai mokėjimai bus sukurti. Jei mokėjimai sukurti rankiniu būdu, galite naudoti puslapį **Sudengti operacijas** norėdami pasirinkti SF sudengimui atlikti. SF galite pasirinkti rankiniu būdu arba galite naudoti parinktį **Žymėti pagal prioritetą**, kad sudengtinos SF būtų pažymėtos automatiškai. Parinktis **Žymėti pagal prioritetą** galima gautinoms sumoms. Norėdami įgalinti šią parinktį naudokite puslapį **Sudengimo prioritetas** gautinų sumų parametrų dalyje. Jei mokėjimą tvarkantis darbuotojas įveda mokėjimą, bet nesudengia jo prieš užregistruodamas, mokėjimą galima sudengti automatiškai. Gautinų sumų ir mokėtinų sumų parametrų dalyje galite įjungti automatinį sudengimą. Kai naudojate automatinį sudengimą, galite taikyti iš anksto nustatytą sudengimo tvarką arba galite patys nustatyti sudengimo prioritetų tvarką Gautinų sumų parametrų dalyje. Ši funkcija galima tik gautinoms sumoms.

## <a name="results-of-settlement"></a>Sudengimo rezultatai
Atlikus operacijų sudengiamą kiekvienos operacijos nepamokėtas likutis atitinkamai padidėja arba sumažėja. Paprastai sudengus SF ir mokėjimą, kiekvienos operacijos būsena ir balansas atnaujinami pagal šias taisykles:

-   Jei mokėjimo suma yra didesnė už SF sumą, SF balansas yra sumažinamas iki 0,00 ir SF uždaroma. Mokėjimas lieka atviras, o balansas reiškia sumą, kuria mokėjimo suma viršija SF sumą.
-   Jei mokėjimo suma yra mažesnė už SF sumą, mokėjimo balansas sumažėja iki 0,00 ir mokėjimas uždaromas. SF lieka atvira, o balansas yra suma, kurios trūksta, kad mokėjimo suma būtų lygi SF sumai.
-   Jei mokėjimo suma yra lygi SF sumai, mokėjimas ir SF uždaromi, jų balansas yra 0,00.

Jei [mokėjimas yra mažesnis už SF sumą](../accounts-payable/vendor-payments-partial-amount.md) dėl mokėjimo nuolaidos, nurašymo arba neprimokėjimo, SF ir mokėjimas vis tiek gali būti uždaryti – tai priklauso nuo sudengimo parametrų, nustatytų mokėtinų sumų ir gautinų sumų parametrų dalyje. Be to, sudengimas gali generuoti operacijas. Pvz., SF ir mokėjimo sudengimas gali sąlygoti mokėjimo nuolaidą, gautą pelną arba patirtą nuostolį, PVM koregavimus, nurašymai arba centų skirtumus.




