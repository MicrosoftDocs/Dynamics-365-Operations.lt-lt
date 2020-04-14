---
title: Įjungti produktų rekomendacijas
description: Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154418"
---
# <a name="enable-product-recommendations"></a>Įjungti produktų rekomendacijas

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Rekomendacijų išankstinė patikra

Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Commerce“ klientams, perkėlusiems savo saugyklą naudoti „Azure Data Lake Storage“ (ADLS). 

Norėdami sužinoti apie veiksmus, skirtus ADLS įgalinti, žr. [Kaip įjungti ADLS „Dynamics 365“ aplinkoje](enable-ADLS-environment.md).

Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai. Norėdami sužinoti daugiau apie šį sąrankos procesą, eikite [čia.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Rekomendacijų įjungimas

Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba &gt; Produktų rekomendacijos &gt; Rekomendacijų parametrai**.
1. Bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.
1. Parinktį **Įjungti rekomendacijas** nustatykite kaip **Taip**.

![įjungti produktų rekomendacijas](./media/enableproductrecommendations.png)

> [!NOTE]
> Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą. Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.

## <a name="configure-recommendation-list-parameters"></a>Rekomendacijų sąrašo parametrų konfigūravimas

Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės. Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą. Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Rekomendacijų rodymas EKA įrenginiuose

Po to, kai bus įjungtos rekomendacijos „Commerce“ tarnybiniame biure, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį. Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Personalizuotų rekomendacijų įjungimas

Norėdami daugiau sužinoti apie tai, kaip gauti personalizuotų rekomendacijų, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[ADLS įgalinimas „Dynamics 365 Commerce” aplinkoje](enable-adls-environment.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)

