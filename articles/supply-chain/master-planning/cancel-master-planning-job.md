---
title: Bendrojo planavimo užduoties atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti aktyvią planavimo užduotį, kurios metu naudojama integruota planavimo funkcija.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40d657a02df0cba66918a6853ec62621501cfdfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989798"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="52f16-103">Bendrojo planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="52f16-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52f16-104">Naudojant „Microsoft Dynamics 365 Supply Chain Management“, atšaukti bendrojo planavimo užduotį galima keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="52f16-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="52f16-105">Pavyzdžiui, atšaukti bendrojo planavimo užduotį galbūt norėsite tada, jei ji buvo pradėta per klaidą arba jei ji vykdoma ilgiau, nei tikėtasi, ir norite ją baigti.</span><span class="sxs-lookup"><span data-stu-id="52f16-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="52f16-106">Geriausias būdas atšaukti planavimo užduotį yra naudoti puslapį **Nebaigti planavimo procesai**.</span><span class="sxs-lookup"><span data-stu-id="52f16-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="52f16-107">Alternatyvias parinktis, esančias puslapiuose **Paketinės užduotys** ir **Patobulintos paketinės užduotys**, reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="52f16-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="52f16-108">Pageidaujama atšaukimo parinktis</span><span class="sxs-lookup"><span data-stu-id="52f16-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="52f16-109">Bendrojo planavimo užduoties atšaukimas puslapyje **Nebaigti planavimo procesai**</span><span class="sxs-lookup"><span data-stu-id="52f16-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="52f16-110">Nueikite į **Bendrasis planavimas > Užklausos ir ataskaitos > Bendrasis planavimas > Nebaigti planavimo procesai**.</span><span class="sxs-lookup"><span data-stu-id="52f16-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="52f16-111">Pasirinkite eilutę, kurioje yra norimas atšaukti planavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="52f16-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="52f16-112">Spustelėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="52f16-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="52f16-113">Papildomos atšaukimo parinktys</span><span class="sxs-lookup"><span data-stu-id="52f16-113">Additional cancel options</span></span>
<span data-ttu-id="52f16-114">Jas reikėtų naudoti, tik jei bendrojo planavimo užduotis puslapyje **Nebaigti planavimo procesai** neatšaukiama per kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="52f16-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="52f16-115">Bendrojo planavimo užduoties panaikinimas puslapyje **Paketinės užduotys**</span><span class="sxs-lookup"><span data-stu-id="52f16-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="52f16-116">Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="52f16-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="52f16-117">Pasirinkite eilutę, kurioje yra norima panaikinti planavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="52f16-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="52f16-118">Spustelėkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="52f16-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="52f16-119">Bendrojo planavimo užduoties nutraukimas puslapyje **Patobulintos paketinės užduotys**</span><span class="sxs-lookup"><span data-stu-id="52f16-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="52f16-120">Eikite į **Sistemos administravimas > Užklausos > Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="52f16-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="52f16-121">Jei sąraše užduoties ID nerodomas, spustelėkite **Perjungti į patobulintą formą**, kitu atveju pereikite prie kito veiksmo.</span><span class="sxs-lookup"><span data-stu-id="52f16-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="52f16-122">Paketinę užduotį atidarykite.</span><span class="sxs-lookup"><span data-stu-id="52f16-122">Open the batch job.</span></span> <span data-ttu-id="52f16-123">Spustelėkite paketinės užduoties, kurios elementus norite baigti, **ID**.</span><span class="sxs-lookup"><span data-stu-id="52f16-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="52f16-124">Dalyje **Paketinės užduotys** pasirinkite užduotis, kurias norite baigti.</span><span class="sxs-lookup"><span data-stu-id="52f16-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="52f16-125">Spustelėkite **Keisti būseną**, pasirinkite **Atšaukiama** ir spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="52f16-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="52f16-126">„FastTab“ konteineryje **Paketinės užduotys** spustelėkite **Nutraukti**.</span><span class="sxs-lookup"><span data-stu-id="52f16-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
