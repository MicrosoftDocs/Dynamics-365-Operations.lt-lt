---
title: Trikčių šalinimo kaštų valdymas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis susiduriate dirbdami su kaštų valdymu.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4434038"
---
# <a name="troubleshoot-cost-management"></a>Trikčių šalinimo kaštų valdymas

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis susiduriate dirbdami su kaštų valdymu.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funkciniai pertrūkiai tarp invenoriaus vertės/senėjimo ataskaitų ir jų laikymo versijų

[Inventoriaus senėjimo ataskaitos laikymas](inventory-aging-report-storage.md) ir [Inventoriaus vertės laikymo ataskaita](inventory-value-report-storage.md) funkcijos įjungimas „Supply Chain Management“ siekiant rodyti didelės apimties inventoriaus perlaidas. Visais atvejais, ataskaitos rezultatai yra įrašomi į naršymą ir eksportavimą, skirtingai nei šių ataskaitų nelaikymo versijos. Nepaisant to, kai kurios funkcijos esančio šių ataskaitų nelaikymo versijose neegzistuoja laikymo versijose. Tolesni papildomi skyriai apibendrina skirtumus ir pateikia apėjimus.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Laikymo ataskaitos neapiba papildomų tarpines sumos, net jei jos įjungtos ataskaitos išdėstyme.

Tarpinės sumos gali sukelti problemas, kai rezultatas yra eksportuojamas, ypač jei naudotojai keičia įrašo seką.

Norėdami patikrinti tarpines sumas, galite eksportuoti rezultatą į „Microsoft Excel“. Kitu atveju, jei norite patikrinti tarpines sumas „Supply Chain Management“, naudokite [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte *Naujo tinklelio valdiklį* ir *(Peržiūrą) Grupavimą į tinklelius* funkciją, kuri suteikia lankstesnį būdą matyti tarpines sumas bet kuriai kitai stulpelio grupei. Norėdami gauti daugiau informacijos, žr. [Tinklelio galimybės](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Inventoriaus vertės talpinimo ataskaita nepalaiko buhalterinės sąskaitos informacijos

Galite vykdyti bandyminį balansą tam, kad gautumėte inventoriaus sąskaitas ir palygintumėte jas su **Inventoriaus vertės laikymo** ataskaita.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Įspėjimai ar klaidos yra rodomi keičiant buhalterinės knygos laikotarpio būseną neužvėrus inventoriaus

„Microsoft“ pristatė tolesnius patvirtinimus siekiant išvengti problemų, kurias sukėlė netinkamas laikotarpio pabaigos procesas dėl kaštų. Jei susiduriate su bet kuriuo iš šių klaidos pranešimų, žr. [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) dėl išsamesnės informacijos apie tai, kaip spręsti šias problemas.

- Rengiatės vykdyti pakartotinį skaičiavimą su data %1 (10-02-2019). Paskutinis registruotas pakartotinis skaičiavimas buvo vykdytas ankstesniu laikotarpiu su data %2 (20-01-2019). Nėra jokio inventoriaus uždarymo vykdymo su data %3 (31-01-2019), kuris atitinka registruotą laikotarpio pabaigą. Prašome atsiminti, kad turite vykdyti inventoriaus uždarymą %3 (31-01-2019) pagla atitinkančio laikotarpio pabaigą. Inventorių vertinimas, parduotų prekių kaštai ir pakeitimai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol jis nebus atliktas.

- Rengiatės pakeisti buhalterinės laikotarpio knygose būseną %1 į %2. Nėra jokio inventoriaus uždarymo vykdymo su data %3, kuris atitinka registruotą laikotarpio pabaigą. Prašome vykdyti inventoriaus uždarymą %3 pagal atitinkančio laikotarpio pabaigą prieš pakeisdami būseną. Inventorių vertinimas, parduotų prekių kaštai ir pakeitimai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol jis nebus atliktas. Pranešta iš juridinio asmens %4. Kol kas šis veiksmas yra informacinio pobūdžio, tačiau ateityje jums reikės atlikti tokį veiksmą.

- Buhalterijos struktūra %1 buvo pakeista. Viena ar daugiau pagrindinių sąskaitų %2 nebeegzistuoja. Šios pagrindinės sąskaitos turi būti pagal %3 datą %4. Prašome įtraukti šias pagrindines sąskaitas į buhalterijos struktūrą %1 prieš tai, kai galėsite tęsti %3 darbą. Kol kas šis veiksmas yra informacinio pobūdžio, tačiau ateityje jums reikės atlikti tokį veiksmą.

- Rengiatės vykdyti inventoriaus uždarymą su data %1 (31-01-2019). Nėra jokio atgalinio nuleidimo kaštų apskaičiavimo vykdymo su data %2 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą. Prašome nepamiršti vykdyti atgalinio nuleidimo kaštų apskaičiavimo vykdymo su data %3 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą. Inventorių vertinimas, parduotų prekių kaštai ir pakeitimai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol jis nebus atliktas.

- Rengiatės vykdyti atgalinio nuleidimo kaštų skaičiavimą su data %1 (2019 02 28). Paskutinis registruotas atgalinis kaštų skaičiavimas buvo vykdytas ankstesniu laikotarpiu su data %2 (2019 01 31). Nėra jokio inventoriaus uždarymo vykdymo su data %3 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą.
Prašome atsiminti, kad turite vykdyti inventoriaus uždarymą %3 (2019 01 31) pagal atitinkančio laikotarpio pabaigą. Inventorių vertinimas, parduotų prekių kaštai ir pakeitimai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol inventoriaus uždarymas nebus įvykdytas.

## <a name="inventory-aging-report-discrepancies"></a>Inventoriaus senėjimo ataskaitos neatitikimai

**Inventoriaus senėjimo ataskaita** rodo kitas vertes, kai žvelgiate į skirtingus talpinimo matmenis (tokius kaip vieta ar sandėlis). Dėl išsamesnės informacijos apie ataskaitų teikimo logiką, žr. [Inventoriaus senėjimo ataskaitos pavyzdžiai ir logika](inventory-aging-report.md).
