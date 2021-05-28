---
title: Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA
description: Šioje temoje aprašoma, kaip sinchronizuoti užduočių valdymą tarp „Microsoft Teams” ir „Dynamics 365 Commerce” elektroninio kasos aparato (EKA).
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
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020632"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="95352-103">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="95352-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95352-104">Šioje temoje aprašoma, kaip sinchronizuoti užduočių valdymą tarp „Microsoft Teams” ir „Dynamics 365 Commerce” elektroninio kasos aparato (EKA).</span><span class="sxs-lookup"><span data-stu-id="95352-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="95352-105">Vienas iš pagrindinių „Teams” integravimo tikslų yra užduočių sinchronizavimo tarp EKA programos ir „Teams” įgalinimas.</span><span class="sxs-lookup"><span data-stu-id="95352-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="95352-106">Tokiu būdu parduotuvės darbuotojai užduotims valdyti gali naudoti tiek EKA programą, tiek „Teams”, ir jiems nereikia perjungti programų.</span><span class="sxs-lookup"><span data-stu-id="95352-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="95352-107">Kadangi planavimo priemonė yra naudojama kaip „Teams” užduočių saugykla, todėl turi būti saitas tarp „Teams” ir „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="95352-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="95352-108">Šis saitas nustatomas naudojant konkretų plano ID tam tikrai parduotuvės komandai.</span><span class="sxs-lookup"><span data-stu-id="95352-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="95352-109">Toliau pateiktose procedūrose rodoma, kaip nustatyti užduočių valdymo sinchronizavimą tarp EKA ir „Teams” programų.</span><span class="sxs-lookup"><span data-stu-id="95352-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="95352-110">Testavimo užduočių sąrašo publikavimas „Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="95352-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="95352-111">Toliau pateiktoje procedūroje laikoma, kad jūsų parduotuvių komandos naudoja „Microsoft Teams” užduočių valdymo integravimą su „Commerce” pirmą kartą.</span><span class="sxs-lookup"><span data-stu-id="95352-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="95352-112">Norėdami publikuoti testavimo užduočių sąrašą „Teams” platformoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="95352-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="95352-113">Prisijunkite prie „Teams” kaip komunikacijos vadovas.</span><span class="sxs-lookup"><span data-stu-id="95352-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="95352-114">Įprastai, komunikacijos vadovai yra vartotojai, turintys **Regiono vadovo** vaidmenį „Commerce” platformoje.</span><span class="sxs-lookup"><span data-stu-id="95352-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="95352-115">Kairiojoje naršymo srityje pasirinkite **Planavimo priemonės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="95352-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="95352-116">Skirtuko **Publikuoti sąrašai** apatinėje kairėje dalyje pasirinkite **Naujas sąrašas** ir pavadinkite jį **Testavimo užduočių sąrašu**.</span><span class="sxs-lookup"><span data-stu-id="95352-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="95352-117">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="95352-117">Select **Create**.</span></span> <span data-ttu-id="95352-118">Naujas sąrašas rodomas dalyje **Juodraščiai**.</span><span class="sxs-lookup"><span data-stu-id="95352-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="95352-119">Prie **Užduoties pavadinimo** suteikite pirmajai užduočiai pavadinimą **„Teams” integravimo testavimas**.</span><span class="sxs-lookup"><span data-stu-id="95352-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="95352-120">Tada pasirinkite **Įvesti**.</span><span class="sxs-lookup"><span data-stu-id="95352-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="95352-121">Sąraše **Juodraščiai** pasirinkite užduočių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="95352-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="95352-122">Tada viršutiniame dešiniajame kampe pasirinkite  **Publikuoti** .</span><span class="sxs-lookup"><span data-stu-id="95352-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="95352-123">Dialogo lange **Pasirinkti, kam publikuoti** pažymėkite komandas, kurios turėtų gauti testavimo užduočių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="95352-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="95352-124">Pasirinkite **Pirmyn**, norėdami peržiūrėti savo publikavimo planą.</span><span class="sxs-lookup"><span data-stu-id="95352-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="95352-125">Jei turite atlikti pakeitimus, pasirinkite  **Atgal**.</span><span class="sxs-lookup"><span data-stu-id="95352-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="95352-126">Pasirinkite **Patvirtinti, kad tęsiate**, o tada pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="95352-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="95352-127">Užbaigus publikavimą, skirtuko **Publikuoti sąrašai** viršuje esantis pranešimas nurodo, ar jūsų užduočių sąrašas buvo sėkmingai pristatytas.</span><span class="sxs-lookup"><span data-stu-id="95352-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="95352-128">Daugiau informacijos rasite [Užduočių sąrašų publikavimas jūsų organizacijos darbo kūrimui ir sekimui](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="95352-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="95352-129">EKA ir „Teams” susiejimas užduotims valdyti</span><span class="sxs-lookup"><span data-stu-id="95352-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="95352-130">Norėdami susieti EKA ir „Microsoft Teams” programas, skirtas užduočių valdymui „Commerce” būstinėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="95352-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="95352-131">Eikite į **Mažmeninė prekyba ir komercija \> Užduočių valdymas \> Užduočių integravimas su „Microsoft Teams”**.</span><span class="sxs-lookup"><span data-stu-id="95352-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="95352-132">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="95352-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="95352-133">Nustatykite parinktį **Įgalinti užduočių valdymo integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="95352-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="95352-134">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="95352-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="95352-135">Veiksmų srityje pasirinkite **Užduočių valdymo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="95352-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="95352-136">Turėtumėte gauti pranešimą, nurodantį, kad kuriama paketinė užduotis pavadinimu **„Teams” parengimas**.</span><span class="sxs-lookup"><span data-stu-id="95352-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="95352-137">Eikite į **Sistemos administravimas \> Užklausos \> Paketinės užduotys** ir suraskite naujausią užduotį, kurios aprašymas yra **Komandų parengimas**.</span><span class="sxs-lookup"><span data-stu-id="95352-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="95352-138">Palaukite tol, kol ši užduotis bus baigta.</span><span class="sxs-lookup"><span data-stu-id="95352-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="95352-139">Vykdykite **CDX užduotį 1070**, kad publikuotumėte plano ID ir parduotuvės nuorodas į „Retail Server”.</span><span class="sxs-lookup"><span data-stu-id="95352-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95352-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="95352-140">Additional resources</span></span>

[<span data-ttu-id="95352-141">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="95352-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="95352-142">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="95352-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="95352-143">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="95352-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="95352-144">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="95352-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="95352-145">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="95352-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="95352-146">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="95352-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
