---
title: Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui
description: Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams.
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
ms.openlocfilehash: 217bab38544c2794d2e57410f8c2a979605106b0
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567012"
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