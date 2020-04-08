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
# <a name="enable-product-recommendations"></a><span data-ttu-id="ada6c-103">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="ada6c-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ada6c-104">Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.</span><span class="sxs-lookup"><span data-stu-id="ada6c-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ada6c-105">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ada6c-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ada6c-106">Rekomendacijų išankstinė patikra</span><span class="sxs-lookup"><span data-stu-id="ada6c-106">Recommendations pre-check</span></span>

<span data-ttu-id="ada6c-107">Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Commerce“ klientams, perkėlusiems savo saugyklą naudoti „Azure Data Lake Storage“ (ADLS).</span><span class="sxs-lookup"><span data-stu-id="ada6c-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="ada6c-108">Norėdami sužinoti apie veiksmus, skirtus ADLS įgalinti, žr. [Kaip įjungti ADLS „Dynamics 365“ aplinkoje](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ada6c-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="ada6c-109">Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="ada6c-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ada6c-110">Norėdami sužinoti daugiau apie šį sąrankos procesą, eikite [čia.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="ada6c-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="ada6c-111">Rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-111">Turn on recommendations</span></span>

<span data-ttu-id="ada6c-112">Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ada6c-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ada6c-113">Eikite į **Mažmeninė prekyba ir prekyba &gt; Produktų rekomendacijos &gt; Rekomendacijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ada6c-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="ada6c-114">Bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="ada6c-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="ada6c-115">Parinktį **Įjungti rekomendacijas** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ada6c-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![įjungti produktų rekomendacijas](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="ada6c-117">Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="ada6c-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ada6c-118">Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ada6c-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ada6c-119">Rekomendacijų sąrašo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="ada6c-120">Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ada6c-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ada6c-121">Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą.</span><span class="sxs-lookup"><span data-stu-id="ada6c-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ada6c-122">Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ada6c-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ada6c-123">Rekomendacijų rodymas EKA įrenginiuose</span><span class="sxs-lookup"><span data-stu-id="ada6c-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="ada6c-124">Po to, kai bus įjungtos rekomendacijos „Commerce“ tarnybiniame biure, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="ada6c-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ada6c-125">Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ada6c-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ada6c-126">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-126">Enable personalized recommendations</span></span>

<span data-ttu-id="ada6c-127">Norėdami daugiau sužinoti apie tai, kaip gauti personalizuotų rekomendacijų, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ada6c-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ada6c-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ada6c-128">Additional resources</span></span>

[<span data-ttu-id="ada6c-129">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ada6c-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ada6c-130">ADLS įgalinimas „Dynamics 365 Commerce” aplinkoje</span><span class="sxs-lookup"><span data-stu-id="ada6c-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ada6c-131">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ada6c-132">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="ada6c-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ada6c-133">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="ada6c-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ada6c-134">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="ada6c-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ada6c-135">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ada6c-136">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="ada6c-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ada6c-137">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="ada6c-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ada6c-138">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="ada6c-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

