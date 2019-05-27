---
title: Atidėjimai
description: Šioje temoje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1a8c738fffda76f2a8492c20e2c67a154c68559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1522294"
---
# <a name="delays"></a><span data-ttu-id="856f4-104">Atidėjimai</span><span class="sxs-lookup"><span data-stu-id="856f4-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="856f4-105">Šioje temoje pateikta informacija apie atidėtas bendrojo planavimo datas.</span><span class="sxs-lookup"><span data-stu-id="856f4-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="856f4-106">Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.</span><span class="sxs-lookup"><span data-stu-id="856f4-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="856f4-107">Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą.</span><span class="sxs-lookup"><span data-stu-id="856f4-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="856f4-108">Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku.</span><span class="sxs-lookup"><span data-stu-id="856f4-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="856f4-109">Todėl užsakymas atidedamas.</span><span class="sxs-lookup"><span data-stu-id="856f4-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="856f4-110">Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus.</span><span class="sxs-lookup"><span data-stu-id="856f4-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="856f4-111">Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų.</span><span class="sxs-lookup"><span data-stu-id="856f4-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="856f4-112">Tada užsakymui suteikiama atidėjimo data.</span><span class="sxs-lookup"><span data-stu-id="856f4-112">The order then receives a delayed date.</span></span> <span data-ttu-id="856f4-113">Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="856f4-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="856f4-114">Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="856f4-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="856f4-115">Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="856f4-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="856f4-116">Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai.</span><span class="sxs-lookup"><span data-stu-id="856f4-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="856f4-117">Vėliau prie prekės galite pridėti padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="856f4-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="856f4-118">Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką.</span><span class="sxs-lookup"><span data-stu-id="856f4-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="856f4-119">Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas.</span><span class="sxs-lookup"><span data-stu-id="856f4-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="856f4-120">Ankstesnėse versijose apskaičiuoti atidėjimai buvo vadinami *ateities pranešimais*, atidėjimo data buvo vadinama *ateities data*, o atidėta *operacija buvo vadinama į ateitį nustatyta operacija*.</span><span class="sxs-lookup"><span data-stu-id="856f4-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="856f4-121">Norima data</span><span class="sxs-lookup"><span data-stu-id="856f4-121">Desired date</span></span>

<span data-ttu-id="856f4-122">Puslapio **Suplanuotas užsakymas** skirtuke **Atidėjimai** nurodyta suplanuoto užsakymo **Norima data**.</span><span class="sxs-lookup"><span data-stu-id="856f4-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="856f4-123">Norima suplanuoto užsakymo data yra pagrindinė atidėjimų data – apskaičiuota data, lygi **pageidaujamai datai**, apskaičiuotai pagal **grynąjį poreikį**.</span><span class="sxs-lookup"><span data-stu-id="856f4-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="856f4-124">Jei suplanuotas užsakymas yra KS eilutė, gamybos eilutė arba „kanban“ eilutė, norima data nustatoma pagal **pageidaujamą datą** ir norima data nebus rodoma puslapyje **Suplanuotas užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="856f4-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="856f4-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="856f4-125">Additional resources</span></span>
--------

[<span data-ttu-id="856f4-126">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="856f4-126">Coverage settings</span></span>](coverage-settings.md)
