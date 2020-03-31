---
title: Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas
description: Šiame straipsnyje aiškinama, kaip įrašyti užduoties vedlius į „Microsoft Dynamics Lifecycle Services“ (LCS) ir leisti juos pakartotinai.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b55937c0867117809471f50f1987f7bf12a4b25d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010010"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="07949-103">Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas</span><span class="sxs-lookup"><span data-stu-id="07949-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="07949-104">**Aplinkos informacija**</span><span class="sxs-lookup"><span data-stu-id="07949-104">**Environment details**</span></span> 

<span data-ttu-id="07949-105">„Microsoft Dynamics 365 Human Resources“, įdiegtas naudojant „Microsoft Dynamics Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="07949-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="07949-106">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="07949-106">**Issue**</span></span>

<span data-ttu-id="07949-107">Klientas nori įrašyti naują užduoties įrašą į savo LCS projektą, tada pakartotinai leisti įrašytus užduoties vedlius.</span><span class="sxs-lookup"><span data-stu-id="07949-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="07949-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="07949-108">**Resolution**</span></span>

<span data-ttu-id="07949-109">Norėdami įrašyti užduoties įrašą į LCS, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07949-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="07949-110">Prisijunkite prie LCS ir pasirinkite projektą.</span><span class="sxs-lookup"><span data-stu-id="07949-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="07949-111">Pasirinkite plytelę **Verslo procesų modeliavimo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="07949-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="07949-112">Peržiūrėti puslapį atnaujintoje BPM programoje.</span><span class="sxs-lookup"><span data-stu-id="07949-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="07949-113">Pasirinkite biblioteką, tada – **Kopijuoti**.</span><span class="sxs-lookup"><span data-stu-id="07949-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="07949-114">Įveskite Verslo procesų modeliavimo įrankio (BPM) modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07949-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="07949-115">Prisijunkite prie „Human Resources“ iš LCS.</span><span class="sxs-lookup"><span data-stu-id="07949-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="07949-116">Lauke **Ieškoti** įveskite **žinynas**.</span><span class="sxs-lookup"><span data-stu-id="07949-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="07949-117">Bus atidarytas „Lifecycle Services“ žinynas.</span><span class="sxs-lookup"><span data-stu-id="07949-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="07949-118">Pasirinkite mygtuką **Atnaujinti**, kad galėtumėte konfigūruoti „Lifecycle Services“ žinyną.</span><span class="sxs-lookup"><span data-stu-id="07949-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="07949-119">Turėtų būti rodoma jūsų nauja BPM biblioteka. Ji turėtų būti aktyvi.</span><span class="sxs-lookup"><span data-stu-id="07949-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="07949-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="07949-120">Close the page.</span></span>
10. <span data-ttu-id="07949-121">Sukurkite užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="07949-121">Create a task recording.</span></span>
11. <span data-ttu-id="07949-122">Baigę pasirinkite **Įrašyti į „Lifecycle Services“**.</span><span class="sxs-lookup"><span data-stu-id="07949-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Įrašyti į „Lifecycle Services“](media/task-guides.png)

12. <span data-ttu-id="07949-124">Pasirinkite BPM biblioteką ir mazgą, į kuriuos norite įrašyti užduoties įrašą.</span><span class="sxs-lookup"><span data-stu-id="07949-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="07949-125">Norėdami pakartotinai paleisti LCS užduoties vedlį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07949-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="07949-126">Paleiskite užduočių įrašymo priemonę.</span><span class="sxs-lookup"><span data-stu-id="07949-126">Start Task recorder.</span></span>
2. <span data-ttu-id="07949-127">Pasirinkite **Atidaryti iš LCS**.</span><span class="sxs-lookup"><span data-stu-id="07949-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="07949-128">Pasirinkite biblioteką ir BPM mazgą, kuriame yra įrašytas užduoties vedlys.</span><span class="sxs-lookup"><span data-stu-id="07949-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="07949-129">Atidarykite užduoties vedlį.</span><span class="sxs-lookup"><span data-stu-id="07949-129">Open the task guide.</span></span>