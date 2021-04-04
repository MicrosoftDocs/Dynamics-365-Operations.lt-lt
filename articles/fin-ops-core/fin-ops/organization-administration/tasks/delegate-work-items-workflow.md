---
title: Perduoti darbo eigos darbo elementus
description: Jei planuojate išvykti ar šiaip negalėsite dirbti su darbo elementais, juos galite perduoti arba iš naujo priskirti kitiems vartotojams.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 054e183374d2b24f38b0f90ff90acfeeca013861
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560560"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="d8547-103">Darbo eigos darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="d8547-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="d8547-104">Rankinis darbo elemento perdavimas</span><span class="sxs-lookup"><span data-stu-id="d8547-104">Manually delegate a work item</span></span>

<span data-ttu-id="d8547-105">Norėdami perduoti atskirą darbo elementą, meniu **Darbo eiga** pasirinkite parinktį **Perduoti**, tada įveskite vartotoją, kuriam elementą reikia perduoti, ir komentarą.</span><span class="sxs-lookup"><span data-stu-id="d8547-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="d8547-106">Taip darbo elementas bus iš naujo priskirtas tam vartotojui, kad jis elementą galėtų baigti.</span><span class="sxs-lookup"><span data-stu-id="d8547-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="d8547-107">Neautomatiniu būdu perduokite kelis darbo elementus</span><span class="sxs-lookup"><span data-stu-id="d8547-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="d8547-108">Gali būti perduoti keli darbo elementai kartu iš **Man perduoti darbo elementai** puslapio.</span><span class="sxs-lookup"><span data-stu-id="d8547-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="d8547-109">Šiems darbo eigos tipams taikomas masinis pervedimas: pirkimo sutarties patvirtinimo darbo eiga, pirkimo užsakymo darbo eiga, pirkimo paraiškų peržiūra ir tiekėjo SF darbo eiga.</span><span class="sxs-lookup"><span data-stu-id="d8547-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="d8547-110">Numatyta, kad **Perduoti keletą darbo elementų** funkcija yra išjungta ir gali būti suaktyvinta **Darbo sritys > Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="d8547-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="d8547-111">Norėdami suaktyvinti šią funkciją, kreipkitės į sistemos administratorių.</span><span class="sxs-lookup"><span data-stu-id="d8547-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="d8547-112">Pereikite į **Įprasti > Bendri > Darbo elementai > Man priskirti darbo elementai**.</span><span class="sxs-lookup"><span data-stu-id="d8547-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="d8547-113">Pasirinkite darbo elementus, kurie bus perduoti.</span><span class="sxs-lookup"><span data-stu-id="d8547-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="d8547-114">Spustelėkite **Perduoti darbo elementus** meniu.</span><span class="sxs-lookup"><span data-stu-id="d8547-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="d8547-115">Lauke **Vartotojas** lauke pasirinkite vartotoją, kuriam perduosite darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="d8547-116">Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="d8547-117">Spustelėkite **Perduoti darbo elementus** mygtuką, kad užbaigtumėte darbo elementų perdavimą.</span><span class="sxs-lookup"><span data-stu-id="d8547-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="d8547-118">Automatinis darbo elementų perdavimas</span><span class="sxs-lookup"><span data-stu-id="d8547-118">Automatically delegate work items</span></span>

<span data-ttu-id="d8547-119">Jei tam tikrą laiką planuojate nebūti biure ar dėl kitų priežasčių negalėsite atlikti veiksmų su darbo elementais, naudodami puslapį **Vartotojo parinktys** naujus darbo elementus galite automatiškai perduoti kitiems vartotojams.</span><span class="sxs-lookup"><span data-stu-id="d8547-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="d8547-120">Automatinio perdavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d8547-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="d8547-121">Eikite į **Bendra > Sąranka > Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="d8547-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="d8547-122">Spustelėkite skirtuką **Darbo eiga**. Įsitikinkite, ar perdavimo skyrius išplėstas.</span><span class="sxs-lookup"><span data-stu-id="d8547-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="d8547-123">Norėdami sukonfigūruoti sistemą taip, kad jūsų darbo elementai kitiems vartotojams būtų perduodami automatiškai, turite sukurti perdavimo taisykles, nurodančias, kada bus perduoti tam tikrų tipų darbo elementai.</span><span class="sxs-lookup"><span data-stu-id="d8547-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="d8547-124">Norėdami sukurti perdavimo taisyklę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d8547-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="d8547-125">Spustelėkite **Pridėti**.</span><span class="sxs-lookup"><span data-stu-id="d8547-125">Click **Add**.</span></span>
4. <span data-ttu-id="d8547-126">**Tikslas** laukelyje, pasirinkite parinktį:</span><span class="sxs-lookup"><span data-stu-id="d8547-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="d8547-127">Visi – perduoti visus jums priskirtus darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="d8547-128">Modulis – perduoti tik su tam tikro tipo darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="d8547-129">Jei pasirenkate šią parinktį, privalote pasirinkti darbo srauto tipą **Pavadinimas** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="d8547-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="d8547-130">Darbo eiga – perduoti tik su tam tikra darbo eiga susijusius darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="d8547-131">Jei pasirenkate šią parinktį, privalote pasirinkti darbo srauto tipą **Pavadinimas** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="d8547-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="d8547-132">**Pavadinimas** laukelis:</span><span class="sxs-lookup"><span data-stu-id="d8547-132">In the **Name** field:</span></span>
    - <span data-ttu-id="d8547-133">**Modulis** tikslui, pasirinkite paskirties modulį.</span><span class="sxs-lookup"><span data-stu-id="d8547-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="d8547-134">**Darbo srauto** tikslui, pasirinkite paskirties darbo srautą.</span><span class="sxs-lookup"><span data-stu-id="d8547-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="d8547-135">Lauke **Perduoti** pasirinkite vartotoją, kuriam perduosite darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="d8547-136">Naudokite **Datos/laiko pradžia** ir **Datos/laiko pabaiga** laukelius tam, kad nurodytumėte elementų automatinio priskyrimo laiką.</span><span class="sxs-lookup"><span data-stu-id="d8547-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="d8547-137">Lauke **Pradžios data / laikas** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="d8547-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="d8547-138">Lauke **Pabaigos data / laikas** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="d8547-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="d8547-139">Pasirinkite žymės langelį **Įjungta**, kad aktyvuotumėte perdavimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="d8547-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="d8547-140">Lauke **Komentaras** įveskite komentarą, kuriuo paaiškinate kodėl perduodate darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="d8547-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]