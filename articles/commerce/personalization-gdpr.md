---
title: Atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų
description: Šioje temoje pateikiama informacija, kaip galite leisti klientams atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų, naudojant „Microsoft Dynamics 365 Commerce“.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e65fc54f87664caec95b2bc2c579d0820ae08c0f
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477689"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="3db25-103">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="3db25-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3db25-104">Šioje temoje pateikiama informacija, kaip galite leisti klientams atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3db25-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3db25-105">Kuriant paskyrą, nauji klientai automatiškai gauna asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="3db25-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="3db25-106">Tačiau „Dynamics 365 Commerce“ siūlo įvairius būdus, kaip mažmenininkams leisti vartotojams atsisakyti gauti šias rekomendacijas ir apriboti jų asmeninių duomenų tvarkymą.</span><span class="sxs-lookup"><span data-stu-id="3db25-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="3db25-107">Autentifikuoti vartotojai, kurie atsisako gauti asmeniniams poreikiams pritaikytas rekomendacijas, iškart nustos matyti asmeniniams poreikiams pritaikytus sąrašus.</span><span class="sxs-lookup"><span data-stu-id="3db25-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="3db25-108">Be to, visi asmeniniai duomenys, kurie renkami asmeninių poreikių pritaikymui, bus pašalinti iš asmeniniams poreikiams pritaikytų rekomendacijų modelių.</span><span class="sxs-lookup"><span data-stu-id="3db25-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="3db25-109">Norėdami gauti daugiau informacijos apie asmeniniams poreikiams pritaikytas produkto rekomendacijas, žr. [Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3db25-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="3db25-110">Būdai, kaip mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų</span><span class="sxs-lookup"><span data-stu-id="3db25-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="3db25-111">Mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų trimis būdais.</span><span class="sxs-lookup"><span data-stu-id="3db25-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="3db25-112">Atsisakymas vartotojų vardu</span><span class="sxs-lookup"><span data-stu-id="3db25-112">Opting out on behalf of users</span></span>

<span data-ttu-id="3db25-113">„Commerce“ operacijų skyriuje, Sąskaitų tvarkymas, mažmenininkai gali atsisakyti vartotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="3db25-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="3db25-114">Pagrindiniame operacijų skyriaus puslapyje ieškokite **visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="3db25-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="3db25-115">Ieškokite ir pasirinkite klientą, tada pasirinkite „FastTab“ **Mažmeninė prekyba**.</span><span class="sxs-lookup"><span data-stu-id="3db25-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![„FastTab“ mažmeninė prekyba](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="3db25-117">Būdami **Privatumas**, nustatykite parinktį **Išjungti asmeninius poreikius** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3db25-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Privatumo nustatymai](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="3db25-119">Pasirinkite **Išsaugoti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3db25-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="3db25-120">Moduliais pagrįsta atsisakymo galimybė</span><span class="sxs-lookup"><span data-stu-id="3db25-120">Module-based opt-out experience</span></span>

<span data-ttu-id="3db25-121">Mažmenininkai gali leisti autentifikuotiems vartotojams patiems atsisakyti gauti asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="3db25-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="3db25-122">Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.</span><span class="sxs-lookup"><span data-stu-id="3db25-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="3db25-123">Pasirinktiniai plėtiniai</span><span class="sxs-lookup"><span data-stu-id="3db25-123">Custom extensions</span></span>

<span data-ttu-id="3db25-124">Mažmenininkai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę.</span><span class="sxs-lookup"><span data-stu-id="3db25-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="3db25-125">Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="3db25-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="3db25-126">Autentifikuoto vartotojo vardu gaukite skaitmeninę asmeniniams poreikiams pritaikytų rekomendacijų duomenų kopiją</span><span class="sxs-lookup"><span data-stu-id="3db25-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="3db25-127">Klientai gali norėti įsigyti skaitmeninę savo asmeninių duomenų kopiją ir pamatyti jų rekomendacijų rezultatų eksportuotą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3db25-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="3db25-128">Jei klientas prašo šios informacijos, mažmenininkas turi sukurti pritaikytą plėtinį, iškviečiantį Mažmeninio serverio programos programavimo sąsają (angl. API), ir visų rezultatų užklausas iš sąrašo **Parinkta jums**, remiantis kliento ID.</span><span class="sxs-lookup"><span data-stu-id="3db25-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="3db25-129">Tada, kableliais atskyrus vertes (angl. CSV), rezultatus galima eksportuoti ir bendrinti su klientu.</span><span class="sxs-lookup"><span data-stu-id="3db25-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="3db25-130">Toliau parodytame pavyzdyje matoma, kaip mažmenininkas gali įvykdyti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="3db25-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="3db25-131">Mažmenininkas sukuria pasirinktinį plėtinį, kad vartotojo vardu būtų galima gauti asmeninių rekomendacijų duomenis.</span><span class="sxs-lookup"><span data-stu-id="3db25-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="3db25-132">Norėdami gauti informacijos apie tai, kaip sukurti modulius, klonuoti esamus modulius, iškviesti Mažmeninės prekybos serverio API ir iškviesti duomenų veiksmus, žr. [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="3db25-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="3db25-133">Pasirinktinis plėtinys iškviečia pagrindinių duomenų veiksmą **gauti rekomendacijas** ir perduoda reikiamą informaciją, remdamasis sąrašo reikalavimais.</span><span class="sxs-lookup"><span data-stu-id="3db25-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="3db25-134">Sąraše **Parinkta jums** plėtinys duomenų perdavimui turi perduoti teisingą sąrašo pavadinimą ir kliento ID.</span><span class="sxs-lookup"><span data-stu-id="3db25-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="3db25-135">Vienas iš būdų sukurti pasirinktinį plėtinį yra esamo produktų rinkimo modulio, naudojamo grąžinti rekomendacijų rezultatus, klonavimas.</span><span class="sxs-lookup"><span data-stu-id="3db25-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="3db25-136">Klonuodamas šį esamą modulį, mažmenininkas gali modifikuoti esamą kodą ir pridėti naują mygtuką, kuris eksportuoja rekomendacijų rezultatus į CSV failą.</span><span class="sxs-lookup"><span data-stu-id="3db25-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="3db25-137">Daugiau informacijos rasite [Modulių bibliotekos modulio klonavimas](e-commerce-extensibility/clone-starter-module.md) ir [Produktų kolekcijos moduliai](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3db25-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="3db25-138">Norėdami pamatyti visą Mažmeninės prekybos serverio API bibliotekos vaizdą, žr. [Mažmeninės prekybos serverių klientų ir vartotojų API](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="3db25-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="3db25-139">Sukūręs pasirinktinį plėtinį, mažmenininkas gali eksportuoti visų rekomendacijų rezultatų CSV failą, pagrįstą unikaliu autentifikuoto vartotojo kliento ID.</span><span class="sxs-lookup"><span data-stu-id="3db25-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="3db25-140">Mažmenininkas gali bendrinti eksportuotą CSV failą, kuriame yra visas asmeniniams poreikiams pritaikytų rekomenduojamų produktų sąrašas su autentifikuotu vartotoju.</span><span class="sxs-lookup"><span data-stu-id="3db25-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3db25-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3db25-141">Additional resources</span></span>

[<span data-ttu-id="3db25-142">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="3db25-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3db25-143">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="3db25-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="3db25-144">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="3db25-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="3db25-145">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="3db25-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3db25-146">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="3db25-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="3db25-147">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="3db25-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="3db25-148">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="3db25-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3db25-149">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="3db25-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="3db25-150">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="3db25-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="3db25-151">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="3db25-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="3db25-152">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="3db25-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
