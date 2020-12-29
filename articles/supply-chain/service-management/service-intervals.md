---
title: Aptarnavimo intervalai
description: Aptarnavimo intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai kuriate aptarnavimo užsakymus.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433681"
---
# <a name="service-intervals"></a><span data-ttu-id="3fa33-103">Aptarnavimo intervalai</span><span class="sxs-lookup"><span data-stu-id="3fa33-103">Service intervals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fa33-104">Aptarnavimo sutarties intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai automatiškai kuriate aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="3fa33-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="3fa33-105">Kai automatiškai kuriate aptarnavimo užsakymus, aptarnavimo užsakymo eilutės kuriamos pagal intervalą, kurį nurodėte aptarnavimo sutarties eilutėje, nuo sutarties eilutės pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="3fa33-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="3fa33-106">Jei puslapyje **Aptarnavimo sutartys** esančios aptarnavimo sutarties eilutės laukas **Intervalas** yra tuščias, eilutė yra vienkartinis įvykis, ir ji nenaudojama pakartotinai kurti aptarnavimo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="3fa33-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="3fa33-107">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3fa33-107">Example</span></span>

<span data-ttu-id="3fa33-108">Šis pavyzdys iliustruoja, kaip aptarnavimo intervalas paveiks aptarnavimo sutarties eilutes ir aptarnavimo užsakymo eilutes aptarnavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="3fa33-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="3fa33-109">Aptarnavimo sutarties kūrimas</span><span class="sxs-lookup"><span data-stu-id="3fa33-109">Create a service agreement</span></span>

<span data-ttu-id="3fa33-110">Pirma, sukurkite aptarnavimo sutartį ir nustatykite parinkties **Jungti aptarnavimo užsakymus** kriterijų **Pagal aptarnavimo sutartį**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="3fa33-111">Spustelėkite **Aptarnavimo sutartys**</span><span class="sxs-lookup"><span data-stu-id="3fa33-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="3fa33-112">**Veiksmų srityje**, skirtuke **Aptarnavimo sutartis**, grupėje **Nauja** spustelėkite **Aptarnavimo sutartis**, kad sukurtumėte naują aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="3fa33-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="3fa33-113">Įveskite aprašymą, lauke **Projekto ID** pasirinkite projektą ir įveskite datą lauke **Pradžios data**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="3fa33-114">Lauke **Jungti aptarnavimo užsakymus** pasirinkite **Pagal aptarnavimo sutartį**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="3fa33-115">Dabar sukūrėte tokią aptarnavimo sutartį:</span><span class="sxs-lookup"><span data-stu-id="3fa33-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="3fa33-116">Project</span><span class="sxs-lookup"><span data-stu-id="3fa33-116">Project</span></span>      | <span data-ttu-id="3fa33-117">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="3fa33-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa33-118">Jūsų projektas</span><span class="sxs-lookup"><span data-stu-id="3fa33-118">Your project</span></span> | <span data-ttu-id="3fa33-119">Jūsų nurodyta projekto data.</span><span class="sxs-lookup"><span data-stu-id="3fa33-119">The date you specified for the project.</span></span> <span data-ttu-id="3fa33-120">Šiame pavyzdyje naudojama dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="3fa33-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="3fa33-121">Aptarnavimo sutarties eilutės kūrimas</span><span class="sxs-lookup"><span data-stu-id="3fa33-121">Create a service agreement line</span></span>

<span data-ttu-id="3fa33-122">Po to sukurkite aptarnavimo sutarties eilutę, kurios operacijos tipas yra **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="3fa33-123">Norėdami baigti šią pavyzdžio dalį, puslapyje **Aptarnavimo intervalai** turite sukurti 10 dienų aptarnavimo intervalą.</span><span class="sxs-lookup"><span data-stu-id="3fa33-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="3fa33-124">Pasirinkite ką tik sukurtą aptarnavimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="3fa33-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="3fa33-125">„FastTab“ skirtuke **Eilutės** spustelėkite mygtuką **Pridėti**, kad sukurtumėte naują eilutę apatinėje puslapio **Aptarnavimo sutartys** srityje.</span><span class="sxs-lookup"><span data-stu-id="3fa33-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="3fa33-126">Lauke **Operacijos tipas** pasirinkite **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="3fa33-127">Lauke **Darbininkas** pasirinkite darbininką, kuris atliks aptarnavimą.</span><span class="sxs-lookup"><span data-stu-id="3fa33-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="3fa33-128">Lauke **Aptarnavimo intervalas** pasirinkite 10 dienų intervalą.</span><span class="sxs-lookup"><span data-stu-id="3fa33-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="3fa33-129">Ką tik sukūrėte tokią aptarnavimo sutarties eilutę su tokia informacija:</span><span class="sxs-lookup"><span data-stu-id="3fa33-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="3fa33-130">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="3fa33-130">Transaction type</span></span> | <span data-ttu-id="3fa33-131">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="3fa33-131">Start date</span></span>                               | <span data-ttu-id="3fa33-132">Paslaugos intervalas</span><span class="sxs-lookup"><span data-stu-id="3fa33-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="3fa33-133">Valanda</span><span class="sxs-lookup"><span data-stu-id="3fa33-133">Hour</span></span>             | <span data-ttu-id="3fa33-134">Dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="3fa33-134">The current date.</span></span>                        | <span data-ttu-id="3fa33-135">Kas 10 dienų</span><span class="sxs-lookup"><span data-stu-id="3fa33-135">Every 10 days</span></span>    |
| <span data-ttu-id="3fa33-136">Darbuotojas</span><span class="sxs-lookup"><span data-stu-id="3fa33-136">Worker</span></span>           | <span data-ttu-id="3fa33-137">Darbininkas, atliksiantis aptarnavimą.</span><span class="sxs-lookup"><span data-stu-id="3fa33-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="3fa33-138">Eilutėje nenurodytas joks laiko langas.</span><span class="sxs-lookup"><span data-stu-id="3fa33-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="3fa33-139">Suplanuotų aptarnavimo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="3fa33-139">Create planned service orders</span></span>

<span data-ttu-id="3fa33-140">Dabar galite kurti suplanuotus aptarnavimo užsakymus ir aptarnavimo užsakymų eilutes kitam mėnesiui.</span><span class="sxs-lookup"><span data-stu-id="3fa33-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="3fa33-141">Puslapyje **Aptarnavimo sutartys**, **Veiksmų srityje**, skirtuke **Pristatyti** spustelėkite **Suplanuoti aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="3fa33-142">Puslapyje **Aptarnavimo užsakymų kūrimas** esančiame lauke **Nuo kada** įveskite dabartinę datą, o lauke **Iki kada** – datą, kuri yra už vieno mėnesio nuo dabartinės datos.</span><span class="sxs-lookup"><span data-stu-id="3fa33-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="3fa33-143">Slankiklį **Valanda** nustatykite į padėtį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="3fa33-144">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-144">Click **OK**.</span></span>

<span data-ttu-id="3fa33-145">Aptarnavimo užsakymas nepriskirtas grupei (grupavimą nurodo pasirinktis **Pagal aptarnavimo sutartį** lauke **Jungti aptarnavimo užsakymus**), vienam aptarnavimo užsakymui sukuriama viena aptarnavimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="3fa33-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="3fa33-146">Sukurti aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="3fa33-146">Service orders created</span></span>

<span data-ttu-id="3fa33-147">Sukurtos trys aptarnavimo užsakymo eilutės patenka į laiko ribas, kurias nurodėte dialogo lange **Aptarnavimo užsakymų kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="3fa33-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="3fa33-148">Aptarnavimo užsakymo eilutes galite peržiūrėti puslapyje **Aptarnavimo sutartys** (**Veiksmų sritis** \> skirtukas **Pristatyti** \>mygtukas **Peržiūrėti**).</span><span class="sxs-lookup"><span data-stu-id="3fa33-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fa33-149">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="3fa33-149">Related topics</span></span>

[<span data-ttu-id="3fa33-150">Aptarnavimo intervalų nustatymas</span><span class="sxs-lookup"><span data-stu-id="3fa33-150">Set up service intervals</span></span>](set-up-service-intervals.md)  

