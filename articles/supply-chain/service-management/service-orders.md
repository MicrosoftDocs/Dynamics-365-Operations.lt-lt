---
title: "Aptarnavimo užsakymai"
description: "Aptarnavimo užsakymas rodo techniko apsilankymą pas klientą tam tikrą dieną."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4da0b965f3719bc16b5a73538df111ff6df071be
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="service-orders"></a><span data-ttu-id="a9dab-103">Aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="a9dab-103">Service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a9dab-104">Aptarnavimo užsakymas rodo techniko apsilankymą pas klientą tam tikrą dieną.</span><span class="sxs-lookup"><span data-stu-id="a9dab-104">A service order represents a visit that a service technician makes to a customer site on a specific date.</span></span> <span data-ttu-id="a9dab-105">Kiekvieną aptarnavimo užsakymą sudaro viena arba daugiau aptarnavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="a9dab-105">Each service order consists of one or more service order lines.</span></span> <span data-ttu-id="a9dab-106">Aptarnavimo užsakymo eilutėse rodomos privalomos techniko darbo valandos ir susijusios prekės, išlaidos bei mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="a9dab-106">Service order lines represent the hours of work that must be performed by the service technician, and the related items, expenses, and fees.</span></span>

<span data-ttu-id="a9dab-107">Prie aptarnavimo užsakymo eilutės galite pridėti užduočių ir objektų.</span><span class="sxs-lookup"><span data-stu-id="a9dab-107">You can attach tasks and objects to a service order line.</span></span> <span data-ttu-id="a9dab-108">Po to galite galite grupuoti aptarnavimo užsakymo eilutes pagal užduotį arba objektą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-108">You can then group service order lines by task or by object.</span></span> <span data-ttu-id="a9dab-109">Taip pat prie aptarnavimo užsakymo eilučių galima pridėti atsargose išvardytų prekių.</span><span class="sxs-lookup"><span data-stu-id="a9dab-109">You can also attach items that are listed in inventory to service order lines.</span></span>

## <a name="create-service-orders"></a><span data-ttu-id="a9dab-110">Kurti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="a9dab-110">Create service orders</span></span>

<span data-ttu-id="a9dab-111">Pagal aptarnavimo sutartį ir tos sutarties eilutes galite sukurti aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-111">You can create service orders based on a service agreement and the lines that are contained in that agreement.</span></span> <span data-ttu-id="a9dab-112">Tačiau galite sukurti aptarnavimo užsakymus, kurie susieti su aptarnavimo sutartimi tik sutartyje nurodytu laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="a9dab-112">However, you can create service orders that are associated with a service agreement only in the period that is specified in the agreement.</span></span> <span data-ttu-id="a9dab-113">Pavyzdžiui, jei aptarnavimo sutartis galioja 2011 kalendoriniams metams, galite sukurti sutarties aptarnavimo užsakymą nuo 2011 m. sausio 1 d. iki 2011 m. gruodžio 31 d.</span><span class="sxs-lookup"><span data-stu-id="a9dab-113">For example, if a service agreement is valid for the 2011 calendar year, you can create service orders for the agreement from January 1, 2011, and December 31, 2011.</span></span>

<span data-ttu-id="a9dab-114">Taip pat galite sukurti atskirus aptarnavimo užsakymus, nesusiedami jų su sutartimi.</span><span class="sxs-lookup"><span data-stu-id="a9dab-114">You can also create service orders individually, without associating them with an agreement.</span></span> <span data-ttu-id="a9dab-115">Šiuos aptarnavimo užsakymus galima panaudoti apdorojant nesuplanuotus arba vienkartinius aptarnavimo vizitus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-115">These service orders can be used to handle unscheduled or one-time service visits.</span></span> <span data-ttu-id="a9dab-116">Pavyzdžiui, kovo mėnesį jūsų klientas nori, kad aptarnavimas būtų atliktas dviem mašinoms, neskaitant aptarnavimo sutartyje nurodytų mašinų.</span><span class="sxs-lookup"><span data-stu-id="a9dab-116">For example, in the month of March, your customer wants service to be performed on two machines, in addition to the machines that are specified in the service agreement.</span></span> <span data-ttu-id="a9dab-117">Šiai užduočiai sukuriate aptarnavimo užsakymus, bet nesusiejate jų su sutartimi.</span><span class="sxs-lookup"><span data-stu-id="a9dab-117">For this task, you create service orders but do not associate them with an agreement.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a9dab-118">Norėdami sukurti su aptarnavimo sutartimi nesusietus aptarnavimo užsakymus, formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG> turite pažymėti žymės langelį <STRONG>Leisti be aptarnavimo sutarties</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a9dab-118">To create service orders that are not associated with a service agreement, you must select the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form.</span></span></P>

<span data-ttu-id="a9dab-119">**Scenarijus**</span><span class="sxs-lookup"><span data-stu-id="a9dab-119">**Scenario**</span></span>

<span data-ttu-id="a9dab-120">Toliau pateiktoje situacijoje aprašoma kita situacija, kurioje naudinga sukurti su aptarnavimo sutartimi nesusietą aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-120">The following scenario describes another situation where it is useful to create a service order that is not associated with a service agreement.</span></span>

<span data-ttu-id="a9dab-121">Įmonės dispečeris sulaukia skambučio dėl skubaus elevatoriaus remonto.</span><span class="sxs-lookup"><span data-stu-id="a9dab-121">The company dispatcher receives a call requesting emergency service on an elevator.</span></span> <span data-ttu-id="a9dab-122">Nėra laiko paruošti aptarnavimo sutartį ir aptarnavimo projektą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-122">There is no time to set up a service agreement and a project for the service.</span></span> <span data-ttu-id="a9dab-123">Todėl dispečeris aptarnavimo užsakymą sukuria tiesiogiai formoje **Aptarnavimo užsakymai**, prie esamo projekto prideda aptarnavimo užsakymą ir sukuria aptarnavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="a9dab-123">Therefore, the dispatcher creates a service order directly in the **Service orders** form, attaches the service order to an existing project, and creates the service order lines.</span></span> <span data-ttu-id="a9dab-124">Esamam aptarnavimo užsakymui dispečeris taip pat sukuria užduoties arba objekto ryšį, kad būtų galima įrašyti su aptarnavimo sutartimi nesusijusį darbą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-124">The dispatcher also creates a task or object relation for an existing service order, to record work that is not related to the service agreement.</span></span> <span data-ttu-id="a9dab-125">Daugiau informacijos rasite failuose [Neautomatinis aptarnavimo užsakymų kūrimas](create-service-orders-manually.md) ir [Aptarnavimo užduočių ryšių kūrimas](create-service-task-relations.md).</span><span class="sxs-lookup"><span data-stu-id="a9dab-125">For more information, see [Create service orders manually](create-service-orders-manually.md) and [Create service task relations](create-service-task-relations.md).</span></span>

## <a name="monitor-the-progress-of-service-orders"></a><span data-ttu-id="a9dab-126">Stebėkite aptarnavimo užsakymų vykdymo eigą</span><span class="sxs-lookup"><span data-stu-id="a9dab-126">Monitor the progress of service orders</span></span>

<span data-ttu-id="a9dab-127">Norėdami stebėti pardavimo užsakymo vykdymo eigą (pagal įvairias komandas ir darbo procesus), galite nustatyti aptarnavimo užsakymų etapų sistemą ir priežasčių kodus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-127">To monitor the progress of a sales order through the different teams and work processes, you can set up a system of stages and reason codes for service orders.</span></span> <span data-ttu-id="a9dab-128">Galite nurodyti leistinus kiekvieno etapo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-128">For each stage, you can specify the actions that are allowed.</span></span> <span data-ttu-id="a9dab-129">Daugiau informacijos rasite faile [Priežasčių kodų kūrimas](create-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a9dab-129">For more information, see [Create reason codes](create-reason-codes.md).</span></span>

<span data-ttu-id="a9dab-130">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="a9dab-130">**Example**</span></span>

<span data-ttu-id="a9dab-131">Aptarnavimo užsakymą patvirtina dispečeris.</span><span class="sxs-lookup"><span data-stu-id="a9dab-131">A service order is approved by the dispatcher.</span></span> <span data-ttu-id="a9dab-132">Dispečeris atnaujina aptarnavimo užsakymo etapą ir nurodo priežasties kodą, reiškiantį, kad aptarnavimo užsakymas perduotas aptarnaujančiam technikui.</span><span class="sxs-lookup"><span data-stu-id="a9dab-132">The dispatcher updates the stage of the service order and specifies a reason code that indicates that the service order has been released to the service technician.</span></span> <span data-ttu-id="a9dab-133">Technikas vyksta pas klientą ir atlieka aptarnavimo darbus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-133">The technician goes to the customer site and performs the service.</span></span>

## <a name="specify-item-requirements-for-service-orders"></a><span data-ttu-id="a9dab-134">Prekių poreikių nurodymas pagal aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="a9dab-134">Specify item requirements for service orders</span></span>

<span data-ttu-id="a9dab-135">Galite nurodyti aptarnavimo užsakymams vykdyti reikiamas atsargų prekes.</span><span class="sxs-lookup"><span data-stu-id="a9dab-135">You can specify the inventory items that are required for service orders.</span></span> <span data-ttu-id="a9dab-136">Tačiau aptarnavimo užsakymas turi būti susietas su projektu.</span><span class="sxs-lookup"><span data-stu-id="a9dab-136">However, the service order must be associated with a project.</span></span> <span data-ttu-id="a9dab-137">Prekės poreikiai aptarnavimo užsakymuose apdorojami vykdant projektą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-137">Item requirements for service orders are processed through a project.</span></span> 

<span data-ttu-id="a9dab-138">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="a9dab-138">**Example**</span></span>

<span data-ttu-id="a9dab-139">Pagal aptarnavimo sutartį sukurtus aptarnavimo užsakymus apdoroja dispečeris.</span><span class="sxs-lookup"><span data-stu-id="a9dab-139">The service orders that are created from the service agreement are processed by the dispatcher.</span></span> <span data-ttu-id="a9dab-140">Dispečeris pastebi, kad norint įvykdyti pirmą aptarnavimo užsakymą technikui prireiks svarbios atsarginės detalės, kurios nėra atsargose.</span><span class="sxs-lookup"><span data-stu-id="a9dab-140">For the first service order, the dispatcher realizes that the service technician requires an important spare part that is not in the on-hand inventory.</span></span> <span data-ttu-id="a9dab-141">Todėl tiesiogiai aptarnavimo užsakyme dispečeris sukuria tos atsarginės dalies prekės poreikį.</span><span class="sxs-lookup"><span data-stu-id="a9dab-141">Therefore, the dispatcher creates an item requirement for the spare part directly from the service order.</span></span>

## <a name="move-and-post-lines"></a><span data-ttu-id="a9dab-142">Eilučių perkėlimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="a9dab-142">Move and post lines</span></span>

<span data-ttu-id="a9dab-143">Aptarnavimo technikas grįžta po aptarnavimo vizito ir pakeičia bei atnaujina aptarnavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="a9dab-143">A service technician returns from a service visit, and then modifies and updates the service order lines.</span></span> <span data-ttu-id="a9dab-144">Per šį aptarnavimo vizitą technikas taip pat atliko aptarnavimo užduotį, kurią buvo suplanuota atlikti per kitą aptarnavimo vizitą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-144">During the service visit, the technician performed a service job that was scheduled for the next service visit.</span></span> <span data-ttu-id="a9dab-145">Todėl kito aptarnavimo vizito eilutes technikas perkelia į dabartinį aptarnavimo vizitą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-145">Therefore, the technician moves the lines from the next service visit to the current service visit.</span></span> <span data-ttu-id="a9dab-146">Po to technikas užregistruoja aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-146">The technician then posts the service order.</span></span> <span data-ttu-id="a9dab-147">Daugiau informacijos rasite faile [Aptarnavimo užsakymų eilučių perkėlimas](move-service-order-lines.md).</span><span class="sxs-lookup"><span data-stu-id="a9dab-147">For more information, see [Move service order lines](move-service-order-lines.md).</span></span>

## <a name="cancel-service-orders"></a><span data-ttu-id="a9dab-148">Atšaukti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="a9dab-148">Cancel service orders</span></span>

<span data-ttu-id="a9dab-149">Vienas iš kitų sausio mėnesiui sugeneruotų aptarnavimo užsakymų tampa nereikalingas, nes užduotis atšaukta.</span><span class="sxs-lookup"><span data-stu-id="a9dab-149">One of the other service orders that was generated for the month of January becomes obsolete, because the job is canceled.</span></span> <span data-ttu-id="a9dab-150">Todėl dispečeris atšaukia aptarnavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a9dab-150">Therefore, the service dispatcher cancels the service order.</span></span> <span data-ttu-id="a9dab-151">Daugiau informacijos rasite faile [Aptarnavimo užsakymų atšaukimas](cancel-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a9dab-151">For more information, see [Cancel service orders](cancel-service-orders.md).</span></span>

## <a name="post-from-projects"></a><span data-ttu-id="a9dab-152">Registravimas iš projektų</span><span class="sxs-lookup"><span data-stu-id="a9dab-152">Post from projects</span></span>

<span data-ttu-id="a9dab-153">Kiekvienos savaitės pabaigoje dispečeris nori užregistruoti visus prie tam tikro projekto pridėtus aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-153">At the end of each week, the dispatcher wants to post all service orders that are attached to a specific project.</span></span> <span data-ttu-id="a9dab-154">Todėl dispečeris suranda reikiamą projektą formoje **Projektai** ir užregistruoja įvykdytus aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-154">Therefore, the dispatcher locates the relevant project in the **Projects** form and posts the service orders that have been completed.</span></span> <span data-ttu-id="a9dab-155">Daugiau informacijos ieškokite [Aptarnavimo užsakymų registravimas (klasės forma)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="a9dab-155">For more information, see [Post service orders (class form)](https://technet.microsoft.com/en-us/library/aa574685\(v=ax.60\)).</span></span>

## <a name="delete-service-orders"></a><span data-ttu-id="a9dab-156">Naikinti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="a9dab-156">Delete service orders</span></span>

<span data-ttu-id="a9dab-157">Antroje metų pusėje jūsų klientas nusprendžia, kad aptarnavimo vizitai pernelyg reti.</span><span class="sxs-lookup"><span data-stu-id="a9dab-157">During the second half of the year, your customer decides that the service visits are too infrequent.</span></span> <span data-ttu-id="a9dab-158">Likusiam aptarnavimo sutarties laikotarpiui turite sukurti naują, dažnesnių apsilankymų seriją.</span><span class="sxs-lookup"><span data-stu-id="a9dab-158">You must create a new, more frequent series of service visits for the remaining time on the service agreement.</span></span> <span data-ttu-id="a9dab-159">Todėl reikia panaikinti esamus aptarnavimo užsakymus ir sukurti naujus.</span><span class="sxs-lookup"><span data-stu-id="a9dab-159">Therefore, you must delete the existing service orders and create new service orders.</span></span> <span data-ttu-id="a9dab-160">Daugiau informacijos rasite faile [Aptarnavimo užsakymų naikinimas](delete-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a9dab-160">For more information, see [Delete service orders](delete-service-orders.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a9dab-161">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a9dab-161">See also</span></span>

<span data-ttu-id="a9dab-162">[Aptarnavimo užsakymai (forma)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a9dab-162">[Service orders (form)](https://technet.microsoft.com/en-us/library/aa554361\(v=ax.60\))</span></span>

  


