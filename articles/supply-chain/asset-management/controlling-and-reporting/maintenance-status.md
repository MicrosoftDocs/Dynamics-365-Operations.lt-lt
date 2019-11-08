---
title: Priežiūros būsena
description: Šioje temoje aprašoma, kaip skaičiuoti priežiūros būseną skiltyje Turto valdymas.
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
ms.openlocfilehash: 8f336086838632dd3f464de2870e9a9197746daa
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652131"
---
# <a name="maintenance-status"></a><span data-ttu-id="e9364-103">Priežiūros būsena</span><span class="sxs-lookup"><span data-stu-id="e9364-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e9364-104">Skiltyje Turto valdymas galite vykdyti skaičiavimus, norėdami matyti nurodyto laikotarpio naujų, aktyvių ir baigtų priežiūros užklausų, darbo užsakymų ir prižiūrimo turto prastovos veiklų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="e9364-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="e9364-105">Tai pat galite matyti nurodyto laikotarpio baigtų sąlygų įvertinimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="e9364-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="e9364-106">Naudokite šį skaičiavimą peržiūrėti darbo krūvį, susijusį su gautinomis ir baigtomis priežiūros užklausomis ir darbo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="e9364-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="e9364-107">Vykdykite priežiūros būsenos skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="e9364-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="e9364-108">Spustelėkite **Turto valdymas** > **Užklausos** > **Priežiūros būsena**.</span><span class="sxs-lookup"><span data-stu-id="e9364-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="e9364-109">Dialogo lange **Apskaičiuoti būseną** pasirinkite laiko intervalą, pagal kurį norite atlikti skaičiavimą, laukuose **Nuo datos** ir **Iki datos**.</span><span class="sxs-lookup"><span data-stu-id="e9364-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="e9364-110">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti priežiūros eilutėse.</span><span class="sxs-lookup"><span data-stu-id="e9364-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="e9364-111">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl būseną į eilutę galėsite įtraukti iš žemiau esančių funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="e9364-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="e9364-112">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, priežiūros eilutes.</span><span class="sxs-lookup"><span data-stu-id="e9364-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="e9364-113">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e9364-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="e9364-114">Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis.</span><span class="sxs-lookup"><span data-stu-id="e9364-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e9364-115">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="e9364-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e9364-116">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="e9364-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="e9364-117">Nepamirškite spustelėti mygtuko **Naujinti**, kad skaičiavimai kiekvienąkart atsinaujintų, kai atliksite keitimus suaktyvindami arba išjungdami mygtukus **Grupuoti pagal** arba atlikdami naujo laikotarpio skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="e9364-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="e9364-118">Spustelėkite **Būsena**, jei norite sukurti naują priežiūros būsenos skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="e9364-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="e9364-119">Skiltyje **Priežiūros būsena** rezultatai formuojami tik iš priežiūros užklausų ir darbo užsakymų, kurie turi faktinius pradžios datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="e9364-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="e9364-120">Pabaigos data ir laikas gali būti tušti.</span><span class="sxs-lookup"><span data-stu-id="e9364-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="e9364-121">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e9364-121">Example 1</span></span>

<span data-ttu-id="e9364-122">Toliau pateiktoje ekrano kopijoje yra suaktyvinti mygtukai **Metai** ir **Mėnuo**.</span><span class="sxs-lookup"><span data-stu-id="e9364-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="e9364-123">Pasirinkę šias **Grupuoti pagal** parinktis, galite matyti bendrą mėnesinę darbo krūvio ir našumo, susijusio su priežiūros užklausomis ir darbo užsakymais, apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="e9364-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Mėnesinio darbo krūvio pavyzdys](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="e9364-125">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e9364-125">Example 2</span></span>

<span data-ttu-id="e9364-126">Toliau pateiktoje ekrino kopijoje buvo įterpta informacija apie funkcines vietas.</span><span class="sxs-lookup"><span data-stu-id="e9364-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="e9364-127">Dabar galite palyginti darbo krūvį ir našumą funkcinėse vietose, kuriose gali nurodyti geografines vietas, gamyklas arba darbo vietas.</span><span class="sxs-lookup"><span data-stu-id="e9364-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Mėnesinio darbo krūvio su funkcinėmis vietomis pavyzdys](media/14-controlling-and-reporting.png)

