---
title: "Atidėjimai"
description: "Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="delays"></a><span data-ttu-id="b0d97-104">Atidėjimai</span><span class="sxs-lookup"><span data-stu-id="b0d97-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b0d97-105">Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas.</span><span class="sxs-lookup"><span data-stu-id="b0d97-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="b0d97-106">Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.</span><span class="sxs-lookup"><span data-stu-id="b0d97-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="b0d97-107">Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą.</span><span class="sxs-lookup"><span data-stu-id="b0d97-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="b0d97-108">Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku.</span><span class="sxs-lookup"><span data-stu-id="b0d97-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="b0d97-109">Todėl užsakymas atidedamas.</span><span class="sxs-lookup"><span data-stu-id="b0d97-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="b0d97-110">Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus.</span><span class="sxs-lookup"><span data-stu-id="b0d97-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="b0d97-111">Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų.</span><span class="sxs-lookup"><span data-stu-id="b0d97-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="b0d97-112">Tada užsakymui suteikiama atidėjimo data.</span><span class="sxs-lookup"><span data-stu-id="b0d97-112">The order then receives a delayed date.</span></span> <span data-ttu-id="b0d97-113">Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="b0d97-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="b0d97-114">Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="b0d97-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="b0d97-115">Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="b0d97-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="b0d97-116">Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai.</span><span class="sxs-lookup"><span data-stu-id="b0d97-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="b0d97-117">Vėliau prie prekės galite pridėti padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="b0d97-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="b0d97-118">Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką.</span><span class="sxs-lookup"><span data-stu-id="b0d97-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="b0d97-119">Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas.</span><span class="sxs-lookup"><span data-stu-id="b0d97-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="b0d97-120">**Pastaba:** ankstesnėse versijose apskaičiuoti atidėjimai buvo žinomi kaip *ateities pranešimai*, atidėjimo data buvo žinoma kaip *ateities data*, o atidėta operacija buvo vadinama *į ateitį nustatyta operacija*.</span><span class="sxs-lookup"><span data-stu-id="b0d97-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="b0d97-121">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b0d97-121">See also</span></span>
--------

[<span data-ttu-id="b0d97-122">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="b0d97-122">Coverage settings</span></span>](coverage-settings.md)



