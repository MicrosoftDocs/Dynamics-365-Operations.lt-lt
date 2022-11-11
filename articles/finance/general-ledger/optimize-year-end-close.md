---
title: Uždarymo metų pabaigoje optimizavimas
description: Šiame straipsnyje aprašomas metų pabaigos uždarymo paslaugos priedas, skirtas DK metų pabaigos uždarymo procesui.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/08/2022
ms.locfileid: "9749998"
---
# <a name="optimize-year-end-close"></a>Uždarymo metų pabaigoje optimizavimas

Optimizuojant Microsoft Dynamics metų pabaigos uždarymo tarnybos priedą, kuris skirtas 365 finansų, metų pabaigos uždarymo apdorojimas leidžia veikti ne programos objektų serverio (AOS) egzemplioriaus, skirto "Dynamics 365" finansų ištekliams, išorėje. Jis naudoja mikroservice technologiją. Išmokos, susijusios su metų pabaigos uždarymo optimizavimo funkcija, apima didesnį našumą ir sumažintą poveikį SQL duomenų bazei metų pabaigos uždarymo apdorojimo metu.

Norėdami naudoti metų pabaigos uždarymo funkcijų optimizavimą, turite atlikti šias užduotis:

1. Įdiekite metų pabaigos uždarymo tarnybos priedą iš savo ciklo Microsoft Dynamics tarnybos projekto.
2. Funkcijų valdymo **įjungti funkciją Optimizuoti metų** pabaigos uždarymą.

> [!NOTE]
> Išjungę funkcijų valdymo funkciją **optimizuokite** metų pabaigos uždarymo funkciją, vis tiek galite naudoti šių metų pabaigos uždarymo funkciją, kuri skirta finansų ištekliams.

## <a name="improved-performance"></a>Geresnis efektyvumas

Metų **pabaigos uždarymo optimizavimo** funkcija yra skirta pagreitinti metų pabaigos uždarymo apdorojimą, ypač klientams, kurie turi didelius duomenų kiekius. Kai metų pabaigos uždarymas vykdomas su paslauga, sunkus apdorojimas iškeliamas iš finansinių išteklių, siekiant sumažinti apdorojimo laiką ir atlaisvinti išteklių, kurie gali paveikti kitų vartotojų kasdienes operacijas.

Metų **pabaigos uždarymo optimizavimo** funkcija gali padėti pasiekti šiuos tikslus:

- Pagerinti metų pabaigos uždarymo našumą, sumažinus vykdyklės laiką.
- Sumažinti kitų procesų poveikį metų pabaigos uždarymo vykdymo metu.
- Pagerinti metų pabaigos rezultatų ataskaitas ir koregavimus, nes metų pabaigos uždarymas užtrunka mažiau laiko.

## <a name="new-options-and-visibility"></a>Naujos parinktys ir matomumas

Įgalinus **metų pabaigos uždarymo optimizavimo** priemonę, į šias **vietas** **įtraukiami** du nauji stulpeliai, rezultatai ir būsena:

- Uždarymo **metų pabaigoje** puslapyje
- **Metų pabaigos uždarymo rezultatų dialogo** lange
- Balanso **finansinės dimensijos perkėlimo pasirinktyse**, metų **pabaigos uždarymo šablono** puslapyje

Toliau esanti iliustracija rodo rezultatų ir **būsenos** **stulpelių** pavyzdį metų **pabaigos uždarymo** puslapyje. Norėdami atidaryti metų **pabaigos uždarymo** rezultatus **, stulpelyje** Rezultatai galite pasirinkti rezultatų saitą Peržiūrėti rezultatus. Būsenos **stulpelyje** rodoma dabartinė metų pabaigos uždarymo proceso būsena. Todėl naujuose stulpeliuose galima matyti metų pabaigos uždarymo proceso eigą.

[![Rezultatų ir būsenos stulpeliai metų pabaigos uždarymo puslapyje.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Be to, kai įgalinta **metų** pabaigos uždarymo optimizavimo funkcija, **·** "FastTab **" balanso finansines dimensijas galite rasti metų pabaigos uždarymo šablono** puslapyje. Uždarę metus, galite naudoti šį "FastTab" norėdami išsamiai nurodyti balanso finansines dimensijas. Ši galimybė yra lygiagreti su jau galima pelno ir nuostolio sąskaitų pajėgumais.

## <a name="architecture-and-data-flow"></a>Architektūra ir duomenų srautai

Norėdami naudotis **metų** pabaigos uždarymo funkcija ir paleisti metų pabaigos uždarymą mikroservice, **turite** įdiegti metų pabaigos uždarymo tarnybos priedą iš vykdymo ciklo tarnybų ir įgalinti funkciją Optimizuoti metų pabaigos uždarymą funkcijų valdymo srityje.

Kaip parodyta pateiktoje iliustracijoje, uždarymo metų pabaigoje apdorojimo metu patikrinama, ar įdiegtas priedas ir ar priemonė įgalinta. Jeigu atitinka abu būtinuosius komponentus, metų pabaigos uždarymas vyksta mikroservice.

[![Duomenų srauto diagrama.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Aukšto lygio srautas metų pabaigos uždarymui apdoroti

1. Metų pabaigos uždarymo procesas prasideda finansuose, DK **laikotarpio \> uždarymo metų \> pabaigoje**. Proceso metu sukuriamos uždaromos juridinių subjektų paketinės užduotys ir užduotys.
2. Metų pabaigos uždarymas nulemia, ar metų pabaigos uždarymas turi būti vykdomas mikroservice, ar dabartinėje uždarymo logitikoje.

    - Jei optimizuokite metų pabaigos uždarymo tarnybos priedą vykdymo ciklo tarnybose **ir** funkcijų valdymo funkcija optimizuoti metų pabaigos uždarymą yra įgalinta, metų pabaigos uždarymas bus paleistas mikrotarnėje.

        1. Metų pabaigos uždarymo optimizavimo funkcija sukuria metų pabaigos aptarnavimo užduotį kiekvienam uždaromame juridiniame subjekte, tada vykdo metų pabaigos uždarymo logiką. Mikroservice atlieka metų pabaigos uždarymą.
        2. Finansai klauso metų pabaigos pabaigos mikroservice, kad nustatytumėte, kada mikroservice baigė darbą. Tada uždarymo metų pabaigoje rezultatai atnaujinami finansų **metų pabaigos** uždarymo puslapyje.

    - Kitu atveju metų pabaigos uždarymas bus vykdomas pagal dabartinę uždarymo logiką.
