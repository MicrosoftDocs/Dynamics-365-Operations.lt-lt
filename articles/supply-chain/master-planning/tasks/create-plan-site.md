--- 
title: "Vietos plano kūrimas"
description: "Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a>Vietos plano kūrimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus. Kai sukurti šaltinių pasiūlymai, užsakymus jis randa vietoje, kuriai planuoja ir juos patvirtina, pradėdamas nuo skubių. Skubiausi užsakymai yra tie, kuriuos patvirtinti reikia šią dieną. Šioms užduotims atlikti naudokite demonstracinių duomenų įmonę USMF.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Prekės medžiagų ir pajėgumų plano kūrimas
1. Spustelėkite Bendrasis planavimas.
    * Turite pereiti į numatytąją ataskaitų sritį.  
2. Spustelėkite Vykdyti.
3. Išplėskite dalį Įtrauktini įrašai.
4. Spustelėkite Filtras.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Kriterijai surinkite reikšmę.
    * Pavyzdys: D0001  
7. Spustelėkite GERAI.
8. Spustelėkite GERAI.
    * Tai gali užtrukti keletą minučių.  
9. Atnaujinkite puslapį.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Skubių suplanuotų prekės užsakymų identifikavimas
1. Atidarykite stulpelio filtrą Prekės numeris.
2. Lauke „Prekės numeris‟ pritaikykite filtrą, naudodami reikšmę „D0001‟ ir filtro operatorių „prasideda‟.
3. Atidarykite stulpelio filtrą Užsakymo data.
4. Laukui Užsakymo data taikykite filtrą – šios dienos reikšmę, naudodami filtro operatorių „yra tiksliai‟.

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Visų skubių prekės užsakymų patvirtinimas
1. Pažymėkite arba atžymėkite visas sąrašo eilutes.
2. Spustelėkite Patvirtinti.
3. Spustelėkite GERAI.


