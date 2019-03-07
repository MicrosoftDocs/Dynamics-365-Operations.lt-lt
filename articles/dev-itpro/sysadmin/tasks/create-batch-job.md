---
title: Sukurkite paketinę užduotį
description: Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "313364"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="cd137-103">Sukurkite paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="cd137-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd137-104">Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.</span><span class="sxs-lookup"><span data-stu-id="cd137-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="cd137-105">Paketinės užduotys yra vykdomos naudojant užduotį sukūrusio naudotojo saugos kredencialus.</span><span class="sxs-lookup"><span data-stu-id="cd137-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="cd137-106">Norėdami sukurti paketinę užduotį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="cd137-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="cd137-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="cd137-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="cd137-108">Kurti paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="cd137-108">Create the batch job</span></span>
1. <span data-ttu-id="cd137-109">Pasirinkite Sistemos administravimas > Užklausos > Paketinės užduotys.</span><span class="sxs-lookup"><span data-stu-id="cd137-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="cd137-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cd137-110">Click New.</span></span>
3. <span data-ttu-id="cd137-111">Lauke Užduoties aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd137-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="cd137-112">Lauke Suplanuota pradžios data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="cd137-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="cd137-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="cd137-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="cd137-114">Kurti pasikartojimą</span><span class="sxs-lookup"><span data-stu-id="cd137-114">Create a recurrence</span></span>
1. <span data-ttu-id="cd137-115">Veiksmų srityje spustelėkite Paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="cd137-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cd137-116">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="cd137-116">Click Recurrence.</span></span>
    * <span data-ttu-id="cd137-117">Naudokite šias parinktis, kad norėdami įvesti pasikartojimo diapazoną ir šabloną.</span><span class="sxs-lookup"><span data-stu-id="cd137-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="cd137-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cd137-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="cd137-119">Įtraukti įspėjimų</span><span class="sxs-lookup"><span data-stu-id="cd137-119">Add alerts</span></span>
1. <span data-ttu-id="cd137-120">Veiksmų srityje spustelėkite Paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="cd137-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cd137-121">Spustelėkite Įspėjimai.</span><span class="sxs-lookup"><span data-stu-id="cd137-121">Click Alerts.</span></span>
    * <span data-ttu-id="cd137-122">Nurodykite, ar norite, kad būtų siunčiami įspėjimo pranešimai, kai paketinė užduotis yra baigta, atšaukta arba kai iškyla klaida.</span><span class="sxs-lookup"><span data-stu-id="cd137-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="cd137-123">Tada nurodykite, ar norite, kad įspėjimai būtų rodomi kaip iššokantieji pranešimai.</span><span class="sxs-lookup"><span data-stu-id="cd137-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="cd137-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cd137-124">Click OK.</span></span>

