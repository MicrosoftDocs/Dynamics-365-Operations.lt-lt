---
title: Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija
description: Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914544"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.

## <a name="overview"></a>Peržiūrėti

Žiniatinklio analizė yra esminė priemonė, kai norima suprasti, kaip klientai elgiasi jūsų svetainėje, ir priimti sprendimus, kurie padės optimizuoti maksimalaus konvertavimo tikslą. Šiems tikslams pasiekti yra daug žiniatinklio analizės paketų, pvz., „Google Analytics“, „Clicky“, „Moz Analytics“ ir „KISSMetrics“. Naudojant daugumą žiniatinklio analizės paketų reikalaujama, kad visuose svetainės puslapiuose į HTML elementą **\<head\>** įtrauktumėte kliento scenarijaus kodą.

> [!NOTE]
> Šioje temoje pateiktos instrukcijos taikomos ir kitoms pasirinktinėms kliento funkcijoms, kurių „Microsoft Dynamics 365 Commerce“ pati nesiūlo.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Pakartotinai galimo naudoti fragmento sukūrimas scenarijaus kodui

Sukūrus scenarijaus kodo fragmentą, jį galima pakartotinai naudoti visuose svetainės puslapiuose.

1. Nueikite į **Fragmentai \> Naujas puslapio fragmentas**.
2. Pasirinkite **Išorinis scenarijus**, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.
3. Fragmentų hierarchijoje pasirinkite ką tik sukurto fragmento antrinį modulį **scenarijaus injektorius**.
4. Dešinėje esančioje ypatybių srityje įtraukite kliento scenarijų ir pagal poreikį nustatykite kitas konfigūracijos parinktis.

## <a name="add-the-fragment-to-templates"></a>Fragmento įtraukimas į šablonus

1. Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.
2. Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.
3. Pasirinkite prie vietos **HTML antraštė** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti fragmentą**.
4. Pasirinkite fragmentą, kurį sukūrėte savo scenarijaus kodui.
5. Šabloną įrašykite ir atrakinkite.

> [!NOTE]
> Baigę turite publikuoti fragmentą ir pagrindinį šabloną. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

