---
title: Suplanuotų užsakymų tvirtinimas
description: Šioje temoje aprašomas suplanuotų užsakymų, palaikomų „Planning Optimization“, tvirtinimas.
author: ChristianRytt
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 6c215a89403f16336caae5c62cde6df469c4091c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825896"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="0744b-103">Suplanuotų užsakymų tvirtinimas</span><span class="sxs-lookup"><span data-stu-id="0744b-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0744b-104">Šioje temoje pateikiama informacija apie tai, kaip atnaujinti suplanuotų užsakymų būseną „Planning Optimization“.</span><span class="sxs-lookup"><span data-stu-id="0744b-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="0744b-105">Atkreipkite dėmesį, kad suplanuotų užsakymų tvirtinimas yra pasirinktinis veiksmas, skirtas sukurti patvirtintą suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0744b-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="0744b-106">Rekomenduojama patvirtinti modifikuotus suplanuotus užsakymus, kitu atveju pakeitimų bus nepaisoma ir jie bus perrašyti kito planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="0744b-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Suplanuoto užsakymo srautas](media/approved-planned-orders-1.png)

<span data-ttu-id="0744b-108">Laukas **Būsena** padeda sekti jūsų procesą naudojant toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0744b-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="0744b-109">**Neapdorota:** kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra *Neapdorota*.</span><span class="sxs-lookup"><span data-stu-id="0744b-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="0744b-110">Šios būsenos suplanuoti užsakymai bus panaikinti kito planavimo vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="0744b-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="0744b-111">**Baigta:** jei nusprendžiate netvirtinti suplanuoto užsakymo, galite pakeisti būseną į *Baigta*, kad nurodytumėte, jog baigėte šio suplanuoto užsakymo vertinimą.</span><span class="sxs-lookup"><span data-stu-id="0744b-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="0744b-112">Atkreipkite dėmesį, kad būsenas *Neapdorota* ir *Baigta* sistema valdo vienodai.</span><span class="sxs-lookup"><span data-stu-id="0744b-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="0744b-113">**Patvirtinta:** jei norite palikti pakeitimus arba planuojate tvirtinti suplanuotą užsakymą, pakeiskite būseną į *Patvirtinta*.</span><span class="sxs-lookup"><span data-stu-id="0744b-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="0744b-114">Suplanuoti užsakymai, kurių būsena yra *Patvirtinta*, laikomi fiksuotais ir numatyto tiekimo bendrojo planavimo metu, kad nebūtų modifikuojami ar panaikinami vėlesnių pagrindinio planavimo vykdymų metu.</span><span class="sxs-lookup"><span data-stu-id="0744b-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="0744b-115">Norint tai pasiekti, planavimo logika kopijuoja *patvirtintus* suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu.</span><span class="sxs-lookup"><span data-stu-id="0744b-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="0744b-116">Atkreipkite dėmesį, kad suplanuoti užsakymai, kurių būsena *Patvirtinta*, laikomi numatyto tiekimo tik konkrečiame pagrindiniame plane.</span><span class="sxs-lookup"><span data-stu-id="0744b-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="0744b-117">Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**.</span><span class="sxs-lookup"><span data-stu-id="0744b-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]