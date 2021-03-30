---
title: Gamybos užsakymo savikainos įvertinimas
description: Šiame straipsnyje pateikta informacija apie gamybos savikainos įvertinimą. Gamybos savikainos įvertinime pateiktos numatomo prekės gamybos medžiagų ir pajėgumo suvartojimo išlaidos pagal suplanuotą gamybos užsakymo kiekį.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 881ba7058a22a98d85730fa1f0aa6c38af7d248c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208164"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="36697-104">Gamybos užsakymo savikainos įvertinimas</span><span class="sxs-lookup"><span data-stu-id="36697-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36697-105">Šiame straipsnyje pateikta informacija apie gamybos savikainos įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="36697-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="36697-106">Gamybos savikainos įvertinime pateiktos numatomo prekės gamybos medžiagų ir pajėgumo suvartojimo išlaidos pagal suplanuotą gamybos užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="36697-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="36697-107">Sukūrę gamybos užsakymą, turite įvertinti gamybos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="36697-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="36697-108">Tikslas yra įvertinti prekės ir maršruto suvartojimą gamybos proceso metu, nes šie įvertinimai naudojami kaip tolesnio planavimo ir gamybos procesų pagrindas.</span><span class="sxs-lookup"><span data-stu-id="36697-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="36697-109">Gamybos savikainos įvertinimas</span><span class="sxs-lookup"><span data-stu-id="36697-109">Production cost estimation</span></span>
<span data-ttu-id="36697-110">Gamybos išlaidų įvertinimas pagrįstas šia informacija:</span><span class="sxs-lookup"><span data-stu-id="36697-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="36697-111">Gamybos užsakymo kiekis</span><span class="sxs-lookup"><span data-stu-id="36697-111">The quantity on the production order</span></span>
-   <span data-ttu-id="36697-112">Gamybos komplektavimo specifikacijų (KS) komponentai</span><span class="sxs-lookup"><span data-stu-id="36697-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="36697-113">Gamybos maršruto nukreipimo operacijos</span><span class="sxs-lookup"><span data-stu-id="36697-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="36697-114">Netiesioginės išlaidos, taikomos komponentams ir operacijoms</span><span class="sxs-lookup"><span data-stu-id="36697-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="36697-115">Aktyvių išlaidų duomenys, turimi skaičiavimo dieną</span><span class="sxs-lookup"><span data-stu-id="36697-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="36697-116">Jei gamybos KS yra fiktyvios eilutės prekė, skaičiavimai atspindi fiktyvius komponentus ir maršruto operacijas.</span><span class="sxs-lookup"><span data-stu-id="36697-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="36697-117">Galite naudoti įvertinimo užduotį, norėdami perskaičiuoti įvertintas išlaidas taip, kad jos atspindėtų atnaujintą informaciją.</span><span class="sxs-lookup"><span data-stu-id="36697-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="36697-118">Pvz., atnaujinta informacija gali būti gamybos užsakymo kiekio, gamybos KS komponentų, gamybos maršruto nukreipimo operacijų, netiesioginių išlaidų, taikomų tiems komponentams ir operacijoms, ar aktyviems išlaidų duomenims, turimiems perskaičiavimo dieną, pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="36697-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="36697-119">Be to, įvertintų savikainų skaičiavimai išlaidų ir antkainio sumos būdu gali pateikti gamybos prekės pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="36697-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="36697-120">Papildomai įvertintų išlaidų skaičiavimas gali būti taikomas užsakymams nurodyti, kurie atspindi kitus gamybos užsakymus, susietus su tuo gamybos užsakymu.</span><span class="sxs-lookup"><span data-stu-id="36697-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="36697-121">Peržiūrėkite įvertintas išlaidas</span><span class="sxs-lookup"><span data-stu-id="36697-121">View the estimated costs</span></span>
<span data-ttu-id="36697-122">Atlikę įvertinimą, rezultatus galite peržiūrėti puslapyje **Kainos skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="36697-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="36697-123">Įvertinimo metu apskaičiuojamos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="36697-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="36697-124">**Gamybos išlaidos** – gamybos savikaina yra svarbiausia įvertinimo eilutė.</span><span class="sxs-lookup"><span data-stu-id="36697-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="36697-125">Joje pateikiamos visos gamybos užsakymo išlaidos ir bendra pagamintos prekės pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="36697-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="36697-126">Tai yra visų įvertinimo savikainos eilučių suma.</span><span class="sxs-lookup"><span data-stu-id="36697-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="36697-127">**Maršruto arba išteklių išlaidos** – maršruto arba išteklių išlaidos yra gamybos operacijų išlaidos.</span><span class="sxs-lookup"><span data-stu-id="36697-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="36697-128">Jos apima nustatymo laiko, vykdymo laiko savikainą ir pridėtines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="36697-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="36697-129">**Medžiagų išlaidos** – medžiagų išlaidos yra komplektavimo specifikacijų (KS) komponentų, reikiamų prekei pagaminti, išlaidos ir kainos.</span><span class="sxs-lookup"><span data-stu-id="36697-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="36697-130">Šios išlaidos buvo iš anksto nustatytos ir įvestos į sistemą.</span><span class="sxs-lookup"><span data-stu-id="36697-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="36697-131">Kita savikainos įvertinimo nauda</span><span class="sxs-lookup"><span data-stu-id="36697-131">Other uses of cost estimation</span></span>
<span data-ttu-id="36697-132">Savikainos įvertinime taip pat pateikta ši informacija:</span><span class="sxs-lookup"><span data-stu-id="36697-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="36697-133">reikšmingi kainos pasiūlymai;</span><span class="sxs-lookup"><span data-stu-id="36697-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="36697-134">užsakymo pelningumo įvertinimas;</span><span class="sxs-lookup"><span data-stu-id="36697-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="36697-135">žaliavos suvartojimo įvertinimas;</span><span class="sxs-lookup"><span data-stu-id="36697-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="36697-136">ankstesnių gamybos procesų savikainos informacijos palyginimas;</span><span class="sxs-lookup"><span data-stu-id="36697-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="36697-137">biudžeto ir prognozės informaciją;</span><span class="sxs-lookup"><span data-stu-id="36697-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="36697-138">gamybos apimties, kuri reikalinga tam tikrai savikainai išlaikyti, įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="36697-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]