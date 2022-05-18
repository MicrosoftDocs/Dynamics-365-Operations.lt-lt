---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734136"
---
# <a name="create-cost-objects"></a>Išlaidų objektų kūrimas   

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. 


## <a name="create-new-cost-objects"></a>Naujų išlaidų objektų kūrimas
1. Pereikite į kaštų **apskaitos > dimensijų > išlaidų objekto dimensijas**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. **Dimensijos narių lauke duomenų jungtį** įveskite arba pasirinkite vertę.
5. Lauke **Aprašo laukas** surinkite reikšmę.
6. Spustelėkite **Įrašyti**.

## <a name="configure-the-data-connector"></a>Duomenų jungties konfigūravimas
1. Spustelėkite Konfigūruoti **dimensijos nario teikėją**.
    * Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.  
2. **Dimensijos pavadinimo lauke** pasirinkite Išlaidų centrą.
3. Spustelėkite **Gerai**.

## <a name="import-cost-centers"></a>Importuoti išlaidų centrus
1. Spustelėkite **Importuoti dimensijos narius**.
2. Spustelėkite **Gerai**.

## <a name="view-the-imported-cost-centers"></a>Importuotų išlaidų centrų peržiūra
1. Spustelėkite **Peržiūrėti dimensijos narius**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
