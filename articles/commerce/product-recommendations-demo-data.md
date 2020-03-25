---
title: Rekomendacijų su demonstraciniais duomenimis kūrimas
description: Šiuo dokumentu pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.
author: bebeale
manager: AnnBe
ms.date: 03/12/20
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2e790d78b4d5216822ffda3a3895feb674876bd8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127841"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="b3a21-103">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="b3a21-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b3a21-104">Šiuo dokumentu pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="b3a21-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="b3a21-105">Daugiakanalės produktų rekomendacijos pateikia atrinktų arba programiškai sugeneruotų produktų surikiuotą sąrašą.</span><span class="sxs-lookup"><span data-stu-id="b3a21-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="b3a21-106">Šiuos sąrašus galima naudoti keliuose scenarijuose, atsižvelgiant į verslo poreikį.</span><span class="sxs-lookup"><span data-stu-id="b3a21-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="b3a21-107">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b3a21-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="b3a21-108">Antros ir aukštesnių pakopų „Dynamics 365“ aplinkose produktų rekomendacijos automatiškai apskaičiuojamos pagal kliento duomenis.</span><span class="sxs-lookup"><span data-stu-id="b3a21-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="b3a21-109">Naudojant produktų rekomendacijų demonstracinius duomenis, produktų rekomendacijų sprendimas, kuris jau parengtas aplinkoje, ir išlaidos, susijusios su jo naudojimu, neišjungiamos.</span><span class="sxs-lookup"><span data-stu-id="b3a21-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="b3a21-110">Pirmos pakopos aplinkose produktų rekomendacijos yra paremtos tik statiniais demonstraciniais duomenimis, saugomais .csv faile.</span><span class="sxs-lookup"><span data-stu-id="b3a21-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="b3a21-111">Produktų rekomendacijų demonstracinių duomenų įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b3a21-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="b3a21-112">Klientai turi įdiegti „Dynamics 365 Commerce“ peržiūros demonstracinį plėtinį į atitinkamą aplinką, automatiškai įgalinančiu produktų rekomendacijų demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="b3a21-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="b3a21-113">Tai atlikus automatiškai įgalinami produkto rekomendacijų demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="b3a21-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="b3a21-114">Numatytieji demonstraciniai duomenys</span><span class="sxs-lookup"><span data-stu-id="b3a21-114">Default demo data</span></span>
<span data-ttu-id="b3a21-115">Kiekvienoje „Onebox“ tipo aplinkoje yra iš anksto įkeltų produktų rekomendacijų rinkinys, skirtas demonstraciniams duomenims, saugomiems kableliu atskirtame „reco_demo_data.csv“ faile, esančiame „Commerce Scale Unit“.</span><span class="sxs-lookup"><span data-stu-id="b3a21-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="b3a21-116">Šie duomenys suskirstyti į šiuos stulpelius.</span><span class="sxs-lookup"><span data-stu-id="b3a21-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="b3a21-117">Stulpelio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="b3a21-117">Column name</span></span>         | <span data-ttu-id="b3a21-118">Privalomas</span><span class="sxs-lookup"><span data-stu-id="b3a21-118">Mandatory</span></span>          | <span data-ttu-id="b3a21-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="b3a21-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="b3a21-120">Galimos reikšmės</span><span class="sxs-lookup"><span data-stu-id="b3a21-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b3a21-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="b3a21-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="b3a21-123">Konkretus produktų rekomendacijų sąrašo tipas, kurį turi sugeneruoti demonstracinių duomenų elementas.</span><span class="sxs-lookup"><span data-stu-id="b3a21-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="b3a21-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="b3a21-124">RecoBestSelling</span></span></li><li><span data-ttu-id="b3a21-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="b3a21-125">RecoNew</span></span></li><li><span data-ttu-id="b3a21-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="b3a21-126">RecoTrending</span></span></li><li><span data-ttu-id="b3a21-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="b3a21-127">RecoCart</span></span></li><li><span data-ttu-id="b3a21-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="b3a21-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="b3a21-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="b3a21-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="b3a21-131">Konkretus valdymo vieneto numeris, kuriame turėtų būti pateikiamos produktų rekomendacijos.</span><span class="sxs-lookup"><span data-stu-id="b3a21-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="b3a21-132">Kategorija</span><span class="sxs-lookup"><span data-stu-id="b3a21-132">Category</span></span>            |                    |    <span data-ttu-id="b3a21-133">Kategorija, kuriai turėtų būti pateiktas konkretus sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b3a21-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="b3a21-134">Jei kategorija nenurodyta, sąrašas yra skirtas tik naršymo hierarchijos viršutinei daliai.</span><span class="sxs-lookup"><span data-stu-id="b3a21-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="b3a21-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="b3a21-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="b3a21-136">Sąrašų, kuriuose reikia pateikti pirminę reikšmę (RecoPeopleAlsoBuy ir RecoCart), produktų sąraše turėtų būti rodomi papildomi produktai.</span><span class="sxs-lookup"><span data-stu-id="b3a21-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="b3a21-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="b3a21-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="b3a21-139">Vienas arba daugiau produktų, kuriuos dėl to reikia grąžinti, atskirti „;“.</span><span class="sxs-lookup"><span data-stu-id="b3a21-139">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="b3a21-140">Tinkinti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="b3a21-140">Customize demo data</span></span>
<span data-ttu-id="b3a21-141">Galite redaguoti numatytuosius demonstracinius duomenis, naudodami bet kokią produkto ir kategorijos informaciją, sukonfigūruotą būstinėje.</span><span class="sxs-lookup"><span data-stu-id="b3a21-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="b3a21-142">Atnaujinus .csv failą, klientams pateikiamose produktų rekomendacijose iš karto rodomi keitimai.</span><span class="sxs-lookup"><span data-stu-id="b3a21-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="b3a21-143">Plėtinyje yra duomenų failas, pavadintas „RecoMockDataset.csv“, kuriuo galite kontroliuoti duomenų rinkinį, naudojamą, norint gauti netikrus rekomendacijų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="b3a21-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="b3a21-144">Failo pavadinimą galima kontroliuoti naudojant plėtinio konfigūraciją ir parametrą **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="b3a21-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="b3a21-145">Tai jums leidžia turėti keletą duomenų rinkinių, kuriuos galima lengvai perjungti naudojant konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="b3a21-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="b3a21-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b3a21-146">Additional Resources</span></span>

[<span data-ttu-id="b3a21-147">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b3a21-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b3a21-148">ADLS įgalinimas „Dynamics 365 Commerce” aplinkoje</span><span class="sxs-lookup"><span data-stu-id="b3a21-148">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b3a21-149">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="b3a21-149">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b3a21-150">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="b3a21-150">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b3a21-151">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="b3a21-151">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b3a21-152">Rekomendacijų sąrašų įtraukimas į el. prekybos svetainę</span><span class="sxs-lookup"><span data-stu-id="b3a21-152">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b3a21-153">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="b3a21-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b3a21-154">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="b3a21-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b3a21-155">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="b3a21-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b3a21-156">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="b3a21-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b3a21-157">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="b3a21-157">Product recommendations FAQ</span></span>](faq-recommendations.md)
