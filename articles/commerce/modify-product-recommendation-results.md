---
title: DI-MM pagrįstų produktų rekomendacijų rezultatų koregavimas
description: Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfe04881e71558ed326025d8f2545c3c611df3aa
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796975"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="d88f0-103">DI-MM pagrįstų produktų rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="d88f0-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d88f0-104">Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).</span><span class="sxs-lookup"><span data-stu-id="d88f0-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="d88f0-105">Įjungus produkto rekomendacijas, numatytieji parametrai įsigalios. Šie parametrai bus naudingi arba galės būti naudingi daugeliu atvejų.</span><span class="sxs-lookup"><span data-stu-id="d88f0-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="d88f0-106">Geriausia planuoti skirti kažkiek laiko įvertinant, ar rezultatai atitinka produktų pardavimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="d88f0-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="d88f0-107">Prieš vėl atliekant bandymą, rekomenduojame įvertinti kelių dienų rezultatus prieš keičiant parametrus.</span><span class="sxs-lookup"><span data-stu-id="d88f0-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="d88f0-108">Rekomendacijų sąrašo parametrų supratimas</span><span class="sxs-lookup"><span data-stu-id="d88f0-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="d88f0-109">Prieš keisdami parametrus, sužinokite, kaip jie paveiks toliau esančius rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d88f0-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="d88f0-110">Produktų sąrašas „Populiariausi“</span><span class="sxs-lookup"><span data-stu-id="d88f0-110">"Trending" product list</span></span>

<span data-ttu-id="d88f0-111">Produktų sąraše „Populiariausi“ galima pakeisti du parametrus.</span><span class="sxs-lookup"><span data-stu-id="d88f0-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Sąrašo „Populiariausi“ numatytųjų parametrų pavyzdys](./media/exampletrendingparameters.png)

1. <span data-ttu-id="d88f0-113">**Įtraukti naujų produktų iš paskutinių X dienų** – produktus, įtrauktus į nurodytą dienų skaičių iki esamos datos, galima naudoti renkant produktų kandidatus.</span><span class="sxs-lookup"><span data-stu-id="d88f0-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="d88f0-114">Numatytoji paveikslėlio vertė rodo, kad produktai, esantys 180 dienų, gali būti naudojami populiariausių produktų sąraše.</span><span class="sxs-lookup"><span data-stu-id="d88f0-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="d88f0-115">**Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų.</span><span class="sxs-lookup"><span data-stu-id="d88f0-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="d88f0-116">Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą populiariausių produktų sąraše.</span><span class="sxs-lookup"><span data-stu-id="d88f0-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="d88f0-117">Produktų sąrašas „Geriausiai parduodami“</span><span class="sxs-lookup"><span data-stu-id="d88f0-117">"Best selling" product list</span></span>

<span data-ttu-id="d88f0-118">Atsižvelgiant į jūsų verslą, sąrašas „Geriausiai parduodami“ gali duoti kitokių rezultatų nei „Populiariausi“, net jei jie abu užsako produktus naudodamiesi operacijų duomenimis.</span><span class="sxs-lookup"><span data-stu-id="d88f0-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="d88f0-119">Kadangi perkamiausi produktai nėra atskiriami pagal asortimento datą, sąraše Perkamiausi vis tiek galima išskirti labai populiarius, senesnius produktus, kurie galbūt nebepatenka į populiariausių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d88f0-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="d88f0-120">„Populiariausi“ produktų sąraše galima pakeisti vieną parametrą.</span><span class="sxs-lookup"><span data-stu-id="d88f0-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Sąrašo Perkamiausi numatytojo parametro pavyzdys](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="d88f0-122">**Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų.</span><span class="sxs-lookup"><span data-stu-id="d88f0-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="d88f0-123">Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą produktų sąraše Perkamiausi.</span><span class="sxs-lookup"><span data-stu-id="d88f0-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="d88f0-124">Produktų įtraukimas į rekomendacijų sąrašus arba pašalinimas iš jų rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="d88f0-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="d88f0-125">Sąrašai „Naujas“, „Populiariausi“ arba „Geriausiai parduodami“</span><span class="sxs-lookup"><span data-stu-id="d88f0-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="d88f0-126">Eikite į **Mažmeninė prekyba ir komercija** > **Produkto rekomendacijos** > **Rekomendacijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="d88f0-127">Bendrinamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="d88f0-128">Pasirinkite sąrašą, į kurį įtrauksite produktus arba iš kurio juos pašalinsite.</span><span class="sxs-lookup"><span data-stu-id="d88f0-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="d88f0-129">Norėdami prie lentelės pridėti produktų, pasirinkite **įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="d88f0-130">Stulpelyje Produktas ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Produkto paieškos sąraše „Nauji produktai“ pavyzdys](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="d88f0-132">Stulpelyje Eilutės tipas pasirinkite vieną iš dviejų parinkčių:</span><span class="sxs-lookup"><span data-stu-id="d88f0-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="d88f0-133">**Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį</span><span class="sxs-lookup"><span data-stu-id="d88f0-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="d88f0-134">**Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše</span><span class="sxs-lookup"><span data-stu-id="d88f0-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Produkto įtraukimo arba neįtraukimo į sąrašą „Nauji produktai“ pavyzdys](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="d88f0-136">Pakeitus **Rodymo tvarka**, bus pakeista produktų žymėjimo tvarka ir sąraše pasirodys **įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="d88f0-137">Jei du produktai turi tokią pačią reikšmę **Rodymo tvarka**, tada galutinė tvarka tų dviejų rezultatų gali skirtis nuo esančios įmonės padalinyje.</span><span class="sxs-lookup"><span data-stu-id="d88f0-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="d88f0-138">Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="d88f0-139">Sąrašai „Žmonėms taip pat patiko“ arba „Kartu taip pat perkama“</span><span class="sxs-lookup"><span data-stu-id="d88f0-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="d88f0-140">Sąrašuose „Kartu taip pat perkama“ arba „Žmonėms taip pat patiko“ naudojamas mašininis mokymas, kuris išanalizuoja vartotojų pirkimo elgseną, kad būtų galima rekomenduoti su pradiniu produktu susijusius produktus, paprastai įsigyjamus kartu.</span><span class="sxs-lookup"><span data-stu-id="d88f0-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="d88f0-141">*Pradinis produktas* yra produktas, kuriam norite generuoti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d88f0-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="d88f0-142">Norėdami rankiniu būdu pakoreguoti rekomendacijų sąrašus, įtraukiate šiam produktui rezultatus arba pašalinate juos.</span><span class="sxs-lookup"><span data-stu-id="d88f0-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="d88f0-143">Atlikite šiuos veiksmus, kad pradiniam produktui rankiniu būdu įtrauktumėte rezultatų arba juos pašalintumėte:</span><span class="sxs-lookup"><span data-stu-id="d88f0-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="d88f0-144">Pasirinkite **Pradinis produktas**.</span><span class="sxs-lookup"><span data-stu-id="d88f0-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="d88f0-145">Stulpelyje **Produktas** ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris.**
![Produkto ieškos sąraše Dažnai kartu perkama pavyzdys](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="d88f0-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="d88f0-146">Stulpelyje **Eilutės tipas** pasirinkite vieną iš dviejų parinkčių:</span><span class="sxs-lookup"><span data-stu-id="d88f0-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="d88f0-147">**Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį</span><span class="sxs-lookup"><span data-stu-id="d88f0-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="d88f0-148">**Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše</span><span class="sxs-lookup"><span data-stu-id="d88f0-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="d88f0-149">![Produkto, esančio sąraše Dažnai kartu perkama, įtraukimo arba neįtraukimo pavyzdys](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="d88f0-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="d88f0-150">Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite Pašalinti.</span><span class="sxs-lookup"><span data-stu-id="d88f0-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d88f0-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d88f0-151">Additional resources</span></span>

[<span data-ttu-id="d88f0-152">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d88f0-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d88f0-153">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="d88f0-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d88f0-154">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d88f0-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d88f0-155">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="d88f0-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d88f0-156">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="d88f0-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d88f0-157">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d88f0-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="d88f0-158">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="d88f0-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d88f0-159">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="d88f0-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d88f0-160">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="d88f0-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d88f0-161">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="d88f0-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d88f0-162">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d88f0-162">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]