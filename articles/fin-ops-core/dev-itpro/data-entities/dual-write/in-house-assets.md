---
title: Vidaus paslaugų turtas
description: Šioje temoje aprašoma, kaip galite naudoti „Microsoft Dynamics 365 Field Service“, kad būtų galima aptarnauti kliento turtą ir turtą įmonėje.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: d931811e9fbea3c10f83b048a3c3fbeda5396d39
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112488"
---
# <a name="in-house-assets-for-servicing"></a>Vidaus paslaugų turtas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

„Microsoft Dynamics 365 Field Service“ sukurta klientų turtui aptarnauti. Dynamics 365 Supply Chain Management turto valdymas yra skirtas valdyti vidaus turtą. Integravę šias dvi programėles, galite naudoti „Field Service“, kad aptarnautumėte tiek kliento, tiek vidaus turtą. Taip pat galite klasifikuoti turtą, pagrįstą funkcine vieta ar hierarchija, ir sekti aptarnavimą išsamesniu lygiu.

Daugiau informacijos rasite [Dynamics 365 Field Service ir „Supply Chain Management“ integravimas](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Šablonai

Vidinį turtą sudaro pagrindinių objektų schemų, veikiančių kartu, kai duomenys yra naudojami interaktyviai, rinkinys, kaip parodyta tolesnėje lentelėje.

| „Finance and Operations” programėlės | Modeliu grįstos programos „Dynamics 365“ | aprašymas |
|-----------------------------|-----------------------------------|-------------|
| Turto valdymo turto ciklo modeliai | msdyn\_assetlifecyclemodels | |
| Turto valdymo turto ciklo modelių būsenos | msdyn\_assetlifecyclestates | |
| Turto valdymo turtas | msdyn\_customerassets | |
| Turto valdymo turto tipai | msdyn\_customerassetcategories | |
| Turto valdymo funkcinių vietų ciklo modeliai | msdyn\_functionallocationlifecyclemodels | |
| Turto valdymo funkcinių vietų ciklo būsenos | msdyn\_functionallocationlifecyclestates | |
| Turto valdymo funkcinės vietos | msdyn\_functionallocations | |
| Turto valdymo funkcinių vietų tipai | msdyn\_functionallocationtypes | |
| Turto valdymo gamintojai | msdyn\_manufacturers | |
| Turto valdymo modeliai | msdyn\_models | |
| Turto valdymo garantija | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]
