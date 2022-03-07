---
title: Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo
description: Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f72be341b81515b7c5540d66f61647df93af41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567036"
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