---
title: Įvertinimų ir atsiliepimų tvarkymas
description: Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698031"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="69c86-103">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="69c86-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="69c86-104">Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="69c86-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="69c86-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="69c86-105">Overview</span></span>

<span data-ttu-id="69c86-106">„Dynamics 365 Commerce“ naudojama „Microsoft Azure“ pažinimo tarnyba automatiškai moderuoti atsiliepimo tekstą pašalinant keiksmažodžius.</span><span class="sxs-lookup"><span data-stu-id="69c86-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="69c86-107">Be to, moderatoriai gali naudoti įvertinimų ir apžvalgų moderavimo įrankį šioms neautomatinėms užduotims:</span><span class="sxs-lookup"><span data-stu-id="69c86-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="69c86-108">Moderuokite apžvalgas atsakydami į juos arba juos pašalindami.</span><span class="sxs-lookup"><span data-stu-id="69c86-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="69c86-109">Panaikinkite kliento apžvalgas klientui pateikus dėl to užklausą.</span><span class="sxs-lookup"><span data-stu-id="69c86-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="69c86-110">Visų produktų masinio importo įvertinimų ir apžvalgų duomenys į „Microsoft Power BI“ šabloną, kad įvertinimų ir atsiliepimų tendencijos galėtų būti analizuojamos.</span><span class="sxs-lookup"><span data-stu-id="69c86-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="69c86-111">Apžvalgos skaitymas</span><span class="sxs-lookup"><span data-stu-id="69c86-111">Read a review</span></span> 

1. <span data-ttu-id="69c86-112">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="69c86-113">Norėdami filtruotiapžvalgas, kurios rodomos produkto ID, produkto pavadinime arba apžvalgos tekste, naudokite ieškos lauką, esantį viršutiniame dešiniajame puslapio kampe.</span><span class="sxs-lookup"><span data-stu-id="69c86-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="69c86-114">Papildomais filtrais galima riboti apžvalgas pagal laikotarpį, vertinimą, kanalą arba su būseną (pašalinta, atsakyta arba pranešta).</span><span class="sxs-lookup"><span data-stu-id="69c86-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderavimo pagrindinis puslapis](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="69c86-116">Atsakymas į apžvalgą</span><span class="sxs-lookup"><span data-stu-id="69c86-116">Respond to a review</span></span> 

<span data-ttu-id="69c86-117">Kartais klientai, kurie pirko produktą, pareiškia savo pasitenkinimą ar nepasitenkinimą, arba nesupranta, kaip naudoti produktą.</span><span class="sxs-lookup"><span data-stu-id="69c86-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="69c86-118">Kaip moderatorius galite paskelbti atsakymą į apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="69c86-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="69c86-119">Šis atsakymas rodomas kartu su apžvalga svetainėje.</span><span class="sxs-lookup"><span data-stu-id="69c86-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="69c86-120">Norėdami atsakyti į apžvalgą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69c86-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="69c86-121">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="69c86-122">Suraskite ir pasirinkite apžvalgą, į kurį reikia atsakyti.</span><span class="sxs-lookup"><span data-stu-id="69c86-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="69c86-123">Dešiniojoje ypatybių srityje pasirinkite **Įtraukti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="69c86-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="69c86-124">Įveskite atsakymo tekstą ir pavadinimą, kuris turi būti rodomas atsakytojui.</span><span class="sxs-lookup"><span data-stu-id="69c86-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="69c86-125">Numatytasis atsakytojo pavadinimas yra **Moderatorius**.</span><span class="sxs-lookup"><span data-stu-id="69c86-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="69c86-126">Baigę pasirinkite **Skelbti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="69c86-126">When you've finished, select **Post response**.</span></span>

![Atsakymas į apžvalgą](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="69c86-128">Apžvalgos šalinimas</span><span class="sxs-lookup"><span data-stu-id="69c86-128">Take down a review</span></span> 

<span data-ttu-id="69c86-129">Kartais dėl verslo priežasčių moderatoriai turi pašalinti klientų apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="69c86-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="69c86-130">Norėdami pašalinti apžvalgą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69c86-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="69c86-131">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="69c86-132">Suraskite ir pasirinkite apžvalgą, kurią reikia pašalinti.</span><span class="sxs-lookup"><span data-stu-id="69c86-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="69c86-133">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pašalinimo priežastį ir pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="69c86-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="69c86-134">Kliento apžvalgų naikinimas klientui pateikus užklausą</span><span class="sxs-lookup"><span data-stu-id="69c86-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="69c86-135">Kartais klientai nori, kad jų įvertinimų ir apžvalgų duomenys būtų visam laikui panaikinti iš el. prekybos svetainės.</span><span class="sxs-lookup"><span data-stu-id="69c86-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="69c86-136">Moderatorius, gavęs pašalinimo užklausą iš kliento, gali pašalinti kliento duomenis naudodamas apžvalgos naikinimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="69c86-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="69c86-137">Norint surasti ir panaikinti kliento duomenis, moderatoriui reikia el. pašto adreso, kurį klientas naudojo prisijungdamas ir pateikdamas apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="69c86-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="69c86-138">Norėdami rasti ir panaikinti kliento duomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69c86-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="69c86-139">Eikite į **Pagrindinis \> Apžvalgos \>Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="69c86-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="69c86-140">Lauke **Ieškoti vartotojų pagal el. pašto adresą** įveskite kliento el. pašto adresą ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="69c86-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="69c86-141">Jei klientas atliko apžvalgos veiklų (pavyzdžiui, atsiliepimų teikimas, balsavimai, kiek kito kliento atsiliepimai buvo naudingi, arba komentavimas apie kito kliento atsiliepimą), rezultatai rodomi.</span><span class="sxs-lookup"><span data-stu-id="69c86-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="69c86-142">Kiekviename elemente yra mygtukas **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="69c86-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="69c86-143">Kiekvienam elementui, kurį reikia naikinti, pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="69c86-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="69c86-144">Kai būsite paraginti patvirtinti, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69c86-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Kliento duomenų naikinimas](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="69c86-146">Norint, kad duomenys būtų visiškai pašalinti iš sistemos, tai gali užtrukti iki septynių dienų.</span><span class="sxs-lookup"><span data-stu-id="69c86-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="69c86-147">Moderatoriai turėtų informuoti klientus apie šį vėlavimą.</span><span class="sxs-lookup"><span data-stu-id="69c86-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="69c86-148">Jei klientai pakeitė savo pavadinimą savo paskyros parametruose, ieškos rezultatuose gali būti rodomi keli elementai.</span><span class="sxs-lookup"><span data-stu-id="69c86-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="69c86-149">Šiuo atveju, kad būtų visiškai panaikinti kliento duomenys, moderatorius turi pasirinkti **Naikinti** kiekvienam elementui.</span><span class="sxs-lookup"><span data-stu-id="69c86-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="69c86-150">Įvertinimų ir apžvalgų duomenų atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="69c86-150">Download ratings and reviews data</span></span>

<span data-ttu-id="69c86-151">Įvertinimų ir apžvalgų moderavimo įrankiu moderatoriai gali importuoti įvertinimų ir atsiliepimų duomenis masiškai, kad jie galėtų analizuoti tendencijas.</span><span class="sxs-lookup"><span data-stu-id="69c86-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="69c86-152">Galimas „Power BI“ šablonas, kuriame yra pagrindinė metrika.</span><span class="sxs-lookup"><span data-stu-id="69c86-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="69c86-153">Moderatoriai gali naudoti šį šabloną masiškai importuotiems duomenims sujungti ir peržiūrėti ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="69c86-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="69c86-154">Jiems nebūtina sukurti tinkintą ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="69c86-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="69c86-155">Moderatoriai taip pat gali tinkinti „Power BI“ šabloną, kad patenkintų konkrečius poreikius.</span><span class="sxs-lookup"><span data-stu-id="69c86-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="69c86-156">Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69c86-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="69c86-157">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="69c86-158">Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis kableliais atskirtų reikšmių (CSV) formatu, pasirinkite **Atsisiųsti apžvalgų duomenis**.</span><span class="sxs-lookup"><span data-stu-id="69c86-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="69c86-159">Įvertinimų ir apžvalgų tendencijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="69c86-159">View ratings and reviews trends</span></span>

<span data-ttu-id="69c86-160">Moderatoriai gali atsisiųsti „Power BI“ šabloną, kad galėtų peržiūrėti tendencijas ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="69c86-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="69c86-161">Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69c86-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="69c86-162">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="69c86-163">Pasirinkite **„PowerBI“ šablonas**, kad atsisiųstumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="69c86-163">Select **PowerBI template** to download the template.</span></span>

    ![„Power BI“ šablono atsisiuntimas](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="69c86-165">Atidarykite atsisiųstą šabloną naudojantis „Power BI“ programėle.</span><span class="sxs-lookup"><span data-stu-id="69c86-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="69c86-166">Uždarykite pasirodžiusį dialogo langą **Prieiga prie interneto turinio** ir uždarykite pasirodžiusį klaidos pranešimą „Atnaujinti“.</span><span class="sxs-lookup"><span data-stu-id="69c86-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="69c86-167">Eikite į **Pagrindinis**, pasirinkite **Redaguoti užklausas** ir pasirinkite **Duomenų šaltinio parametrai**.</span><span class="sxs-lookup"><span data-stu-id="69c86-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="69c86-168">Dialogo lange **Duomenų šaltinio parametrai** pasirinkite **Keisti šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="69c86-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="69c86-169">Lauke **URL** įveskite apžvalgų duomenų, kuriuos atsisiuntėte ankstesne procedūra, maršrutą (pvz., **c:\\apžvalgos\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="69c86-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Kableliais atskirtų reikšmių dialogo lango URL laukas](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="69c86-171">Pasirinkite **Gerai**, tada – **Taikyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="69c86-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="69c86-172">Užtruks nuo vienos iki dviejų minučių, kol jūsų keitimai bus pritaikyti duomenų šaltinyje.</span><span class="sxs-lookup"><span data-stu-id="69c86-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="69c86-173">Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, pasirinkite **Tendencijų lapas**.</span><span class="sxs-lookup"><span data-stu-id="69c86-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Įvertinimų ir apžvalgų tendencijos](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="69c86-175">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="69c86-175">Additional resources</span></span>

[<span data-ttu-id="69c86-176">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="69c86-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="69c86-177">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="69c86-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="69c86-178">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="69c86-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="69c86-179">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="69c86-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
