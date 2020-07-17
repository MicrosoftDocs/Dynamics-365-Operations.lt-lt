---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: ChrisGarty
manager: AnnBe
ms.date: 06/23/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d98d84b89f1f3322a9c896b74b63a3b6425b13b
ms.sourcegitcommit: 267864eb0dccd6e26d49d280bd4ad1b770a73a77
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/26/2020
ms.locfileid: "3515769"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="fb2c5-103">Darbo eigos darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="fb2c5-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="fb2c5-104">Rankinis darbo elemento perdavimas</span><span class="sxs-lookup"><span data-stu-id="fb2c5-104">Manually delegate a work item</span></span>

<span data-ttu-id="fb2c5-105">Norėdami perduoti atskirą darbo elementą, meniu **Darbo eiga** pasirinkite parinktį **Perduoti**, tada įveskite vartotoją, kuriam elementą reikia perduoti, ir komentarą.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="fb2c5-106">Taip darbo elementas bus iš naujo priskirtas tam vartotojui, kad jis elementą galėtų baigti.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="fb2c5-107">Neautomatiniu būdu perduokite kelis darbo elementus</span><span class="sxs-lookup"><span data-stu-id="fb2c5-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="fb2c5-108">Gali būti perduoti keli darbo elementai kartu iš **Man perduoti darbo elementai** puslapio.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="fb2c5-109">Šiems darbo eigos tipams taikomas masinis pervedimas: pirkimo sutarties patvirtinimo darbo eiga, pirkimo užsakymo darbo eiga, pirkimo paraiškų peržiūra ir tiekėjo SF darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="fb2c5-110">Numatyta, kad **Perduoti keletą darbo elementų** funkcija yra išjungta ir gali būti suaktyvinta **Darbo sritys > Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="fb2c5-111">Norėdami suaktyvinti šią funkciją, kreipkitės į sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="fb2c5-112">Pereikite į **Įprasti > Bendri > Darbo elementai > Man priskirti darbo elementai**.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="fb2c5-113">Pasirinkite darbo elementus, kurie bus perduoti.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="fb2c5-114">Spustelėkite **Perduoti darbo elementus** meniu.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="fb2c5-115">Lauke **Vartotojas** lauke pasirinkite vartotoją, kuriam perduosite darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="fb2c5-116">Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="fb2c5-117">Spustelėkite **Perduoti darbo elementus** mygtuką, kad užbaigtumėte darbo elementų perdavimą.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="fb2c5-118">Automatinis darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="fb2c5-118">Automatically delegate work items</span></span>

<span data-ttu-id="fb2c5-119">Jei tam tikrą laiką planuojate nebūti biure ar dėl kitų priežasčių negalėsite atlikti veiksmų su darbo elementais, naudodami puslapį **Vartotojo parinktys** naujus darbo elementus galite automatiškai perduoti kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="fb2c5-120">Automatinio perdavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="fb2c5-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="fb2c5-121">Eikite į **Bendra > Sąranka > Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="fb2c5-122">Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar perdavimo skyrius išplėstas.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="fb2c5-123">Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="fb2c5-124">Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="fb2c5-125">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-125">Click **Add**.</span></span>
4. <span data-ttu-id="fb2c5-126">Lauke **Aprėptis** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-126">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="fb2c5-127">Visi – perduoti visus jums priskirtus darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="fb2c5-128">Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="fb2c5-129">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigos tipą.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-129">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="fb2c5-130">Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="fb2c5-131">Jei pasirinksite šią parinktį, lauke Pavadinimas turite pasirinkti darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-131">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="fb2c5-132">Lauke **Perduoti** pasirinkite vartotoją, kuriam perduosite darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-132">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="fb2c5-133">Norėdami nurodyti, kada darbo elementai turėtų būti perduodami automatiškai, naudokite laukų Pradžios data / laikas ir Pabaigos data / laikas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-133">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="fb2c5-134">Lauke **Pradžios data / laikas** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-134">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="fb2c5-135">Lauke **Pabaigos data / laikas** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-135">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="fb2c5-136">Pasirinkite žymės langelį **Įjungta**, kad aktyvuotumėte perdavimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-136">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="fb2c5-137">Jei kaip aprėptį pasirinkote **Modulis**, turite pasirinkti modulį pavadinimo lauke.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-137">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="fb2c5-138">Jei kaip aprėptį pasirinkote **Darbo eiga**, turite pasirinkti konkrečią perdavimo darbo eigą pavadinimo lauke.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-138">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="fb2c5-139">Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="fb2c5-139">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>

