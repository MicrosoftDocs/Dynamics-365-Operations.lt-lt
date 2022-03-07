---
title: Įspėjimai ar klaidos yra rodomi keičiant buhalterinės knygos laikotarpio būseną neužvėrus inventoriaus
description: Įspėjimai ar klaidos yra rodomi keičiant buhalterinės knygos laikotarpio būseną neužvėrus inventoriaus
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477078"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Įspėjimai ar klaidos yra rodomi keičiant buhalterinės knygos laikotarpio būseną neužvėrus inventoriaus

„Microsoft“ pristatė tolesnius patvirtinimus siekiant išvengti problemų, kurias sukėlė netinkamas laikotarpio pabaigos procesas dėl kaštų. Jei susiduriate su bet kuriuo iš šių klaidos pranešimų, žr. [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) dėl išsamesnės informacijos apie tai, kaip spręsti šias problemas.

- Rengiatės vykdyti pakartotinį skaičiavimą su data %1 (10-02-2019). Paskutinis registruotas pakartotinis skaičiavimas buvo vykdytas ankstesniu laikotarpiu su data %2 (20-01-2019). Nėra jokio inventoriaus uždarymo vykdymo su data %3 (31-01-2019), kuris atitinka registruotą laikotarpio pabaigą. Prašome atsiminti, kad turite vykdyti inventoriaus uždarymą %3 (31-01-2019) pagla atitinkančio laikotarpio pabaigą. Atsargų vertinimas, parduotų prekių išlaidos ir nuokrypiai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol šis veiksmas nebus atliktas.

- Rengiatės pakeisti buhalterinės laikotarpio knygose būseną %1 į %2. Nėra jokio inventoriaus uždarymo vykdymo su data %3, kuris atitinka registruotą laikotarpio pabaigą. Prašome vykdyti inventoriaus uždarymą %3 pagal atitinkančio laikotarpio pabaigą prieš pakeisdami būseną. Atsargų vertinimas, parduotų prekių išlaidos ir nuokrypiai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol šis veiksmas nebus atliktas. Pranešta iš juridinio asmens %4. Kol kas šis veiksmas yra informacinio pobūdžio, tačiau ateityje jums reikės atlikti tokį veiksmą.

- Buhalterijos struktūra %1 buvo pakeista. Viena ar daugiau pagrindinių sąskaitų %2 nebeegzistuoja. Šios pagrindinės sąskaitos turi būti pagal %3 datą %4. Prašome įtraukti šias pagrindines sąskaitas į buhalterijos struktūrą %1 prieš tai, kai galėsite tęsti %3 darbą. Kol kas šis veiksmas yra informacinio pobūdžio, tačiau ateityje jums reikės atlikti tokį veiksmą.

- Rengiatės vykdyti inventoriaus uždarymą su data %1 (31-01-2019). Nėra jokio atgalinio nuleidimo kaštų apskaičiavimo vykdymo su data %2 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą. Prašome nepamiršti vykdyti atgalinio nuleidimo kaštų apskaičiavimo vykdymo su data %3 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą. Atsargų vertinimas, parduotų prekių išlaidos ir nuokrypiai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol šis veiksmas nebus atliktas.

- Rengiatės vykdyti atgalinio nuleidimo kaštų skaičiavimą su data %1 (2019 02 28). Paskutinis registruotas atgalinis kaštų skaičiavimas buvo vykdytas ankstesniu laikotarpiu su data %2 (2019 01 31). Nėra jokio inventoriaus uždarymo vykdymo su data %3 (2019 01 31), kuris atitinka registruotą laikotarpio pabaigą.

Prašome atsiminti, kad turite vykdyti inventoriaus uždarymą %3 (2019 01 31) pagal atitinkančio laikotarpio pabaigą. Inventorių vertinimas, parduotų prekių kaštai ir pakeitimai gali būti neteisingi papildomoje buhalterijos knygoje ar pagrindinėje knygoje, kol inventoriaus uždarymas nebus įvykdytas.