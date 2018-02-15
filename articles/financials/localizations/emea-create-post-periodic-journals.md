---
title: "Išskaidyti laikotarpiai periodiniuose žurnaluose"
description: "Šioje temoje pateikiama informacijos išskaidytus periodinių ar pasikartojančių žurnalų laikotarpius, kuriuos naudoja juridiniai subjektai Čekijoje, Estijoje, Latvijoje, Lenkijoje, Lietuvoje, Rusijoje ir Vengrijoje."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a523ff097eedf9a4a2cb0341b3be9d05abfa09fa
ms.openlocfilehash: 4fda7ad6405b00597eca354d5822f388e1ef164e
ms.contentlocale: lt-lt
ms.lasthandoff: 01/23/2018

---

# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="0d6df-103">Išskaidyti laikotarpiai periodiniuose žurnaluose</span><span class="sxs-lookup"><span data-stu-id="0d6df-103">Split periods in periodic journals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0d6df-104">Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas.</span><span class="sxs-lookup"><span data-stu-id="0d6df-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="0d6df-105">Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius.</span><span class="sxs-lookup"><span data-stu-id="0d6df-105">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="0d6df-106">Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d6df-106">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="0d6df-107">Norėdami pakartotinai nuskaityti ir registruoti operacijos eilutes, galite naudoti puslapį **Periodiniai žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="0d6df-107">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="0d6df-108">Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Latvijoje, Lietuvoje, Lenkijoje arba Rusijoje, į puslapį **Periodiniai žurnalai** įtraukiama laikotarpių skaidymo funkcija.</span><span class="sxs-lookup"><span data-stu-id="0d6df-108">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="0d6df-109">Daugiau informacijos ieškokite [Periodinio žurnalo registravimas](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="0d6df-109">For more information, see [Post a periodic journal](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="0d6df-110">Pavyzdys: laikotarpių skaidymas periodiniuose žurnaluose</span><span class="sxs-lookup"><span data-stu-id="0d6df-110">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="0d6df-111">Draudimo įmonė siūlo jūsų organizacijai nuolaidą už išankstinį draudimo strategijos apmokėjimą visiems metams.</span><span class="sxs-lookup"><span data-stu-id="0d6df-111">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="0d6df-112">Mokėjimas registruojamas į turto sąskaitą, pvz., iš anksto sumokėto draudimo.</span><span class="sxs-lookup"><span data-stu-id="0d6df-112">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="0d6df-113">Tada amortizuojate savo mėnesio draudimo išlaidas per metus sukurdami periodinį žurnalą, kuriame yra iš anksto apmokėtos draudimo sąskaitos kreditas ir draudimo išlaidų debetas.</span><span class="sxs-lookup"><span data-stu-id="0d6df-113">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="0d6df-114">Šiuo atveju galite naudoti laikotarpių skaidymo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="0d6df-114">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="0d6df-115">Puslapio **Periodinių žurnalų** **eilutės** veiksmų srityje spustelėkite mygtuką **Skaidyti laikotarpius**, o tada nurodykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="0d6df-115">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6df-116">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="0d6df-116">**Field**</span></span>             | <span data-ttu-id="0d6df-117">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="0d6df-117">**Description**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="0d6df-118">**Pradžios data**</span><span class="sxs-lookup"><span data-stu-id="0d6df-118">**Start date**</span></span>        | <span data-ttu-id="0d6df-119">Pasirinkite pirmosios periodinio žurnalo eilutės datą.</span><span class="sxs-lookup"><span data-stu-id="0d6df-119">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="0d6df-120">**Laikotarpių skaičius**</span><span class="sxs-lookup"><span data-stu-id="0d6df-120">**Number of periods**</span></span> | <span data-ttu-id="0d6df-121">Įveskite laikotarpių, per kuriuos padalinti žurnalo eilutes, skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d6df-121">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="0d6df-122">Ši reikšmė nurodo, kiek naujų operacijų bus generuojama.</span><span class="sxs-lookup"><span data-stu-id="0d6df-122">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="0d6df-123">Operacijos suma paskirstoma tolygiai naujose operacijose.</span><span class="sxs-lookup"><span data-stu-id="0d6df-123">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="0d6df-124">**Vienetas**</span><span class="sxs-lookup"><span data-stu-id="0d6df-124">**Unit**</span></span>              | <span data-ttu-id="0d6df-125">Pasirinkite laikotarpio matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="0d6df-125">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="0d6df-126">**Laikotarpio intervalas**</span><span class="sxs-lookup"><span data-stu-id="0d6df-126">**Period interval**</span></span>   | <span data-ttu-id="0d6df-127">Nustatykite intervalą tarp registravimo laikotarpių.</span><span class="sxs-lookup"><span data-stu-id="0d6df-127">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="0d6df-128">Pvz., norėdami generuoti ketvirčio registravimus, įveskite **4** lauke **Laikotarpių skaičius**, lauke **Vienetas** pasirinkite **Mėnesiai** ir lauke **Laikotarpio intervalas** įveskite **3**.</span><span class="sxs-lookup"><span data-stu-id="0d6df-128">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="0d6df-129">Sistema sugeneruos keturias žurnalo eilutes, po vieną kiekvienam ketvirtadaliui visos įvestos žurnalo eilutės sumos, 3 mėnesių intervalais.</span><span class="sxs-lookup"><span data-stu-id="0d6df-129">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="0d6df-130">Panaši funkcija taip pat pateikiama bendrajame žurnale.</span><span class="sxs-lookup"><span data-stu-id="0d6df-130">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="0d6df-131">Peržiūrėdami bendrojo žurnalo eilutes, pasirinkite **Periodiniai žurnalai** &gt; **Įrašyti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="0d6df-131">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>




