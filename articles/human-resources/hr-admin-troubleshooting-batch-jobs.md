---
title: Optimizuokite našumą suplanuodami paketines užduotis po valandų
description: Šioje temoje paaiškinama, kaip išspręsti konkrečias našumo problemas naudojant „Microsoft Dynamics 365 Human Resources“, suplanuojant ilgai veikiančias paketines užduotis po valandų.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500510"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="5f462-103">Optimizuokite našumą suplanuodami paketines užduotis po valandų</span><span class="sxs-lookup"><span data-stu-id="5f462-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="5f462-104">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="5f462-104">Issue</span></span>

<span data-ttu-id="5f462-105">„Microsoft Dynamics 365 Human Resources” gali išbandyti našumo problemas, jei ilgai trunkančios paketinės užduotys vykdomos įprastu darbo laiku.</span><span class="sxs-lookup"><span data-stu-id="5f462-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f462-106">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="5f462-106">Resolution</span></span>

<span data-ttu-id="5f462-107">Suplanuokite šias paketines užduotis nedarbo valandomis.</span><span class="sxs-lookup"><span data-stu-id="5f462-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="5f462-108">Taip pat rekomenduojame peržiūrėti dažnai vykdomų paketinių užduočių dažnumą.</span><span class="sxs-lookup"><span data-stu-id="5f462-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="5f462-109">Jei įmanoma, sumažinkite paketinės užduoties pasikartojimą.</span><span class="sxs-lookup"><span data-stu-id="5f462-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="5f462-110">Daugeliu atvejų numatytasis dažnumas yra tinkamas.</span><span class="sxs-lookup"><span data-stu-id="5f462-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="5f462-111">Šios paketinės užduotys turėtų būti vykdomos naktį arba po valandų.</span><span class="sxs-lookup"><span data-stu-id="5f462-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="5f462-112">Būtinai patikrinkite laiko juostą šioms pasikartojančioms paketinėms užduotims.</span><span class="sxs-lookup"><span data-stu-id="5f462-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="5f462-113">Kai kurios paketinės užduotys gali naudoti Ramiojo vandenyno standartinį laiką (PST).</span><span class="sxs-lookup"><span data-stu-id="5f462-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="5f462-114">Paketinė užduotis</span><span class="sxs-lookup"><span data-stu-id="5f462-114">Batch job</span></span> | <span data-ttu-id="5f462-115">Numatytasis pasirodymas</span><span class="sxs-lookup"><span data-stu-id="5f462-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="5f462-116">Paketinės užduoties istorijos valymas</span><span class="sxs-lookup"><span data-stu-id="5f462-116">Batch job history cleanup</span></span> | <span data-ttu-id="5f462-117">1 kartą per mėnesį</span><span class="sxs-lookup"><span data-stu-id="5f462-117">1 time per month</span></span> |
| <span data-ttu-id="5f462-118">Eksportavimo išdėstymo valymas</span><span class="sxs-lookup"><span data-stu-id="5f462-118">Export staging cleanup</span></span> | <span data-ttu-id="5f462-119">1 kartą per dieną</span><span class="sxs-lookup"><span data-stu-id="5f462-119">1 time per day</span></span> |
| <span data-ttu-id="5f462-120">„Common Data Service“ integracijoje trūksta užklausos sinchronizavimo</span><span class="sxs-lookup"><span data-stu-id="5f462-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="5f462-121">1 kartą per dieną</span><span class="sxs-lookup"><span data-stu-id="5f462-121">1 time per day</span></span> |
| <span data-ttu-id="5f462-122">Duomenų bazės glaudinimo sistemos užduotis, kurią reikia reguliariai vykdyti nedarbo valandomis</span><span class="sxs-lookup"><span data-stu-id="5f462-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="5f462-123">1 kartą per dieną</span><span class="sxs-lookup"><span data-stu-id="5f462-123">1 time per day</span></span> |
| <span data-ttu-id="5f462-124">Duomenų bazės indekso atkūrimo sistemos užduotis, kurią reikia reguliariai vykdyti nedarbo valandomis</span><span class="sxs-lookup"><span data-stu-id="5f462-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="5f462-125">1 kartą per dieną</span><span class="sxs-lookup"><span data-stu-id="5f462-125">1 time per day</span></span> |

1. <span data-ttu-id="5f462-126">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="5f462-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="5f462-127">**Ieška** juostoje ieškokite vienos iš aukščiau nurodytų paketinių užduočių.</span><span class="sxs-lookup"><span data-stu-id="5f462-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="5f462-128">Pasirinkite **Vykdyti fone**, tada pasirinkite **Pasikartojimas**.</span><span class="sxs-lookup"><span data-stu-id="5f462-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Pasikartojimo nustatymas](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="5f462-130">Po **Apibrėžti pasikartojimą** nustatykite **Pradžios datą** ir **Pradžios laiką**, kad pasirodytų nedarbo valandomis arba savaitgalį.</span><span class="sxs-lookup"><span data-stu-id="5f462-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="5f462-131">Pasirinkite **Nėra pabaigos datos**.</span><span class="sxs-lookup"><span data-stu-id="5f462-131">Select **No end date**.</span></span> 

   ![Pasikartojimo pradžios datos ir laiko nurodymas](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="5f462-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5f462-133">Select **OK**.</span></span>

6. <span data-ttu-id="5f462-134">Jei būtina, pakeiskite parametrus **Vykdyti fone** dalyje ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5f462-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f462-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5f462-135">Additional resources</span></span>

[<span data-ttu-id="5f462-136">Efektyvumo optimizavimas naudojant automatinio valymo užduotis</span><span class="sxs-lookup"><span data-stu-id="5f462-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)