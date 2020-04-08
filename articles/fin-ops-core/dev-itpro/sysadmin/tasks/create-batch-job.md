---
title: Sukurkite paketinę užduotį
description: Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143678"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="057fe-103">Sukurkite paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="057fe-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="057fe-104">Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.</span><span class="sxs-lookup"><span data-stu-id="057fe-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="057fe-105">Paketinės užduotys yra vykdomos naudojant užduotį sukūrusio naudotojo saugos kredencialus.</span><span class="sxs-lookup"><span data-stu-id="057fe-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="057fe-106">Norėdami sukurti paketinę užduotį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="057fe-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="057fe-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="057fe-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="057fe-108">Kurti paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="057fe-108">Create the batch job</span></span>
1. <span data-ttu-id="057fe-109">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="057fe-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="057fe-110">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="057fe-110">Click **New**.</span></span>
3. <span data-ttu-id="057fe-111">Lauke **Užduoties aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="057fe-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="057fe-112">Lauke **Suplanuota pradžios data / laikas** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="057fe-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="057fe-113">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="057fe-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="057fe-114">Kurti pasikartojimą</span><span class="sxs-lookup"><span data-stu-id="057fe-114">Create a recurrence</span></span>
1. <span data-ttu-id="057fe-115">Veiksmų srityje spustelėkite **Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="057fe-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="057fe-116">Spustelėkite **Pasikartojimas**.</span><span class="sxs-lookup"><span data-stu-id="057fe-116">Click **Recurrence**.</span></span> <span data-ttu-id="057fe-117">Naudokite šias parinktis, kad norėdami įvesti pasikartojimo diapazoną ir šabloną.</span><span class="sxs-lookup"><span data-stu-id="057fe-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="057fe-118">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="057fe-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="057fe-119">Įtraukti įspėjimų</span><span class="sxs-lookup"><span data-stu-id="057fe-119">Add alerts</span></span>
1. <span data-ttu-id="057fe-120">Veiksmų srityje spustelėkite **Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="057fe-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="057fe-121">Spustelėkite **Įspėjimai**.</span><span class="sxs-lookup"><span data-stu-id="057fe-121">Click **Alerts**.</span></span> <span data-ttu-id="057fe-122">Nurodykite, ar norite, kad būtų siunčiami įspėjimo pranešimai, kai paketinė užduotis yra baigta, atšaukta arba kai iškyla klaida.</span><span class="sxs-lookup"><span data-stu-id="057fe-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="057fe-123">Tada nurodykite, ar norite, kad įspėjimai būtų rodomi kaip iššokantieji pranešimai.</span><span class="sxs-lookup"><span data-stu-id="057fe-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="057fe-124">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="057fe-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="057fe-125">Paketinės užduoties būsenos koregavimas</span><span class="sxs-lookup"><span data-stu-id="057fe-125">Adjust batch job status</span></span>
1. <span data-ttu-id="057fe-126">Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="057fe-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="057fe-127">Pasirinkite atitinkamą paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="057fe-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="057fe-128">Veiksmų srityje spustelėkite **Paketinė užduotis > Funkcijos > Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="057fe-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="057fe-129">Pasirinkite atitinkamą būseną:</span><span class="sxs-lookup"><span data-stu-id="057fe-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="057fe-130">**Sulaikyti**: nustatykite paketinę užduotį kaip **sulaikytą**, kad užduotis būtų sulaikyta paketinių užduočių planuoklėje.</span><span class="sxs-lookup"><span data-stu-id="057fe-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="057fe-131">Prilygsta *sustabdymui*.</span><span class="sxs-lookup"><span data-stu-id="057fe-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="057fe-132">**Laukiama**: nustatykite paketinę užduotį kaip **laukiančią**, kad jį būtų eilėje, kol ją paims paketinių užduočių planuoklę.</span><span class="sxs-lookup"><span data-stu-id="057fe-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="057fe-133">Prilygsta *vykdymui*.</span><span class="sxs-lookup"><span data-stu-id="057fe-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="057fe-134">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="057fe-134">Click **OK**.</span></span>
