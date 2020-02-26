---
title: „Finance and Operations“ programų ir „Common Data Service“ pradinio sinchronizavimo vykdymo tvarka
description: Šioje temoje nurodoma sinchronizavimo tvarka, kurią turite sekti, kad sukurtumėte pradinius duomenis.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019920"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>„Finance and Operations“ programų ir „Common Data Service“ pradinio sinchronizavimo vykdymo tvarka

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Prieš pradėdami naudoti duomenų integraciją, turite sukurti pradinius duomenis, reikalingus klientams, tiekėjams ir kontaktams. Pavyzdžiui, norite sukurti naują elementą **Tiekėjų grupė** ir nustatyti jo **Mokėjimo sąlygos** reikšmę į **„Net30“**. Tokiu atveju, prieš bandydami sukurti elementą **Tiekėjų grupė**, turite įsitikinti, kad **„Net30“** yra ir programoje, ir „Common Data Service” (Ateityje „Microsoft“ išleis dvigubo rašymo platformos funkciją, vadinamą pradiniu sinchronizavimu. Ši funkcija atliks vienkartinį duomenų sinchronizavimą tarp programos ir „Common Data Service“ kaip dvigubo rašymo sąrankos dalis.)

> [!TIP]
> „Microsoft“ išleidžia dvigubo rašymo schemą visiems nuorodos duomenims, įskaitant **Mokėjimo sąlygos** (mokėjimo sąlygas). Jei jau turite pradinius duomenis vienoje sistemoje, mažas įrašo naujinimas gali sukelti įraše dvigubą rašymą.

Turite sekti šią pirmumo tvarką ir įsitikinti, kad pradiniai duomenys prieinami programoje ir „Common Data Service“.

## <a name="vendor"></a>Tiekėjas

Objekto **Tiekėjas** vykdymo tvarka:

1. Tiekėjų grupė

    1. Mokėjimo sąlygos

        1. Mokėjimo diena ir eilutės
        2. Mokėjimo grafikas

2. Tiekėjo mokėjimo būdas

## <a name="customer-organization"></a>Kliento organizacija

Objekto **Klientas** vykdymo tvarka:

1. Klientų grupė

    1. Mokėjimo sąlygos

        1. Mokėjimo diena ir eilutės
        2. Mokėjimas 

2. Kliento mokėjimo būdas

## <a name="contact-person"></a>Kontaktinis asmuo

Objekto **Kontaktas** vykdymo tvarka:

1. Klientas
2. Tiekėjas
