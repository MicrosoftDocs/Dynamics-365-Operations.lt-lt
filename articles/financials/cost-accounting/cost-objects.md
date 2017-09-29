---
title: Savikainos objekto dimensijos
description: "Analizuodami išlaidas ir norėdami nustatyti, kur nukreiptas išlaidų srautas, naudojate išlaidų elemento dimensijas. Išlaidų objekto dimensijas naudojate tada, kai norite nustatyti, kur reikia priskirti išlaidas. Šioje temoje pateikiama informacijos apie išlaidų objekto dimensijas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: ed6aa29234f8e9dc8dbb4835ec260adc538989d3
ms.contentlocale: lt-lt
ms.lasthandoff: 09/18/2017

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="56b1b-105">Savikainos objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="56b1b-105">Cost object dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="56b1b-106">Analizuodami išlaidas ir norėdami nustatyti, kur nukreiptas išlaidų srautas, naudojate išlaidų elemento dimensijas.</span><span class="sxs-lookup"><span data-stu-id="56b1b-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="56b1b-107">Išlaidų objekto dimensijas naudojate tada, kai norite nustatyti, kur reikia priskirti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="56b1b-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="56b1b-108">Šioje temoje pateikiama informacijos apie išlaidų objekto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="56b1b-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="56b1b-109">Išlaidų objektas gali būti bet kokio tipo objektas, kurį norite įvertinti, kuriam norite paskirstyti išlaidas arba kurį norite tiesiogiai išmatuoti.</span><span class="sxs-lookup"><span data-stu-id="56b1b-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="56b1b-110">Dažniausiai pasitaikantys išlaidų objektai yra produktai, projektai, ištekliai, padaliniai, išlaidų centrai ir geografiniai regionai.</span><span class="sxs-lookup"><span data-stu-id="56b1b-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="56b1b-111">Valdyba naudoja išlaidų objektus norėdama apskaičiuoti išlaidas ir atlikti pelningumo analizę.</span><span class="sxs-lookup"><span data-stu-id="56b1b-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="56b1b-112">Išlaidų objekto dimensijos ir išlaidų objekto dimensijos nariai</span><span class="sxs-lookup"><span data-stu-id="56b1b-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="56b1b-113">Išlaidų objektai vadinami *išlaidų objekto dimensijos*.</span><span class="sxs-lookup"><span data-stu-id="56b1b-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="56b1b-114">Po to, kai nuspręsite, kurį objektą turėtų nurodyti išlaidų objekto dimensija, turite nurodyti atskiras dimensijos vertes arba importuoti jas į išlaidų apskaitą iš kitų išteklių sistemų.</span><span class="sxs-lookup"><span data-stu-id="56b1b-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="56b1b-115">Šios atskiros dimensijos vertės vadinamos *išlaidų objekto dimensijos nariai*.</span><span class="sxs-lookup"><span data-stu-id="56b1b-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="56b1b-116">Pavyzdžiui, norite naudoti finansinę dimensiją, kurios pavadinimas Išlaidų centras, kaip išlaidų objekto dimensiją.</span><span class="sxs-lookup"><span data-stu-id="56b1b-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="56b1b-117">Norėdami pamatyti išlaidų srautą į atskirus išlaidų centrus, turite importuoti išlaidų objekto dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="56b1b-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="56b1b-118">Šiuo atveju išlaidų objekto dimensijos nariai yra faktinių išlaidų centrai, pavyzdžiui, pardavimai, gamyba, administravimas ir geografinės vietos.</span><span class="sxs-lookup"><span data-stu-id="56b1b-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="56b1b-119">Toliau pateikiamoje ekrano nuotraukoje pavaizduotas išlaidų centrų pavyzdys, kai išlaidų centrai yra išlaidų objekto dimensija su savo faktinių išlaidų centrais, kurie yra išlaidų objekto dimensijos nariai.</span><span class="sxs-lookup"><span data-stu-id="56b1b-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="56b1b-120">[savikainos objekto dimensijos![](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="56b1b-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="56b1b-121">Išlaidų objekto dimensijos narių importavimas naudojant duomenų jungtis</span><span class="sxs-lookup"><span data-stu-id="56b1b-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="56b1b-122">Siekdami palengvinti išlaidų objekto dimensijos narių importavimą ir gauti vertes iš objektų, kuriuos norite naudoti kaip išlaidų objekto dimensijas, naudojate duomenų jungtis.</span><span class="sxs-lookup"><span data-stu-id="56b1b-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="56b1b-123">Galite naudoti iš anksto paruoštas duomenų jungtis arba savo sukurtas pasirinktines duomenų jungtis.</span><span class="sxs-lookup"><span data-stu-id="56b1b-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



