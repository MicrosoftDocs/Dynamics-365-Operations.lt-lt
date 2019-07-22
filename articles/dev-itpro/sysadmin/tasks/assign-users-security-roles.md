---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711136"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="adf22-103">Vartotojų priskyrimas saugos vaidmenims</span><span class="sxs-lookup"><span data-stu-id="adf22-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="adf22-104">Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="adf22-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="adf22-105">Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus.</span><span class="sxs-lookup"><span data-stu-id="adf22-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="adf22-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="adf22-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="adf22-107">Automatinis vartotojų priskyrimas vaidmenims</span><span class="sxs-lookup"><span data-stu-id="adf22-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="adf22-108">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="adf22-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="adf22-109">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="adf22-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="adf22-110">Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="adf22-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="adf22-111">Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="adf22-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="adf22-112">Spustelėkite **Įtraukti taisyklę**, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="adf22-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="adf22-113">Sąraše **Pasirinkti užklausą** raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="adf22-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="adf22-114">Pasirinkite su šia taisykle naudotiną užklausą.</span><span class="sxs-lookup"><span data-stu-id="adf22-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="adf22-115">Sąraše **Narystės taisyklės pavadinimas** spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="adf22-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="adf22-116">Spustelėkite **Redaguoti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="adf22-116">Click **Edit query**.</span></span> <span data-ttu-id="adf22-117">Pagal poreikį užklausą redaguokite.</span><span class="sxs-lookup"><span data-stu-id="adf22-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="adf22-118">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="adf22-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="adf22-119">Vartotojų šalinimas iš automatinio vaidmenų priskyrimo</span><span class="sxs-lookup"><span data-stu-id="adf22-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="adf22-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="adf22-120">Close the page.</span></span>
2. <span data-ttu-id="adf22-121">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims**.</span><span class="sxs-lookup"><span data-stu-id="adf22-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="adf22-122">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="adf22-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="adf22-123">Pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="adf22-123">Select a role.</span></span> <span data-ttu-id="adf22-124">Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="adf22-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="adf22-125">Meniu **Vaidmeniui priskirti vartotojai** pasirinkite **Rankiniu būdu priskirti / pašalinti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="adf22-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="adf22-126">Sąraše **Priskirti vartotojus vaidmeniui arba iš jo pašalinti** pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="adf22-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="adf22-127">Pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="adf22-127">Select a user.</span></span>  
6. <span data-ttu-id="adf22-128">Dalyje **Veiksmų sritis** pasirinkite **Pašalinti iš vaidmens**.</span><span class="sxs-lookup"><span data-stu-id="adf22-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="adf22-129">Spustelėkite **Pašalinti iš vaidmens**, kad pasirinktus vartotojus pašalintumėte iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="adf22-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="adf22-130">Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti, ir spustelėkite **Nustatyti būseną iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="adf22-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="adf22-131">Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="adf22-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="adf22-132">Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="adf22-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="adf22-133">Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="adf22-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
