---
title: „Microsoft Teams” parengimas iš „Dynamics 365 Commerce”
description: Šioje temoje aprašoma, kaip parengti „Microsoft Teams” naudojant organizacinius duomenis iš „Dynamics 365 Commerce”.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022451"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="f8e58-103">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="f8e58-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8e58-104">Šioje temoje aprašoma, kaip parengti „Microsoft Teams” naudojant organizacinius duomenis iš „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="f8e58-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f8e58-105">„Dynamics 365 Commerce” leidžia lengvai parengti „Teams”, jeigu ten dar nenustatėte komandų savo mažmeninės prekybos parduotuvėms.</span><span class="sxs-lookup"><span data-stu-id="f8e58-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="f8e58-106">Pasinaudodami gerai apibrėžtą informacija iš „Commerce”, kurią norite naudoti „Teams”, galite padėti savo parduotuvės darbuotojams pradėti naudotis „Teams” platforma.</span><span class="sxs-lookup"><span data-stu-id="f8e58-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="f8e58-107">Ši informacija apima organizacijos hierarchiją, parduotuvių pavadinimus, darbuotojų informaciją ir „Azure Active Directory” (Azure AD) abonementus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="f8e58-108">„Teams” parengimo procesas susideda iš dviejų pagrindinių žingsnių:</span><span class="sxs-lookup"><span data-stu-id="f8e58-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="f8e58-109">„Teams” platformoje sukurkite komandą kiekvienai mažmeninės prekybos parduotuvei ir kaip atitinkamos komandos narius įtraukite parduotuvės darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="f8e58-110">Jeigu darbuotojas yra susietas su daugiau nei viena mažmeninės prekybos parduotuve, komandos narystė atspindės šį faktą.</span><span class="sxs-lookup"><span data-stu-id="f8e58-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="f8e58-111">Užduočių publikavimui iš „Teams” palengvinimui bus sukurta komunikacijos komanda, kurios nariai bus regioniniai vadovai.</span><span class="sxs-lookup"><span data-stu-id="f8e58-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="f8e58-112">Įkelkite savo organizacijos hierarchiją iš „Commerce” į „Teams”.</span><span class="sxs-lookup"><span data-stu-id="f8e58-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="f8e58-113">„Teams” parengimas „Commerce” būstinėje</span><span class="sxs-lookup"><span data-stu-id="f8e58-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="f8e58-114">Prieš parengdami „Microsoft Teams”, atlikite šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="f8e58-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="f8e58-115">Patvirtinkite, kad visi regiono vadovai yra komunikacijos vadovai.</span><span class="sxs-lookup"><span data-stu-id="f8e58-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="f8e58-116">Patvirtinkite, kad kiekvieno parduotuvės vadovo ir darbininko „Azure” abonementas yra susietas su to vadovo arba darbininko darbuotojo įrašu „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="f8e58-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="f8e58-117">Norėdami parengti „Teams” platformą „Commerce“ būstinėje, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f8e58-118">Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f8e58-119">Veiksmų srityje pasirinkite **Komandų parengimas**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="f8e58-120">Sukuriama paketinė užduotis pavadinimu **Komandų parengimas**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="f8e58-121">Eikite į **Sistemos administravimas \> Užklausos \> Paketinės užduotys** ir suraskite naujausią užduotį, kurios aprašymas yra **Komandų parengimas**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="f8e58-122">Palaukite tol, kol ši užduotis bus baigta.</span><span class="sxs-lookup"><span data-stu-id="f8e58-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="f8e58-123">Jei nė vienas iš jūsų regiono vadovų, parduotuvių vadovų ir parduotuvės darbuotojų nėra susietas su „Teams” licencija, jūs galite gauti šį klaidos pranešimą: „Nepavyko nuskaityti vartotojui taikytinų Sku kategorijų.”</span><span class="sxs-lookup"><span data-stu-id="f8e58-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="f8e58-124">Norėdami išspręsti šią problemą, veiksmų srityje pasirinkite **Sinchronizuoti komandas ir narius**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="f8e58-125">„Teams” parengimo patvirtinimas „Teams” administravimo centre</span><span class="sxs-lookup"><span data-stu-id="f8e58-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="f8e58-126">Norėdami patvirtinti „Microsoft Teams” parengimą „Microsoft Teams” administravimo centre, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="f8e58-127">Eikite į [„Teams” administravimo centrą](https://admin.teams.microsoft.com/) ir prisijunkite kaip jūsų el. prekybos nuomotojo administratorius.</span><span class="sxs-lookup"><span data-stu-id="f8e58-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="f8e58-128">Kairiojoje naršymo srityje pasirinkite **Komandos** jų išplėtimui ir tada pasirinkite **Tvarkyti komandas**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="f8e58-129">Patvirtinkite, kad kiekvienai „Commerce” mažmeninės prekybos parduotuvei buvo sukurta viena komanda.</span><span class="sxs-lookup"><span data-stu-id="f8e58-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="f8e58-130">Pasirinkite komandą ir patvirtinkite, kad parduotuvės darbuotojai buvo įtraukti į ją kaip nariai.</span><span class="sxs-lookup"><span data-stu-id="f8e58-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="f8e58-131">Kairiojoje naršymo srityje pasirinkite **Vartotojai** ir patvirtinkite, kad visų parduotuvių visi darbuotojai buvo įtraukti kaip vartotojai.</span><span class="sxs-lookup"><span data-stu-id="f8e58-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="f8e58-132">Šioje iliustracijoje pateiktas „Teams” administravimo centro puslapio **Tvarkyti komandas** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f8e58-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![„Teams” administravimo centro puslapio Tvarkyti komandas pavyzdys](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="f8e58-134">Organizacijos hierarchijos įkėlimas iš „Commerce” į „Teams”</span><span class="sxs-lookup"><span data-stu-id="f8e58-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="f8e58-135">„Commerce” organizacijos hierarchija gali būti naudojama „Microsoft Teams” platformoje užduočių publikavimui visoms arba pasirinktoms parduotuvėms, naudojančioms tą pačią hierarchijos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="f8e58-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="f8e58-136">Norėdami įkelti „Commerce“ organizacijos hierarchiją į „Teams”, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="f8e58-137">„Commerce” būstinėje eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> „Microsoft Teams” integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="f8e58-138">Pasirinkite **Atsisiųsti tikslinę hierarchiją**, o tada pasirinkite **Mažmeninės prekybos parduotuvės pagal regioną** tam, kad atsisiųstumėte organizacijos hierarchijos kableliais atskirtų reikšmių (CSV) failą.</span><span class="sxs-lookup"><span data-stu-id="f8e58-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="f8e58-139">Įdiekite „Microsoft Teams PowerShell” modulį atlikdami skyriuje [„Microsoft Teams PowerShell” diegimas](/microsoftteams/teams-powershell-install) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="f8e58-140">Kai gausite raginimą „Teams PowerShell” lange, prisijunkite naudodami savo nuomotojo „Azure AD” administratoriaus abonementą.</span><span class="sxs-lookup"><span data-stu-id="f8e58-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="f8e58-141">Atlikite skyriuje [Jūsų komandos tikslinės hierarchijos nustatymas](/microsoftteams/set-up-your-team-hierarchy) nurodytus veiksmus, kad įkeltumėte tikslinės hierarchijos CSV failą.</span><span class="sxs-lookup"><span data-stu-id="f8e58-141">Follow the steps in [Set up your team targeting hierarchy](/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="f8e58-142">Patikrinkite, ar organizacijos hierarchija buvo įkelta į „Teams”</span><span class="sxs-lookup"><span data-stu-id="f8e58-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="f8e58-143">Norėdami patikrinti, ar organizacijos hierarchija buvo įkelta į „Microsoft Teams”, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8e58-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="f8e58-144">Prisijunkite prie „Teams” kaip komunikacijos vadovas.</span><span class="sxs-lookup"><span data-stu-id="f8e58-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="f8e58-145">Kairiojoje naršymo srityje pasirinkite **Planavimo priemonės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="f8e58-146">Skirtuke **Publikuoti sąrašai** sukurkite naują sąrašą, kuriame yra bandomųjų užduočių.</span><span class="sxs-lookup"><span data-stu-id="f8e58-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="f8e58-147">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="f8e58-147">Select **Publish**.</span></span> <span data-ttu-id="f8e58-148">Organizacijos hierarchija turėtų atsirasti dialogo lange **Pasirinkti, kas turi publikuoti**, kaip parodyta toliau pateiktos iliustracijos pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="f8e58-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Organizacijos hierarchijos pavyzdys dialogo lange „Pasirinkti, kam publikuoti”](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="f8e58-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f8e58-150">Additional resources</span></span>

[<span data-ttu-id="f8e58-151">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="f8e58-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f8e58-152">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="f8e58-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="f8e58-153">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="f8e58-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f8e58-154">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="f8e58-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="f8e58-155">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="f8e58-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="f8e58-156">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="f8e58-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)