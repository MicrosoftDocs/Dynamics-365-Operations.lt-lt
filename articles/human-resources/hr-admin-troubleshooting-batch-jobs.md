---
title: Optimizuokite našumą suplanuodami paketines užduotis po valandų
description: Šiame straipsnyje paaiškinama, kaip išspręsti efektyvumo problemas su "Microsoft Dynamics 365 Human Resources ", planuojant ilgalaikes paketines užduotis po valandų.
author: twheeloc
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6efb0a906bb948a47f03665dd6e7a8dd43434083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896082"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimizuokite našumą suplanuodami paketines užduotis po valandų


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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

   ![Pasikartojimo nustatymas.](media/talent-batch-history-cleanup-recurrence.png)

4. Po **Apibrėžti pasikartojimą** nustatykite **Pradžios datą** ir **Pradžios laiką**, kad pasirodytų nedarbo valandomis arba savaitgalį. Pasirinkite **Nėra pabaigos datos**. 

   ![Pasikartojimo pradžios datos ir laiko nurodymas.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Pasirinkite **Gerai**.

6. Jei būtina, pakeiskite parametrus **Vykdyti fone** dalyje ir pasirinkite **Gerai**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Efektyvumo optimizavimas naudojant automatinio valymo užduotis](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
