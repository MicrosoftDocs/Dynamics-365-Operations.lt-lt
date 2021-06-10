---
title: Optimizuokite našumą suplanuodami paketines užduotis po valandų
description: Šioje temoje paaiškinama, kaip išspręsti konkrečias našumo problemas naudojant „Microsoft Dynamics 365 Human Resources“, suplanuojant ilgai veikiančias paketines užduotis po valandų.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053472"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimizuokite našumą suplanuodami paketines užduotis po valandų

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Išdavimas

„Microsoft Dynamics 365 Human Resources” gali išbandyti našumo problemas, jei ilgai trunkančios paketinės užduotys vykdomos įprastu darbo laiku.

## <a name="resolution"></a>Skiriamoji geba

Suplanuokite šias paketines užduotis nedarbo valandomis. Taip pat rekomenduojame peržiūrėti dažnai vykdomų paketinių užduočių dažnumą. Jei įmanoma, sumažinkite paketinės užduoties pasikartojimą. Daugeliu atvejų numatytasis dažnumas yra tinkamas.

Šios paketinės užduotys turėtų būti vykdomos naktį arba po valandų. Būtinai patikrinkite laiko juostą šioms pasikartojančioms paketinėms užduotims. Kai kurios paketinės užduotys gali naudoti Ramiojo vandenyno standartinį laiką (PST).

| Paketinė užduotis | Numatytasis pasirodymas |
| --- | --- |
| Paketinės užduoties istorijos valymas | 1 kartą per mėnesį |
| Eksportavimo išdėstymo valymas | 1 kartą per dieną |
| „Common Data Service“ integracijoje trūksta užklausos sinchronizavimo | 1 kartą per dieną |
| Duomenų bazės glaudinimo sistemos užduotis, kurią reikia reguliariai vykdyti nedarbo valandomis | 1 kartą per dieną |
| Duomenų bazės indekso atkūrimo sistemos užduotis, kurią reikia reguliariai vykdyti nedarbo valandomis | 1 kartą per dieną |

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. **Ieška** juostoje ieškokite vienos iš aukščiau nurodytų paketinių užduočių.

3. Pasirinkite **Vykdyti fone**, tada pasirinkite **Pasikartojimas**.

   ![Pasikartojimo nustatymas](media/talent-batch-history-cleanup-recurrence.png)

4. Po **Apibrėžti pasikartojimą** nustatykite **Pradžios datą** ir **Pradžios laiką**, kad pasirodytų nedarbo valandomis arba savaitgalį. Pasirinkite **Nėra pabaigos datos**. 

   ![Pasikartojimo pradžios datos ir laiko nurodymas](media/talent-batch-history-cleanup-define-recurrence.png)

5. Pasirinkite **Gerai**.

6. Jei būtina, pakeiskite parametrus **Vykdyti fone** dalyje ir pasirinkite **Gerai**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Efektyvumo optimizavimas naudojant automatinio valymo užduotis](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]