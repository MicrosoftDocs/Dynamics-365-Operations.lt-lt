---
title: "Laikotarpių skaidymas periodiniuose žurnaluose"
description: "Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73ccfc906e8d7a91e7bae5ae21d9ddad9d58f109
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="89a6c-105">Laikotarpių skaidymas periodiniuose žurnaluose</span><span class="sxs-lookup"><span data-stu-id="89a6c-105">Split periods in periodic journals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89a6c-106">Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas.</span><span class="sxs-lookup"><span data-stu-id="89a6c-106">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="89a6c-107">Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius.</span><span class="sxs-lookup"><span data-stu-id="89a6c-107">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="89a6c-108">Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="89a6c-108">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="89a6c-109">Norėdami pakartotinai nuskaityti ir registruoti operacijos eilutes, galite naudoti puslapį **Periodiniai žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="89a6c-109">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="89a6c-110">Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Latvijoje, Lietuvoje, Lenkijoje arba Rusijoje, į puslapį **Periodiniai žurnalai** įtraukiama laikotarpių skaidymo funkcija.</span><span class="sxs-lookup"><span data-stu-id="89a6c-110">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="89a6c-111">Daugiau informacijos ieškokite [Periodinio žurnalo registravimas](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="89a6c-111">For more information, see [Post a periodic journal](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="89a6c-112">Pavyzdys: laikotarpių skaidymas periodiniuose žurnaluose</span><span class="sxs-lookup"><span data-stu-id="89a6c-112">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="89a6c-113">Draudimo įmonė siūlo jūsų organizacijai nuolaidą už išankstinį draudimo strategijos apmokėjimą visiems metams.</span><span class="sxs-lookup"><span data-stu-id="89a6c-113">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="89a6c-114">Mokėjimas registruojamas į turto sąskaitą, pvz., iš anksto sumokėto draudimo.</span><span class="sxs-lookup"><span data-stu-id="89a6c-114">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="89a6c-115">Tada amortizuojate savo mėnesio draudimo išlaidas per metus sukurdami periodinį žurnalą, kuriame yra iš anksto apmokėtos draudimo sąskaitos kreditas ir draudimo išlaidų debetas.</span><span class="sxs-lookup"><span data-stu-id="89a6c-115">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="89a6c-116">Šiuo atveju galite naudoti laikotarpių skaidymo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="89a6c-116">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="89a6c-117">Puslapio **Periodinių žurnalų** **eilutės** veiksmų srityje spustelėkite mygtuką **Skaidyti laikotarpius**, o tada nurodykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="89a6c-117">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a6c-118">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="89a6c-118">**Field**</span></span>             | <span data-ttu-id="89a6c-119">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="89a6c-119">**Description**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="89a6c-120">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="89a6c-120">**Start date**</span></span>        | <span data-ttu-id="89a6c-121">Pasirinkite pirmosios periodinio žurnalo eilutės datą.</span><span class="sxs-lookup"><span data-stu-id="89a6c-121">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="89a6c-122">**Laikotarpių skaičius**</span><span class="sxs-lookup"><span data-stu-id="89a6c-122">**Number of periods**</span></span> | <span data-ttu-id="89a6c-123">Įveskite laikotarpių, per kuriuos padalinti žurnalo eilutes, skaičių.</span><span class="sxs-lookup"><span data-stu-id="89a6c-123">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="89a6c-124">Ši reikšmė nurodo, kiek naujų operacijų bus generuojama.</span><span class="sxs-lookup"><span data-stu-id="89a6c-124">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="89a6c-125">Operacijos suma paskirstoma tolygiai naujose operacijose.</span><span class="sxs-lookup"><span data-stu-id="89a6c-125">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="89a6c-126">**Vienetas**</span><span class="sxs-lookup"><span data-stu-id="89a6c-126">**Unit**</span></span>              | <span data-ttu-id="89a6c-127">Pasirinkite laikotarpio matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="89a6c-127">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="89a6c-128">**Laikotarpio intervalas**</span><span class="sxs-lookup"><span data-stu-id="89a6c-128">**Period interval**</span></span>   | <span data-ttu-id="89a6c-129">Nustatykite intervalą tarp registravimo laikotarpių.</span><span class="sxs-lookup"><span data-stu-id="89a6c-129">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="89a6c-130">Pvz., norėdami generuoti ketvirčio registravimus, įveskite **4** lauke **Laikotarpių skaičius**, lauke **Vienetas** pasirinkite **Mėnesiai** ir lauke **Laikotarpio intervalas** įveskite **3**.</span><span class="sxs-lookup"><span data-stu-id="89a6c-130">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="89a6c-131">Sistema sugeneruos keturias žurnalo eilutes, po vieną kiekvienam ketvirtadaliui visos įvestos žurnalo eilutės sumos, 3 mėnesių intervalais.</span><span class="sxs-lookup"><span data-stu-id="89a6c-131">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="89a6c-132">Panaši funkcija taip pat pateikiama bendrajame žurnale.</span><span class="sxs-lookup"><span data-stu-id="89a6c-132">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="89a6c-133">Peržiūrėdami bendrojo žurnalo eilutes, pasirinkite **Periodiniai žurnalai** &gt; **Įrašyti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="89a6c-133">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>




