---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0215e815e3e44568fb81ab7fad9b44c219e961cb6ef68996bf43218ef817e8d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765057"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]