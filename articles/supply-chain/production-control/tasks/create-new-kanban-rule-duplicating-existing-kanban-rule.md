---
title: Kurti naują „kanban“ taisyklę dubliuojant esamą „kanban“ taisyklę
description: Šioje procedūroje didžiausias dėmesys skiriamas esamos „kanban“ taisyklės kopijos kūrimui.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aef2725152d39e49070f33d0c56089200c94353
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837811"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="fb055-103">Kurti naują „kanban“ taisyklę dubliuojant esamą „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="fb055-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb055-104">Šioje procedūroje didžiausias dėmesys skiriamas esamos „kanban“ taisyklės kopijos kūrimui.</span><span class="sxs-lookup"><span data-stu-id="fb055-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="fb055-105">Tai naudinga, jei norite kurti naujas „kanban“ taisykles pagal esamas „kanban“ taisykles.</span><span class="sxs-lookup"><span data-stu-id="fb055-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="fb055-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="fb055-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fb055-107">Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia pakeistos gamybos eigos arba naujos papildymo taisyklės gamybą.</span><span class="sxs-lookup"><span data-stu-id="fb055-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="fb055-108">Pasirinkite „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="fb055-108">Select a kanban rule</span></span>
1. <span data-ttu-id="fb055-109">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="fb055-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="fb055-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="fb055-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fb055-111">Pasirinkite produkto M0006 „kanban“ taisyklę 000017.</span><span class="sxs-lookup"><span data-stu-id="fb055-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="fb055-112">„Kanban“ taisyklės kopijavimas</span><span class="sxs-lookup"><span data-stu-id="fb055-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="fb055-113">Spustelėkite „Kanban“ taisyklės kopijavimas.</span><span class="sxs-lookup"><span data-stu-id="fb055-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="fb055-114">Dauginant „kanban“ taisyklę galima pasirinkti ir pakeisti tipą, datas, veiklas ir produktą.</span><span class="sxs-lookup"><span data-stu-id="fb055-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="fb055-115">Kitame veiksme pakeiskite šios procedūros produktą.</span><span class="sxs-lookup"><span data-stu-id="fb055-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="fb055-116">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fb055-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="fb055-117">Pažymėkite M0007.</span><span class="sxs-lookup"><span data-stu-id="fb055-117">Select M0007.</span></span>  
3. <span data-ttu-id="fb055-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fb055-118">Click OK.</span></span>
    * <span data-ttu-id="fb055-119">Atkreipkite dėmesį, kad sukuriama „kanban“ taisyklės 000017 kopija.</span><span class="sxs-lookup"><span data-stu-id="fb055-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

