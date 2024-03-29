---
title: Produkto informacijos puslapių apžvalga
description: Šiame straipsnyje pateikiama informacijos apie produktą puslapių (PDPs) apžvalga Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4856e6e208834d7dcc16d19ad4afb63c329a5868
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278506"
---
# <a name="product-details-pages-overview"></a>Produkto informacijos puslapių apžvalga

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacijos apie produktą puslapių (PDPs) apžvalga Microsoft Dynamics 365 Commerce.

PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą. PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.

Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.

![Produkto informacijos puslapio pavyzdys.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Antraštės ir poraštės moduliai

PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų. Puslapio apačioje yra poraštė, kurioje pateikiami spartieji saitai į įvairius straipsnius, kurie gali jus domina klientus.

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
