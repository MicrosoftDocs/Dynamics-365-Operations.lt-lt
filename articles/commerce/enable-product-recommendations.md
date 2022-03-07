---
title: Įjungti produktų rekomendacijas
description: Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466321"
---
# <a name="enable-product-recommendations"></a>Įjungti produktų rekomendacijas

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Rekomendacijų išankstinė patikra

1. Įsitikinkite, kad turite galiojančią „Dynamics 365 Commerce“ Rekomendacijų licenciją.
1. Įsitikinkite, kad objekto saugykla prijungta prie kliento „Azure Data Lake Storage“ Gen2 sąskaitos. Daugiau informacijos žr. [Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje](enable-ADLS-environment.md).
1. Patvirtinkite, kad „Azure AD” tapatybės konfigūracijoje yra rekomendacijų įrašas. Toliau pateikiama daugiau informacijos apie tai, kaip atlikti šį veiksmą.
1. Įsitikinkite, kad objekto saugyklos kasdienis „Azure Data Lake Storage“ atnaujinimas į Gen2 yra suplanuotas. Daugiau informacijos žr. [Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Įgalinkite objektų parduotuvės „RetailSale" matavimus. Norėdami sužinoti daugiau apie šį sąrankos procesą, žr. [Darbas su priemonėmis](/dynamics365/ai/customer-insights/pm-measures).

Užbaigę aukščiau aprašytus veiksmus, būsite pasiruošę įgalinti rekomendacijas.

## <a name="azure-ad-identity-configuration"></a>„Azure AD” tapatybės konfigūracija

Šis veiksmas būtinas visiems klientams, kurie naudoja infrastruktūrą kaip paslaugos (IaaS) konfigūraciją. „Azure AD“ Tapatybės konfigūracija yra automatinė klientams, kurie paleisti, bet rekomenduojama patikrinti, ar parametras „Azure Service Fabric“ sukonfigūruotas kaip tikėtasi.

### <a name="setup"></a>Sąranka

1. Programos "Commerce Headquarters" ieškokite **Azure Active Directory programų** puslapio.
1. Patikrinkite, ar yra įrašas **RecommendationSystemApplication-1**. Jei įrašo nėra, sukurkite jį naudodami šią informaciją:

    - **Kliento ID**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Pavadinimas**: RecommendationSystemApplication-1
    - **Vartotojo ID**: RetailServiceAccount

1. Įrašykite ir uždarykite puslapį. 

## <a name="turn-on-recommendations"></a>Rekomendacijų įjungimas

Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.

1. "Commerce Headquarters" ieškokite **Funkcijų valdymas**.
1. Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**. 
1. Ieškos lauke įveskite **Rekomendacijos**.
1. Pasirinkite **Produkto rekomendacijos** funkciją.
1. **Produkto rekomendacijos** srityje Ypatybės ,pasirinkite **Įgalinti dabar**.

![Rekomendacijų įjungimas.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą. Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.
> - Ši konfigūracija įgalina ne visas rekomendacijų priemones. Išplėstinės funkcijos, pvz., personalizuotos rekomendacijos, „panašus į parduotuvę" ir „parduotuvės panašios aprašymo" kontroliuojamos paskirtų funkcijų valdymo įrašais. Informacijos apie šių funkcijų įgalinimas „Commerce Headquarters", žr.  [rekomendacijas Įgalinti pritaikytu](personalized-recommendations.md), [Įgalinti „parduotuvės panašius rodinius“](shop-similar-looks.md), ir [Įgalinti „parduotuvės panašų aprašą“ rekomendacijas](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Rekomendacijų sąrašo parametrų konfigūravimas

Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės. Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą. Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Įtraukti rekomendacijas į el. komercijos patirtį

Įgalinus „Commerce Headquarters" rekomendacijas, „Commerce" moduliai, naudojami el. prekybos patirties rekomendacijų rezultatams rodyti, yra parengti konfigūruoti. Dėl daugiau informacijos, žr. [Produkto surinkimo moduliai](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Rekomendacijų rodymas EKA įrenginiuose

Po to, kai bus įjungtos rekomendacijos „Commerce“ štabe, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį. Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalizuotų rekomendacijų įjungimas

Naudojant „Microsoft Dynamics 365 Commerce“, mažmenininkai gali pritaikyti produktų rekomendacijas asmeniniams poreikiams (dar žinoma kaip suasmeninimas). Tokiu būdu asmeniniams poreikiams pritaikytos rekomendacijos gali būti įtrauktos į klientų patirtį internete ir elektroniniame kasos aparate. Įjungus suasmeninimo funkciją, sistema gali susieti vartotojo pirkinio ir produkto informaciją, kad sugeneruotų individualizuotas produkto rekomendacijas.

Norėdami daugiau sužinoti apie personalizuotas rekomendacijas, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
