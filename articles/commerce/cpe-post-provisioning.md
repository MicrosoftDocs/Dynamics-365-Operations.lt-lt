---
title: „Dynamics 365 Commerce” peržiūros aplinkos konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti parengtą „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024711"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="b7b05-103">„Dynamics 365 Commerce” peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b7b05-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b7b05-104">Šioje temoje paaiškinama, kaip sukonfigūruoti parengtą „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="b7b05-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="b7b05-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b7b05-105">Overview</span></span>

<span data-ttu-id="b7b05-106">Šios temos procedūras atlikite tik tada, kai „Commerce“ peržiūros aplinka yra parengta.</span><span class="sxs-lookup"><span data-stu-id="b7b05-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="b7b05-107">Informacijos apie tai, kaip parengti „Commerce“ peržiūros aplinką, rasite temoje [„Commerce“ peržiūros aplinkos parengimas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b7b05-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="b7b05-108">Kai „Commerce“ peržiūros aplinka visapusiškai parengta, pradėti ją vertinti galėsite tik atlikę papildomus po parengimo atliekamus konfigūravimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="b7b05-109">Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), „Dynamics 365 Commerce“ ir „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="b7b05-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="b7b05-110">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="b7b05-110">Before you start</span></span>

1. <span data-ttu-id="b7b05-111">Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="b7b05-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="b7b05-112">Nueikite į savo projektą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-112">Go to your project.</span></span>
1. <span data-ttu-id="b7b05-113">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b7b05-114">Sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="b7b05-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="b7b05-115">Dešinėje esančioje informacijos apie aplinką srityje pasirinkite **Visa informacija**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="b7b05-116">Pasirinkite **Prisijungimas**, kad atidarytumėte meniu, tada – **Įeiti į aplinką**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="b7b05-117">Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="b7b05-118">Elektroninio kasos aparato konfigūravimas portale LCS</span><span class="sxs-lookup"><span data-stu-id="b7b05-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="b7b05-119">Darbuotojo susiejimas su jūsų tapatybe</span><span class="sxs-lookup"><span data-stu-id="b7b05-119">Associate a worker with your identity</span></span>

<span data-ttu-id="b7b05-120">Norėdami susieti darbuotoją su jūsų tapatybe portale LCS, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b7b05-121">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Darbuotojai \> Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="b7b05-122">Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="b7b05-123">Veiksmų srityje pasirinkite **„Retail“**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="b7b05-124">Pasirinkite **Susieti esamą tapatybę**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="b7b05-125">Lauko **Ieškoti naudojant el. paštą** dešinėje esančiame lauke **El. paštas** įveskite savo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="b7b05-126">Pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-126">Select **Search**.</span></span>
1. <span data-ttu-id="b7b05-127">Pasirinkite įrašą su savo vardu.</span><span class="sxs-lookup"><span data-stu-id="b7b05-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="b7b05-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-128">Select **OK**.</span></span>
1. <span data-ttu-id="b7b05-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="b7b05-130">Aktyvinti debesies EKA</span><span class="sxs-lookup"><span data-stu-id="b7b05-130">Activate Cloud POS</span></span>

<span data-ttu-id="b7b05-131">Norėdami portale LCS aktyvinti debesies EKA, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b7b05-132">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b7b05-133">Sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="b7b05-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="b7b05-134">Dešinėje esančioje informacijos apie aplinką srityje pasirinkite **Visa informacija**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="b7b05-135">Pasirinkite **Prisijungti**, kad atidarytumėte meniu, tada – **Įeiti į debesies elektroninį kasos aparatą**, kad atidarytumėte elektroninį kasos aparatą (EKA).</span><span class="sxs-lookup"><span data-stu-id="b7b05-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="b7b05-136">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-136">Select **Next**.</span></span>
1. <span data-ttu-id="b7b05-137">Prisijunkite naudodami savo „Microsoft Azure Active Directory“ („Azure AD“) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="b7b05-138">Dalyje **Parduotuvės pavadinimas**pasirinkite **San Fransiskas**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="b7b05-139">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-139">Select **Next**.</span></span>
1. <span data-ttu-id="b7b05-140">Dalyje **Registras ir įrenginys**pasirinkite **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="b7b05-141">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-141">Select **Activate**.</span></span> <span data-ttu-id="b7b05-142">Esate atjungiami ir nukreipiami į EKA prisijungimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="b7b05-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="b7b05-143">Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="b7b05-144">Svetainės nustatymas programoje „Commerce“</span><span class="sxs-lookup"><span data-stu-id="b7b05-144">Set up your site in Commerce</span></span>

<span data-ttu-id="b7b05-145">Norėdami pradėti nustatyti peržiūros svetainę programoje „Commerce“, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b7b05-146">Prisijunkite prie svetainių valdymo įrankio naudodami URL, kurį pasižymėjote inicijuodami el. prekybą jos konfigūravimo metu (žr. [El. prekybos inicijavimas](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="b7b05-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b7b05-147">Pasirinkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="b7b05-148">Pasirinkite domeną, kurį įvedėte inicijuodami el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="b7b05-149">Kaip numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="b7b05-150">(Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę.)</span><span class="sxs-lookup"><span data-stu-id="b7b05-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="b7b05-151">Kaip numatytąją kalbą pasirinkite **lt-lt**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="b7b05-152">Lauko **Kelias** reikšmę palikite tokią, kokia yra.</span><span class="sxs-lookup"><span data-stu-id="b7b05-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="b7b05-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-153">Select **OK**.</span></span> <span data-ttu-id="b7b05-154">Atsiranda svetainės puslapių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b7b05-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="b7b05-155">Užduočių įjungimas programoje „Retail“</span><span class="sxs-lookup"><span data-stu-id="b7b05-155">Enable jobs in Retail</span></span>

<span data-ttu-id="b7b05-156">Norėdami programoje „Retail“ įjungti užduotis, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="b7b05-157">Prisijunkite prie aplinkos (būstinėje).</span><span class="sxs-lookup"><span data-stu-id="b7b05-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="b7b05-158">Naudodami kairėje esantį meniu, nueikite į **„Retail“ \> Užklausos ir ataskaitos \> Paketines užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="b7b05-159">Likusius šios procedūros veiksmus reikia atlikti su kiekviena iš tolesnių užduočių.</span><span class="sxs-lookup"><span data-stu-id="b7b05-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="b7b05-160">Apdoroti mažmeninės prekybos el. paštu siunčiamą pranešimą</span><span class="sxs-lookup"><span data-stu-id="b7b05-160">Process retail order email notification</span></span>
    * <span data-ttu-id="b7b05-161">Produkto prieinamumas</span><span class="sxs-lookup"><span data-stu-id="b7b05-161">Product availability</span></span>
    * <span data-ttu-id="b7b05-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="b7b05-162">P-0001</span></span>
    * <span data-ttu-id="b7b05-163">Užsakymų sinchronizavimo užduotis</span><span class="sxs-lookup"><span data-stu-id="b7b05-163">Synchronize orders job</span></span>

1. <span data-ttu-id="b7b05-164">Naudodami spartųjį filtrą, užduoties galite ieškoti pagal pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="b7b05-165">Jei užduoties būsena yra **Sulaikyta**, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="b7b05-166">Pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-166">Select the record.</span></span>
    1. <span data-ttu-id="b7b05-167">Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="b7b05-168">Pasirinkite **Laukiama**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="b7b05-169">Visų duomenų sinchronizavimas programoje „Retail“</span><span class="sxs-lookup"><span data-stu-id="b7b05-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="b7b05-170">Norėdami sinchronizuoti visus duomenis programoje „Retail“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7b05-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="b7b05-171">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Būstinės sąranka \> Duomenų apsikeitimo valdymas \> Kanalo duomenų bazė**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="b7b05-172">Kairėje esančiame sąraše pasirenkamas kanalas **Numatytasis**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="b7b05-173">Pasirinkite kitą galimą kanalą.</span><span class="sxs-lookup"><span data-stu-id="b7b05-173">Select the other available channel.</span></span> <span data-ttu-id="b7b05-174">Šio kanalas pavadinimas – **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="b7b05-175">Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="b7b05-176">Įveskite **9999** kaip paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="b7b05-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="b7b05-177">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-177">Select **OK**.</span></span>
1. <span data-ttu-id="b7b05-178">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b7b05-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="b7b05-179">Bandomosios kredito kortelės informacija bandomiesiems pirkimams atlikti</span><span class="sxs-lookup"><span data-stu-id="b7b05-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="b7b05-180">Norėdami svetainėje atlikti bandomąsias operacijas, galite naudoti tolesnę bandomosios kredito kortelės informaciją.</span><span class="sxs-lookup"><span data-stu-id="b7b05-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="b7b05-181">**Kortelės numeris:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="b7b05-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="b7b05-182">**Galiojimo pabaigos data:** 10/20</span><span class="sxs-lookup"><span data-stu-id="b7b05-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="b7b05-183">**Kortelės tikrinimo vertės (CVV) kodas:** 737</span><span class="sxs-lookup"><span data-stu-id="b7b05-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7b05-184">Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.</span><span class="sxs-lookup"><span data-stu-id="b7b05-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b7b05-185">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="b7b05-185">Next steps</span></span>

<span data-ttu-id="b7b05-186">Kai parengimo ir konfigūravimo veiksmai baigti, esate pasirengę vertinti peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="b7b05-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="b7b05-187">Naudodami „Commerce“ svetainių valdymo įrankio URL, galite pradėti naudoti kūrimo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b7b05-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="b7b05-188">Naudodami „Commerce“ svetainės URL, galite pradėti naudoti mažmeninės prekybos klientų svetainės funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b7b05-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="b7b05-189">Norėdami konfigūruoti pasirenkamas „Commerce“ peržiūros aplinkos funkcijas, žr. [Pasirenkamų „Commerce“ peržiūros aplinkos funkcijų konfigūravimas](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="b7b05-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7b05-190">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b7b05-190">Additional resources</span></span>

[<span data-ttu-id="b7b05-191">„Dynamics 365 Commerce“ peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="b7b05-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b7b05-192">„Dynamics 365 Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="b7b05-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b7b05-193">„Dynamics 365 Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b7b05-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b7b05-194">DUK apie „Dynamics 365 Commerce“ peržiūros aplinką</span><span class="sxs-lookup"><span data-stu-id="b7b05-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b7b05-195">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="b7b05-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b7b05-196">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b7b05-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b7b05-197">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="b7b05-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b7b05-198">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="b7b05-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
