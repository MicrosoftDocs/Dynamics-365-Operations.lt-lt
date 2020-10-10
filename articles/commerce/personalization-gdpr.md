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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6a64b45e1326673dd84c3c705491c9c100cdd069
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817528"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="5998f-103">Atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų</span><span class="sxs-lookup"><span data-stu-id="5998f-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5998f-104">Šioje temoje pateikiama informacija, kaip galite leisti klientams atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5998f-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5998f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="5998f-105">Overview</span></span>

<span data-ttu-id="5998f-106">Kuriant paskyrą, nauji klientai automatiškai gauna asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="5998f-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="5998f-107">Tačiau „Dynamics 365 Commerce“ siūlo įvairius būdus, kaip mažmenininkams leisti vartotojams atsisakyti gauti šias rekomendacijas ir apriboti jų asmeninių duomenų tvarkymą.</span><span class="sxs-lookup"><span data-stu-id="5998f-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="5998f-108">Autentifikuoti vartotojai, kurie atsisako gauti asmeniniams poreikiams pritaikytas rekomendacijas, iškart nustos matyti asmeniniams poreikiams pritaikytus sąrašus.</span><span class="sxs-lookup"><span data-stu-id="5998f-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="5998f-109">Be to, visi asmeniniai duomenys, kurie renkami asmeninių poreikių pritaikymui, bus pašalinti iš asmeniniams poreikiams pritaikytų rekomendacijų modelių.</span><span class="sxs-lookup"><span data-stu-id="5998f-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="5998f-110">Norėdami gauti daugiau informacijos apie asmeniniams poreikiams pritaikytas produkto rekomendacijas, žr. [Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="5998f-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="5998f-111">Būdai, kaip mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų</span><span class="sxs-lookup"><span data-stu-id="5998f-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="5998f-112">Mažmenininkai gali atsisakyti asmeniniams poreikiams pritaikytų rekomendacijų trimis būdais.</span><span class="sxs-lookup"><span data-stu-id="5998f-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="5998f-113">Atsisakymas vartotojų vardu</span><span class="sxs-lookup"><span data-stu-id="5998f-113">Opting out on behalf of users</span></span>

<span data-ttu-id="5998f-114">„Commerce“ operacijų skyriuje, Sąskaitų tvarkymas, mažmenininkai gali atsisakyti vartotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="5998f-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="5998f-115">Pagrindiniame operacijų skyriaus puslapyje ieškokite **visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="5998f-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="5998f-116">Ieškokite ir pasirinkite klientą, tada pasirinkite „FastTab“ **Mažmeninė prekyba**.</span><span class="sxs-lookup"><span data-stu-id="5998f-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![„FastTab“ mažmeninė prekyba](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="5998f-118">Būdami **Privatumas**, nustatykite parinktį **Išjungti asmeninius poreikius** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5998f-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Privatumo nustatymai](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="5998f-120">Pasirinkite **Išsaugoti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5998f-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="5998f-121">Moduliais pagrįsta atsisakymo galimybė</span><span class="sxs-lookup"><span data-stu-id="5998f-121">Module-based opt-out experience</span></span>

<span data-ttu-id="5998f-122">Mažmenininkai gali leisti autentifikuotiems vartotojams patiems atsisakyti gauti asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="5998f-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="5998f-123">Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.</span><span class="sxs-lookup"><span data-stu-id="5998f-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="5998f-124">Pasirinktiniai plėtiniai</span><span class="sxs-lookup"><span data-stu-id="5998f-124">Custom extensions</span></span>

<span data-ttu-id="5998f-125">Mažmenininkai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę.</span><span class="sxs-lookup"><span data-stu-id="5998f-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="5998f-126">Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5998f-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="5998f-127">Autentifikuoto vartotojo vardu gaukite skaitmeninę asmeniniams poreikiams pritaikytų rekomendacijų duomenų kopiją</span><span class="sxs-lookup"><span data-stu-id="5998f-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="5998f-128">Klientai gali norėti įsigyti skaitmeninę savo asmeninių duomenų kopiją ir pamatyti jų rekomendacijų rezultatų eksportuotą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="5998f-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="5998f-129">Jei klientas prašo šios informacijos, mažmenininkas turi sukurti pritaikytą plėtinį, iškviečiantį Mažmeninio serverio programos programavimo sąsają (angl. API), ir visų rezultatų užklausas iš sąrašo **Parinkta jums**, remiantis kliento ID.</span><span class="sxs-lookup"><span data-stu-id="5998f-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="5998f-130">Tada, kableliais atskyrus vertes (angl. CSV), rezultatus galima eksportuoti ir bendrinti su klientu.</span><span class="sxs-lookup"><span data-stu-id="5998f-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="5998f-131">Toliau parodytame pavyzdyje matoma, kaip mažmenininkas gali įvykdyti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="5998f-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="5998f-132">Mažmenininkas sukuria pasirinktinį plėtinį, kad vartotojo vardu būtų galima gauti asmeninių rekomendacijų duomenis.</span><span class="sxs-lookup"><span data-stu-id="5998f-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="5998f-133">Norėdami gauti informacijos apie tai, kaip sukurti modulius, klonuoti esamus modulius, iškviesti Mažmeninės prekybos serverio API ir iškviesti duomenų veiksmus, žr. [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="5998f-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="5998f-134">Pasirinktinis plėtinys iškviečia pagrindinių duomenų veiksmą **gauti rekomendacijas** ir perduoda reikiamą informaciją, remdamasis sąrašo reikalavimais.</span><span class="sxs-lookup"><span data-stu-id="5998f-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="5998f-135">Sąraše **Parinkta jums** plėtinys duomenų perdavimui turi perduoti teisingą sąrašo pavadinimą ir kliento ID.</span><span class="sxs-lookup"><span data-stu-id="5998f-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="5998f-136">Vienas iš būdų sukurti pasirinktinį plėtinį yra esamo produktų rinkimo modulio, naudojamo grąžinti rekomendacijų rezultatus, klonavimas.</span><span class="sxs-lookup"><span data-stu-id="5998f-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="5998f-137">Klonuodamas šį esamą modulį, mažmenininkas gali modifikuoti esamą kodą ir pridėti naują mygtuką, kuris eksportuoja rekomendacijų rezultatus į CSV failą.</span><span class="sxs-lookup"><span data-stu-id="5998f-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="5998f-138">Daugiau informacijos rasite [Modulių bibliotekos modulio klonavimas](e-commerce-extensibility/clone-starter-module.md) ir [Produktų kolekcijos moduliai](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5998f-138">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="5998f-139">Norėdami pamatyti visą Mažmeninės prekybos serverio API bibliotekos vaizdą, žr. [Mažmeninės prekybos serverių klientų ir vartotojų API](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="5998f-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="5998f-140">Sukūręs pasirinktinį plėtinį, mažmenininkas gali eksportuoti visų rekomendacijų rezultatų CSV failą, pagrįstą unikaliu autentifikuoto vartotojo kliento ID.</span><span class="sxs-lookup"><span data-stu-id="5998f-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="5998f-141">Mažmenininkas gali bendrinti eksportuotą CSV failą, kuriame yra visas asmeniniams poreikiams pritaikytų rekomenduojamų produktų sąrašas su autentifikuotu vartotoju.</span><span class="sxs-lookup"><span data-stu-id="5998f-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5998f-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5998f-142">Additional resources</span></span>

[<span data-ttu-id="5998f-143">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="5998f-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="5998f-144">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="5998f-144">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="5998f-145">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="5998f-145">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="5998f-146">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="5998f-146">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="5998f-147">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="5998f-147">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="5998f-148">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="5998f-148">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="5998f-149">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="5998f-149">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="5998f-150">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="5998f-150">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="5998f-151">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="5998f-151">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="5998f-152">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="5998f-152">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="5998f-153">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="5998f-153">Product recommendations FAQ</span></span>](faq-recommendations.md)
