---
title: Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą
description: Kompensacijų ir išmokų vadovas gali darbuotojus priskirti pastoviosios atlyginimo dalies planams, kad valdytų jų pagrindinį užmokestį.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 843db6bc133382a701d4b25b164794e57df152c7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010014"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="91d44-103">Darbuotojo įtraukimas į fiksuoto atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="91d44-103">Enroll an employee in a fixed compensation plan</span></span>

<span data-ttu-id="91d44-104">Kompensacijų ir išmokų vadovas gali darbuotojus priskirti pastoviosios atlyginimo dalies planams, kad valdytų jų pagrindinį užmokestį.</span><span class="sxs-lookup"><span data-stu-id="91d44-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="91d44-105">Ši procedūra daro prielaidą, kad fiksuotos dalies planas yra sukurtas ir aktyvus bei kad nustatytos plano tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="91d44-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="91d44-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="91d44-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91d44-107">Norėdami pradėti procedūrą, eikite į Žmogiškieji ištekliai > Darbuotojai > Darbuotojai > Kompensavimas > Fiksuotas planas</span><span class="sxs-lookup"><span data-stu-id="91d44-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="91d44-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="91d44-108">Click New.</span></span>
2. <span data-ttu-id="91d44-109">Lauke Veiksmas pasirinkite Samdos / Pakartotinės samdos tipo pastoviosios atlyginimo dalies veiksmą, kad apibūdintumėte darbuotojo kompensacijos pokytį.</span><span class="sxs-lookup"><span data-stu-id="91d44-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="91d44-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="91d44-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="91d44-111">Lauke Pareigos spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="91d44-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="91d44-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="91d44-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="91d44-113">Lygis rodomas iš Pareigų Darbo Kompensacijos lygio.</span><span class="sxs-lookup"><span data-stu-id="91d44-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="91d44-114">Prieš darbuotojui priskiriant kompensaciją, turi būti nustatytas Darbo lygis.</span><span class="sxs-lookup"><span data-stu-id="91d44-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="91d44-115">Lauke Planas pasirinkite darbuotojo pastoviosios atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="91d44-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="91d44-116">Filtruojama Plano peržvalga, kad būtų rodomi tik tie planai, į kuriuos darbuotojas turi teisę pagal Tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="91d44-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="91d44-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="91d44-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="91d44-118">Pagal numatytąsias nuostatas kompensacijos Įsigaliojimo ir Galiojimo pabaigos datos naudojamos tokios pačios, kaip ir darbuotojo paskyrimo į pareigas pradžios ir pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="91d44-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="91d44-119">Prireikus šias datas galima koreguoti.</span><span class="sxs-lookup"><span data-stu-id="91d44-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="91d44-120">Jei Pastoviosios atlyginimo dalies planas yra veiksmų planas, pasirinkite veiksmą, kuriame yra tinkamas darbuotojo užmokesčio tarifas.</span><span class="sxs-lookup"><span data-stu-id="91d44-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="91d44-121">Jei pastoviosios atlyginimo dalies planas yra kategorijų ar intervalų planas, darbuotojo užmokesčio tarifą įveskite.</span><span class="sxs-lookup"><span data-stu-id="91d44-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="91d44-122">Užmokesčio tarifas bus patikrintas pagal plano leistino nuokrypio nuostatas ir minimalius bei maksimalius darbo kompensacijos lygio atskaitos taškus.</span><span class="sxs-lookup"><span data-stu-id="91d44-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="91d44-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="91d44-123">Click OK.</span></span>

