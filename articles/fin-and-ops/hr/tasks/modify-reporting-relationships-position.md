--- 
title: "Pareigų ataskaitų ryšių modifikavimas"
description: "Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 2e52552ec5bce957ac43c2e34ac9a0e42829accd
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="modify-the-reporting-relationships-for-positions"></a><span data-ttu-id="c8509-103">Pareigų ataskaitų ryšių modifikavimas</span><span class="sxs-lookup"><span data-stu-id="c8509-103">Modify the reporting relationships for positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8509-104">Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį.</span><span class="sxs-lookup"><span data-stu-id="c8509-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="c8509-105">Ataskaitų ryšį galima naudoti dokumentams per darbo eigą nukreipti.</span><span class="sxs-lookup"><span data-stu-id="c8509-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="c8509-106">Procedūra taip pat nurodo, kaip darbuotoją priskirti papildomoms hierarchijoms.</span><span class="sxs-lookup"><span data-stu-id="c8509-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="c8509-107">Pavyzdžiui, darbuotojas gali būti projekto komandos narys ir turėti neoficialų ataskaitų ryšį su projekto vadovu.</span><span class="sxs-lookup"><span data-stu-id="c8509-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="c8509-108">Galima nustatyti papildomus pareigų ataskaitų ryšius, kad veiktų įvairūs projekto arba matricos scenarijai.</span><span class="sxs-lookup"><span data-stu-id="c8509-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="c8509-109">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="c8509-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c8509-110">Pasirinkite Personalas > Pareigos > Pareigos.</span><span class="sxs-lookup"><span data-stu-id="c8509-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="c8509-111">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="c8509-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c8509-112">Pvz., filtruokite lauką Pareigos reikšme „000091“.</span><span class="sxs-lookup"><span data-stu-id="c8509-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="c8509-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c8509-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c8509-114">Išplėskite sekciją Teikia ataskaitas pareigų atstovui.</span><span class="sxs-lookup"><span data-stu-id="c8509-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="c8509-115">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c8509-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="c8509-116">Lauke Teikia ataskaitas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8509-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="c8509-117">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="c8509-117">Click Create.</span></span>
8. <span data-ttu-id="c8509-118">Išplėskite sekciją Ryšiai.</span><span class="sxs-lookup"><span data-stu-id="c8509-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="c8509-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="c8509-119">Click Add.</span></span>
10. <span data-ttu-id="c8509-120">Tinklelio kairėje pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="c8509-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="c8509-121">Lauke Hierarchijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8509-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="c8509-122">Pavyzdys: projektas</span><span class="sxs-lookup"><span data-stu-id="c8509-122">Example: Project</span></span>  
12. <span data-ttu-id="c8509-123">Lauke Teikia ataskaitas pareigų atstovui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c8509-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="c8509-124">Pavyzdys: 000437</span><span class="sxs-lookup"><span data-stu-id="c8509-124">Example:  000437</span></span>
13. <span data-ttu-id="c8509-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c8509-125">Click Save.</span></span>


