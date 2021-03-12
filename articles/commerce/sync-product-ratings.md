---
title: „Dynamics 365 Commerce“ produktų įvertinimų sinchronizavimas
description: Šioje temoje aprašoma, kaip sinchronizuoti produktų įvertinimus naudojant „Microsoft Dynamics 365 Commerce“.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006290"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="f424f-103">„Dynamics 365 Commerce“ produktų įvertinimų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="f424f-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f424f-104">Šioje temoje aprašoma, kaip sinchronizuoti produktų įvertinimus naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="f424f-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f424f-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="f424f-105">Overview</span></span>

<span data-ttu-id="f424f-106">Norint produktų įvertinimus naudoti daugiakanaliuose, pvz., elektroniniame kasos aparate (EKA) ir skambučių centruose, produktų įvertinimus iš vertinimų ir atsiliepimų paslaugos reikia importuoti į „Commerce“ kanalo duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="f424f-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="f424f-107">Kai produktų įvertinimai pateikiami daugiakanaliuose, jie gali netiesiogiai padėti klientams bendraujant su pardavimo darbuotojais.</span><span class="sxs-lookup"><span data-stu-id="f424f-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="f424f-108">Šioje temoje aprašomos toliau nurodytos užduotys.</span><span class="sxs-lookup"><span data-stu-id="f424f-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="f424f-109">Konfigūruokite **Produkto įvertinimų sinchronizavimo užduotį** kaip paketinę užduotį, kad galėtumėte sinchronizuoti produktų įvertinimus iš **Vertinimų ir atsiliepimų paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="f424f-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="f424f-110">Patikrinkite, ar produkto vertinimų sinchronizavimo paketinė užduotis sėkmingai įvykdyta.</span><span class="sxs-lookup"><span data-stu-id="f424f-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="f424f-111">Produkto įvertinimus pateikite EKA.</span><span class="sxs-lookup"><span data-stu-id="f424f-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="f424f-112">Paketinės užduoties konfigūravimas produkto įvertinimams sinchronizuoti</span><span class="sxs-lookup"><span data-stu-id="f424f-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f424f-113">Prieš pradėdami įsitikinkite, kad įdiegta „Dynamics 365 Commerce“ 10.0.6 arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="f424f-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="f424f-114">Prekybos planuoklės inicijavimas</span><span class="sxs-lookup"><span data-stu-id="f424f-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="f424f-115">Norėdami inicijuoti prekybos planuoklę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f424f-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="f424f-116">Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Inicijuoti prekybos planuoklę**.</span><span class="sxs-lookup"><span data-stu-id="f424f-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="f424f-117">Taip pat galite ieškoti „Inicijuoti prekybos planuoklę“.</span><span class="sxs-lookup"><span data-stu-id="f424f-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="f424f-118">Dialogo lange **Inicijuoti prekybos planuoklę** patikrinkite, ar parinktis **Naikinti esamą konfigūraciją** nustatyta kaip **Ne**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f424f-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="f424f-119">Antrinės užduoties „RetailProductRating“ tikrinimas</span><span class="sxs-lookup"><span data-stu-id="f424f-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="f424f-120">Norėdami patikrinti, ar yra antrinė užduotis **RetailProductRating**, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f424f-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="f424f-121">Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Duomenų apsikeitimo valdymo antrinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="f424f-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="f424f-122">Taip pat galite ieškoti „duomenų apsikeitimo valdymo antrinės užduotys“.</span><span class="sxs-lookup"><span data-stu-id="f424f-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="f424f-123">Antrinių užduočių sąraše raskite antrinę užduotį **RetailProductRating** arba jos ieškokite.</span><span class="sxs-lookup"><span data-stu-id="f424f-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="f424f-124">Toliau pateiktoje iliustracijoje rodomas išsamios antrinės užduoties informacijos programoje „Commerce“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f424f-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Išsami antrinės užduoties „RetailProductRating“ informacija](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="f424f-126">Jeigu antrinės užduoties **RetailProductRating** nerandate, galbūt užduotį **Produkto įvertinimų sinchronizavimas** ir užduotį **1040 CDX** įvykdėte prieš inicijuodami „Commerce” planuoklę.</span><span class="sxs-lookup"><span data-stu-id="f424f-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="f424f-127">Tokiu atveju atlikite toliau nurodytus veiksmus, kad vykdytumėte užduotį **Visas duomenų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="f424f-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="f424f-128">Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos planuoklė \> Kanalo duomenų bazė**.</span><span class="sxs-lookup"><span data-stu-id="f424f-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="f424f-129">Taip pat galite ieškoti „kanalo duomenų bazė“.</span><span class="sxs-lookup"><span data-stu-id="f424f-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="f424f-130">Pasirinkite kanalo duomenų bazę, kurią norite sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="f424f-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="f424f-131">Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="f424f-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="f424f-132">Išskleidžiamajame dialogo lange **Pasirinkti paskirstymo grafiką** pasirinkite **1040 – produktai**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f424f-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="f424f-133">Pakartokite pirmesnės procedūros veiksmus, kad patikrintumėte, ar buvo sukurta antrinė užduotis **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="f424f-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="f424f-134">Produkto įvertinimų importavimas</span><span class="sxs-lookup"><span data-stu-id="f424f-134">Import product ratings</span></span>

<span data-ttu-id="f424f-135">Norėdami produkto įvertinimus iš įvertinimų ir atsiliepimų tarnybos importuoti į „Commerce”, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f424f-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="f424f-136">Eikite į **Mažmeninė prekyba ir prekyba \> Valdymo sąranka \> Prekybos planuoklė \> Produkto įvertinimų sinchronizavimo užduotis**.</span><span class="sxs-lookup"><span data-stu-id="f424f-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="f424f-137">Taip pat galite ieškoti „produkto įvertinimų sinchronizavimo užduotis“.</span><span class="sxs-lookup"><span data-stu-id="f424f-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="f424f-138">Dialogo lango **Gauti produkto įvertinimus** „FastTab“ **Vykdyti fone** pasirinkite **Pasikartojimas**.</span><span class="sxs-lookup"><span data-stu-id="f424f-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="f424f-139">Dialogo lange **Nustatyti pasikartojimą** nustatykite pasikartojimo modelį.</span><span class="sxs-lookup"><span data-stu-id="f424f-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="f424f-140">(Siūloma reikšmė yra dvi valandos.) Neplanuokite pasikartojimo, kuris yra mažesnis nei viena valanda.</span><span class="sxs-lookup"><span data-stu-id="f424f-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="f424f-141">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f424f-141">Select **OK**.</span></span>
1. <span data-ttu-id="f424f-142">Parinktį **Paketinis vykdymas** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f424f-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="f424f-143">Šis parametras padeda užtikrinti, kad galėsite tikrinti žurnalus ir paketinių užduočių vykdymo būseną.</span><span class="sxs-lookup"><span data-stu-id="f424f-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="f424f-144">Norėdami suplanuoti paketinę užduotį pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f424f-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="f424f-145">Toliau pateiktoje iliustracijoje rodomas antrinės užduoties konfigūracijos programoje „Commerce“ pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f424f-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Produkto įvertinimų sinchronizavimo paketinės užduoties konfigūracija](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="f424f-147">Tikrinimas, ar produkto įvertinimų sinchronizavimo paketinė užduotis buvo sėkmingai įvykdyta</span><span class="sxs-lookup"><span data-stu-id="f424f-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="f424f-148">Norėdami patikrinti, ar paketinė užduotis **Produkto įvertinimų sinchronizavimas** buvo sėkmingai įvykdyta, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f424f-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="f424f-149">Eikite į dalį **Mažmeninė prekyba ir prekyba \> Sistemos administratorius \> Užklausos \> Paketinės užduotys**, arba, jei naudojate tik prekybos sandėliavimo vienetą (SKU), eikite į dalį **Mažmeninė prekyba ir prekyba \> Užklausos ir ataskaitos \> Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="f424f-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="f424f-150">Taip pat galite ieškoti „paketinės užduotys“.</span><span class="sxs-lookup"><span data-stu-id="f424f-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="f424f-151">Norėdami peržiūrėti išsamią paketinės užduoties informaciją, paketinių užduočių sąrašo stulpelyje **Užduoties aprašymas** ieškokite aprašymo, kuriame yra „Gauti produkto įvertinimus“.</span><span class="sxs-lookup"><span data-stu-id="f424f-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="f424f-152">Pasirinkite užduoties ID, kad peržiūrėtumėte išsamią paketinės užduoties informaciją, pvz., suplanuotą pradžios datą ir (arba) laiką ir pasikartojimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="f424f-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="f424f-153">Toliau pateiktoje iliustracijoje parodytas išsamios paketinės užduoties informacijos programoje „Commerce“ pavyzdys, kai paketinė užduotis suplanuota vykdyti kas dvi valandas.</span><span class="sxs-lookup"><span data-stu-id="f424f-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Produkto įvertinimų sinchronizavimo paketinės užduoties išsami informacija](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="f424f-155">Produkto įvertinimų pateikimas EKA</span><span class="sxs-lookup"><span data-stu-id="f424f-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="f424f-156">„Dynamics 365 Commerce“ įvertinimų ir atsiliepimų sprendimas yra daugiakanalis sprendimas.</span><span class="sxs-lookup"><span data-stu-id="f424f-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="f424f-157">Tačiau pagal numatytuosius nustatymus produktų įvertinimai EKA nerodomi.</span><span class="sxs-lookup"><span data-stu-id="f424f-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="f424f-158">Norėdami, kad klientai parduotuvėse, kai juos aptarnauja pardavimo darbuotojai, matytų įvertinimus ir atsiliepimus, EKA turite įjungti produkto įvertinimus.</span><span class="sxs-lookup"><span data-stu-id="f424f-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="f424f-159">Norėdami EKA įjungti produkto įvertinimus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f424f-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="f424f-160">Eikite į **Mažmeninė prekyba ir prekyba \> Prekybos sąranka \> Parametrai \> Commerce parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f424f-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="f424f-161">Taip pat galite ieškoti „Commerce“ parametrai“.</span><span class="sxs-lookup"><span data-stu-id="f424f-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="f424f-162">Skirtuke **Konfigūracijos parametrai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f424f-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="f424f-163">Įveskite pavadinimą, pavyzdžiui, **RatingsAndReviews.EnableProductRatingsForRetailStores** ir nustatykite reikšmę **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="f424f-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="f424f-164">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f424f-164">Select **Save**.</span></span>
1. <span data-ttu-id="f424f-165">Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="f424f-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="f424f-166">Taip pat galite ieškoti „paskirstymo grafikas“.</span><span class="sxs-lookup"><span data-stu-id="f424f-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="f424f-167">Užduočių sąraše pasirinkite **1110** (**visuotinė konfigūracija**), tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="f424f-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="f424f-168">Sėkmingai įvykdžius užduotį patikrinkite, ar dabar produktų įvertinimai rodomi EKA.</span><span class="sxs-lookup"><span data-stu-id="f424f-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="f424f-169">Toliau pateiktame paveikslėlyje parodytas „Commerce“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f424f-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![„Commerce“ parametrų konfigūracijos norint EKA įjungti produkto įvertinimus pavyzdys](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="f424f-171">Tolesnėje iliustracijoje pateikiamas produkto įvertinimų EKA pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f424f-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Produkto įvertinimai EKA](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="f424f-173">Toliau pateiktoje iliustracijoje pateikiamas produkto įvertinimų skambučių centro kanaluose pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f424f-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Produkto įvertinimai skambučių centro kanale](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="f424f-175">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f424f-175">Additional resources</span></span>

[<span data-ttu-id="f424f-176">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="f424f-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f424f-177">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="f424f-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f424f-178">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="f424f-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f424f-179">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f424f-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
