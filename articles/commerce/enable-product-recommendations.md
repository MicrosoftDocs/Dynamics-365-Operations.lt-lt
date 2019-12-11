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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770144"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="88728-103">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="88728-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="88728-104">Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.</span><span class="sxs-lookup"><span data-stu-id="88728-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="88728-105">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="88728-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="88728-106">Rekomendacijų išankstinė patikra</span><span class="sxs-lookup"><span data-stu-id="88728-106">Recommendations pre-check</span></span>
<span data-ttu-id="88728-107">Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Finance and Operations“ klientams turintiems 10.0.6 komponavimo versiją ir perkėlusiems savo saugyklą naudoti BDL.</span><span class="sxs-lookup"><span data-stu-id="88728-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="88728-108">Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="88728-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="88728-109">Norėdami sužinoti daugiau apie šį sąrankos procesą, eikite [čia.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="88728-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="88728-110">Rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="88728-110">Turn on recommendations</span></span>

<span data-ttu-id="88728-111">Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="88728-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="88728-112">Eikite į **„Retail“** &gt; **Produktų rekomendacijos** &gt; **Rekomendacijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="88728-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="88728-113">Mažmeninės prekybos bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="88728-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="88728-114">Parinktį **Įjungti rekomendacijas** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="88728-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![įjungti produktų rekomendacijas](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="88728-116">Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="88728-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="88728-117">Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 for Commerce“.</span><span class="sxs-lookup"><span data-stu-id="88728-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="88728-118">Rekomendacijų sąrašo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="88728-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="88728-119">Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="88728-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="88728-120">Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą.</span><span class="sxs-lookup"><span data-stu-id="88728-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="88728-121">Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="88728-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="88728-122">Rekomendacijų rodymas EKA įrenginiuose</span><span class="sxs-lookup"><span data-stu-id="88728-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="88728-123">Po to, kai bus įjungtos rekomendacijos mokėjimo ir atsiskaitymo sistemose, rekomendacijos skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="88728-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="88728-124">Norėdami sužinoti apie šį procesą, eikite [čia.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="88728-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="88728-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="88728-125">Additional resources</span></span>

[<span data-ttu-id="88728-126">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="88728-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="88728-127">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="88728-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="88728-128">Rekomendacijų skydelio įtraukimas į EKA įrenginius</span><span class="sxs-lookup"><span data-stu-id="88728-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


