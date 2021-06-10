---
title: Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas
description: Šiame straipsnyje aiškinama, kaip įrašyti užduoties vedlius į „Microsoft Dynamics Lifecycle Services“ (LCS) ir leisti juos pakartotinai.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053280"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="3cf9b-103">Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas</span><span class="sxs-lookup"><span data-stu-id="3cf9b-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3cf9b-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="3cf9b-104">**Environment details**</span></span> 

<span data-ttu-id="3cf9b-105">„Microsoft Dynamics 365 Human Resources“, įdiegtas naudojant „Microsoft Dynamics Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="3cf9b-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="3cf9b-106">**Išdavimas**</span><span class="sxs-lookup"><span data-stu-id="3cf9b-106">**Issue**</span></span>

<span data-ttu-id="3cf9b-107">Klientas nori įrašyti naują užduoties įrašą į savo LCS projektą, tada pakartotinai leisti įrašytus užduoties vedlius.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-107">The customer wants to save new task recordings to the LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="3cf9b-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="3cf9b-108">**Resolution**</span></span>

<span data-ttu-id="3cf9b-109">Norėdami įrašyti užduoties įrašą į LCS, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="3cf9b-110">Prisijunkite prie LCS ir pasirinkite projektą.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="3cf9b-111">Pasirinkite plytelę **Verslo procesų modeliavimo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="3cf9b-112">Peržiūrėti puslapį atnaujintoje BPM programoje.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="3cf9b-113">Pasirinkite biblioteką, tada – **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="3cf9b-114">Įveskite Verslo procesų modeliavimo įrankio (BPM) modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="3cf9b-115">Prisijunkite prie „Human Resources“ iš LCS.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="3cf9b-116">Lauke **Ieškoti** įveskite **žinynas**.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="3cf9b-117">Bus atidarytas „Lifecycle Services“ žinynas.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="3cf9b-118">Pasirinkite mygtuką **Atnaujinti**, kad galėtumėte konfigūruoti „Lifecycle Services“ žinyną.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="3cf9b-119">Turėtų būti rodoma jūsų nauja BPM biblioteka. Ji turėtų būti aktyvi.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="3cf9b-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-120">Close the page.</span></span>
10. <span data-ttu-id="3cf9b-121">Sukurkite užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-121">Create a task recording.</span></span>
11. <span data-ttu-id="3cf9b-122">Baigę pasirinkite **Įrašyti į „Lifecycle Services“**.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Įrašyti į „Lifecycle Services“](media/task-guides.png)

12. <span data-ttu-id="3cf9b-124">Pasirinkite BPM biblioteką ir mazgą, į kuriuos norite įrašyti užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="3cf9b-125">Norėdami pakartotinai paleisti LCS užduoties vedlį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="3cf9b-126">Paleiskite užduočių įrašymo priemonę.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-126">Start Task recorder.</span></span>
2. <span data-ttu-id="3cf9b-127">Pasirinkite **Atidaryti iš LCS**.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="3cf9b-128">Pasirinkite biblioteką ir BPM mazgą, kuriame yra įrašytas užduoties vedlys.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="3cf9b-129">Atidarykite užduoties vedlį.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]