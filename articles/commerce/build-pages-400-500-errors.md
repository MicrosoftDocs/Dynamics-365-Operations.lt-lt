---
title: Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius
description: Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697111"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.

## <a name="overview"></a>Peržiūrėti

Jei užklausa nėra sėkminga, serveris pateikia HTTP būsenos kodo klaidų atsakus. Būsenos kodas 404 užfiksuojamas ir pateikiamas neradus puslapio, o būsenos kodas 500 – įvykus serverio klaidai. Programos „Dynamics 365 Commerce“ vartotojai gali kurti pasirinktinius būsenos kodo klaidų atsako puslapių, kurie rodomi vartotojams dėl tokių būsenos kodo klaidų atsako.

## <a name="build-a-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio kūrimas

Norėdami pradėti kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.

1. Savo pageidaujamoje žiniatinklio naršyklėje prisijunkite prie „Dynamics 365 Commerce“. 
1. Pasirinkite svetainę, kuriai norite sukurti 4xx / 5xx būsenos kodo klaidų atsako puslapį.

### <a name="build-the-template"></a>Šablono kūrimas

Norėdami sukurti būsenos kodo klaidų atsako puslapio šabloną, atlikite tolesnius veiksmus.

1. Nueikite į **Šablonai \> Naujas šablonas**.
1. Naująjį šabloną pavadinkite.
1. Sukurkite šabloną su norima būsenos kodo klaidų atsako puslapio struktūra.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.

### <a name="build-the-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio kūrimas

Norėdami kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.

1. Nueikite į **Puslapiai \> Naujas puslapis**.
1. Pavadinkite būsenos kodo klaidų atsako puslapį, tačiau **nenustatykite** lauko **URL**.
1. Sukurkite puslapį.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

> [!NOTE]
> Galite sukurti atskirus būsenos kodo klaidų atsako puslapius, skirtus 4xx ir 5xx būsenos kodo klaidoms. Taip pat galite naudoti tą patį bendrą būsenos kodo klaidų atsako puslapį abiem klaidų kategorijoms.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Būsenos kodo klaidų atsako puslapio peradresavimo nustatymas

Norėdami nustatyti būsenos kodo klaidų atsako puslapio peradresavimą, atlikite tolesnius veiksmus.

1. Nueikite į **URL \> Naujas \> Naujas pseudonimas** ir pasirinkite anksčiau sukurtą būsenos kodo klaidų atsako puslapį.
1. Lauke **Pseudonimas** įveskite **numatytasis-4xx** arba **numatytasis-5xx**, atsižvelgdami į būsenos kodo klaidų atsako puslapį, kurio peradresavimą nustatote. Šiuos pseudonimus reikia publikuoti. Kitu atveju peradresavimas neveiks.
1. Pasirinkite **Gerai**, kad patvirtintumėte susiejimą.

> [!NOTE]
> Jei abiem klaidų kategorijoms naudojate vieną būsenos kodo klaidų atsako puslapį, pakartokite šią procedūrą, kad kitos klaidų kategorijos pseudonimą susietumėte su tuo pačiu puslapiu.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbas su šablonais](work-with-templates.md)

[Įtraukti naują svetainės puslapį](add-new-page.md)

[Kurti puslapio URL](create-page-url.md)
