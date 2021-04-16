---
title: „Dynamics 365 Commerce” vertinimo aplinkos parengimas
description: Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19cedf01d1b916de785454d55448f41d1f5db1df
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792296"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="7e4dc-103">„Dynamics 365 Commerce” vertinimo aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="7e4dc-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e4dc-104">Ši tema paaiškina, kaip galite parengti „Microsoft Dynamics 365 Commerce“ vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="7e4dc-105">Prieš pradedant konfigūraciją, rekomenduojame perskaityti šią temą, kad suprastumėte proceso eigą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="7e4dc-106">Komercijos vertinimo aplinkos dažniausiai nėra prieinamos ir yra suteikiamos partneriams ir klientams atskiru jų prašymu.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="7e4dc-107">Dėl išsamesnės informacijos, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="7e4dc-108">Tam, kad sėkmingai parengtumėte Komercijos vertinimo aplinką privalote sukurti projektą, kuris turi konkretų gaminio pavadinimą ir tipą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="7e4dc-109">Aplinka ir „Commerce Scale Unit“ (CSU) taip pat turi keletą specifinių parametrų, kuriuos privalote naudoti tikėdamiesi vėliau nustatyti „e-Commerce“.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="7e4dc-110">Šioje temoje pateiktos instrukcijos aprašo visus žingsnius būtinus užbaigti jūsų privalomą naudoti parengimą ir parametrus.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="7e4dc-111">Kai sėkmingai parengėte savo Komercijos vertinimo aplinką, privalote užbaigti keletą žingsnių po nustatymo tam, kad pasirengtumėte naudojimui.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="7e4dc-112">Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="7e4dc-113">Visada galite atlikti pasirinktinius veiksmus vėliau.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="7e4dc-114">Dėl informacijos, kaip konfigūruoti savo Komercijos vertinimo aplinką po jos parengimo, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7e4dc-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="7e4dc-115">Dėl informacijos, kaip konfigūruoti pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [CKonfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="7e4dc-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7e4dc-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="7e4dc-116">Prerequisites</span></span>

<span data-ttu-id="7e4dc-117">Toliau pateikti būtinieji komponentai privalo būti pritaikyti prieš jūsų Komercijos vertinimo aplinkos nustatymo:</span><span class="sxs-lookup"><span data-stu-id="7e4dc-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="7e4dc-118">Buvote priimtas į vertinimo programą ir jums suteiktos galimybės vertinimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="7e4dc-119">Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="7e4dc-120">Esate „Microsoft Dynamics 365” partneris ar klientas ir galite sukurti „Dynamics 365 Commerce“ projektą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="7e4dc-121">Jūs turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos ir galite susisiekti su jos administratoriumi, kuris pagelbės jums esant poreikiui.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="7e4dc-122">Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="7e4dc-123">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="7e4dc-124">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="7e4dc-125">(Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="7e4dc-126">Atkreipiame dėmesį, kad šis sąrašas nėra baigtinis.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="7e4dc-127">Jei turite problemų, susisiekite su „Microsoft“ partnerio pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="7e4dc-128">Parenkite savo Komercijos vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="7e4dc-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="7e4dc-129">Šios procedūros paaiškina, kaip galite parengti Komercijos vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="7e4dc-130">Po to, kai jas sėkmingai atliksite, Komercijos vertinimo aplinka bus parengta konfigūravimui.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="7e4dc-131">Visos čia aprašytos veiklos vyksta LCS portale.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="7e4dc-132">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="7e4dc-132">Create a new project</span></span>

<span data-ttu-id="7e4dc-133">Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="7e4dc-134">LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="7e4dc-135">Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="7e4dc-136">Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="7e4dc-137">Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="7e4dc-138">Įveskite pavadinimą, aprašą ir pramonės šaką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="7e4dc-139">Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7e4dc-140">Lauke **Produkto versija** pasirinkite **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="7e4dc-141">Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="7e4dc-142">Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="7e4dc-143">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-143">Select **Create**.</span></span> <span data-ttu-id="7e4dc-144">Pateikiamas projekto rodinys.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="7e4dc-145">„Azure“ jungties įtraukimas</span><span class="sxs-lookup"><span data-stu-id="7e4dc-145">Add the Azure Connector</span></span>

<span data-ttu-id="7e4dc-146">„Azure Connector“ įtraukimui į savo LCS projektą, atlikite šiuos žingsnius [Baigtame „Azure Resource Manager“ (ARM) įtraukimo procese](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="7e4dc-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="7e4dc-147">Aplinkos diegimas</span><span class="sxs-lookup"><span data-stu-id="7e4dc-147">Deploy the environment</span></span>

<span data-ttu-id="7e4dc-148">Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="7e4dc-149">Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="7e4dc-150">Kai esate rodinyje **Aplinkos parametrai**, įsitikinkite, kad tekstas **Dynamics 365 Commerce – Demo (10.0.* x* su platformos atnaujinimu *xx*)\*\* rodomas tiesiai virš lauko **Aplinkos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="7e4dc-151">Norėdami gauti išsamesnės informacijos, žr. iliustraciją, pavaizduotą po 8 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="7e4dc-152">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="7e4dc-153">Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="7e4dc-154">Lauke **Programos versija** pasirinkite naujausią versiją.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="7e4dc-155">Jei norite pasirinkti ne naujausią programos versiją, nesirinkite versijos, ankstesnės nei versija **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="7e4dc-156">Lauke **Platformos versija** naudokite platformos versiją, kuri automatiškai parenkama jūsų pasirinktai programos versijai.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. <span data-ttu-id="7e4dc-158">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-158">Select **Next**.</span></span>
1. <span data-ttu-id="7e4dc-159">Pasirinkite aplinkos topologiją **Demonstracinė versija**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-159">Select **Demo** as the environment topology.</span></span>

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. <span data-ttu-id="7e4dc-161">Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="7e4dc-162">Nekeiskite išplėstinių parametrų.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-162">Leave the advanced settings as they are.</span></span>

    ![Puslapis Diegti aplinką](./media/project4.png)

1. <span data-ttu-id="7e4dc-164">Pagal poreikį pakoreguokite VM dydį.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-164">Adjust the VM size as required.</span></span> <span data-ttu-id="7e4dc-165">(Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="7e4dc-166">Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="7e4dc-167">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-167">Select **Next**.</span></span>
1. <span data-ttu-id="7e4dc-168">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="7e4dc-169">Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="7e4dc-170">Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="7e4dc-171">Aplinkos darbo eigoms užbaigti prireiks laiko.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="7e4dc-172">Todėl patikrinkite vėl maždaug po šešių–devynių valandų.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="7e4dc-173">Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="7e4dc-174">Inicijuoti „Commerce Scale Unit“ (debesyje)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="7e4dc-175">Norėdami pradėti CSU, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="7e4dc-176">Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="7e4dc-177">Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="7e4dc-178">Rodomas aplinkos išsamios informacijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-178">The environment details view appears.</span></span>
1. <span data-ttu-id="7e4dc-179">Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="7e4dc-180">Skirtuke **„Commerce“** pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="7e4dc-181">Rodomas CSU inicijavimo parametrų rodinys.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="7e4dc-182">**Regiono** laukelyje pasirinkite tą patį regioną arba artimą regioną, kuriame įdiegėte savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="7e4dc-183">Palikite **Versija** laukelį tokį, koks yra.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="7e4dc-184">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="7e4dc-185">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="7e4dc-186">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="7e4dc-187">Jūsų CSU jau buvo rengimo eilėje.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="7e4dc-188">Prieš tęsdami įsitikinkite, kad jūsų CSU būsena yra **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="7e4dc-189">Inicijavimas trunka maždaug dvi–penkias valandas.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="7e4dc-190">Jei negalite surasti **Tvarkyti** nuorodos aplinkos informacijos peržiūroje, susisiekite su savo „Microsoft“ pagalbos centru.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="7e4dc-191">Talpinimo proceso metu, galite gauti šią klaidos žinutę:</span><span class="sxs-lookup"><span data-stu-id="7e4dc-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="7e4dc-192">Demonstracinės ar testavimo aplinkos vertinimas turi būti registruojamas skalės vieneto jungties programoje \<application ID\> būstinėje.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="7e4dc-193">Jei CSU pradžia nepavyksta ir gaunate šią klaidos žinutę, užsirašykite programos ID, kuris bendrai yra unikalus identifikatorius (GUID) ir tuomet atlikite veiksmus kitame skyriuje siekiant registruoti CSU talpinimo programą „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="7e4dc-194">Registruokite CSU talpinimo programą „Commerce“ būstinėje (jei būtina)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="7e4dc-195">Norėdami registruoti CSU talpinimo programą „Commerce“ būstinėje, imkitės šių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7e4dc-196">„Commerce“ būstinėje, eikite į **Sistemos administravimas \> Nustatymai \> „Azure Active Directory“ programos**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="7e4dc-197">Stulpelyje **Kliento Id** įveskite programos ID iš CSU pradžios klaidos pranešimo, kurį gavote.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="7e4dc-198">Stulpelyje **Pavadinimas** įveskite bet kokį aprašantį tekstą (pavyzdžiui, **„CSU Eval“**).</span><span class="sxs-lookup"><span data-stu-id="7e4dc-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="7e4dc-199">Stulpelyje **Vartotojo ID** įveskite **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="7e4dc-200">Dar kartą bandykite CSU pradžia ir talpinimas iš LCS.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="7e4dc-201">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="7e4dc-201">Initialize e-Commerce</span></span>

<span data-ttu-id="7e4dc-202">Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7e4dc-203">**e-Commerce** skirtuke peržiūrėkite vertinimo sutikimą ir tuomet pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="7e4dc-204">**„e-Commerce“ aplinkos pavadinimas** laukelyje, įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="7e4dc-205">Būkite atsargūs, nes šis pavadinimas bus rodomas kai kuriuose URL nuorodose, kurios veda į jūsų „e-Commerce“ objektą.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="7e4dc-206">Lauke **„Commerce Scale Unit“ pavadinimas** iš sąrašo pasirinkite savo CSU.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="7e4dc-207">(Sąraše turėtų būti tik viena parinktis.)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="7e4dc-208">**„e-Commerce“ geografija** laukelis nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="7e4dc-209">Pasirinkite **Pirmyn**, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="7e4dc-210">Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="7e4dc-211">**AAD saugos grupė sistemos administratoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7e4dc-212">Pasirinkite tinkamą saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="7e4dc-213">**AAD saugos grupė reitingavimo ir peržiūros moderatoriui** laukelyje, pirmiausia įveskite kelias jūsų norimos naudoti saugos grupės pavadinimo raides ir tuomet pasirinkite didinamojo stiklo simbolį ieškos rezultatų peržiūrai.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="7e4dc-214">Pasirinkite tinkamą saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="7e4dc-215">Palikite **Reitingavimo ir peržiūros paslaugų įjungimas** parinktį nustatytą į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="7e4dc-216">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-216">Select **Initialize**.</span></span> <span data-ttu-id="7e4dc-217">Vėl rodomas rodinys **„Commerce“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="7e4dc-218">„E-Commerce“ inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="7e4dc-219">Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="7e4dc-220">Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="7e4dc-221">**„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="7e4dc-222">**Komercijos vietos kūrėjas** – Nuoroda į vietos valdymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="7e4dc-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7e4dc-223">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="7e4dc-223">Next steps</span></span>

<span data-ttu-id="7e4dc-224">Jūsų Komercijos vertinimo aplinkos parengimo ir konfigūravimo proceso tąsai, žr. [Komercijos vertinimo aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="7e4dc-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e4dc-225">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7e4dc-225">Additional resources</span></span>

[<span data-ttu-id="7e4dc-226">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="7e4dc-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7e4dc-227">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="7e4dc-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7e4dc-228">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7e4dc-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="7e4dc-229">Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="7e4dc-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="7e4dc-230">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="7e4dc-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7e4dc-231">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7e4dc-232">„Commerce Scale Unit“ (debesyje)</span><span class="sxs-lookup"><span data-stu-id="7e4dc-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7e4dc-233">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="7e4dc-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7e4dc-234">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="7e4dc-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
