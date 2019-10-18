---
title: „Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft“ „Dynamics 365 Finance“ projekto išlaidų kategorijas su „Dynamics 365 Project Service Automation“.
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
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250512"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="77bfd-103">„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="77bfd-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="77bfd-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Dynamics 365 Finance“ projekto išlaidų kategorijas su „Dynamics 365 Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="77bfd-105">Projektų užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiami 8.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="77bfd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="77bfd-106">Faktinių duomenų integravimas pasiekiamas 8.0.1 arba naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="77bfd-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="77bfd-107">Jei naudojate „Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą.</span><span class="sxs-lookup"><span data-stu-id="77bfd-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="77bfd-108">Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="77bfd-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="77bfd-109">„Project Service Automation“ ir „Finance“ duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="77bfd-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="77bfd-110">Sprendime „Project Service Automation“ ir „Finance“ integravimas naudojama duomenų sinchronizavimo funkcija duomenims „Project Service Automation“ ir „Finance“ egzemplioriuose sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="77bfd-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="77bfd-111">Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto išlaidų operacijos kategorijas srautas tarp „Finance“ ir „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="77bfd-112">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Finance“, integravimo srautas pirmiausia yra iš „Finance“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="77bfd-113">Tada projekto išlaidų kategorijų integravimo ID atnaujinami atliekant „Project Service Automation“ sinchronizavimą su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="77bfd-114">Jei projekto išlaidų kategorijos tvarkomos naudojantis „Project Service Automation“, integravimo srautas pirmiausia yra iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="77bfd-115">Prieš atliekant sinchronizavimą iš „Project Service Automation“, projekto kategorijos jau turi būti sukonfigūruotos naudojantis „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="77bfd-116">Po to sinchronizuokite iš „Finance“ į „Project Service Automation“, o po to vėl iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="77bfd-117">Tokiu būdu padedate užtikrinti, kad kategorijos yra susietos ir nesukurta dublikatų.</span><span class="sxs-lookup"><span data-stu-id="77bfd-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="77bfd-118">Paprastai projekto išlaidų kategorijos tvarkomos naudojantis „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="77bfd-119">Tačiau, jei išlaidų kategorijos jau buvo sukurtos „Project Service Automation“, pirma turite jas sinchronizuoti, naudodami projekto išlaidų operacijos kategorijų (iš PSA į „Fin and Ops“) šabloną.</span><span class="sxs-lookup"><span data-stu-id="77bfd-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="77bfd-120">Tada sinchronizuokite naudodami projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA) šabloną.</span><span class="sxs-lookup"><span data-stu-id="77bfd-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="77bfd-121">Tada turėtumėte dar kartą atlikti „Project Service Automation“ sinchronizavimą su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="77bfd-122">Jei pirmiausia sinchronizuojate iš „Project Service Automation“, prieš atlikdami sinchronizavimą turite įvykdyti toliau pateikiamus „Finance“ reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="77bfd-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="77bfd-123">Turi būti bendro naudojimo kategorija, kuri sutampa su projekto kategorija, nustatyta „Project Service Automation“, be to, ji turi būti įgalinta ir **Projektui** ir **Išlaidoms**.</span><span class="sxs-lookup"><span data-stu-id="77bfd-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="77bfd-124">Kiekvienam „Finance“ juridiniam subjektui, kuris turi būti integruotas, turi būti toliau pateikiamos projekto kategorijos.</span><span class="sxs-lookup"><span data-stu-id="77bfd-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="77bfd-125">**Projektas/kategorija** yra.</span><span class="sxs-lookup"><span data-stu-id="77bfd-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="77bfd-126">**Naudoti tvarkant išlaidas** įgalintas.</span><span class="sxs-lookup"><span data-stu-id="77bfd-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="77bfd-127">**Aktyvus žurnale** įgalintas.</span><span class="sxs-lookup"><span data-stu-id="77bfd-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="77bfd-128">Nustatyta **Operacijos tipas** **Išlaidos**</span><span class="sxs-lookup"><span data-stu-id="77bfd-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="77bfd-129">Toliau esančiame paveikslėlyje pavaizduotas duomenų sinchronizavimas tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="77bfd-130">[![„Project Service Automation“ integravimo su „Finance“ duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="77bfd-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="77bfd-131">„Finance“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="77bfd-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="77bfd-132">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="77bfd-132">Template and task</span></span>

<span data-ttu-id="77bfd-133">Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="77bfd-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="77bfd-134">Toliau pateiktas šablonas ir pagrindinė užduotis naudojami sinchronizuojant „Finance“ projekto išlaidų kategorijas su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="77bfd-135">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA)</span><span class="sxs-lookup"><span data-stu-id="77bfd-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="77bfd-136">**Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su PSA</span><span class="sxs-lookup"><span data-stu-id="77bfd-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="77bfd-137">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="77bfd-137">Entity set</span></span>

| <span data-ttu-id="77bfd-138">Finansai</span><span class="sxs-lookup"><span data-stu-id="77bfd-138">Finance</span></span>                           | <span data-ttu-id="77bfd-139">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="77bfd-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="77bfd-140">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="77bfd-140">Integration entity for categories</span></span> | <span data-ttu-id="77bfd-141">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="77bfd-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="77bfd-142">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="77bfd-142">Entity flow</span></span>

<span data-ttu-id="77bfd-143">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="77bfd-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="77bfd-144">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="77bfd-144">Power Query</span></span>

<span data-ttu-id="77bfd-145">Sinchronizuojant su „Project Service Automation“, jei norima nustatyti operacijos kategorijos atsiskaitymo tipą, būtina naudoti „Microsoft Power Query for Excel“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="77bfd-146">Projekto išlaidų operacijos kategorijų (iš „Fin and Ops“ į PSA) šablone pateikiamas numatytasis stulpelis ir susiejimas.</span><span class="sxs-lookup"><span data-stu-id="77bfd-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="77bfd-147">Norint sukurti savo šabloną į „Power Query“ būtina įtraukti sąlyginį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="77bfd-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="77bfd-148">Atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="77bfd-148">Follow these steps.</span></span>

1. <span data-ttu-id="77bfd-149">Spustelėkite rodyklę, kad atidarytumėte projekto išlaidų kategorijų užduoties susiejimą projekto išlaidų kategorijų (iš „Fin and Ops“ į PSA) šablone.</span><span class="sxs-lookup"><span data-stu-id="77bfd-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="77bfd-150">Spustelėkite nuorodą **Išplėstinė užklausa ir Filtravimas**, kad atidarytumėte „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="77bfd-151">Paspauskite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="77bfd-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="77bfd-152">Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="77bfd-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="77bfd-153">Įveskite šią sąlygą: jei reikšmė **CATEGORYID nėra lygi neapibrėžtai reikšmei, tada 19235001, kitais atvejais reikšmė neapibrėžta**.</span><span class="sxs-lookup"><span data-stu-id="77bfd-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="77bfd-154">Stulpelyje spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="77bfd-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="77bfd-155">Įsitikinkite, kad šis stulpelis susietas susiejimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="77bfd-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="77bfd-156">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="77bfd-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="77bfd-157">Susiejime rodoma „Finance“ laukų informacija, kuri bus sinchronizuojama su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="77bfd-158">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="77bfd-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="77bfd-159">„Project Service Automation“ projekto išlaidų kategorijų sinchronizavimas su „Finance“</span><span class="sxs-lookup"><span data-stu-id="77bfd-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="77bfd-160">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="77bfd-160">Template and task</span></span>

<span data-ttu-id="77bfd-161">Toliau pateiktas šablonas ir pagrindinė užduotis naudojami sinchronizuojant „Project Service Automation“ projekto išlaidų kategorijas su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="77bfd-162">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="77bfd-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="77bfd-163">**Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su „Fin Ops“</span><span class="sxs-lookup"><span data-stu-id="77bfd-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="77bfd-164">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="77bfd-164">Entity set</span></span>

| <span data-ttu-id="77bfd-165">„Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="77bfd-165">Project Service Automation</span></span> | <span data-ttu-id="77bfd-166">Finansai</span><span class="sxs-lookup"><span data-stu-id="77bfd-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="77bfd-167">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="77bfd-167">Transaction categories</span></span>     | <span data-ttu-id="77bfd-168">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="77bfd-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="77bfd-169">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="77bfd-169">Entity flow</span></span>

<span data-ttu-id="77bfd-170">Projekto išlaidų kategorijos tvarkomos naudojantis „Finance“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="77bfd-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="77bfd-171">Vėl sinchronizuojant su „Finance“ atnaujinama „Finance“ projekto kategorijos „Project Service Automation“ integravimo ID reikšmė.</span><span class="sxs-lookup"><span data-stu-id="77bfd-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="77bfd-172">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="77bfd-172">Template mapping in Data integration</span></span>

<span data-ttu-id="77bfd-173">Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="77bfd-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="77bfd-174">Susiejime rodoma „Project Service Automation“ laukų informacija, kuri bus sinchronizuojama su „Finance“.</span><span class="sxs-lookup"><span data-stu-id="77bfd-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="77bfd-175">[![Šablono susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="77bfd-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
