---
title: Įjungti produktų rekomendacijas
description: Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 59d6b298896c92cbc0f6bbae17096ee1f027b922
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799160"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="ea7f1-103">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea7f1-104">Šioje temoje paaiškinama, kaip pateikti produkto rekomendacijas, paremtas dirbtinio intelekto mašininiu mokymu (AI-ML), kurį gali naudoti „Microsoft Dynamics 365 Commerce“ klientai.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="ea7f1-105">Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="ea7f1-106">Rekomendacijų išankstinė patikra</span><span class="sxs-lookup"><span data-stu-id="ea7f1-106">Recommendations pre-check</span></span>

<span data-ttu-id="ea7f1-107">Prieš įjungdami, atkreipkite dėmesį, kad produkto rekomendacijos palaikomos tik „Commerce“ klientams, perkėlusiems savo saugyklą naudoti „Azure Data Lake Storage“.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="ea7f1-108">Prieš įgalinant rekomendacijas tarnybiniame biure turi būti įjungtos toliau pateiktos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="ea7f1-109">Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="ea7f1-110">Daugiau informacijos žr. [Užtikrinkite, kad „Azure Data Lake Storage“ buvo nupirktas ir sėkmingai patikrintas aplinkoje](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="ea7f1-111">Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="ea7f1-112">Daugiau informacijos žr. [Užtikrinkite, kad objektų saugyklos atnaujinimas buvo automatizuotas](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="ea7f1-113">Patvirtinkite, kad „Azure AD” tapatybės konfigūracijoje yra rekomendacijų įrašas.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="ea7f1-114">Toliau pateikiama daugiau informacijos apie tai, kaip atlikti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="ea7f1-115">Be to, užtikrinkite, kad būtų įjungti RetailSale matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="ea7f1-116">Norėdami sužinoti daugiau apie šį sąrankos procesą, žr. [Darbas su priemonėmis](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="ea7f1-117">„Azure AD” tapatybės konfigūracija</span><span class="sxs-lookup"><span data-stu-id="ea7f1-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="ea7f1-118">Šis veiksmas būtinas visiems klientams, kurie naudoja infrastruktūrą kaip paslaugos (IaaS) konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="ea7f1-119">Klientams, naudojantiems „Service Fabric“ (SF), šis veiksmas turėtų būti automatinis ir rekomenduojame patikrinti, ar parametras sukonfigūruotas taip, kaip tikėtasi.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="ea7f1-120">Sąranka</span><span class="sxs-lookup"><span data-stu-id="ea7f1-120">Setup</span></span>

1. <span data-ttu-id="ea7f1-121">Tarnybiniame biure ieškokite puslapio **„Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="ea7f1-122">Patikrinkite, ar yra įrašas „RecommendationSystemApplication-1”.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="ea7f1-123">Jei įrašo nėra, pridėkite naują įrašą su toliau pateikta informacija.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="ea7f1-124">**Kliento ID** – d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="ea7f1-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="ea7f1-125">**Pavadinimas** – „RecommendationSystemApplication-1”</span><span class="sxs-lookup"><span data-stu-id="ea7f1-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="ea7f1-126">**Vartotojo ID** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="ea7f1-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="ea7f1-127">Įrašykite ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="ea7f1-128">Rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-128">Turn on recommendations</span></span>

<span data-ttu-id="ea7f1-129">Norėdami įjungti produktų rekomendacijas, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="ea7f1-130">"Commerce Headquarters" ieškokite **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="ea7f1-131">Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="ea7f1-132">Ieškos lauke įveskite **Rekomendacijos**.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="ea7f1-133">Pasirinkite **Produkto rekomendacijos** funkciją.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="ea7f1-134">**Produkto rekomendacijos** srityje Ypatybės ,pasirinkite **Įgalinti dabar**.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Rekomendacijų įjungimas](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="ea7f1-136">Ši procedūra paleidžia produktų rekomendacijų sąrašų generavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="ea7f1-137">Gali užtrukti iki kelių valandų, kol sąrašai bus pasiekiami ir juos bus galima matyti elektroniniame kasos aparate (EKA) arba programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="ea7f1-138">Rekomendacijų sąrašo parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="ea7f1-139">Pagal numatytuosius parametrus, AI-ML pagrįstame produktų rekomendacijų sąraše teikiamos siūlomos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="ea7f1-140">Galite keisti numatytąsias siūlomas reikšmes į atitinkančias jūsų verslo srautą.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="ea7f1-141">Norėdami daugiau sužinoti apie tai, kaip pakeisti numatytuosius parametrus, eikite į [AI-ML pagrįstų rekomendacijų rezultatų valdymas](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="ea7f1-142">Rekomendacijų rodymas EKA įrenginiuose</span><span class="sxs-lookup"><span data-stu-id="ea7f1-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="ea7f1-143">Po to, kai bus įjungtos rekomendacijos „Commerce“ tarnybiniame biure, rekomendacijų skydas turi būti pridėtas prie valdiklio EKA ekrano naudojant išdėstymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="ea7f1-144">Norėdami sužinoti apie šį procesą, žr. [Rekomendacijų valdiklio įtraukimas į EKA įrenginių operacijų ekraną](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="ea7f1-145">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-145">Enable personalized recommendations</span></span>

<span data-ttu-id="ea7f1-146">Naudojant „Microsoft Dynamics 365 Commerce“, mažmenininkai gali pritaikyti produktų rekomendacijas asmeniniams poreikiams (dar žinoma kaip suasmeninimas).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="ea7f1-147">Tokiu būdu asmeniniams poreikiams pritaikytos rekomendacijos gali būti įtrauktos į klientų patirtį internete ir elektroniniame kasos aparate.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="ea7f1-148">Įjungus suasmeninimo funkciją, sistema gali susieti vartotojo pirkinio ir produkto informaciją, kad sugeneruotų individualizuotas produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="ea7f1-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="ea7f1-149">Norėdami daugiau sužinoti apie personalizuotas rekomendacijas, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ea7f1-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea7f1-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ea7f1-150">Additional resources</span></span>

[<span data-ttu-id="ea7f1-151">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ea7f1-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ea7f1-152">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="ea7f1-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ea7f1-153">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ea7f1-154">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ea7f1-155">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ea7f1-156">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="ea7f1-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ea7f1-157">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="ea7f1-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ea7f1-158">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ea7f1-159">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="ea7f1-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ea7f1-160">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ea7f1-161">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="ea7f1-161">Product recommendations FAQ</span></span>](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]