---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/12/2019
ms.locfileid: "976786"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="26631-103">Darbo eigos darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="26631-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="26631-104">Rankinis darbo elemento perdavimas</span><span class="sxs-lookup"><span data-stu-id="26631-104">Manually delegate a work item</span></span>

<span data-ttu-id="26631-105">Norėdami perduoti atskirą darbo elementą, meniu **Darbo eiga** pasirinkite parinktį **Perduoti**, tada įveskite vartotoją, kuriam elementą reikia perduoti, ir komentarą.</span><span class="sxs-lookup"><span data-stu-id="26631-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="26631-106">Taip darbo elementas bus iš naujo priskirtas tam vartotojui, kad jis elementą galėtų baigti.</span><span class="sxs-lookup"><span data-stu-id="26631-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="26631-107">Automatinis darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="26631-107">Automatically delegate work items</span></span>

<span data-ttu-id="26631-108">Jei tam tikrą laiką planuojate nebūti biure ar dėl kitų priežasčių negalėsite atlikti veiksmų su darbo elementais, naudodami puslapį **Vartotojo parinktys** naujus darbo elementus galite automatiškai perduoti kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="26631-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="26631-109">Automatinio perdavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="26631-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="26631-110">Eikite į Bendra > Nustatymas > Vartotojo parinktys.</span><span class="sxs-lookup"><span data-stu-id="26631-110">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="26631-111">Spustelėkite skirtuką Darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="26631-111">Click the Workflow tab.</span></span>
    * <span data-ttu-id="26631-112">Įsitikinkite, kad dalis Perdavimas yra išskleista.</span><span class="sxs-lookup"><span data-stu-id="26631-112">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="26631-113">Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="26631-113">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="26631-114">Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="26631-114">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="26631-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="26631-115">Click Add.</span></span>
4. <span data-ttu-id="26631-116">Lauke Aprėptis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="26631-116">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="26631-117">Visi – perduoti visus jums priskirtus darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="26631-117">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="26631-118">Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="26631-118">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="26631-119">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigos tipą.</span><span class="sxs-lookup"><span data-stu-id="26631-119">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="26631-120">Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="26631-120">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="26631-121">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="26631-121">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="26631-122">Lauke Perduoti pasirinkite vartotoją, kuriam norite perduoti darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="26631-122">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="26631-123">Norėdami nurodyti, kada darbo elementai turėtų būti perduodami automatiškai, naudokite laukų Pradžios data / laikas ir Pabaigos data / laikas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="26631-123">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="26631-124">Lauke Pradžios data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="26631-124">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="26631-125">Lauke Pabaigos data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="26631-125">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="26631-126">Pasirinkite žymės langelį Įgalinta, kad suaktyvintumėte perdavimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="26631-126">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="26631-127">Jei modulį pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti modulį.</span><span class="sxs-lookup"><span data-stu-id="26631-127">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="26631-128">Jei darbo eigą pasirinkote kaip aprėptį, lauke Pavadinimas turite pasirinkti tam tikrą darbo eigą, kuriai reikia perduoti.</span><span class="sxs-lookup"><span data-stu-id="26631-128">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="26631-129">Lauke Komentaras įveskite komentarą, paaiškinantį, kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="26631-129">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

