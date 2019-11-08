---
title: Darbo užsakymų kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo užsakymus turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: 6e910b2400106baf9f9dc06f6bc0d3daee8e4a43
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570081"
---
# <a name="creating-work-orders"></a><span data-ttu-id="56855-103">Darbo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="56855-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="56855-104">Kai suplanavote prevencinės priežiūros užduotis, kitas žingsnis yra sukurti šių užduočių darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="56855-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="56855-105">Tai atliekame viename iš priežiūros grafikų.</span><span class="sxs-lookup"><span data-stu-id="56855-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="56855-106">Suplanuotos užduotys priežiūros grafike gali turėti skirtingus nuorodos numerius.</span><span class="sxs-lookup"><span data-stu-id="56855-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="56855-107">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="56855-107">Reference type</span></span> | <span data-ttu-id="56855-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="56855-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56855-109">Priežiūros planai</span><span class="sxs-lookup"><span data-stu-id="56855-109">Maintenance plans</span></span>     | <span data-ttu-id="56855-110">Prevencinės priežiūros užduotys, pagrįstos priežiūros plano tipais Laikas arba Skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="56855-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="56855-111">Priežiūros ciklai</span><span class="sxs-lookup"><span data-stu-id="56855-111">Maintenance rounds</span></span>    | <span data-ttu-id="56855-112">Prevencinės priežiūros užduotys, kuriose yra keli turtai, kuriems reikia atlikti panašaus tipo priežiūrą.</span><span class="sxs-lookup"><span data-stu-id="56855-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="56855-113">Priežiūros užklausa</span><span class="sxs-lookup"><span data-stu-id="56855-113">Maintenance request</span></span>   | <span data-ttu-id="56855-114">Rankiniu būdu sukurta turto priežiūros arba remonto užklausa, kurią galima pakeisti į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="56855-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="56855-115">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Visi priežiūros grafikai** arba **Atviros priežiūros grafiko eilutės**, arba **Atviri priežiūros grafiko telkiniai**.</span><span class="sxs-lookup"><span data-stu-id="56855-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="56855-116">Pasirinkite suplanuotas priežiūros užduotis, kurioms norite sukurti darbo užsakymą, tada spustelėkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="56855-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="56855-117">Dialogo lange **Darbo užsakymų kūrimas** bendras pasirinktų eilučių numatytų valandų skaičius rodomas lauke **Numatytos priežiūros valandos**.</span><span class="sxs-lookup"><span data-stu-id="56855-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="56855-118">Skyriuje **Parametrai** pasirinkite, kiek darbo užsakymų turi būti sukurta.</span><span class="sxs-lookup"><span data-stu-id="56855-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="56855-119">Vienai priežiūros grafiko eilutei galite sukurti vieną darbo užsakymą arba kelis darbo užsakymus pagal pasirinkimus skyriuje **Vienas darbo užsakymas vienai**.</span><span class="sxs-lookup"><span data-stu-id="56855-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="56855-120">Pažymėkite **Darbo užsakymo tipas**, kuris bus naudojamas visiems sukurtiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="56855-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="56855-121">Toliau pateiktame paveikslėlyje parodytas dialogo lango **Darbo užsakymų kūrimas** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="56855-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![1 pav.](media/18-preventive-maintenance.png)

5. <span data-ttu-id="56855-123">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="56855-123">Click **OK**.</span></span> <span data-ttu-id="56855-124">Sukurtas vienas arba keli darbo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="56855-124">One or more work orders are created.</span></span>

