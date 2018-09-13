---
title: "Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="44c96-103">Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="44c96-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="44c96-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="44c96-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.</span><span class="sxs-lookup"><span data-stu-id="44c96-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="44c96-106">Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.</span><span class="sxs-lookup"><span data-stu-id="44c96-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="44c96-107">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="44c96-108">Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="44c96-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="44c96-109">„Project Service Automation“ duomenų srautas į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="44c96-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="44c96-110">Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="44c96-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="44c96-111">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie apytiksles projekto grafiko ir projekto išlaidų reikšmes srautas iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="44c96-112">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="44c96-113">[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="44c96-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="44c96-114">Apytikslės projekto grafiko reikšmės</span><span class="sxs-lookup"><span data-stu-id="44c96-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="44c96-115">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="44c96-115">Template and tasks</span></span>

<span data-ttu-id="44c96-116">Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="44c96-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="44c96-117">Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant apytiksles „Project Service Automation“ projekto grafiko reikšmes su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="44c96-118">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto grafiko reikšmės (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="44c96-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="44c96-119">**Užduočių pavadinimas projekte**</span><span class="sxs-lookup"><span data-stu-id="44c96-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="44c96-120">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="44c96-120">Transaction relationships</span></span>
    - <span data-ttu-id="44c96-121">Numatomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="44c96-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="44c96-122">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="44c96-122">Entity set</span></span>

| <span data-ttu-id="44c96-123">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="44c96-123">Project Service Automation</span></span> | <span data-ttu-id="44c96-124">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="44c96-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="44c96-125">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="44c96-125">Project tasks</span></span>              | <span data-ttu-id="44c96-126">Projekto valandų įvertinimo duomenų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="44c96-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="44c96-127">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="44c96-127">Entity flow</span></span>

<span data-ttu-id="44c96-128">Apytikslės projekto grafiko reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip grafikų prognozės.</span><span class="sxs-lookup"><span data-stu-id="44c96-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="44c96-129">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="44c96-129">Prerequisites</span></span>

<span data-ttu-id="44c96-130">Prieš sinchronizavimą projekto valandų įvertinimo gali atsirasti, galite sinchronizuoti projektus, projekto užduotims ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="44c96-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="44c96-131">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="44c96-131">Power Query</span></span>

<span data-ttu-id="44c96-132">Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto grafiko reikšmių šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.</span><span class="sxs-lookup"><span data-stu-id="44c96-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="44c96-133">Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="44c96-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="44c96-134">Filtruoti visus užduotyje esančius konkretaus ištekliaus įrašus, dėl kurių galėtų nepavykti integravimas į grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="44c96-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="44c96-135">Filtruoti visas tuščias operacijos kategorijos eilutes.</span><span class="sxs-lookup"><span data-stu-id="44c96-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="44c96-136">Nepavykus atlikti užduoties, gali būti pateikiamos klaidingos grafikų prognozės.</span><span class="sxs-lookup"><span data-stu-id="44c96-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="44c96-137">Nustatyti numatytąjį prognozės modelio ID</span><span class="sxs-lookup"><span data-stu-id="44c96-137">Set the default forecast model ID</span></span>

<span data-ttu-id="44c96-138">Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="44c96-139">Tada pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="44c96-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="44c96-140">Jei naudojate numatytąjį apytikslių „Microsoft Project“ grafiko reikšmių (iš PSA į „Fin and Ops“) šabloną, sąraše **Pritaikyti veiksmai** paspauskite **Įterpta sąlyga**.</span><span class="sxs-lookup"><span data-stu-id="44c96-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="44c96-141">Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="44c96-142">Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="44c96-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="44c96-143">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="44c96-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="44c96-144">Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="44c96-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="44c96-145">Įveskite stulpelio sąlygą: jei projekto užduotis apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.</span><span class="sxs-lookup"><span data-stu-id="44c96-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="44c96-146">Filtruoti tam tikro ištekliaus įrašus</span><span class="sxs-lookup"><span data-stu-id="44c96-146">Filter out resource-specific records</span></span>

<span data-ttu-id="44c96-147">Apytikslių projekto grafiko reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo naudojantis pašalinami visi konkretaus ištekliaus įrašai.</span><span class="sxs-lookup"><span data-stu-id="44c96-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="44c96-148">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="44c96-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="44c96-149">Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad filtruotumėte stulpelį **msdyn\_islinetask**, kad būtų įtraukiami tik užrašu **Klaidinga** pažymėti įrašai.</span><span class="sxs-lookup"><span data-stu-id="44c96-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="44c96-150">Tuščių operacijos kategorijos eilučių filtravimas</span><span class="sxs-lookup"><span data-stu-id="44c96-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="44c96-151">Norėdami pašalinti visas eilutes, kurių operacijos kategorijos yra tuščios, turite įtraukti filtrą.</span><span class="sxs-lookup"><span data-stu-id="44c96-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="44c96-152">Šią užduotį atlikti būtina, nepriklausomai nuo to, ar naudojate numatytąjį šabloną, ar sukuriate savo šabloną.</span><span class="sxs-lookup"><span data-stu-id="44c96-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="44c96-153">Naudojantis šiuo filtru pašalinamos visos iš „Project Service Automation“ gautos eilutės, dėl kurių galėtų būti pateikiamos klaidingos „Finance and Operations“ grafikų prognozės.</span><span class="sxs-lookup"><span data-stu-id="44c96-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="44c96-154">Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad būtų filtruojami neapibrėžti stulpelio **msdyn\_transactioncategory\_value** įrašai.</span><span class="sxs-lookup"><span data-stu-id="44c96-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="44c96-155">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="44c96-155">Template mapping in Data integration</span></span>

<span data-ttu-id="44c96-156">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="44c96-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="44c96-157">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="44c96-158">[![Šablono susiejimas](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="44c96-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="44c96-159">Apytikslės projekto išlaidų reikšmės</span><span class="sxs-lookup"><span data-stu-id="44c96-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="44c96-160">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="44c96-160">Template and tasks</span></span>

<span data-ttu-id="44c96-161">Toliau pateiktas šablonas ir pagrindinės užduotys naudojami sinchronizuojant apytiksles „Project Service Automation“ projekto išlaidų reikšmes su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="44c96-162">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto išlaidų reikšmės (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="44c96-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="44c96-163">**Užduočių pavadinimas projekte**</span><span class="sxs-lookup"><span data-stu-id="44c96-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="44c96-164">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="44c96-164">Transaction relationships</span></span> 
    - <span data-ttu-id="44c96-165">Numatomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="44c96-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="44c96-166">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="44c96-166">Entity set</span></span>

| <span data-ttu-id="44c96-167">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="44c96-167">Project Service Automation</span></span> | <span data-ttu-id="44c96-168">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="44c96-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="44c96-169">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="44c96-169">Transaction Connections</span></span>    | <span data-ttu-id="44c96-170">Projekto operacijų ryšių integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="44c96-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="44c96-171">Įvertinimo eilutės</span><span class="sxs-lookup"><span data-stu-id="44c96-171">Estimate Lines</span></span>             | <span data-ttu-id="44c96-172">Projekto išlaidų įvertinimo duomenų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="44c96-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="44c96-173">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="44c96-173">Entity flow</span></span>

<span data-ttu-id="44c96-174">Apytikslės projekto išlaidų reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto išlaidų prognozės.</span><span class="sxs-lookup"><span data-stu-id="44c96-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="44c96-175">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="44c96-175">Prerequisites</span></span>

<span data-ttu-id="44c96-176">Prieš atliekant apytikslių projekto išlaidų reikšmių sinchronizavimą būtina sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="44c96-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="44c96-177">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="44c96-177">Power Query</span></span>

<span data-ttu-id="44c96-178">Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto išlaidų reikšmių šablone turite naudoti „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="44c96-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="44c96-179">Filtruokite taip, kad būtų įtraukti tik apytikslių išlaidų reikšmių eilučių įrašai.</span><span class="sxs-lookup"><span data-stu-id="44c96-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="44c96-180">Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.</span><span class="sxs-lookup"><span data-stu-id="44c96-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="44c96-181">Pakeiskite atsiskaitymo tipus.</span><span class="sxs-lookup"><span data-stu-id="44c96-181">Transform the billing types.</span></span>
- <span data-ttu-id="44c96-182">Pakeiskite operacijų tipus.</span><span class="sxs-lookup"><span data-stu-id="44c96-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="44c96-183">Filtruokite taip, kad būtų įtrauktos tik apytikslių išlaidų reikšmių eilutės</span><span class="sxs-lookup"><span data-stu-id="44c96-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="44c96-184">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuris atliekant integravimą apima tik išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="44c96-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="44c96-185">Norint sukurti savo šabloną būtina įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="44c96-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="44c96-186">Pasirinkite užduotį **Operacijos ryšiai**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="44c96-187">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="44c96-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="44c96-188">Filtruokite taip, kad stulpelyje **msdyn\_transactiontype1** būtų nurodyta tik **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="44c96-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="44c96-189">Nustatyti numatytąjį prognozės modelio ID</span><span class="sxs-lookup"><span data-stu-id="44c96-189">Set the default forecast model ID</span></span>

<span data-ttu-id="44c96-190">Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, pasirinkite užduotį **Apytikslės išlaidų reikšmės**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="44c96-191">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="44c96-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="44c96-192">Jei naudojate numatytąjį apytikslių „Microsoft Project“ išlaidų reikšmių (iš PSA į „Fin and Ops“) šabloną, naudodami „Power Query“, skyriuje **Pritaikyti veiksmai** paspauskite pirmą parinktį **Įterpta sąlyga**.</span><span class="sxs-lookup"><span data-stu-id="44c96-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="44c96-193">Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="44c96-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="44c96-194">Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="44c96-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="44c96-195">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="44c96-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="44c96-196">Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="44c96-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="44c96-197">Įveskite stulpelio sąlygą: jei apytikslės reikšmės eilutės ID reikšmė apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.</span><span class="sxs-lookup"><span data-stu-id="44c96-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="44c96-198">Atsiskaitymo tipų keitimas</span><span class="sxs-lookup"><span data-stu-id="44c96-198">Transform the billing types</span></span>

<span data-ttu-id="44c96-199">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems atsiskaitymo tipams keisti.</span><span class="sxs-lookup"><span data-stu-id="44c96-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="44c96-200">Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="44c96-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="44c96-201">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="44c96-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="44c96-202">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="44c96-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="44c96-203">Tada įveskite toliau nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="44c96-203">Then enter the following condition:</span></span>

<span data-ttu-id="44c96-204">Jei **msdyn\_billingtype** = 192350000, tada **NonChargeable**,</span><span class="sxs-lookup"><span data-stu-id="44c96-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="44c96-205">o jei **msdyn\_billingtype** = 192350001, tada **Chargeable**,</span><span class="sxs-lookup"><span data-stu-id="44c96-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="44c96-206">o jei **msdyn\_billingtype** = 192350002, tada **Complimentary**,</span><span class="sxs-lookup"><span data-stu-id="44c96-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="44c96-207">kitais atvejais **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="44c96-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="44c96-208">Operacijų tipų pakeitimas</span><span class="sxs-lookup"><span data-stu-id="44c96-208">Transform the transaction types</span></span>

<span data-ttu-id="44c96-209">Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems operacijų tipams keisti.</span><span class="sxs-lookup"><span data-stu-id="44c96-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="44c96-210">Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="44c96-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="44c96-211">Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="44c96-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="44c96-212">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="44c96-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="44c96-213">Tada įveskite toliau nurodytą sąlygą.</span><span class="sxs-lookup"><span data-stu-id="44c96-213">Then enter the following condition:</span></span>

<span data-ttu-id="44c96-214">Jei **msdyn\_transactiontypecode** = 192350000, tada **Cost**,</span><span class="sxs-lookup"><span data-stu-id="44c96-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="44c96-215">o jei **msdyn\_transactiontypecode** = 192350005, tada **Sales**,</span><span class="sxs-lookup"><span data-stu-id="44c96-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="44c96-216">kitu atveju **null**</span><span class="sxs-lookup"><span data-stu-id="44c96-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="44c96-217">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="44c96-217">Template mapping in Data integration</span></span>

<span data-ttu-id="44c96-218">Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="44c96-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="44c96-219">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="44c96-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="44c96-220">[![Šablono susiejimas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="44c96-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="44c96-221">[![Šablono susiejimas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="44c96-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
