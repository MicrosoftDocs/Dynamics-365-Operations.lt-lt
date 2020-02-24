---
title: Įjungti produktų rekomendacijas
description: Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024961"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="d1a99-103">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d1a99-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d1a99-104">Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.</span><span class="sxs-lookup"><span data-stu-id="d1a99-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="d1a99-105">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d1a99-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="d1a99-106">Rekomendacijų išankstinė patikra</span><span class="sxs-lookup"><span data-stu-id="d1a99-106">Recommendations pre-check</span></span>

<span data-ttu-id="d1a99-107">Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Commerce“ klientams, perkėlusiems savo saugyklą naudoti „Azure Data Lake Storage“ (ADLS).</span><span class="sxs-lookup"><span data-stu-id="d1a99-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="d1a99-108">Norėdami sužinoti apie veiksmus, skirtus ADLS įgalinti, žr. [Kaip įjungti ADLS „Dynamics 365“ aplinkoje](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d1a99-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="d1a99-109">Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="d1a99-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="d1a99-110">Norėdami sužinoti daugiau apie šį sąrankos procesą, eikite [čia.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="d1a99-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="d1a99-111">Rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="d1a99-111">Turn on recommendations</span></span>

<span data-ttu-id="d1a99-112">Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d1a99-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="d1a99-113">Eikite į **Mažmeninė prekyba ir prekyba &gt; Produktų rekomendacijos &gt; Rekomendacijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d1a99-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="d1a99-114">Bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="d1a99-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="d1a99-115">Parinktį **Įjungti rekomendacijas** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d1a99-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![įjungti produktų rekomendacijas](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="d1a99-117">Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="d1a99-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="d1a99-118">Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="d1a99-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="d1a99-119">Rekomendacijų sąrašo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d1a99-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="d1a99-120">Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="d1a99-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="d1a99-121">Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą.</span><span class="sxs-lookup"><span data-stu-id="d1a99-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="d1a99-122">Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="d1a99-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="d1a99-123">Rekomendacijų rodymas EKA įrenginiuose</span><span class="sxs-lookup"><span data-stu-id="d1a99-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="d1a99-124">Po to, kai bus įjungtos rekomendacijos „Commerce“ tarnybiniame biure, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="d1a99-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="d1a99-125">Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="d1a99-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="d1a99-126">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="d1a99-126">Enable personalized recommendations</span></span>

<span data-ttu-id="d1a99-127">Norėdami daugiau sužinoti apie tai, kaip gauti personalizuotų rekomendacijų, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d1a99-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1a99-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d1a99-128">Additional resources</span></span>

[<span data-ttu-id="d1a99-129">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d1a99-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d1a99-130">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="d1a99-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d1a99-131">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="d1a99-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d1a99-132">Rekomendacijų skydelio įtraukimas į EKA įrenginius</span><span class="sxs-lookup"><span data-stu-id="d1a99-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d1a99-133">Produktų rinkinio modulio peržiūra</span><span class="sxs-lookup"><span data-stu-id="d1a99-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="d1a99-134">ADLS įgalinimas „Dynamics 365“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="d1a99-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

