---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558716"
---
# <a name="create-new-users"></a><span data-ttu-id="6a9f8-103">Naujų vartotojų kūrimas</span><span class="sxs-lookup"><span data-stu-id="6a9f8-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6a9f8-104">Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="6a9f8-105">Sistemos administratoriai gali atlikitti šią procedūrą, kad įtrauktų vartotojus į sistemą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="6a9f8-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="6a9f8-107">Naujo vartotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="6a9f8-107">Add a new user</span></span>
1. <span data-ttu-id="6a9f8-108">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="6a9f8-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-109">Click New.</span></span>
3. <span data-ttu-id="6a9f8-110">Lauke „Vartotojo ID“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="6a9f8-111">Įveskite unikalų vartotojo identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="6a9f8-112">Reikės vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-112">A user ID is required.</span></span>  
4. <span data-ttu-id="6a9f8-113">Lauke „Vartotojo vardas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="6a9f8-114">Įveskite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="6a9f8-115">Lauke „Domenas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="6a9f8-116">Įveskite vartotojo domeną.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="6a9f8-117">Lauke „Pseudonimas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="6a9f8-118">Įveskite vartotojo pseudonimą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="6a9f8-119">Lauke „Įmonė“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6a9f8-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6a9f8-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a9f8-122">Pasirinkite vartotoją įmonę</span><span class="sxs-lookup"><span data-stu-id="6a9f8-122">Select the user's company</span></span>  
10. <span data-ttu-id="6a9f8-123">Spustelėkite „Priskirti vaidmenis“.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-123">Click Assign roles.</span></span>
11. <span data-ttu-id="6a9f8-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6a9f8-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-125">Click OK.</span></span>
13. <span data-ttu-id="6a9f8-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="6a9f8-127">Importuoti vartotojus</span><span class="sxs-lookup"><span data-stu-id="6a9f8-127">Import users</span></span>
1. <span data-ttu-id="6a9f8-128">Spustelėkite „Importuoti vartotojus“.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-128">Click Import users.</span></span>
2. <span data-ttu-id="6a9f8-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6a9f8-130">Spustelėkite „Importuoti vartotojus“.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-130">Click Import users.</span></span>
4. <span data-ttu-id="6a9f8-131">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="6a9f8-131">Click Close.</span></span>

