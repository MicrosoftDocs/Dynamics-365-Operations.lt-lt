---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142322"
---
# <a name="create-cost-objects"></a>Išlaidų objektų kūrimas   

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. 


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

