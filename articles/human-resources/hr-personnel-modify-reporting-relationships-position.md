---
title: Modifikuoti pareigų ataskaitų ryšius
description: Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd884362393674a4f55ea0410548edbb72786fff
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465395"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="4804b-103">Modifikuoti pareigų ataskaitų ryšius</span><span class="sxs-lookup"><span data-stu-id="4804b-103">Modify reporting relationships for a position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="4804b-104">Ši procedūra nurodo, kaip pakeisti darbuotojo ataskaitų ryšį.</span><span class="sxs-lookup"><span data-stu-id="4804b-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="4804b-105">Ataskaitų ryšį galima naudoti dokumentams per darbo eigą nukreipti.</span><span class="sxs-lookup"><span data-stu-id="4804b-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="4804b-106">Procedūra taip pat nurodo, kaip darbuotoją priskirti papildomoms hierarchijoms.</span><span class="sxs-lookup"><span data-stu-id="4804b-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="4804b-107">Pavyzdžiui, darbuotojas gali būti projekto komandos narys ir turėti neoficialų ataskaitų ryšį su projekto vadovu.</span><span class="sxs-lookup"><span data-stu-id="4804b-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="4804b-108">Galima nustatyti papildomus pareigų ataskaitų ryšius, kad veiktų įvairūs projekto arba matricos scenarijai.</span><span class="sxs-lookup"><span data-stu-id="4804b-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="4804b-109">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="4804b-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4804b-110">Pasirinkite Personalas > Pareigos > Pareigos.</span><span class="sxs-lookup"><span data-stu-id="4804b-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="4804b-111">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="4804b-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4804b-112">Pvz., filtruokite lauką Pareigos reikšme „000091“.</span><span class="sxs-lookup"><span data-stu-id="4804b-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="4804b-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4804b-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4804b-114">Išplėskite sekciją Teikia ataskaitas pareigų atstovui.</span><span class="sxs-lookup"><span data-stu-id="4804b-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="4804b-115">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="4804b-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="4804b-116">Lauke Teikia ataskaitas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4804b-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="4804b-117">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="4804b-117">Click Create.</span></span>
8. <span data-ttu-id="4804b-118">Išplėskite sekciją Ryšiai.</span><span class="sxs-lookup"><span data-stu-id="4804b-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="4804b-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4804b-119">Click Add.</span></span>
10. <span data-ttu-id="4804b-120">Tinklelio kairėje pažymėkite žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="4804b-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="4804b-121">Lauke Hierarchijos pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4804b-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="4804b-122">Pavyzdys: projektas</span><span class="sxs-lookup"><span data-stu-id="4804b-122">Example: Project</span></span>  
12. <span data-ttu-id="4804b-123">Lauke Teikia ataskaitas pareigų atstovui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4804b-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="4804b-124">Pavyzdys: 000437</span><span class="sxs-lookup"><span data-stu-id="4804b-124">Example:  000437</span></span>
13. <span data-ttu-id="4804b-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4804b-125">Click Save.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]