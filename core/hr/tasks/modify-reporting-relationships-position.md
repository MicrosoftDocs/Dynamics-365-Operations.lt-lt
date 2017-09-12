--- 
title: "Modifikuoti pareigų ataskaitų ryšius"
description: "Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 002fffc7e8c3186eedf9060d36d2b4a77749da98
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="85398-103">Modifikuoti pareigų ataskaitų ryšius</span><span class="sxs-lookup"><span data-stu-id="85398-103">Modify reporting relationships for a position</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85398-104">Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį.</span><span class="sxs-lookup"><span data-stu-id="85398-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="85398-105">Ataskaitų ryšį galima naudoti dokumentams per darbo eigą nukreipti.</span><span class="sxs-lookup"><span data-stu-id="85398-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="85398-106">Procedūra taip pat nurodo, kaip darbuotoją priskirti papildomoms hierarchijoms.</span><span class="sxs-lookup"><span data-stu-id="85398-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="85398-107">Pavyzdžiui, darbuotojas gali būti projekto komandos narys ir turėti neoficialų ataskaitų ryšį su projekto vadovu.</span><span class="sxs-lookup"><span data-stu-id="85398-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="85398-108">Galima nustatyti papildomus pareigų ataskaitų ryšius, kad veiktų įvairūs projekto arba matricos scenarijai.</span><span class="sxs-lookup"><span data-stu-id="85398-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="85398-109">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="85398-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="85398-110">Pasirinkite Personalas > Pareigos > Pareigos.</span><span class="sxs-lookup"><span data-stu-id="85398-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="85398-111">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="85398-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="85398-112">Pvz., filtruokite lauką Pareigos reikšme „000091“.</span><span class="sxs-lookup"><span data-stu-id="85398-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="85398-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="85398-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="85398-114">Išplėskite sekciją Teikia ataskaitas pareigų atstovui.</span><span class="sxs-lookup"><span data-stu-id="85398-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="85398-115">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="85398-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="85398-116">Lauke Teikia ataskaitas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85398-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="85398-117">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="85398-117">Click Create.</span></span>
8. <span data-ttu-id="85398-118">Išplėskite sekciją Ryšiai.</span><span class="sxs-lookup"><span data-stu-id="85398-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="85398-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="85398-119">Click Add.</span></span>
10. <span data-ttu-id="85398-120">Tinklelio kairėje pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="85398-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="85398-121">Lauke Hierarchijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85398-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="85398-122">Pavyzdys: projektas</span><span class="sxs-lookup"><span data-stu-id="85398-122">Example: Project</span></span>  
12. <span data-ttu-id="85398-123">Lauke Teikia ataskaitas pareigų atstovui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85398-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="85398-124">Pavyzdys: 000437</span><span class="sxs-lookup"><span data-stu-id="85398-124">Example:  000437</span></span>
13. <span data-ttu-id="85398-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="85398-125">Click Save.</span></span>


