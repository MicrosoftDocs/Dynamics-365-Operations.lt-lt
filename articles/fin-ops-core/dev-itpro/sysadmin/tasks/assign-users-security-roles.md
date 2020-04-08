---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad vartotojai galėtų pasiekti „Finance and Operations“ programas, jiems reikia priskirti saugos vaidmenis.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143560"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="ae0fe-103">Vartotojų priskyrimas saugos vaidmenims</span><span class="sxs-lookup"><span data-stu-id="ae0fe-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae0fe-104">Norėdami naudoti bet ką, išskyrus bendrąsias galimybes, vartotojai turi būti priskirti saugos vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="ae0fe-105">Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="ae0fe-106">Automatinis vartotojų priskyrimas vaidmenims</span><span class="sxs-lookup"><span data-stu-id="ae0fe-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="ae0fe-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="ae0fe-108">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="ae0fe-109">Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="ae0fe-110">Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="ae0fe-111">Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="ae0fe-112">Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="ae0fe-113">Pasirinkite su šia taisykle naudotiną užklausą.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="ae0fe-114">Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ae0fe-115">Spustelėkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-115">Click **Edit query**.</span></span> <span data-ttu-id="ae0fe-116">Pagal poreikį užklausą redaguokite.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="ae0fe-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-117">Click **OK**.</span></span>
8. <span data-ttu-id="ae0fe-118">Spustelėkite **Automatiškai priskirti vaidmenį**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="ae0fe-119">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Vartotojai > Vartotojai** (geriausia – atskiroje naršyklės kortelėje).</span><span class="sxs-lookup"><span data-stu-id="ae0fe-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="ae0fe-120">Peržiūrėkite vaidmenis, priskirtus skirtingiems vartotojams, kad patvirtintumėte, jog vaidmenų priskyrimo užklausa yra teisinga.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="ae0fe-121">Jei reikia, pakoreguokite ir vykdykite iš naujo.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="ae0fe-122">Vartotojų šalinimas iš automatinio vaidmenų priskyrimo</span><span class="sxs-lookup"><span data-stu-id="ae0fe-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="ae0fe-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-123">Close the page.</span></span>
2. <span data-ttu-id="ae0fe-124">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="ae0fe-125">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="ae0fe-126">Pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-126">Select a role.</span></span> <span data-ttu-id="ae0fe-127">Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="ae0fe-128">Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="ae0fe-129">Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="ae0fe-130">Pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-130">Select a user.</span></span>  
6. <span data-ttu-id="ae0fe-131">Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="ae0fe-132">Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="ae0fe-133">Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="ae0fe-134">Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-134">When you remove an exclusion by resetting the user's status, the user's role is again assigned automatically.</span></span> <span data-ttu-id="ae0fe-135">Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="ae0fe-136">Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="ae0fe-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
