---
title: Daugiakanalių produktų rekomendacijų demonstraciniai duomenys
description: Šiuo dokumentu siekiama pateikti patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872331"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="8e406-103">Daugiakanalių produktų rekomendacijų demonstraciniai duomenys</span><span class="sxs-lookup"><span data-stu-id="8e406-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="8e406-104">Šiuo dokumentu siekiama pateikti patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="8e406-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="8e406-105">Daugiakanalės produktų rekomendacijos pateikia atrinktų arba programiškai sugeneruotų užsakytų produktų surikiuotą sąrašą.</span><span class="sxs-lookup"><span data-stu-id="8e406-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="8e406-106">Šiuos sąrašus galima naudoti keliuose scenarijuose, atsižvelgiant į verslo poreikį.</span><span class="sxs-lookup"><span data-stu-id="8e406-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="8e406-107">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="8e406-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="8e406-108">Antros ir aukštesnių pakopų „Dynamics“ aplinkose produktų rekomendacijos automatiškai apskaičiuojamos pagal kliento duomenis.</span><span class="sxs-lookup"><span data-stu-id="8e406-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="8e406-109">Naudojant produktų rekomendacijų demonstracinius duomenis, produktų rekomendacijų sprendimas, kuris jau parengtas aplinkoje, ir išlaidos, susijusios su jo naudojimu, neišjungiamos.</span><span class="sxs-lookup"><span data-stu-id="8e406-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="8e406-110">Pirmos pakopos aplinkose produktų rekomendacijos yra paremtos tik statiniais demonstraciniais duomenimis, saugomais CSV faile.</span><span class="sxs-lookup"><span data-stu-id="8e406-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="8e406-111">Produktų rekomendacijų demonstracinių duomenų įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="8e406-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="8e406-112">Klientai turi įdiegti **„Dynamics 365 Commerce“ peržiūros demonstracinį plėtinį** į atitinkamą aplinką, kuris automatiškai įgalina produktų rekomendacijų demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="8e406-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="8e406-113">Numatytieji demonstraciniai duomenys</span><span class="sxs-lookup"><span data-stu-id="8e406-113">Default demo data</span></span>
<span data-ttu-id="8e406-114">Kiekviena „Onebox“ tipo aplinka pateikiama su iš anksto įkeltu produktų rekomendacijų demonstracinių duomenų rinkiniu, saugomu kableliais atskirtame faile **„reco_demo_data.csv“**, esančiame „Retail Server“, viename aplanke su šiuo dokumentu.</span><span class="sxs-lookup"><span data-stu-id="8e406-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="8e406-115">Šie duomenys suskirstyti į šiuos stulpelius</span><span class="sxs-lookup"><span data-stu-id="8e406-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="8e406-116">Stulpelio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="8e406-116">Column name</span></span>         | <span data-ttu-id="8e406-117">Privalomas</span><span class="sxs-lookup"><span data-stu-id="8e406-117">Mandatory</span></span>          | <span data-ttu-id="8e406-118">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="8e406-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="8e406-119">Galimos reikšmės</span><span class="sxs-lookup"><span data-stu-id="8e406-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8e406-120">RecoList</span><span class="sxs-lookup"><span data-stu-id="8e406-120">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="8e406-122">Konkretus produktų rekomendacijų sąrašo tipas, kurį turi sugeneruoti demonstracinių duomenų elementas.</span><span class="sxs-lookup"><span data-stu-id="8e406-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="8e406-123">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="8e406-123">RecoBestSelling</span></span></li><li><span data-ttu-id="8e406-124">RecoNew</span><span class="sxs-lookup"><span data-stu-id="8e406-124">RecoNew</span></span></li><li><span data-ttu-id="8e406-125">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="8e406-125">RecoTrending</span></span></li><li><span data-ttu-id="8e406-126">RecoCart</span><span class="sxs-lookup"><span data-stu-id="8e406-126">RecoCart</span></span></li><li><span data-ttu-id="8e406-127">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="8e406-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="8e406-128">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="8e406-128">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="8e406-130">Konkretus valdymo vieneto numeris, kuriame turėtų būti pateikiamos produktų rekomendacijos.</span><span class="sxs-lookup"><span data-stu-id="8e406-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="8e406-131">Kategorija</span><span class="sxs-lookup"><span data-stu-id="8e406-131">Category</span></span>            |                    |    <span data-ttu-id="8e406-132">Kategorija, kuriai turėtų būti pateiktas konkretus sąrašas.</span><span class="sxs-lookup"><span data-stu-id="8e406-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="8e406-133">Jei kategorija nenurodyta, sąrašas yra skirtas tik naršymo hierarchijos viršutinei daliai.</span><span class="sxs-lookup"><span data-stu-id="8e406-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="8e406-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="8e406-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="8e406-135">Sąrašų, kuriuose reikia pateikti pirminę reikšmę (RecoPeopleAlsoBuy ir RecoCart), produktų sąraše turėtų būti rodomi papildomi produktai.</span><span class="sxs-lookup"><span data-stu-id="8e406-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="8e406-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="8e406-136">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="8e406-138">Vienas arba daugiau produktų, kuriuos dėl to reikia grąžinti, atskirti **„;“**.</span><span class="sxs-lookup"><span data-stu-id="8e406-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="8e406-139">Tinkinti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="8e406-139">Customize demo data</span></span>
<span data-ttu-id="8e406-140">Klientai gali redaguoti numatytuosius demonstracinius duomenis, naudodami bet kokią produkto ir kategorijos informaciją, sukonfigūruotą būstinėje.</span><span class="sxs-lookup"><span data-stu-id="8e406-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="8e406-141">Atnaujinus CSV failą, klientams pateikiamose produktų rekomendacijose iš karto rodomi keitimai.</span><span class="sxs-lookup"><span data-stu-id="8e406-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="8e406-142">Plėtinyje yra duomenų failas, pavadintas RecoMockDataset.csv, kuri leidžia klientui kontroliuoti duomenų rinkinį, naudojamą, norint gauti netikrus rekomendacijų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="8e406-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="8e406-143">Failo pavadinimą galima kontroliuoti naudojant plėtinio konfigūraciją ir parametrą **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="8e406-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="8e406-144">Tai leidžia klientams turėti keletą duomenų rinkinių, kuriuos galima lengvai perjungti naudojant konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="8e406-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="8e406-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8e406-145">Additional resources</span></span>

[<span data-ttu-id="8e406-146">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="8e406-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="8e406-147">Aplinkos planavimas</span><span class="sxs-lookup"><span data-stu-id="8e406-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
