---
title: „Dynamics 365 Commerce“ vertinimo aplinkos parengimas
description: Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4414502"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="7602b-103">„Dynamics 365 Commerce“ vertinimo aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="7602b-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7602b-104">Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="7602b-105">Prieš pradedant konfigūraciją, rekomenduojame perskaityti šią temą, kad suprastumėte proceso eigą.</span><span class="sxs-lookup"><span data-stu-id="7602b-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="7602b-106">Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskyru jų prašymu.</span><span class="sxs-lookup"><span data-stu-id="7602b-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="7602b-107">Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7602b-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="7602b-108">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="7602b-108">Overview</span></span>

<span data-ttu-id="7602b-109">Tam, kad sėkmingai parengtumėte Komercijos vertinimo aplinką privalote sukurti projektą, kuris turi konkretų gaminio pavadinimą ir tipą.</span><span class="sxs-lookup"><span data-stu-id="7602b-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="7602b-110">Aplinka ir „Commerce Scale Unit“ (CSU) taip pat turi keletą specifinių parametrų, kuriuos privalote naudoti tikėdamiesi vėliau nustatyti „e-Commerce“.</span><span class="sxs-lookup"><span data-stu-id="7602b-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="7602b-111">Šioje temoje pateiktos instrukcijos aprašo visus žingsnius būtinus užbaigti jūsų privalomą naudoti parengimą ir parametrus.</span><span class="sxs-lookup"><span data-stu-id="7602b-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="7602b-112">Kai sėkmingai parengėte savo Komercijos vertinimo aplinką, privalote užbaigti keletą žingsnių po nustatymo tam, kad pasirengtumėte naudojimui.</span><span class="sxs-lookup"><span data-stu-id="7602b-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="7602b-113">Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti.</span><span class="sxs-lookup"><span data-stu-id="7602b-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="7602b-114">Visada galite atlikti pasirinktinius veiksmus vėliau.</span><span class="sxs-lookup"><span data-stu-id="7602b-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="7602b-115">Dėl informacijos, kaip konfigūruoti savo Komercijos vertinimo aplinką po jos parengimo, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7602b-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="7602b-116">Dėl informacijos, kaip konfigūruoti pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [CKonfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="7602b-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7602b-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="7602b-117">Prerequisites</span></span>

<span data-ttu-id="7602b-118">Toliau pateikti būtinieji komponentai privalo būti pritaikyti prieš jūsų Komercijos vertinimo aplinkos nustatymo:</span><span class="sxs-lookup"><span data-stu-id="7602b-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="7602b-119">Buvote priimtas į vertinimo programą ir jums suteiktos galimybės vertinimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="7602b-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="7602b-120">Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.</span><span class="sxs-lookup"><span data-stu-id="7602b-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="7602b-121">Esate „Microsoft Dynamics“ 365 partneris ar klientas ir galite sukurti „Dynamics 365 Commerce“ projektą.</span><span class="sxs-lookup"><span data-stu-id="7602b-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="7602b-122">Jūs turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos ir galite susisiekti su jos administratoriumi, kuris pagelbės jums esant poreikiui.</span><span class="sxs-lookup"><span data-stu-id="7602b-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="7602b-123">Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="7602b-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="7602b-124">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="7602b-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="7602b-125">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="7602b-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="7602b-126">(Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)</span><span class="sxs-lookup"><span data-stu-id="7602b-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="7602b-127">Atkreipiame dėmesį, kad šis sąrašas nėra baigtinis.</span><span class="sxs-lookup"><span data-stu-id="7602b-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="7602b-128">Jei turite problemų, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7602b-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="7602b-129">Parenkite savo Komercijos vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="7602b-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="7602b-130">Šios procedūros paaiškina, kaip galite parengti Komercijos vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="7602b-131">Po to, kai jas sėkmingai atliksite, Komercijos vertinimo aplinka bus parengta konfigūravimui.</span><span class="sxs-lookup"><span data-stu-id="7602b-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="7602b-132">Visos čia aprašytos veiklos vyksta LCS portale.</span><span class="sxs-lookup"><span data-stu-id="7602b-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="7602b-133">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="7602b-133">Create a new project</span></span>

<span data-ttu-id="7602b-134">Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7602b-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="7602b-135">LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.</span><span class="sxs-lookup"><span data-stu-id="7602b-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="7602b-136">Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7602b-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="7602b-137">Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="7602b-138">Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="7602b-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="7602b-139">Įveskite pavadinimą, aprašą ir pramonės šaką.</span><span class="sxs-lookup"><span data-stu-id="7602b-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="7602b-140">Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="7602b-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7602b-141">Lauke **Produkto versija** pasirinkite **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="7602b-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7602b-142">Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.</span><span class="sxs-lookup"><span data-stu-id="7602b-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="7602b-143">Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.</span><span class="sxs-lookup"><span data-stu-id="7602b-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="7602b-144">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-144">Select **Create**.</span></span> <span data-ttu-id="7602b-145">Pateikiamas projekto rodinys.</span><span class="sxs-lookup"><span data-stu-id="7602b-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="7602b-146">„Azure“ jungties įtraukimas</span><span class="sxs-lookup"><span data-stu-id="7602b-146">Add the Azure Connector</span></span>

<span data-ttu-id="7602b-147">„Azure Connector“ įtraukimui į savo LCS projektą, atlikite šiuos žingsnius [Baigtame „Azure Resource Manager“ (ARM) įtraukimo procese](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="7602b-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="7602b-148">Aplinkos diegimas</span><span class="sxs-lookup"><span data-stu-id="7602b-148">Deploy the environment</span></span>

<span data-ttu-id="7602b-149">Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="7602b-150">Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami.</span><span class="sxs-lookup"><span data-stu-id="7602b-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="7602b-151">Kai esate rodinyje **Aplinkos parametrai**, įsitikinkite, kad tekstas **Dynamics 365 Commerce – Demo (10.0.* x* su platformos atnaujinimu *xx*)\*\* rodomas tiesiai virš lauko **Aplinkos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="7602b-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="7602b-152">Norėdami gauti išsamesnės informacijos, žr. iliustraciją, pavaizduotą po 8 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="7602b-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="7602b-153">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7602b-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="7602b-154">Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="7602b-155">Lauke **Programos versija** pasirinkite naujausią versiją.</span><span class="sxs-lookup"><span data-stu-id="7602b-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="7602b-156">Jei norite pasirinkti ne naujausią programos versiją, nesirinkite versijos, ankstesnės nei versija **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="7602b-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="7602b-157">Lauke **Platformos versija** naudokite platformos versiją, kuri automatiškai parenkama jūsų pasirinktai programos versijai.</span><span class="sxs-lookup"><span data-stu-id="7602b-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. <span data-ttu-id="7602b-159">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="7602b-159">Select **Next**.</span></span>
1. <span data-ttu-id="7602b-160">Pasirinkite aplinkos topologiją **Demonstracinė versija**.</span><span class="sxs-lookup"><span data-stu-id="7602b-160">Select **Demo** as the environment topology.</span></span>

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. <span data-ttu-id="7602b-162">Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7602b-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="7602b-163">Nekeiskite išplėstinių parametrų.</span><span class="sxs-lookup"><span data-stu-id="7602b-163">Leave the advanced settings as they are.</span></span>

    ![Puslapis Diegti aplinką](./media/project4.png)

1. <span data-ttu-id="7602b-165">Pagal poreikį pakoreguokite VM dydį.</span><span class="sxs-lookup"><span data-stu-id="7602b-165">Adjust the VM size as required.</span></span> <span data-ttu-id="7602b-166">(Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)</span><span class="sxs-lookup"><span data-stu-id="7602b-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="7602b-167">Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.</span><span class="sxs-lookup"><span data-stu-id="7602b-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="7602b-168">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="7602b-168">Select **Next**.</span></span>
1. <span data-ttu-id="7602b-169">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="7602b-170">Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="7602b-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="7602b-171">Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama.</span><span class="sxs-lookup"><span data-stu-id="7602b-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="7602b-172">Aplinkos darbo eigoms užbaigti prireiks laiko.</span><span class="sxs-lookup"><span data-stu-id="7602b-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="7602b-173">Todėl patikrinkite vėl maždaug po šešių–devynių valandų.</span><span class="sxs-lookup"><span data-stu-id="7602b-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="7602b-174">Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="7602b-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="7602b-175">Inicijuoti „Commerce Scale Unit“ (debesyje)</span><span class="sxs-lookup"><span data-stu-id="7602b-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="7602b-176">Norėdami inicijuoti CSU, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7602b-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="7602b-177">Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="7602b-178">Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="7602b-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="7602b-179">Rodomas aplinkos išsamios informacijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="7602b-179">The environment details view appears.</span></span>
1. <span data-ttu-id="7602b-180">Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="7602b-181">Skirtuke **„Commerce“** pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="7602b-182">Rodomas CSU inicijavimo parametrų rodinys.</span><span class="sxs-lookup"><span data-stu-id="7602b-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="7602b-183">**Regiono** laukelyje pasirinkite tą patį regioną arba artimą regioną, kuriame įdiegėte savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7602b-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="7602b-184">Palikite **Versija** laukelį tokį, koks yra.</span><span class="sxs-lookup"><span data-stu-id="7602b-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="7602b-185">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="7602b-186">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7602b-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="7602b-187">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="7602b-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="7602b-188">Jūsų CSU jau buvo rengimo eilėje.</span><span class="sxs-lookup"><span data-stu-id="7602b-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="7602b-189">Prieš tęsdami įsitikinkite, kad jūsų CSU būsena yra **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="7602b-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="7602b-190">Inicijavimas trunka maždaug dvi–penkias valandas.</span><span class="sxs-lookup"><span data-stu-id="7602b-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="7602b-191">Jei negalite surasti **Tvarkyti** nuorodos aplinkos informacijos peržiūroje, susisiekite su savo „Microsoft“ pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7602b-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="7602b-192">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="7602b-192">Initialize e-Commerce</span></span>

<span data-ttu-id="7602b-193">Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7602b-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7602b-194">**e-Commerce** skirtuke peržiūrėkite vertinimo sutikimą ir tuomet pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="7602b-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="7602b-195">**„e-Commerce“ aplinkos pavadinimas** laukelyje, įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7602b-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="7602b-196">Būkite atsargūs, nes šis pavadinimas bus rodomas kai kuriuose URL nuorodose, kurios veda į jūsų „e-Commerce“ objektą.</span><span class="sxs-lookup"><span data-stu-id="7602b-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="7602b-197">Lauke **„Commerce Scale Unit“ pavadinimas** iš sąrašo pasirinkite savo CSU.</span><span class="sxs-lookup"><span data-stu-id="7602b-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="7602b-198">(Sąraše turėtų būti tik viena parinktis.)</span><span class="sxs-lookup"><span data-stu-id="7602b-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="7602b-199">**„e-Commerce“ geografija** laukelis nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="7602b-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="7602b-200">Pasirinkite **Pirmyn**, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="7602b-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="7602b-201">Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="7602b-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="7602b-202">**AAD saugos grupė sistemos administratoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai. </span><span class="sxs-lookup"><span data-stu-id="7602b-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7602b-203">Pasirinkite tinkamą saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="7602b-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="7602b-204">**AAD saugos grupė reitingavimo ir peržiūros moderatoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai. </span><span class="sxs-lookup"><span data-stu-id="7602b-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7602b-205">Pasirinkite tinkamą saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="7602b-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="7602b-206">Palikite **Reitingavimo ir peržiūros paslaugų įjungimas** parinktį nustatytą į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7602b-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="7602b-207">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7602b-207">Select **Initialize**.</span></span> <span data-ttu-id="7602b-208">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="7602b-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="7602b-209">„E-Commerce“ inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="7602b-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="7602b-210">Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.</span><span class="sxs-lookup"><span data-stu-id="7602b-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="7602b-211">Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.</span><span class="sxs-lookup"><span data-stu-id="7602b-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="7602b-212">**„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.</span><span class="sxs-lookup"><span data-stu-id="7602b-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="7602b-213">**Komercijos vietos kūrėjas** – Nuoroda į vietos valdymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="7602b-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7602b-214">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="7602b-214">Next steps</span></span>

<span data-ttu-id="7602b-215">Jūsų Komercijos vertinimo aplinkos parengimo ir konfigūravimo proceso tąsai, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7602b-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7602b-216">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7602b-216">Additional resources</span></span>

[<span data-ttu-id="7602b-217">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="7602b-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7602b-218">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="7602b-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7602b-219">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7602b-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="7602b-220">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7602b-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="7602b-221">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="7602b-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7602b-222">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="7602b-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7602b-223">„Commerce Scale Unit“ (debesyje)</span><span class="sxs-lookup"><span data-stu-id="7602b-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7602b-224">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="7602b-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7602b-225">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="7602b-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
