---
title: Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą
description: Kompensacijų ir išmokų vadovas gali darbuotojus įtraukti į kintamosios atlyginimo dalies planus, kad būtų galima apskaičiuoti darbuotojų grynųjų pinigų ir negrynųjų pinigų premijas.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d120f8bb52252956d75178d2ffac6ab632385e00
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179135"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="117db-103">Darbuotojo įtraukimas į kintamosios atlyginimo dalies planą</span><span class="sxs-lookup"><span data-stu-id="117db-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="117db-104">Kompensacijų ir išmokų vadovas gali darbuotojus įtraukti į kintamosios atlyginimo dalies planus, kad būtų galima apskaičiuoti darbuotojų grynųjų pinigų ir negrynųjų pinigų premijas.</span><span class="sxs-lookup"><span data-stu-id="117db-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="117db-105">Ši procedūra daro prielaidą, kad kintamosios atlyginimo dalies planas sukurtas ir jo laukas Leisti registraciją nustatytas į Taip bei sukurtos to kintamosios atlyginimo dalies plano tinkamumo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="117db-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="117db-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="117db-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="117db-107">Norėdami pradėti šią procedūrą, pasirinkite Personalas > Darbuotojai > Darbuotojai > Kompensavimas > Kintamojo plano registracija</span><span class="sxs-lookup"><span data-stu-id="117db-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="117db-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="117db-108">Click New.</span></span>
2. <span data-ttu-id="117db-109">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="117db-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="117db-110">Bus filtruojama plano peržvalga, kad būtų rodomi tik tie kintamosios atlyginimo dalies planai, į kuriuos darbuotojas turi teisę pagal tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="117db-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="117db-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="117db-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="117db-112">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="117db-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="117db-113">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="117db-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="117db-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="117db-114">Click Save.</span></span>
7. <span data-ttu-id="117db-115">Perjunkite dalies Nepaisymai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="117db-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="117db-116">Neprivaloma: kai nurodyta pasirinkto kintamojo plano samdos taisyklė yra Procentas, galima nustatyti, kad samdos taisyklės data nepaisytų darbuotojo samdos datos.</span><span class="sxs-lookup"><span data-stu-id="117db-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="117db-117">Jei kintamasis planas yra pagrindinio plano procentas, galima nepaisyti darbuotojo premijos procento.</span><span class="sxs-lookup"><span data-stu-id="117db-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="117db-118">Jei kintamosios atlyginimo dalies planas yra vienetų skaičiaus planas, galima nepaisyti darbuotojo vienetų skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="117db-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="117db-119">Jei darbuotojui turėtų būti skirta standartinė premijos suma, ją galite nustatyti čia.</span><span class="sxs-lookup"><span data-stu-id="117db-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="117db-120">Perjunkite dalies Organizacijos struktūros nepaisymai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="117db-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="117db-121">Jei, vertinant darbuotojo našumą, reikėtų atsižvelgti į kitų skyrių našumą, ar kito, ne darbuotojo pareigoms priskirto skyriaus našumą, skyriaus galima nepaisyti.</span><span class="sxs-lookup"><span data-stu-id="117db-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="117db-122">Visa Procento stulpelio suma turėtų būti 100.</span><span class="sxs-lookup"><span data-stu-id="117db-122">The Percent column should total 100.</span></span>  

