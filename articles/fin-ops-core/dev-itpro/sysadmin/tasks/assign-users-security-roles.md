---
title: Vartotojų priskyrimas saugos vaidmenims
description: Norint pasiekti „Finance and Operations“ programas, vartotojams turi būti priskirti saugos vaidmenys.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180972"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="1b4d7-103">Vartotojų priskyrimas saugos vaidmenims</span><span class="sxs-lookup"><span data-stu-id="1b4d7-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b4d7-104">Norėdami naudoti bet ką, išskyrus bendrąsias galimybes, vartotojai turi būti priskirti saugos vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="1b4d7-105">Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="1b4d7-106">Automatinis vartotojų priskyrimas vaidmenims</span><span class="sxs-lookup"><span data-stu-id="1b4d7-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="1b4d7-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="1b4d7-108">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1b4d7-109">Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="1b4d7-110">Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="1b4d7-111">Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="1b4d7-112">Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="1b4d7-113">Pasirinkite su šia taisykle naudotiną užklausą.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="1b4d7-114">Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1b4d7-115">Spustelėkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-115">Click **Edit query**.</span></span> <span data-ttu-id="1b4d7-116">Pagal poreikį užklausą redaguokite.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="1b4d7-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="1b4d7-118">Vartotojų šalinimas iš automatinio vaidmenų priskyrimo</span><span class="sxs-lookup"><span data-stu-id="1b4d7-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="1b4d7-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-119">Close the page.</span></span>
2. <span data-ttu-id="1b4d7-120">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="1b4d7-121">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1b4d7-122">Pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-122">Select a role.</span></span> <span data-ttu-id="1b4d7-123">Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="1b4d7-124">Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="1b4d7-125">Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="1b4d7-126">Pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-126">Select a user.</span></span>  
6. <span data-ttu-id="1b4d7-127">Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="1b4d7-128">Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="1b4d7-129">Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="1b4d7-130">Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="1b4d7-131">Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="1b4d7-132">Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="1b4d7-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
