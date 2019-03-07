---
title: Aptarnavimo valdymas
description: Naudodamiesi parinktimi Paslaugų valdymas galite nustatyti paslaugų sutarčių sąlygas ir paslaugų abonementinius mokesčius, tvarkyti paslaugų užsakymus ir klientų užklausas, valdyti ir analizuoti paslaugų teikimą klientams.
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "343816"
---
# <a name="service-management"></a><span data-ttu-id="776e3-103">Aptarnavimo valdymas</span><span class="sxs-lookup"><span data-stu-id="776e3-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="776e3-104">Naudodamiesi parinktimi **Paslaugų valdymas** galite nustatyti paslaugų sutarčių sąlygas ir paslaugų abonementinius mokesčius, tvarkyti paslaugų užsakymus ir klientų užklausas, valdyti ir analizuoti paslaugų teikimą klientams.</span><span class="sxs-lookup"><span data-stu-id="776e3-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="776e3-105">Paslaugų sutartis galite naudoti norėdami nustatyti išteklius, naudojamus įprastam paslaugos vizitui.</span><span class="sxs-lookup"><span data-stu-id="776e3-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="776e3-106">Paslaugų sutartis taip pat galite naudoti norėdami peržiūrėti, kaip klientui išrašoma tų išteklių sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="776e3-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="776e3-107">Į paslaugų sutartį taip pat gali įeiti aptarnavimo lygio sutartis, kurioje nurodomas standartinis atsakymo laikas ir siūlomi faktiniam laikui įrašyti reikalingi įrankiai.</span><span class="sxs-lookup"><span data-stu-id="776e3-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="776e3-108">Galite sukurti paslaugų užsakymus, kad valdytumėte informaciją apie suplanuotus ir nesuplanuotus techninio darbuotojo vizitus kliento kompiuteryje.</span><span class="sxs-lookup"><span data-stu-id="776e3-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="776e3-109">Paslaugų užsakymuose pateikiama tokia informacija:</span><span class="sxs-lookup"><span data-stu-id="776e3-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="776e3-110">Techninio darbuotojo darbo valandos</span><span class="sxs-lookup"><span data-stu-id="776e3-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="776e3-111">Paslaugos ar remonto tipas</span><span class="sxs-lookup"><span data-stu-id="776e3-111">The type of service or repair</span></span>

3.  <span data-ttu-id="776e3-112">Prekė, kuriai reikalingas remontas, įskaitant išsamią informaciją apie požymius ir diagnozę</span><span class="sxs-lookup"><span data-stu-id="776e3-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="776e3-113">Visos išlaidos ir mokesčiai, susiję su paslauga arba remontu</span><span class="sxs-lookup"><span data-stu-id="776e3-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="776e3-114">Galite gauti, apdoroti ir išsiųsti aptarnavimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="776e3-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="776e3-115">Sukūrę paslaugų užsakymą, naudodami paslaugų etapus jūs galite stebėti eigą ir apibrėžti taisykles, kurios kontroliuoja, kokie veiksmai galimi kiekviename etape.</span><span class="sxs-lookup"><span data-stu-id="776e3-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="776e3-116">Baigę pildyti paslaugų užsakymą, galite išsiregistruoti ir patvirtinti, kad užsakymas baigtas, tada išsiųsti užsakymą ir pradėti sąskaitos faktūros procesą.</span><span class="sxs-lookup"><span data-stu-id="776e3-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="776e3-117">Naudokite ataskaitų įrankius, kad galėtumėte stebėti paslaugų užsakymų maržas ir abonementines operacijas ir spausdinti darbo aprašymus ir darbo kvitus.</span><span class="sxs-lookup"><span data-stu-id="776e3-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="776e3-118">Verslo procesai</span><span class="sxs-lookup"><span data-stu-id="776e3-118">Business processes</span></span>

<span data-ttu-id="776e3-119">Toliau pateiktoje diagramoje pavaizduoti aukšto lygio parinkties **Aptarnavimo valdymas** verslo procesai ir parodoma, kur aptarnavimo procesai integruojami su kitais „Microsoft Dynamics 365 for Finance and Operations“ moduliais.</span><span class="sxs-lookup"><span data-stu-id="776e3-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="776e3-120">[![Aptarnavimo valdymo verslo proceso diagrama](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="776e3-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="776e3-121">Paslaugų valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="776e3-121">Service management at a glance</span></span>

|<span data-ttu-id="776e3-122">Svarbios užduotys</span><span class="sxs-lookup"><span data-stu-id="776e3-122">Important tasks</span></span>           | <span data-ttu-id="776e3-123">Pagrindiniai puslapiai</span><span class="sxs-lookup"><span data-stu-id="776e3-123">Primary pages</span></span>                         |<span data-ttu-id="776e3-124">Populiarios ataskaitos</span><span class="sxs-lookup"><span data-stu-id="776e3-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="776e3-125">Aptarnavimo sutarčių vykdymas</span><span class="sxs-lookup"><span data-stu-id="776e3-125">Fulfill service agreements</span></span>|<span data-ttu-id="776e3-126">Aptarnavimo sutartys</span><span class="sxs-lookup"><span data-stu-id="776e3-126">Service agreements</span></span>                     |<span data-ttu-id="776e3-127">Aptarnavimo užsakymo marža</span><span class="sxs-lookup"><span data-stu-id="776e3-127">Service order margin</span></span>         |
|<span data-ttu-id="776e3-128">Apdoroti klientų užklausas</span><span class="sxs-lookup"><span data-stu-id="776e3-128">Handle customer inquiries</span></span> |<span data-ttu-id="776e3-129">Aptarnavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="776e3-129">Service orders</span></span>                         |<span data-ttu-id="776e3-130">Darbo aprašymas</span><span class="sxs-lookup"><span data-stu-id="776e3-130">Work description</span></span>             |
|                          |<span data-ttu-id="776e3-131">Išsiuntimo informacijos lenta</span><span class="sxs-lookup"><span data-stu-id="776e3-131">Dispatch board</span></span>                         |<span data-ttu-id="776e3-132">Operacija – Abonementas</span><span class="sxs-lookup"><span data-stu-id="776e3-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="776e3-133">Abonementinio mokesčio operacijos</span><span class="sxs-lookup"><span data-stu-id="776e3-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="776e3-134">Paslaugų valdymo integravimas</span><span class="sxs-lookup"><span data-stu-id="776e3-134">Integration of Service management</span></span>

<span data-ttu-id="776e3-135">Paslaugų valdymas gali būti integruotas į šiuos modulius:</span><span class="sxs-lookup"><span data-stu-id="776e3-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="776e3-136">Pardavimas ir rinkodara</span><span class="sxs-lookup"><span data-stu-id="776e3-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="776e3-137">Personalas</span><span class="sxs-lookup"><span data-stu-id="776e3-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  

