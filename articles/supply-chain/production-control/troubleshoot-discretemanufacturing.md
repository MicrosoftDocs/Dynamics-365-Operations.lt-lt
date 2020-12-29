---
title: Trikties šalinimo diskretiška gamyba
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su diskretiška gamyba.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 604e0c3406b15d885991fcb067e93ef83533e3b0
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516836"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Trikties šalinimo diskretiška gamyba

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su diskretiška gamyba.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Gaunu tolesnį klaidos pranešimą: „Sandėlio valdymo procesai šiuo metu yra naudojami. Jei darbo eilučių dar neregistravote, galite atšaukti sukurtą darbą ir bet kurį krovinį ar siuntimo eilutes ir tuomet tęsti paėmimą ar siuntimo procesą.“

### <a name="issue-description"></a>Problemos aprašas

Ši klaida atsitinka, jei bandote rezervuoti ar atlaisvinti darbą eilutei, bet inventoriaus perleidimo būsena yra *Paimta*, kuri rodo, kad medžiaga buvo paimta.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Norėdami ištaisyti šią klaidą, atlikite vieną iš tolesnių veiksmų.

- Keiskite gamybos užsakymo būseną atgal į *Apskaičiuota* ar *Išleista*.
- Atverkite informacijos puslapį atitinkamam gamybos užsakymui. Veiksmų juostoje, **Sandėlio** skirtuke **Stabdymo** grupėje pasirinkite **Stabdyti ir išpakuoti** siekiant išpakuoti visas supakuotas perlaidas. Tada pasirinkite **Panaikinti stabdymą** tam, kad apdorotumėte gamybos darbą.

Čia pateikiamas funkcijų *Išpakuoti* ir *Stabdyti* paaiškinimas:

- **Išpakuoti** – Ši funkcija atkeičia inventoriaus perlaidų būseną medžiagų važtaraščiui (BOM) eilutėms ir formulės eilutes, kurios turi būseną iš *Paimta* iki *Užsakyme*. Kai darbas žaiavų paėmimui yra užbaigtas, būsena eilutėms nustatyta į *Paimta*. Ši būsena neleidžia gamybos užsakymo paleisti iš naujo į *Sukurta* būseną. Šiuo atveju, galite naudoti *Išpakuoti* funkciją, kad grąžintumėte perlaidas iš *Paimta* būsenos ir tada paleistumėte iš naujo gamybos užsakymą į *Sukurta* būseną.
- **Stabdyti** – Ši funkcija nustato **Sustabdyta** vėliavą gamybos užsakyme siekiant apsaugoti bet kokią naujinimo užsakymo būseną. Galite rasti **Sustabdyta** vėliavą **Sandėlio** „FastTab“ gamybos užsakymo išsamios informacijos puslapyje.

> [!NOTE]
>
> - Mygtukai yra matomi tik, kai gamybos užsakymas yra sukuriamas prekėms įjungtoms sandėlio procesuose.
> - **Stabdymo** grupė yra matoma tik **Sandėlio** skirtuke gamybos užsakymo veiksmų juostos išsamios informacijos puslapyje. Ji nėra matoma **Sandėlio** „FastTab“ puslapyje **Gamybos užsakymai**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Atitikties resurso pavadinimas nėra naujintas po to, kai keičiu darbuotojo pavadinimą bendroje adresų knygoje.

### <a name="issue-description"></a>Problemos aprašas

Jei keičiate darbuotojo vardą bendrų adresų knygyne, atitinkamas resursų pavadinimas nėra naujinamas pagrindinėje resursų grupėje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Šis scenarijus šiuo metu nepalaikomas. Norėdami ištaisyti problemą, turite rankiniu būdu naujinti resurso pavadinimą.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Man sukuriant naują gamybos užsakymą, negaunu tolesnio pavadinimo: „Įveskite vekiančią važtaraščio versiją ir maršrutą?“

### <a name="issue-description"></a>Problemos aprašas

Jums sukūrus naują gamybos užsakymą ir įvedus prekės numerį, **Vietos** ir **Sandėlio** laukeliai yra automatiškai nustatyti į numatytąją vietą ir sandėlį, kurie yra nurodyti **Numatytojo užsakymo nustatymų** puslapyje baigtų prekių vienetui. Taip pat, galiojantis BOM numeris ir maršruto pavadinimas yra įvedami automatiškai. Negausite tolesnio pranešimo, kuris skatins jus įvesti šias vertes:

> Įvesti galiojančią važtaraščio versiją ir maršrutą?

### <a name="issue-resolution"></a>Problemos paaiškinimas

Nesate skatinamas įvesti BOM ir maršruto skaičius, jei pasirenkate produktą, kurio vieta ir sandėlis yra nustatyti **Numatytieji užsakymo nustatymai** puslapyje. Esate skatinamas tik, jei šios vertės nėra nustatytos pasirinktam produktui.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Gamybos užsakymai nėra rodomi ženklinimo puslapyje.

### <a name="issue-description"></a>Problemos aprašas

Kai kurie gamybos užsakymai nėra rodomi **Ženklinimo** puslapyje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Produktai turintys tolesnį konfigūravimą nėra prieinami ženklinimui. Dėl to, jie nebus rodomi **Ženklinimo** puslapyje:

- Produktai yra nustatyti kaip produktai kaip *gauto svorio* rūšis.
- Jie yra įjungti papildomuose sandėlio procesuose.
- Jie yra konfigūruojami, kad juos valdytų *Standartinės kainos* principas.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Bandydamas užbaigti gamybos užsakymą, gaunu šį klaidos pranešimas: „BOM apskaičiavimas vartojimo kaštų vertė turi būti neigiama atsiradus problemai iš inventoriaus."

Ši problema buvo ištaisyta 10.0.15 leidime.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Kai gamybos užsakymo būsena yra keičiama iš „Reported“ į baigtus kaip „End“, gaunu šį tolesnį klaidos pranešimą: „Naujinti konfiktą“. Standartiniai kaštai neatitinka su finansinio inventoriaus verte po naujinimo“ ir „Kritinė klaida atsitinka InventCostMovement.checkVariance funkcijoje."

Ši klaida atsitinka, nes pagrindiniai duomenys buvo pakeisti kito proceso. Procesas bandys naujinti duomenis iki penkių kartų. Jei konfliktas vis dar yra po penkių bandymų, gausite tolesnį klaidos pranešimą:

> Naujinti konfliktą. Standartiniai kaštai neatitinka su finansine inventoriaus verte po naujinimo.

> Kritinė klaida įvyko funkcijoje InventCostMovement.checkVariance.

Toks veikimo būdas yra numatytas. Norėdami sustabdyti šią problemą, tęskite bendro kiekio darbą. Jis turėtų užbaigti vykdymą.

Jei bendro kiekio darbas nuolatos nepavyksta po jo naujinimo, patikrinkite, ar apvalinimo tikslumas buhalterinės klaidos nustatytajai valiutai atitinka apvalnimą taikomą vertės „InventSum“ lentelėje. Jei apvalinimo tikslumas buvo pakeistas į neatitinkančią vertę, greičiausiai turite atkeisti ją atgal į atitinkančią vertę. Ieškokite **ModifiedDateTime**. Šiuo atveju, vertė dažniausiai rodys, kad apvalinimo tikslumas neseniai buvo pakeistas.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Paleisdamas į sandėlį gaunu tolesnį klaidos pranešimą: „Prekė RM negali būti pilnai rezervuota. Įsitikinkite, kad visas kiekis yra prieinamas arba rezervuokite prekes rankiniu būdu, jei rezervacijos laukelis BOM eilutėje yra nustatytas į rankinį ar pradėtą. Nepavyko paleisti užsakymo į sandėlį dėl to, kad kai kurių medžiagų nepavyko rezervuoti.“ Nepaisant to, būsena yra naujinta į išleistą.

### <a name="issue-description"></a>Problemos aprašas

Jei ne visos BOM eilutės prekės yra fiziškai prieinamos, kai gamybos užsakymas yra išleistas ir **Išleisti į sandėlį** politika yra nustatyta į *Būtina visa rezervacija* gamybos užsakyme, gausite tolesnį klaidos pranešimą:

> Prekė RM negali būti iki galo rezervuota. Įsitikinkite, kad visas kiekis yra prieinamas arba rezervuokite prekes rankiniu būdu, jei rezervacijos laukelis BOM eilutėje yra nustatytas į rankinį ar pradėtą. Nepavyko išleisti užsakymo į sandėlį, nes nepavyko rezervuoti kai kurių medžiagų.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Šis elgesys yra suprojektuotas tokiu būdu ir veikia kaip tikėtasi.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Bandydamas užbaigti gamybos užsakymą ir pranešti kaip baigtą, gaunu tolesnį klaidos pranešimą: „Bendras prekių kiekis, apie kurį pranšta kaip baigtą gamybai, bus %1. Paskutinės operacijos atsiliepimas yra 0,00 bendrai."

### <a name="issue-description"></a>Problemos aprašas

Jums bandant publikuoti ataskaitą kaip baigtą žurnalą gamybos užsakyme, gausite tolesnį klaidos pranešimą:

> Bendras prekių kiekis, kuris yra paskelbtas baigtas gamybai, bus %1. Paskutinės operacijos atsiliepimas yra 0,00 bendrai.

### <a name="possible-cause"></a>Galima priežastis

Ši problema atsitinka, jei publikuoti kiekiai paskutinėse operacijose nebuvo teisingi. Pavyzdžiui, jei gamyba yra pradėta, bet nurodytas kiekis negali būti priskirtas, maršruto kortelės žurnalas bus publikuotas be jokių eilučių. Norėdami patvirtinti situaciją, atverkite gamybos užsakymą ir tada veiksmų juostoje, **Peržiūros** skirtuke pasirinkite **Nukreipti kortelę**.

### <a name="workaround"></a>Apėjimo būdas

Galite ištaisyti šią klaidą publikuodami papildomus žurnalus operacijoms, kurioms žurnalai nebuvo tinkamai publikuoti. Paleiskite iš naujo gamybos užsakymą ir rinkitės papildomų žurnalų publikavimą. Šis veiksmas nepradės gamybos užsakymo, bet publikuos žurnalus. Maršruto kortelė tuomet turi rodyti publikuotus kiekius ir jūs tūrėtumėte galėti užbaigti gamybos užsakymus sėkmingai.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Ar galiu pranešti apie gamybos užsakymą kaip baigtą pranešdamas klaidos kiekį, bet nepranešdamas kiekio laiką ar medžiagas?

Negaliu pranešti klaidos kiekio gamybos užsakyme, nebent galite taip pat pranešti apie gerą kiekį. Šis scenarijus **nėra** palaikomas. Baigtų pranešimo naujinimas galiausiai nepavyks jums bandant užbaigti gamybos užsakymą ir jūs gausite tolesnį klaidos pranešimą:

> Nėra ataskaitos apie kiekį, paskelbtą užbaigtu.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Ar galiu sekti serijinius baigtų prekių numerius lyginant su suvartotų prekių serijiniais numeriais?

Negalite sekti baigtų prekių serijinius numerius lyginant su medžiagos serijiniais numeriais, kurią suvartoja gamybos užsakymas tam, kad būtų užbaigtos prekės. Šis scenarijus šiuo metu nepalaikomas. Apėjimą galima atlikti sukuriant gamybos užsakymus 1 kiekiui.
