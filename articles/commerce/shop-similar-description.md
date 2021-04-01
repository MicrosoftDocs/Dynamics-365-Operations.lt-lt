---
title: Įjunkite „parduotuvės panašaus aprašo“ rekomendacijas
description: Šioje temoje aprašoma, kaip įjungti „panašių į parduotuvės aprašą“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234394"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="c9b34-103">Rekomendacijų „pirkti su panašiu aprašymu“ įjungimas</span><span class="sxs-lookup"><span data-stu-id="c9b34-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9b34-104">Šioje temoje aprašoma, kaip įjungti „panašių į parduotuvės aprašą“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c9b34-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c9b34-105">„Panašios į paruodutuvės aprašą“ rekomendacijų funkcija „Dynamics 365 Commerce“ naudoja dirbtinį intelektą ir mašininį mokymąsi (AI-ML) tam, kad pateiktų rekomendacijas produktams, kurių aprašai yra panašūs į kliento ieškomus.</span><span class="sxs-lookup"><span data-stu-id="c9b34-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="c9b34-106">Padarydami „į parduotuvę panašų aprašą“ rekomendacijas prieinamas visiems mažmenos kanalams „Commerce“, mažmenos prekeiviai gali padėti klientams nesunkiai surasti jų norimus dalykus.</span><span class="sxs-lookup"><span data-stu-id="c9b34-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="c9b34-107">Funkcija „panašių į parduotuvės aprašą“ rekomendacijoms naudoja produkto pavadinimą ir matytų produktų aprašą siekiant surasti ir rekomenduojamus panašius produktus mažmeninių prekeivių produkto kataloge.</span><span class="sxs-lookup"><span data-stu-id="c9b34-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="c9b34-108">„Į parduotuvės aprašą panašios“ rekomendacijos yra prieinamos prekybos vietoje ir el. komercijos patirtyse.</span><span class="sxs-lookup"><span data-stu-id="c9b34-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="c9b34-109">Scenarijų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="c9b34-109">Example scenarios</span></span>

<span data-ttu-id="c9b34-110">Tolesnio pavyzdžio scenarijai rodo rekomendacijų tipus, kuriuos „į parduotuvės aprašą panašios“ funkcijos gali pateikti:</span><span class="sxs-lookup"><span data-stu-id="c9b34-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="c9b34-111">Klientas mato retro stiliaus ragų formos porą ir gauna rekomendacijų rinkinį kitiems akiniams, kurie turi panašų dizainą mažmenos prekybininko pramonės kontekste.</span><span class="sxs-lookup"><span data-stu-id="c9b34-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="c9b34-112">Klientas naudoja „į parduotuvę panašų aprašą“ rekomendacijas siekiant gauti kavos skonius, kurie yra panašūs į skonį, kurį anksčiau įsigijo iš mažmenininko.</span><span class="sxs-lookup"><span data-stu-id="c9b34-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="c9b34-113">Nustatykite „į parduotuvės aprašą panašias“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="c9b34-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="c9b34-114">Produkto rekomendacijos yra palaikomos tik „Commerce“ vartotojams, kurie perkėlė savo laikymus į „Azure Data Lake Storage“ Gen2.</span><span class="sxs-lookup"><span data-stu-id="c9b34-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c9b34-115">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="c9b34-115">Prerequisites</span></span>

<span data-ttu-id="c9b34-116">Prieš tai, kai „į parduotuvės aprašą panašios“ rekomendacijos gali būti rodomos klientams, turite užbaigti tolesnes išankstines sąlygas:</span><span class="sxs-lookup"><span data-stu-id="c9b34-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="c9b34-117">[Įjungti produkto rekomendacijas](enable-product-recommendations.md) prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="c9b34-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="c9b34-118">Patvirtinti, kad medijos serveris palaiko HTTPS skambučius.</span><span class="sxs-lookup"><span data-stu-id="c9b34-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="c9b34-119">Įjunkite „į parduotuvės aprašą panašias“ rekomendacijų funkciją</span><span class="sxs-lookup"><span data-stu-id="c9b34-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="c9b34-120">Norėdami įjungti „į parduotuvės aprašą panašias“ rekomendacijas ir jų funkciją „Commerce“ būstinėje, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="c9b34-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c9b34-121">Darbo srtiyje **Funkcijų valdymas**, esamų funkcijų sąraše, ieškokite ir rinkitės **Į parduotuvę apanšų aprašą**.</span><span class="sxs-lookup"><span data-stu-id="c9b34-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="c9b34-122">Dešiniojoje juostoje rinkitės **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="c9b34-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="c9b34-123">Jums įjungus funkciją, sistema pradeda kurti produkto rekomendacijų sąrašus.</span><span class="sxs-lookup"><span data-stu-id="c9b34-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="c9b34-124">Gali užtrukti iki dienos, kol sąrašai bus prieinami ir matomi internete ir POS terminaluose.</span><span class="sxs-lookup"><span data-stu-id="c9b34-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="c9b34-125">Jei išjungsite funkciją, kiti produkto rekomendacijų tipai paveikti nebus.</span><span class="sxs-lookup"><span data-stu-id="c9b34-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="c9b34-126">Dėl išsamesnės informacijos apie produkto rekomendacijas, žr. [Produkto rekomendacijų apžvalga](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="c9b34-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="c9b34-127">Įtraukti į parduotuvę panašaus aprašo mygtuką į parduotuvės išsamios informacijos puslapius</span><span class="sxs-lookup"><span data-stu-id="c9b34-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="c9b34-128">Jums įjungus į „parduotuvės aprašą panašias“ rekomendacijas ir jų funkciją „Commerce“ štabe, galite įtraukti **Į parduotuvę panašaus aprašo** mygtuką į įsigijimo laukelį bet kurio produkto išsamios informacijos puslapyje (PDP).</span><span class="sxs-lookup"><span data-stu-id="c9b34-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="c9b34-129">Klientas pasirinkęs šį mygtuką yra nuvedamas į paskirtą **Į parduotuvę panašaus aprašą** puslapį, kuriame rodomi panašūs produktai.</span><span class="sxs-lookup"><span data-stu-id="c9b34-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="c9b34-130">Klientas tada gali naudoti parinkiklius tolesniam produktų filtravimui.</span><span class="sxs-lookup"><span data-stu-id="c9b34-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="c9b34-131">Norėdami įtrarukti **į parduotuvės aprašą panašų** mygtuką PDP naudodami „Commerce“ saito kūrimo įrankį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="c9b34-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c9b34-132">Atverkite esantį vietos kūrimo įrankio puslapį, turintį įsigijimo laukelio modulį.</span><span class="sxs-lookup"><span data-stu-id="c9b34-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="c9b34-133">Kairėje naršymo juostoje pasirinkite įsigijimo laukelio modulį.</span><span class="sxs-lookup"><span data-stu-id="c9b34-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="c9b34-134">Dešiniojoje juostoje, rinkitės **Įjungti į parduotuvės aprašą panašią nuorodą** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="c9b34-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="c9b34-135">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c9b34-135">Select **Save**.</span></span>
1. <span data-ttu-id="c9b34-136">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="c9b34-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="c9b34-137">Publikavus puslapį, PDP apims **Į parduotuvę panašaus aprašo** mygtuką.</span><span class="sxs-lookup"><span data-stu-id="c9b34-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="c9b34-138">Tolesnis paveikslėlis rodo **Įjungti į parduotuvę panašaus aprašo nuorodą** žymimą laukelį ir **Į parduotuvę panašaus aprašo** mygtuką PDP pavyzdyje saito kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="c9b34-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Įjunkite į parduotuvę panašaus aprašo nuorodą žymimame laukelyje ir į parduotuvę panašaus aprašo mygtuką PDP saito kūrimo įrankyje](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="c9b34-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c9b34-140">Additional resources</span></span>

[<span data-ttu-id="c9b34-141">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c9b34-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="c9b34-142">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="c9b34-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="c9b34-143">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="c9b34-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="c9b34-144">Įjungti „pirkti panašios išvaizdos“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="c9b34-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="c9b34-145">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="c9b34-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="c9b34-146">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="c9b34-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="c9b34-147">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="c9b34-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]