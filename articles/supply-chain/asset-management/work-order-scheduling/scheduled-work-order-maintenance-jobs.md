---
title: Suplanuotos darbo užsakymo priežiūros užduotys
description: Šioje temoje paaiškintos suplanuotų darbo užsakymų priežiūros užduotys modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887187"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="53f1e-103">Suplanuotos darbo užsakymo priežiūros užduotys</span><span class="sxs-lookup"><span data-stu-id="53f1e-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="53f1e-104">Puslapis **Suplanuotų darbo užsakymų priežiūros užduotys** skirtas apžvelgti ištekliams priskirtus darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="53f1e-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="53f1e-105">Sąraše rodomi darbo užsakymai, kuriuose naudojami išteklių tipai „Žmogiškieji ištekliai“, „Įrankis“ ir „Įrenginys“.</span><span class="sxs-lookup"><span data-stu-id="53f1e-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="53f1e-106">Sąrašą galima naudoti norint apžvelgti konkretiems ištekliams priskirtus darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="53f1e-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="53f1e-107">Taip pat galite jį naudoti, kad greitai rastumėte priežiūros darbuotojui, kuris, pavyzdžiui, šį rytą pranešė, kad susirgo, priskirtą darbo užsakymą, o tada galėtumėte užduočiai greitai priskirti kitą priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="53f1e-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="53f1e-108">Suplanuotų darbo užsakymų priežiūros užduočių peržiūra</span><span class="sxs-lookup"><span data-stu-id="53f1e-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="53f1e-109">Spustelėkite **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Suplanuotų darbo užsakymų priežiūros užduotys**.</span><span class="sxs-lookup"><span data-stu-id="53f1e-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="53f1e-110">Matysite visų darbo užsakymų, kurių nustatyta darbo užsakymo ciklo būsena yra „Suplanuotas“ arba „Vykdomas“, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="53f1e-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="53f1e-111">Sąrašą galite rikiuoti, pavyzdžiui, pagal priežiūros darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="53f1e-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="53f1e-112">Taip pat galite naudoti filtrą, kad sąraše būtų rodomi tik konkretiems ištekliams ar priežiūros darbuotojui priskirti darbo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="53f1e-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="53f1e-113">Galite matyti darbo užsakymo pastabas ir, jei reikia, įtraukti naujų pastabų sąraše pasirinkę darbo užsakymo užduotį ir spustelėję **Pastabos**.</span><span class="sxs-lookup"><span data-stu-id="53f1e-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="53f1e-114">Jei darbo užsakymui norite priskirti vieną priežiūros darbuotoją, sąraše pasirinkite darbo užsakymą ir spustelėkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="53f1e-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="53f1e-115">Bus atidarytas puslapis **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="53f1e-115">The **Work order** page opens.</span></span> <span data-ttu-id="53f1e-116">Spustelėkite **Išsiųsti**, kad suplanuotumėte darbo užsakymą konkrečiam priežiūros darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="53f1e-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="53f1e-117">Daugiau informacijos apie kelių darbo užsakymų arba vieno darbo užsakymo planavimą žr. [Darbo užsakymų planavimas](../work-order-scheduling/schedule-work-orders.md) ir [Darbo užsakymo išsiuntimas](../work-order-scheduling/dispatch-work-order.md).</span><span class="sxs-lookup"><span data-stu-id="53f1e-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="53f1e-118">Žemiau pateiktame paveikslėlyje parodytas puslapio **Suplanuotų darbo užsakymų priežiūros užduotys** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="53f1e-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![1 pav.](media/07-work-order-scheduling.png)

