---
title: Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft“ „Dynamics 365 Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Dynamics 365 Finance“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770294"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="51526-103">Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="51526-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="51526-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Dynamics 365 Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="51526-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiami 8.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="51526-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="51526-106">Faktinių duomenų integravimas pasiekiamas 8.0.1 arba naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="51526-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="51526-107">„Project Service Automation“ duomenų srautas į „Finance“</span><span class="sxs-lookup"><span data-stu-id="51526-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="51526-108">Sprendime „Project Service Automation“ ir „Finance“ integravimas naudojama duomenų sinchronizavimo funkcija duomenims „Project Service Automation“ ir „Finance“ egzemplioriuose sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="51526-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="51526-109">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie apytiksles projekto grafiko ir projekto išlaidų reikšmes srautas iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="51526-110">Toliau esančiame paveikslėlyje pavaizduotas duomenų sinchronizavimas tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="51526-111">[![„Project Service Automation“ integravimo su „Finance“ duomenų srautas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="51526-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="51526-112">Apytikslės projekto grafiko reikšmės</span><span class="sxs-lookup"><span data-stu-id="51526-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="51526-113">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="51526-113">Template and tasks</span></span>

<span data-ttu-id="51526-114">Norėdami atidaryti pasiekiamus šablonus, „Microsoft Power Apps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="51526-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="51526-115">Toliau pateiktas šablonas ir pagrindinės užduotys naudojami sinchronizuojant apytiksles „Project Service Automation“ projekto grafiko reikšmes su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="51526-116">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto grafiko reikšmės (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="51526-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="51526-117">**Užduočių pavadinimas projekte**</span><span class="sxs-lookup"><span data-stu-id="51526-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="51526-118">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="51526-118">Transaction relationships</span></span>
    - <span data-ttu-id="51526-119">Numatomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="51526-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="51526-120">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="51526-120">Entity set</span></span>

| <span data-ttu-id="51526-121">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="51526-121">Project Service Automation</span></span> | <span data-ttu-id="51526-122">Finansai</span><span class="sxs-lookup"><span data-stu-id="51526-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="51526-123">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="51526-123">Project tasks</span></span>              | <span data-ttu-id="51526-124">Projekto valandų įvertinimo duomenų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="51526-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="51526-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="51526-125">Entity flow</span></span>

<span data-ttu-id="51526-126">Apytikslės projekto grafiko reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance“ kaip projekto grafiko prognozės.</span><span class="sxs-lookup"><span data-stu-id="51526-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="51526-127">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="51526-127">Prerequisites</span></span>

<span data-ttu-id="51526-128">Prieš sinchronizavimą projekto valandų įvertinimo gali atsirasti, galite sinchronizuoti projektus, projekto užduotims ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="51526-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="51526-129">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="51526-129">Power Query</span></span>

<span data-ttu-id="51526-130">Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto grafiko reikšmių šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.</span><span class="sxs-lookup"><span data-stu-id="51526-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="51526-131">Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="51526-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="51526-132">Filtruoti visus užduotyje esančius konkretaus ištekliaus įrašus, dėl kurių galėtų nepavykti integravimas į grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="51526-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="51526-133">Filtruoti visas tuščias operacijos kategorijos eilutes.</span><span class="sxs-lookup"><span data-stu-id="51526-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="51526-134">Nepavykus atlikti užduoties, gali būti pateikiamos klaidingos grafikų prognozės.</span><span class="sxs-lookup"><span data-stu-id="51526-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="51526-135">Nustatyti numatytąjį prognozės modelio ID</span><span class="sxs-lookup"><span data-stu-id="51526-135">Set the default forecast model ID</span></span>

<span data-ttu-id="51526-136">Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="51526-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="51526-137">Tada pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="51526-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="51526-138">Jei naudojate numatytąjį apytikslių „Microsoft Project“ grafiko reikšmių (iš PSA į „Fin and Ops“) šabloną, sąraše **Pritaikyti veiksmai** paspauskite **Įterpta sąlyga**.</span><span class="sxs-lookup"><span data-stu-id="51526-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="51526-139">Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="51526-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="51526-140">Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="51526-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="51526-141">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="51526-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="51526-142">Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="51526-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="51526-143">Įveskite stulpelio sąlygą: jei projekto užduotis apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.</span><span class="sxs-lookup"><span data-stu-id="51526-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="51526-144">Filtruoti tam tikro ištekliaus įrašus</span><span class="sxs-lookup"><span data-stu-id="51526-144">Filter out resource-specific records</span></span>

<span data-ttu-id="51526-145">Apytikslių projekto grafiko reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo naudojantis pašalinami visi konkretaus ištekliaus įrašai.</span><span class="sxs-lookup"><span data-stu-id="51526-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="51526-146">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="51526-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="51526-147">Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad filtruotumėte stulpelį **msdyn\_islinetask**, kad būtų įtraukiami tik užrašu **Klaidinga** pažymėti įrašai.</span><span class="sxs-lookup"><span data-stu-id="51526-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="51526-148">Tuščių operacijos kategorijos eilučių filtravimas</span><span class="sxs-lookup"><span data-stu-id="51526-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="51526-149">Norėdami pašalinti visas eilutes, kurių operacijos kategorijos yra tuščios, turite įtraukti filtrą.</span><span class="sxs-lookup"><span data-stu-id="51526-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="51526-150">Šią užduotį atlikti būtina, nepriklausomai nuo to, ar naudojate numatytąjį šabloną, ar sukuriate savo šabloną.</span><span class="sxs-lookup"><span data-stu-id="51526-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="51526-151">Naudojantis šiuo filtru, iš „Project Service Automation“ pašalinamos visos santraukos eilutės, dėl kurių galėtų būti pateikiamos klaidingos „Finance“ grafikų prognozės.</span><span class="sxs-lookup"><span data-stu-id="51526-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="51526-152">Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad būtų filtruojami neapibrėžti stulpelio **msdyn\_transactioncategory\_value** įrašai.</span><span class="sxs-lookup"><span data-stu-id="51526-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="51526-153">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="51526-153">Template mapping in Data integration</span></span>

<span data-ttu-id="51526-154">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="51526-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="51526-155">Susiejime rodoma „Project Service Automation“ laukų informacija, kuri bus sinchronizuojama su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="51526-156">[![Šablono susiejimas](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="51526-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="51526-157">Apytikslės projekto išlaidų reikšmės</span><span class="sxs-lookup"><span data-stu-id="51526-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="51526-158">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="51526-158">Template and tasks</span></span>

<span data-ttu-id="51526-159">Toliau pateiktas šablonas ir pagrindinės užduotys naudojami sinchronizuojant apytiksles „Project Service Automation“ projekto grafiko reikšmes su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="51526-160">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto išlaidų reikšmės (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="51526-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="51526-161">**Užduočių pavadinimas projekte**</span><span class="sxs-lookup"><span data-stu-id="51526-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="51526-162">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="51526-162">Transaction relationships</span></span> 
    - <span data-ttu-id="51526-163">Numatomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="51526-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="51526-164">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="51526-164">Entity set</span></span>

| <span data-ttu-id="51526-165">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="51526-165">Project Service Automation</span></span> | <span data-ttu-id="51526-166">Finansai</span><span class="sxs-lookup"><span data-stu-id="51526-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="51526-167">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="51526-167">Transaction Connections</span></span>    | <span data-ttu-id="51526-168">Projekto operacijų ryšių integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="51526-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="51526-169">Įvertinimo eilutės</span><span class="sxs-lookup"><span data-stu-id="51526-169">Estimate Lines</span></span>             | <span data-ttu-id="51526-170">Projekto išlaidų įvertinimo duomenų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="51526-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="51526-171">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="51526-171">Entity flow</span></span>

<span data-ttu-id="51526-172">Apytikslės projekto išlaidų reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance“ kaip projekto išlaidų prognozės.</span><span class="sxs-lookup"><span data-stu-id="51526-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="51526-173">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="51526-173">Prerequisites</span></span>

<span data-ttu-id="51526-174">Prieš atliekant apytikslių projekto išlaidų reikšmių sinchronizavimą būtina sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="51526-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="51526-175">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="51526-175">Power Query</span></span>

<span data-ttu-id="51526-176">Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto išlaidų reikšmių šablone turite naudoti „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="51526-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="51526-177">Filtruokite taip, kad būtų įtraukti tik apytikslių išlaidų reikšmių eilučių įrašai.</span><span class="sxs-lookup"><span data-stu-id="51526-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="51526-178">Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="51526-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="51526-179">Pakeiskite atsiskaitymo tipus.</span><span class="sxs-lookup"><span data-stu-id="51526-179">Transform the billing types.</span></span>
- <span data-ttu-id="51526-180">Pakeiskite operacijų tipus.</span><span class="sxs-lookup"><span data-stu-id="51526-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="51526-181">Filtruokite taip, kad būtų įtrauktos tik apytikslių išlaidų reikšmių eilutės</span><span class="sxs-lookup"><span data-stu-id="51526-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="51526-182">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuris atliekant integravimą apima tik išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="51526-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="51526-183">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="51526-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="51526-184">Pasirinkite užduotį **Operacijos ryšiai**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="51526-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="51526-185">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="51526-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="51526-186">Filtruokite taip, kad stulpelyje **msdyn\_transactiontype1** būtų nurodyta tik **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="51526-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="51526-187">Nustatyti numatytąjį prognozės modelio ID</span><span class="sxs-lookup"><span data-stu-id="51526-187">Set the default forecast model ID</span></span>

<span data-ttu-id="51526-188">Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, pasirinkite užduotį **Apytikslės išlaidų reikšmės**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="51526-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="51526-189">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="51526-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="51526-190">Jei naudojate numatytąjį apytikslių „Microsoft Project“ išlaidų reikšmių (iš PSA į „Fin and Ops“) šabloną, naudodami „Power Query“, skyriuje **Pritaikyti veiksmai** paspauskite pirmą parinktį **Įterpta sąlyga**.</span><span class="sxs-lookup"><span data-stu-id="51526-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="51526-191">Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="51526-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="51526-192">Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="51526-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="51526-193">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="51526-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="51526-194">Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="51526-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="51526-195">Įveskite stulpelio sąlygą: jei apytikslės reikšmės eilutės ID reikšmė apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.</span><span class="sxs-lookup"><span data-stu-id="51526-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="51526-196">Atsiskaitymo tipų keitimas</span><span class="sxs-lookup"><span data-stu-id="51526-196">Transform the billing types</span></span>

<span data-ttu-id="51526-197">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems atsiskaitymo tipams keisti.</span><span class="sxs-lookup"><span data-stu-id="51526-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="51526-198">Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="51526-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="51526-199">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="51526-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="51526-200">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="51526-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="51526-201">Tada įveskite toliau nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="51526-201">Then enter the following condition:</span></span>

<span data-ttu-id="51526-202">Jei **msdyn\_billingtype** = 192350000, tada **NonChargeable**,</span><span class="sxs-lookup"><span data-stu-id="51526-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="51526-203">o jei **msdyn\_billingtype** = 192350001, tada **Chargeable**,</span><span class="sxs-lookup"><span data-stu-id="51526-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="51526-204">o jei **msdyn\_billingtype** = 192350002, tada **Complimentary**,</span><span class="sxs-lookup"><span data-stu-id="51526-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="51526-205">kitais atvejais **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="51526-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="51526-206">Operacijų tipų pakeitimas</span><span class="sxs-lookup"><span data-stu-id="51526-206">Transform the transaction types</span></span>

<span data-ttu-id="51526-207">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems operacijų tipams keisti.</span><span class="sxs-lookup"><span data-stu-id="51526-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="51526-208">Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="51526-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="51526-209">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="51526-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="51526-210">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="51526-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="51526-211">Tada įveskite toliau nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="51526-211">Then enter the following condition:</span></span>

<span data-ttu-id="51526-212">Jei **msdyn\_transactiontypecode** = 192350000, tada **Cost**,</span><span class="sxs-lookup"><span data-stu-id="51526-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="51526-213">o jei **msdyn\_transactiontypecode** = 192350005, tada **Sales**,</span><span class="sxs-lookup"><span data-stu-id="51526-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="51526-214">kitu atveju **null**</span><span class="sxs-lookup"><span data-stu-id="51526-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="51526-215">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="51526-215">Template mapping in Data integration</span></span>

<span data-ttu-id="51526-216">Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="51526-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="51526-217">Susiejime rodoma „Project Service Automation“ laukų informacija, kuri bus sinchronizuojama su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="51526-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="51526-218">[![Šablono susiejimas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="51526-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="51526-219">[![Šablono susiejimas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="51526-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
