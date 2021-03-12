---
title: Trikčių šalinimo proceso gamyba
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti su proceso gamyba.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966185"
---
# <a name="troubleshoot-process-manufacturing"></a>Trikčių šalinimo proceso gamyba

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti su proceso gamyba.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Naudodamas darbo kortelės įrenginį siekiant pranešti apie dalinį kiekį paskutiniame darbe gamybos užsakyme visi ankstesni darbai tame užsakyme turi progreso būseną ir automatiškai užbaigiami.

Toks veikimo būdas yra numatytas. Puslapyje **Gamybos užsakymo nustatytosios vertės** skirtuke **Pranešti kaip baigtą** yra parinktis pavadinimus **Paskutinės žymos kelias**. Jei ši tema nustatyta į *Taip*, kelio kortelės žurnalas yra viešinamas kaip darbuotojas naudoja darbo kortelės įrenginį ir darbo kortelės terminalą siekiant pranešti apie paskutinę operaciją. Šis žurnalas rodo visas operacijas kaip baigtas ir užbaigia visus gamybos darbus. Kai **Paskutinės žymos kelio** parinktis yra nustayta į *Taip*, sistema nebeatsižvelgia į darbo būseną, kurią darbuotojas pasirinko jam pranešant apie paskutinę operaciją. Sistema taip pat neatsižvelgia į tai, ar darbuotojas praneša visą ar dalinį kiekį.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Bandydamas uždaryti atsargas gaunu tolesnį įspėjimo pranešimą: „Nevykdomas „Backflush“ kaštų skaičiavimas su data %1 atitikties periodo pabaiga buvo registruota."

Ankstesnėse nei 10.0.13 versijose, jei nenaudojate pasvirų gamybos kaštų srauto, gausite tolesnį neteisingą įspėjimo pranešimą uždarant inventorių:

> Jūs norite atlikti inventoriaus uždarymą su data %1. Nevykdomas „Backflush“ kaštų skaičiavimas su data %1 atitikties periodo pabaiga buvo registruota. Prašome prisiminti, kad turite atlikti „Backflush“ kaštų skaičiavimą pagal datą %1 su atitikties periodo pabaiga. Inventoriaus įvertinimas, parduotų prekių kaina ir pakeitimai gali būti neteisingi papildomoje ar pagrindinėje buhalterijos knygoja, kol ji nebus įgyvendinta.

Ši klaida buvo ištaisyta 10.0.13 leidime ir vėliau. Dėl išsamesnės informacijos: [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
