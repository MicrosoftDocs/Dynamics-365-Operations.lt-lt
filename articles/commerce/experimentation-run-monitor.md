---
title: Eksperimento vykdymas ir stebėjimas
description: Šioje temoje aprašoma, kaip vykdyti ir stebėti eksperimentą trečiosios šalies paslaugoje. Taip pat aprašoma, kaip atlikti variacijų keitimus po to, kai eksperimentas pradėtas.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ee86a6761b27f3c08a65a2e250659cdcfd71db44
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097027"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="4cee4-104">Eksperimento vykdymas ir stebėjimas</span><span class="sxs-lookup"><span data-stu-id="4cee4-104">Run and monitor an experiment</span></span>

<span data-ttu-id="4cee4-105">Šioje temoje aprašoma, kaip vykdyti ir stebėti jūsų eksperimentą trečiosios šalies programoje ir kaip atlikti variacijų keitimus, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="4cee4-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="4cee4-106">Prieš atlikdami šioje temoje aprašytus veiksmus, pirmiausia turite [publikuoti](experimentation-preview-publish.md) jūsų eksperimentą „Commerce”.</span><span class="sxs-lookup"><span data-stu-id="4cee4-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="4cee4-107">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="4cee4-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4cee4-108">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="4cee4-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="4cee4-109">[ ![Vartotojo eksperimentavimo kelionė – vykdymas ir stebėjimas](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="4cee4-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="4cee4-110">Publikavus jūsų variacijas, visi veiksmai, kuriuos reikia atlikti „Commerce”, kad jūsų eksperimentas būtų vykdomas, yra baigti.</span><span class="sxs-lookup"><span data-stu-id="4cee4-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="4cee4-111">Kitas veiksmas – nustatyti, kurią variaciją parodyti kiekvienam vartotojui, reikalaujančiam puslapio.</span><span class="sxs-lookup"><span data-stu-id="4cee4-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="4cee4-112">Šį nustatymą atlieka trečiosios šalies paslauga, bet pirmiausia jūs turite suaktyvinti eksperimentą paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="4cee4-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="4cee4-113">Kadangi eksperimento aktyvavimo veiksmai priklauso nuo paslaugos, turite sekti instrukcijas, įtrauktas kartu su jūsų paslauga ar tiekėju.</span><span class="sxs-lookup"><span data-stu-id="4cee4-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="4cee4-114">Jei eksperimentas nesuaktyvintas, vartotojai matys tik numatytąją puslapio versiją (variacijos nebus rodomos).</span><span class="sxs-lookup"><span data-stu-id="4cee4-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="4cee4-115">Jums reikės vykdyti eksperimentą tiek laiko, kad būtų surinkti statistiškai tinkamų rezultatų duomenys.</span><span class="sxs-lookup"><span data-stu-id="4cee4-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="4cee4-116">Naudokite trečiosios šalies paslaugą, norėdami stebėti su eksperimentu susijusius duomenis ir analizę eksperimento vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="4cee4-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="4cee4-117">Jūsų variacijų koregavimas</span><span class="sxs-lookup"><span data-stu-id="4cee4-117">Adjust your variations</span></span>
<span data-ttu-id="4cee4-118">Jei dėl kokių nors priežasčių reikia koreguoti jūsų variacijas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4cee4-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cee4-119">Jei atliekate aktyvaus eksperimento keitimus „Commerce” arba trečiosios šalies paslaugoje, rezultatai gali būti reikšmingai paveikti.</span><span class="sxs-lookup"><span data-stu-id="4cee4-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="4cee4-120">Apsvarstykite galimybę leisti eksperimentui įvykti ir tada sukurti naują didelių pakeitimų eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="4cee4-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="4cee4-121">„Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="4cee4-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="4cee4-122">Pasirinkite norimą atnaujinti variaciją iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="4cee4-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="4cee4-123">Atlikite reikiamus keitimus, tada peržiūrėkite ir publikuokite variacijas.</span><span class="sxs-lookup"><span data-stu-id="4cee4-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="4cee4-124">Daugiau informacijos žr. [Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="4cee4-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="4cee4-125">Norėdami atlikti bet kokius su eksperimento nustatymu susijusius keitimus, eikite į trečiosios šalies paslaugą.</span><span class="sxs-lookup"><span data-stu-id="4cee4-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="4cee4-126">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="4cee4-126">Previous step</span></span>
[<span data-ttu-id="4cee4-127">Eksperimento peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="4cee4-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="4cee4-128">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="4cee4-128">Next step</span></span>
[<span data-ttu-id="4cee4-129">Variacijos skatinimas ir eksperimento užbaigimas</span><span class="sxs-lookup"><span data-stu-id="4cee4-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
