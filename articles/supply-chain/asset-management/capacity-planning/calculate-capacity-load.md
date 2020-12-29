---
title: Skaičiuoti pajėgumą
description: Šioje temoje aiškinama, kaip išsiųsti apskaičiuoti pajėgumą turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433711"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="881e2-103">Pajėgumo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="881e2-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="881e2-104">Turto valdyme galite apskaičiuoti pajėgumą šiems elementams:</span><span class="sxs-lookup"><span data-stu-id="881e2-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="881e2-105">priežiūros grafiko eilutės</span><span class="sxs-lookup"><span data-stu-id="881e2-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="881e2-106">darbo užsakymai, kurie dar nėra suplanuoti</span><span class="sxs-lookup"><span data-stu-id="881e2-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="881e2-107">suplanuoti darbo užsakymai</span><span class="sxs-lookup"><span data-stu-id="881e2-107">scheduled work orders</span></span>

<span data-ttu-id="881e2-108">Tai naudinga, jei norite peržiūrėti numatytą pajėgumą konkrečiu laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="881e2-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="881e2-109">Galima apskaičiuoti viso turto arba pasirinkto turto pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="881e2-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="881e2-110">Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklas arba darbo užsakymų telkinius.</span><span class="sxs-lookup"><span data-stu-id="881e2-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="881e2-111">Spustelėkite mygtuką **Turto valdymas** > **Užklausos** > **Pajėgumas** arba **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** / **Aktyvių darbo užsakymų telkiniai** >pasirinkti darbo užsakymų telkinį sąraše > **Pajėgumas** arba mygtuką **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos** / **Aktyvios prižiūrimo turto prastovos veiklos** > pasirinkti priežiūros veiklą sąraše > **Pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="881e2-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="881e2-112">Dialoge **Skaičiuoti pajėgumą** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="881e2-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="881e2-113">Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į skaičiavimą įtraukti priežiūros grafiko eilutes.</span><span class="sxs-lookup"><span data-stu-id="881e2-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="881e2-114">Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į skaičiavimą įtraukti darbo užsakymo užduotis.</span><span class="sxs-lookup"><span data-stu-id="881e2-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="881e2-115">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti pajėgumo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="881e2-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="881e2-116">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="881e2-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="881e2-117">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="881e2-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="881e2-118">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="881e2-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="881e2-119">Grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis.</span><span class="sxs-lookup"><span data-stu-id="881e2-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="881e2-120">Toliau pateiktoje ekrano kopijoje pasirinkti mygtukai **Grupuoti pagal** yra pažymėti mėlynai.</span><span class="sxs-lookup"><span data-stu-id="881e2-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="881e2-121">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="881e2-121">Click on a button to activate or deactivate it.</span></span>

    ![1 pav.](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="881e2-123">Jei norite planuoti tik suplanuotų darbo užsakymų pajėgumą, žr. [Suplanuotų darbo užsakymų pajėgumo skaičiavimas](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="881e2-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

