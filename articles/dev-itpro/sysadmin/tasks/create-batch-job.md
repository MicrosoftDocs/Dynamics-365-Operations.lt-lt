--- 
title: "Sukurkite paketinę užduotį"
description: "Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 55b153e6044f61f16e19ae0b264e3f23538e004a
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="4f112-103">Sukurkite paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="4f112-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f112-104">Paketinė užduotis yra užduočių, pateiktų programos objektų serverio (AOS) egzemplioriui automatiškai apdoroti, grupė.</span><span class="sxs-lookup"><span data-stu-id="4f112-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="4f112-105">Paketinės užduotys yra vykdomos naudojant užduotį sukūrusio naudotojo saugos kredencialus.</span><span class="sxs-lookup"><span data-stu-id="4f112-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="4f112-106">Norėdami sukurti paketinę užduotį, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="4f112-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="4f112-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="4f112-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="4f112-108">Kurti paketinę užduotį</span><span class="sxs-lookup"><span data-stu-id="4f112-108">Create the batch job</span></span>
1. <span data-ttu-id="4f112-109">Pasirinkite Sistemos administravimas > Užklausos > Paketinės užduotys.</span><span class="sxs-lookup"><span data-stu-id="4f112-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="4f112-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4f112-110">Click New.</span></span>
3. <span data-ttu-id="4f112-111">Lauke Užduoties aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4f112-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="4f112-112">Lauke Suplanuota pradžios data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="4f112-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="4f112-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4f112-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="4f112-114">Kurti pasikartojimą</span><span class="sxs-lookup"><span data-stu-id="4f112-114">Create a recurrence</span></span>
1. <span data-ttu-id="4f112-115">Veiksmų srityje spustelėkite Paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="4f112-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="4f112-116">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="4f112-116">Click Recurrence.</span></span>
    * <span data-ttu-id="4f112-117">Naudokite šias parinktis, kad norėdami įvesti pasikartojimo diapazoną ir šabloną.</span><span class="sxs-lookup"><span data-stu-id="4f112-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="4f112-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4f112-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="4f112-119">Įtraukti įspėjimų</span><span class="sxs-lookup"><span data-stu-id="4f112-119">Add alerts</span></span>
1. <span data-ttu-id="4f112-120">Veiksmų srityje spustelėkite Paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="4f112-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="4f112-121">Spustelėkite Įspėjimai.</span><span class="sxs-lookup"><span data-stu-id="4f112-121">Click Alerts.</span></span>
    * <span data-ttu-id="4f112-122">Nurodykite, ar norite, kad būtų siunčiami įspėjimo pranešimai, kai paketinė užduotis yra baigta, atšaukta arba kai iškyla klaida.</span><span class="sxs-lookup"><span data-stu-id="4f112-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="4f112-123">Tada nurodykite, ar norite, kad įspėjimai būtų rodomi kaip iššokantieji pranešimai.</span><span class="sxs-lookup"><span data-stu-id="4f112-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="4f112-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4f112-124">Click OK.</span></span>


