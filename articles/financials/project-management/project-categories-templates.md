---
title: "„Project Service Automation“ projekto išlaidų kategorijų sinchronizavimas"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Dynamics 365 for Project Service Automation“."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="4aec9-103">„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="4aec9-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="4aec9-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Dynamics 365 for Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="4aec9-105">Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.</span><span class="sxs-lookup"><span data-stu-id="4aec9-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="4aec9-106">„Project Service Automation“ ir „Finance and Operations“ duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="4aec9-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="4aec9-107">Naudojantis „Project Service Automation“ ir „Finance and Operations“ integravimo sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="4aec9-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="4aec9-108">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto išlaidų operacijos kategorijas srautas iš „Finance and Operations“ ir „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="4aec9-109">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“, integravimo srautas pirmiausia yra iš „Finance and Operations“ į „Project Service Automation“, o po to, sinchronizuojant iš „Project Service Automation“ į „Finance and Operations“, atnaujinamos projekto išlaidų kategorijų integravimo ID reikšmės.</span><span class="sxs-lookup"><span data-stu-id="4aec9-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4aec9-110">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Project Service Automation“, integravimo srautas pirmiausia yra iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="4aec9-111">Prieš atliekant sinchronizavimą iš „Project Service Automation“, projekto kategorijos jau turi būti sukonfigūruotos naudojantis „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="4aec9-112">Po to sinchronizuokite iš „Finance and Operations“ į „Project Service Automation“, o po to vėl iš „Project Service Automation“ į „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="4aec9-113">Taip užtikrinama, kad tikrai susiejamos kategorijos ir nesukuriamos pasikartojančios kategorijos.</span><span class="sxs-lookup"><span data-stu-id="4aec9-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="4aec9-114">Paprastai projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="4aec9-115">Jei jūsų atveju taip nėra arba jau turite sukūrę „Project Service Automation“ išlaidų kategorijas, pirmiausia turite sinchronizuoti naudodami projekto išlaidų operacijos kategorijas (iš PSA į „Fin and Ops“), o po to – naudodami projekto išlaidų operacijos kategorijas (iš „Fin and Ops“ į PSA).</span><span class="sxs-lookup"><span data-stu-id="4aec9-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="4aec9-116">Tada turėtumėte dar kartą paleisti sinchronizavimą iš PSA į „Fin and Ops“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="4aec9-117">Jei pirmiausia sinchronizuojama iš „Project Service Automation“, jau turi būti nustatytos „Finance and Operations“ projekto kategorijos, taip pat turi būti nustatyta visų kitų projekto kategorijų, kurias reikia sinchronizuoti su „Project Service Automation“ operacijos kategorijomis, reikšmė **Aktyvios žurnaluose**.</span><span class="sxs-lookup"><span data-stu-id="4aec9-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="4aec9-118">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="4aec9-119">[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4aec9-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="4aec9-120">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="4aec9-120">Templates and tasks</span></span>

<span data-ttu-id="4aec9-121">Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="4aec9-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4aec9-122">Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Project Service Automation“ projekto išlaidų kategorijas su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="4aec9-123">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA)</span><span class="sxs-lookup"><span data-stu-id="4aec9-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="4aec9-124">**Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su PSA</span><span class="sxs-lookup"><span data-stu-id="4aec9-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="4aec9-125">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="4aec9-125">Entity set</span></span>

| <span data-ttu-id="4aec9-126">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="4aec9-126">Finance and Operations</span></span>               | <span data-ttu-id="4aec9-127">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="4aec9-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="4aec9-128">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="4aec9-128">Integration entity for categories</span></span>    | <span data-ttu-id="4aec9-129">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="4aec9-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="4aec9-130">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="4aec9-130">Entity flow</span></span>

<span data-ttu-id="4aec9-131">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="4aec9-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="4aec9-132">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="4aec9-132">Power Query</span></span>

<span data-ttu-id="4aec9-133">Sinchronizuojant su „Project Service Automation“, jei norima nustatyti operacijos kategorijos atsiskaitymo tipą, būtina naudoti „Microsoft Power Query“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="4aec9-134">Projekto išlaidų operacijos kategorijų (iš „Fin and Ops“ į PSA) šablone jau pateikiamas numatytasis stulpelis ir susiejimas.</span><span class="sxs-lookup"><span data-stu-id="4aec9-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="4aec9-135">Norint sukurti savo šabloną į „Power Query“ būtina įtraukti sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="4aec9-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="4aec9-136">Atlikdami projekto išlaidų kategorijų susiejimo užduotį atidarykite formą Išplėstinė užklausa ir filtravimas.</span><span class="sxs-lookup"><span data-stu-id="4aec9-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="4aec9-137">Paspauskite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="4aec9-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="4aec9-138">Nurodykite naujo stulpelio pavadinimą, pvz., „BillingType“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="4aec9-139">Įveskite šią sąlygą: jei reikšmė **CATEGORYID nėra lygi neapibrėžtai reikšmei, tada 19235001, kitais atvejais reikšmė neapibrėžta**.</span><span class="sxs-lookup"><span data-stu-id="4aec9-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="4aec9-140">Stulpelyje spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4aec9-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="4aec9-141">Įsitikinkite, kad šis stulpelis susietas susiejimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="4aec9-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="4aec9-142">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="4aec9-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="4aec9-143">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="4aec9-144">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4aec9-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="4aec9-145">Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Project Service Automation“ projekto išlaidų kategorijas su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="4aec9-146">-**Duomenų integravimo šablono pavadinimas:** Projekto išlaidų operacijos kategorijos (iš PSA į „Fin and Ops“) -**Projekto užduoties pavadinimas:** Kategorijų sinchronizavimas su „Fin Ops“</span><span class="sxs-lookup"><span data-stu-id="4aec9-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="4aec9-147">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="4aec9-147">Entity set</span></span>

| <span data-ttu-id="4aec9-148">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="4aec9-148">Project Service Automation</span></span>      | <span data-ttu-id="4aec9-149">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="4aec9-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="4aec9-150">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="4aec9-150">Transaction categories</span></span>          | <span data-ttu-id="4aec9-151">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="4aec9-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="4aec9-152">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="4aec9-152">Entity flow</span></span>

<span data-ttu-id="4aec9-153">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="4aec9-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="4aec9-154">Vėl sinchronizuojant su „Finance and Operations“ atnaujinama „Finance and Operations“ projekto kategorijos „Project Service Automation“ integravimo ID reikšmė.</span><span class="sxs-lookup"><span data-stu-id="4aec9-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="4aec9-155">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="4aec9-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="4aec9-156">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4aec9-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4aec9-157">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="4aec9-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

