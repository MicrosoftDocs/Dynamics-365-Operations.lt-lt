---
title: Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus
description: Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770075"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="7a750-103">Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus</span><span class="sxs-lookup"><span data-stu-id="7a750-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7a750-104">Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).</span><span class="sxs-lookup"><span data-stu-id="7a750-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="7a750-105">Įjungus produkto rekomendacijas, numatytieji parametrai įsigalios. Šie parametrai bus naudingi arba galės būti naudingi daugeliu atvejų.</span><span class="sxs-lookup"><span data-stu-id="7a750-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="7a750-106">Geriausia planuoti skirti kažkiek laiko įvertinant, ar rezultatai atitinka produktų pardavimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="7a750-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="7a750-107">Prieš vėl atliekant bandymą, rekomenduojame įvertinti kelių dienų rezultatus prieš keičiant parametrus.</span><span class="sxs-lookup"><span data-stu-id="7a750-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="7a750-108">Rekomendacijų sąrašo parametrų supratimas</span><span class="sxs-lookup"><span data-stu-id="7a750-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="7a750-109">Prieš keisdami parametrus, sužinokite, kaip jie paveiks toliau esančius rezultatus.</span><span class="sxs-lookup"><span data-stu-id="7a750-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="7a750-110">Populiariausių produktų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7a750-110">Trending product list</span></span>

<span data-ttu-id="7a750-111">Produktų sąraše **Populiaru** yra du parametrai, kuriuos galima keisti: ![Sąrašo Populiariu numatytųjų parametrų pavyzdys](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="7a750-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="7a750-112">**Įtraukti naujų produktų iš paskutinių X dienų** – produktus, įtrauktus į nurodytą dienų skaičių iki esamos datos, galima naudoti renkant produktų kandidatus.</span><span class="sxs-lookup"><span data-stu-id="7a750-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="7a750-113">Numatytoji paveikslėlio vertė rodo, kad produktai, esantys 180 dienų, gali būti naudojami populiariausių produktų sąraše.</span><span class="sxs-lookup"><span data-stu-id="7a750-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="7a750-114">**Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų.</span><span class="sxs-lookup"><span data-stu-id="7a750-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="7a750-115">Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą populiariausių produktų sąraše.</span><span class="sxs-lookup"><span data-stu-id="7a750-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="7a750-116">Perkamiausių produktų sąrašas</span><span class="sxs-lookup"><span data-stu-id="7a750-116">Best selling product list</span></span>

<span data-ttu-id="7a750-117">Atsižvelgiant į jūsų verslą, perkamiausių produktų rezultatai gali skirtis nuo populiariausių produktų, net jei abiems naudojami operacijų duomenys užsakyti produktų.</span><span class="sxs-lookup"><span data-stu-id="7a750-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="7a750-118">Kadangi perkamiausi produktai nėra atskiriami pagal asortimento datą, sąraše Perkamiausi vis tiek galima išskirti labai populiarius, senesnius produktus, kurie galbūt nebepatenka į populiariausių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="7a750-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="7a750-119">Produktų sąraše **Perkamiausi** yra vienas parametras, kurį galima pakeisti:</span><span class="sxs-lookup"><span data-stu-id="7a750-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Sąrašo Perkamiausi numatytojo parametro pavyzdys](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="7a750-121">**Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų.</span><span class="sxs-lookup"><span data-stu-id="7a750-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="7a750-122">Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą produktų sąraše Perkamiausi.</span><span class="sxs-lookup"><span data-stu-id="7a750-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="7a750-123">Produktų įtraukimas į rekomendacijų sąrašus arba pašalinimas iš jų rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="7a750-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="7a750-124">Sąrašams Nauja, Populiaru arba Perkamiausi</span><span class="sxs-lookup"><span data-stu-id="7a750-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="7a750-125">Eikite į **„Retail“** > **Produktų rekomendacijos** > **Rekomendacijų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7a750-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="7a750-126">Mažmeninės prekybos bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.</span><span class="sxs-lookup"><span data-stu-id="7a750-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="7a750-127">Pasirinkite sąrašą, į kurį įtrauksite produktus arba iš kurio juos pašalinsite.</span><span class="sxs-lookup"><span data-stu-id="7a750-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="7a750-128">Norėdami prie lentelės pridėti produktų, pasirinkite **įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="7a750-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="7a750-129">Stulpelyje Produktas suraskite produktą pagal **pavadinimą** arba **produkto numerį.**
![Produkto ieškos sąraše Nauji produktai pavyzdys](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="7a750-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="7a750-130">Stulpelyje Eilutės tipas pasirinkite vieną iš dviejų parinkčių:</span><span class="sxs-lookup"><span data-stu-id="7a750-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="7a750-131">**Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį</span><span class="sxs-lookup"><span data-stu-id="7a750-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="7a750-132">**Neįtraukti** – produktas nerodomas sąraše ![Naujų produktų sąrašo įtraukimo ir neįtraukimo pavyzdys](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="7a750-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="7a750-133">Pakeitus **Rodymo tvarka**, bus pakeista produktų žymėjimo tvarka ir sąraše pasirodys **įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7a750-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="7a750-134">Jei du produktai turi tokią pačią reikšmę **Rodymo tvarka**, tada galutinė tvarka tų dviejų rezultatų gali skirtis nuo esančios įmonės padalinyje.</span><span class="sxs-lookup"><span data-stu-id="7a750-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="7a750-135">Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="7a750-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="7a750-136">Sąrašai Žmonėms, taip pat patiko ar Dažnai kartu perkama</span><span class="sxs-lookup"><span data-stu-id="7a750-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="7a750-137">Atsižvelgiant į sąrašus **Dažnai kartu perkama** ir **Žmonės taip pat patiko**, mašininis mokymas yra naudojamas vartotojų pirkimo tendencijoms analizuoti, kad būtų rekomenduojami susiję produktai, kurie paprastai įsigijami kartu su unikaliu pradiniu produktu.</span><span class="sxs-lookup"><span data-stu-id="7a750-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="7a750-138">**Pradinis produktas** yra produktas, kuriam norite generuoti rezultatus.</span><span class="sxs-lookup"><span data-stu-id="7a750-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="7a750-139">Norėdami rankiniu būdu pakoreguoti rekomendacijų sąrašus, įtraukiate šiam produktui rezultatus arba pašalinate juos.</span><span class="sxs-lookup"><span data-stu-id="7a750-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="7a750-140">Atlikite šiuos veiksmus, kad pradiniam produktui rankiniu būdu įtrauktumėte rezultatų arba juos pašalintumėte:</span><span class="sxs-lookup"><span data-stu-id="7a750-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="7a750-141">Pasirinkite **Pradinis produktas**.</span><span class="sxs-lookup"><span data-stu-id="7a750-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="7a750-142">Stulpelyje **Produktas** ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris.**
![Produkto ieškos sąraše Dažnai kartu perkama pavyzdys](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="7a750-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="7a750-143">Stulpelyje **Eilutės tipas** pasirinkite vieną iš dviejų parinkčių:</span><span class="sxs-lookup"><span data-stu-id="7a750-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="7a750-144">**Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį</span><span class="sxs-lookup"><span data-stu-id="7a750-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="7a750-145">**Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše</span><span class="sxs-lookup"><span data-stu-id="7a750-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="7a750-146">![Produkto, esančio sąraše Dažnai kartu perkama, įtraukimo arba neįtraukimo pavyzdys](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="7a750-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="7a750-147">Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite Pašalinti.</span><span class="sxs-lookup"><span data-stu-id="7a750-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7a750-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7a750-148">Additional resources</span></span>

[<span data-ttu-id="7a750-149">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="7a750-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="7a750-150">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="7a750-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="7a750-151">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="7a750-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
