--- 
title: Perduoti darbo eigos darbo elementus
description: "Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams."
author: jasongre
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 978f2956e25d3b92edea9e611e7b20155c22e411
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="7b165-103">Perduoti darbo eigos darbo elementus</span><span class="sxs-lookup"><span data-stu-id="7b165-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b165-104">Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7b165-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="7b165-105">Ši procedūra padės sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitam vartotojui būtų perduodami automatiškai.</span><span class="sxs-lookup"><span data-stu-id="7b165-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="7b165-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7b165-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="7b165-107">Automatinio perdavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="7b165-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="7b165-108">Eikite į Bendra > Nustatymas > Vartotojo parinktys.</span><span class="sxs-lookup"><span data-stu-id="7b165-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="7b165-109">Spustelėkite skirtuką Darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="7b165-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="7b165-110">Įsitikinkite, kad dalis Perdavimas yra išskleista.</span><span class="sxs-lookup"><span data-stu-id="7b165-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="7b165-111">Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="7b165-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="7b165-112">Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7b165-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="7b165-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="7b165-113">Click Add.</span></span>
4. <span data-ttu-id="7b165-114">Lauke Aprėptis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7b165-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="7b165-115">Visi – perduoti visus jums priskirtus darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7b165-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="7b165-116">Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7b165-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="7b165-117">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigos tipą.</span><span class="sxs-lookup"><span data-stu-id="7b165-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="7b165-118">Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7b165-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="7b165-119">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="7b165-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="7b165-120">Lauke Perduoti pasirinkite vartotoją, kuriam norite perduoti darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7b165-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="7b165-121">Norėdami nurodyti, kada darbo elementai turėtų būti perduodami automatiškai, naudokite laukų Pradžios data / laikas ir Pabaigos data / laikas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7b165-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="7b165-122">Lauke Pradžios data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b165-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="7b165-123">Lauke Pabaigos data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="7b165-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="7b165-124">Pasirinkite žymės langelį Įgalinta, kad suaktyvintumėte perdavimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="7b165-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="7b165-125">Jei modulį pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti modulį.</span><span class="sxs-lookup"><span data-stu-id="7b165-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="7b165-126">Jei darbo eigą pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti tam tikrą darbo eigą, kuriai reikia perduoti.</span><span class="sxs-lookup"><span data-stu-id="7b165-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="7b165-127">Lauke Komentaras įveskite komentarą, paaiškinantį, kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="7b165-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


