---
title: Produkto informacijos puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697870"
---
# <a name="overview-of-product-details-pages"></a>Produkto informacijos puslapių apžvalga

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.

## <a name="overview"></a>Peržiūrėti

PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą. PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.

Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.

![Produkto informacijos puslapio pavyzdys](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Antraštės ir poraštės moduliai

PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų. Puslapio apačioje yra poraštė, kurioje yra spartieji saitai su įvairiomis temomis, kurios gali sudominti klientus.

## <a name="buy-box-module"></a>Pirkimo langelio modulis

Svarbiausias PDP modulis yra pirkimo langelių modulis. Todėl jis yra pirmas pagrindinės puslapio dalies elementas. Pirkimo langelių modulis yra konteinerio modulis ir jame saugomi keli moduliai, kuriuose yra svarbiausia informacija apie produktą. Į šią informaciją įeina produkto pavadinimas, produkto atvaizdai, aprašas, kaina ir produktų įvertinimai.

Pirkimo langelių modulis leidžia klientui pasirinkti produkto parinktis (pavyzdžiui, dydžio, stiliaus ir spalvos) ir įtraukti produktą į krepšelį. Be to, juo klientas gali pirkti produktą internetu ir atsiimti jį parduotuvėje. Pirkimo internetu ir atsiėmimo parduotuvėje modulis naudoja integravimą su „Bing“ žemėlapių programos programavimo sąsajomis (API), kad būtų galima rasti netoliese esančių parduotuvių arba parduotuvių kitoje vietoje, kurią nurodo klientas.

Pirkimo langelių moduliui reikia produkto ID. Šis ID išvestas iš puslapio konteksto. Jei pirkimo langelių modulis yra įtrauktas į puslapį, kurio puslapio kontekste nėra produkto ID, jis tinkamai negeneruos informacijos.

## <a name="product-specifications-module"></a>Produkto specifikacijų modulis

Produkto specifikacijų modulį galima naudoti norint parodyti papildomą produkto informaciją. Ši išsami informacija paimama iš produkto atributų, esančių „Dynamics 365 Retail“. Produkto specifikacijų modulyje nurodomas kiekvienas atributas, kurio **matoma** ypatybė nustatyta kaip **teisinga**. Jis reikalauja, kad produkto ID gautų produkto atributus.

## <a name="recommendations-module"></a>Rekomendacijų modulis

Rekomendacijų modulis yra svarbus PDP modulis. Vartotojams naršant produktus, turi būti pateikiama daugiau produktų, kad jie galėtų rasti tinkamą produktą ir atlikti pirkimą. Rekomendacijos padeda klientams lengvai atrasti susijusį turinį ir tęsti apsipirkimą.

Galimi skirtingi rekomendacijų sąrašų tipai:

- **Žmonėms taip pat patiko** sąrašas pagrįstas mašininiu mokymu. Jam naudojama kitų klientų operacijų retrospektyvą pateikti rekomendacijų. Šį sąrašą generuoja rekomendacijų tarnyba ir primena sąrašus „Klientai, kurie pirko, taip pat pirko...“. Šiam sąrašui generuoti reikia produkto ID.
- **Susiję** sąrašą galima konfigūruoti produktui „Retail“ programoje. Pavyzdžiui, rudos odos kelioninei rankinei gali būti konfigūruojama susijusiame sąraše daugiau rankinių, kurios yra iš odos arba skirtos kelionėms. Kiti susiję sąrašai, pvz. **Papuošalai** ir **Daugiau panašių**, taip pat gali būti sukonfigūruoti „Retail“ programoje. Šiam sąrašui generuoti reikia produkto ID. Todėl, jei jis pridėtas prie pagrindinio puslapio, kuriame puslapio kontekste nėra produkto ID, sąrašas bus tuščias.
- Algoritmiškai sugeneruoti rekomendacijų sąrašai, pvz. **Populiaru**, **Perkamiausi** ir **Nauja**, galima naudoti PDP. Nors šie sąrašai gali būti tiesiogiai nesusiję su PDP produktu, jie yra dar vienas būdas padėti klientams rasti produktus, kurie gali juos dominti. Šie sąrašų tipai nereikalauja produkto ID. Jie yra bendri sąrašai, sugeneruoti pagal pirkimo tendencijas svetainėje.
- Redakciniai sąrašai yra neautomatiniu būdu kuruoti sąrašai. Pavyzdžiui, pardavėjas gali nuspręsti neautomatiniu būdu kuruoti produktų, kuriuos norima rodyti, sąrašą.

## <a name="ratings-and-reviews-module"></a>Įvertinimų ir apžvalgų modulis

Modulyje įvertinimai ir apžvalgos pateikiami įvertinimai ir apžvalgos, kuriuos pateikė kiti klientai. Jame klientai taip pat gali parašyti produkto apžvalgą. Be to, jame yra histograma, rodanti produkto įvertinimų tendenciją. Daugiau informacijos žr. [Įvertinimų ir apžvalgų apžvalga](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Rinkodaros moduliai

Jeigu rinkodaros turinys yra unikalus konkrečiam produktui, bet koks rinkodaros modulis gali būti pridėtas prie PDP. Galite įtraukti rinkodaros modulius į PDP, naudodami puslapio „papildymą“. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinio puslapio apžvalga](quick-tour-home-page.md)

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Krepšelio ir pirkimo užbaigimo puslapių apžvalga](quick-tour-cart-checkout.md)

[Paskyros valdymo puslapių apžvalga](quick-tour-account-management.md)
