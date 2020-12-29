---
title: Įvesti projekto tabelius
description: Ši procedūra padeda kurti grafikus naudojant tuščias grafikų formas.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10dbb43cec47a758d11362947f27932a4911911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419742"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="591a8-103">Įvesti projekto tabelius</span><span class="sxs-lookup"><span data-stu-id="591a8-103">Enter project timesheets</span></span>



<span data-ttu-id="591a8-104">Ši procedūra padeda kurti grafikus naudojant tuščias grafikų formas.</span><span class="sxs-lookup"><span data-stu-id="591a8-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="591a8-105">Naujas grafikas gali būti pagrįstas ankstesniojo grafiko arba projekto ir veiklos užduočių informacija puslapyje **Mano parankiniai**.</span><span class="sxs-lookup"><span data-stu-id="591a8-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="591a8-106">Pagal numatytuosius nustatymus, sąrašo puslapis **Visi grafikai** rodo visus jūsų dabartinio laikotarpio grafikus.</span><span class="sxs-lookup"><span data-stu-id="591a8-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="591a8-107">Galite naudoti išplečiamąjį sąrašą, skirtą puslapyje **Mano grafikai** esančiam laukui **Rodyti**, kad filtruotumėte grafikų sąrašą pagal laikotarpį ar projektą, arba kad peržiūrėtumėte kitų darbuotojų vardu sukurtus grafikus.</span><span class="sxs-lookup"><span data-stu-id="591a8-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="591a8-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USSI.</span><span class="sxs-lookup"><span data-stu-id="591a8-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="591a8-109">Parinktyje **Naršymo sritis** eikite į **Moduliai > Projekto valdymas ir apskaita > Grafikai > Mano grafikai**.</span><span class="sxs-lookup"><span data-stu-id="591a8-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="591a8-110">Norėdami įvesti naują grafiką, spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="591a8-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="591a8-111">Pagal numatytuosius parametrus išplečiamajame sąraše Ištekliai rodomas darbuotojas, priskirtas dabartinio vartotojui.</span><span class="sxs-lookup"><span data-stu-id="591a8-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="591a8-112">Jei vartotojas yra nustatomas kaip perėmėjas, bus pateiktos pavardės, kad vartotojas pats galėtų įvesti grafiką.</span><span class="sxs-lookup"><span data-stu-id="591a8-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="591a8-113">Lauke **Data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="591a8-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="591a8-114">Jei ši parinktis pasirinkta, naujos grafiko eilutės bus sukurtos naudojant grafiko parametrus, kurie buvo sukonfigūruoti kaip parankiniai.</span><span class="sxs-lookup"><span data-stu-id="591a8-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="591a8-115">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="591a8-115">Click **OK**.</span></span>
5. <span data-ttu-id="591a8-116">Spustelėkite **Nauja eilutė**.</span><span class="sxs-lookup"><span data-stu-id="591a8-116">Click **New line**.</span></span>
6. <span data-ttu-id="591a8-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="591a8-117">In the list, mark the selected row.</span></span> <span data-ttu-id="591a8-118">Lauke **Juridinis subjektas** rodomas dabartinis juridinis subjektas, nustatytas pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="591a8-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="591a8-119">Lauke **Projektas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="591a8-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="591a8-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="591a8-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="591a8-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="591a8-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="591a8-122">Lauke **Veiklos numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="591a8-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="591a8-123">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="591a8-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="591a8-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="591a8-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="591a8-125">Lauke **Kategorija** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="591a8-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="591a8-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="591a8-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="591a8-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="591a8-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="591a8-128">Įveskite valandų skaičių, dirbtą kiekvieną dieną.</span><span class="sxs-lookup"><span data-stu-id="591a8-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="591a8-129">Įveskite valandas dešimtainių formatu.</span><span class="sxs-lookup"><span data-stu-id="591a8-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="591a8-130">Pvz., jei dirbote dvi valandas ir penkiolika minčių, įveskite 2,25.</span><span class="sxs-lookup"><span data-stu-id="591a8-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="591a8-131">Parinktyje **Išsami eilučių informacija** galimos šios parinktys:</span><span class="sxs-lookup"><span data-stu-id="591a8-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="591a8-132">Pridėti informaciją apie mokesčių ir finansines dimensijas skirtukuose **Bendra** ir **Finansinės dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="591a8-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="591a8-133">Pridėti komentarų apie grafiko eilutę skirtuke **Komentaras**.</span><span class="sxs-lookup"><span data-stu-id="591a8-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="591a8-134">Parinktyje **Veiksmų sritis** spustelėkite **Darbo eiga**, kad atidarytumėte tiesioginio dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="591a8-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="591a8-135">Spustelėkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="591a8-135">Click **Submit**.</span></span>
22. <span data-ttu-id="591a8-136">Spustelėkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="591a8-136">Click **Submit**.</span></span>

