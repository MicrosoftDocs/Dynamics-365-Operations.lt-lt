---
title: „Dynamics 365 Commerce“ vertinimo aplinkos konfigūravimas
description: Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje „Microsoft Dynamics 365 Commerce“ vertinimo aplinką, po to kai ji buvo parengta.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9b11ab600bb2aa17cf330947304f5b22dd522081
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477978"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="5fa5f-103">„Dynamics 365 Commerce“ vertinimo aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5fa5f-104">Šiame skyriuje paaiškinama, kaip sukonfigūruoti pirkimą internetu, pasiėmimą parduotuvėje „Microsoft Dynamics 365 Commerce“ vertinimo aplinką, po to kai ji buvo parengta.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="5fa5f-105">Pabaikite šio skyriaus procedūras po to, kai jūsų Komercijos vertinimo aplinka buvo parengta ir sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="5fa5f-106">Dėl informacijo, kaip nustatyti savo Komercijos vertinimo aplinką po jos nustatymo, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="5fa5f-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="5fa5f-107">Po to kai jūsų Komercijos vertinimo aplinka buvo parengta iki galo, papildomas jos parengimo konfigūravimo žingsniai turi būti pateikti iki tol, kol pradėsite vertinti aplinką.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="5fa5f-108">Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="5fa5f-109">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="5fa5f-109">Before you start</span></span>

1. <span data-ttu-id="5fa5f-110">Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="5fa5f-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="5fa5f-111">Nueikite į savo projektą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-111">Go to your project.</span></span>
1. <span data-ttu-id="5fa5f-112">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="5fa5f-113">Sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="5fa5f-114">Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie aplinkos**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="5fa5f-115">Būsite nukreipti į komercijos būstinę.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="5fa5f-116">Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="5fa5f-117">Po parengimo veiksmų komercijos būstinėje, įsitikinkite, kad **USRT** juridinis asmuo yra visuomet pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="5fa5f-118">Sukonfigūruokite prekybos tašką</span><span class="sxs-lookup"><span data-stu-id="5fa5f-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="5fa5f-119">Darbuotojo susiejimas su jūsų tapatybe</span><span class="sxs-lookup"><span data-stu-id="5fa5f-119">Associate a worker with your identity</span></span>

<span data-ttu-id="5fa5f-120">Tam, kad susietumėte darbuotoją su savo tapatybe, atlikite šiuos veiksmus Komercijos būstinėje.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="5fa5f-121">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Darbuotojai \> Darbininkai**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="5fa5f-122">Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="5fa5f-123">Veiksmų juostoje pasirinkite **Komercija**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="5fa5f-124">Pasirinkite **Susieti esamą tapatybę**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="5fa5f-125">Lauko **Ieškoti naudojant el. paštą** dešinėje esančiame lauke **El. paštas** įveskite savo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="5fa5f-126">Pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-126">Select **Search**.</span></span>
1. <span data-ttu-id="5fa5f-127">Pasirinkite įrašą su savo vardu.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="5fa5f-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-128">Select **OK**.</span></span>
1. <span data-ttu-id="5fa5f-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="5fa5f-130">Aktyvinti debesies EKA</span><span class="sxs-lookup"><span data-stu-id="5fa5f-130">Activate Cloud POS</span></span>

<span data-ttu-id="5fa5f-131">„Cloud POS“ įjungimui, atlikite šiuos veiksmus LCS.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="5fa5f-132">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="5fa5f-133">Sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="5fa5f-134">Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie debesies prekybos taško**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="5fa5f-135">Pasirinkite **Kitas** tam, kad atvertumėte **Prieš pradžią** teksto laukelį.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="5fa5f-136">Palikite **Serverio URL** laukelį tokį, koks yra.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="5fa5f-137">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-137">Select **Next**.</span></span>
1. <span data-ttu-id="5fa5f-138">Prisijunkite naudodami savo „Microsoft Azure Active Directory“ („Azure AD“) paskyrą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="5fa5f-139">**Parduotuvės pavadinimo** laukelyje pasirinkite **San Franciskas** ir tuomet pasirinkite **Kitas**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="5fa5f-140">Dalyje **Registras ir įrenginys** pasirinkite **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="5fa5f-141">Pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-141">Select **Activate**.</span></span> <span data-ttu-id="5fa5f-142">Esate atjungiami ir nukreipiami į EKA prisijungimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="5fa5f-143">Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="5fa5f-144">Svetainės nustatymas programoje „Commerce“</span><span class="sxs-lookup"><span data-stu-id="5fa5f-144">Set up your site in Commerce</span></span>

<span data-ttu-id="5fa5f-145">Jūsų vertinimo vietos komercijoje nustatymo pradžiai, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5fa5f-146">Prisijunkite prie vietos kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="5fa5f-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="5fa5f-147">Pasirinkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="5fa5f-148">Pasirinkite domeną, kurį įvedėte inicijuodami el. prekybą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="5fa5f-149">Kaip numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="5fa5f-150">(Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę.)</span><span class="sxs-lookup"><span data-stu-id="5fa5f-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="5fa5f-151">Kaip numatytąją kalbą pasirinkite **lt-lt**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="5fa5f-152">Lauko **Kelias** reikšmę palikite tokią, kokia yra.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="5fa5f-153">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-153">Select **OK**.</span></span> <span data-ttu-id="5fa5f-154">Atsiranda svetainės puslapių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="5fa5f-155">Užduočių įgalinimas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-155">Enable jobs</span></span>

<span data-ttu-id="5fa5f-156">Norėdami programoje „Commerce“ įjungti užduotis, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5fa5f-157">Prisijunkite prie aplinkos (būstinėje).</span><span class="sxs-lookup"><span data-stu-id="5fa5f-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="5fa5f-158">Naudodami kairėje esantį meniu, nueikite į **Mažmeninė prekyba ir prekyba \> Užklausos ir ataskaitos \> Paketines užduotys**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="5fa5f-159">Likusius šios procedūros veiksmus reikia atlikti su kiekviena iš tolesnių užduočių.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="5fa5f-160">Apdoroti mažmeninės prekybos el. paštu siunčiamą pranešimą</span><span class="sxs-lookup"><span data-stu-id="5fa5f-160">Process retail order email notification</span></span>
    * <span data-ttu-id="5fa5f-161">Produkto prieinamumas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-161">Product availability</span></span>
    * <span data-ttu-id="5fa5f-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="5fa5f-162">P-0001</span></span>
    * <span data-ttu-id="5fa5f-163">Užsakymų sinchronizavimo užduotis</span><span class="sxs-lookup"><span data-stu-id="5fa5f-163">Synchronize orders job</span></span>

1. <span data-ttu-id="5fa5f-164">Naudodami spartųjį filtrą, užduoties galite ieškoti pagal pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="5fa5f-165">Jei darbo būsena yra **Vykdoma**, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="5fa5f-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="5fa5f-166">Pasirinkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-166">Select the record.</span></span>
    1. <span data-ttu-id="5fa5f-167">Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="5fa5f-168">Pasirinkite **Atšaukti**, tuomet pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="5fa5f-169">Pasirinktinai, taip pat galite nustatyti sutapimo intervalą ties (1) minute šiems veiksmams:</span><span class="sxs-lookup"><span data-stu-id="5fa5f-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="5fa5f-170">Mažmenos užsakymo elektroninio pašto pranešimo darbo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-170">Process retail order email notification job</span></span>
* <span data-ttu-id="5fa5f-171">P-0001 darbas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-171">P-0001 job</span></span>
* <span data-ttu-id="5fa5f-172">Užsakymų sinchronizavimo užduotis</span><span class="sxs-lookup"><span data-stu-id="5fa5f-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="5fa5f-173">Vykdyti visą duomenų sinchronizavimą</span><span class="sxs-lookup"><span data-stu-id="5fa5f-173">Run full data synchronization</span></span>

<span data-ttu-id="5fa5f-174">Visų duomenų sinchronizavimo komercijoje vykdymui, atlikite šiuos veiksmus komercijos būstinėje.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="5fa5f-175">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos tvarkaraštis \> Kanalo duomenų bazė**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="5fa5f-176">Pasirinkite kanalą pavadinimu **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="5fa5f-177">Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="5fa5f-178">Įveskite **9999** kaip paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="5fa5f-179">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-179">Select **OK**.</span></span>
1. <span data-ttu-id="5fa5f-180">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="5fa5f-181">Bandomosios kredito kortelės informacija bandomiesiems pirkimams atlikti</span><span class="sxs-lookup"><span data-stu-id="5fa5f-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="5fa5f-182">Norėdami svetainėje atlikti bandomąsias operacijas, galite naudoti tolesnę bandomosios kredito kortelės informaciją.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="5fa5f-183">**Kortelės numeris:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="5fa5f-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="5fa5f-184">**Galiojimo pabaigos data:** 10/20</span><span class="sxs-lookup"><span data-stu-id="5fa5f-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="5fa5f-185">**Kortelės tikrinimo vertės (CVV) kodas:** 737</span><span class="sxs-lookup"><span data-stu-id="5fa5f-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fa5f-186">Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5fa5f-187">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="5fa5f-187">Next steps</span></span>

<span data-ttu-id="5fa5f-188">Po parengimo ir konfigūravimo žingsnių atlikimo, galite pradėti naudoti savo vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="5fa5f-189">Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į autorizavimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="5fa5f-190">Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į mažmenos kliento vietos patirtį.</span><span class="sxs-lookup"><span data-stu-id="5fa5f-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="5fa5f-191">Tam, kad sukonfigūruotumėte pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [Konfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="5fa5f-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fa5f-192">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5fa5f-192">Additional resources</span></span>

[<span data-ttu-id="5fa5f-193">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="5fa5f-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="5fa5f-194">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="5fa5f-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="5fa5f-195">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="5fa5f-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="5fa5f-196">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="5fa5f-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="5fa5f-197">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="5fa5f-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="5fa5f-198">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="5fa5f-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="5fa5f-199">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="5fa5f-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="5fa5f-200">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="5fa5f-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="5fa5f-201">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="5fa5f-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
