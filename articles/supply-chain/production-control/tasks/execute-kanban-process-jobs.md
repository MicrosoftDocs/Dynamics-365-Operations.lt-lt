---
title: Vykdyti „kanban“ proceso užduotis
description: Šioje procedūroje parodyta, kaip vykdyti „kanban“ proceso užduotis.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566584"
---
# <a name="execute-kanban-process-jobs"></a>Vykdyti „kanban“ proceso užduotis

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodyta, kaip vykdyti „kanban“ proceso užduotis. Pirmoji užduotis baigta su numatytu kiekiu ir be klaidų. Antroji užduotis baigta su klaidomis. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta mašinos operatoriui.


## <a name="select-a-kanban-job"></a>„Kanban‟ užduoties pasirinkimas
1. Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ sritis proceso užduotims.
2. Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Spustelėkite eilutę su 1250 išteklių grupe. Užduočių sąrašas filtruojamas, kad būtų rodomos tik 1250 darbo elemento užduotys.
    * Pažymėkite eilutę, kurios būsena – Suplanuota užduotis.  

## <a name="complete-a-job-with-expected-quantity"></a>Užduoties baigimas su numatytu kiekiu
1. Išplėskite arba sutraukite sekciją Informacija.
    * Šioje dalyje rodoma svarbi informacija apie kortelės numerį, prekės numerį, užsakytą kiekį ir veiklos pavadinimą.  
2. Išplėskite arba sutraukite dalį Gamybos instrukcijos.
    * Šioje dalyje rodomos veiklos gamybos instrukcijos. Instrukcijos gali būti tekstas, paveikslėliai, eskizai ir kiti dokumentai.  
3. Spustelėkite Pradėti.
    * Pasirinkite nepabaigtą užduotį. Naudokite būsenos piktogramas lauke Užduoties būsena, kad peržiūrėtumėte užduoties būseną.      
4. Spustelėkite Baigti.
    * Užduotis baigta, jos kokybė numatyta.  

## <a name="complete-a-job-with-errors"></a>Užduoties baigimas su klaidomis
1. Spustelėkite Pradėti.
    * Kai užduotis baigiama, automatiškai pasirenkama kita sąrašo užduotis. Todėl, prieš spustelėjant Pradėti, nereikia pasirinkti užduoties.  
2. Veiksmų srityje spustelėkite Gamyba.
3. Spustelėkite Užbaigti (informacija).
4. Sąraše pažymėkite pasirinktą eilutę.
5. Lauke Klaidų kiekis įveskite skaičių.
6. Lauke Tinkamas kiekis įveskite skaičių.
7. Spustelėkite GERAI.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]