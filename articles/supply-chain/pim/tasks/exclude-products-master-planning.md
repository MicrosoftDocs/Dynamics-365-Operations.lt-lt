---
title: Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo
description: Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818042"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]