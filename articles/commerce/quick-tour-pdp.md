---
title: Produktų informacijos puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3a1fbd6a71c8d00e862183c32fb9f7e17dcc5bd1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351993"
---
# <a name="product-details-pages-overview"></a>Produkto informacijos puslapių apžvalga

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.

PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą. PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.

Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.

![Produkto informacijos puslapio pavyzdys.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Antraštės ir poraštės moduliai

PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų. Puslapio apačioje yra poraštė, kurioje yra spartieji saitai su įvairiomis temomis, kurios gali sudominti klientus.

## <a name="buy-box-module"></a>Pirkimo langelio modulis

Svarbiausias PDP modulis yra pirkimo langelio modulis, kuris pasirodo kaip pirmasis elementas pagrindinėje puslapio dalyje. Pirkimo langelių modulyje rodoma svarbi informacija apie produktą, kaip pavyzdžiui, produkto pavadinimas, produkto aprašymas, produkto kaina, produkto nuotraukos ir produkto įvertinimas.

Pirkimo langelių modulis leidžia klientui pasirinkti produkto parinktis (pavyzdžiui, dydžio, stiliaus ir spalvos) ir įtraukti produktą į krepšelį. Be to, juo klientas gali pirkti produktą internetu ir atsiimti jį parduotuvėje. Pirkimo internetu ir atsiėmimo parduotuvėje modulis naudoja integravimą su „Bing“ žemėlapių programos programavimo sąsajomis (API), kad būtų galima rasti netoliese esančių parduotuvių arba parduotuvių kitoje vietoje, kurią nurodo klientas.

Pirkimo langelių moduliui reikia produkto ID. Šis ID išvestas iš puslapio konteksto. Jei pirkimo langelių modulis yra įtrauktas į puslapį, kurio puslapio kontekste nėra produkto ID, jis tinkamai negeneruos informacijos.

## <a name="product-specifications-module"></a>Produkto specifikacijų modulis

Produkto specifikacijų modulį galima naudoti norint parodyti papildomą produkto informaciją. Ši informacija yra paimta iš produkto atributų, esančių „Commerce“. Produkto specifikacijų modulyje nurodomas kiekvienas atributas, kurio **matoma** ypatybė nustatyta kaip **teisinga**. Jis reikalauja, kad produkto ID gautų produkto atributus.

## <a name="recommendations-module"></a>Rekomendacijų modulis

Rekomendacijų modulis yra svarbus PDP modulis. Vartotojams naršant produktus, turi būti pateikiama daugiau produktų, kad jie galėtų rasti tinkamą produktą ir atlikti pirkimą. Rekomendacijos padeda klientams lengvai atrasti susijusį turinį ir tęsti apsipirkimą.

Galimi skirtingi rekomendacijų sąrašų tipai:

- **Žmonėms taip pat patiko** sąrašas pagrįstas mašininiu mokymu. Jam naudojama kitų klientų operacijų retrospektyvą pateikti rekomendacijų. Šį sąrašą generuoja rekomendacijų tarnyba ir primena sąrašus „Klientai, kurie pirko, taip pat pirko...“. Šiam sąrašui generuoti reikia produkto ID.
- **„Susiję“** sąrašą galima sukonfigūruoti „Commerce“ produktui. Pavyzdžiui, rudos odos kelioninei rankinei gali būti konfigūruojama susijusiame sąraše daugiau rankinių, kurios yra iš odos arba skirtos kelionėms. Kitų tipų susijusius sąrašus, tokius kaip **Aksesuarai** ir **Daugiau panašių**, taip pat galima sukonfigūruoti „Commerce“. Šiam sąrašui generuoti reikia produkto ID. Todėl, jei jis pridėtas prie pagrindinio puslapio, kuriame puslapio kontekste nėra produkto ID, sąrašas bus tuščias.
- Algoritmiškai sugeneruoti rekomendacijų sąrašai, pvz. **Populiaru**, **Perkamiausi** ir **Nauja**, galima naudoti PDP. Nors šie sąrašai gali būti tiesiogiai nesusiję su PDP produktu, jie yra dar vienas būdas padėti klientams rasti produktus, kurie gali juos dominti. Šie sąrašų tipai nereikalauja produkto ID. Jie yra bendri sąrašai, sugeneruoti pagal pirkimo tendencijas svetainėje.
- Redakciniai sąrašai yra neautomatiniu būdu kuruoti sąrašai. Pavyzdžiui, pardavėjas gali nuspręsti neautomatiniu būdu kuruoti produktų, kuriuos norima rodyti, sąrašą.

## <a name="ratings-and-reviews-modules"></a>Įvertinimų ir apžvalgų moduliai

Norint parodyti ir pridėti apžvalgas, gali būti naudojami trys moduliai.

- **Apžvalgos** – šiame modulyje pateikiami įvertinimai ir apžvalgos, kuriuos pateikė kiti klientai. Klientai gali rūšiuoti ir filtruoti apžvalgas. Šis modulis taip pat leidžia klientams pamėgti ar nepamėgti apžvalgas ir pranešti apie problemas.
- **Rašyti apžvalgą** – šis modulis leidžia klientams parašyti savo apžvalgą apie produktą.
- **Įvertinimo histograma** – šiame modulyje yra histograma, rodanti produkto įvertinimo tendencijas.

Daugiau informacijos žr. [Įvertinimų ir apžvalgų apžvalga](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Rinkodaros moduliai

Jeigu rinkodaros turinys yra unikalus konkrečiam produktui, bet koks rinkodaros modulis gali būti pridėtas prie PDP. Galite įtraukti rinkodaros modulius į PDP, naudodami puslapio „papildymą“. Norėdami gauti išsamesnės informacijos, žr. [„Papildyti produkto puslapį“](enrich-product-page.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Pagrindinio puslapio apžvalga](quick-tour-home-page.md)

[Krepšelio ir pirkimo užbaigimo puslapių apžvalga](quick-tour-cart-checkout.md)

[Paskyrų tvarkymo puslapių apžvalga](quick-tour-account-management.md)

[„Papildyti produkto aprašymo puslapį“.](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
