---
title: Vietos plano kūrimas
description: Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ef805ba42500175d29208f1dcd5d383c63adb8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214351"
---
# <a name="create-a-plan-for-a-site"></a>Vietos plano kūrimas

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]