---
title: Apskaičiuoti KS naudojant vieno lygio struktūrą (2016 m. vasario mėn.)
description: Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant vieno lygio išskleidimą, paremtą įkainojimo lapu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f74f8e4efc4474693f0a5b543c1300c3b64ecda0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "361595"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a><span data-ttu-id="f1f8c-103">Apskaičiuoti KS naudojant vieno lygio struktūrą (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="f1f8c-103">Calculate a BOM by using a single level structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1f8c-104">Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant vieno lygio išskleidimą, paremtą įkainojimo lapu.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="f1f8c-105">Tai šeštoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="f1f8c-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f1f8c-107">Eikite į Išleisti produktai.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-107">Go to Released products.</span></span>
2. <span data-ttu-id="f1f8c-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f1f8c-109">Pasirinkite produktą BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="f1f8c-110">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="f1f8c-111">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-111">Click Item price.</span></span>
5. <span data-ttu-id="f1f8c-112">Spustelėkite Skaičiuoti prekės savikainą.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="f1f8c-113">Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="f1f8c-114">Lauke Įkainojimo versija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f1f8c-115">Norėdami pademonstruoti, pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-115">For this demo, select 10.</span></span> <span data-ttu-id="f1f8c-116">Tai ta pati įkainojimo versija, naudojama savikainai į komponentus įtraukti.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="f1f8c-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-117">Click OK.</span></span>
8. <span data-ttu-id="f1f8c-118">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-118">Click View calculation details.</span></span>
    * <span data-ttu-id="f1f8c-119">Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="f1f8c-120">Čia yra išlaidų sudėtis: • 10 kilęs iš ITEM_A, ITEM_B, 10 BOM_2 iš 10.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="f1f8c-121">Šiuo atveju nėra išsamios informacijos apie BOM_2, nes jis nebuvo apskaičiuotas – tik įvesta BOM_2 standartinės savikainos reikšmė 10.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="f1f8c-122">•  7 išvedamas iš nustatymo laiko, kuris yra pastovios išlaidos, o papildomas 7 išvedamas iš apdorojimo laiko operacijos (Apdoroti).</span><span class="sxs-lookup"><span data-stu-id="f1f8c-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="f1f8c-123">•  Taip pat yra kitų sumų, sutampančių su netiesioginėmis išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="f1f8c-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. <span data-ttu-id="f1f8c-124">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="f1f8c-124">@SysTaskRecorder:_RequestClose</span></span>

