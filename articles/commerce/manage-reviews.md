---
title: Įvertinimų ir atsiliepimų tvarkymas
description: Šioje temoje paaiškinama, kaip valdyti įvertinimus ir apžvalgas „Microsoft Dynamics 365 Commerce“ svetainių daryklėje.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a70d0526fb2443605a6b11df3ee281d4dd12f1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982571"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="0a23c-103">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="0a23c-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a23c-104">Šioje temoje paaiškinama, kaip valdyti įvertinimus ir apžvalgas „Microsoft Dynamics 365 Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="0a23c-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="0a23c-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="0a23c-105">Overview</span></span>

<span data-ttu-id="0a23c-106">„Dynamics 365 Commerce“ naudojama „Microsoft Azure“ pažinimo tarnyba automatiškai moderuoti atsiliepimo tekstą pašalinant keiksmažodžius.</span><span class="sxs-lookup"><span data-stu-id="0a23c-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="0a23c-107">Be to, moderatoriai gali naudoti „Dynamics 365 Commerce“ svetainių daryklę vykdyti šioms rankiniu būdu atliekamoms užduotims.</span><span class="sxs-lookup"><span data-stu-id="0a23c-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="0a23c-108">Moderuokite apžvalgas atsakydami į juos arba juos pašalindami.</span><span class="sxs-lookup"><span data-stu-id="0a23c-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="0a23c-109">Panaikinkite kliento apžvalgas klientui pateikus dėl to užklausą.</span><span class="sxs-lookup"><span data-stu-id="0a23c-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="0a23c-110">Visų produktų masinio importo įvertinimų ir apžvalgų duomenys į „Microsoft Power BI“ šabloną, kad įvertinimų ir atsiliepimų tendencijos galėtų būti analizuojamos.</span><span class="sxs-lookup"><span data-stu-id="0a23c-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="0a23c-111">Apžvalgos skaitymas</span><span class="sxs-lookup"><span data-stu-id="0a23c-111">Read a review</span></span> 

<span data-ttu-id="0a23c-112">Norėdami perskaityti atsiliepimą „Commerce“ svetainių daryklėje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-113">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="0a23c-114">Norėdami filtruotiapžvalgas, kurios rodomos produkto ID, produkto pavadinime arba apžvalgos tekste, naudokite ieškos lauką, esantį viršutiniame dešiniajame puslapio kampe.</span><span class="sxs-lookup"><span data-stu-id="0a23c-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="0a23c-115">Papildomais filtrais galima riboti apžvalgas pagal laikotarpį, vertinimą, kanalą arba su būseną (pašalinta, atsakyta arba pranešta).</span><span class="sxs-lookup"><span data-stu-id="0a23c-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Moderavimo pagrindinis puslapis](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="0a23c-117">Atsakymas į apžvalgą</span><span class="sxs-lookup"><span data-stu-id="0a23c-117">Respond to a review</span></span> 

<span data-ttu-id="0a23c-118">Kartais klientai, kurie pirko produktą, pareiškia savo pasitenkinimą ar nepasitenkinimą, arba nesupranta, kaip naudoti produktą.</span><span class="sxs-lookup"><span data-stu-id="0a23c-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="0a23c-119">Kaip moderatorius galite paskelbti atsakymą į apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="0a23c-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="0a23c-120">Šis atsakymas rodomas kartu su apžvalga svetainėje.</span><span class="sxs-lookup"><span data-stu-id="0a23c-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="0a23c-121">Norėdami atsakyti į atsiliepimą „Commerce“ svetainių daryklėje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-122">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="0a23c-123">Suraskite ir pasirinkite apžvalgą, į kurį reikia atsakyti.</span><span class="sxs-lookup"><span data-stu-id="0a23c-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="0a23c-124">Dešiniojoje ypatybių srityje pasirinkite **Įtraukti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="0a23c-125">Įveskite atsakymo tekstą ir pavadinimą, kuris turi būti rodomas atsakytojui.</span><span class="sxs-lookup"><span data-stu-id="0a23c-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="0a23c-126">Numatytasis atsakytojo pavadinimas yra **Moderatorius**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="0a23c-127">Baigę pasirinkite **Skelbti atsakymą**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-127">When you've finished, select **Post response**.</span></span>

![Atsakymas į apžvalgą](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="0a23c-129">Apžvalgos šalinimas</span><span class="sxs-lookup"><span data-stu-id="0a23c-129">Take down a review</span></span> 

<span data-ttu-id="0a23c-130">Kartais dėl verslo priežasčių moderatoriai turi pašalinti klientų apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="0a23c-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="0a23c-131">Norėdami pašalinti atsiliepimą „Commerce“ svetainių daryklėje, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-132">Eikite į **Pagrindinis \> Apžvalgos \>Moderavimas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="0a23c-133">Suraskite ir pasirinkite apžvalgą, kurią reikia pašalinti.</span><span class="sxs-lookup"><span data-stu-id="0a23c-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="0a23c-134">Dešinėje pusėje esančioje ypatybių srityje, dalyje **Šalinti apžvalgą**, pasirinkite pašalinimo priežastį, o tada pasirinkite **Pašalinti**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="0a23c-135">Kliento apžvalgų naikinimas klientui pateikus užklausą</span><span class="sxs-lookup"><span data-stu-id="0a23c-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="0a23c-136">Kartais klientai nori, kad jų įvertinimų ir apžvalgų duomenys būtų visam laikui panaikinti iš el. prekybos svetainės.</span><span class="sxs-lookup"><span data-stu-id="0a23c-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="0a23c-137">Moderatorius, gavęs pašalinimo užklausą iš kliento, gali pašalinti kliento duomenis naudodamas apžvalgos naikinimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="0a23c-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="0a23c-138">Norint surasti ir panaikinti kliento duomenis, moderatoriui reikia el. pašto adreso, kurį klientas naudojo prisijungdamas ir pateikdamas apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="0a23c-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="0a23c-139">Norėdami rasti ir panaikinti kliento duomenis „Commerce“ svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-140">Eikite į **Pagrindinis \> Apžvalgos \>Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="0a23c-141">Lauke **Ieškoti vartotojų pagal el. pašto adresą** įveskite kliento el. pašto adresą ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="0a23c-142">Jei klientas atliko apžvalgos veiklų (pavyzdžiui, atsiliepimų teikimas, balsavimai, kiek kito kliento atsiliepimai buvo naudingi, arba komentavimas apie kito kliento atsiliepimą), rezultatai rodomi.</span><span class="sxs-lookup"><span data-stu-id="0a23c-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="0a23c-143">Kiekviename elemente yra mygtukas **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="0a23c-144">Kiekvienam elementui, kurį reikia naikinti, pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="0a23c-145">Kai būsite paraginti patvirtinti, pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Kliento duomenų naikinimas](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="0a23c-147">Norint, kad duomenys būtų visiškai pašalinti iš sistemos, tai gali užtrukti iki septynių dienų.</span><span class="sxs-lookup"><span data-stu-id="0a23c-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="0a23c-148">Moderatoriai turėtų informuoti klientus apie šį vėlavimą.</span><span class="sxs-lookup"><span data-stu-id="0a23c-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="0a23c-149">Jei klientai pakeitė savo pavadinimą savo paskyros parametruose, ieškos rezultatuose gali būti rodomi keli elementai.</span><span class="sxs-lookup"><span data-stu-id="0a23c-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="0a23c-150">Šiuo atveju, kad būtų visiškai panaikinti kliento duomenys, moderatorius turi pasirinkti **Naikinti** kiekvienam elementui.</span><span class="sxs-lookup"><span data-stu-id="0a23c-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="0a23c-151">Įvertinimų ir apžvalgų duomenų atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="0a23c-151">Download ratings and reviews data</span></span>

<span data-ttu-id="0a23c-152">Naudodami „Commerce“ svetainių daryklę, moderatoriai gali importuoti įvertinimų ir atsiliepimų duomenis masiškai, kad galėtų analizuoti tendencijas.</span><span class="sxs-lookup"><span data-stu-id="0a23c-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="0a23c-153">Galimas „Power BI“ šablonas, kuriame yra pagrindinė metrika.</span><span class="sxs-lookup"><span data-stu-id="0a23c-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="0a23c-154">Moderatoriai gali naudoti šį šabloną masiškai importuotiems duomenims sujungti ir peržiūrėti ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="0a23c-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="0a23c-155">Jiems nebūtina sukurti tinkintą ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="0a23c-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="0a23c-156">Moderatoriai taip pat gali tinkinti „Power BI“ šabloną, kad patenkintų konkrečius poreikius.</span><span class="sxs-lookup"><span data-stu-id="0a23c-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="0a23c-157">Norėdami atsisiųsti įvertinimų ir atsiliepimų duomenis „Commerce“ svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-158">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="0a23c-159">Norėdami atsisiųsti įvertinimų ir atsiliepimų duomenis kableliais atskirtų reikšmių (CSV) formatu, pasirinkite **Atsisiųsti atsiliepimų duomenis**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="0a23c-160">Įvertinimų ir apžvalgų tendencijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="0a23c-160">View ratings and reviews trends</span></span>

<span data-ttu-id="0a23c-161">Moderatoriai gali atsisiųsti „Power BI“ šabloną, kad galėtų peržiūrėti tendencijas ataskaitų srityje.</span><span class="sxs-lookup"><span data-stu-id="0a23c-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="0a23c-162">Norėdami peržiūrėti įvertinimų ir atsiliepimų tendencijas „Commerce“ svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a23c-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0a23c-163">Eikite į **Pagrindinis \>Apžvalgos \> Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="0a23c-164">Pasirinkite **„PowerBI“ šablonas**, kad atsisiųstumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="0a23c-164">Select **PowerBI template** to download the template.</span></span>

    ![„Power BI“ šablono atsisiuntimas](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="0a23c-166">Atidarykite atsisiųstą šabloną naudojantis „Power BI“ programėle.</span><span class="sxs-lookup"><span data-stu-id="0a23c-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="0a23c-167">Uždarykite pasirodžiusį dialogo langą **Prieiga prie interneto turinio** ir uždarykite pasirodžiusį klaidos pranešimą „Atnaujinti“.</span><span class="sxs-lookup"><span data-stu-id="0a23c-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="0a23c-168">Eikite į **Pagrindinis**, pasirinkite **Redaguoti užklausas** ir pasirinkite **Duomenų šaltinio parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="0a23c-169">Dialogo lange **Duomenų šaltinio parametrai** pasirinkite **Keisti šaltinį**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="0a23c-170">Lauke **URL** įveskite apžvalgų duomenų, kuriuos atsisiuntėte ankstesne procedūra, maršrutą (pvz., **c:\\apžvalgos\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="0a23c-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Kableliais atskirtų reikšmių dialogo lango URL laukas](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="0a23c-172">Pasirinkite **Gerai**, tada – **Taikyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="0a23c-173">Užtruks nuo vienos iki dviejų minučių, kol jūsų keitimai bus pritaikyti duomenų šaltinyje.</span><span class="sxs-lookup"><span data-stu-id="0a23c-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="0a23c-174">Norėdami peržiūrėti įvertinimų ir apžvalgų tendencijas, pasirinkite **Tendencijų lapas**.</span><span class="sxs-lookup"><span data-stu-id="0a23c-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Įvertinimų ir apžvalgų tendencijos](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="0a23c-176">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0a23c-176">Additional resources</span></span>

[<span data-ttu-id="0a23c-177">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="0a23c-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="0a23c-178">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="0a23c-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="0a23c-179">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0a23c-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="0a23c-180">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="0a23c-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
