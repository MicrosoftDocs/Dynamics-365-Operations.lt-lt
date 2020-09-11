---
title: Įgalinti asmeniniams poreikiams pritaikytų produktų rekomendacijas
description: Šioje temoje pateikiama informacija, kaip klientams pritaikyti produktų rekomendacijas asmeniniams poreikiams, naudojant „Microsoft Dynamics 365 Commerce“.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: d3b970c3b93d8be12886b1c5a6bf91f0b33726dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2020
ms.locfileid: "3700871"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="37288-103">Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="37288-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37288-104">Šioje temoje pateikiama informacija, kaip klientams pritaikyti produktų rekomendacijas asmeniniams poreikiams, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="37288-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="37288-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="37288-105">Overview</span></span>

<span data-ttu-id="37288-106">Naudojant „Microsoft Dynamics 365 Commerce“, mažmenininkai gali pritaikyti produktų rekomendacijas asmeniniams poreikiams (dar žinoma kaip suasmeninimas).</span><span class="sxs-lookup"><span data-stu-id="37288-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="37288-107">Tokiu būdu asmeniniams poreikiams pritaikytos rekomendacijos gali būti įtrauktos į klientų patirtį internete ir elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="37288-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="37288-108">Įjungus suasmeninimo funkciją, sistema gali susieti vartotojo pirkinio ir produkto informaciją, kad sugeneruotų individualizuotas produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="37288-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="37288-109">Suasmeninimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="37288-109">Personalization prerequisites</span></span>

<span data-ttu-id="37288-110">Prieš pateikdami asmeniniams poreikiams pritaikytų produktų rekomendacijas vartotojams, atkreipkite dėmesį, kad produktų rekomendacijos palaikomos tik tiems „Commerce“ vartotojams, kurie perkėlė saugyklą į „Azure Data Lake Store“.</span><span class="sxs-lookup"><span data-stu-id="37288-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="37288-111">Kad klientai galėtų gauti asmeniniams poreikiams pritaikytų produktų rekomendacijas, mažmenininkai turi [Įjungti produktų rekomendacijas](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="37288-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="37288-112">Įjungdami produktų rekomendacijas, taip pat įjungiate suasmeninimą.</span><span class="sxs-lookup"><span data-stu-id="37288-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="37288-113">Tačiau jei išjungiate suasmeninimą, negalite išjungti kitų produktų tipų rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="37288-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="37288-114">Norėdami gauti daugiau informacijos apie produkto rekomendacijas, žr. [Produktų rekomendacijų apžvalga](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="37288-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="37288-115">Įjungti suasmeninimą</span><span class="sxs-lookup"><span data-stu-id="37288-115">Turn on personalization</span></span>

<span data-ttu-id="37288-116">Norėdami įjungti suasmeninimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="37288-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="37288-117">"Commerce Headquarters" ieškokite **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="37288-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="37288-118">Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="37288-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="37288-119">Ieškos lauke įveskite **Rekomendacijos**.</span><span class="sxs-lookup"><span data-stu-id="37288-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="37288-120">Pasirinkite **Suasmenintos produktų rekomendacijos** funkciją.</span><span class="sxs-lookup"><span data-stu-id="37288-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="37288-121">Ypatybių srityje **Suasmenintos produktų rekomendacijos** pasirinkite **Įgalinti dabar**.</span><span class="sxs-lookup"><span data-stu-id="37288-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Suasmeninimo įjungimas](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="37288-123">Įjungus suasmeninimą, pradedamas asmeniniams poreikiams pritaikytų produktų rekomendacijų sąrašų generavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="37288-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="37288-124">Gali prireikti vienos dienos, kol šie sąrašai bus prieinami ir matomi internete ir EKA.</span><span class="sxs-lookup"><span data-stu-id="37288-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="37288-125">Asmeniniams poreikiams pritaikyti sąrašai</span><span class="sxs-lookup"><span data-stu-id="37288-125">Personalized lists</span></span>

<span data-ttu-id="37288-126">Be to, kad yra galimybė suasmeninti esamus mašinų sugeneruotus sąrašus, rekomendacijų tarnyba suteikia galimybę suasmeninti produkto aptikimą tiek internetu, tiek EKA.</span><span class="sxs-lookup"><span data-stu-id="37288-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="37288-127">Įjungus suasmeninimą, mažmenininkai gali rodyti pirkėjų asmeniniams poreikiams pritaikytus „Parinkta jums“ sąrašus internete arba „Rekomenduojama klientui“ sąrašus EKA terminaluose.</span><span class="sxs-lookup"><span data-stu-id="37288-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="37288-128">Be to, mažmenininkai gali pritaikyti suasmeninimą esamiems produktų rekomendacijų sąrašams ir leisti autentifikuotiems vartotojams atsisakyti Bendrojo duomenų apsaugos reglamento (BDAR).</span><span class="sxs-lookup"><span data-stu-id="37288-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="37288-129">Jei išjungsite suasmeninimą, taip pat išjungsite ir šias funkcijas.</span><span class="sxs-lookup"><span data-stu-id="37288-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="37288-130">Internetinis sąrašas „Parinkta jums“</span><span class="sxs-lookup"><span data-stu-id="37288-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="37288-131">Sąrašas „Parinkta jums“ yra dirbtinio intelekto ir mašininio mokymosi (angl. AI-ML) sąrašas, kuriame autentifikuotam vartotojui pateikiamas asmeniniams poreikiams pritaikytas siūlomų produktų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="37288-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="37288-132">Šis sąrašas yra pagrįstas vartotojo kanalų pirkimo istorija.</span><span class="sxs-lookup"><span data-stu-id="37288-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="37288-133">Pagal asmeninius poreikius pritaikytos rekomendacijos yra dinamiškai atnaujinamos, jei vartotojas perka daugiau.</span><span class="sxs-lookup"><span data-stu-id="37288-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="37288-134">Šio tipo sąrašai taip pat palaiko kategorijų filtravimą, kad mažmenininkai galėtų parodyti populiariausias parinktis, remiantis naršymo hierarchijomis.</span><span class="sxs-lookup"><span data-stu-id="37288-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="37288-135">Kad bet kuriame „e-Commerce“ puslapyje galėtų būti sąrašas „Parinkta jums“, turi būti įvykdyti šie reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="37288-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="37288-136">Vartotojas privalo būti prisijungęs.</span><span class="sxs-lookup"><span data-stu-id="37288-136">Users must be signed in.</span></span> <span data-ttu-id="37288-137">Anoniminis vartotojas nematys asmeniniams poreikiams pritaikytų rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="37288-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="37288-138">Vartotojo paskyroje turi būti bent vienas pirkinys.</span><span class="sxs-lookup"><span data-stu-id="37288-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="37288-139">Vartotojas turi pasirinkti gauti asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="37288-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="37288-140">Toliau parodytame paveikslėlyje pateiktas internetinės parduotuvės puslapyje esančio sąrašo „Parinkta jums“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="37288-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Internetinis sąrašas „Parinkta jums“](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="37288-142">Sąrašai „Rekomenduojama klientui“, esantys EKA</span><span class="sxs-lookup"><span data-stu-id="37288-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="37288-143">Norėdami padidinti savo klientų dėmesį, mažmenininkai gali pagal asmeninius poreikius pritaikyti esamus informacijos apie klientus puslapius, pridėdami kontekstinį sąrašą „Rekomenduojama klientui“.</span><span class="sxs-lookup"><span data-stu-id="37288-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="37288-144">Toliau parodytame paveikslėlyje pateiktas EKA terminale esančio sąrašo „Rekomenduojama klientui“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="37288-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Sąrašai „Rekomenduojama klientui“, esantys EKA](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="37288-146">Suasmeninimo esamiems rekomendacijų sąrašams pritaikymas</span><span class="sxs-lookup"><span data-stu-id="37288-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="37288-147">Mažmenininkai gali pritaikyti suasmeninimą esamiems rekomendacijų sąrašams, tokiems kaip „Naujas“, „Populiariausi“, „Geriausiai parduodami“, „Žmonėms taip pat patiko“ ir „Kartu taip pat perkama“.</span><span class="sxs-lookup"><span data-stu-id="37288-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="37288-148">Kai suasmeninimas pritaikomas esamiems sąrašams, prekės, kurias prisijungęs vartotojas nusipirko anksčiau, pašalinamos iš tų sąrašų.</span><span class="sxs-lookup"><span data-stu-id="37288-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="37288-149">Tiek anoniminiams vartotojams, tiek vartotojams, kurie atsisakė gauti asmeniniams poreikiams pritaikytas rekomendacijas, rodomos numatytos esamų sąrašų versijos.</span><span class="sxs-lookup"><span data-stu-id="37288-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="37288-150">Todėl mažmenininkams nereikia rankiniu būdu prižiūrėti atskirų puslapių.</span><span class="sxs-lookup"><span data-stu-id="37288-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="37288-151">Pavyzdžiui, prisijungęs vartotojas jau nusipirko juodą laikrodį ir rudus darbo batus, kurie pateikiami toliau pateiktoje iliustracijoje, sąraše „Populiariausi – numatytasis“.</span><span class="sxs-lookup"><span data-stu-id="37288-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="37288-152">Todėl vartotojas vietoje tų produktų matys naujus produktus, kaip parodyta sąraše „Populiariausi – asmeniniams poreikiams pritaikyta“.</span><span class="sxs-lookup"><span data-stu-id="37288-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Suasmeninimo pritaikymas](./media/applypersonalization.png)

<span data-ttu-id="37288-154">Jei norite pritaikyti suasmeninimą esamam rekomendacijų sąrašui, esančiam „Commerce“ svetainės daryklėje, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="37288-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="37288-155">Atidarykite esamą svetainių daryklių puslapį, kuriame yra produktų rinkimo modulis.</span><span class="sxs-lookup"><span data-stu-id="37288-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="37288-156">Kairėje naršymo srityje pasirinkite produkto rinkimo modulį.</span><span class="sxs-lookup"><span data-stu-id="37288-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="37288-157">Dešinėje naršymo srityje, skyriuje **Produktai**, pasirinkite sąrašą.</span><span class="sxs-lookup"><span data-stu-id="37288-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="37288-158">Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**, skyriuje **Tipas**, pasirinkite sąrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="37288-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="37288-159">Pažymėkite žymės langelį **Taikyti suasmeninimą**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="37288-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Suasmeninimo pritaikymas populiariausiam sąrašui](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="37288-161">Išsaugokite puslapį, baikite jį redaguoti ir paskelbkite.</span><span class="sxs-lookup"><span data-stu-id="37288-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="37288-162">Paskelbus puslapį, prisijungę vartotojai matys asmeniniams poreikiams pritaikytus populiariausius sąrašus.</span><span class="sxs-lookup"><span data-stu-id="37288-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37288-163">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="37288-163">Additional resources</span></span>

[<span data-ttu-id="37288-164">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="37288-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="37288-165">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="37288-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="37288-166">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="37288-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="37288-167">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="37288-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="37288-168">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="37288-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="37288-169">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="37288-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="37288-170">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="37288-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="37288-171">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="37288-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="37288-172">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="37288-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="37288-173">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="37288-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="37288-174">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="37288-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
