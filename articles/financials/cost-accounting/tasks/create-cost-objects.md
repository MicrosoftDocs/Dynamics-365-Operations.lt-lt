---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant Dynamics 365 for Finance and Operations redakcijos įmonėms išlaidų centro finansinę dimensiją į savikainos apskaitą per duomenų jungtį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543776"
---
# <a name="create-cost-objects"></a>Išlaidų objektų kūrimas   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant Dynamics 365 for Finance and Operations redakcijos įmonėms išlaidų centro finansinę dimensiją į savikainos apskaitą per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai kaštų apskaitos funkcijai aprašyti.


## <a name="create-new-cost-objects"></a>Naujų išlaidų objektų kūrimas
1. Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.
5. Lauke Aprašas įveskite reikšmę.
6. Spustelėkite Įrašyti.

## <a name="configure-the-data-connector"></a>Duomenų jungties konfigūravimas
1. Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.
    * Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.  
2. Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.
3. Spustelėkite GERAI.

## <a name="import-cost-centers"></a>Importuoti išlaidų centrus
1. Spustelėkite Importuoti dimensijos narius.
2. Spustelėkite GERAI.

## <a name="view-the-imported-cost-centers"></a>Importuotų išlaidų centrų peržiūra
1. Spustelėkite Peržiūrėti dimensijos narius.

