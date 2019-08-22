---
title: Vykdymo tvarka, skirta pradiniam „Finance and Operations“ ir „Common Data Service“ sinchronizavimui.
description: Šioje temoje nurodomas sinchronizavimas, kurį reikia atlikti norint sukurti pradinius duomenis.
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797303"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Vykdymo tvarka, skirta pradiniam „Finance and Operations“ ir „Common Data Service“ sinchronizavimui.

Prieš pradėdami naudoti duomenų integravimą, turite sukurti pradinius duomenis, reikalingus pirkėjams, tiekėjams ir kontaktams. Pavyzdžiui, jei norite sukurti naują **„Tiekėjo grupė“** prekę ir nustatyti jos **„Mokėjimo sąlygos“** kaip **„Net30“**, prieš bandydami sukurti **„Tiekėjo grupė“** prekę, turite įsitikinti, kad **„Net30“** egzistuoja tiek „Finance and Operations“ ir „Common Data Service“. (Ateityje išleisime dvigubo rašymo platformos funkciją, vadinamą **Initial Sync**. Tai atliks vienkartinį duomenų sinchronizavimą tarp „Finance and Operations“ ir Common Data Service kaip dvigubo rašymo sąrankos dalis.)

Patarimai: Patarimai: mes išleisime dvigubo rašymo žemėlapį visiems nuorodos duomenis, įskaitant **„Mokėjimo sąlygas“** (mokėjimo sąlygos). Jei jau turite pradinius duomenis vienoje sistemoje, mažas įrašo naujinimas gali sukelti įraše dvigubą rašymą. 

Turite vadovautis toliau pateikiama pirmumo tvarka ir užtikrinti, kad pradiniai duomenys būtų pasiekiami ir „Finance and Operations" ir „Common Data Service“.   

## <a name="vendor"></a>Tiekėjas

Tiekėjo vykdymo tvarka:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Kliento organizacija

Kliento vykdymo tvarka:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontaktinis asmuo

Kontakto vykdymo tvarka:

```
Customer
Vendor               
```
