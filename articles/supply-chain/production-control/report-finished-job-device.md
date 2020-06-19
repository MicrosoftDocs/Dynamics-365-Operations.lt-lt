---
title: Pranešti kaip baigtą iš užduoties kortelės įrenginio
description: Šioje temoje aprašoma, kaip konfigūruoti sistemą, kad užduočių kortelės įrenginio vartotojai galėtų pranešti apie gatavus produktus iš gamybos užsakymo į atsargas.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403267"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="c74c7-103">Pranešti kaip baigtą iš užduoties kortelės įrenginio</span><span class="sxs-lookup"><span data-stu-id="c74c7-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c74c7-104">Darbuotojai naudoja **Progreso ataskaita** užduoties kortelės įrenginio ataskaitos puslapį, kad galėtų pranešti apie gamybos užduočiai baigtus kiekius.</span><span class="sxs-lookup"><span data-stu-id="c74c7-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="c74c7-105">Kontroliuokite, ar kiekiai, kurie pranešami baigtais, įtraukiami į atsargas</span><span class="sxs-lookup"><span data-stu-id="c74c7-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="c74c7-106">Norėdami kontroliuoti, ar ir kaip kiekiai, pateikti baigtais paskutinėje operacijoje, turi būti pridėti į atsargas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c74c7-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="c74c7-107">Eikite į **Produkto kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos užsakymo numatytieji nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="c74c7-108">Skirtuke **Pranešti kaip baigta** nustatykite **Atnaujinti baigtą ataskaitą prisijungus** lauką pagal vieną iš šių verčių:</span><span class="sxs-lookup"><span data-stu-id="c74c7-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="c74c7-109">**Ne** – joks kiekis nebus pridėtas į atsargas, kai pranešama apie paskutinės operacijos kiekius.</span><span class="sxs-lookup"><span data-stu-id="c74c7-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="c74c7-110">Gamybos užsakymo būsena niekada nesikeičia.</span><span class="sxs-lookup"><span data-stu-id="c74c7-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="c74c7-111">**Būsena + Kiekis** – gamybos užsakymo būsena pasikeis į *Pranešti kaip baigta*, o kiekis bus praneštas baigtu į atsargas.</span><span class="sxs-lookup"><span data-stu-id="c74c7-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="c74c7-112">**Kiekis** – kiekis pranešamas kaip baigtas į atsargas, bet gamybos užsakymo būsena niekada nepasikeis.</span><span class="sxs-lookup"><span data-stu-id="c74c7-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="c74c7-113">**Būsena** – tik gamybos užsakymo būsena pasikeis.</span><span class="sxs-lookup"><span data-stu-id="c74c7-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="c74c7-114">Joks kiekis nebus pridėtas į atsargas , kai apie kiekius pranešama paskutinės operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="c74c7-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="c74c7-115">Kiekiai nėra stebimi atsargose, jei operacijos, kuriose pranešti baigti, nėra nustatyta kaip paskutinė operacija.</span><span class="sxs-lookup"><span data-stu-id="c74c7-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="c74c7-116">Tačiau šie kiekiai gali būti naudojami peržiūrėti eigą.</span><span class="sxs-lookup"><span data-stu-id="c74c7-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="c74c7-117">Jie taip pat gali būti įtraukti į taisykles, kontroliuojančias, ar darbuotojai gali pradėti kitą operaciją prieš pasiekus pranešamų kiekių nustatytą ribą ankstesnės operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="c74c7-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="c74c7-118">Galite nustatyti šias taisykles **Kiekio tikrinimas** skirtuke, esančiame **Gamybos užsakymo numatytieji nustatymai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c74c7-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="c74c7-119">Daugiau informacijos apie tai, kaip naudoti **Gamybos užsakymo numatytieji nustatymai** puslapį, žr. [Gamybos parametrų gamyboje vykdymas](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="c74c7-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="c74c7-120">Paketo kontroliuojamų prekių kaip baigta pranešimas</span><span class="sxs-lookup"><span data-stu-id="c74c7-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="c74c7-121">Užduoties kortelės įrenginys palaiko tris paketo elementų ataskaitų scenarijus.</span><span class="sxs-lookup"><span data-stu-id="c74c7-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="c74c7-122">Šie scenarijai taikomi tiek prekėms, apdorojamoms pažangių sandėliavimo procesų metu, tiek prekėms, neapdorojamoms pažangių sandėliavimo procesų metu.</span><span class="sxs-lookup"><span data-stu-id="c74c7-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="c74c7-123">**Rankiniu būdu priskirti paketo numeriai:** darbuotojai įveda pasirinktinį paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="c74c7-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="c74c7-124">Šis paketo numeris gali atsirasti iš išorinio šaltinio, kuris nežinomas sistemai.</span><span class="sxs-lookup"><span data-stu-id="c74c7-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="c74c7-125">**Iš anksto nustatyti paketo numeriai:** darbuotojai pasirenka paketo numerių sąraše esantį paketo numerį, kurį sistema automatiškai sugeneruoja prieš paleidžiant gamybos užsakymą į užduočių kortelės įrenginį.</span><span class="sxs-lookup"><span data-stu-id="c74c7-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="c74c7-126">**Fiksuoti paketo numeriai:** darbuotojai neįveda ar nesitenka paketo numerio.</span><span class="sxs-lookup"><span data-stu-id="c74c7-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="c74c7-127">Vietoj to, sistema automatiškai priskiria gamybos užsakymo paketo numerį prieš jį išleidžiant.</span><span class="sxs-lookup"><span data-stu-id="c74c7-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="c74c7-128">Norėdami įjungti scenarijų, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c74c7-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="c74c7-129">Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c74c7-130">Pasirinkite konfigūruotiną produktą.</span><span class="sxs-lookup"><span data-stu-id="c74c7-130">Select the product to configure.</span></span>
1. <span data-ttu-id="c74c7-131">**Tvarkyti atsargas** „FastTab” **Paketo numerio grupė** lauke pasirinkite sekimo numerio grupę, kuri nustatyta palaikyti jūsų scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c74c7-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="c74c7-132">Pagal numatytuosius nustatymus, jeigu paketo numerio grupė nepriskirta paketo valdomam produktui, užduoties kortelės įrenginys suteikia rankinį paketo numerio įvedimą, kai pranešama, kad baigta.</span><span class="sxs-lookup"><span data-stu-id="c74c7-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="c74c7-133">Toliau esančiuose poskyriuose aprašoma, kaip nustatyti sekimo numerių grupes, kad būtų palaikomas kiekvienas iš trijų paketo elementų ataskaitų scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c74c7-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="c74c7-134">Įjunkite paketo numerio ataskaitą užduoties kortelės įrenginyje</span><span class="sxs-lookup"><span data-stu-id="c74c7-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="c74c7-135">Norėdami įjungti savo užduoties kortelės įrenginius, kad būtų galima priimti paketo numerį ataskaitos metu, kad baigta, turite naudoti [funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte šias funkcijas (šia tvarka):</span><span class="sxs-lookup"><span data-stu-id="c74c7-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="c74c7-136">Patobulinta Ataskaitos eigos dialogo lango vartotojo patirtis Užduoties kortelės įrenginyje</span><span class="sxs-lookup"><span data-stu-id="c74c7-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="c74c7-137">Įjunkite, kad galėtumėte įvesti paketo ir serijos numerius, kai pranešate apie baigimą Užduoties kortelės įrenginiu (peržiūra)</span><span class="sxs-lookup"><span data-stu-id="c74c7-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="c74c7-138">Nustatykite sekimo numerių grupę, kuri leidžia darbuotojams neautomatiniu būdu priskirti paketo numerį</span><span class="sxs-lookup"><span data-stu-id="c74c7-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="c74c7-139">Norėdami leisti rankiniu būdu nustatyti paketo numerius, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c74c7-140">Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c74c7-141">Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.</span><span class="sxs-lookup"><span data-stu-id="c74c7-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c74c7-142">**Bendra** skirtuke „FastTab” nustatykite **Rankinis** pasirinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="c74c7-143">![Sekimo numerių grupių puslapis](media/tracking-number-group-manual.png "Sekimo numerių grupių puslapis")</span><span class="sxs-lookup"><span data-stu-id="c74c7-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="c74c7-144">Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c74c7-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c74c7-145">Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra teksto laukas, kuriame darbuotojai gali įvesti bet kokią vertę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="c74c7-146">![Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas](media/job-card-device-batch-manual.png "Ataskaitos eigos puslapis, kuriame yra rankinio paketo numerių laukas")</span><span class="sxs-lookup"><span data-stu-id="c74c7-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="c74c7-147">Nustatykite sekimo numerių grupę, kuri pateikia iš anksto nustatytų paketų numerių sąrašą</span><span class="sxs-lookup"><span data-stu-id="c74c7-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="c74c7-148">Norėdami pateikti iš anksto nustatytų paketo numerių sąrašą, atlikite šiuos veiksmus, kad nustatytumėte sekimo numerių grupę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c74c7-149">Eikite į **Atsargų valdymas \> Sąranka > Dimensijos \> Sekimo numerių grupės**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c74c7-150">Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.</span><span class="sxs-lookup"><span data-stu-id="c74c7-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c74c7-151">**Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="c74c7-152">Naudokite **Už vnt.** lauką, kad perskirtumėte paketo numerius už kiekį, atsižvelgdami į jūsų įvestą vertę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="c74c7-153">Pavyzdžiui, turite gamybos užsakymo dešimt vienetų, o **Už vnt.** laukas nustatytas į *2*.</span><span class="sxs-lookup"><span data-stu-id="c74c7-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="c74c7-154">Šiuo atveju, sukurti penki paketo numerius bus priskirti gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="c74c7-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="c74c7-155">![Sekimo numerių grupių puslapis](media/tracking-number-group-predefined.png "Sekimo numerių grupių puslapis")</span><span class="sxs-lookup"><span data-stu-id="c74c7-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="c74c7-156">Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c74c7-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c74c7-157">Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, yra išsiskleidžiantis dialogo sąrašas, kuriame darbuotojai turi įvesti iš anksto nustatytą vertę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="c74c7-158">![Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas](media/job-card-device-batch-predefined.png "Ataskaitos eigos puslapi su iš anksto nustatytų paketo numerių laukas")</span><span class="sxs-lookup"><span data-stu-id="c74c7-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="c74c7-159">Nustatykite sekimo numerių grupę, kuri leidžia automatiškai priskirti paketo numerius</span><span class="sxs-lookup"><span data-stu-id="c74c7-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="c74c7-160">Jei paketo numeriai turi būti automatiškai priskirti, be darbuotojo įvesties, atlikite šiuos veiksmus, norėdami nustatyti sekimo numerių grupę.</span><span class="sxs-lookup"><span data-stu-id="c74c7-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c74c7-161">Eikite į **Atsargų valdymas \>Nustatymas \>Dimensijos \>Sekimo numerių grupes**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c74c7-162">Sukurkite arba pasirinkite sekimo numerių grupę, kurią norite nustatyti.</span><span class="sxs-lookup"><span data-stu-id="c74c7-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c74c7-163">**Bendra** skirtuke „FastTab” nustatykite **Tik atsargų operacijos** pasirinktį į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="c74c7-164">Nustatykite **Rankinis** pasirinktis **Nr.**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="c74c7-165">![Sekimo numerių grupių puslapis](media/tracking-number-group-fixed.png "Sekimo numerių grupių puslapis")</span><span class="sxs-lookup"><span data-stu-id="c74c7-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="c74c7-166">Esant poreikiui, nustatykite kitas vertes, tada pasirinkite šią sekimo numerių grupę kaip paketų numerių grupę, skirtą išleistiems produktams, kuriems norite naudoti šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="c74c7-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c74c7-167">Naudojant šį scenarijų, **Paketo numerio** laukas, kurį **Eigos ataskaita** puslapis pateikia Užduočių kortelės įrenginyje, rodo vertę, bet darbuotojai negali redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c74c7-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="c74c7-168">![Ataskaitos eigos puslapis su fiksuotu paketo numeriu](media/job-card-device-batch-fixed.png "Ataskaitos eigos puslapis su fiksuotu paketo numeriu")</span><span class="sxs-lookup"><span data-stu-id="c74c7-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="c74c7-169">Praneškite kaip baigta į numerio lentelę</span><span class="sxs-lookup"><span data-stu-id="c74c7-169">Report as finished to a license plate</span></span>

<span data-ttu-id="c74c7-170">Papildomiems sandėlių procesams gali būti naudojama numerio lentelės dimensija, kad sektumėte atsargas sandėlių vietose, nustatytose šiam tikslui.</span><span class="sxs-lookup"><span data-stu-id="c74c7-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="c74c7-171">Šiuo atveju, numerio lentelės numeris reikalingas, kai darbuotojas praneša apie baigtus kiekius.</span><span class="sxs-lookup"><span data-stu-id="c74c7-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="c74c7-172">Numerio lentelės ataskaita ir etiketės spausdinimas</span><span class="sxs-lookup"><span data-stu-id="c74c7-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="c74c7-173">Norėdami naudoti šiame skyriuje aprašytas funkcijas, turite naudoti [funkcijų valdymą, ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad galėtumėte įjungti šias funkcijas (šia tvarka):</span><span class="sxs-lookup"><span data-stu-id="c74c7-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="c74c7-174">Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį</span><span class="sxs-lookup"><span data-stu-id="c74c7-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="c74c7-175">Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą</span><span class="sxs-lookup"><span data-stu-id="c74c7-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="c74c7-176">Spausdinti etiketę iš užduoties kortelės įrenginio</span><span class="sxs-lookup"><span data-stu-id="c74c7-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="c74c7-177">Nustatykite baigimo pranešimą į numerio lentelę</span><span class="sxs-lookup"><span data-stu-id="c74c7-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="c74c7-178">Norėdami kontroliuoti, ar darbuotojai turėtų dar kartą panaudoti numerio lentelę, ar generuoti naują numerio lentelę, kai jie praneša apie baigtus kiekius, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c74c7-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="c74c7-179">Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \>Konfigūruoti įrenginių užduoties kortelę**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="c74c7-180">Nustatykite šias parinktis kiekvienam įrenginiui:</span><span class="sxs-lookup"><span data-stu-id="c74c7-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="c74c7-181">**Generuoti numerio lentelę** – nustatykite šią pasirinktį į **Taip**, kad sugeneruotumėte naują numerio lentelę kiekvienai baigimo ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="c74c7-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="c74c7-182">Nustatykite į **Ne**, jei esama numerio lentelė turėtų būti naudojama kiekvienai baigimo ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="c74c7-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="c74c7-183">**Spausdinti etiketę** – nustatykite šią pasirinktį į **Taip**, jei darbuotojas privalo atspausdinti numerio lentelės etiketę kiekvienai baigimo ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="c74c7-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="c74c7-184">Nustatykite į **Ne**, jei nereikia nei vienos etiketės.</span><span class="sxs-lookup"><span data-stu-id="c74c7-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="c74c7-185">![Užduoties kortelės konfigūravimas įrenginių puslapiui](media/config-job-card-raf.png "Užduoties kortelės konfigūravimas įrenginių puslapiui")</span><span class="sxs-lookup"><span data-stu-id="c74c7-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="c74c7-186">Norėdami konfigūruoti etiketę, eikite į **Sandėlio valdymas \> Sąranka \> Dokumentų nukreipimas \> Dokumentų nukreipimas**.</span><span class="sxs-lookup"><span data-stu-id="c74c7-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="c74c7-187">Norėdami gauti daugiau informacijos, žr. [Numerio lentelės etiketės spausdinimo įjungimas](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="c74c7-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
