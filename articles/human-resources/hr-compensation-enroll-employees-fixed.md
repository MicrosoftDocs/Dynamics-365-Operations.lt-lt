---
title: Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą
description: Kompensacijų ir išmokų vadovas gali darbuotojus priskirti pastoviosios atlyginimo dalies planams, kad valdytų jų pagrindinį užmokestį.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a129bf9a6cb6a3ef92597e2ff9d126e3e5ce973b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468256"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="ff933-103">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="ff933-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ff933-104">Kompensacijų ir išmokų vadovas gali darbuotojus priskirti pastoviosios atlyginimo dalies planams, kad valdytų jų pagrindinį užmokestį.</span><span class="sxs-lookup"><span data-stu-id="ff933-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="ff933-105">Ši procedūra daro prielaidą, kad fiksuotos dalies planas yra sukurtas ir aktyvus bei kad nustatytos plano tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="ff933-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="ff933-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ff933-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ff933-107">Norėdami pradėti procedūrą, eikite į Žmogiškieji ištekliai > Darbuotojai > Darbuotojai > Kompensavimas > Fiksuotas planas</span><span class="sxs-lookup"><span data-stu-id="ff933-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="ff933-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ff933-108">Click New.</span></span>
2. <span data-ttu-id="ff933-109">Lauke Veiksmas pasirinkite Samdos / Pakartotinės samdos tipo pastoviosios atlyginimo dalies veiksmą, kad apibūdintumėte darbuotojo kompensacijos pokytį.</span><span class="sxs-lookup"><span data-stu-id="ff933-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="ff933-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ff933-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ff933-111">Lauke Pareigos spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ff933-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ff933-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ff933-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ff933-113">Lygis rodomas iš Pareigų Darbo Kompensacijos lygio.</span><span class="sxs-lookup"><span data-stu-id="ff933-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="ff933-114">Prieš darbuotojui priskiriant kompensaciją, turi būti nustatytas Darbo lygis.</span><span class="sxs-lookup"><span data-stu-id="ff933-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="ff933-115">Lauke Planas pasirinkite darbuotojo pastoviosios atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="ff933-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="ff933-116">Filtruojama Plano peržvalga, kad būtų rodomi tik tie planai, į kuriuos darbuotojas turi teisę pagal Tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="ff933-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="ff933-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ff933-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff933-118">Pagal numatytąsias nuostatas kompensacijos Įsigaliojimo ir Galiojimo pabaigos datos naudojamos tokios pačios, kaip ir darbuotojo paskyrimo į pareigas pradžios ir pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="ff933-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="ff933-119">Prireikus šias datas galima koreguoti.</span><span class="sxs-lookup"><span data-stu-id="ff933-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="ff933-120">Jei Pastoviosios atlyginimo dalies planas yra veiksmų planas, pasirinkite veiksmą, kuriame yra tinkamas darbuotojo užmokesčio tarifas.</span><span class="sxs-lookup"><span data-stu-id="ff933-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="ff933-121">Jei pastoviosios atlyginimo dalies planas yra kategorijų ar intervalų planas, darbuotojo užmokesčio tarifą įveskite.</span><span class="sxs-lookup"><span data-stu-id="ff933-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="ff933-122">Užmokesčio tarifas bus patikrintas pagal plano leistino nuokrypio nuostatas ir minimalius bei maksimalius darbo kompensacijos lygio atskaitos taškus.</span><span class="sxs-lookup"><span data-stu-id="ff933-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="ff933-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ff933-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]