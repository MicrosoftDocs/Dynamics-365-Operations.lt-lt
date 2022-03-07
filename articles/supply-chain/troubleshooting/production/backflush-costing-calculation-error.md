---
title: Įkainojimo atvirkštine tvarka skaičiavimo klaida uždarant atsargas
description: Ankstesniuose leidimuose atsargų uždarymo metu galėjote gauti įkainojimo atvirkštine tvarka skaičiavimo klaidą. Ši klaida buvo ištaisyta.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477077"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Įkainojimo atvirkštine tvarka skaičiavimo klaida uždarant atsargas

## <a name="symptoms"></a>Požymiai

Ankstesnėse nei 10.0.13 versijose, jei nenaudojate pasvirų gamybos kaštų srauto, gausite tolesnį neteisingą įspėjimo pranešimą uždarant inventorių:

> Jūs norite atlikti inventoriaus uždarymą su data %1. Nevykdomas „Backflush“ kaštų skaičiavimas su data %1 atitikties periodo pabaiga buvo registruota. Prašome prisiminti, kad turite atlikti įkainojimo atvirkštine tvarka skaičiavimą pagal datą %1 su atitikties periodo pabaiga. Inventoriaus įvertinimas, parduotų prekių kaina ir pakeitimai gali būti neteisingi papildomoje ar pagrindinėje buhalterijos knygoje, kol ji nebus įgyvendinta.

## <a name="resolution"></a>Sprendimas

Ši klaida buvo ištaisyta 10.0.13 ir vėlesniuose leidimuose. Dėl išsamesnės informacijos: [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
