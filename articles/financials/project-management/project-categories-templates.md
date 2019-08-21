---
title: „Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Microsoft Dynamics 365 for Project Service Automation“.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838372"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="31ef2-103">„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="31ef2-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31ef2-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Microsoft Dynamics 365 for Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="31ef2-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.</span><span class="sxs-lookup"><span data-stu-id="31ef2-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="31ef2-106">Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.</span><span class="sxs-lookup"><span data-stu-id="31ef2-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="31ef2-107">Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą.</span><span class="sxs-lookup"><span data-stu-id="31ef2-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="31ef2-108">Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="31ef2-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="31ef2-109">„Project Service Automation“ ir „Finance and Operations“ duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="31ef2-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="31ef2-110">Naudojantis „Project Service Automation“ ir „Finance and Operations“ integravimo sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="31ef2-111">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto išlaidų operacijos kategorijas srautas iš „Finance and Operations“ ir „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="31ef2-112">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“, integravimo srautas pirmiausia yra iš „Finance and Operations“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="31ef2-113">Tada projekto išlaidų kategorijų integravimo ID atnaujinami atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="31ef2-114">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Project Service Automation“, integravimo srautas pirmiausia yra iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="31ef2-115">Prieš atliekant sinchronizavimą iš „Project Service Automation“, projekto kategorijos jau turi būti sukonfigūruotos naudojantis „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="31ef2-116">Po to sinchronizuokite iš „Finance and Operations“ į „Project Service Automation“, o po to vėl iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="31ef2-117">Tokiu būdu padedate užtikrinti, kad kategorijos yra susietos ir nesukurta dublikatų.</span><span class="sxs-lookup"><span data-stu-id="31ef2-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="31ef2-118">Paprastai projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="31ef2-119">Tačiau, jei išlaidų kategorijos nebus tvarkomos naudojantis „Finance and Operations“ arba jos jau buvo sukurtos „Project Service Automation“, pirma turite jas sinchronizuoti, naudodami projekto išlaidų kategorijos (iš PSA į „Fin and Ops“) šabloną.</span><span class="sxs-lookup"><span data-stu-id="31ef2-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="31ef2-120">Tada sinchronizuokite naudodami projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA) šabloną.</span><span class="sxs-lookup"><span data-stu-id="31ef2-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="31ef2-121">Tada turėtumėte dar kartą atlikti „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="31ef2-122">Jei pirmiausia sinchronizuojate iš „Project Service Automation“, prieš atlikdami sinchronizavimą turite įvykdyti tokius „Finance and Operations“ reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="31ef2-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="31ef2-123">Turi būti bendro naudojimo kategorija, kuri sutampa su projekto kategorija, nustatyta „Project Service Automation“, be to, ji turi būti įgalinta ir **Projektui** ir **Išlaidoms**.</span><span class="sxs-lookup"><span data-stu-id="31ef2-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="31ef2-124">Kiekvienam „Finance and Operations“ juridiniam subjektui, kuris turi būti integruotas, turi būti tokios projekto kategorijos:</span><span class="sxs-lookup"><span data-stu-id="31ef2-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="31ef2-125">**Projektas/kategorija** yra.</span><span class="sxs-lookup"><span data-stu-id="31ef2-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="31ef2-126">**Naudoti tvarkant išlaidas** įgalintas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="31ef2-127">**Aktyvus žurnale** įgalintas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="31ef2-128">Nustatyta **Operacijos tipas** **Išlaidos**</span><span class="sxs-lookup"><span data-stu-id="31ef2-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="31ef2-129">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="31ef2-130">[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="31ef2-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="31ef2-131">„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="31ef2-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="31ef2-132">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="31ef2-132">Template and task</span></span>

<span data-ttu-id="31ef2-133">Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="31ef2-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="31ef2-134">Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Finance and Operations“ projekto išlaidų kategorijas su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="31ef2-135">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA)</span><span class="sxs-lookup"><span data-stu-id="31ef2-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="31ef2-136">**Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su PSA</span><span class="sxs-lookup"><span data-stu-id="31ef2-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="31ef2-137">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="31ef2-137">Entity set</span></span>

| <span data-ttu-id="31ef2-138">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="31ef2-138">Finance and Operations</span></span>            | <span data-ttu-id="31ef2-139">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="31ef2-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="31ef2-140">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="31ef2-140">Integration entity for categories</span></span> | <span data-ttu-id="31ef2-141">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="31ef2-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="31ef2-142">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="31ef2-142">Entity flow</span></span>

<span data-ttu-id="31ef2-143">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="31ef2-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="31ef2-144">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="31ef2-144">Power Query</span></span>

<span data-ttu-id="31ef2-145">Sinchronizuojant su „Project Service Automation“, jei norima nustatyti operacijos kategorijos atsiskaitymo tipą, būtina naudoti „Microsoft Power Query for Excel“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="31ef2-146">Projekto išlaidų operacijos kategorijų (iš „Fin and Ops“ į PSA) šablone pateikiamas numatytasis stulpelis ir susiejimas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="31ef2-147">Norint sukurti savo šabloną į „Power Query“ būtina įtraukti sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="31ef2-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="31ef2-148">Atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="31ef2-148">Follow these steps.</span></span>

1. <span data-ttu-id="31ef2-149">Spustelėkite rodyklę, kad atidarytumėte projekto išlaidų kategorijų užduoties susiejimą projekto išlaidų kategorijų (iš „Fin and Ops“ į PSA) šablone.</span><span class="sxs-lookup"><span data-stu-id="31ef2-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="31ef2-150">Spustelėkite nuorodą **Išplėstinė užklausa ir Filtravimas**, kad atidarytumėte „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="31ef2-151">Paspauskite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="31ef2-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="31ef2-152">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="31ef2-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="31ef2-153">Įveskite šią sąlygą: jei reikšmė **CATEGORYID nėra lygi neapibrėžtai reikšmei, tada 19235001, kitais atvejais reikšmė neapibrėžta**.</span><span class="sxs-lookup"><span data-stu-id="31ef2-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="31ef2-154">Stulpelyje spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="31ef2-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="31ef2-155">Įsitikinkite, kad šis stulpelis susietas susiejimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="31ef2-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="31ef2-156">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="31ef2-157">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="31ef2-158">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="31ef2-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="31ef2-159">„Project Service Automation“ projekto išlaidų kategorijų sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="31ef2-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="31ef2-160">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="31ef2-160">Template and task</span></span>

<span data-ttu-id="31ef2-161">Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Finance and Operations“ projekto išlaidų kategorijas su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="31ef2-162">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="31ef2-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="31ef2-163">**Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su „Fin Ops“</span><span class="sxs-lookup"><span data-stu-id="31ef2-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="31ef2-164">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="31ef2-164">Entity set</span></span>

| <span data-ttu-id="31ef2-165">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="31ef2-165">Project Service Automation</span></span> | <span data-ttu-id="31ef2-166">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="31ef2-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="31ef2-167">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="31ef2-167">Transaction categories</span></span>     | <span data-ttu-id="31ef2-168">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="31ef2-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="31ef2-169">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="31ef2-169">Entity flow</span></span>

<span data-ttu-id="31ef2-170">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="31ef2-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="31ef2-171">Vėl sinchronizuojant su „Finance and Operations“ atnaujinama „Finance and Operations“ projekto kategorijos „Project Service Automation“ integravimo ID reikšmė.</span><span class="sxs-lookup"><span data-stu-id="31ef2-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="31ef2-172">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="31ef2-172">Template mapping in Data integration</span></span>

<span data-ttu-id="31ef2-173">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="31ef2-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="31ef2-174">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="31ef2-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="31ef2-175">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="31ef2-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
