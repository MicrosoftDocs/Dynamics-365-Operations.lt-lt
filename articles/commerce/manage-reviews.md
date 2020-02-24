---
title: Įvertinimų ir atsiliepimų tvarkymas
description: Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027247"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="ac45c-103">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="ac45c-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac45c-104">Šioje temoje paaiškinama, kaip tvarkyti įvertinimus ir apžvalgas naudojant „Microsoft Dynamics 365 Commerce“ įvertinimų ir apžvalgų moderavimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="ac45c-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="ac45c-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ac45c-105">Overview</span></span>

<span data-ttu-id="ac45c-106">„Dynamics 365 Commerce“ naudojama „Microsoft Azure“ pažinimo tarnyba automatiškai moderuoti atsiliepimo tekstą pašalinant keiksmažodžius.</span><span class="sxs-lookup"><span data-stu-id="ac45c-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="ac45c-107">Be to, moderatoriai gali naudoti įvertinimų ir apžvalgų moderavimo įrankį šioms neautomatinėms užduotims:</span><span class="sxs-lookup"><span data-stu-id="ac45c-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="ac45c-108">Moderuokite apžvalgas atsakydami į juos arba juos pašalindami.</span><span class="sxs-lookup"><span data-stu-id="ac45c-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="ac45c-109">Panaikinkite kliento apžvalgas klientui pateikus dėl to užklausą.</span><span class="sxs-lookup"><span data-stu-id="ac45c-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="ac45c-110">Visų produktų masinio importo įvertinimų ir apžvalgų duomenys į „Microsoft Power BI“ šabloną, kad įvertinimų ir atsiliepimų tendencijos galėtų būti analizuojamos.</span><span class="sxs-lookup"><span data-stu-id="ac45c-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="ac45c-111">Įvertinimų ir apžvalgų valdymo funkcijų prieiga</span><span class="sxs-lookup"><span data-stu-id="ac45c-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="ac45c-112">Norėdami pasiekti įvertinimų ir apžvalgų valdymo funkcijas „e-Commerce“ svetainės valdymo įrankyje, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-113">Prisijunkite prie [„Microsoft Lifecycle Services“ (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ac45c-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="ac45c-114">Atidarykite projektą, kuriame yra aplinka, kurioje norima paleisti el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="ac45c-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="ac45c-115">Skyriuje **Aplinkos** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="ac45c-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="ac45c-116">Skyriuje **Aplinkos funkcijos** pasirinkite **Mažmeninės prekybos valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="ac45c-117">Skirtuke **„e-Commerce“**, esančiame **Nuorodos**, pasirinkite **„e-Commerce“ svetainės valdymo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="ac45c-118">Apžvalgos skaitymas</span><span class="sxs-lookup"><span data-stu-id="ac45c-118">Read a review</span></span> 

1. <span data-ttu-id="ac45c-119">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ac45c-120">Norėdami filtruotiapžvalgas, kurios rodomos produkto ID, produkto pavadinime arba apžvalgos tekste, naudokite ieškos lauką, esantį viršutiniame dešiniajame puslapio kampe.</span><span class="sxs-lookup"><span data-stu-id="ac45c-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="ac45c-121">Papildomais filtrais galima riboti apžvalgas pagal laikotarpį, vertinimą, kanalą arba su būseną (pašalinta, atsakyta arba pranešta).</span><span class="sxs-lookup"><span data-stu-id="ac45c-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderavimo pagrindinis puslapis](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="ac45c-123">Atsakymas į apžvalgą</span><span class="sxs-lookup"><span data-stu-id="ac45c-123">Respond to a review</span></span> 

<span data-ttu-id="ac45c-124">Kartais klientai, kurie pirko produktą, pareiškia savo pasitenkinimą ar nepasitenkinimą, arba nesupranta, kaip naudoti produktą.</span><span class="sxs-lookup"><span data-stu-id="ac45c-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="ac45c-125">Kaip moderatorius galite paskelbti atsakymą į apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="ac45c-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="ac45c-126">Šis atsakymas rodomas kartu su apžvalga svetainėje.</span><span class="sxs-lookup"><span data-stu-id="ac45c-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="ac45c-127">Norėdami atsakyti į apžvalgą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-128">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ac45c-129">Suraskite ir pasirinkite apžvalgą, į kurį reikia atsakyti.</span><span class="sxs-lookup"><span data-stu-id="ac45c-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="ac45c-130">Dešiniojoje ypatybių srityje pasirinkite **Įtraukti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="ac45c-131">Įveskite atsakymo tekstą ir pavadinimą, kuris turi būti rodomas atsakytojui.</span><span class="sxs-lookup"><span data-stu-id="ac45c-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="ac45c-132">Numatytasis atsakytojo pavadinimas yra **Moderatorius**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="ac45c-133">Baigę pasirinkite **Skelbti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-133">When you've finished, select **Post response**.</span></span>

![Atsakymas į apžvalgą](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="ac45c-135">Apžvalgos šalinimas</span><span class="sxs-lookup"><span data-stu-id="ac45c-135">Take down a review</span></span> 

<span data-ttu-id="ac45c-136">Kartais dėl verslo priežasčių moderatoriai turi pašalinti klientų apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="ac45c-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="ac45c-137">Norėdami pašalinti apžvalgą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-138">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="ac45c-139">Suraskite ir pasirinkite apžvalgą, kurią reikia pašalinti.</span><span class="sxs-lookup"><span data-stu-id="ac45c-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="ac45c-140">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pašalinimo priežastį ir pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="ac45c-141">Kliento apžvalgų naikinimas klientui pateikus užklausą</span><span class="sxs-lookup"><span data-stu-id="ac45c-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="ac45c-142">Kartais klientai nori, kad jų įvertinimų ir apžvalgų duomenys būtų visam laikui panaikinti iš el. prekybos svetainės.</span><span class="sxs-lookup"><span data-stu-id="ac45c-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="ac45c-143">Moderatorius, gavęs pašalinimo užklausą iš kliento, gali pašalinti kliento duomenis naudodamas apžvalgos naikinimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="ac45c-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="ac45c-144">Norint surasti ir panaikinti kliento duomenis, moderatoriui reikia el. pašto adreso, kurį klientas naudojo prisijungdamas ir pateikdamas apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="ac45c-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="ac45c-145">Norėdami rasti ir panaikinti kliento duomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-146">Eikite į **Pagrindinis \> Apžvalgos \>Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="ac45c-147">Lauke **Ieškoti vartotojų pagal el. pašto adresą** įveskite kliento el. pašto adresą ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="ac45c-148">Jei klientas atliko apžvalgos veiklų (pavyzdžiui, atsiliepimų teikimas, balsavimai, kiek kito kliento atsiliepimai buvo naudingi, arba komentavimas apie kito kliento atsiliepimą), rezultatai rodomi.</span><span class="sxs-lookup"><span data-stu-id="ac45c-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="ac45c-149">Kiekviename elemente yra mygtukas **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="ac45c-150">Kiekvienam elementui, kurį reikia naikinti, pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="ac45c-151">Kai būsite paraginti patvirtinti, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Kliento duomenų naikinimas](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="ac45c-153">Norint, kad duomenys būtų visiškai pašalinti iš sistemos, tai gali užtrukti iki septynių dienų.</span><span class="sxs-lookup"><span data-stu-id="ac45c-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="ac45c-154">Moderatoriai turėtų informuoti klientus apie šį vėlavimą.</span><span class="sxs-lookup"><span data-stu-id="ac45c-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="ac45c-155">Jei klientai pakeitė savo pavadinimą savo paskyros parametruose, ieškos rezultatuose gali būti rodomi keli elementai.</span><span class="sxs-lookup"><span data-stu-id="ac45c-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="ac45c-156">Šiuo atveju, kad būtų visiškai panaikinti kliento duomenys, moderatorius turi pasirinkti **Naikinti** kiekvienam elementui.</span><span class="sxs-lookup"><span data-stu-id="ac45c-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="ac45c-157">Įvertinimų ir apžvalgų duomenų atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="ac45c-157">Download ratings and reviews data</span></span>

<span data-ttu-id="ac45c-158">Įvertinimų ir apžvalgų moderavimo įrankiu moderatoriai gali importuoti įvertinimų ir atsiliepimų duomenis masiškai, kad jie galėtų analizuoti tendencijas.</span><span class="sxs-lookup"><span data-stu-id="ac45c-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="ac45c-159">Galimas „Power BI“ šablonas, kuriame yra pagrindinė metrika.</span><span class="sxs-lookup"><span data-stu-id="ac45c-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="ac45c-160">Moderatoriai gali naudoti šį šabloną masiškai importuotiems duomenims sujungti ir peržiūrėti ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="ac45c-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="ac45c-161">Jiems nebūtina sukurti tinkintą ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="ac45c-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="ac45c-162">Moderatoriai taip pat gali tinkinti „Power BI“ šabloną, kad patenkintų konkrečius poreikius.</span><span class="sxs-lookup"><span data-stu-id="ac45c-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="ac45c-163">Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-164">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ac45c-165">Norėdami atsisiųsti įvertinimų ir apžvalgų duomenis kableliais atskirtų reikšmių (CSV) formatu, pasirinkite **Atsisiųsti apžvalgų duomenis**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="ac45c-166">Įvertinimų ir apžvalgų tendencijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="ac45c-166">View ratings and reviews trends</span></span>

<span data-ttu-id="ac45c-167">Moderatoriai gali atsisiųsti „Power BI“ šabloną, kad galėtų peržiūrėti tendencijas ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="ac45c-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="ac45c-168">Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ac45c-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="ac45c-169">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="ac45c-170">Pasirinkite **„PowerBI“ šablonas**, kad atsisiųstumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="ac45c-170">Select **PowerBI template** to download the template.</span></span>

    ![„Power BI“ šablono atsisiuntimas](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="ac45c-172">Atidarykite atsisiųstą šabloną naudojantis „Power BI“ programėle.</span><span class="sxs-lookup"><span data-stu-id="ac45c-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="ac45c-173">Uždarykite pasirodžiusį dialogo langą **Prieiga prie interneto turinio** ir uždarykite pasirodžiusį klaidos pranešimą „Atnaujinti“.</span><span class="sxs-lookup"><span data-stu-id="ac45c-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="ac45c-174">Eikite į **Pagrindinis**, pasirinkite **Redaguoti užklausas** ir pasirinkite **Duomenų šaltinio parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="ac45c-175">Dialogo lange **Duomenų šaltinio parametrai** pasirinkite **Keisti šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="ac45c-176">Lauke **URL** įveskite apžvalgų duomenų, kuriuos atsisiuntėte ankstesne procedūra, maršrutą (pvz., **c:\\apžvalgos\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="ac45c-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Kableliais atskirtų reikšmių dialogo lango URL laukas](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="ac45c-178">Pasirinkite **Gerai**, tada – **Taikyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="ac45c-179">Užtruks nuo vienos iki dviejų minučių, kol jūsų keitimai bus pritaikyti duomenų šaltinyje.</span><span class="sxs-lookup"><span data-stu-id="ac45c-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="ac45c-180">Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, pasirinkite **Tendencijų lapas**.</span><span class="sxs-lookup"><span data-stu-id="ac45c-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Įvertinimų ir apžvalgų tendencijos](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="ac45c-182">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ac45c-182">Additional resources</span></span>

[<span data-ttu-id="ac45c-183">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ac45c-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="ac45c-184">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="ac45c-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="ac45c-185">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ac45c-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="ac45c-186">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="ac45c-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
