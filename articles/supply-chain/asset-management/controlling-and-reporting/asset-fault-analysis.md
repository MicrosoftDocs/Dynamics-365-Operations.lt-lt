---
title: Turto klaidų analizė
description: Šioje temoje aiškinama turto gedimų analizė turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43772903f6845409cb33c7f2a13a049a3e9aa208
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652407"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="fd8ba-103">Turto klaidų analizė</span><span class="sxs-lookup"><span data-stu-id="fd8ba-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="fd8ba-104">Turto valdyme galite analizuoti turto gedimų registracijas, kad galėtumėte peržiūrėti bendrą konkrečiu laikotarpiu užregistruotų gedimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="fd8ba-105">Gedimų registracijas galima analizuoti skirtingais būdais, pavyzdžiui, pagal turtą, turto tipus, funkcines vietas, gedimo požymius ar gedimų tipus.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="fd8ba-106">Spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimo analizė**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="fd8ba-107">Dialoge lange **Turto gedimo analizės skaičiavimas** galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto gedimo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="fd8ba-108">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos turto gedimo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="fd8ba-109">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, turto gedimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="fd8ba-110">Jei norite apriboti iešką, „FastTab“ **Įtrauktini įrašai** galite pažymėti konkretų turtą, gedimų datas, gedimo priežastis ir gedimo šalinimo priemones.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="fd8ba-111">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="fd8ba-112">Skirtuke **Turto gedimo analizė** spustelėkite vieną ar daugiau mygtukų **Grupuoti pagal**, kad būtų rodoma lygio, kurį norite matyti, išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="fd8ba-113">Suaktyvinti mygtukai yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="fd8ba-114">Suaktyvinkite arba deaktyvinkite mygtukus juos spustelėdami.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="fd8ba-115">Spustelėkite **Naujinti skaičiavimus**, kad pasirinkimai būtų rodomi ekrane.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="fd8ba-116">Kiekvieną kartą, kai aktyvindami arba deaktyvindami mygtuką **Grupuoti pagal**, nepamirškite spustelėti mygtuko **Naujinti skaičiavimus**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="fd8ba-117">Taip reikia, nes kai perskaičiuojama gedimo tikimybė, apdorojamas didelis kiekis duomenų.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="fd8ba-118">Pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="fd8ba-118">Examples</span></span>

<span data-ttu-id="fd8ba-119">Yra daug būdų, kaip analizuoti gedimų registracijas.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="fd8ba-120">Šiame skyriuje pateikti penki pavyzdžiai, kaip analizuojant turto gedimų registracijas skirtingai pasirinkus duomenis galima gauti daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="fd8ba-121">Grupuoti pagal požymius</span><span class="sxs-lookup"><span data-stu-id="fd8ba-121">Group by symptoms</span></span>

<span data-ttu-id="fd8ba-122">Toliau pateiktoje ekrano kopijoje pažymėtas tik mygtukas **Požymis**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="fd8ba-123">Gedimo registracijos atliktos pagal tris gedimo požymius: „Oro nuotėkis“, „Perdegęs saugiklis“ ir „Užstrigo įranga“.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="fd8ba-124">Stulpelyje **Tikimybės %** visi procentai sumuojami iki 100 %.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="fd8ba-125">Šioje gedimo analizėje tikimybė pagrįsta visomis **Požymis** registracijomis.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![1 pav.](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="fd8ba-127">Grupuoti pagal požymius ir laikotarpį</span><span class="sxs-lookup"><span data-stu-id="fd8ba-127">Group by symptoms and time period</span></span>

<span data-ttu-id="fd8ba-128">Toliau pateiktoje ekrano kopijoje įtraukti **Metai** ir **Mėnuo**, kad pamatytumėte, kaip galite peržiūrėti gedimų registracijas pagal pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="fd8ba-129">Dabar gedimo požymiai rodomi kaip registracijos pagal metus / mėnesį.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="fd8ba-130">Stulpelyje **Tikimybės %**, jei įtraukiate visus kiekvieno mėnesio procentus, jie sumuojami iki 100 %.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="fd8ba-131">Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="fd8ba-132">Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![2 pav.](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="fd8ba-134">Grupuoti pagal kelis simptomus ir turtą</span><span class="sxs-lookup"><span data-stu-id="fd8ba-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="fd8ba-135">Turto ir turto tipo derinys naudojamas remiantis skaičiavimais, parodytais toliau pateiktose trijose ekrano kopijose, kurie didėja pagal išsamumo lygį.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="fd8ba-136">Paprastai, veiksmų srities grupių **Grupuoti pagal datą**, **Grupuoti pagal turtą**, **Grupuoti pagal funkcinę vietą** mygtukai ir mygtukas **Gedimas** (gedimo ID) turi laikotarpius arba turto ryšius.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="fd8ba-137">Mygtukai **Požymis**, **Sritis**, **Tipas**, **Priežastis** ir **Šalinimo priemonė** yra kategorizacijos, naudojamos turto valdyme norint analizuoti turto gedimą ir nurodyti problemos sritis.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="fd8ba-138">**Grupuoti pagal požymį, turtą ir turto tipą**</span><span class="sxs-lookup"><span data-stu-id="fd8ba-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="fd8ba-139">Toliau pateiktoje ekrano kopijoje įtraukti **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="fd8ba-140">Dabar gedimo požymiai yra padalinti į derinius **Turtas** / **Turto tipas** / **Požymis**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="fd8ba-141">Stulpelyje **Tikimybė %**, jei įtraukiate visus derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="fd8ba-142">Šioje gedimo analizėje tikimybė pagrįsta **Požymis** registracijomis.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="fd8ba-143">Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo požymį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo požymio registracijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![3 pav.](media/08-controlling-and-reporting.png)

<span data-ttu-id="fd8ba-145">**Grupuoti pagal du požymius, turtą ir turto tipą**</span><span class="sxs-lookup"><span data-stu-id="fd8ba-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="fd8ba-146">Toliau pateiktose ekrano kopijoje **Sritis** įtraukta į **Požymis**, **Turtas** ir **Turto tipas**, kad būtų rodoma daugiau informacijos apie gedimo registracijas.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="fd8ba-147">Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="fd8ba-148">Šioje gedimo analizėje tikimybė pagrįsta **Požymis** ir **Sritis** registracijomis.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="fd8ba-149">Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo sritį reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo srities registracijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![4 pav.](media/09-controlling-and-reporting.png)

<span data-ttu-id="fd8ba-151">**Grupuoti pagal tris požymius, turtą ir turto tipą**</span><span class="sxs-lookup"><span data-stu-id="fd8ba-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="fd8ba-152">Toliau pateiktoje ekrano nuotraukoje buvo įtrauktas **Tipas** ir šiame pavyzdyje pateikiamas išsamiausias skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="fd8ba-153">Stulpelyje **Tikimybės %**, jei įtraukiate visus turto derinio **Turtas** / **Turto tipas** / **Požymis** procentus, kiekvienas iš jų sumuojamas iki 100 %.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="fd8ba-154">Šioje gedimo analizėje tikimybė pagrįsta **Požymis**, **Sritis** ir **Tipas** deriniu.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="fd8ba-155">Jei yra daug turto eilučių, tačiau vienoje eilutėje rodomas didelis procentas, reiškia, kad gedimo tipą reikia išanalizuoti išsamiau, kad rastumėte būdą, kaip apriboti gedimo tipo registracijų skaičių.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![5 paveikslėlis](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="fd8ba-157">Norėdami peržiūrėti visas gedimų registracijas, sukurtas darbo užsakymuose ir priežiūros užklausose, spustelėkite **Turto valdymas** > **Užklausos** > **Turto gedimas** > **Turto gedimai**.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="fd8ba-158">Puslapyje **Turto gedimai** pažymėkite turto gedimo registraciją ir išplėskite sritį **Susijusi informacija**, kad matytumėte susijusio darbo užsakymo arba priežiūros užklausos informaciją.</span><span class="sxs-lookup"><span data-stu-id="fd8ba-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

