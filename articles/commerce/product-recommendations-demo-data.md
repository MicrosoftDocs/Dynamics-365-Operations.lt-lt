---
title: Gaukite produktų rekomendacijas, naudodami demonstracinius duomenis
description: Šiuo dokumentu pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
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
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042785"
---
# <a name="get-product-recommendations-using-demo-data"></a><span data-ttu-id="ac4f1-103">Gaukite produktų rekomendacijas, naudodami demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="ac4f1-103">Get product recommendations using demo data</span></span>
<span data-ttu-id="ac4f1-104">Šiuo dokumentu pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-104">This document provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="ac4f1-105">Daugiakanalės produktų rekomendacijos pateikia atrinktų arba programiškai sugeneruotų produktų surikiuotą sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="ac4f1-106">Šiuos sąrašus galima naudoti keliuose scenarijuose, atsižvelgiant į verslo poreikį.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="ac4f1-107">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ac4f1-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="ac4f1-108">Antros ir aukštesnių pakopų „Dynamics 365“ aplinkose produktų rekomendacijos automatiškai apskaičiuojamos pagal kliento duomenis.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="ac4f1-109">Naudojant produktų rekomendacijų demonstracinius duomenis, produktų rekomendacijų sprendimas, kuris jau parengtas aplinkoje, ir išlaidos, susijusios su jo naudojimu, neišjungiamos.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="ac4f1-110">Pirmos pakopos aplinkose produktų rekomendacijos yra paremtos tik statiniais demonstraciniais duomenimis, saugomais .csv faile.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="ac4f1-111">Produktų rekomendacijų demonstracinių duomenų įgalinimas aplinkoje</span><span class="sxs-lookup"><span data-stu-id="ac4f1-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="ac4f1-112">Klientai turi įdiegti „Dynamics 365 Commerce“ peržiūros demonstracinį plėtinį į atitinkamą aplinką, automatiškai įgalinančiu produktų rekomendacijų demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-112">To enable product recommensations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="ac4f1-113">Tai atlikus automatiškai įgalinami produkto rekomendacijų demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="ac4f1-114">Numatytieji demonstraciniai duomenys</span><span class="sxs-lookup"><span data-stu-id="ac4f1-114">Default demo data</span></span>
<span data-ttu-id="ac4f1-115">Kiekvienoje „Onebox“ tipo aplinkoje yra iš anksto įkeltų produktų rekomendacijų rinkinys, skirtas demonstraciniams duomenims, saugomiems kableliu atskirtame „reco_demo_data.csv“ faile, esančiame „Commerce Scale Unit“.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-115">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated ‘reco_demo_data.csv’ file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="ac4f1-116">Šie duomenys suskirstyti į šiuos stulpelius.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="ac4f1-117">Stulpelio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ac4f1-117">Column name</span></span>         | <span data-ttu-id="ac4f1-118">Privalomas</span><span class="sxs-lookup"><span data-stu-id="ac4f1-118">Mandatory</span></span>          | <span data-ttu-id="ac4f1-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="ac4f1-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="ac4f1-120">Galimos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ac4f1-120">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ac4f1-121">RecoList</span><span class="sxs-lookup"><span data-stu-id="ac4f1-121">RecoList</span></span>            | :heavy_check_mark: | <span data-ttu-id="ac4f1-123">Konkretus produktų rekomendacijų sąrašo tipas, kurį turi sugeneruoti demonstracinių duomenų elementas.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="ac4f1-124">RecoBestSelling</span><span class="sxs-lookup"><span data-stu-id="ac4f1-124">RecoBestSelling</span></span></li><li><span data-ttu-id="ac4f1-125">RecoNew</span><span class="sxs-lookup"><span data-stu-id="ac4f1-125">RecoNew</span></span></li><li><span data-ttu-id="ac4f1-126">RecoTrending</span><span class="sxs-lookup"><span data-stu-id="ac4f1-126">RecoTrending</span></span></li><li><span data-ttu-id="ac4f1-127">RecoCart</span><span class="sxs-lookup"><span data-stu-id="ac4f1-127">RecoCart</span></span></li><li><span data-ttu-id="ac4f1-128">RecoPeopleAlsoBuy</span><span class="sxs-lookup"><span data-stu-id="ac4f1-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="ac4f1-129">OperatingUnitNumber</span><span class="sxs-lookup"><span data-stu-id="ac4f1-129">OperatingUnitNumber</span></span> | :heavy_check_mark: | <span data-ttu-id="ac4f1-131">Konkretus valdymo vieneto numeris, kuriame turėtų būti pateikiamos produktų rekomendacijos.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="ac4f1-132">Kategorija</span><span class="sxs-lookup"><span data-stu-id="ac4f1-132">Category</span></span>            |                    |    <span data-ttu-id="ac4f1-133">Kategorija, kuriai turėtų būti pateiktas konkretus sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="ac4f1-134">Jei kategorija nenurodyta, sąrašas yra skirtas tik naršymo hierarchijos viršutinei daliai.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="ac4f1-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="ac4f1-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="ac4f1-136">Sąrašų, kuriuose reikia pateikti pirminę reikšmę (RecoPeopleAlsoBuy ir RecoCart), produktų sąraše turėtų būti rodomi papildomi produktai.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="ac4f1-137">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ac4f1-137">ItemIds</span></span>             | :heavy_check_mark: | <span data-ttu-id="ac4f1-139">Vienas arba daugiau produktų, kuriuos dėl to reikia grąžinti, atskirti „;“.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-139">One or more products to be returned as the result, separated by ‘;’.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="ac4f1-140">Tinkinti demonstracinius duomenis</span><span class="sxs-lookup"><span data-stu-id="ac4f1-140">Customize demo data</span></span>
<span data-ttu-id="ac4f1-141">Galite redaguoti numatytuosius demonstracinius duomenis, naudodami bet kokią produkto ir kategorijos informaciją, sukonfigūruotą būstinėje.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-141">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="ac4f1-142">Atnaujinus .csv failą, klientams pateikiamose produktų rekomendacijose iš karto rodomi keitimai.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-142">Once you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="ac4f1-143">Plėtinyje yra duomenų failas, pavadintas „RecoMockDataset.csv“, kuriuo galite kontroliuoti duomenų rinkinį, naudojamą, norint gauti netikrus rekomendacijų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-143">The extension contains a datafile called 'RecoMockDataset.csv' which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="ac4f1-144">Failo pavadinimą galima kontroliuoti naudojant plėtinio konfigūraciją ir parametrą **ext.Recommendations.DemoFilePath**.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-144">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="ac4f1-145">Tai jums leidžia turėti keletą duomenų rinkinių, kuriuos galima lengvai perjungti naudojant konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="ac4f1-145">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="ac4f1-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ac4f1-146">Additional Resources</span></span>

[<span data-ttu-id="ac4f1-147">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ac4f1-147">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ac4f1-148">Aplinkos planavimas</span><span class="sxs-lookup"><span data-stu-id="ac4f1-148">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
