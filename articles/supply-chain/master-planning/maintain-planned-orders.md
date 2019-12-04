---
title: Suplanuotų užsakymų tvarkymas
description: Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus. Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bccb632255eac975dc150cf322d4c579ff2f24
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813781"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="b7a60-104">Suplanuotų užsakymų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="b7a60-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7a60-105">Šioje temoje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b7a60-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="b7a60-106">Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.</span><span class="sxs-lookup"><span data-stu-id="b7a60-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="b7a60-107">Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="b7a60-108">Suplanuoto užsakymo būsena</span><span class="sxs-lookup"><span data-stu-id="b7a60-108">Planned order status</span></span>
<span data-ttu-id="b7a60-109">Galite naudoti lauką **Būsena** progresui sekti.</span><span class="sxs-lookup"><span data-stu-id="b7a60-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="b7a60-110">Naudojamos toliau nurodytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="b7a60-110">The following values are used:</span></span>

-   <span data-ttu-id="b7a60-111">Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra **Neapdorota**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="b7a60-112">Jei nenorite patvirtinti suplanuoto užsakymo, galite jam nustatyti būseną **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="b7a60-113">Jei norite patvirtinti suplanuotą užsakymą, galite pakeisti būseną į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="b7a60-114">Suplanuoti užsakymai, kurių būsena yra **Patvirtinta**, neliečiami bendrojo planavimo metu, kad nebūtų modifikuojami ar panaikinami vėlesnio pagrindinio planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="b7a60-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="b7a60-115">Suplanuotų užsakymų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="b7a60-115">Firming planned orders</span></span> 
<span data-ttu-id="b7a60-116">Patvirtinant suplanuotus užsakymus, sukuriami realūs užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b7a60-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="b7a60-117">Jie taip pat vadinami *paskelbtais* arba *atvirais užsakymais*.</span><span class="sxs-lookup"><span data-stu-id="b7a60-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="b7a60-118">Kai suplanuotas užsakymas patvirtinamas, jis perkeliamas į atitinkamo modulio užsakymų dalį.</span><span class="sxs-lookup"><span data-stu-id="b7a60-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="b7a60-119">Galite pasirinkti dvi patvirtinimo parinktis iš puslapio **Suplanuoti užsakymai**:</span><span class="sxs-lookup"><span data-stu-id="b7a60-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="b7a60-120">**Patvirtinti** – patvirtinti vieną ar kelis pasirinktus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b7a60-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="b7a60-121">**Patvirtinti visus** – patvirtinti visus filtruojamus suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b7a60-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="b7a60-122">Naudojant **Patvirtinti visus**, jums nereikia pasirinkti suplanuoto užsakymo, nes visi filtruojami suplanuoti užsakymai bus patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="b7a60-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="b7a60-123">Ši pasirinktis gali būti naudinga, jei jūs norite patvirtinti daug suplanuotų užsakymų.</span><span class="sxs-lookup"><span data-stu-id="b7a60-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="b7a60-124">Galite sekti suplanuotą užsakymą, kuris buvo patvirtintas iš **Patvirtinimų retrospektyvos**, esančios **suplanuotų užsakymų formoje > Peržiūrėti > Patvirtinimų retrospektyva**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="b7a60-125">Sugretinti tvirtinimą</span><span class="sxs-lookup"><span data-stu-id="b7a60-125">Parallelize firming</span></span>
<span data-ttu-id="b7a60-126">Jeigu planuojate patvirtinti daug užsakymų tuo pačiu metu, lygiagretus vykdymas gali sutrumpinti apdorojimo laiką arba padidinti efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="b7a60-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="b7a60-127">Ši pasirinktis pasiekiama patvirtinant kelis suplanuotus užsakymus pasirinkus **Patvirtinti** arba **Patvirtinti visus**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="b7a60-128">Galimi tolesni parametrai.</span><span class="sxs-lookup"><span data-stu-id="b7a60-128">The following parameters are available:</span></span>

-   <span data-ttu-id="b7a60-129">**Lygiagretinti patvirtinimą** – jei reikšmė yra **Taip**, lygiagretinimo procesas bus atliekamas naudojant gijų skaičių, nurodytą **Gijų skaičius**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="b7a60-130">**Gijų skaičius** – kontroliuoja gijų skaičių, naudojamą patvirtinimo procesui lygiagretinti.</span><span class="sxs-lookup"><span data-stu-id="b7a60-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="b7a60-131">Parametras rodomas tik tada, kai nustatyta **Lygiagretinti patvirtinimą** reikšmė **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b7a60-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="b7a60-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b7a60-132">Additional resources</span></span>
--------

[<span data-ttu-id="b7a60-133">Bendrųjų planų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b7a60-133">Master plans overview</span></span>](master-plans.md)



