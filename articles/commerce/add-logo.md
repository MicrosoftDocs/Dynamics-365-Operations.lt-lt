---
title: Įtraukti logotipą
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914628"
---
# <a name="add-a-logo"></a>Įtraukti logotipą

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.

## <a name="overview"></a>Peržiūrėti

Kuriant svetainę vienas iš pirmųjų atliekamų veiksmų yra įmonės ar prekės ženklo logotipo įtraukimas į svetainės antraštę. „Dynamics 365 Commerce“ internetiniame darbo pradžios rinkinyje yra modulis, kurį naudojant šią užduotį atlikti lengva.

Logotipą galite įtraukti tiesiai į šabloną, maketą arba puslapį. Tokiu būdu galite lengvai keisti logotipą, kuris rodomas konkrečiuose puslapiuose arba puslapių grupėse. Tačiau šioje temoje aprašoma dažniausiai pasitaikanti situacija, kai logotipas įtraukiamas į antraštės fragmentą, kurį galima pakartotinai naudoti visuose svetainės puslapiuose.

## <a name="prerequisites"></a>Būtinieji komponentai

Kad galėtumėte įtraukti logotipą į visus svetainės puslapius, turite atlikti tolesnes užduotis.

1. Logotipą nusiųskite į skaitmeninių išteklių tvarkytuvą, kurį galite pasiekti puslapyje **Ištekliai**.
1. Sukurkite antraštės fragmentą. Daugiau informacijos apie tai, kaip kurti ir naudoti fragmentus, rasite temoje [Darbas su fragmentais](work-with-fragments.md).
1. Antraštės fragmentą įtraukite į šabloną, kuris svetainės puslapiuose naudojamas kaip jų maketo ir modulių parinktys. Daugiau informacijos apie šablonus rasite temoje [Darbas su šablonais](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logotipo įtraukimas į antraštės fragmentą

Norėdami logotipą įtraukti į svetainės antraštės fragmentą, atlikite toliau nurodytus veiksmus.

1. Kairėje esančioje naršymo srityje pasirinkite **Fragmentai**, tada – savo sukurtą antraštės fragmentą.
2. Pasirinkite **Paimti**.
3. Išplėskite dalis **Antraštė** ir **Logotipas**.
4. Pasirinkite prie dalies **Logotipas** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.
5. Pasirinkite logotipo modulį.
6. Dešinėje esančioje ypatybių srityje sukonfigūruokite logotipo modulį, kad jame būtų rodomas jūsų logotipas.
7. Antraštės fragmentą įrašykite, atrakinkite ir publikuokite.

Publikavus atnaujintą antraštės fragmentą, visuose svetainės puslapiuose, kuriuose naudojamas šablonas su šiuo antraštės fragmentu, bus rodomas jūsų logotipas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

