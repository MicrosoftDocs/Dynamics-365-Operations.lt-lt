---
title: Tęstinumo programos naudojimas
description: Šioje procedūroje parodoma, kaip parduoti tęstinumo programą ir apdoroti susijusius pardavimo užsakymus.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45bd4a3cc9f9b03c713d33638d6dc93aa696c581
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564916"
---
# <a name="using-continuity-program"></a><span data-ttu-id="cfa46-103">Tęstinumo programos naudojimas</span><span class="sxs-lookup"><span data-stu-id="cfa46-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cfa46-104">Šioje procedūroje parodoma, kaip parduoti tęstinumo programą ir apdoroti susijusius pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="cfa46-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="cfa46-105">Norint atlikti šią procedūrą, vartotojas turi būti nustatytas kaip skambučių centro vartotojas.</span><span class="sxs-lookup"><span data-stu-id="cfa46-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="cfa46-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="cfa46-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="cfa46-107">Pasirinkite Mažmeninė prekyba ir prekyba > Klientai > Klientų aptarnavimas.</span><span class="sxs-lookup"><span data-stu-id="cfa46-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="cfa46-108">Lauke Ieškos tekstas įveskite Karen ir paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="cfa46-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="cfa46-109">Turėtų pasirodyti išplėstinės ieškos dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="cfa46-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="cfa46-110">Jei jis nepasirodo, spustelėkite parinktį Ieškoti, esančią dešinėje šio lauko pusėje.</span><span class="sxs-lookup"><span data-stu-id="cfa46-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="cfa46-111">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="cfa46-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cfa46-112">Tik vienoje eilutėje turi būti rodoma Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="cfa46-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="cfa46-113">Pasirinkite eilutę spustelėdami žymės langelio stulpelyje tolimojoje kairėje tinklelio pusėje.</span><span class="sxs-lookup"><span data-stu-id="cfa46-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="cfa46-114">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="cfa46-114">Click Select.</span></span>
5. <span data-ttu-id="cfa46-115">Spustelėkite Naujas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="cfa46-115">Click New sales order.</span></span>
    * <span data-ttu-id="cfa46-116">Neblogai būtų įsidėmėti pardavimo užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="cfa46-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="cfa46-117">Jo prireiks vėliau šios procedūros metu.</span><span class="sxs-lookup"><span data-stu-id="cfa46-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="cfa46-118">Lauke Prekės numeris įveskite 88000 ir paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="cfa46-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="cfa46-119">Tai yra tęstinė prekė demonstracinių duomenų įmonėje USRT.</span><span class="sxs-lookup"><span data-stu-id="cfa46-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="cfa46-120">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="cfa46-120">Click Complete.</span></span>
8. <span data-ttu-id="cfa46-121">Lauke Mokėjimo būdas įveskite Visa.</span><span class="sxs-lookup"><span data-stu-id="cfa46-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="cfa46-122">Spustelėkite Įtraukti kredito kortelę.</span><span class="sxs-lookup"><span data-stu-id="cfa46-122">Click Add credit card.</span></span>
    * <span data-ttu-id="cfa46-123">Įveskite reikiamą kredito kortelės informaciją šiame puslapį.</span><span class="sxs-lookup"><span data-stu-id="cfa46-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="cfa46-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cfa46-124">Click OK.</span></span>
11. <span data-ttu-id="cfa46-125">Išplėskite skyrių „Mokėjimas“.</span><span class="sxs-lookup"><span data-stu-id="cfa46-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="cfa46-126">Norint pateikti skambučių centro užsakymą, turi būti įvesti užsakymo mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="cfa46-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="cfa46-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cfa46-127">Click OK.</span></span>
13. <span data-ttu-id="cfa46-128">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="cfa46-128">Click Submit.</span></span>
    * <span data-ttu-id="cfa46-129">Sukūrėte naują tęstinumo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="cfa46-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="cfa46-130">Dabar reikia atlikti du paketinius procesus, kurie yra naudojami tęstinumo užsakymams apdoroti.</span><span class="sxs-lookup"><span data-stu-id="cfa46-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="cfa46-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="cfa46-131">Close the page.</span></span>
15. <span data-ttu-id="cfa46-132">Pasirinkite Mažmeninė prekyba ir prekyba > Tęstinumas > Apdoroti tęstinius mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="cfa46-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="cfa46-133">Lauke Tęstinė prekė įveskite 88000 ir paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="cfa46-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="cfa46-134">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cfa46-134">Click OK.</span></span>
18. <span data-ttu-id="cfa46-135">Pasirinkite Mažmeninė prekyba ir prekyba > Tęstinumas > Tęstinių antrinių užsakymų kūrimas.</span><span class="sxs-lookup"><span data-stu-id="cfa46-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="cfa46-136">Šiuo procesu bus sukurti nauji pardavimo užsakymai pagal tęstinumo programos parametrus.</span><span class="sxs-lookup"><span data-stu-id="cfa46-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="cfa46-137">Lauke Tęstinė prekė įveskite 88000 ir paspauskite klavišą TAB.</span><span class="sxs-lookup"><span data-stu-id="cfa46-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="cfa46-138">Prekė 88000 yra tęstinė prekė demonstracinių duomenų įmonėje USRT.</span><span class="sxs-lookup"><span data-stu-id="cfa46-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="cfa46-139">Lauke Pardavimo užsakymas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cfa46-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="cfa46-140">Įveskite pardavimo užsakymo numerį, kurį įsidėmėjote šios procedūros metu anksčiau.</span><span class="sxs-lookup"><span data-stu-id="cfa46-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="cfa46-141">Tokiu būdu šios procedūros metu apdorojimo laikas bus kiek įmanoma trumpesnis.</span><span class="sxs-lookup"><span data-stu-id="cfa46-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="cfa46-142">Laukas Pardavimo užsakymo nėra būtinas – galite apdoroti visus bet kurios vienos programos užsakymus.</span><span class="sxs-lookup"><span data-stu-id="cfa46-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="cfa46-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cfa46-143">Click OK.</span></span>

