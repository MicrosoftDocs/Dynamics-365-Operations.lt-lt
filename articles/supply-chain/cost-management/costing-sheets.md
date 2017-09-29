---
title: "Įkainojimo lapai"
description: "Įkainojimo lapo nustatymas apima du tikslus. Pirmasis tikslas yra apibrėžti informacijos rodymo formatą parduotų prekių savikainai, informacijai apie pagamintą prekę ar gamybos užsakymui. Suformatuotas rodinys vadinamas įkainojimo lapu. Antrasis tikslas yra apibrėžti netiesioginių išlaidų apskaičiavimo pagrindą. Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcija informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms. Šiame straipsnyje aprašomi du įkainojimo lapo nustatymo tikslai."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostSheetDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7aaa8a6a47bbd5c1d26cea7b05c3c5d031495382
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="costing-sheets"></a><span data-ttu-id="76cb3-108">Įkainojimo lapai</span><span class="sxs-lookup"><span data-stu-id="76cb3-108">Costing sheets</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76cb3-109">Įkainojimo lapo nustatymas apima du tikslus.</span><span class="sxs-lookup"><span data-stu-id="76cb3-109">Setting up the costing sheet involves two objectives.</span></span> <span data-ttu-id="76cb3-110">Pirmasis tikslas yra apibrėžti informacijos rodymo formatą parduotų prekių savikainai, informacijai apie pagamintą prekę ar gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="76cb3-110">As the first objective, you define the format for displaying cost of goods sold information about a manufactured item or production order.</span></span> <span data-ttu-id="76cb3-111">Suformatuotas rodinys vadinamas įkainojimo lapu.</span><span class="sxs-lookup"><span data-stu-id="76cb3-111">The formatted display is termed a costing sheet.</span></span> <span data-ttu-id="76cb3-112">Antrasis tikslas yra apibrėžti netiesioginių išlaidų apskaičiavimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-112">As the second objective, you define the basis for calculating indirect costs.</span></span> <span data-ttu-id="76cb3-113">Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcija informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms.</span><span class="sxs-lookup"><span data-stu-id="76cb3-113">The costing sheet setup builds on the cost group feature for displaying information and for the indirect cost calculation formulas.</span></span> <span data-ttu-id="76cb3-114">Šiame straipsnyje aprašomi du įkainojimo lapo nustatymo tikslai.</span><span class="sxs-lookup"><span data-stu-id="76cb3-114">The two objectives of costing sheet setup are described in this article.</span></span> 

<span data-ttu-id="76cb3-115">Įkainojimo lapas yra suformatuotas informacijos apie parduotų gaminamos prekės arba gamybos užsakymo prekių savikainą rodinys.</span><span class="sxs-lookup"><span data-stu-id="76cb3-115">A costing sheet is the formatted display of information about the cost of goods that are sold for a manufactured item or a production order.</span></span> <span data-ttu-id="76cb3-116">Kai nustatote įkainojimo lapą, nurodote informacijos formatą ir apibrėžiate netiesioginių išlaidų skaičiavimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-116">When you set up a costing sheet, you define the format for the information and also define the basis for calculating indirect costs.</span></span> <span data-ttu-id="76cb3-117">Įkainojimo lapo nustatymas pagrįstas išlaidų grupės funkcijomis informacijai rodyti ir netiesioginių išlaidų skaičiavimo formulėms.</span><span class="sxs-lookup"><span data-stu-id="76cb3-117">The costing sheet setup builds on the cost group features for displaying information and for the formulas that are used to calculated indirect cost.</span></span> <span data-ttu-id="76cb3-118">Toliau pateikiama daugiau informacijos apie du įkainojimo lapo nustatymo tikslus.</span><span class="sxs-lookup"><span data-stu-id="76cb3-118">Here is more information about the two objectives of costing sheet setup:</span></span>
-   <span data-ttu-id="76cb3-119">**Apibrėžti įkainojimo lapo formatą.**</span><span class="sxs-lookup"><span data-stu-id="76cb3-119">**Define the format for the costing sheet.**</span></span> <span data-ttu-id="76cb3-120">Vartotojo apibrėžiamas išlaidų lapo formatas nustato išlaidų, kurias sudaro pagamintos prekės parduotų prekių savikaina, segmentavimą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-120">The user-defined format for a costing sheet identifies the segmentation of costs that contain a manufactured item’s cost of goods sold.</span></span> <span data-ttu-id="76cb3-121">Pavyzdžiui, informaciją apie prekės parduotų prekių savikainą galima segmentuoti į medžiagą, darbą ir pridėtines išlaidas pagal išlaidų grupes.</span><span class="sxs-lookup"><span data-stu-id="76cb3-121">For example, the information about an item’s cost of goods sold can be segmented into material, labor, and overhead, based on cost groups.</span></span> <span data-ttu-id="76cb3-122">Šios išlaidų grupės yra priskiriamos prekėms, išlaidų kategorijoms nukreipimo operacijoms ir netiesioginių išlaidų apskaičiavimo formulėms.</span><span class="sxs-lookup"><span data-stu-id="76cb3-122">These cost groups are assigned to items, cost categories for routing operations, and indirect cost calculation formulas.</span></span> <span data-ttu-id="76cb3-123">Įkainojimo lapo formatui paprastai reikia tarpinių sumų, kai norima apibrėžti keletą išlaidų grupių.</span><span class="sxs-lookup"><span data-stu-id="76cb3-123">The format for the costing sheet typically requires intermediate totals when multiple cost groups have been defined.</span></span> <span data-ttu-id="76cb3-124">Pavyzdžiui, galima agreguoti keletą išlaidų grupių, kurios susijusios su medžiaga.</span><span class="sxs-lookup"><span data-stu-id="76cb3-124">For example, multiple cost groups that are related to material can be aggregated.</span></span> <span data-ttu-id="76cb3-125">Išlaidų lapo formato apibrėžimas yra laisvai pasirenkamas, tačiau išlaidų lapo formatas turi būti apibrėžtas, jei skaičiuojamos netiesioginės išlaidos.</span><span class="sxs-lookup"><span data-stu-id="76cb3-125">The definition of a costing sheet format is optional, but a costing sheet format must be defined if indirect costs will be calculated.</span></span>
-   <span data-ttu-id="76cb3-126">**Aprašykite netiesioginių išlaidų apskaičiavimo pagrindą.**</span><span class="sxs-lookup"><span data-stu-id="76cb3-126">**Define the basis for calculating indirect costs.**</span></span> <span data-ttu-id="76cb3-127">Netiesioginės išlaidos atspindi pridėtines gamybos išlaidas, susijusias su pagamintos prekės gamyba.</span><span class="sxs-lookup"><span data-stu-id="76cb3-127">Indirect costs reflect manufacturing overhead that is associated with the production of a manufactured item.</span></span> <span data-ttu-id="76cb3-128">Netiesioginių išlaidų skaičiavimo formulė gali būti išreikšta kaip papildomas mokestis arba tarifas.</span><span class="sxs-lookup"><span data-stu-id="76cb3-128">An indirect cost calculation formula can be expressed as either a surcharge or a rate.</span></span> <span data-ttu-id="76cb3-129">Papildomas mokestis pateikiamas vertės procentu, o tarifas yra suma per nukreipimo operacijos valandą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-129">A surcharge represents a percentage of value, whereas a rate represents an amount per hour for a routing operation.</span></span> <span data-ttu-id="76cb3-130">Išlaidų grupė apibrėžia skaičiavimo formulės pagrindą, pvz., 100 % papildomas darbo išlaidų grupės išlaidas arba 50,00 USD mašinų išlaidų grupės valandinį tarifą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-130">A cost group defines the basis for the calculation formula, such as a 100-percent surcharge for a labor cost group or a USD 50.00 hourly rate for a machine cost group.</span></span> <span data-ttu-id="76cb3-131">Siekiant apibrėžti skaičiavimo formulę ir jos išlaidų grupės pagrindą, norint nustatyti išlaidų lapą būtina identifikuoti išlaidų grupę, kuri nurodo pridėtines išlaidas, ir pasirinkti naudoti papildomo mokesčio arba tarifo metodą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-131">If you want to define a calculation formula and its cost group basis, the costing sheet setup requires that you identify the cost group that represents the overhead, and select whether a surcharge or rate approach is used.</span></span>

<span data-ttu-id="76cb3-132">Kiekviena skaičiavimo formulė turi būti įvesta kaip išlaidų įrašas.</span><span class="sxs-lookup"><span data-stu-id="76cb3-132">Each calculation formula must be entered as a cost record.</span></span> <span data-ttu-id="76cb3-133">Išlaidų įrašą sudaro nustatyta įkainojimo versija, papildomo mokesčio procentas arba tarifo suma, išlaidų grupės pagrindas, būsena ir galiojimo data.</span><span class="sxs-lookup"><span data-stu-id="76cb3-133">The cost record consists of a specified costing version, a surcharge percentage or a rate amount, the cost group basis, a status, and an effective date.</span></span> <span data-ttu-id="76cb3-134">Kai pirmą kartą įvedamas išlaidų įrašas, jo būsena yra **Laukiantis** ir jis turi įsigaliojimo datą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-134">When a cost record is first entered, it has **Pending** status and an effective date.</span></span> <span data-ttu-id="76cb3-135">Kai išlaidų įrašą suaktyvinate, būsena atnaujinama ir įrašas būna dabartinis aktyvus įrašas, o įsigaliojimo data atnaujinama į aktyvinimo datą.</span><span class="sxs-lookup"><span data-stu-id="76cb3-135">When you activate the cost record, the status is updated to so that the record is the current active record, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="76cb3-136">Išlaidų įrašas taip pat gali nurodyti konkrečios teritorijos skaičiavimo formulės teritoriją.</span><span class="sxs-lookup"><span data-stu-id="76cb3-136">The cost record can also specify a site for a site-specific calculation formula.</span></span> <span data-ttu-id="76cb3-137">Taip pat lauką **Teritorija** galite palikti tuščią, jei norite nurodyti, kad skaičiavimo formulė yra visos įmonės formulė.</span><span class="sxs-lookup"><span data-stu-id="76cb3-137">Alternatively, you can leave the **Site** field blank to indicate that the calculation formula is a company-wide formula.</span></span> <span data-ttu-id="76cb3-138">Išlaidų įrašą pasirinktinai gali sudaryti nustatyta prekė arba prekių grupė, kai skaičiavimo formulė pažymėta kaip formulė, skirta vienai prekei.</span><span class="sxs-lookup"><span data-stu-id="76cb3-138">The cost record can optionally consist of a specified item or item group when the calculation formula has been marked as a per-item formula.</span></span> 

<span data-ttu-id="76cb3-139">Šiuo metu aktyvūs išlaidų įrašai netiesioginių išlaidų skaičiavimo formulėse naudojami gamybos užsakymo išlaidoms įvertinti.</span><span class="sxs-lookup"><span data-stu-id="76cb3-139">The current active cost records for indirect cost calculation formulas are used to estimate production order costs.</span></span> <span data-ttu-id="76cb3-140">Jie taip pat naudojami skaičiuojant faktines išlaidas, susijusias su faktiniu laiko ir medžiagų suvartojimu.</span><span class="sxs-lookup"><span data-stu-id="76cb3-140">They are also used to calculate actual costs that are related to actual consumption of time and material.</span></span> <span data-ttu-id="76cb3-141">Laukiančių išlaidų įrašai naudojami būsimiems komplektavimo specifikacijų (KS) skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="76cb3-141">Pending cost records are used in bill of materials (BOM) calculations for a future date.</span></span> 

<span data-ttu-id="76cb3-142">Dvi išlaidų versijos blokavimo strategijos nustato, ar laukiančios išlaidos gali būti tvarkomos ir ar galima pradėti laukiančias išlaidas.</span><span class="sxs-lookup"><span data-stu-id="76cb3-142">Two blocking policies for a costing version determine whether pending costs can be maintained, and whether the pending cost can be started.</span></span> <span data-ttu-id="76cb3-143">Norėdami leisti tvarkyti duomenis, o vėliau neleisti tvarkyti išlaidų duomenų įkainojimo versijoje, naudokite blokavimo strategijas.</span><span class="sxs-lookup"><span data-stu-id="76cb3-143">Use the blocking policies to permit data maintenance, and then to prevent data maintenance for the cost data in a costing version.</span></span> 

<span data-ttu-id="76cb3-144">Apibrėžus išlaidų lapo formatą ir netiesioginių išlaidų skaičiavimus, reikia atlikti atskirą veiksmą informacijai patikrinti ir išsaugoti.</span><span class="sxs-lookup"><span data-stu-id="76cb3-144">After you define the costing sheet format and calculations for indirect costs, you must perform a separate step to validate and save the information.</span></span> <span data-ttu-id="76cb3-145">Įkainojimo lapas pateikia visos įmonės formatą, skirtą nuolat rodyti parduotų prekių išlaidų informaciją.</span><span class="sxs-lookup"><span data-stu-id="76cb3-145">The costing sheet represents a company-wide format for consistently displaying information about the costs of goods sold.</span></span> 

<span data-ttu-id="76cb3-146">Įkainojimo lapas rodomas kaip puslapio **Skaičiuoti prekės savikainą** dalis.</span><span class="sxs-lookup"><span data-stu-id="76cb3-146">The costing sheet is displayed as part of the **Calculate item cost** page.</span></span> <span data-ttu-id="76cb3-147">Įkainojimo lapas gali būti rodomas gaminamos prekės apskaičiuotų išlaidų įrašui puslapyje **Prekės kaina** arba konkretaus užsakymo skaičiavimo įrašui puslapyje **KS skaičiavimo rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="76cb3-147">The costing sheet can be displayed for a manufactured item’s calculated cost record on the **Item price** page or for an order-specific calculation record on the **BOM calculation results** page.</span></span> <span data-ttu-id="76cb3-148">Taip pat jis gali būti rodomas kaip gamybos užsakymo puslapio **Kainos skaičiavimas** dalis.</span><span class="sxs-lookup"><span data-stu-id="76cb3-148">It can also be displayed as part of the **Price calculation** page for a production order.</span></span>





