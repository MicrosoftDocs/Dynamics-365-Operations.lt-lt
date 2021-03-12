---
title: Valdyti atostogų laiką
description: Ši procedūra apžvelgia darbuotojų atostogų įrašų kūrimą.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd49e4c1c5c97094061fa119ac1dda99ef69e5e4
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797996"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="5f739-103">Valdyti atostogų laiką</span><span class="sxs-lookup"><span data-stu-id="5f739-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f739-104">Ši procedūra apžvelgia darbuotojų atostogų įrašų kūrimą.</span><span class="sxs-lookup"><span data-stu-id="5f739-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="5f739-105">Galite sekti atostogų, kurių priežastis medicininė, švietimo ar susijusi su tėvų veikla, laiką.</span><span class="sxs-lookup"><span data-stu-id="5f739-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="5f739-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="5f739-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="5f739-107">Pasirinkite Personalas > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="5f739-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="5f739-108">Sąraše pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="5f739-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="5f739-109">Išsamią informaciją apie pasirinktą darbuotoją galite peržiūrėti pasirinkdami darbuotojo vardą ir pavardę.</span><span class="sxs-lookup"><span data-stu-id="5f739-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="5f739-110">Spustelėkite skirtuką Užimtumas.</span><span class="sxs-lookup"><span data-stu-id="5f739-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="5f739-111">Spustelėkite Atostogos.</span><span class="sxs-lookup"><span data-stu-id="5f739-111">Click Leave.</span></span>
6. <span data-ttu-id="5f739-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="5f739-112">Click New.</span></span>
7. <span data-ttu-id="5f739-113">Lauke Atostogų tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5f739-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5f739-114">Formoje Atostogų tipai galite susieti atostogų tipą su pajamų kodu.</span><span class="sxs-lookup"><span data-stu-id="5f739-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="5f739-115">Jei atostogų tipas susietas su pajamų kodu, įvestu atostogų laikotarpiu bus generuojama pajamų eilutė su susietu pajamų kodu.</span><span class="sxs-lookup"><span data-stu-id="5f739-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="5f739-116">Sąraše pasirinkite atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="5f739-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="5f739-117">Pavyzdžiui: įsivaikinimas</span><span class="sxs-lookup"><span data-stu-id="5f739-117">For example: Adoption</span></span>  
9. <span data-ttu-id="5f739-118">Įveskite datą, kada atostogos prasidės.</span><span class="sxs-lookup"><span data-stu-id="5f739-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="5f739-119">Pavyzdys: „2015-10-26‟</span><span class="sxs-lookup"><span data-stu-id="5f739-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="5f739-120">Pavyzdžiui: 2015-10-26</span><span class="sxs-lookup"><span data-stu-id="5f739-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="5f739-121">Įveskite datą, kada atostogos prasidės.</span><span class="sxs-lookup"><span data-stu-id="5f739-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="5f739-122">Pavyzdžiui: 2015-11-20</span><span class="sxs-lookup"><span data-stu-id="5f739-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="5f739-123">Pastabų lauke įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="5f739-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="5f739-124">Pavyzdžiui: įsivaikinimo atostogos</span><span class="sxs-lookup"><span data-stu-id="5f739-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="5f739-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="5f739-125">Click Save.</span></span>

