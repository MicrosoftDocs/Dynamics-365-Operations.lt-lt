---
title: Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui
description: Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226742"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams. Būtina sąlyga: pirmiausia turite paleisti užduočių vedlį „Kurti naują produkto ciklo būseną“, kad įsitikintumėte, jog prieš paleidžiant šį užduočių vedlį yra sukurta bent viena produkto ciklo būsena.


## <a name="find-a-released-product-master"></a>Rasti išleistą bendrąjį produktą
1. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
2. Sąraše raskite ir pasirinkite norimą įrašą.

> [!NOTE]
> Nurodytas bendrojo produkto potipis Bendrasis produktas.  

## <a name="update-the-lifecycle-state"></a>Atnaujinti ciklo būseną
1. Spustelėkite Redaguoti.
2. Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.
3. Spustelėkite Įrašyti.
4. Spustelėkite Taip.

> [!NOTE]
> Pasirinkus Taip visų susijusio išleisto produkto variantų, kurių pradinė būsena tokia pati kaip išleisto bendrojo produkto, būsena taip pat atnaujinamą į naują produkto ciklo būseną. Pasirinkus Ne išsaugoma faktinė visų variantų būsena. Variantai, kurių produkto ciklo būsena skiriasi nuo išleisto bendrojo produkto būsenos, neatnaujinami.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Patvirtinti variantų ciklo būseną
1. Spustelėkite Išleistų produktų variantai.

> [!NOTE]
> Atkreipkite dėmesį į tai, kad visi variantai įgavo pasirinktą bendrojo produkto ciklo būseną.  

2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]