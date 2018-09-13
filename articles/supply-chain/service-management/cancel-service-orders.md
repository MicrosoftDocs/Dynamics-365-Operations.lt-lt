---
title: "Atšaukti aptarnavimo užsakymus"
description: "Galite atšaukti aptarnavimo užsakymą arba aptarnavimo užsakymo eilutę arba galite atšaukti kelis aptarnavimo užsakymus vykdydami periodinę užduotį."
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
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="df6cd-103">Atšaukti aptarnavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="df6cd-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="df6cd-104">Galite atšaukti aptarnavimo užsakymą arba aptarnavimo užsakymo eilutę arba galite atšaukti kelis aptarnavimo užsakymus vykdydami periodinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="df6cd-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="df6cd-105">Aptarnavimo užsakymai negali būti atšaukti, jei aptarnavimo užsakymo etapas neleidžia atšaukti, jei aptarnavimo užsakymas turi prekių poreikį arba jei aptarnavimo užsakymas jau užregistruotas.</span><span class="sxs-lookup"><span data-stu-id="df6cd-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="df6cd-106">Aptarnavimo užsakymų formoje esančių aptarnavimo užsakymų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="df6cd-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="df6cd-107">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="df6cd-108">Pasirinkite aptarnavimo užsakymą ir veiksmų srityje spustelėkite **Atšaukti užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="df6cd-109">Aptarnavimo užsakymo eilutės atšaukimas</span><span class="sxs-lookup"><span data-stu-id="df6cd-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="df6cd-110">Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="df6cd-111">Dukart spustelėkite aptarnavimo užsakymą, kuriame yra eilutė, kurią norite atšaukti.</span><span class="sxs-lookup"><span data-stu-id="df6cd-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="df6cd-112">Pasirinkite aptarnavimo užsakymo eilutę, kurią norite atšaukti, tada spustelėję **Atšaukti užsakymo eilutę** pakeisite eilutės būseną į **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="df6cd-113">Norėdami panaikinti aptarnavimo užsakymo eilutės atšaukimą ir pakeisti būseną atgal į <STRONG>Sukurta</STRONG>, spustelėkite <STRONG> anuliuoti atšaukimą</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="df6cd-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="df6cd-114">Kelių aptarnavimo užsakymų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="df6cd-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="df6cd-115">Spustelėkite **Aptarnavimo valdymas** \> **Periodinis** \> **Aptarnavimo užsakymai** \> **Atšaukti aptarnavimo užsakymus**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="df6cd-116">Spustelėkite mygtuką **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="df6cd-117">Formos **Užklausa** stulpelyje **Kriterijai** pasirinkite aptarnavimo užsakymus, kuriuos norite atšaukti.</span><span class="sxs-lookup"><span data-stu-id="df6cd-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="df6cd-118">Spustelėję **Gerai** uždarykite formą **Užklausa**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="df6cd-119">Pažymėkite žymės langelį **Rodyti sistemos pranešimą** norėdami sugeneruoti sistemos pranešimą, kuriame būtų nurodyti atšaukti aptarnavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="df6cd-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="df6cd-120">Pažymėkite žymės langelį **Anuliuoti atšaukimą**, jei norite panaikinti aptarnavimo užsakymo būseną **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="df6cd-121">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-121">Click **OK**.</span></span>

<span data-ttu-id="df6cd-122">Pasirinkti aptarnavimo užsakymai yra arba atšaukti, arba jų eigos būsena **Atšaukta** buvo pakeista į **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="df6cd-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="df6cd-123">Jei pažymėjote žymės langelį <STRONG>Anuliuoti atšaukimą</STRONG>, aptarnavimo užsakymai, kurių eigos būsena yra <STRONG>Atšaukta</STRONG>, yra pakeičiami ir jokie aptarnavimo užsakymų, kurių eigos būsena yra <STRONG>Vykdoma</STRONG>, atšaukimai nevykdomi.</span><span class="sxs-lookup"><span data-stu-id="df6cd-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  


