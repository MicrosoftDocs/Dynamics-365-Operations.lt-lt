---
title: Įgalinti asmeniniams poreikiams pritaikytų produktų rekomendacijas
description: Šioje temoje pateikiama informacija, kaip klientams pritaikyti produktų rekomendacijas asmeniniams poreikiams, naudojant „Microsoft Dynamics 365 Commerce“.
author: bebeale
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804434"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="9ddcc-103">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9ddcc-104">Šioje temoje pateikiama informacija, kaip klientams pritaikyti produktų rekomendacijas asmeniniams poreikiams, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9ddcc-105">Naudojant „Microsoft Dynamics 365 Commerce“, mažmenininkai gali pritaikyti produktų rekomendacijas asmeniniams poreikiams (dar žinoma kaip suasmeninimas).</span><span class="sxs-lookup"><span data-stu-id="9ddcc-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="9ddcc-106">Tokiu būdu asmeniniams poreikiams pritaikytos rekomendacijos gali būti įtrauktos į klientų patirtį internete ir elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="9ddcc-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="9ddcc-107">Įjungus suasmeninimo funkciją, sistema gali susieti vartotojo pirkinio ir produkto informaciją, kad sugeneruotų individualizuotas produkto rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="9ddcc-108">Suasmeninimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="9ddcc-108">Personalization prerequisites</span></span>

<span data-ttu-id="9ddcc-109">Prieš pateikdami asmeniniams poreikiams pritaikytų produktų rekomendacijas vartotojams, atkreipkite dėmesį, kad produktų rekomendacijos palaikomos tik tiems „Commerce“ vartotojams, kurie perkėlė saugyklą į „Azure Data Lake Store“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="9ddcc-110">Kad klientai galėtų gauti asmeniniams poreikiams pritaikytų produktų rekomendacijas, mažmenininkai turi [Įjungti produktų rekomendacijas](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9ddcc-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9ddcc-111">Įjungdami produktų rekomendacijas, taip pat įjungiate suasmeninimą.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="9ddcc-112">Tačiau jei išjungiate suasmeninimą, negalite išjungti kitų produktų tipų rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="9ddcc-113">Norėdami gauti daugiau informacijos apie produkto rekomendacijas, žr. [Produktų rekomendacijų apžvalga](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="9ddcc-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="9ddcc-114">Įjungti suasmeninimą</span><span class="sxs-lookup"><span data-stu-id="9ddcc-114">Turn on personalization</span></span>

<span data-ttu-id="9ddcc-115">Norėdami įjungti suasmeninimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="9ddcc-116">"Commerce Headquarters" ieškokite **Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="9ddcc-117">Norėdami pamatyti galimų funkcijų sąrašą, pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="9ddcc-118">Ieškos lauke įveskite **Rekomendacijos**.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="9ddcc-119">Pasirinkite **Suasmenintos produktų rekomendacijos** funkciją.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="9ddcc-120">Ypatybių srityje **Suasmenintos produktų rekomendacijos** pasirinkite **Įgalinti dabar**.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Suasmeninimo įjungimas](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="9ddcc-122">Įjungus suasmeninimą, pradedamas asmeniniams poreikiams pritaikytų produktų rekomendacijų sąrašų generavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="9ddcc-123">Gali prireikti vienos dienos, kol šie sąrašai bus prieinami ir matomi internete ir EKA.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="9ddcc-124">Asmeniniams poreikiams pritaikyti sąrašai</span><span class="sxs-lookup"><span data-stu-id="9ddcc-124">Personalized lists</span></span>

<span data-ttu-id="9ddcc-125">Be to, kad yra galimybė suasmeninti esamus mašinų sugeneruotus sąrašus, rekomendacijų tarnyba suteikia galimybę suasmeninti produkto aptikimą tiek internetu, tiek EKA.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="9ddcc-126">Įjungus suasmeninimą, mažmenininkai gali rodyti pirkėjų asmeniniams poreikiams pritaikytus „Parinkta jums“ sąrašus internete arba „Rekomenduojama klientui“ sąrašus EKA terminaluose.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="9ddcc-127">Be to, mažmenininkai gali pritaikyti suasmeninimą esamiems produktų rekomendacijų sąrašams ir leisti autentifikuotiems vartotojams atsisakyti Bendrojo duomenų apsaugos reglamento (BDAR).</span><span class="sxs-lookup"><span data-stu-id="9ddcc-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="9ddcc-128">Jei išjungsite suasmeninimą, taip pat išjungsite ir šias funkcijas.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="9ddcc-129">Internetinis sąrašas „Parinkta jums“</span><span class="sxs-lookup"><span data-stu-id="9ddcc-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="9ddcc-130">Sąrašas „Parinkta jums“ yra dirbtinio intelekto ir mašininio mokymosi (angl. AI-ML) sąrašas, kuriame autentifikuotam vartotojui pateikiamas asmeniniams poreikiams pritaikytas siūlomų produktų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="9ddcc-131">Šis sąrašas yra pagrįstas vartotojo kanalų pirkimo istorija.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="9ddcc-132">Pagal asmeninius poreikius pritaikytos rekomendacijos yra dinamiškai atnaujinamos, jei vartotojas perka daugiau.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="9ddcc-133">Šio tipo sąrašai taip pat palaiko kategorijų filtravimą, kad mažmenininkai galėtų parodyti populiariausias parinktis, remiantis naršymo hierarchijomis.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="9ddcc-134">Kad bet kuriame „e-Commerce“ puslapyje galėtų būti sąrašas „Parinkta jums“, turi būti įvykdyti šie reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="9ddcc-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="9ddcc-135">Vartotojas privalo būti prisijungęs.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-135">Users must be signed in.</span></span> <span data-ttu-id="9ddcc-136">Anoniminis vartotojas nematys asmeniniams poreikiams pritaikytų rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="9ddcc-137">Vartotojo paskyroje turi būti bent vienas pirkinys.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="9ddcc-138">Vartotojas turi pasirinkti gauti asmeniniams poreikiams pritaikytas rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="9ddcc-139">Toliau parodytame paveikslėlyje pateiktas internetinės parduotuvės puslapyje esančio sąrašo „Parinkta jums“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Internetinis sąrašas „Parinkta jums“](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="9ddcc-141">Sąrašai „Rekomenduojama klientui“, esantys EKA</span><span class="sxs-lookup"><span data-stu-id="9ddcc-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="9ddcc-142">Norėdami padidinti savo klientų dėmesį, mažmenininkai gali pagal asmeninius poreikius pritaikyti esamus informacijos apie klientus puslapius, pridėdami kontekstinį sąrašą „Rekomenduojama klientui“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="9ddcc-143">Toliau parodytame paveikslėlyje pateiktas EKA terminale esančio sąrašo „Rekomenduojama klientui“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Sąrašai „Rekomenduojama klientui“, esantys EKA](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="9ddcc-145">Suasmeninimo esamiems rekomendacijų sąrašams pritaikymas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="9ddcc-146">Mažmenininkai gali pritaikyti suasmeninimą esamiems rekomendacijų sąrašams, tokiems kaip „Naujas“, „Populiariausi“, „Geriausiai parduodami“, „Žmonėms taip pat patiko“ ir „Kartu taip pat perkama“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="9ddcc-147">Kai suasmeninimas pritaikomas esamiems sąrašams, prekės, kurias prisijungęs vartotojas nusipirko anksčiau, pašalinamos iš tų sąrašų.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="9ddcc-148">Tiek anoniminiams vartotojams, tiek vartotojams, kurie atsisakė gauti asmeniniams poreikiams pritaikytas rekomendacijas, rodomos numatytos esamų sąrašų versijos.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="9ddcc-149">Todėl mažmenininkams nereikia rankiniu būdu prižiūrėti atskirų puslapių.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="9ddcc-150">Pavyzdžiui, prisijungęs vartotojas jau nusipirko juodą laikrodį ir rudus darbo batus, kurie pateikiami toliau pateiktoje iliustracijoje, sąraše „Populiariausi – numatytasis“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="9ddcc-151">Todėl vartotojas vietoje tų produktų matys naujus produktus, kaip parodyta sąraše „Populiariausi – asmeniniams poreikiams pritaikyta“.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Suasmeninimo pritaikymas](./media/applypersonalization.png)

<span data-ttu-id="9ddcc-153">Jei norite pritaikyti suasmeninimą esamam rekomendacijų sąrašui, esančiam „Commerce“ svetainės daryklėje, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9ddcc-154">Atidarykite esamą svetainių daryklių puslapį, kuriame yra produktų rinkimo modulis.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="9ddcc-155">Kairėje naršymo srityje pasirinkite produkto rinkimo modulį.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="9ddcc-156">Dešinėje naršymo srityje, skyriuje **Produktai**, pasirinkite sąrašą.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="9ddcc-157">Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**, skyriuje **Tipas**, pasirinkite sąrašo tipą.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="9ddcc-158">Pažymėkite žymės langelį **Taikyti suasmeninimą**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Suasmeninimo pritaikymas populiariausiam sąrašui](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="9ddcc-160">Išsaugokite puslapį, baikite jį redaguoti ir paskelbkite.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="9ddcc-161">Paskelbus puslapį, prisijungę vartotojai matys asmeniniams poreikiams pritaikytus populiariausius sąrašus.</span><span class="sxs-lookup"><span data-stu-id="9ddcc-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ddcc-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9ddcc-162">Additional resources</span></span>

[<span data-ttu-id="9ddcc-163">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9ddcc-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="9ddcc-164">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="9ddcc-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="9ddcc-165">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="9ddcc-166">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="9ddcc-167">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="9ddcc-168">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="9ddcc-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="9ddcc-169">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="9ddcc-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="9ddcc-170">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="9ddcc-171">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="9ddcc-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="9ddcc-172">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="9ddcc-173">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="9ddcc-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
