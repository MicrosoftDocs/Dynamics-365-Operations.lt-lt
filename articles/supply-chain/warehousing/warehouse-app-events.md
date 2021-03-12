---
title: Sandėlio programos įvykiai
description: Šioje temoje aprašomas sandėlio programos įvykių apdorojimas, naudojamas siekiant apdoroti sandėlio programos įvykių pranešimus kaip paketinės užduoties dalį.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 66a5ca8a679563b59ca23992f7e0b4ee6fab470b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993809"
---
# <a name="warehouse-app-event-processing"></a><span data-ttu-id="e01ec-103">Sandėlio programos įvykių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="e01ec-103">Warehouse app event processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e01ec-104">„Supply Chain Management“ vykdomos paketinės užduotys gali naudoti duomenis iš apdorojimo įvykių eilės, kuri yra gaunama iš sandėlio programos, kad, jei reikia, galėtų reaguoti į pateikiamus įvykius.</span><span class="sxs-lookup"><span data-stu-id="e01ec-104">Batch jobs running in Supply Chain Management can use data from a queue for processing events issued by the warehouse app to react as needed to the signaled events.</span></span> <span data-ttu-id="e01ec-105">Ši funkcija įtraukia atitinkamus įvykius į eilę, reaguodama į tam tikrų tipų veiksmus, kuriuos atlieka darbuotojai naudodami programą.</span><span class="sxs-lookup"><span data-stu-id="e01ec-105">This feature add relevant events to the queue in response to certain types of actions taken by workers using the app.</span></span> <span data-ttu-id="e01ec-106">Pavyzdžiui, kai naudojate funkciją **Kurti ir apdoroti perkėlimo užsakymus iš sandėlio programos**, sistemai vykdant paketinę užduotį **Apdoroti sandėlio programos įvykius** fone sukuriama ir atnaujinama perkėlimo užsakymo antraštė bei eilutės.</span><span class="sxs-lookup"><span data-stu-id="e01ec-106">An example is when using the **Create and process transfer orders from the warehouse app** feature, the transfer order header and lines get created and updated in the back end when the system is running the **Process warehouse app events** batch job.</span></span>

## <a name="enable-the-process-warehouse-app-events-feature"></a><span data-ttu-id="e01ec-107">Sandėlio programos įvykių apdorojimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="e01ec-107">Enable the Process warehouse app events feature</span></span>

<span data-ttu-id="e01ec-108">Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="e01ec-108">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="e01ec-109">Administratoriai gali naudoti [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="e01ec-109">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="e01ec-110">Sandėlio programos įvykių funkcijos elementai:</span><span class="sxs-lookup"><span data-stu-id="e01ec-110">The Process warehouse app events feature is listed as:</span></span>

- <span data-ttu-id="e01ec-111">**Modulis** – Sandėlio valdymas</span><span class="sxs-lookup"><span data-stu-id="e01ec-111">**Module** - Warehouse management</span></span>
- <span data-ttu-id="e01ec-112">**Funkcijos pavadinimas** – apdoroti sandėlio programos įvykius</span><span class="sxs-lookup"><span data-stu-id="e01ec-112">**Feature name** - Process warehouse app events</span></span>

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a><span data-ttu-id="e01ec-113">Sandėlio programos įvykių apdorojimo paketinės užduoties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e01ec-113">Set up a batch job to process warehouse app events</span></span>

### <a name="process-warehouse-app-events"></a><span data-ttu-id="e01ec-114">Apdoroti sandėlio programos įvykius</span><span class="sxs-lookup"><span data-stu-id="e01ec-114">Process warehouse app events</span></span>

<span data-ttu-id="e01ec-115">Sukonfigūruokite suplanuotą paketinę užduotį sandėlio programos įvykių apdorojimui kuriant perkėlimo užsakymą ir atnaujinant eilutes.</span><span class="sxs-lookup"><span data-stu-id="e01ec-115">Set up a scheduled batch job to process the warehouse app events for the transfer order creation and line updates.</span></span>

1. <span data-ttu-id="e01ec-116">Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Apdoroti sandėlio programos įvykius**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-116">Go to **Warehouse management \> Periodic tasks \> Process warehouse app events**.</span></span>
1. <span data-ttu-id="e01ec-117">Atidaromas sandėlio programos įvykių apdorojimo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="e01ec-117">The Process warehouse app events dialog box opens.</span></span> <span data-ttu-id="e01ec-118">Išplėskite „FastTab“ **Vykdyti fone** ir nustatykite **Paketinis apdorojimas** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-118">Expand the **Run in background** FastTab and set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="e01ec-119">**Vykdyti fone** „FastTab“, pasirinkite **Pakartojimas**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-119">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="e01ec-120">**Nustatyti pakartojimą** langas atsidaro.</span><span class="sxs-lookup"><span data-stu-id="e01ec-120">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="e01ec-121">Vykdykite tvarkaraštį, kaip būtina jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="e01ec-121">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="e01ec-122">Pasirinkite **Gerai**, kad sugrįžtumėte į dialogo langą **Apdoroti sandėlio programos įvykius**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-122">Select **OK** to return to the **Process warehouse app events** dialog box.</span></span>
1. <span data-ttu-id="e01ec-123">Dialogo lange **Apdoroti sandėlio programos įvykius** pasirinkite **Gerai**, kad įtrauktumėte paketinę užduotį į paketo eilę.</span><span class="sxs-lookup"><span data-stu-id="e01ec-123">Select **OK** in the **Process warehouse app events** dialog box to add the batch job to the batch queue.</span></span>

## <a name="query-warehouse-app-events"></a><span data-ttu-id="e01ec-124">Pateikite sandėlio programos įvykių užklausą</span><span class="sxs-lookup"><span data-stu-id="e01ec-124">Query warehouse app events</span></span>

<span data-ttu-id="e01ec-125">Sandėlio programos sugeneruotą įvykių eilę ir įvykių pranešimus galite peržiūrėti nuėję į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-125">You can view the event queue and events messages generated by the warehouse app by going to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>

## <a name="the-standard-event-queue-process"></a><span data-ttu-id="e01ec-126">Standartinis įvykių eilės procesas</span><span class="sxs-lookup"><span data-stu-id="e01ec-126">The standard event queue process</span></span>

<span data-ttu-id="e01ec-127">Sandėlio programos įvykių eilės apdorojimas atliekamas toliau aprašyta tvarka:</span><span class="sxs-lookup"><span data-stu-id="e01ec-127">The warehouse apps events queue will typically be used with the following described flow:</span></span>

1. <span data-ttu-id="e01ec-128">Įvykis įtraukiamas į eilę kartu su įvykio pranešimu.</span><span class="sxs-lookup"><span data-stu-id="e01ec-128">An event gets added to the queue  with an event message.</span></span> <span data-ttu-id="e01ec-129">Iš pradžių naujo pranešimo įvykio būsena yra **Laukiama**, o tai reiškia, kad paketinė užduotis **Apdoroti sandėlio programos įvykius** šio pranešimo neišrinks ir neapdoros.</span><span class="sxs-lookup"><span data-stu-id="e01ec-129">The new message initially has an Event state of **Waiting**, which means that the **Process warehouse app events** batch job will not pick up and process this message.</span></span>
1. <span data-ttu-id="e01ec-130">Iš karto, kai pranešimo būsena atnaujinama į **Eilėje**, įvykių paketinė užduotis **Apdoroti sandėlio programos įvykius** išrinks ir apdoros įvykį.</span><span class="sxs-lookup"><span data-stu-id="e01ec-130">As soon as the message state is updated to **Queued**, the **Process warehouse app** events batch job will pick up and process the event.</span></span>
1. <span data-ttu-id="e01ec-131">Priklausomai nuo to, ar reikiamą procesą buvo įmanoma atlikti, paketinė užduotis atnaujina įvykių būsenas į **Atlikta** arba **Nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-131">The batch job updates the event states to either **Completed** or **Failed**, depending on whether the requested process was possible.</span></span>
1. <span data-ttu-id="e01ec-132">Kai visų susijusių įvykio pranešimų būsena yra **Atlikta**, įvykis pašalinamas iš eilės.</span><span class="sxs-lookup"><span data-stu-id="e01ec-132">When all the related event messages are **Completed**, the event is deleted from the queue.</span></span>

 <span data-ttu-id="e01ec-133">Išsamų pavyzdį žr. [Kurti perkėlimo užsakymą naudojant sandėlio programos procesą](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="e01ec-133">For a detailed example, see [Create transfer order from warehouse app process](create-transfer-order-from-warehouse-app.md).</span></span>

## <a name="handle-event-errors"></a><span data-ttu-id="e01ec-134">Įvykio klaidų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="e01ec-134">Handle event errors</span></span>

<span data-ttu-id="e01ec-135">Atliekant sandėlio įvykių apdorojimą, reikiamai pranešimo veiklai gali nebūti suteikti paketinės užduoties procesai.</span><span class="sxs-lookup"><span data-stu-id="e01ec-135">As part of the warehouse event processing, the requested message activity may not receive processes from the batch job.</span></span> <span data-ttu-id="e01ec-136">Šiuo atveju įvykio pranešimas pasikeis į **Nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-136">In this case, the event message will change to **Failed**.</span></span> <span data-ttu-id="e01ec-137">Norėdami sužinoti priežastį ir imtis reikiamų veiksmų, kad išspręstumėte problemas, galite naudoti **paketo žurnalo** informaciją.</span><span class="sxs-lookup"><span data-stu-id="e01ec-137">You can use the **Batch log** information to learn why and take needed action to correct any problems.</span></span>

<span data-ttu-id="e01ec-138">Išsamų pavyzdį žr. [Kurti perkėlimo užsakymą naudojant sandėlio programą](create-transfer-order-from-warehouse-app.md).</span><span class="sxs-lookup"><span data-stu-id="e01ec-138">For a detailed example, see [Create transfer order from warehouse app](create-transfer-order-from-warehouse-app.md).</span></span>

<span data-ttu-id="e01ec-139">Norėdami atkurti nesėkmingo sandėlio programos įvykio pranešimą:</span><span class="sxs-lookup"><span data-stu-id="e01ec-139">To reset a failed warehouse app event message:</span></span>

1. <span data-ttu-id="e01ec-140">Eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-140">Go to **Warehouse management \> Inquiries and reports \> Mobile device logs \> Warehouse app events**.</span></span>
1. <span data-ttu-id="e01ec-141">„FastTab“ **Sandėlio programos įvykių pranešimai** suraskite ir pasirinkite atitinkamą įvykį, kurio būsena stulpelyje **Įvykio būsena** yra **Nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-141">On the **Warehouse app event messages** FastTab, find and select a relevant event that is showing **Failed** in the **Event state** column.</span></span>
1. <span data-ttu-id="e01ec-142">Įrankių juostoje **Sandėlio programos įvykių pranešimai** pasirinkite **Atkurti**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-142">Select **Reset** from the **Warehouse app event messages** toolbar.</span></span>
1. <span data-ttu-id="e01ec-143">Tęskite darbą, kol atkursite visus susijusius pranešimus.</span><span class="sxs-lookup"><span data-stu-id="e01ec-143">Continue working until all relevant messages are reset.</span></span>

<span data-ttu-id="e01ec-144">Įvykio pranešimą **Nepavyko** taip pat galite pašalinti naudodami parinktį **Naikinti**, pasiekiamą įrankių juostoje **Sandėlio programos įvykių pranešimai**.</span><span class="sxs-lookup"><span data-stu-id="e01ec-144">You can also remove a **Failed** event message by using the **Delete** option on the **Warehouse app event messages** toolbar.</span></span>
