---
title: Teisių užsakyti produktus kito darbuotojo vardu nustatymas
description: Šioje temoje paaiškinta, kaip suteikti darbuotojams teises rengti pirkimo paraiškas kitų darbuotojų vardu.
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe8ad0540febcc703554e2451f7f644338e4d57b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149465"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="060c4-103">Teisių užsakyti produktus kito darbuotojo vardu nustatymas</span><span class="sxs-lookup"><span data-stu-id="060c4-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="060c4-104">Šioje temoje paaiškinta, kaip suteikti darbuotojams teises rengti pirkimo paraiškas kitų darbuotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="060c4-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="060c4-105">Kitaip tariant, pirkimo paraiškos „rengėjas“ gali kurti paraišką kitam „rengėjui“.</span><span class="sxs-lookup"><span data-stu-id="060c4-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="060c4-106">Procedūroje taip pat parodoma, kaip darbuotojui suteikti teisę užsakyti prekes ir paslaugas skirtinguose juridiniuose subjektuose arba valdymo vienetuose.</span><span class="sxs-lookup"><span data-stu-id="060c4-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="060c4-107">Šias užduotis paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="060c4-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="060c4-108">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba naudodami savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="060c4-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="060c4-109">Suteikti teisę kito darbuotojo vardu įvesti pirkimo paraiškas</span><span class="sxs-lookup"><span data-stu-id="060c4-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="060c4-110">Naršymo srityje eikite į **Moduliai > Paraiškos > Sąranka > Strategijos > Pirkimo paraiškos teisės**.</span><span class="sxs-lookup"><span data-stu-id="060c4-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="060c4-111">Įsitikinkite, kad lauke **Dabartinis rodinys** nustatyta reikšmė **Pagal rengėją**.</span><span class="sxs-lookup"><span data-stu-id="060c4-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="060c4-112">Kairiojoje srityje esančiame sąraše pateikiami asmenys, kuriems galima suteikti teisę rengti paraiškas kitų asmenų vardu.</span><span class="sxs-lookup"><span data-stu-id="060c4-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="060c4-113">Pasirinkite asmenį, kuriam norite suteikti teisę (t. y. rengėją).</span><span class="sxs-lookup"><span data-stu-id="060c4-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="060c4-114">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="060c4-114">Select **Add**.</span></span>
4. <span data-ttu-id="060c4-115">Raskite ir pasirinkite asmenį, kurį norite įtraukti kaip prašytoją.</span><span class="sxs-lookup"><span data-stu-id="060c4-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="060c4-116">Prašytojas yra asmuo, kurio vardu rengėjas gali kurti paraiškas.</span><span class="sxs-lookup"><span data-stu-id="060c4-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="060c4-117">Lauke **Autorizavimas** pasirinkite **Specialus**, jei rengėjui turėtų būti leidžiama kurti pirkimo paraiškas pasirinkto darbuotojo vardu.</span><span class="sxs-lookup"><span data-stu-id="060c4-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="060c4-118">Pasirinkite **Ataskaitų teikimas**, jei rengėjui taip pat turėtų būti leidžiama kurti pirkimo paraiškas visų darbuotojų, kurie atsiskaito tam darbuotojui, vardu.</span><span class="sxs-lookup"><span data-stu-id="060c4-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="060c4-119">Lauke **Įsigalioja** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="060c4-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="060c4-120">Lauke **Galiojimo pabaiga** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="060c4-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="060c4-121">Peržiūrėti rengėjus, kurie turi teisę pasirinktam darbuotojui kurti pirkimo paraiškas</span><span class="sxs-lookup"><span data-stu-id="060c4-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="060c4-122">Lauke **Dabartinis rodinys** pasirinkite **Pagal prašytoją**.</span><span class="sxs-lookup"><span data-stu-id="060c4-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="060c4-123">Šiame rodinyje rodomas rengėjų, kuriems suteikta teisė pasirinkto darbuotojo vardu kurti pirkimo paraiškas, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="060c4-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="060c4-124">Naudokite spartųjį filtrą, norėdami rasti darbuotoją, kurį ką tik įtraukėte kaip prašytoją.</span><span class="sxs-lookup"><span data-stu-id="060c4-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="060c4-125">Pasirinkite prašytoją.</span><span class="sxs-lookup"><span data-stu-id="060c4-125">Select the requester.</span></span> <span data-ttu-id="060c4-126">Sąraše Rengėjas rodomi asmenys, kurie turi teisę prekes užsakyti kairiojoje srityje pasirinkto prašytojo vardu.</span><span class="sxs-lookup"><span data-stu-id="060c4-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="060c4-127">Čia galite įtraukti papildomų rengėjų.</span><span class="sxs-lookup"><span data-stu-id="060c4-127">You can add additional preparers here.</span></span> <span data-ttu-id="060c4-128">Šiame rodinyje taip pat galite prašytojui suteikti teisę kurti paraiškas juridiniame subjekte ar valdymo vienete, kuris nėra to asmens pagrindinis juridinis subjektas ar valdymo vienetas.</span><span class="sxs-lookup"><span data-stu-id="060c4-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

