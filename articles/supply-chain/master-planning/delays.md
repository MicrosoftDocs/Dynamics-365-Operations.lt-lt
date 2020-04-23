---
title: Atidėjimai
description: Šioje temoje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.
author: roxanadiaconu
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34252e5cd9ee5151b1cba47975fc0cc612521a17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203853"
---
# <a name="delays"></a><span data-ttu-id="f2f9e-104">Atidėjimai</span><span class="sxs-lookup"><span data-stu-id="f2f9e-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2f9e-105">Šioje temoje pateikta informacija apie atidėtas bendrojo planavimo datas.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="f2f9e-106">Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="f2f9e-107">Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="f2f9e-108">Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="f2f9e-109">Todėl užsakymas atidedamas.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="f2f9e-110">Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="f2f9e-111">Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="f2f9e-112">Tada užsakymui suteikiama atidėjimo data.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-112">The order then receives a delayed date.</span></span> <span data-ttu-id="f2f9e-113">Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="f2f9e-114">Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="f2f9e-115">Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="f2f9e-116">Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="f2f9e-117">Vėliau prie prekės galite pridėti padengimo grupę.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="f2f9e-118">Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="f2f9e-119">Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="f2f9e-120">Ankstesnėse versijose apskaičiuoti atidėjimai buvo vadinami *ateities pranešimais*, atidėjimo data buvo vadinama *ateities data*, o atidėta *operacija buvo vadinama į ateitį nustatyta operacija*.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="f2f9e-121">Riboti vėlavimai gamybos sąrankoje, turinčioje kelis KS lygius</span><span class="sxs-lookup"><span data-stu-id="f2f9e-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="f2f9e-122">Kai dirbate su vėlavimais gamybos sąrankoje, turinčioje kelis KS lygius, svarbu atkreipti dėmesį, kad tik prekės, esančios tiesiai virš prekės (KS struktūroje), kurios sukelia vėlavimą, bus atnaujintos vėlavimu kaip bendrojo planavimo vykdymo dalis.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="f2f9e-123">Kitoms KS struktūros prekėms nebus taikomas vėlavimas iki pirmo bendrojo planavimo vykdymo, kai patvirtinamas aukščiausio lygio suplanuotas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="f2f9e-124">Norint apeiti šį žinomą apribojimą, prieš kitą bendrojo planavimo vykdymą KS struktūros viršuje esantys gamybos užsakymai su vėlavimais gali būti patvirtinami.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="f2f9e-125">Taip bus saugomas atidėto patvirtinto suplanuoto gamybos užsakymo vėlavimas ir atitinkamai atnaujinti visi esami komponentai.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="f2f9e-126">Veiksmo pranešimus taip pat galima naudoti norint nustatyti suplanuotus užsakymus, kuriuos galima perkelti į vėlesnę datą dėl kitų KS struktūros vėlavimų.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="f2f9e-127">Norima data</span><span class="sxs-lookup"><span data-stu-id="f2f9e-127">Desired date</span></span>

<span data-ttu-id="f2f9e-128">Puslapio **Suplanuotas užsakymas** skirtuke **Atidėjimai** nurodyta suplanuoto užsakymo **Norima data**.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="f2f9e-129">Norima suplanuoto užsakymo data yra pagrindinė atidėjimų data – apskaičiuota data, lygi **pageidaujamai datai**, apskaičiuotai pagal **grynąjį poreikį**.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="f2f9e-130">Jei suplanuotas užsakymas yra KS eilutė, gamybos eilutė arba „kanban“ eilutė, norima data nustatoma pagal **pageidaujamą datą** ir norima data nebus rodoma puslapyje **Suplanuotas užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="f2f9e-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f2f9e-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f2f9e-131">Additional resources</span></span>
--------

[<span data-ttu-id="f2f9e-132">Padengimo parametrai</span><span class="sxs-lookup"><span data-stu-id="f2f9e-132">Coverage settings</span></span>](coverage-settings.md)
