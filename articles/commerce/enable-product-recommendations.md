---
title: Įjungti produktų rekomendacijas
description: Šiame straipsnyje paaiškinama, kaip pateikti produktų rekomendacijas, pagrįstas klientų tyrimų– įrenginių mokymosi (AI-AIF) Microsoft Dynamics 365 Commerce rezultatais.
author: bebeale
ms.date: 09/08/2022
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
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460027"
---
# <a name="enable-product-recommendations"></a>Įjungti produktų rekomendacijas

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip pateikti produktų rekomendacijas, pagrįstas klientų tyrimų– įrenginių mokymosi (AI-AIF) Microsoft Dynamics 365 Commerce rezultatais. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Rekomendacijų išankstinė patikra

1. Įsitikinkite, kad turite galiojančią „Dynamics 365 Commerce“ Rekomendacijų licenciją.
1. Įsitikinkite, kad objekto saugykla prijungta prie kliento „Azure Data Lake Storage“ Gen2 sąskaitos. Daugiau informacijos žr. [Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje](enable-ADLS-environment.md).
1. Patvirtinkite, kad „Azure AD” tapatybės konfigūracijoje yra rekomendacijų įrašas. Toliau pateikiama daugiau informacijos apie tai, kaip atlikti šį veiksmą.
1. Įsitikinkite, kad objekto saugyklos kasdienis „Azure Data Lake Storage“ atnaujinimas į Gen2 yra suplanuotas. Daugiau informacijos žr. [Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Įgalinkite objektų parduotuvės „RetailSale" matavimus. Norėdami sužinoti daugiau apie šį sąrankos procesą, žr. [Darbas su priemonėmis](/dynamics365/ai/customer-insights/pm-measures).
1. Įsitikinkite, kad jūsų aplinka sukonfigūravo jau palaikomuose regionuose, kuriuose palaikomi regionai, pavyzdžiui:

    - **Palaikomi rodyti regionai:** EU/US/CA/AU.
    - **Palaikomi regionuose regionuose:** JAV / CA / AU. Jei esantys regionai neatitinka vieno iš esamų palaikomų regionų, rekomendacijų tarnyba parinks artimiausią palaikomą regioną.

Užbaigę aukščiau aprašytus veiksmus, būsite pasiruošę įgalinti rekomendacijas.

> [!NOTE]
> Yra žinoma problema, kai rekomendacijos nepasirodo po to, kai šie veiksmai yra atlikti. Ši problema kyla dėl duomenų srauto problemų aplinkoje. Jei jūsų aplinkoje nerodyti rekomendacijų rezultatų, [sukonfigūruokite alternatyvius rekomendacijų paslaugos duomenis, atlikite veiksmus, aprašytus nustatyti alternatyvų rekomendacijų duomenų srautą](set-up-alternate-data-flow.md). Norėdami atlikti šiuos veiksmus turite turėti "Azure" administratoriaus teises. Jei jums reikia pagalbos, susisiekite su savo FastTrack atstovu.

## <a name="azure-ad-identity-configuration"></a>„Azure AD” tapatybės konfigūracija

Šis veiksmas būtinas tik klientams, kurie vykdo infrastruktūrą kaip paslaugos (IaaS) konfigūraciją. Azure AD tapatybės konfigūracija yra automatinė klientams, kurie paleidžia Azure Service Fabric programą, bet mes rekomenduojame patikrinti, ar parametras sukonfigūruotas kaip tikėtasi.

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

[Nustatyti alternatyvų rekomendacijų duomenų srautą](set-up-alternate-data-flow.md)

[Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas](personalized-recommendations.md)

[Įjungti „pirkti panašios išvaizdos“ rekomendacijas](shop-similar-looks.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
