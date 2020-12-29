---
title: Automatiniai siuntos atnaujinimai
description: Šioje temoje pateikiama funkcijos, leidžiančios automatiškai atnaujinti siuntas, apžvalga.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable,SalesTableListPage,SalesTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fa2684340f5ce45b99ff9aee9937071f936b81a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433391"
---
# <a name="shipment-auto-updates"></a>Automatiniai siuntos atnaujinimai

[!include [banner](../includes/banner.md)]

Automatinio siuntos atnaujinimo funkcija automatiškai atnaujina krovinio eilučių, susietų su siunta, kiekius (ir padidėjimus, ir sumažėjimus) po to, kai krovinys yra paleistas į sandėlį. Ši funkcija lieka įjungta, kol krovinio ar siuntos krovinio eilutė apdorojama bangoje. Kai ji naudojama, užsakymo atnaujinimai gali automatiškai keliauti į sandėlį be rankinio įsikišimo, kol sukuriamas sandėlio darbas.

Kai automatinio siuntos atnaujinimo funkcija nenaudojama, tik kiekio sumažėjimai automatiškai keliauja, kol sukuriamas sandėlio darbas. Vartotojai turi rankiniu būdu atnaujinti arba panaikinti eilutes ir tada iš naujo paleisti eilutes, jei yra padidinami užsakymo kiekiai arba įtraukiamos naujos užsakymo eilutės. Naudodamos automatinio siuntos atnaujinimo funkciją, įmonės gali sklandžiai nusiųsti naujinimus į sandėlį be nerimavimo, kad susijusios siuntos ir kroviniai neatitiks užsakymo eilučių atnaujinimų.

Automatinio siuntos atnaujinimo funkcija taikoma ir pardavimo užsakymo eilutėms, ir perkėlimo užsakymo eilutėms, ir yra įjungta tam tikram sandėliui. Todėl įmonės gali pagal poreikį taikyti skirtingas automatinio siuntos atnaujinimo strategijas. Pagal numatytuosius nustatymus automatinio siuntos atnaujinimo strategija, skirta kiekio sumažėjimams, taikoma visiems sandėliams, kurie naudoja sandėlio valdymo procesus. Kai naudojamas šis numatytasis strategijos parametras, tik kiekio sumažėjimai automatiškai keliauja į siuntą ir krovinį, kol sukuriamas sandėlio darbas. Šis veikimo būdas atitinka būdą, kuris buvo naudojamas prieš automatinio siuntos atnaujinimo funkcijos įvedimą.

## <a name="main-elements-of-the-functionality"></a>Pagrindiniai funkcijos elementai

Automatinio siuntos atnaujinimo funkcija pirmiausia priklauso nuo siuntos būsenos, kad būtų galima nustatyti, ar kiekis krovinio eilutėje turi būti pakeistas, kai atliekami pakeitimai pardavimo užsakymo eilutėje arba perkėlimo užsakymo eilutėje. Ji taip pat pirmiausia priklauso nuo siuntos būsenos, kad būtų galima nustatyti, kada nauja krovinio eilutė turi būti automatiškai įtraukiama į esamą krovinį. Kai siuntos būsena yra **Bangos** arba aukštesnė, automatiškai nenaujinama.

Taip pat automatiniuose naujinimuose atsižvengiama į bangos būseną. Kai su krovinio eilute susijusios bangos būsena yra **Sulaikyta**, **Vykdoma**, **Išleista**, **Paimta** arba **Išsiųsta** ir vartotojas bando sumažinti kiekį krovinio eilutėje (kiekis sumažinamas pardavimo užsakymo eilutėje arba perkėlimo užsakymo eilutėje), rodomas šis klaidos pranešimas: „Rezervacijų šalinti negalima, nes sukurtas šiomis rezervacijomis grindžiamas darbas”. Be to, kai bangos būsena yra viena iš anksčiau minėtų ir vartotojas bando netiesiogiai padidinti krovinio eilutės kiekį padidindamas kiekį pardavimo užsakymo eilutėje arba perkėlimo užsakymo eilutėje, krovinio eilutėje nurodytas kiekis automatiškai nepadidėja. Tokiu atveju krovinio eilutę reikia atnaujinti rankiniu būdu.

## <a name="scenarios"></a>Scenarijai

Automatinio siuntos atnaujinimo funkcija palaiko keturis scenarijus: naujos užsakymo eilutės įtraukimą, kieko didinimą užsakymo eilutėje, kiekio sumažinimą užsakymo eilutėje ir užsakymo eilutės pašalinimą.

- **Naujos užsakymo eilutės įtraukimas**. Kai laukas **Automatiškai atnaujinti siuntą** „FastTab” konteinerio **Sandėlis** puslapyje **Sandėliai** (**Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**) nustatytas kaip **Visada** ir yra užsakymo siunta, o nauja užsakymo eilutė įtraukiama į pardavimo užsakymą ar perkėlimo užsakymą po to, kai jau buvo sukurtas pardavimo užsakymo krovinys, esamas krovinys neatnaujinamas. Nauja krovinio eilutė, kurioje nėra esamo krovinio nuorodos, yra sukuriama ir susieta su esama siunta. Nauja eilutė įtraukiama į krovinį ir išleidžiama.
- **Kiekio didinimas užsakymo eilutėje**. Kai laukas **Automatiškai atnaujinti siuntą** yra nustatytas kaip **Visada** ir yra užsakymo siunta, o esamoje pardavimo užsakymo eilutėje arba perkėlimo užsakymo eilutėje kiekis padidinamas po to, kai jau buvo sukurtas pardavimo užsakymo krovinys, kiekis krovinio eilutėje padidinamas tiek, kiek padidėjo užsakymo eilutėje. Jei krovinys buvo išleistas, bet nebuvo sukurtas darbas, kiekis krovinio eilutėje padidinamas tiek, kiek padidėjo užsakymo eilutėje.
- **Kiekio sumažinimas užsakymo eilutėje**. Kai laukas **Automatiškai atnaujinti siuntą** yra nustatytas kaip **Visada** arba **Sumažinus kiekį** ir yra užsakyme nurodyta siunta, o esamoje pardavimo užsakymo eilutėje arba perkėlimo užsakymo eilutėje kiekis sumažinamas po to, kai jau buvo sukurtas pardavimo užsakymo krovinys, kiekis susietoje krovinio eilutėje atnaujinamas, kad atitiktų, nebent kiekis toje krovinio eilutėje sutampa arba yra mažesnis nei naujas užsakymo eilutės kiekis. Tokiu atveju krovinio eilutė nėra paveikta. Jei krovinys buvo išleistas, bet nebuvo sukurtas darbas, susietos krovinio eilutės kiekis atnaujinamas, kad atitiktų, nebent kiekis toje krovinio eilutėje sutampa arba yra mažesnis nei naujas užsakymo eilutės kiekis. Tokiu atveju krovinio eilutė yra paveikta.
- **Užsakymo eilutės pašalinimas**. Kai laukas **Automatiškai atnaujinti siuntą** nustatytas kaip **Visada** arba **Sumažinus kiekį** ir vartotojas bando pašalinti užsakymo eilutę, kuriai priklauso krovinio eilutė, rodomas klaidos pranešimas.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Pagal šį scenarijų turite turėti įdiegtus demonstracinius duomenis ir naudoti **USMF** demonstracinių duomenų įmonę.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Įjungti automatinio siuntos atnaujinimo funkciją

Norėdami įjungti automatinio siuntos atnaujinimo funkciją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
2. Pasirinkite **24** sandėlį.
3. „FastTab” konteinerio **Sandėlis** lauke **Automatiškai atnaujinti siuntą**, pakeiskite vertę iš **Sumažinus kiekį** į **Visada**.

Po to, kai pakeisite vertę į **Visada**, bet koks kiekio padidėjimas ar sumažėjimas pardavimo užsakymo eilutėse ir perkėlimo užsakymo eilutėse ar bet kokiuose naujų eilučių papildymuose yra rodomas pasirinkto sandėlio siuntose ir kroviniuose, atsižvelgiant į anksčiau minėtus atnaujinimo apribojimus.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Keisti bangos šabloną, kad krovinio eilutės nebūtų automatiškai apdorotos

Norėdami sukonfigūruoti bangos šabloną taip, kad jis automatiškai neapdorotų krovinio eilučių, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
2. Pasirinkite bangos šabloną **24 numatytoji siunta**.
3. Pasirinkite **Redaguoti**.
4. „FastTab” konteineryje **Bendra** nustatykite parinktį **Automatiškai kurti bangą** kaip **Taip** ir įsitikinkite, kad visos kitos pasirinktys nustatytos kaip **Ne**.

Svarbu, kad joks darbas nebūtų automatiškai sukurtas ir paleistas kaip bangos kūrimo proceso dalis. Kai sukuriamas su krovinio eilute, kuri buvo sukurta pardavimo užsakymo eilutei, susijęs darbas, krovinio eilutė nebebus automatiškai atnaujinama, jei pasikeis kiekis pardavimo užsakymo eilutėje.

### <a name="create-a-sales-order"></a>Kurti pardavimo užsakymą

Norėdami sukurti pardavimo užsakymą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite klientą **US-003**.
3. Sukurkite prekės, kurios numeris **A0001**, eilutę.
4. Įvesti kiekį **10**. (Įsitikinkite, kad naudojate sandėlį **24**.)
5. Pasirinkite **Įrašyti**.
6. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**. Sukuriama siunta ir banga.

Dėl to, kad pakeitėte bangos šabloną ankstesnėje procedūroje, nėra sukuriamas krovinys ar darbas. Siuntos būsena yra **Laisva**, o bangos būsena yra **Sukurta**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Sumažinti kiekį pardavimo užsakymo eilutėje

Norėdami sumažinti kiekį pardavimo užsakymo eilutėje, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite pardavimo užsakymą, kurį ką tik išleidote į sandėlį.
3. Pasirinkite pardavimo užsakymo eilutę. Lauke **Kiekis** pakeiskite reikšmę **10** į **8**.
4. Iš pardavimo užsakymo eilutės pasirinkite **Sandėlis \> Siuntos informacija**. Puslapyje **Siuntos informacija**, „FastTab” konteineryje **Krovinio eilutės**, nurodytas kiekis atspindi pardavimo užsakymo eilutės pokytį.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Padidinti kiekį pardavimo užsakymo eilutėje

Norėdami padidinti kiekį pardavimo užsakymo eilutėje, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite pardavimo užsakymą, kurį anksčiau išleidote į sandėlį.
3. Pakeiskite kiekį eilutėje iš **8** į **12**.
4. Pasirinkite **Įrašyti**.
5. Grįžkite į puslapį **Visi pardavimo užsakymai** ir dar kartą pasirinkite pardavimo užsakymą.
5. Veiksmų srities skirtuko **Sandėlis** grupėje **Susijusi informacija** pasirinkite **Siuntos informacija**. Puslapyje **Siuntos informacija**, „FastTab” konteineryje **Krovinio eilutės**, nurodytas kiekis atspindi pardavimo užsakymo eilutės pokytį.

Nors kiekis krovinio eilutėje padidėja nuo 8 iki 12, tik aštuonios prekės lieka rezervuotos, išskyrus atvejus, kai įjungtas automatinis rezervavimas. Jei banga apdorojama be rezervavimo, darbas sukuriamas tik tam kiekiui, kuris jau rezervuotas, kadangi į esamą siuntą pridėtas kiekis nebuvo rezervuotas.

> [!NOTE]
> Sumažėjus kiekiui užsakymo eilutėje, kiekis krovinio eilutėje nėra paveiktas, jei jis sutampa arba yra mažesnis nei naujas užsakymo eilutės kiekis. Padidėjus kiekiui užsakymo eilutėje, kiekis krovinio eilutėje padidinamas tiek, kiek padidėjo užsakymo eilutėje. Jei kiekis užsakymo eilutėje skiriasi nuo kiekio krovinio eilutėje, skirtumas išlieka.

### <a name="add-a-sales-order-line"></a>Įtraukti pardavimo užsakymo eilutę

Norėdami įtraukti pardavimo užsakymo eilutę, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite pardavimo užsakymą, kurį anksčiau išleidote į sandėlį.
3. Sukurkite prekės, kurios numeris **A0002**, eilutę.
4. Lauke **Kiekis** įveskite **10**. (Įsitikinkite, kad naudojate sandėlį **24**.) Nauja eilutė automatiškai įtraukiama į esamą siuntą.
5. Pasirinkite **Įrašyti**.
6. Grįžkite į puslapį **Visi pardavimo užsakymai** ir dar kartą pasirinkite pardavimo užsakymą.
7. Veiksmų srities skirtuko **Sandėlis** grupėje **Susijusi informacija** pasirinkite **Siuntos informacija**. Puslapyje **Siuntos informacija**, „FastTab” konteineryje **Krovinio eilutės**, atkreipkite dėmesį į antrąją krovinio eilutę.

Jei banga apdorojama, darbas kuriamas tik tam kiekiui, kuris nurodytas pirmojoje pardavimo užsakymo eilutėje ir pirmojoje krovinio eilutėje, kadangi pardavimo užsakymo eilutė, kurią ką tik pridėjote prie esamos siuntos, nerezervuota.

### <a name="process-a-wave"></a>Vykdyti bangą

Norėdami vykdyti bangą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
2. Pasirinkite bangą, kurią sukūrėte anksčiau.
3. Veiksmų srities skirtuke **Banga**, grupėje **Banga** pasirinkite **Vykdyti**.

Banga apdorojama ir sukuriamas rezervuotų kiekių, esančių krovinio eilutėse, darbas. Siuntos būsena atnaujinama iš **Laisva** į **Bangos**. Kadangi siuntimo būsena atnaujinama į **Bangos**, bet kokie galimi pakeitimai, pvz., kiekių sumažėjimai ar padidėjimai eilutėse arba naujų eilučių pridėjimas į pardavimo užsakymą, neturi įtakos esamoms krovinio eilutėms, kurios susietos su bangos siunta.

Jei siuntos būsena yra **Bangos** arba aukštesnė, kiekio pardavimo užsakymo eilutėje atnaujinimai neatsispindi arba nepatvirtinami atsižvelgiant į su siunta susietą krovinio eilutę. Kiekio pasikeitimai krovinio eilutėje turi būti atliekami tiesiogiai krovinio eilutėje.

Tikrinimas atliekamas po to, kai sukuriamas krovinio eilutės darbas ir užrezervuojama. Tada kiekio pardavimo užsakymo eilutėje sumažėjimas yra patvirtinamas atsižvelgiant į darbo eilutės rezervavimą.
