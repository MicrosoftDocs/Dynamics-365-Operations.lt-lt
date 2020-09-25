---
title: Projekto išteklių planavimo našumas
description: Šioje temoje pateikiama informacija apie tai, kaip padidinti daugelio projektų išteklių planavimo našumą.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760619"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="31b61-103">Projekto išteklių planavimo našumas</span><span class="sxs-lookup"><span data-stu-id="31b61-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="31b61-104">Našumo problemos, susijusios su išteklių planavimu, gali įvykti, kai projektų skaičius pasiekia tūkstančius.</span><span class="sxs-lookup"><span data-stu-id="31b61-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="31b61-105">Siekiant padidinti išteklių planavimo našumą, siūloma funkcija, leidžianti vartotojams sutrumpinti laiką, kurio reikia išteklių pasiekiamumo formai paleisti.</span><span class="sxs-lookup"><span data-stu-id="31b61-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="31b61-106">Tiksliau sakant, taip pašalinamas išteklių pajėgumų sumavimų sinchronizavimo procesas ir naudojama lentelė **ResProjectResource** siekiant paspartinti išteklių peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="31b61-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="31b61-107">Atkreipkite dėmesį, kad lentelė **ResRollup** nebebus naudojama.</span><span class="sxs-lookup"><span data-stu-id="31b61-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31b61-108">Jei yra priklausomybė nuo išteklių pajėgumų sumavimų sinchronizavimo proceso arba lentelės **ResProjectResource**, nenaudokite šios funkcijos.</span><span class="sxs-lookup"><span data-stu-id="31b61-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="31b61-109">Išteklių planavimo našumo didinimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="31b61-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="31b61-110">Norėdami įjungti išteklių planavimo našumo didinimą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="31b61-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="31b61-111">Eikite į **Funkcijų valdymas** > **Visi** ir funkcijų sąraše suraskite **Įjungti projektų išteklių planavimo našumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="31b61-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="31b61-112">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="31b61-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="31b61-113">Jeigu nerandate funkcijos sąraše, pasirinkite **Tikrinti, ar yra naujinimų**, kad sąrašas būtų atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="31b61-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="31b61-114">Atnaujinkite naršyklę ir eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Projekto ištekliai** > **Sinchronizuoti išteklių kalendorių pajėgumą visose įmonėse**.</span><span class="sxs-lookup"><span data-stu-id="31b61-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="31b61-115">Nustatykite **Pašalinti esamus pajėgumo įrašus** į **Taip** , kad būtų pašalinti ankstesni duomenys.</span><span class="sxs-lookup"><span data-stu-id="31b61-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="31b61-116">Jei norite generuoti papildančius duomenis, nustatykite į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="31b61-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="31b61-117">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio metu turi būti sugeneruoti duomenys.</span><span class="sxs-lookup"><span data-stu-id="31b61-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="31b61-118">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datų nebūtina nurodyti.</span><span class="sxs-lookup"><span data-stu-id="31b61-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="31b61-119">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="31b61-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="31b61-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="31b61-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="31b61-121">Bendrieji duomenys bus paskirstyti į lentelę **ResCalendarCapacity** visose jūsų aplinkos įmonėse, kad paketinė užduotis būtų vykdoma tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="31b61-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="31b61-122">Šios paketinės užduoties duomenys reikalingi, kad būtų galima apskaičiuoti išteklių pajėgumą naudojant susijusį kalendorių.</span><span class="sxs-lookup"><span data-stu-id="31b61-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="31b61-123">Eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Projekto ištekliai** > **Automatiškai įvesti projekto išteklius visose įmonėse** ir pasirinkite **Gerai** .</span><span class="sxs-lookup"><span data-stu-id="31b61-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="31b61-124">Tai yra bendrųjų duomenų naujinimo scenarijus lentelėse **ResProjectResource**, **ResCalendarDateTimeRange** ir **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="31b61-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="31b61-125">Reikšmės, skirtos laukui **PSAPRojSchedRole.RootActivity**, taip pat atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="31b61-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="31b61-126">Jei nevykdoma, gausite įspėjimą, kai bandysite vykdyti išteklių planavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="31b61-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="31b61-127">Išteklių planavimo našumo didinimo išjungimas</span><span class="sxs-lookup"><span data-stu-id="31b61-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="31b61-128">Eikite į **Funkcijų valdymas** > **Visi** ir raskite **Įjungti projektų išteklių planavimo našumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="31b61-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="31b61-129">Pasirinkite funkciją ir tada pasirinkite mygtuką **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="31b61-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="31b61-130">Atnaujinkite naršyklę.</span><span class="sxs-lookup"><span data-stu-id="31b61-130">Refresh your browser.</span></span>
4. <span data-ttu-id="31b61-131">Eikite į **Projektų valdymas ir apskaita** > **Laikotarpio** > **Pajėgumo sinchronizavimas** > **Sinchronizuoti išteklių pajėgumų sumavimus**.</span><span class="sxs-lookup"><span data-stu-id="31b61-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="31b61-132">Norėdami pašalinti ankstesnius duomenis, puslapyje **Pajėgumų sumavimų sinchronizavimas** nustatykite **Pašalinti esamus pajėgumo įrašus** į **Taip** .</span><span class="sxs-lookup"><span data-stu-id="31b61-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="31b61-133">Jei norite generuoti papildančius duomenis, nustatykite į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="31b61-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="31b61-134">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio metu turi būti sugeneruoti duomenys.</span><span class="sxs-lookup"><span data-stu-id="31b61-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="31b61-135">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datų nebūtina nurodyti.</span><span class="sxs-lookup"><span data-stu-id="31b61-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="31b61-136">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="31b61-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="31b61-137">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="31b61-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="31b61-138">Bendrieji duomenys bus paskirstyti į lentelę **ResRollup** visose jūsų aplinkos įmonėse, kad paketinė užduotis būtų vykdoma tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="31b61-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="31b61-139">Ši paketinė užduotis reikalinga visuose rodiniuose **Išteklių pasiekiamumas**.</span><span class="sxs-lookup"><span data-stu-id="31b61-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="31b61-140">Jei ši paketinė užduotis nevykdoma, **ResRollup** duomenys bus generuojami iš karto, o tai gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="31b61-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
