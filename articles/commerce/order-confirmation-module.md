---
title: Išsamios užsakymo informacijos modulis
description: Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026022"
---
# <a name="order-details-module"></a>Išsamios užsakymo informacijos modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Išsamios užsakymo informacijos modulis pateikia užsakymo patvirtinimo informaciją. Pateikiamas užsakymo patvirtinimo ID, užsakymo kontaktinė informacija ir kita išsami informacija apie užsakymą, kaip pvz., įsigytos prekės, mokėjimo informacija ir pristatymo būdas.

## <a name="order-confirmation-module-properties"></a>Užsakymo patvirtinimo modulio ypatybės

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Užsakymo patvirtinimo modulyje gali būti antraštė. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Kontaktinis numeris | Tekstas | Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduliai, kuriuos galima naudoti užsakymo informacijos puslapyje

Kurdami išsamios užsakymo informacijos puslapį, prie užsakymo informacijos modulio galite pridėti ir kitus svarbius modulius. Štai keletas pavyzdžių:

- **Rekomendacijų modulis** – jis gali būti pridėtas prie išsamios užsakymo informacijos puslapio, kad klientui būtų pasiūlyti kiti produktai.
- **Rinkodaros moduliai** – prie išsamios užsakymo informacijos puslapio galima pridėti bet kurį rinkodaros modulį, kad būtų parodytas rinkodaros turinys.

## <a name="create-an-order-details-page-module"></a>Išsamios užsakymo informacijos puslapio modulio kūrimas

1. Sukurkite puslapio šabloną pavadinimu **Užsakymo informacijos šablonas**.
1. Prie numatytojo puslapio tarpsnio **Pagrindinis** pridėkite užsakymo informacijos modulį.
1. Prie užsakymo informacijos modulio pridėkite rekomendacijų modulį.
1. Įrašykite ir peržiūrėkite šabloną. Užsakymo informacijos modulis nebus atvaizduotas, nes tam reikalingas užsakymo patvirtinimo numerio kontekstas.
1. Baikite šablono redagavimą ir publikuokite.
1. Naudokite ką tik sukurtą užsakymo informacijos šabloną pavadinimu **Užsakymo informacijos puslapis**.
1. Pridėkite numatytąjį puslapį prie puslapio struktūros.
1. Į atkarpą **Antraštė** įtraukite antraštės fragmentą.
1. Į atkarpą **Poraštė** įtraukite poraštės fragmentą.
1. Prie tarpsnio **Pagrindinis** pridėkite užsakymo informacijos modulį.
1. Prie išsamios užsakymo informacijos modulio ypatybių srities pridėkite antraštę **Užsakymo informacija**.
1. Po užsakymo informacijos moduliu pridėkite rekomendacijų modulį ir sukonfigūruokite jį taip, kad jame būtų naudojami nustatymai **Naujas** ir **Geriausiai parduodami**.
1. Puslapį įrašykite ir peržiūrėkite.
1. Baikite puslapio redagavimą ir publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
