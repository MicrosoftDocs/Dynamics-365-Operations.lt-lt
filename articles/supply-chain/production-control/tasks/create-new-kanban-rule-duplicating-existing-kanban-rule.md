---
title: Kurti naują „kanban“ taisyklę dubliuojant esamą „kanban“ taisyklę
description: Šioje procedūroje didžiausias dėmesys skiriamas esamos „kanban“ taisyklės kopijos kūrimui.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b89fca4e55aa852bd127eb9b1bda07c0e5bcdc0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255138"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="81430-103">Kurti naują „kanban“ taisyklę dubliuojant esamą „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="81430-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81430-104">Šioje procedūroje didžiausias dėmesys skiriamas esamos „kanban“ taisyklės kopijos kūrimui.</span><span class="sxs-lookup"><span data-stu-id="81430-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="81430-105">Tai naudinga, jei norite kurti naujas „kanban“ taisykles pagal esamas „kanban“ taisykles.</span><span class="sxs-lookup"><span data-stu-id="81430-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="81430-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="81430-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="81430-107">Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia pakeistos gamybos eigos arba naujos papildymo taisyklės gamybą.</span><span class="sxs-lookup"><span data-stu-id="81430-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="81430-108">Pasirinkite „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="81430-108">Select a kanban rule</span></span>
1. <span data-ttu-id="81430-109">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="81430-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="81430-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="81430-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81430-111">Pasirinkite produkto M0006 „kanban“ taisyklę 000017.</span><span class="sxs-lookup"><span data-stu-id="81430-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="81430-112">„Kanban“ taisyklės kopijavimas</span><span class="sxs-lookup"><span data-stu-id="81430-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="81430-113">Spustelėkite „Kanban“ taisyklės kopijavimas.</span><span class="sxs-lookup"><span data-stu-id="81430-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="81430-114">Dauginant „kanban“ taisyklę galima pasirinkti ir pakeisti tipą, datas, veiklas ir produktą.</span><span class="sxs-lookup"><span data-stu-id="81430-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="81430-115">Kitame veiksme pakeiskite šios procedūros produktą.</span><span class="sxs-lookup"><span data-stu-id="81430-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="81430-116">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="81430-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="81430-117">Pažymėkite M0007.</span><span class="sxs-lookup"><span data-stu-id="81430-117">Select M0007.</span></span>  
3. <span data-ttu-id="81430-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="81430-118">Click OK.</span></span>
    * <span data-ttu-id="81430-119">Atkreipkite dėmesį, kad sukuriama „kanban“ taisyklės 000017 kopija.</span><span class="sxs-lookup"><span data-stu-id="81430-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]