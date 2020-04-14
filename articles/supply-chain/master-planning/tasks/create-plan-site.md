---
title: Vietos plano kūrimas
description: Gamybos planuotojas apskaičiuoja konkrečios prekės gamybos medžiagų ir pajėgumų reikalavimus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13238818de10596de34eaf9d8cd7d55562a307eb
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150314"
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

