---
title: Darbo užsakymų kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo užsakymus turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875793"
---
# <a name="creating-work-orders"></a><span data-ttu-id="573c2-103">Darbo užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="573c2-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="573c2-104">Kai suplanavote prevencinės priežiūros užduotis, kitas žingsnis yra sukurti šių užduočių darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="573c2-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="573c2-105">Tai atliekame viename iš priežiūros grafikų.</span><span class="sxs-lookup"><span data-stu-id="573c2-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="573c2-106">Suplanuotos užduotys priežiūros grafike gali turėti skirtingus nuorodos numerius.</span><span class="sxs-lookup"><span data-stu-id="573c2-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="573c2-107">Nuorodos tipas</span><span class="sxs-lookup"><span data-stu-id="573c2-107">Reference type</span></span> | <span data-ttu-id="573c2-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="573c2-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="573c2-109">Priežiūros planai</span><span class="sxs-lookup"><span data-stu-id="573c2-109">Maintenance plans</span></span>     | <span data-ttu-id="573c2-110">Prevencinės priežiūros užduotys, pagrįstos priežiūros plano tipais Laikas arba Skaitiklis.</span><span class="sxs-lookup"><span data-stu-id="573c2-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="573c2-111">Priežiūros ciklai</span><span class="sxs-lookup"><span data-stu-id="573c2-111">Maintenance rounds</span></span>    | <span data-ttu-id="573c2-112">Prevencinės priežiūros užduotys, kuriose yra keli turtai, kuriems reikia atlikti panašaus tipo priežiūrą.</span><span class="sxs-lookup"><span data-stu-id="573c2-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="573c2-113">Priežiūros užklausa</span><span class="sxs-lookup"><span data-stu-id="573c2-113">Maintenance request</span></span>   | <span data-ttu-id="573c2-114">Rankiniu būdu sukurta turto priežiūros arba remonto užklausa, kurią galima pakeisti į darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="573c2-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="573c2-115">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Visi priežiūros grafikai** arba **Atviros priežiūros grafiko eilutės**, arba **Atviri priežiūros grafiko telkiniai**.</span><span class="sxs-lookup"><span data-stu-id="573c2-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="573c2-116">Pasirinkite suplanuotas priežiūros užduotis, kurioms norite sukurti darbo užsakymą, tada spustelėkite **Darbo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="573c2-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="573c2-117">Bendras pasirinktų eilučių numatytų valandų skaičius rodomas lauke **Numatytos priežiūros valandos**.</span><span class="sxs-lookup"><span data-stu-id="573c2-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="573c2-118">Skyriuje **Parametrai** pasirinkite, kiek darbo užsakymų turi būti sukurta.</span><span class="sxs-lookup"><span data-stu-id="573c2-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="573c2-119">Vienai priežiūros grafiko eilutei galite sukurti vieną darbo užsakymą arba kelis darbo užsakymus pagal pasirinkimus skyriuje **Vienas darbo užsakymas vienai**.</span><span class="sxs-lookup"><span data-stu-id="573c2-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="573c2-120">Pažymėkite **Darbo užsakymo tipas**, kuris bus naudojamas visiems sukurtiems darbo užsakymams.</span><span class="sxs-lookup"><span data-stu-id="573c2-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="573c2-121">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="573c2-121">Click **OK**.</span></span> <span data-ttu-id="573c2-122">Sukurtas vienas arba keli darbo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="573c2-122">One or more work orders are created.</span></span>

![1 pav.](media/18-preventive-maintenance.png)

