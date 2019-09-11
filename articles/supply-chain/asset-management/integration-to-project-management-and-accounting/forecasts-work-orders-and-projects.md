---
title: Prognozės, darbo užsakymai ir projektai
description: Šioje temoje aiškinamas prognozių ir darbo užsakymo integravimas su moduliu Projektų valdymas ir apskaita modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886821"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="15eeb-103">Prognozės, darbo užsakymai ir projektai</span><span class="sxs-lookup"><span data-stu-id="15eeb-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="15eeb-104">Modulyje Turto valdymas integruojama su moduliu **Projektų valdymas ir apskaita** siekiant optimizuoti išlaidų kontrolę, kad vartotojai galėtų sekti priežiūros užduočių tipo prognozių ir darbo užsakymo užduočių išlaidas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="15eeb-105">Norint sekti priežiūros užduočių tipo prognozes, būtina nustatyti toliau pateikiamus parametrus.</span><span class="sxs-lookup"><span data-stu-id="15eeb-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="15eeb-106">Pasirinkite projektą modulyje **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai** > spustelėję nuorodą **Turtas** > FastTab **Projektas** > lauke **Priežiūros prognozės projektas**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="15eeb-107">Kai dalyje **Priežiūros užduočių tipų numatytosios reikšmės** sukuriate priežiūros užduoties tipo numatytąją eilutę, automatiškai sukuriamas tos eilutės veiklos numeris (**Turto valdymas** > **Sąranką** > **Užduotys** > **Priežiūros užduočių tipo numatytieji parametrai**).</span><span class="sxs-lookup"><span data-stu-id="15eeb-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="15eeb-108">Yra dvi priežiūros užduočių tipo prognozių paskirtys: modulyje **Projektų valdymas ir apskaita** galite sekti priežiūros užduočių tipo prognozių išlaidas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="15eeb-109">Be to, prognozės automatiškai perkeliamos į darbo užsakymo užduoties projektą, kai pasirenkate darbo užsakymo užduotyje pasirenkate priežiūros užduoties tipą.</span><span class="sxs-lookup"><span data-stu-id="15eeb-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="15eeb-110">Norėdami sekti darbo užsakymų užduočių išlaidas, pirma turite nustatyti darbo užsakymų projektus. </span><span class="sxs-lookup"><span data-stu-id="15eeb-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="15eeb-111">Žr. skyrių [Darbo užsakymų projektų sąranka](../setup-for-work-orders/work-order-project-setup.md), kuriame aprašoma procedūra.</span><span class="sxs-lookup"><span data-stu-id="15eeb-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="15eeb-112">Darbo užsakymo užduočių projektai</span><span class="sxs-lookup"><span data-stu-id="15eeb-112">Work order job projects</span></span>

<span data-ttu-id="15eeb-113">Kai darbo užsakyme sukuriate darbo užsakymo užduotį, darbo užsakymo projektą nulemia darbo užsakymų pirminio projekto sąranka, pasiekiama pasirinkus **Turto valdymas** > **Sąranką** > **Darbo užsakymai** > **Projekto sąranka**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="15eeb-114">Darbo užsakymų užduočių projektai sukuriami naudojant toliau pateikiamų darbo užsakymų duomenų derinį.</span><span class="sxs-lookup"><span data-stu-id="15eeb-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="15eeb-115">Darbo užsakyme pasirinktas darbo užsakymo tipas</span><span class="sxs-lookup"><span data-stu-id="15eeb-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="15eeb-116">Su darbo užsakymo užduotyje esančiu turtu susijusi funkcinė vieta</span><span class="sxs-lookup"><span data-stu-id="15eeb-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="15eeb-117">Su darbo užsakymo užduotyje esančiu turtu susijęs turto tipas</span><span class="sxs-lookup"><span data-stu-id="15eeb-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="15eeb-118">Darbo užsakyme nustatytas numatomas pradžios ir pabaigos laikas</span><span class="sxs-lookup"><span data-stu-id="15eeb-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="15eeb-119">Gali būti, kad darbo užsakyme bus pateikta ne visa pirmiau minėta informacija.</span><span class="sxs-lookup"><span data-stu-id="15eeb-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="15eeb-120">Todėl, darbo užsakymo pirminis projektas ieškomas naudojant turimą duomenų derinį ir pasirenkant projekto ID, atitinkantį darbo užsakymo duomenis.</span><span class="sxs-lookup"><span data-stu-id="15eeb-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="15eeb-121">Pavyzdys. Toliau pateiktame paveikslėlyje turto tipo Sunkvežimio variklis sąranką reiškia, kad kiekviena sukuriama šio turto tipo darbo užsakymo užduotis bus projekto ID 000186 dalis.</span><span class="sxs-lookup"><span data-stu-id="15eeb-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![1 pav.](media/01-integration-to-pma.png)

<span data-ttu-id="15eeb-123">Darbo užsakymo užduotyje pateikiamo projekto ID ir susijusio veiklos numerio (**Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** > sąraše pasirinkite darbo užsakymą > FastTab **Eilutės informacija** > laukas **Projekto ID** ir laukas **Veiklos numeris**) paskirtis yra stebėti išlaidas, susijusias su darbo užsakymo užduotimi, ir turtą, pasirinktą darbo užsakymo užduotyje modulyje **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="15eeb-124">Toliau pateiktame paveikslėlyje matote grafinę darbo užsakymų projektų ir susijusių projektų veiklų apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="15eeb-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![2 paveikslėlis](media/02-integration-to-pma.png)

<span data-ttu-id="15eeb-126">Kai darbo užsakyme sukuriama nauja darbo užsakymo užduotis, automatiškai sukuriamas šios užduoties darbo užsakymo projektas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="15eeb-127">Su darbo užsakymo užduotimi susijusio turto finansinės dimensijos automatiškai perkeliamos į darbo užsakymo užduoties projektą.</span><span class="sxs-lookup"><span data-stu-id="15eeb-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="15eeb-128">Prie darbo užsakymo užduočiai sukurtos projekto veiklos pridedama susijusi informacija dėl priežiūros užduoties tipo, priežiūros užduoties tipo varianto ir pardavimo.</span><span class="sxs-lookup"><span data-stu-id="15eeb-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="15eeb-129">Šie duomenys naudingi jei, pavyzdžiui, kuriate darbo užsakymo pirkimo užsakymą (žr. skyrių [Įsigijimas](../work-orders/procurement.md)) arba jei naudojate modulį **Projektų valdymas ir apskaita** laikui registruoti.</span><span class="sxs-lookup"><span data-stu-id="15eeb-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="15eeb-130">Jei turtas buvo įdiegtas funkcinėje vietoje ir vėliau įdiegtas kitoje funkcinėje vietoje, turto finansinės dimensijos, susijusios su nauja funkcine vieta, automatiškai atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="15eeb-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="15eeb-131">Vėliau, kai sukuriate turto darbo užsakymo užduotį, į darbo užsakymo užduoties darbo užsakymo projektą automatiškai perkeliamos finansinės dimensijos, kurios dabar yra susijusios su turtu.</span><span class="sxs-lookup"><span data-stu-id="15eeb-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="15eeb-132">Tai reiškia, kad kai naudojate funkcines vietas, išlaidas visada galima sekti funkcinėse vietose, kuriose turtas buvo tam tikru laikotarpiu įdiegtas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="15eeb-133">Dėl automatiškai naujinamų finansinių dimensijų užtikrinamas visiškas išlaidų atsekamumas kontroliuojant projektus ir rengiant projektų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="15eeb-134">Darbo užsakymų projektai, darbo užsakymų ciklo būsenos, projekto etapai ir projektų tipai</span><span class="sxs-lookup"><span data-stu-id="15eeb-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="15eeb-135">Siekiant užtikrinti, kad darbo užsakymų ciklo būsenos ir susijusių projektų etapai darbo užsakymuose naudojami tinkamai, išnagrinėkite priklausomybes, susijusias su moduliu **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="15eeb-136">Modulio **Projektų valdymas ir apskaita** dalyje **Projektų valdymo ir apskaitos parametrai** nustatomi projektų tipų projektų etapai.</span><span class="sxs-lookup"><span data-stu-id="15eeb-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="15eeb-137">Dalyje **Projektų valdymo ir apskaitos parametrai** būtinai pasirinkite atitinkamų projektų etapų žymės langelius visuose projektų tipuose, kuriuos ketinate naudoti.</span><span class="sxs-lookup"><span data-stu-id="15eeb-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="15eeb-138">Toliau pateiktame paveikslėlyje pasirinkti penki projektų tipų Laikas ir medžiagos ir Vidinis etapai: **Sukurta** - **Numatoma** - **Suplanuotas** - **Vykdoma** - **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="15eeb-139">Šie penki etapai yra susiję ir su vidine priežiūra, ir su aptarnavimo techninės priežiūros užduotimis.</span><span class="sxs-lookup"><span data-stu-id="15eeb-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="15eeb-140">Modulyje **Turto valdymas** projektų tipai nustatomi pagal projektų grupes, kurias nustatėte formoje **Darbo užsakymų projektų sąranka** > spustelėję nuorodą **Projektų grupė**.</span><span class="sxs-lookup"><span data-stu-id="15eeb-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="15eeb-141">Projektų grupės, nustatytos formoje **Darbo užsakymų projektų sąranka**, naudojamos kuriant darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="15eeb-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="15eeb-142">Kai sukuriamas naujas darbo užsakymas, automatiškai sukuriamas darbo užsakymo darbo.</span><span class="sxs-lookup"><span data-stu-id="15eeb-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="15eeb-143">Kiekviena darbo užsakymo ciklo būsena turi būti susijusi su projekto etapu.</span><span class="sxs-lookup"><span data-stu-id="15eeb-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="15eeb-144">Projekto etapas, susijęs su darbo užsakymo ciklo būsena, turi būti apibrėžtas kaip projektų grupės, apibrėžtos darbo užsakymo projekte, aktyvusis etapas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="15eeb-145">Automatiškai sukuriamas darbo užsakymo projektas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="15eeb-146">Kai sukuriate naują darbo užsakymą, darbo užsakymo projektas automatiškai priskiriamas pagal sąranką formoje **Darbo užsakymų projektų sąranka** (**Turto valdymas** > **Sąranką** > **Darbo užsakymai** > **Projekto sąranka**).</span><span class="sxs-lookup"><span data-stu-id="15eeb-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="15eeb-147">Sąsajos tarp darbo užsakymų projektų grupių, susijusių projektų tipų, projektų etapų ir darbo užsakymų ciklų būsenų pavaizduotos toliau pateikiamuose paveikslėliuose.</span><span class="sxs-lookup"><span data-stu-id="15eeb-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![3 paveikslėlis](media/03-integration-to-pma.png)

![4 paveikslėlis](media/04-integration-to-pma.png)

![5 paveikslėlis](media/05-integration-to-pma.png)

<span data-ttu-id="15eeb-151">Žr. skyrių [Darbo užsakymų projektų sąranka](../setup-for-work-orders/work-order-project-setup.md), norėdami sužinoti, kaip nustatyti darbo užsakymų projektus, ir skyrių [Darbo užsakymų ciklo būsenos](../setup-for-work-orders/work-order-lifecycle-states.md), norėdami sužinoti, kaip kurti darbo užsakymų ciklo būsenas.</span><span class="sxs-lookup"><span data-stu-id="15eeb-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="15eeb-152">Toliau pateikiamame paveikslėlyje pavaizduota grafinė įvairių projektų, kuriamų modulyje **Turto valdymas**, norint integruoti su moduliu **Projektų valdymas ir apskaita**, ir darbo procesų, su kuriais minėti projektai yra susiję, apžvalga.</span><span class="sxs-lookup"><span data-stu-id="15eeb-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![6 paveikslėlis](media/06-integration-to-pma.png)

