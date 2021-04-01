---
title: Įjungti produktų rekomendacijas
description: Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238802"
---
# <a name="enable-product-recommendations"></a>Įjungti produktų rekomendacijas

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Rekomendacijų išankstinė patikra

Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Commerce“ klientams, perkėlusiems savo saugyklą naudoti „Azure Data Lake Storage“. 

Prieš įgalinant rekomendacijas tarnybiniame biure turi būti įjungtos toliau pateiktos konfigūracijos.

1. Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje. Daugiau informacijos žr. [Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje](enable-ADLS-environment.md).
2. Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas. Daugiau informacijos žr. [Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Patvirtinkite, kad „Azure AD” tapatybės konfigūracijoje yra rekomendacijų įrašas. Toliau pateikiama daugiau informacijos apie tai, kaip atlikti šį veiksmą.

Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai. Norėdami sužinoti daugiau apie šį sąrankos procesą, žr. [Darbas su priemonėmis](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>„Azure AD” tapatybės konfigūracija

Šis veiksmas būtinas visiems klientams, kurie naudoja infrastruktūrą kaip paslaugos (IaaS) konfigūraciją. Klientams, naudojantiems „Service Fabric“ (SF), šis veiksmas turėtų būti automatinis ir rekomenduojame patikrinti, ar parametras sukonfigūruotas taip, kaip tikėtasi.

### <a name="setup"></a>Sąranka

1. Tarnybiniame biure ieškokite puslapio **„Azure Active Directory“ programos**.
2. Patikrinkite, ar yra įrašas „RecommendationSystemApplication-1”.

Jei įrašo nėra, pridėkite naują įrašą su toliau pateikta informacija.

- **Kliento ID** – d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Pavadinimas** – „RecommendationSystemApplication-1”
- **Vartotojo ID** – RetailServiceAccount

Įrašykite ir uždarykite puslapį. 

## <a name="turn-on-recommendations"></a>Rekomendacijų įjungimas

Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.

1. "Commerce Headquarters" ieškokite **Funkcijų valdymas**.
1. Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**. 
1. Ieškos lauke įveskite **Rekomendacijos**.
1. Pasirinkite **Produkto rekomendacijos** funkciją.
1. **Produkto rekomendacijos** srityje Ypatybės ,pasirinkite **Įgalinti dabar**.

![Rekomendacijų įjungimas](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą. Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.

## <a name="configure-recommendation-list-parameters"></a>Rekomendacijų sąrašo parametrų konfigūravimas

Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės. Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą. Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Rekomendacijų rodymas EKA įrenginiuose

Po to, kai bus įjungtos rekomendacijos „Commerce“ tarnybiniame biure, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį. Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md). 

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