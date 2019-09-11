---
title: Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti
description: Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 478dd85abebf76dd264e93bcbe3f218a0ff0a5a8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916811"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="ffd13-103">Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti</span><span class="sxs-lookup"><span data-stu-id="ffd13-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffd13-104">Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="ffd13-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="ffd13-105">Tai atliekama naudojant pakankamų atsargų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="ffd13-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ffd13-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ffd13-107">Ši užduotis skirta gamybos planuotojui, kad būtų lengviau tvarkyti mažiausią padengimą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="ffd13-108">Kurti naują pakankamų atsargų žurnalo pavadinimą</span><span class="sxs-lookup"><span data-stu-id="ffd13-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="ffd13-109">**Naršymo srityje** eikite į **Pagrindinis planavimas > Sąranka > Pakankamų atsargų žurnalų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="ffd13-110">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-110">Click **New**.</span></span>
3. <span data-ttu-id="ffd13-111">Lauke **Pavadinimas** įveskite Medžiagos.</span><span class="sxs-lookup"><span data-stu-id="ffd13-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="ffd13-112">Lauke **Aprašas** įveskite Medžiagos.</span><span class="sxs-lookup"><span data-stu-id="ffd13-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="ffd13-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ffd13-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="ffd13-114">Kurti pakankamų atsargų žurnalą</span><span class="sxs-lookup"><span data-stu-id="ffd13-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="ffd13-115">**Naršymo srityje** eikite į **Pagrindinis planavimas > Pagrindinis planavimas > Vykdyti > Pakankamų atsargų skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="ffd13-116">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-116">Click **New**.</span></span>
3. <span data-ttu-id="ffd13-117">Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffd13-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="ffd13-118">Pasirinkite sukurto pakankamų atsargų žurnalo pavadinimą, pvz., Medžiagos.</span><span class="sxs-lookup"><span data-stu-id="ffd13-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="ffd13-119">Spustelėkite **Kurti eilutes**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="ffd13-120">Lauke **Pradžios data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="ffd13-121">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="ffd13-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-122">Click **OK**.</span></span> <span data-ttu-id="ffd13-123">Taip sukursite dimensijų, kuriose yra atsargų operacijų, eilutes.</span><span class="sxs-lookup"><span data-stu-id="ffd13-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="ffd13-124">Apskaičiuoti pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="ffd13-124">Calculate proposal</span></span>
1. <span data-ttu-id="ffd13-125">Spustelėkite **Apskaičiuoti pasiūlymą**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="ffd13-126">Pažymėkite parinktį **Naudoti išdavimo vidurkį per gamybos laiką**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="ffd13-127">Nustatykite **dauginimo koeficientą** 10.</span><span class="sxs-lookup"><span data-stu-id="ffd13-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="ffd13-128">Dauginimo koeficientas naudojamas pasiūlymui koreguoti.</span><span class="sxs-lookup"><span data-stu-id="ffd13-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="ffd13-129">Kadangi demonstraciniuose duomenyse yra tik kelios operacijos, turėsite nustatyti koeficientą, gautumėte realų pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="ffd13-130">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-130">Click **OK**.</span></span> <span data-ttu-id="ffd13-131">Slinkite žemyn ir raskite M0002 bei M0003.</span><span class="sxs-lookup"><span data-stu-id="ffd13-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="ffd13-132">Peržiūrėkite stulpelį **Apskaičiuotas mažiausias kiekis**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="ffd13-133">Naujinti mažiausią kiekį</span><span class="sxs-lookup"><span data-stu-id="ffd13-133">Update minimum quantity</span></span>
1. <span data-ttu-id="ffd13-134">Lauke **Naujas mažiausias kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ffd13-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="ffd13-135">Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffd13-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="ffd13-136">Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffd13-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="ffd13-137">Pavyzdžiui, šiame lauke galite įvesti M0002, kurio sandėlis yra 12-asis, apskaičiuotą mažiausią kiekį.</span><span class="sxs-lookup"><span data-stu-id="ffd13-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="ffd13-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="ffd13-139">Pavyzdžiui, galite pasirinkti M0002, kurio sandėlis yra 12-asis.</span><span class="sxs-lookup"><span data-stu-id="ffd13-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="ffd13-140">Lauke **Naujas mažiausias kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ffd13-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="ffd13-141">Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffd13-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="ffd13-142">Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffd13-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="ffd13-143">Registruoti naują mažiausią kiekį ir patikrinti rezultatą</span><span class="sxs-lookup"><span data-stu-id="ffd13-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="ffd13-144">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="ffd13-144">Click **Post**.</span></span>
2. <span data-ttu-id="ffd13-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-145">Click **OK**.</span></span>
3. <span data-ttu-id="ffd13-146">Lauke **Prekės numeris** spustelėkite saitą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="ffd13-147">Lauke **Prekės numeris** spustelėkite saitą.</span><span class="sxs-lookup"><span data-stu-id="ffd13-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="ffd13-148">**Veiksmų srityje** spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="ffd13-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="ffd13-149">Spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="ffd13-149">Click **Item coverage**.</span></span> <span data-ttu-id="ffd13-150">Atkreipkite dėmesį, kad **Mažiausiais kiekis** buvo atnaujintas pagal naują mažiausią kiekį pakankamų atsargų žurnale. </span><span class="sxs-lookup"><span data-stu-id="ffd13-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

