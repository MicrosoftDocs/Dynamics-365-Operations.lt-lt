---
title: DUK apie produktų rekomendacijas
description: Šioje temoje pateikiama informacija apie procesus ir įrankius, kuriuos galite naudoti problemoms, susijusioms su produkto rekomendacijomis arba jų rezultatais, diagnozuoti.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e27e4c4d8bdf614d6f55f44daeac3bc152219004
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404307"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="73125-103">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="73125-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="73125-104">Šioje temoje pateikiama informacija apie procesus ir įrankius, kuriuos galite naudoti problemoms, susijusioms su [produkto rekomendacijomis](product-recommendations.md) arba jų rezultatais, diagnozuoti.</span><span class="sxs-lookup"><span data-stu-id="73125-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="73125-105">Geriausia praktika</span><span class="sxs-lookup"><span data-stu-id="73125-105">Best practices</span></span>
<span data-ttu-id="73125-106">Labai svarbu naudoti bendrųjų produktų ir variantų koncepciją.</span><span class="sxs-lookup"><span data-stu-id="73125-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="73125-107">Pagrįstu variantų grupavimu su pirminiaisi bendraisiais produktais galima sąrašų algoritmais ir tarnyba kurti geresnius modelius.</span><span class="sxs-lookup"><span data-stu-id="73125-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="73125-108">Be to, tarnyba gali naudoti tik vieną produkto egzempliorių, užuot naudojusi visus glaudžiai susijusius sąrašo variantus.</span><span class="sxs-lookup"><span data-stu-id="73125-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="73125-109">Kai visi artimai susiję variantai yra įtraukti į sąrašą, gali atsirasti klaidingi arba pasikartojantys rezultatai.</span><span class="sxs-lookup"><span data-stu-id="73125-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="73125-110">Kodėl mano rekomendacijų sąrašuose trūksta produktų?</span><span class="sxs-lookup"><span data-stu-id="73125-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="73125-111">Paprastai, jei produkto rekomendacijų sąraše trūksta prekės, gali kilti produkto konfigūracijos problema.</span><span class="sxs-lookup"><span data-stu-id="73125-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="73125-112">Pavyzdžiui, gali būti netinkama produkto pradžios data arba pabaigos data, dimensija gali būti netinkamai sukonfigūruota arba produktas gali būti neatitikti kanalo asortimento ir pan.</span><span class="sxs-lookup"><span data-stu-id="73125-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="73125-113">Jei nėra rekomendacijų sąrašo, kuris yra paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), elemento, jis gali neatitikti rekomendacijų sąrašo kriterijų arba, jam nepakanka pirkimo operacijų, kad būtų rodomas rekomendacijų sąraše.</span><span class="sxs-lookup"><span data-stu-id="73125-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="73125-114">Rekomenduojame patikrinkite, ar atlikti šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="73125-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="73125-115">**Įsitikinkite, ar produkto rekomendacijos buvo įjungtos BŪSTINĖJE.**</span><span class="sxs-lookup"><span data-stu-id="73125-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="73125-116">Daugiau informacijos apie tai, kaip įgalinti šią paslaugą, ieškokite [Produkto rekomendacijų įgalinimas](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="73125-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="73125-117">**Įsitikinkite, kad yra nustatytos pagrindinės produkto ypatybės.**</span><span class="sxs-lookup"><span data-stu-id="73125-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="73125-118">Pavyzdžiui, produktų asortimentai turi būti nustatyti taip, kad **įtrauktų**.</span><span class="sxs-lookup"><span data-stu-id="73125-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="73125-119">**Dėl naujai atrinktų produktų procesas gali užtrukti iki 3 valandų, kol produktas pradės būti rodomas naujame sąraše.**</span><span class="sxs-lookup"><span data-stu-id="73125-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="73125-120">**Jei produktas vis dar nerodomas sąrašuose Populiaru, Perkamiausi, Žmonėms taip pat patiko ar Dažnai kartu perkama, tada šiam produktui nepakanka operacijų.**</span><span class="sxs-lookup"><span data-stu-id="73125-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="73125-121">Tokiu atveju galite palaukti, kol atsiras daugiau operacijų, naujinti numatytuosius rekomendacijų sąrašo parametrus arba naudoti rankinį įsikišimą, kad galėtumėte modifikuoti rekomenduojamų produktų sąrašo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="73125-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="73125-122">Daugiau informacijos apie rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="73125-123">**Įsitikinkite, kad produktas atitinka rekomendacijų sąrašo kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="73125-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="73125-124">Daugiau informacijos apie produktų rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="73125-125">Kaip išvengti prastų rekomendavimo rezultatų generavimo?</span><span class="sxs-lookup"><span data-stu-id="73125-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="73125-126">Rekomendacijų sąrašams reikalingas didelis operacijų kiekis, kad būtų gaunami rezultatai.</span><span class="sxs-lookup"><span data-stu-id="73125-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="73125-127">Todėl svarbu, kad vartotojai pateiktų visus retrospektyvius operacijų duomenis.</span><span class="sxs-lookup"><span data-stu-id="73125-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="73125-128">Be to, produktai, kurie neturi operacijų ar kelių operacijų, paprastai nėra tarp **Žmonėms taip pat patiko** ar **Dažnai kartu perkama** rezultatų, tad nėra rodomi rekomendacijų sąrašuose **Populiaru** ir **Perkamiausi**.</span><span class="sxs-lookup"><span data-stu-id="73125-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="73125-129">Ši situacija dažnai gali kilti dėl labai naujų produktų arba senų produktų, kurių pirkimų skaičius yra mažas.</span><span class="sxs-lookup"><span data-stu-id="73125-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="73125-130">Populiarioms naujos prekėms ši problema greitai išnyksta.</span><span class="sxs-lookup"><span data-stu-id="73125-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="73125-131">Rekomenduojame atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="73125-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="73125-132">**Įsitikinkite, kad produktas atitinka to rekomendacijų sąrašo kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="73125-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="73125-133">Daugiau informacijos apie produktų rekomendacijų parametrus žr. AI-ML pagrįstų produktų rekomendacijų rezultatų modifikavimas.</span><span class="sxs-lookup"><span data-stu-id="73125-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="73125-134">**Jei produktas yra naujas, apsvarstykite galimybę modifikuoti rekomendacijų sąrašą, kol produktas turės daugiau operacijų.**</span><span class="sxs-lookup"><span data-stu-id="73125-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="73125-135">Daugiau informacijos apie tai, kaip modifikuoti rekomendacijų sąrašo rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="73125-136">**Įsitikinkite, kad produktas atitinka to rekomendacijų sąrašo kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="73125-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="73125-137">Daugiau informacijos apie produktų rekomendacijų parametrus žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="73125-138">**Jei produktas yra naujas, apsvarstykite galimybę modifikuoti rekomendacijų sąrašą, kol produktas turės daugiau operacijų.**</span><span class="sxs-lookup"><span data-stu-id="73125-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="73125-139">Daugiau informacijos apie tai, kaip modifikuoti rekomendacijų sąrašo rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="73125-140">Ar galiu pašalinti produktą, bet jį vis dar matys parduotuvėje?</span><span class="sxs-lookup"><span data-stu-id="73125-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="73125-141">Galite pakoreguoti sąrašus, kurie yra algoritmiškai sugeneruoti, jei atsiranda verslo poreikis.</span><span class="sxs-lookup"><span data-stu-id="73125-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="73125-142">Tačiau, jei produktas pašalinamas iš rekomendacijų sąrašo, produktas bus aptinkamas parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="73125-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="73125-143">Daugiau informacijos apie tai, kaip modifikuoti produktų rekomendacijų rezultatus, žr. [AI-ML pagrįstų produktų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="73125-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="73125-144">Jei turite užblokuoti prekę, kuri bus aptikta parduotuvėje, turite pakeisti reikšę **prekių asortimentai** į **Neįtraukti**.</span><span class="sxs-lookup"><span data-stu-id="73125-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="73125-145">Kaip pridėti sąrašą prie el. prekybos puslapio?</span><span class="sxs-lookup"><span data-stu-id="73125-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="73125-146">Norėdami gauti informacijos apie tai, kaip įtraukti produkto rekomendacijų puslapius į savo el. prekybos svetainę, žr. [Produktų rekomendacijų sąrašų įtraukimas į puslapius](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="73125-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="73125-147">Kaip įjungti EKA rekomendacijas?</span><span class="sxs-lookup"><span data-stu-id="73125-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="73125-148">Įjungus produkto rekomendacijas, prie valdiklio EKA ekrano reikės pridėti rekomendacijų skydelį.</span><span class="sxs-lookup"><span data-stu-id="73125-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="73125-149">Daugiau informacijos rasite [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="73125-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73125-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="73125-150">Additional resources</span></span>

[<span data-ttu-id="73125-151">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="73125-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="73125-152">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="73125-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="73125-153">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="73125-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="73125-154">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="73125-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="73125-155">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="73125-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="73125-156">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="73125-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="73125-157">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="73125-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="73125-158">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="73125-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="73125-159">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="73125-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="73125-160">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="73125-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
