--- 
title: "Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui"
description: "Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: f476c1b2585ce0b5b67cd0d91684c86f7d3bda36
ms.contentlocale: lt-lt
ms.lasthandoff: 02/08/2018

---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


