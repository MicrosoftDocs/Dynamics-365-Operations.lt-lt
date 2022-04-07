---
title: Vietos plano kūrimas
description: Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8330fc15074eb59762dac73d0b176bd7faadc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469511"
---
# <a name="create-a-plan-for-a-site"></a>Vietos plano kūrimas

[!include [banner](../../includes/banner.md)]

Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus. Kai sukurti šaltinių pasiūlymai, jis randa užsakymus planuojamoje vietoje ir juos patvirtina, pradėdamas nuo skubiausių. Skubiausi užsakymai yra tie, kuriuos patvirtinti reikia šią dieną. Šioms užduotims atlikti naudokite demonstracinių duomenų įmonę USMF.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]