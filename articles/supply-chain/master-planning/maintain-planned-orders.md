---
title: Suplanuotų užsakymų tvarkymas
description: Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus. Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0becf73ddde6add4076bd5b47a49eb3a0976206
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886901"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="dde49-104">Suplanuotų užsakymų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="dde49-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dde49-105">Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="dde49-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="dde49-106">Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.</span><span class="sxs-lookup"><span data-stu-id="dde49-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="dde49-107">Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="dde49-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="dde49-108">Suplanuoto užsakymo būsena</span><span class="sxs-lookup"><span data-stu-id="dde49-108">Planned order status</span></span>
<span data-ttu-id="dde49-109">Galite naudoti lauką **Būsena** progresui sekti.</span><span class="sxs-lookup"><span data-stu-id="dde49-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="dde49-110">Naudojamos toliau nurodytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="dde49-110">The following values are used:</span></span>

-   <span data-ttu-id="dde49-111">Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra **Neapdorota**.</span><span class="sxs-lookup"><span data-stu-id="dde49-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="dde49-112">Jei nenorite patvirtinti suplanuoto užsakymo, galite jam nustatyti būseną **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="dde49-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="dde49-113">Jei norite patvirtinti suplanuotą užsakymą, galite pakeisti būseną į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="dde49-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="dde49-114">Suplanuoti užsakymai, kurių būsena yra **Patvirtinta**, neliečiami bendrojo planavimo metu, kad nebūtų modifikuojami ar panaikinami vėlesnio pagrindinio planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="dde49-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="dde49-115">Norint tai pasiekti, planavimo logika kopijuoja **patvirtintus** suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="dde49-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="dde49-116">Suplanuotų užsakymų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="dde49-116">Firming planned orders</span></span> 
<span data-ttu-id="dde49-117">Patvirtinant suplanuotus užsakymus, sukuriami realūs užsakymai.</span><span class="sxs-lookup"><span data-stu-id="dde49-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="dde49-118">Jie taip pat vadinami *pateiktais* arba *atvirais užsakymais*.</span><span class="sxs-lookup"><span data-stu-id="dde49-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="dde49-119">Kai suplanuotas užsakymas patvirtinamas, jis perkeliamas į atitinkamo modulio užsakymų dalį.</span><span class="sxs-lookup"><span data-stu-id="dde49-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="dde49-120">Galite pasirinkti dvi patvirtinimo parinktis iš puslapio **Suplanuoti užsakymai**:</span><span class="sxs-lookup"><span data-stu-id="dde49-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="dde49-121">**Patvirtinti** – patvirtinti vieną ar kelis pasirinktus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="dde49-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="dde49-122">**Patvirtinti visus** – patvirtinti visus filtruojamus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="dde49-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="dde49-123">Naudojant **Patvirtinti visus**, jums nereikia pasirinkti suplanuoto užsakymo, nes visi filtruojami suplanuoti užsakymai bus patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="dde49-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="dde49-124">Ši pasirinktis gali būti naudinga, jei jūs norite patvirtinti daug suplanuotų užsakymų.</span><span class="sxs-lookup"><span data-stu-id="dde49-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="dde49-125">Galite sekti suplanuotą užsakymą, kuris buvo patvirtintas iš **Patvirtinimų retrospektyvos**, esančios **suplanuotų užsakymų formoje > Peržiūrėti > Patvirtinimų retrospektyva**.</span><span class="sxs-lookup"><span data-stu-id="dde49-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="dde49-126">Sugretinti tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="dde49-126">Parallelize firming</span></span>
<span data-ttu-id="dde49-127">Jeigu planuojate patvirtinti daug užsakymų tuo pačiu metu, lygiagretus vykdymas gali sutrumpinti apdorojimo laiką arba padidinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="dde49-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="dde49-128">Ši pasirinktis pasiekiama patvirtinant kelis suplanuotus užsakymus pasirinkus **Patvirtinti** arba **Patvirtinti visus**.</span><span class="sxs-lookup"><span data-stu-id="dde49-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="dde49-129">Galimi tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="dde49-129">The following parameters are available:</span></span>

-   <span data-ttu-id="dde49-130">**Lygiagretinti patvirtinimą** – jei reikšmė yra **Taip**, lygiagretinimo procesas bus atliekamas naudojant gijų skaičių, nurodytą **Gijų skaičius**.</span><span class="sxs-lookup"><span data-stu-id="dde49-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="dde49-131">**Gijų skaičius** – kontroliuoja gijų skaičių, naudojamą patvirtinimo procesui lygiagretinti.</span><span class="sxs-lookup"><span data-stu-id="dde49-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="dde49-132">Parametras rodomas tik tada, kai nustatyta **Lygiagretinti patvirtinimą** reikšmė **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dde49-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="dde49-133">Parinktis **Lygiagretinti patvirtinimą** rodoma tik tada, kai turite daugiau nei vieną suplanuotą užsakymą, kurį pasirinkote patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="dde49-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="dde49-134">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dde49-134">Additional resources</span></span>
--------

[<span data-ttu-id="dde49-135">Bendrųjų planų apžvalga</span><span class="sxs-lookup"><span data-stu-id="dde49-135">Master plans overview</span></span>](master-plans.md)



