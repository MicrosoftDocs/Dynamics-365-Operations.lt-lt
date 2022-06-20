---
title: Įtraukti logotipą
description: Šiame straipsnyje aprašoma, kaip prie savo svetainės pridėti logotipą Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 624cd6f7000f5038b9996eb94caf79719d07f99f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871785"
---
# <a name="add-a-logo"></a>Įtraukti logotipą

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip prie savo svetainės pridėti logotipą Microsoft Dynamics 365 Commerce.

Kuriant svetainę vienas iš pirmųjų atliekamų veiksmų yra įmonės ar prekės ženklo logotipo įtraukimas į svetainės antraštę. „Dynamics 365 Commerce“ internetinėje modulių bibliotekoje yra modulis, kurį naudojant šią užduotį atlikti lengva.

Logotipą galite įtraukti tiesiai į šabloną, maketą arba puslapį. Tokiu būdu galite lengvai keisti logotipą, kuris rodomas konkrečiuose puslapiuose arba puslapių grupėse. Tačiau šiame straipsnyje aprašomas dažniausiai naudojamas scenarijus, kai įtraukiate savo logotipą į antraštės fragmentą, kurį galima pakartotinai naudoti visuose jūsų svetainės puslapiuose.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad galėtumėte įtraukti logotipą į visus svetainės puslapius, turite atlikti tolesnes užduotis.

1. Įkelkite savo logotipą į medijos biblioteką.
1. Sukurkite antraštės fragmentą. Daugiau informacijos apie tai, kaip kurti ir naudoti fragmentus, rasite temoje [Darbas su fragmentais](work-with-fragments.md).
1. Antraštės fragmentą įtraukite į šabloną, kuris svetainės puslapiuose naudojamas kaip jų maketo ir modulių parinktys. Daugiau informacijos apie šablonus rasite temoje [Darbas su šablonais](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logotipo įtraukimas į antraštės fragmentą

Norėdami logotipą įtraukti į svetainės antraštės fragmentą, atlikite toliau nurodytus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Fragmentai**.
1. Pasirinkite sukurtą antraštės fragmentą, tada – **Redaguoti**.
1. Išplėskite antraštės modulį.
1. Antraštės modulio ypatybių srityje pateikite vaizdą ir saitą į logotipą. 
1. Įrašykite antraštės fragmentą, baikite redagavimą ir publikuokite.

Publikavus atnaujintą antraštės fragmentą, visuose svetainės puslapiuose, kuriuose naudojamas šablonas su šiuo antraštės fragmentu, bus rodomas jūsų logotipas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
