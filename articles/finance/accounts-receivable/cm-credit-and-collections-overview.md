---
title: Kredito ir surinkimo apžvalga
description: Šioje temoje pateikta kreditų ir surinkimo funkcijų apžvalga.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67e0b3d1058e5fc085f51577ccf0b79e51546de0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976600"
---
# <a name="credit-and-collections-overview"></a><span data-ttu-id="b1e3d-103">Kredito ir surinkimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b1e3d-103">Credit and collections overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e3d-104">Galite valdyti savo klientų kreditų limitus ir vykdyti surinkimo veiklas, kai jos tampa būtinos.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-104">You can manage credit limits for your customers and perform collection activities when they become necessary.</span></span>

## <a name="credit-management"></a><span data-ttu-id="b1e3d-105">Kredito valdymas</span><span class="sxs-lookup"><span data-stu-id="b1e3d-105">Credit management</span></span>

<span data-ttu-id="b1e3d-106">Kliento kredito valdymas leidžia valdyti kreditų limitus ir kontroliuoti pardavimo užsakymų eigą naudojant registravimo procesą, pagrįstą sukurtomis kredito taisyklėmis.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-106">Customer credit management lets you manage credit limits and control the flow of sales orders through the posting process, based on credit rules that you create.</span></span>

<span data-ttu-id="b1e3d-107">Kredito valdymo naudojimo procesas gali apimti bet kuriuos toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-107">The credit management process can include any of the following steps:</span></span>

- <span data-ttu-id="b1e3d-108">Klientų su kredito atributais, kurie suteikia papildomos informacijos apie jų kreditingumą, naujinimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-108">Update credit attributes for customers to provide additional information about their credit worthiness.</span></span>
- <span data-ttu-id="b1e3d-109">Klientų, naudojančių kredito limito koregavimą, kredito limitų kūrimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-109">Create credit limits for customers by using credit limit adjustments.</span></span>
- <span data-ttu-id="b1e3d-110">Klientų, naudojančių kredito limito koregavimą, laikinų kredito limitų kūrimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-110">Create temporary credit limits for customers by using credit limit adjustments.</span></span> <span data-ttu-id="b1e3d-111">Tokiu būdu galite laikinai padidinti arba sumažinti kliento kredito limitus pagal verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-111">In this way, you can temporarily increase or decrease customer credit limits, based on business requirements.</span></span>
- <span data-ttu-id="b1e3d-112">Papildomos informacijos, kuri gali turėti įtakos kredito limitui, pavyzdžiui, draudimo ir garantijų įtraukimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-112">Add information that can affect the credit limit, such as information about insurance and guarantees.</span></span>
- <span data-ttu-id="b1e3d-113">Klientų kredito grupių, kurios susieja klientus, kad jie galėtų naudotis vienu kredito limitu, kūrimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-113">Create customer credit groups that link customers together so that they share a single credit limit.</span></span>
- <span data-ttu-id="b1e3d-114">Rizikos šaltinių priskyrimas klientams ir tokių įvertinimų naudojimas norint automatiškai sugeneruoti kredito limitus klientams, naudojantiems kredito limito koregavimą.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-114">Assign risk scores to customers, and then use the scores to automatically generate credit limits for those customers through credit limit adjustments.</span></span>
- <span data-ttu-id="b1e3d-115">Blokavimo taisyklių, pagal kurias sulaikomas užsakymas vieno ar kelių registravimų proceso metu pagal tokius veiksnius kaip rizika, mokėjimo sąlygos, kredito limitai, pradelstos sumos ir išnaudoto kredito limito procentas kūrimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-115">Create blocking rules that put an order on hold during one or more posting processes, based on factors such as risk, payment terms, credit limits, overdue amounts, and the percentage of the credit limit that has been used.</span></span>
- <span data-ttu-id="b1e3d-116">Sulaikytų pardavimo užsakymų valdymas, sulaikymo priežasčių peržiūrėjimas ir problemų šalinimas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-116">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate issues.</span></span>
- <span data-ttu-id="b1e3d-117">Pardavimo užsakymų išleidimas, kad būtų galima tęsti registravimo procesą.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-117">Release sales orders so that they continue through the posting process.</span></span>
- <span data-ttu-id="b1e3d-118">Darbo eigos, skirtos kredito limito keitimų patvirtinimui ir pardavimo užsakymų išleidimui, nustatymas.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-118">Set up a workflow to manage the approval of credit limit changes and sales order releases.</span></span>

## <a name="collections-management"></a><span data-ttu-id="b1e3d-119">Mokėjimų priežiūros valdymas</span><span class="sxs-lookup"><span data-stu-id="b1e3d-119">Collections management</span></span>

<span data-ttu-id="b1e3d-120">Puslapyje **Mokėjimų priežiūra** pateiktas centralizuotas rodinys, kuriame valdoma gautinų sumų surinkimo informacija.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-120">The **Collections** page provides a centralized view where accounts receivable collections information is managed.</span></span> <span data-ttu-id="b1e3d-121">Naudodami šį centrinį rodinį surinkimo vadovai gali valdyti surinkimą.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-121">Collections managers can use this centralized view to manage collections.</span></span> <span data-ttu-id="b1e3d-122">Surinkimo agentai pradėti surinkimo procesą gali iš klientų sąrašų, kurie sugeneruojami naudojant iš anksto apibrėžtus surinkimo kriterijus, arba iš puslapio **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-122">Collections agents can begin the collections process either from customer lists that are generated by using predefined collection criteria or from the **Customers** page.</span></span>

<span data-ttu-id="b1e3d-123">Prieš pradėdami kurti ar dirbti su surinkimu, turite susipažinti su šiomis sąvokomis:</span><span class="sxs-lookup"><span data-stu-id="b1e3d-123">Before you start to set up or work with collections, you should understand the following concepts:</span></span>

- <span data-ttu-id="b1e3d-124">Klientų skirstymo pagal terminus momentinėje kopijoje yra skirstymo pagal terminus balanso informacija konkrečiu metu.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-124">Customer aging snapshots contain aged balance information at a specific point in time.</span></span>
- <span data-ttu-id="b1e3d-125">Klientų surinkimo telkiniai padės organizuoti darbą.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-125">Collections customer pools help you organize your work.</span></span>
- <span data-ttu-id="b1e3d-126">Surinkimo agentai gali turėti savo klientų telkinius.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-126">Collections agents can have their own customer pools.</span></span>
- <span data-ttu-id="b1e3d-127">Sąrašų puslapiuose organizuojami surinkimo klientai, veikla ir atvejai.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-127">List pages organize collections customers, activities, and cases.</span></span>
- <span data-ttu-id="b1e3d-128">Visa kliento surinkimo informacija yra viename puslapyje, ir iš šio puslapio galite imtis veiksmų.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-128">All collections information for a customer is on one page, and you can take action from that page.</span></span>
- <span data-ttu-id="b1e3d-129">Atsisakyti, grąžinti arba atšaukti palūkanas ir mokesčius galima vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-129">Interest and fees can be waived, reinstated, or reversed in one step.</span></span>
- <span data-ttu-id="b1e3d-130">Sukurti nurašymo operacijas galima sukurti vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-130">Write-off transactions can be created in one step.</span></span>
- <span data-ttu-id="b1e3d-131">Apdoroti lėšų trūkumo (NSF) mokėjimus galima vienu veiksmu.</span><span class="sxs-lookup"><span data-stu-id="b1e3d-131">Not sufficient funds (NSF) payments can be processed in one step.</span></span>

<span data-ttu-id="b1e3d-132">Šių sąvokų aprašymų ieškokite [Pagrindinės surinkimo valdymo koncepcijos](./cm-collections-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="b1e3d-132">For descriptions of these concepts, see [Collections management key concepts](./cm-collections-concepts.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1e3d-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b1e3d-133">Additional resources</span></span>

[<span data-ttu-id="b1e3d-134">Klientų kredito valdymo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b1e3d-134">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="b1e3d-135">Informacija apie klientų kredito valdymo sąranką</span><span class="sxs-lookup"><span data-stu-id="b1e3d-135">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="b1e3d-136">Kliento kredito tvarkymo informacijos įtraukimas</span><span class="sxs-lookup"><span data-stu-id="b1e3d-136">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="b1e3d-137">Kliento kredito grupės</span><span class="sxs-lookup"><span data-stu-id="b1e3d-137">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="b1e3d-138">Kliento kredito limito koregavimai</span><span class="sxs-lookup"><span data-stu-id="b1e3d-138">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="b1e3d-139">Pardavimo užsakymų kredito sulaikymai</span><span class="sxs-lookup"><span data-stu-id="b1e3d-139">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="b1e3d-140">Periodinės kliento kredito valdymo užduotys</span><span class="sxs-lookup"><span data-stu-id="b1e3d-140">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)
