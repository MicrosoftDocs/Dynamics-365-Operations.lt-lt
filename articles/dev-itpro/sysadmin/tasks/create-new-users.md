---
title: Naujų vartotojų kūrimas
description: Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916489"
---
# <a name="create-new-users"></a><span data-ttu-id="bb075-103">Naujų vartotojų kūrimas</span><span class="sxs-lookup"><span data-stu-id="bb075-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb075-104">Vartotojai yra vidiniai jūsų organizacijos darbuotojai arba išoriniai klientai bei tiekėjai, kuriems reikalinga prieiga prie sistemos, kad galėtų atlikti savo užduotis.</span><span class="sxs-lookup"><span data-stu-id="bb075-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="bb075-105">Sistemos administratoriai gali atlikitti šią procedūrą, kad įtrauktų vartotojus į sistemą.</span><span class="sxs-lookup"><span data-stu-id="bb075-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="bb075-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="bb075-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="bb075-107">Naujo vartotojo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="bb075-107">Add a new user</span></span>
1. <span data-ttu-id="bb075-108">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="bb075-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="bb075-109">**Veiksmų sritis** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bb075-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="bb075-110">Lauke **Vartotojo ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb075-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="bb075-111">Įveskite unikalų vartotojo identifikatorių.</span><span class="sxs-lookup"><span data-stu-id="bb075-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="bb075-112">Reikės vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="bb075-112">A user ID is required.</span></span>  
4. <span data-ttu-id="bb075-113">Lauke **Vartotojo vardas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb075-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="bb075-114">Įveskite vartotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="bb075-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="bb075-115">Lauke **Domenas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb075-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="bb075-116">Įveskite vartotojo domeną.</span><span class="sxs-lookup"><span data-stu-id="bb075-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="bb075-117">Lauke **Pseudonimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bb075-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="bb075-118">Įveskite vartotojo pseudonimą.</span><span class="sxs-lookup"><span data-stu-id="bb075-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="bb075-119">Lauke **Įmonė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bb075-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bb075-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bb075-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="bb075-121">Skyriuje **Vartotojo vaidmenys** spustelėkite **Priskirti vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="bb075-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="bb075-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bb075-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bb075-123">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bb075-123">Click **OK**.</span></span>
12. <span data-ttu-id="bb075-124">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bb075-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="bb075-125">Importuoti vartotojus</span><span class="sxs-lookup"><span data-stu-id="bb075-125">Import users</span></span>
1. <span data-ttu-id="bb075-126">**Veiksmų sritis** spustelėkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="bb075-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="bb075-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bb075-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bb075-128">Spustelėkite **Importuoti vartotojus**.</span><span class="sxs-lookup"><span data-stu-id="bb075-128">Click **Import users**.</span></span>
4. <span data-ttu-id="bb075-129">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="bb075-129">Click **Close**.</span></span>

