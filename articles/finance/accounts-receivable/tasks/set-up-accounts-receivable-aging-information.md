---
title: Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją
description: Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19b60d5fcfba995d08f12d0548f41a0c3d2781fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012091"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="fbc3c-103">Nustatyti ir generuoti gautinų sumų skirstymo pagal terminus informaciją</span><span class="sxs-lookup"><span data-stu-id="fbc3c-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbc3c-104">Šis vadovas jums padės nustatyti skirstymo pagal terminus laikotarpio apibrėžtį, pagal terminus skirstyti klientų balansus ir peržiūrėti balansus sąraše Pagal terminus suskirstytas balansas ir puslapyje Mokėjimų priežiūra.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="fbc3c-105">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="fbc3c-106">Kurti skirstymo pagal terminus laikotarpio apibrėžtį</span><span class="sxs-lookup"><span data-stu-id="fbc3c-106">Create an aging period definition</span></span>
1. <span data-ttu-id="fbc3c-107">Eikite į **naršymo sritį > Moduliai > Kreditas ir mokėjimai > Sąranka > Skirstymo pagal terminus laikotarpio apibrėžimai**.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="fbc3c-108">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-108">Click **New**.</span></span>
3. <span data-ttu-id="fbc3c-109">Lauke **Skirstymo pagal terminus laikotarpio apibrėžimai** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="fbc3c-110">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="fbc3c-111">Spustelėdami **Įtraukti po** įterpsite naują skirstymo pagal terminus laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="fbc3c-112">Lauke **Laikotarpis** įveskite aprašą, kuris bus rodomas skirstymo pagal terminus ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="fbc3c-113">Lauke **Vienetas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="fbc3c-114">Lauke **Intervalas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="fbc3c-115">DK laikotarpis suderina laikotarpį su DK kalendoriumi.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="fbc3c-116">Diena, savaite, mėnesiu, ketvirčiu ir metais pagal datos tipą apibrėžiamas intervalas.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="fbc3c-117">Parinktis Neribotas pasirenka visas operacijas prieš ankstesnį laikotarpį arba po jo – tai priklauso nuo to, ar tai pirmas, ar paskutinis laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="fbc3c-118">Lauke **Skirstymo pagal terminus indikatorius** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="fbc3c-119">Pasirinkite laikotarpį tinklelio viršuje.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="fbc3c-120">Atnaujinti aprašą, kad būtų apibūdintas seniausias skirstymo pagal terminus laikotarpio apibrėžties laikotarpis</span><span class="sxs-lookup"><span data-stu-id="fbc3c-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="fbc3c-121">Lauke **Laikotarpis** įveskite naują skirstymo pagal terminus laikotarpio aprašą.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="fbc3c-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="fbc3c-123">Balansus skirstyti pagal terminus</span><span class="sxs-lookup"><span data-stu-id="fbc3c-123">Age the balances</span></span>
1. <span data-ttu-id="fbc3c-124">Pasirinkite **Kreditas ir mokėjimai > Periodinės užduotys > Pagal terminus suskirstyti klientų balansus**.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="fbc3c-125">Lauke **Skirstymo pagal terminus laikotarpio apibrėžimas** pasirinkite savo sukurtą skirstymo pagal terminus laikotarpio apibrėžtį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="fbc3c-126">Kiekvienos skirstymo pagal terminus laikotarpio apibrėžties galite turėti vieną momentinę kopiją.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="fbc3c-127">Visi klientai apdorojami pagal numatytąsias nuostatas.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-127">All customers are processed by default.</span></span> <span data-ttu-id="fbc3c-128">Šią pasirinktį galite naudoti apskaičiuoti vienam klientų mokėjimų priežiūros telkiniui.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="fbc3c-129">Iš operacijos pasirinkite datą, kurią naudosite skirstydami pagal terminus.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="fbc3c-130">Skirstymo pagal terminus datą pasirinkite „nuo‟.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="fbc3c-131">Numatytoji data yra šiandienos, tačiau, šį lauką pakeitę į Pasirinkta data, galėsite pasirinkti norimą datą.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="fbc3c-132">Paketiniam vykdymui naudokite šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="fbc3c-133">Išplėskite **Įmonė** diapazoną.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-133">Expand the **Company** range.</span></span> <span data-ttu-id="fbc3c-134">Galite pasirinkti įmones, kurios bus įtrauktos į momentinę kopiją.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="fbc3c-135">Dabartinė įmonė pasirenkama pagal numatytąsias nuostatas.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="fbc3c-136">Norėdami apdoroti momentinę kopiją, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="fbc3c-137">Apdorojimas šiek tiek užtruks, tad palaukite, kol išnyks slankiklis ir patikrinkite, ar pranešimų centre nėra pranešimo.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="fbc3c-138">Peržiūrėti balansus sąraše Pagal terminus suskirstyti balansai ir puslapyje Rinkinys</span><span class="sxs-lookup"><span data-stu-id="fbc3c-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="fbc3c-139">Pasirinkite **Kreditas ir mokėjimai > Mokėjimų peržiūra > Suskirstyti pagal terminus balansai**.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="fbc3c-140">Sąrašo puslapyje rodomi kliento balansai.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="fbc3c-141">Skirstymo pagal terminus piktograma rodo seniausios operacijos skirstymo pagal terminus laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="fbc3c-142">Pasirinkite klientą, turintį balansą.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="fbc3c-143">Norėdami peržiūrėti pagal terminus suskirstytus balansus, išplėskite **Skirstymo pagal terminus faktas** sritį.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="fbc3c-144">„FactBox‟ skirstymo pagal terminus laikotarpio apibrėžtis paimama iš numatytosios skirstymo pagal terminus apibrėžties, nurodytos parametruose.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="fbc3c-145">Ją keisti galite naudodami meniu Rinkti.</span><span class="sxs-lookup"><span data-stu-id="fbc3c-145">You can change it using the Collect menu.</span></span>  

