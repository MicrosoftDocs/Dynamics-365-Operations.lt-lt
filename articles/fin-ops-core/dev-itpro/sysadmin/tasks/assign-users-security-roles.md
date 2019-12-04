---
title: Vartotojų priskyrimas saugos vaidmenims
description: Norint pasiekti „Finance and Operations“ programas, vartotojams turi būti priskirti saugos vaidmenys.
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
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2019
ms.locfileid: "2808001"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="59cbf-103">Vartotojų priskyrimas saugos vaidmenims</span><span class="sxs-lookup"><span data-stu-id="59cbf-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59cbf-104">Norėdami naudoti bet ką, išskyrus bendrąsias galimybes, vartotojai turi būti priskirti saugos vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="59cbf-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="59cbf-105">Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="59cbf-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="59cbf-106">Automatinis vartotojų priskyrimas vaidmenims</span><span class="sxs-lookup"><span data-stu-id="59cbf-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="59cbf-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="59cbf-108">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="59cbf-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="59cbf-109">Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="59cbf-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="59cbf-110">Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="59cbf-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="59cbf-111">Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="59cbf-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="59cbf-112">Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="59cbf-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="59cbf-113">Pasirinkite su šia taisykle naudotiną užklausą.</span><span class="sxs-lookup"><span data-stu-id="59cbf-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="59cbf-114">Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="59cbf-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="59cbf-115">Spustelėkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-115">Click **Edit query**.</span></span> <span data-ttu-id="59cbf-116">Pagal poreikį užklausą redaguokite.</span><span class="sxs-lookup"><span data-stu-id="59cbf-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="59cbf-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-117">Click **OK**.</span></span>
8. <span data-ttu-id="59cbf-118">Spustelėkite **Automatiškai priskirti vaidmenį**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="59cbf-119">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Vartotojai > Vartotojai** (geriausia – atskiroje naršyklės kortelėje).</span><span class="sxs-lookup"><span data-stu-id="59cbf-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="59cbf-120">Peržiūrėkite vaidmenis, priskirtus skirtingiems vartotojams, kad patvirtintumėte, jog vaidmenų priskyrimo užklausa yra teisinga.</span><span class="sxs-lookup"><span data-stu-id="59cbf-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="59cbf-121">Jei reikia, pakoreguokite ir vykdykite iš naujo.</span><span class="sxs-lookup"><span data-stu-id="59cbf-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="59cbf-122">Vartotojų šalinimas iš automatinio vaidmenų priskyrimo</span><span class="sxs-lookup"><span data-stu-id="59cbf-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="59cbf-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="59cbf-123">Close the page.</span></span>
2. <span data-ttu-id="59cbf-124">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="59cbf-125">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="59cbf-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="59cbf-126">Pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="59cbf-126">Select a role.</span></span> <span data-ttu-id="59cbf-127">Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="59cbf-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="59cbf-128">Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="59cbf-129">Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="59cbf-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="59cbf-130">Pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="59cbf-130">Select a user.</span></span>  
6. <span data-ttu-id="59cbf-131">Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="59cbf-132">Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="59cbf-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="59cbf-133">Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="59cbf-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="59cbf-134">Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="59cbf-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="59cbf-135">Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="59cbf-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="59cbf-136">Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="59cbf-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
