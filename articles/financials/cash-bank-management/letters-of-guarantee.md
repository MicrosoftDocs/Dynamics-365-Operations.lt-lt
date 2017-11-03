---
title: "Garantiniai raštai"
description: "Šiame straipsnyje pateikiama informacija apie garantinius raštus. Garantiniame rašte bankas sutinka mokėti tam tikrą pinigų sumą asmeniui, jei vienas iš banko klientų laiku nesumokės arba neįvykdys įsipareigojimo tam asmeniui."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c3d61bbfdd6a304a7bd2edd81e51e556a4955dce
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="letters-of-guarantee"></a><span data-ttu-id="aab6c-104">Garantiniai raštai</span><span class="sxs-lookup"><span data-stu-id="aab6c-104">Letters of guarantee</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aab6c-105">Šiame straipsnyje pateikiama informacija apie garantinius raštus.</span><span class="sxs-lookup"><span data-stu-id="aab6c-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="aab6c-106">Garantiniame rašte bankas sutinka mokėti tam tikrą pinigų sumą asmeniui, jei vienas iš banko klientų laiku nesumokės arba neįvykdys įsipareigojimo tam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="aab6c-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="aab6c-107">Garantinis raštas yra banko (laiduotojo) sutikimas sumokėti nustatytą sumą pinigų konkrečiam asmeniui (gavėjui), jei banko klientas (vykdytojas) laiku nesumokės arba neįvykdys įsipareigojimo gavėjui.</span><span class="sxs-lookup"><span data-stu-id="aab6c-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="aab6c-108">Garantiniai raštai nėra perduodami.</span><span class="sxs-lookup"><span data-stu-id="aab6c-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="aab6c-109">Jie galioja tik gavėjui, kuris įvardijamas sutartyje.</span><span class="sxs-lookup"><span data-stu-id="aab6c-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="aab6c-110">Vykdytojas gali prašyti padidinti arba sumažinti garantinio rašto vertę, priklausomai nuo sutarties sąlygų.</span><span class="sxs-lookup"><span data-stu-id="aab6c-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="aab6c-111">Norėdamas likviduoti garantinį raštą, gavėjas privalo pateikti originalų garantinį raštą ir informuoti banką apie įgaliotojo įsipareigojimų nevykdymą prieš galiojimo pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="aab6c-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="aab6c-112">Tada bankas sumoka reikiamą sumą, kuri turi būti sumokėta į gavėjo sąskaitą, kaip sutarta garantiniame rašte.</span><span class="sxs-lookup"><span data-stu-id="aab6c-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="aab6c-113">Bankas pasilieka tam tikrą procentą nuo mokėjimo kaip maržą.</span><span class="sxs-lookup"><span data-stu-id="aab6c-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="aab6c-114">Dėl šio procento sutariama ir jis nurodomas sutarties sąlygose.</span><span class="sxs-lookup"><span data-stu-id="aab6c-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="aab6c-115">Galite sukurti kodą, kurį priskirtumėte garantinio rašto paskirčiai.</span><span class="sxs-lookup"><span data-stu-id="aab6c-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="aab6c-116">Taip pat galite nurodyti priežastis, kurios gali būti siejamos su garantinio rašto atšaukimu.</span><span class="sxs-lookup"><span data-stu-id="aab6c-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="aab6c-117">Galite peržiūrėti paskirties kodus ir banko priežastis puslapiuose **Mokėjimo paskirties kodai** ir **Banko priežastys**.</span><span class="sxs-lookup"><span data-stu-id="aab6c-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="aab6c-118">Galite naudoti puslapį **Garantinis raštas**, kad atliktumėte šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="aab6c-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="aab6c-119">Sukurkite teisingus DK įrašus ir išvenkite įvedimo rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="aab6c-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="aab6c-120">Fiksuokite visas pinigines ir nepinigines operacijas bei sekite garantinių raštų balansus.</span><span class="sxs-lookup"><span data-stu-id="aab6c-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="aab6c-121">Fiksuokite ir sekite garantinių raštų būseną ir galiojimo terminą.</span><span class="sxs-lookup"><span data-stu-id="aab6c-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="aab6c-122">Generuokite ataskaitą, kurioje būtų pateikiami bankai, turintys garantinius raštus.</span><span class="sxs-lookup"><span data-stu-id="aab6c-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="aab6c-123">Toliau pateikiamoje lentelėje aprašomi veiksmai, kuriuos galite atlikti su garantiniu raštu.</span><span class="sxs-lookup"><span data-stu-id="aab6c-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="aab6c-124">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="aab6c-124">Action</span></span>              | <span data-ttu-id="aab6c-125">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="aab6c-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab6c-126">Pateikti bankui</span><span class="sxs-lookup"><span data-stu-id="aab6c-126">Submit to bank</span></span>      | <span data-ttu-id="aab6c-127">Pateikti prašymą bankui išduoti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="aab6c-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="aab6c-128">Gauti iš banko</span><span class="sxs-lookup"><span data-stu-id="aab6c-128">Receive from bank</span></span>   | <span data-ttu-id="aab6c-129">Kai bankas sutinka su pateiktu prašymu, paimti iš banko garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="aab6c-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="aab6c-130">Duoti gavėjui</span><span class="sxs-lookup"><span data-stu-id="aab6c-130">Give to beneficiary</span></span> | <span data-ttu-id="aab6c-131">Kai gaunate iš banko garantinį raštą, pateikti garantinį raštą gavėjui.</span><span class="sxs-lookup"><span data-stu-id="aab6c-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="aab6c-132">Padidinti reikšmę</span><span class="sxs-lookup"><span data-stu-id="aab6c-132">Increase value</span></span>      | <span data-ttu-id="aab6c-133">Jei gavėjas ir vykdytojas sutinka, padidinti piniginę vertę.</span><span class="sxs-lookup"><span data-stu-id="aab6c-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="aab6c-134">Sumažinti reikšmę</span><span class="sxs-lookup"><span data-stu-id="aab6c-134">Decrease value</span></span>      | <span data-ttu-id="aab6c-135">Jei gavėjas ir vykdytojas sutinka, sumažinti piniginę vertę.</span><span class="sxs-lookup"><span data-stu-id="aab6c-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="aab6c-136">Išplėsti</span><span class="sxs-lookup"><span data-stu-id="aab6c-136">Extend</span></span>              | <span data-ttu-id="aab6c-137">Kai pateikiate garantinį raštą gavėjui, pratęsti galiojimo laiką, jei to reikia.</span><span class="sxs-lookup"><span data-stu-id="aab6c-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="aab6c-138">Atšaukti</span><span class="sxs-lookup"><span data-stu-id="aab6c-138">Cancel</span></span>              | <span data-ttu-id="aab6c-139">Jei priežasties, dėl kurios buvo prašyta garantinio rašto, nebėra – atšaukti sutartį.</span><span class="sxs-lookup"><span data-stu-id="aab6c-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="aab6c-140">Likviduoti</span><span class="sxs-lookup"><span data-stu-id="aab6c-140">Liquidate</span></span>           | <span data-ttu-id="aab6c-141">Kai gavėjas pateikia garantinį raštą bankui, iškeisti garantinį raštą į grynuosius pinigus.</span><span class="sxs-lookup"><span data-stu-id="aab6c-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="aab6c-142">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="aab6c-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="aab6c-143">Garantinio rašto operacija</span><span class="sxs-lookup"><span data-stu-id="aab6c-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="aab6c-144">Nustatyti garantinio rašto banko priemones ir registravimo šablonus</span><span class="sxs-lookup"><span data-stu-id="aab6c-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)



