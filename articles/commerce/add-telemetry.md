---
title: Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija
description: Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901501"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip į savo svetainės puslapius įtraukti kliento scenarijaus kodą, kad būtų palaikoma kliento telemetrijos rinkimo galimybė.

## <a name="overview"></a>Peržiūrėti

Žiniatinklio analizė yra esminė priemonė, kai norima suprasti, kaip klientai elgiasi jūsų svetainėje, ir priimti sprendimus, kurie padės optimizuoti maksimalaus konvertavimo tikslą. Šiems tikslams pasiekti yra daug žiniatinklio analizės paketų, pvz., „Google Analytics“, „Clicky“, „Moz Analytics“ ir „KISSMetrics“. Didžiajai daliai tinklo analitikos paketų turėsite įtraukti kliento pusės scenarijaus kodą  **\<head\>** HTML elemente visiems jūsų svetainės puslapiams.

> [!NOTE]
> Šioje temoje pateiktos instrukcijos taikomos ir kitoms pasirinktinėms kliento funkcijoms, kurių „Microsoft Dynamics 365 Commerce“ pati nesiūlo.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Pakartotinai galimo naudoti fragmento sukūrimas scenarijaus kodui

Fragmentas leidžia jums pakartotinai naudoti įdėtojo ar išorinio scenarijaus kodą visuose jūsų svetainės puslapiuose, neatsižvelgiant į jų naudojamą šabloną.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Pakartotinai galimo naudoti fragmento sukūrimas įdėtojo scenarijaus kodui

Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti fragmentą įdėtojo scenarijaus kodui, atlikite šiuos veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas**.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Linijinis scenarijus**.
1. Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.
1. Sukurto fragmento dalyje pasirinkite modulį **Numatytasis įdėtasis scenarijaus**.
1. Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų. Tada konfigūruokite kitas parinktis, kaip jums reikia.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Pakartotinai galimo naudoti fragmento sukūrimas išorinio scenarijaus kodui

Norėdami svetainių daryklėje sukurti pakartotinai galimą naudoti fragmentą išorinio scenarijaus kodui, atlikite šiuos veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas**.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Išorinis scenarijus**.
1. Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.
1. Sukurto fragmento dalyje pasirinkite modulį **Numatytasis išorinis scenarijaus**.
1. Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL. Tada konfigūruokite kitas parinktis, kaip jums reikia.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti**.

> [!NOTE]
> Jei jūsų svetainei įjungta turinio saugos strategija (CSP), įsitikinkite, kad visi išoriniai URL įtraukti į CSP direktyvą **script-src** „Commerce” svetainių daryklėje. - Norėdami gauti daugiau informacijos, žr. [turinio saugumo politikos valdymas (CSP)](manage-csp.md).

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Fragmento, kuriame yra scenarijaus kodas, įtraukimas į šabloną

Norėdami svetainių daryklėje į šabloną įtraukti fragmentą, kuriame yra scenarijaus kodas, atlikite šiuos veiksmus.

1. Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.
1. Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.
1. Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti fragmentą**.
1. Pasirinkite fragmentą, kurį sukūrėte savo scenarijaus kodui.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Išorinio scenarijaus arba įdėtojo scenarijaus įtraukimas tiesiai į šabloną

Jeigu norite įterpti įdėtąjį arba išorinį scenarijų tiesiai į vieno šablono valdomų puslapių rinkinį, jums nereikia iš pradžių kurti fragmento.

### <a name="add-an-inline-script-directly-to-a-template"></a>Įdėtojo scenarijaus įtraukimas tiesiai į šabloną

Norėdami svetainių daryklėje įtraukti įdėtąjį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.

1. Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.
1. Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.
1. Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Įdėtasis scenarijus**.
1. Dešinėje esančios ypatybių srities dalyje **Įdėtasis scenarijus** įveskite kliento scenarijų. Tada konfigūruokite kitas parinktis, kaip jums reikia.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti**.

### <a name="add-an-external-script-directly-to-a-template"></a>Išorinio scenarijaus įtraukimas tiesiai į šabloną

Norėdami svetainių daryklėje įtraukti išorinį scenarijų tiesiai į šabloną, atlikite šiuos veiksmus.

1. Nueikite į **Šablonai** ir atidarykite puslapių, į kuriuos norite įtraukti scenarijaus kodą, šabloną.
1. Kairiojoje srityje išplėskite šablonų hierarchiją, kad būtų rodoma vieta **HTML antraštė**.
1. Vietoje **HTML antraštė** pasirinkite daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Išorinis scenarijus**.
1. Dešinėje esančios ypatybių srities dalyje **Scenarijaus šaltinis** pridėkite išorinį arba santykinį išorinio scenarijaus šaltinio URL. Tada konfigūruokite kitas parinktis, kaip jums reikia.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)
