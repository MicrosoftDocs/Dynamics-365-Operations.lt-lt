--- 
title: "Teisių užsakyti produktus kito darbuotojo vardu nustatymas"
description: "Šioje procedūroje parodoma, kaip darbuotojų suteikti teisę pirkimo paraiškas rengti kitų darbuotojų vardu."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9e003f953c05facd5516e2bfa6d1c83ba6381c15
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="f21d6-103">Teisių užsakyti produktus kito darbuotojo vardu nustatymas</span><span class="sxs-lookup"><span data-stu-id="f21d6-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f21d6-104">Šioje procedūroje parodoma, kaip darbuotojų suteikti teisę pirkimo paraiškas rengti kitų darbuotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="f21d6-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="f21d6-105">Kitaip tariant, pirkimo paraiškos „rengėjas“ gali kurti paraišką kitam „prašytojas“.</span><span class="sxs-lookup"><span data-stu-id="f21d6-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="f21d6-106">Procedūroje taip pat parodoma, kaip darbuotojui suteikti teisę užsakyti prekes ir paslaugas skirtinguose juridiniuose subjektuose arba valdymo vienetuose.</span><span class="sxs-lookup"><span data-stu-id="f21d6-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="f21d6-107">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="f21d6-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="f21d6-108">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba naudodami savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="f21d6-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="f21d6-109">Suteikti teisę kito darbuotojo vardu įvesti pirkimo paraiškas</span><span class="sxs-lookup"><span data-stu-id="f21d6-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="f21d6-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo paraiškos teisės.</span><span class="sxs-lookup"><span data-stu-id="f21d6-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="f21d6-111">Įsitikinkite, kad laukas Dabartinio rodinys nustatytas į parinktį Pagal rengėją.</span><span class="sxs-lookup"><span data-stu-id="f21d6-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="f21d6-112">Kairiojoje srityje esančiame sąraše pateikiami asmenys, kuriems galima suteikti teisę rengti paraiškas kitų asmenų vardu.</span><span class="sxs-lookup"><span data-stu-id="f21d6-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="f21d6-113">Pasirinkite asmenį, kuriam norite suteikti teisę (t. y. rengėją).</span><span class="sxs-lookup"><span data-stu-id="f21d6-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="f21d6-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f21d6-114">Click Add.</span></span>
4. <span data-ttu-id="f21d6-115">Raskite ir pasirinkite asmenį, kurį norite įtraukti kaip prašytoją.</span><span class="sxs-lookup"><span data-stu-id="f21d6-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="f21d6-116">Prašytojas yra asmuo, kurio vardu rengėjas gali kurti paraiškas.</span><span class="sxs-lookup"><span data-stu-id="f21d6-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="f21d6-117">Lauke Autorizavimas pasirinkite Konkretus, norėdami, kad rengėjas galėtų kurti pirkimo paraiškas pasirinkto darbuotojo vardu.</span><span class="sxs-lookup"><span data-stu-id="f21d6-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="f21d6-118">Pasirinkite Ataskaitos, norėdami, kad rengėjas taip pat galėtų kurti pirkimo paraiškas visų darbuotojų, teikiančių tam darbuotojui ataskaitas, vardu.</span><span class="sxs-lookup"><span data-stu-id="f21d6-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="f21d6-119">Lauke Įsigalioja įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f21d6-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="f21d6-120">Lauke Galiojimo pabaiga įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f21d6-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="f21d6-121">Peržiūrėti rengėjus, kurie turi teisę pasirinktam darbuotojui kurti pirkimo paraiškas</span><span class="sxs-lookup"><span data-stu-id="f21d6-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="f21d6-122">Lauke Dabartinis rodinys pasirinkite Pagal prašytoją.</span><span class="sxs-lookup"><span data-stu-id="f21d6-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="f21d6-123">Šiame rodinyje rodomas rengėjų, kuriems suteikta teisė pasirinkto darbuotojo vardu kurti pirkimo paraiškas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f21d6-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="f21d6-124">Naudokite spartųjį filtrą, norėdami rasti darbuotoją, kurį ką tik įtraukėte kaip prašytoją.</span><span class="sxs-lookup"><span data-stu-id="f21d6-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="f21d6-125">Pasirinkite prašytoją.</span><span class="sxs-lookup"><span data-stu-id="f21d6-125">Select the requester.</span></span>
    * <span data-ttu-id="f21d6-126">Sąraše Rengėjas rodomi asmenys, kurie turi teisę prekes užsakyti kairiojoje srityje pasirinkto prašytojo vardu.</span><span class="sxs-lookup"><span data-stu-id="f21d6-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="f21d6-127">Čia galite įtraukti papildomų rengėjų.</span><span class="sxs-lookup"><span data-stu-id="f21d6-127">You can add additional preparers here.</span></span>   <span data-ttu-id="f21d6-128">Šiame rodinyje taip pat galite prašytojui suteikti teisę kurti paraiškas juridiniame subjekte ar valdymo vienete, kuris nėra to asmens pagrindinis juridinis subjektas ar valdymo vienetas.</span><span class="sxs-lookup"><span data-stu-id="f21d6-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

