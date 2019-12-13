---
title: Užsakymo patvirtinimo modulis
description: Ši tema apima užsakymo patvirtinimo modulius ir joje aprašoma, kaip juos sukurti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698331"
---
# <a name="order-confirmation-module"></a>Užsakymo patvirtinimo modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Ši tema apima užsakymo patvirtinimo modulius ir joje aprašoma, kaip juos sukurti programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Užsakymo patvirtinimo modulis naudojamas rodyti patvirtinimo pranešimą užsakymo patvirtinimo puslapyje, kai pateikiamas užsakymas. Užsakymo patvirtinimo modulis nurodo užsakymo patvirtinimo numerį ir kliento el. pašto adresą, kuris buvo pateiktas užbaigiant pirkimą.

Kai užsakymas pateikiamas užbaigiant pirkimą, užsakymo patvirtinimo numeris ir kliento el. pašto adresas perduodami į užsakymo patvirtinimo puslapį kaip užklausos eilutė, esanti puslapio URL. Užsakymo patvirtinimo modulis gauna šią informaciją ir užsakymo patvirtinimo puslapyje sugeneruoja užsakymo būseną. Užsakymo patvirtinimo modulyje reikalingas šio puslapio kontekstas, kad būtų pateikta užsakymo būsena.

## <a name="order-confirmation-module-properties"></a>Užsakymo patvirtinimo modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašymas |
|---------------|--------|-------------|
| Antraštė       | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Užsakymo patvirtinimo modulyje gali būti antraštė. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduliai, kuriuos galima naudoti užsakymo patvirtinimo puslapio modulyje 

- **Rekomendacijos** – rekomendacijų modulį galima įtraukti į užsakymo patvirtinimo puslapį, kad klientas galėtų siūlyti kitus produktus.
- **Rinkodara** – rinkodaros modulis gali pridėti rinkodaros turinį į užsakymo patvirtinimo puslapį.

## <a name="create-an-order-confirmation-page-module"></a>Užsakymo patvirtinimo puslapio modulio kūrimas

1. Sukurkite puslapio šabloną, pavadintą **užsakymo patvirtinimo šablonas**.
1. Numatytojo puslapio atkarpoje **Pagrindinis** įtraukite užsakymo patvirtinimo modulį.
1. Užsakymo patvirtinimo modulyje pridėkite rekomendacijų modulį.
1. Įrašykite ir peržiūrėkite šabloną. Užsakymo patvirtinimo modulis negali būti atvaizduotas, nes jam reikia užsakymo patvirtinimo numerio konteksto.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami užsakymo patvirtinimo šabloną, sukurkite puslapį, pavadintą **Užsakymo patvirtinimo puslapis**.
1. Pridėkite numatytąjį puslapį prie puslapio struktūros.
1. Į atkarpą **Antraštė** įtraukite antraštės fragmentą.
1. Į atkarpą **Poraštė** įtraukite poraštės fragmentą.
1. Atkarpoje **Pagrindinis** įtraukite užsakymo patvirtinimo modulį.
1. Užsakymo patvirtinimo modulio ypatybių srityje įtraukite antraštę **Užsakymo patvirtinimas**.
1. Po užsakymo patvirtinimo moduliu įtraukite rekomendacijų modulį ir sukonfigūruokite taip, kad jis naudotų parametrus **Nauja** ir **Perkamiausi**.
1. Puslapį įrašykite ir peržiūrėkite, įrašykite ir atrakinkite bei jį publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
