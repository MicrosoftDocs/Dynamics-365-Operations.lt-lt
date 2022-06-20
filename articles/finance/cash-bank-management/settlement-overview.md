---
title: Sudengimo peržiūra
description: Šiame straipsnyje pateikta bendra informacija apie sudengimo procesą. Joje aprašoma, kurie operacijų tipai gali būti sudengti, bei jų sudengimo laikas ir procesas. Taip pat aprašomi sudengimo proceso rezultatai.
author: panolte
ms.date: 07/30/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14551"
- intro-internal
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a495a71a95032a0022cbab2783f356db48ee349d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887954"
---
# <a name="settlement-overview"></a>Sudengimų apžvalga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Šiame straipsnyje pateikta bendra informacija apie sudengimo procesą. Joje aprašoma, kurie operacijų tipai gali būti sudengti, bei jų sudengimo laikas ir procesas. Taip pat aprašomi sudengimo proceso rezultatai.

Atliekant sudengimą vieno dokumento operacijos sudengiamos su kito dokumento operacijomis, kad būtų padidintas arba sumažintas kiekvieno dokumento balansas. Pvz., mokėjimas gali būti taikomas sąskaitai faktūrai. Įvairių tipų operacijos kaskart gali būti sudengtos skirtingais būdais. Atliekant sudengimo procesą gali būti sugeneruota naujų operacijų.

## <a name="what-transactions-can-be-settled"></a>Kokioms operacijoms galima taikyti sudengimą

Mokėtinų ir gautinų sumų sudengimas gali būti atliekamas su bet kurio tipo operacijomis, kurios turi įtakos tiekėjo arba kliento balansui. Šie operacijų tipai gali apimti SF, mokėjimus, kredito pažymas ir mokesčius. Bet kurio tipo operaciją galima sudengti pagal bet kurį kitą operacijos tipą. Pavyzdžiui, galite sudengti mokėjimą pagal SF, kredito pažymą pagal SF, SF pagal kitą SF ir mokėjimą pagal kitą mokėjimą.

Galima sudengti mokėjimus su operacijomis, atliekamomis to paties arba kito juridinio subjekto. Organizacijose, kuriose naudojamas centralizuoto mokėjimo modelis, [centralizuoti mokėjimai](set-up-centralized-payments.md) gali padėti racionalizuoti mokėjimo procesą.

## <a name="when-to-settle-transactions"></a>Kada taikomas operacijų sudengimas

Operacijos gali būti sudengiamos, kai įvedami mokėjimai. Pavyzdžiui, atliekant mokėjimą tiekėjui, paprastai pasirenkama, kurias SF apmokėti. Pasirinkdami sąskaitas faktūras, jas pažymite sudengti pagal mokėjimą. Kai darbuotojai, atsakingi už gaunamų sumų mokėjimus, užregistruoja kliento mokėjimus, jie gali pažymėti reikiamas sudengti sąskaitas faktūras remiantis kliento kiekvieno mokėjimo informacija. Puslapyje **Sudengti operacijas** galima pažymėti reikiamas sudengti operacijas. Šį puslapį galima atidaryti, jei atitinkama SF arba mokėjimas nėra užregistruoti. Užregistravus operaciją užregistruojamas ir sudengimas. 

Operacijos taip pat gali būti sudengtos jas užregistravus. Galite įvesti ir registruoti kliento mokėjimą neatlikdami sudengimo su jokiomis SF. Tačiau prieš sudengimo registravimą gali prireikti pirmiausia patikrinti, ar mokėjimas sudengtas su tinkama SF. Puslapį **Sudengti operacijas** galima atidaryti iš puslapio **Visi klientai** arba **Visi tiekėjai** arba iš bet kurio kliento ar teikėjo puslapio **Operacijos**.

Be to, galite rezervuoti užregistruotus išankstinius mokėjimus pagal tam tikrą SF sudengimui su pirkimo ar pardavimo užsakymais atlikti. Tokiu atveju, mokėjimas turės atvirą balansą, tačiau negalės būti sudengtas pagal kitą sąskaitą faktūrą. Mokėjimas bus automatiškai sudengtas su ta sąskaita faktūra, kuri sukuriama pagal pirkimo arba pardavimo užsakymą.

## <a name="how-to-settle-transactions"></a>Kaip taikomas operacijų sudengimas

Operacijas galima sudengti rankiniu būdu, automatiškai arba derinant bu būdus. Sudengimo būdo pasirinkimas priklauso nuo jūsų verslo procesų. Puslapiuose **Mokėtinų sumų parametrai** ir **Gautinų sumų parametrai** galite konfigūruoti sudengimo procesą, kad jis būtų suderintas su tais verslo procesais.

Galite kurti tiekėjo mokėjimus ir kliento tiesioginio debeto mokėjimus naudodami mokėjimo pasiūlymą. Mokėjimo pasiūlymas naudojamas apmokėtinoms SF pasirinkti. Mokėjimo pasiūlymas pradedamas rankiniu būdu, tada sistema automatiškai pažymi pasirinktas SF sudengimui atlikti, kai mokėjimai bus sukurti.

Jei mokėjimai sukurti rankiniu būdu, galite naudoti puslapį **Sudengti operacijas** norėdami pasirinkti SF sudengimui atlikti. SF galite pasirinkti rankiniu būdu arba galite naudoti parinktį **Žymėti pagal prioritetą**, kad sudengtinos SF būtų pažymėtos automatiškai. Parinktis **Žymėti pagal prioritetą** galima gautinoms sumoms. Šią parinktį galima įjungti puslapio **Gautinų sumų parametrai** skirtuke **Sudengimo prioritetas**.

Jei mokėjimą tvarkantis darbuotojas įveda mokėjimą, bet nesudengia jo prieš užregistruodamas, mokėjimą galima sudengti automatiškai. Puslapiuose **Gautinų sumų parametrai** ir **Mokėtinų sumų parametrai** galite įjungti automatinį sudengimą. Automatinis sudengimas sudengia operacijas tik tame pačiame juridiniame subjekte. Jis nesudengia operacijų keliuose juridiniuose subjektuose.

Kai naudojate automatinį sudengimą, galite taikyti iš anksto nustatytą sudengimo prioritetą arba galite patys nustatyti sudengimo prioritetų tvarką puslapyje **Gautinų sumų parametrai**. Ši funkcija galima tik gautinoms sumoms.

## <a name="results-of-settlement"></a>Sudengimo rezultatai

Atlikus operacijų sudengiamą kiekvienos operacijos nepamokėtas likutis atitinkamai padidėja arba sumažėja. Paprastai sudengus SF ir mokėjimą, kiekvienos operacijos būsena ir balansas atnaujinami pagal toliau nurodytas taisykles.

- Jei mokėjimo suma yra didesnė už SF sumą, SF balansas yra sumažinamas iki 0,00 ir SF uždaroma. Mokėjimas lieka atviras, o balansas reiškia mokėjimo sumos ir SF sumos skirtumą.
- Jei mokėjimo suma yra mažesnė už SF sumą, mokėjimo balansas sumažėja iki 0,00 ir mokėjimas uždaromas. SF lieka atvira, o balansas reiškia SF sumos ir mokėjimo sumos skirtumą.
- Jei mokėjimo suma yra lygi SF sumai, mokėjimas ir SF uždaromi, o jų balansas sumažinamas iki 0,00.

Jei [mokėjimo suma yra mažesnė už SF sumą](../accounts-payable/vendor-payments-partial-amount.md) dėl mokėjimo nuolaidos, nurašymo arba neprimokėjimo, SF ir mokėjimas vis tiek gali būti uždaryti – tai priklauso nuo sudengimų konfigūravimo puslapiuose **Mokėtinų sumų parametrai** ir **Gautinų sumų parametrai**.

Be to, sudengimai gali generuoti operacijas. Pvz., SF ir mokėjimo sudengimas gali sąlygoti mokėjimo nuolaidą, gautą pelną arba patirtą nuostolį, PVM koregavimus, nurašymai arba centų skirtumus.

## <a name="identifying-marked-transactions-during-settlement"></a>Pažymėtų operacijų nustatymas sudengimo metu

Kai bandote sudengti operaciją, galite pastebėti simbolį, nurodantį, kad operacija pažymėta kitoje vietoje. Tokiu atveju galite pasirinkti operaciją puslapyje **Sudengti operacijas** ir pasirinkti **Užklausa \> Sudengimo lango sudengimas**. Šios užklausos rodinyje nurodomi žurnalai, pardavimo užsakymai, SF, mokėjimo pasiūlymai ir kliento vietos, kurios gali blokuoti sudengimo operaciją. Norėdami išspręsti problemą, galite pasirinkti saitą, kad eitumėte tiesiogiai iš užklausos į blokuojamą vietą. Tada galite atnaujinti dokumentą koregavimais, kurių reikia norint sudengti. Taip pat galite naudoti indikatorių **Pažymėta**, kad nustatytumėte kitus dokumentus, įtrauktus į tą pačią blokuojamą vietą.

## <a name="resolve-issues-with-transactions-that-cant-be-settled"></a>Spręsti problemas, kai yra operacijų, kurių negalima sudengti

Kartais operacijų sudengti negalima, nes šiuo metu dokumentą apdorojusi kita veikla. Jei bandysite sudengti operacijas, įvyksta klaida, nes šios operacijos yra naudojamos. Norėdami išspręsti šią problemą, galite naudoti puslapį **Pažymėtų operacijų informacija** kad rastumėte operacijas, pažymėtas sudengti, ir identifikuotumėte visus kitus prie jų prieitiius procesus.

Operacijos pažymimos sudengti arba kai tiekėjo SF apmokamos arba kai klientai apmoka atviras SF. Kartais šios SF gali būti pažymėtos sudengti. Todėl vartotojai negali jų pasirinkti mokėjimui. SF gali būti pažymėtos kitu kliento mokėjimų žurnalu, pardavimo užsakymu, tiekėjo mokėjimo žurnalu arba pirkimo užsakymu dabartiniame juridiniame subjekte ar kitame juridiniame subjekte.

Jei įvedant kliento mokėjimą operacija yra užblokuota sudengti, atidarykite **kliento pažymėtų operacijų informacijos** puslapį (**Gautinų sumų \> periodinės užduotys \> klientas pažymėjo kaip operacijų informaciją**). Norėdami greitai nustatyti, kur užblokuota operacija, galite nustatyti bet kurį iš šių pasirinkimo parametrų: **Kliento sąskaita**, **Kvitas**, **Data** arba **SF**. Jei nenustatysite jokių pasirinkimo parametrų, sistema siųs visus užblokuotus dabartinės įmonės ar kitos jūsų pasirinktos įmonės dokumentus. Identifikę operaciją, kuri užblokuota sudengti, galite ją pasirinkti, o tada pasirinkti **pasirinktų operacijų atžymėti**. Pasirinkta operacija tada pašalinama iš bet kurio žurnalo, kuriame ji yra. Tačiau dokumentas nepašalinamas iš kitos vietos. Iš to žurnalo pašalinama tik žymėjimo informacija.

Jei įvedant pardavėjo mokėjimą operacija yra užblokuota sudengti, atidarykite **Pardavėjo pažymėtų operacijų informacijos** puslapį (**Mokėtinų sumų \> periodinės užduotys \> pradavėjas pažymėjo kaip operacijų informaciją**). Norėdami greitai nustatyti, kur užblokuota operacija, galite nustatyti bet kurį iš šių pasirinkimo parametrų: **Pradavėjo sąskaita**, **Kvitas**, **Data** arba **SF**. Jei nenustatysite jokių pasirinkimo parametrų, sistema siųs visus užblokuotus dabartinės įmonės ar kitos jūsų pasirinktos įmonės dokumentus. Identifikę operaciją, kuri užblokuota sudengti, galite ją pasirinkti, o tada **pasirinkti pasirinktų operacijų atžymėti** siekiant ištaisyti blokavimo problemą. Pasirinkta operacija tada pašalinama iš bet kurio žurnalo, kuriame ji yra. Tačiau dokumentas nepašalinamas iš kitos vietos. Iš to žurnalo pašalinama tik žymėjimo informacija.

Norėdami identifikuoti visus užblokuotus dokumentus, atidarykite puslapį **Visa pažymėta operacijų informacija** tada (**Gautinų sumų \> periodinės užduotys \> Visa pažymėta operacijų informacija** ar **Mokėtinų sumų \> periodinės užduotys \> Visa pažymėta operacijų informacijas**). Norėdami greitai nustatyti, kur užblokuota operacija, galite nustatyti bet kurį iš šių pasirinkimo parametrų: **Kliento sąskaita**, **Pardavėjo sąskaita**, **Kvitas**, **Data**, ar **SF**. Jei nenustatysite jokių pasirinkimo parametrų, sistema siųs visus užblokuotus dabartinės įmonės ar kitos jūsų pasirinktos įmonės dokumentus. Identifikę operaciją, kuri užblokuota sudengti, galite ją pasirinkti, o tada **pasirinkti pasirinktų operacijų atžymėti** siekiant ištaisyti blokavimo problemą. Pasirinkta operacija tada pašalinama iš bet kurio žurnalo, kuriame ji yra. Tačiau dokumentas nepašalinamas iš kitos vietos. Iš to žurnalo pašalinama tik žymėjimo informacija.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti **Funkcijos valdymas** darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** Grynųjų pinigų ir banko valdymas
- **Priemonės pavadinimas:** pažymėtų operacijų informacijos forma

## <a name="additional-resources"></a>Papildomi ištekliai

- [Sudengti likutį](settle-remainder.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
