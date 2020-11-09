---
title: Eksperimentavimas „Dynamics 365 Commerce”
description: Eksperimentavimas leidžia kurti, redaguoti ir valdyti puslapio maketų bei turinio apdorojimo būdus svetainių daryklėje. Palaikomas visapusis eksperimentavimas el. prekybos puslapiuose ir puslapyje esančiuose objektuose.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 8b2e97167d12b8ceecf72af075ee0362101c4fa0
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930255"
---
# <a name="experimentation-in-dynamics-365-commerce"></a><span data-ttu-id="81ff3-104">Eksperimentavimas „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="81ff3-104">Experimentation in Dynamics 365 Commerce</span></span>
<span data-ttu-id="81ff3-105">Naudokite „Dynamics 365 Commerce” eksperimentavimą, norėdami patvirtinti jūsų „e-Commerce” puslapių efektyvumo hipotezes ir priimti patikimus, duomenimis pagrįstus sprendimus.</span><span class="sxs-lookup"><span data-stu-id="81ff3-105">Use experimentation in Dynamics 365 Commerce to validate hypotheses about the effectiveness of your e-Commerce pages and make decisions with data-driven confidence.</span></span> <span data-ttu-id="81ff3-106">„Commerce” palaiko A / B tikrinimą puslapiuose, moduliuose ir fragmentuose bei leidžia įvertinti siūlomų svetainės pakeitimų poveikį.</span><span class="sxs-lookup"><span data-stu-id="81ff3-106">Commerce supports A/B testing on pages, modules, and fragments and enables you to measure the impact of proposed changes to your website.</span></span>

<span data-ttu-id="81ff3-107">Svetainių daryklėje galite kurti, redaguoti ir valdyti puslapių bei turinio apdorojimo būdus, vadinamus **variacijomis**.</span><span class="sxs-lookup"><span data-stu-id="81ff3-107">You can create, edit, and manage page and content treatments known as **variations** in site builder.</span></span> <span data-ttu-id="81ff3-108">„Commerce” integruojama su trečiųjų šalių paslaugomis, kurias galite naudoti eksperimentams ir apdorojimo užduotims kurti.</span><span class="sxs-lookup"><span data-stu-id="81ff3-108">Commerce integrates with third-party services that you can use to create experiments and treatment assignments.</span></span> <span data-ttu-id="81ff3-109">„Commerce” užfiksuoti realiojo laiko įvykių srautai leidžia atlikti analizę, nurodančią eksperimento rezultatus trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="81ff3-109">Real-time event streams captured in Commerce enable the analytics that define the experiment results in the third-party service.</span></span> <span data-ttu-id="81ff3-110">Tada galite panaudoti šią analizę, norėdami patvirtinti arba paneigti jūsų hipotezę.</span><span class="sxs-lookup"><span data-stu-id="81ff3-110">You can then leverage these analytics to help support or refute your hypothesis.</span></span>

## <a name="set-up-prerequisites"></a><span data-ttu-id="81ff3-111">Būtinųjų sąlygų nustatymas</span><span class="sxs-lookup"><span data-stu-id="81ff3-111">Set up prerequisites</span></span>
1. <span data-ttu-id="81ff3-112">**Gaukite tinkamą „Commerce” versiją** – atnaujinkite jūsų modulių biblioteką, interneto kanalo SDK išplečiamumą ir „Commerce Scale Unit” į „Commerce” 10.0.13 arba naujesnę versiją.</span><span class="sxs-lookup"><span data-stu-id="81ff3-112">**Get the correct version of Commerce** - Upgrade your module library, online channel extensibility SDK, and Commerce scale unit to Commerce version 10.0.13 or later.</span></span>
1. <span data-ttu-id="81ff3-113">**Nustatykite eksperimento jungtį** – eksperimento jungtis leidžia „Commerce” prisijungti prie trečiųjų šalių paslaugų ir gauti eksperimentų sąrašą siekiant nustatyti, kada vartotojui parodyti eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="81ff3-113">**Set up an experimentation connector** - An experimentation connector allows Commerce to connect with third-party services to retrieve the list of experiments and determine when to show an experiment to a user.</span></span> <span data-ttu-id="81ff3-114">Galite įsigyti trečiosios šalies jungtį iš [„AppSource”](https://appsource.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="81ff3-114">You can purchase a third-party connector from [AppSource](https://appsource.microsoft.com).</span></span> <span data-ttu-id="81ff3-115">Sekite leidėjo pateiktas nustatymo instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="81ff3-115">Follow the setup instructions provided by the publisher.</span></span> <span data-ttu-id="81ff3-116">Taip pat galite naudoti „Commerce” bandymo jungtį, norėdami patikrinti eksperimento darbo eigą, nekonfigūruodami išorinės paslaugos.</span><span class="sxs-lookup"><span data-stu-id="81ff3-116">You can alternatively use the sample test connector from Commerce to test the experimentation workflow without needing to configure an external service.</span></span> <span data-ttu-id="81ff3-117">Daugiau informacijos žr. [Jungčių konfigūravimas ir įjungimas](e-commerce-extensibility/connectors.md).</span><span class="sxs-lookup"><span data-stu-id="81ff3-117">For more information, see [Configure and enable connectors](e-commerce-extensibility/connectors.md).</span></span> 
1. <span data-ttu-id="81ff3-118">**Įjunkite eksperimentavimo funkcijų vėliavėles „Commerce”** – galite įjungti eksperimentavimą nuomotojo lygiu, nuėję į **Nuomotojo parametrai > Funkcijos**, arba svetainės lygiu, nuėję į **Svetainės parametrai > Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="81ff3-118">**Turn on the experimentation feature flags in Commerce** - You can enable experimentation at the tenant level by going to **Tenant Settings > Features** or at the site level at **Site Settings > Features**.</span></span>
    - <span data-ttu-id="81ff3-119">Įjunkite vėliavėlę **Eksperimentavimas**, norėdami sukurti puslapyje esančių modulių eksperimento variacijas, nepaveikdami ar nekopijuodami kito turinio, kuris nėra eksperimento dalis.</span><span class="sxs-lookup"><span data-stu-id="81ff3-119">Enable the **Experimentation** flag to create experiment variations of modules within a page without affecting or copying other content that isn't part of the experiment.</span></span> <span data-ttu-id="81ff3-120">Tai užtikrina, kad vykdomi turinio naujinimai ne eksperimente liks sinchronizuoti eksperimento ciklo metu.</span><span class="sxs-lookup"><span data-stu-id="81ff3-120">This ensures that ongoing content updates outside the experiment stay in sync during the experiment lifecycle.</span></span> <span data-ttu-id="81ff3-121">Išjungus šią vėliavėlę, sustabdomas visų eksperimentų rodymas vartotojams ir pašalinamos visos svetainių daryklės redagavimo funkcijos.</span><span class="sxs-lookup"><span data-stu-id="81ff3-121">Disabling this flag stops all experiments from being shown to users and removes all editing functions within site builder.</span></span>
    - <span data-ttu-id="81ff3-122">Įjunkite vėliavėlę **Puslapių ar fragmentų eksperimentų vykdymas**, norėdami vykdyti puslapio ar fragmento eksperimentus.</span><span class="sxs-lookup"><span data-stu-id="81ff3-122">Enable the **Experiment on pages or fragments** flag to run experiments on a page or fragment.</span></span> <span data-ttu-id="81ff3-123">Tai sukuria visą visų modulių, esančių puslapyje arba fragmente, puslapio arba fragmento egzemplioriaus kopiją.</span><span class="sxs-lookup"><span data-stu-id="81ff3-123">This creates a full instance copy of the entire page or fragment for all modules within the page or fragment.</span></span> <span data-ttu-id="81ff3-124">Naudokite šį režimą, kai norite tikrinti išsamius turinio keitimus arba kai vykdomų turinio pakeitimų sinchronizavimas egzemplioriuose nėra problema.</span><span class="sxs-lookup"><span data-stu-id="81ff3-124">Use this mode when you want to test comprehensive content changes, or where synchronizing ongoing content changes across instances isn't a concern.</span></span> <span data-ttu-id="81ff3-125">Išjungus šią vėliavėlę, neleidžiama kurti ir redaguoti naujų puslapių ir fragmentų eksperimentų.</span><span class="sxs-lookup"><span data-stu-id="81ff3-125">Disabling this flag prevents creation and editing of new experiments on pages and fragments.</span></span>
    > [!NOTE]
    > <span data-ttu-id="81ff3-126">Vėliavėlė **Eksperimentavimas** turi būti įjungta, kad veiktų funkcija **Puslapių ar fragmentų eksperimentų vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="81ff3-126">The **Experimentation** flag must also be enabled for the **Experiment on pages or fragments** functionality to work.</span></span>
    
## <a name="experimentation-lifecycle"></a><span data-ttu-id="81ff3-127">Eksperimento ciklas</span><span class="sxs-lookup"><span data-stu-id="81ff3-127">Experimentation lifecycle</span></span>
<span data-ttu-id="81ff3-128">Eksperimento nustatymas, variacijų kūrimas ir eksperimento vykdymas yra kartotinis procesas.</span><span class="sxs-lookup"><span data-stu-id="81ff3-128">Setting up an experiment, creating variations, and running an experiment is an iterative process.</span></span> <span data-ttu-id="81ff3-129">Toliau pateiktoje diagramoje rodomas eksperimento ciklas „Commerce” ir trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="81ff3-129">The diagram below illustrates the experimentation lifecycle in Commerce and the third-party service.</span></span> 

<span data-ttu-id="81ff3-130">[ ![Eksperimento ciklas](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="81ff3-130">[ ![Experimentation lifecycle](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span></span>

<span data-ttu-id="81ff3-131">Norėdami sužinoti daugiau apie kiekvieną eksperimentavimo proceso veiksmą, žr. toliau pateiktas temas.</span><span class="sxs-lookup"><span data-stu-id="81ff3-131">To learn more about each step in the experimentation process, refer to the following topics.</span></span>
- [<span data-ttu-id="81ff3-132">Eksperimento hipotezės ir metrikos nustatymas</span><span class="sxs-lookup"><span data-stu-id="81ff3-132">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md)
- [<span data-ttu-id="81ff3-133">Eksperimento nustatymas</span><span class="sxs-lookup"><span data-stu-id="81ff3-133">Set up an experiment</span></span>](experimentation-setup.md)
- [<span data-ttu-id="81ff3-134">Eksperimento prijungimas ir redagavimas</span><span class="sxs-lookup"><span data-stu-id="81ff3-134">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
- [<span data-ttu-id="81ff3-135">Eksperimento peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="81ff3-135">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
- [<span data-ttu-id="81ff3-136">Eksperimento vykdymas ir stebėjimas</span><span class="sxs-lookup"><span data-stu-id="81ff3-136">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
- [<span data-ttu-id="81ff3-137">Variacijos skatinimas ir eksperimento užbaigimas</span><span class="sxs-lookup"><span data-stu-id="81ff3-137">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)

> [!NOTE]
> <span data-ttu-id="81ff3-138">Norėdami sužinoti, kurioje ciklo vietoje yra eksperimentas, eikite į skirtuką **Eksperimentai** svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="81ff3-138">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="81ff3-139">Rodomas eksperimentų sąrašas su kiekvieno eksperimento būsena „Commerce” ir trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="81ff3-139">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service.</span></span> <span data-ttu-id="81ff3-140">Daugiau informacijos žr. [Eksperimento būsenos peržiūra](experimentation-status.md).</span><span class="sxs-lookup"><span data-stu-id="81ff3-140">For more information, see [Review the status of an experiment](experimentation-status.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="81ff3-141">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="81ff3-141">Next step</span></span>
[<span data-ttu-id="81ff3-142">Eksperimento hipotezės ir sėkmės metrikos nustatymas</span><span class="sxs-lookup"><span data-stu-id="81ff3-142">Identify a hypothesis and determine success metrics for an experiment</span></span>](experimentation-identify.md) 