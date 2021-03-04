---
title: Gabenimo valdymo būsenos
description: Šioje temoje paaiškinta, kaip sukurti gabenimo būseną ir žemėlapį, kuris nurodo vežėjo būseną.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3f7d471771ec2b4703d878fbf395cd90902b6669
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434056"
---
# <a name="transportation-management-statuses"></a>Gabenimo valdymo būsenos

[!include [banner](../includes/banner.md)]

Nustatykite pagrindinius kodus gabenimo būsenoms, kad interpretuotumėte kodus, kurie pateikti jūsų gabenimo vežėjų. Jis leidžia jums integruoti su gabenimo vežėjais siekiant suteikti būseną. Gabenimo būsena, kurią pateikiate gabenimo pagrindinės būsenos koduis, jums padeda sekti krovinio, siuntimo ar talpos būseną. Konkreti gabenimo būsena kroviniui, siuntimui ar talpyklai gali būti naujinama per duomenų integravimą, o ne rankiniu būdu per vartotojo sąsają.

## <a name="create-a-transportation-status"></a>Sukurkite gabenimo būseną

Norėdami sukurti gabenimo būseną, atlikite šiuos žingsnius:

1. Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo būsenos pagrindiniai duomenys**.
1. Pasirinkite **Naujas**, kad sukurtumėte gabenimo būsenos pagrindinius duomenis.
1. Laukelyje **Gabenimo būsenos pagrindiniai duomenys** įveskite unikalų kodą gabenimo būsenai.
1. Laukelyje **Gabenimo tipas** pasirinkite  *Siunčiantis vežėjas* ar *Centras* kaip gabenimo tipą.
1. Įveskite gabenimo būseną ir pavadinimą.
1. Uždarykite puslapį.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Sudarykite gabenimo būsenos žemėlapį vežėjo būsenai

Siekiant sudaryti gabenimo būsenos žemėlapį vežėjo būsenai, elkitės taip:

1. Eikite į **Gabenimo valdymas \> Nustatymai \> Vežėjai \> Vežėjo gabenimo būsena**.
1. Rinkitės **Naujas** siekiant sudaryti žemėlapį kodui iš gabenimo vežėjo į gabenimo būsenos pagrindinį kodą.
1. Pasirinkite unikalų ID gabenimo vežėjui ir vežėjo paslaugoms.
1. Pasirinkite gabenimo būsenos kodą, kuriam norite sudaryti žemėlapį ir pasirinkti gabenimo vežėjo kodą.
1. Įveskite išorės kodą, kurį naudoja gabenimo vežėjas.
1. Uždarykite puslapį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]