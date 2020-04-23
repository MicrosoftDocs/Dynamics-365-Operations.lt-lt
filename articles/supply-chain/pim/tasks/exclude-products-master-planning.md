---
title: Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo
description: Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 999702b9a14965271b1ed350cda752e715a22a25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203600"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.


## <a name="create-an-obsolete-state"></a>Kurti nebenaudojamą būseną
1. Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.
2. Spustelėkite Naujas.
3. Lauke Būsena įveskite reikšmę.
4. Lauke Suaktyvinta planavimui pažymėkite Ne.
5. Lauke Aprašas įveskite reikšmę.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Susieti nebenaudojamą būseną su išleistu produktu
1. Uždarykite puslapį.
2. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
3. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Ieškos pavadinimas nurodydami reikšmę „M00“.
4. Spustelėkite Redaguoti.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.

