---
title: Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti
description: Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "341102"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="68b01-103">Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti</span><span class="sxs-lookup"><span data-stu-id="68b01-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68b01-104">Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="68b01-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="68b01-105">Tai atliekama naudojant pakankamų atsargų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="68b01-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="68b01-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="68b01-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="68b01-107">Ši užduotis skirta gamybos planuotojui, kad būtų lengviau tvarkyti mažiausią padengimą.</span><span class="sxs-lookup"><span data-stu-id="68b01-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="68b01-108">Kurti naują pakankamų atsargų žurnalo pavadinimą</span><span class="sxs-lookup"><span data-stu-id="68b01-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="68b01-109">Pasirinkite Pakankamų atsargų žurnalų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="68b01-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="68b01-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="68b01-110">Click New.</span></span>
3. <span data-ttu-id="68b01-111">Lauke Pavadinimas įveskite „Medžiagos“.</span><span class="sxs-lookup"><span data-stu-id="68b01-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="68b01-112">Lauke Aprašas įveskite „Medžiagos“.</span><span class="sxs-lookup"><span data-stu-id="68b01-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="68b01-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="68b01-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="68b01-114">Kurti pakankamų atsargų žurnalą</span><span class="sxs-lookup"><span data-stu-id="68b01-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="68b01-115">Pasirinkite Pakankamų atsargų skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="68b01-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="68b01-116">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="68b01-116">Click New.</span></span>
3. <span data-ttu-id="68b01-117">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68b01-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="68b01-118">Pasirinkite sukurto pakankamų atsargų žurnalo pavadinimą, pvz., Medžiagos.</span><span class="sxs-lookup"><span data-stu-id="68b01-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="68b01-119">Spustelėkite Kurti eilutes.</span><span class="sxs-lookup"><span data-stu-id="68b01-119">Click Create lines.</span></span>
5. <span data-ttu-id="68b01-120">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="68b01-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="68b01-121">Nustatykite datą į „2015-01-02“.</span><span class="sxs-lookup"><span data-stu-id="68b01-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="68b01-122">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="68b01-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="68b01-123">Nustatykite datą į „2015-12-30“.</span><span class="sxs-lookup"><span data-stu-id="68b01-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="68b01-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="68b01-124">Click OK.</span></span>
    * <span data-ttu-id="68b01-125">Taip sukursite dimensijų, kuriose yra atsargų operacijų, eilutes.</span><span class="sxs-lookup"><span data-stu-id="68b01-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="68b01-126">Apskaičiuoti pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="68b01-126">Calculate proposal</span></span>
1. <span data-ttu-id="68b01-127">Spustelėkite Apskaičiuoti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="68b01-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="68b01-128">Pasirinkite parinktį Naudoti išdavimo vidurkį per gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="68b01-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="68b01-129">Nustatykite dauginimo koeficientą į 10.</span><span class="sxs-lookup"><span data-stu-id="68b01-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="68b01-130">Dauginimo koeficientas naudojamas pasiūlymui koreguoti.</span><span class="sxs-lookup"><span data-stu-id="68b01-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="68b01-131">Kadangi demonstraciniuose duomenyse yra tik kelios operacijos, turėsite nustatyti koeficientą, gautumėte realų pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="68b01-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="68b01-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="68b01-132">Click OK.</span></span>
    * <span data-ttu-id="68b01-133">Slinkite žemyn ir raskite M0002 bei M0003.</span><span class="sxs-lookup"><span data-stu-id="68b01-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="68b01-134">Peržiūrėkite stulpelį Apskaičiuotas mažiausias kiekis.</span><span class="sxs-lookup"><span data-stu-id="68b01-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="68b01-135">Naujinti mažiausią kiekį</span><span class="sxs-lookup"><span data-stu-id="68b01-135">Update minimum quantity</span></span>
1. <span data-ttu-id="68b01-136">Lauke Naujas mažiausias kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="68b01-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="68b01-137">Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68b01-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="68b01-138">Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68b01-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="68b01-139">Pavyzdžiui, šiame lauke galite įvesti M0002, kurio sandėlis yra 12-asis, apskaičiuotą mažiausią kiekį.</span><span class="sxs-lookup"><span data-stu-id="68b01-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="68b01-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="68b01-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="68b01-141">Pavyzdžiui, galite pasirinkti M0002, kurio sandėlis yra 12-asis.</span><span class="sxs-lookup"><span data-stu-id="68b01-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="68b01-142">Lauke Naujas mažiausias kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="68b01-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="68b01-143">Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68b01-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="68b01-144">Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="68b01-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="68b01-145">Registruoti naują mažiausią kiekį ir patikrinti rezultatą</span><span class="sxs-lookup"><span data-stu-id="68b01-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="68b01-146">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="68b01-146">Click Post.</span></span>
2. <span data-ttu-id="68b01-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="68b01-147">Click OK.</span></span>
3. <span data-ttu-id="68b01-148">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="68b01-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="68b01-149">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="68b01-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="68b01-150">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="68b01-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="68b01-151">Spustelėkite Prekės padengimas.</span><span class="sxs-lookup"><span data-stu-id="68b01-151">Click Item coverage.</span></span>
    * <span data-ttu-id="68b01-152">Atkreipkite dėmesį, kad mažiausias kiekis buvo atnaujintas, įvedus naują mažiausią kiekį iš pakankamų atsargų žurnalo.</span><span class="sxs-lookup"><span data-stu-id="68b01-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

