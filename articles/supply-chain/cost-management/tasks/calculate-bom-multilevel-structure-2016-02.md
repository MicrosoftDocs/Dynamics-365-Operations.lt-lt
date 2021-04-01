---
title: Apskaičiuoti KS naudojant kelių lygių struktūrą (2016 m. vasario mėn.)
description: Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant kelių lygių išskleidimą, paremtą įkainojimo lapu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbbc1e3c7941fd12991f1f6eaec4e9daf35fde9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239515"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="1c049-103">Apskaičiuoti KS naudojant kelių lygių struktūrą (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="1c049-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c049-104">Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant kelių lygių išskleidimą, paremtą įkainojimo lapu.</span><span class="sxs-lookup"><span data-stu-id="1c049-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="1c049-105">Tai septintoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="1c049-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="1c049-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="1c049-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="1c049-107">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="1c049-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1c049-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1c049-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1c049-109">Pasirinkite produktą BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1c049-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="1c049-110">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="1c049-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="1c049-111">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="1c049-111">Click Item price.</span></span>
5. <span data-ttu-id="1c049-112">Spustelėkite Skaičiuoti prekės savikainą.</span><span class="sxs-lookup"><span data-stu-id="1c049-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="1c049-113">Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.</span><span class="sxs-lookup"><span data-stu-id="1c049-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="1c049-114">Lauke Įkainojimo versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1c049-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="1c049-115">Pasirinkite įkainojimo versijos reikšmę 20, nes jos suplanuotų išlaidų tipas ir išskleidimo režimas yra kelių lygių.</span><span class="sxs-lookup"><span data-stu-id="1c049-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="1c049-116">Kelių lygių išskleidimo režimas skirtas suplanuotoms išlaidoms ir modeliavimui.</span><span class="sxs-lookup"><span data-stu-id="1c049-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="1c049-117">Jis nenaudojamas standartinei savikainai.</span><span class="sxs-lookup"><span data-stu-id="1c049-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="1c049-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1c049-118">Click OK.</span></span>
8. <span data-ttu-id="1c049-119">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="1c049-119">Click View calculation details.</span></span>
    * <span data-ttu-id="1c049-120">Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.</span><span class="sxs-lookup"><span data-stu-id="1c049-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="1c049-121">Šiuo atveju atkreipkite dėmesį, kaip apskaičiuota BOM_2 atsižvelgiant į žaliavas, procesą ir pridėtines išlaidas (iš viso – 29,40) vietoj standartinės savikainos – 10, suaktyvintos pradiniame šios serijos užduočių vadove.</span><span class="sxs-lookup"><span data-stu-id="1c049-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="1c049-122">Spustelėkite skirtuką Įkainojimo lapas.</span><span class="sxs-lookup"><span data-stu-id="1c049-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="1c049-123">Perėjus į skirtuką Įkainojimo lapas, išlaidų grupės bendrosios sumos skiriasi lyginant su ankstesniame užduočių vadove atliktu skaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="1c049-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="1c049-124">Lauke „Lygis” pasirinkite „Keli”.</span><span class="sxs-lookup"><span data-stu-id="1c049-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="1c049-125">Pasirinkus Keli, išlaidos klasifikuojamos pagal BOM_2 sudėtį, kur 10 išvedamas iš M1 išlaidų grupės (ITEM_C), o 15,60 išvedama iš jos gamybos, kur išlaidų grupė yra L2.</span><span class="sxs-lookup"><span data-stu-id="1c049-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="1c049-126">Netiesioginės išlaidos taip pat skiriasi.</span><span class="sxs-lookup"><span data-stu-id="1c049-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="1c049-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c049-127">Close the page.</span></span>
12. <span data-ttu-id="1c049-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1c049-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]