---
title: Apibrėžkite išteklių galimybės
description: Išteklių pajėgumai apibūdina, ką gali atlikti operacijų ištekliai.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c07d3fe1969f3baea484991e74f668eade813d78
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433293"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="d8fc6-103">Apibrėžkite išteklių galimybės</span><span class="sxs-lookup"><span data-stu-id="d8fc6-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8fc6-104">Išteklių pajėgumai apibūdina, ką gali atlikti operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="d8fc6-105">Planuojant, kiekvienos užduoties ir operacijos reikalavimai lyginami su turimų išteklių pajėgumais.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="d8fc6-106">Šis užduočių vadovas jums padės sukurti išteklių pajėgumą ir jį priskirti ištekliui.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="d8fc6-107">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="d8fc6-108">Kurti ištekliaus pajėgumą</span><span class="sxs-lookup"><span data-stu-id="d8fc6-108">Create a resource capability</span></span>
1. <span data-ttu-id="d8fc6-109">Eikite į Išteklių pajėgumai.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="d8fc6-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-110">Click New.</span></span>
3. <span data-ttu-id="d8fc6-111">Lauke Pajėgumas surinkite ištekliaus pajėgumo ID.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="d8fc6-112">Atliekant konkrečią operaciją, naudojamas pajėgumų ID, siekiant nurodyti, kad ištekliai turi šių pajėgumų operacijai atlikti.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="d8fc6-113">Lauke Aprašas įveskite pajėgumo aprašą.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="d8fc6-114">Priskirti pajėgumą ištekliui</span><span class="sxs-lookup"><span data-stu-id="d8fc6-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="d8fc6-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-115">Click Add.</span></span>
2. <span data-ttu-id="d8fc6-116">Lauke Išteklius surinkite ištekliaus ID.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="d8fc6-117">Išteklių pajėgumus galima priskirti vienam ar keliems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="d8fc6-118">Lauke Galiojimo pabaiga įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="d8fc6-119">Šį lauką galite naudoti norėdami nurodyti, kad pajėgumų išteklius turi tik ribotą laiką.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="d8fc6-120">Lauke Prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="d8fc6-121">Kai planuojate užduotis ir operacijas, galite nurodyti, ar išteklius pasirinkti pagal prioritetą.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="d8fc6-122">Jei pasirenkate daryti taip, ir užduotį arba operaciją iki pageidaujamos datos gali atlikti daugiau nei vienas išteklius, pasirenkamas išteklius, kurio prioritetas reikiamų pajėgumų atžvilgiu yra žemiausias.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="d8fc6-123">Lauke Lygis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="d8fc6-124">Kai nurodote, kad užduočiai arba operacijai atlikti reikia konkrečių pajėgumų, taip pat galite nurodyti minimalų reikiamą lygį.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="d8fc6-125">Pajėgumų lygį naudokite norėdami diferencijuoti išteklius, kurie gali atlikti tą pačią užduotį, tik skirtingu greičiu, pajėgumu, mastu ir t. t.</span><span class="sxs-lookup"><span data-stu-id="d8fc6-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

