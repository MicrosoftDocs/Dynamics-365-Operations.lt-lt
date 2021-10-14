---
title: Kurti numatytąją produkto ciklo būseną
description: Ši procedūra nurodo, kaip sukurti numatytąją produkto ciklo būseną, taip pat kaip susieti numatytąją būseną su išleistais produktais.
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
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578205"
---
# <a name="create-a-default-product-lifecycle-state"></a>Kurti numatytąją produkto ciklo būseną

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti numatytąją produkto ciklo būseną, taip pat kaip susieti numatytąją būseną su išleistais produktais.


## <a name="create-a-default-lifecycle-state"></a>Kurti numatytąją ciklo būseną
1. Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.
2. Spustelėkite Naujas.
3. Lauke Būsena įveskite reikšmę.
4. Lauke Numatytoji reikšmė, kai išduodama juridiniam subjektui pasirinkite Taip.
5. Lauke Aprašas įveskite reikšmę.
6. Lauke Suaktyvinta planavimui pažymėkite Ne.

> [!NOTE]
> Jei naujas išleistas produktas neturėtų būti įtrauktas į procesą Bendrasis planavimas, pasirinkite Ne. Jei jis turėtų būti įtrauktas į procesą Bendrasis planavimas, palikite numatytąją valdiklio reikšmę Taip.  

## <a name="create-a-new-released-product"></a>Kurti naują išleistą produktą
1. Uždarykite puslapį.
2. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
3. Spustelėkite Naujas.
4. Lauke „Produkto numeris“ įveskite reikšmę.
5. Lauke Produkto pavadinimas įveskite reikšmę.
6. Lauke Ieškos pavadinimas įveskite reikšmę.
7. Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.
8. Lauke Prekių grupė įveskite arba pasirinkite vertę.
9. Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.
10. Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.
11. Spustelėkite GERAI.

> [!NOTE]
> Numatytoji produkto ciklo būsena yra visuotinis apibrėžimas.  

## <a name="change-the-product-to-an-active-state"></a>Keisti produkto būseną aktyvia
1. Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.

> [!NOTE]
> Tarkime, kad nustatėte aktyvią būseną, todėl dabar galite pasirinkti tokią aktyvią būseną, kuri leistų naudoti produktą vykstant procesams Bendrasis planavimas ir Lygio KS skaičiavimas. Žinoma, tai prasminga tik tuo atveju, jei nurodyta visa norint atlikti nuoseklų planavimą reikalinga produkto informacija.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]