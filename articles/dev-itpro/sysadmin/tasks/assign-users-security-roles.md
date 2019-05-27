---
title: Vartotojų priskyrimas saugos vaidmenims
description: Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556714"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="6724d-103">Vartotojų priskyrimas saugos vaidmenims</span><span class="sxs-lookup"><span data-stu-id="6724d-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6724d-104">Kad vartotojai galėtų pasiekti Microsoft Dynamics 365 for Finance and Operations redakciją įmonėms, jiems reikia priskirti saugos vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="6724d-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="6724d-105">Šia procedūra paaiškinama, kaip sistemos administratoriai gali automatiškai pagal verslo duomenis priskirti vartotojus.</span><span class="sxs-lookup"><span data-stu-id="6724d-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="6724d-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="6724d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="6724d-107">Automatinis vartotojų priskyrimas vaidmenims</span><span class="sxs-lookup"><span data-stu-id="6724d-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="6724d-108">Eikite į Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="6724d-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="6724d-109">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="6724d-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="6724d-110">Pasirinkite vaidmenį, kurio taisyklę norite sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="6724d-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="6724d-111">Šiame pavyzdyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="6724d-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="6724d-112">Spustelėkite Įtraukti taisyklę, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="6724d-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="6724d-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6724d-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6724d-114">Pasirinkite su šia taisykle naudotiną užklausą.</span><span class="sxs-lookup"><span data-stu-id="6724d-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="6724d-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6724d-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6724d-116">Spustelėkite Redaguoti užklausą.</span><span class="sxs-lookup"><span data-stu-id="6724d-116">Click Edit query.</span></span>
    * <span data-ttu-id="6724d-117">Pagal poreikį užklausą redaguokite.</span><span class="sxs-lookup"><span data-stu-id="6724d-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="6724d-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6724d-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="6724d-119">Vartotojų šalinimas iš automatinio vaidmenų priskyrimo</span><span class="sxs-lookup"><span data-stu-id="6724d-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="6724d-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6724d-120">Close the page.</span></span>
2. <span data-ttu-id="6724d-121">Eikite į Sistemos administravimas > Sauga > Priskirti vartotojus vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="6724d-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="6724d-122">Medyje pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="6724d-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="6724d-123">Pasirinkite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="6724d-123">Select a role.</span></span> <span data-ttu-id="6724d-124">Šiam pavyzdžiui pasirinkite Apskaitos prižiūrėtojas.</span><span class="sxs-lookup"><span data-stu-id="6724d-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="6724d-125">Spustelėkite Rankiniu būdu priskirti / pašalinti vartotojus.</span><span class="sxs-lookup"><span data-stu-id="6724d-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="6724d-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="6724d-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6724d-127">Pasirinkite vartotoją.</span><span class="sxs-lookup"><span data-stu-id="6724d-127">Select a user.</span></span>  
6. <span data-ttu-id="6724d-128">Spustelėkite Pašalinti iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="6724d-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="6724d-129">Spustelėkite Pašalinti iš vaidmens, kad pasirinktus vartotojus pašalintumėte iš vaidmens.</span><span class="sxs-lookup"><span data-stu-id="6724d-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="6724d-130">Norėdami pašalinti pašalinimus, pasirinkite vartotojus, kurių pašalinimus norite pašalinti ir spustelėkite Grąžinti būseną.</span><span class="sxs-lookup"><span data-stu-id="6724d-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="6724d-131">Kai pašalinate pašalinimą grąžindami vartotojo būseną, vartotojo vaidmuo vėl priskiriamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="6724d-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="6724d-132">Tačiau, grąžinus būseną, vartotojas ne iš kato priskiriamas vaidmeniui ar iš vaidmens pašalinamas.</span><span class="sxs-lookup"><span data-stu-id="6724d-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="6724d-133">Vartotojas vaidmeniui priskiriamas arba iš vaidmens pašalinamas kitą kartą vykdant automatinio vaidmenų priskyrimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="6724d-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

