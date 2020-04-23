---
title: Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį
description: Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1086a88c341b95d6af03adc81c4e3e5d76adc69
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210208"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="296a7-103">Darbininko konfigūravimas naudojant mobilųjį užduočių įrenginį</span><span class="sxs-lookup"><span data-stu-id="296a7-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="296a7-104">Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.</span><span class="sxs-lookup"><span data-stu-id="296a7-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="296a7-105">Patikrinkite, ar darbuotojui priskirtas konkretus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="296a7-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="296a7-106">Pavyzdys: prieš sukonfigūruodami darbuotojo abonementą patikrinkite, ar vartotojui „SHANNON“ yra priskirtas mašinos operatoriaus vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="296a7-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="296a7-107">Eikite į **Naršymo sritis > Moduliai > Sistemos administravimas > Užklausos > Paketinė užduotis**.</span><span class="sxs-lookup"><span data-stu-id="296a7-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="296a7-108">Ieškokite vartojo naudodami spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="296a7-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="296a7-109">Šiame pavyzdyje įveskite `shannon`.</span><span class="sxs-lookup"><span data-stu-id="296a7-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="296a7-110">Stulpelyje **Vartotojo ID** pasirinkite atsirandančios vartotojo paskyros saitą.</span><span class="sxs-lookup"><span data-stu-id="296a7-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="296a7-111">Medyje **Vartotojo vaidmenys** pasirinkite **Vaidmenys > Mašinų operatorius**.</span><span class="sxs-lookup"><span data-stu-id="296a7-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="296a7-112">Uždarykite puslapius **Vartotojo duomenys** ir **Vartotojai**, kad grįžtumėte į pradžios puslapį.</span><span class="sxs-lookup"><span data-stu-id="296a7-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="296a7-113">Konfigūruokite darbuotojo abonementą.</span><span class="sxs-lookup"><span data-stu-id="296a7-113">Configure worker account</span></span>
1. <span data-ttu-id="296a7-114">Eikite į **Naršymo sritis > Moduliai > Žmogiškieji ištekliai > Darbuotojai > Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="296a7-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="296a7-115">Ieškokite vartojo naudodami spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="296a7-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="296a7-116">Šiame pavyzdyje įveskite `shannon`.</span><span class="sxs-lookup"><span data-stu-id="296a7-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="296a7-117">Atsidariusiame vartotojo paskyros stulpelyje **Pavadinimas** pasirinkite saitą.</span><span class="sxs-lookup"><span data-stu-id="296a7-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="296a7-118">Pasirinkite skirtuką **Laiko registracija**.</span><span class="sxs-lookup"><span data-stu-id="296a7-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="296a7-119">Pasirinkite **Suaktyvinti registruojant terminalus**.</span><span class="sxs-lookup"><span data-stu-id="296a7-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="296a7-120">Šiuose laukuose pasirinkite vertes:</span><span class="sxs-lookup"><span data-stu-id="296a7-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="296a7-121">**Skaičiavimo grupė**</span><span class="sxs-lookup"><span data-stu-id="296a7-121">**Calculation group**</span></span>  
    - <span data-ttu-id="296a7-122">**Numatytoji skaičiavimo grupė**</span><span class="sxs-lookup"><span data-stu-id="296a7-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="296a7-123">**Patvirtinimo grupė**</span><span class="sxs-lookup"><span data-stu-id="296a7-123">**Approval group**</span></span>  
    - <span data-ttu-id="296a7-124">**Standartinis šablonas**</span><span class="sxs-lookup"><span data-stu-id="296a7-124">**Standard profile**</span></span>  
    - <span data-ttu-id="296a7-125">**Šablono grupė**</span><span class="sxs-lookup"><span data-stu-id="296a7-125">**Profile group**</span></span>  

7. <span data-ttu-id="296a7-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="296a7-126">Select **OK**.</span></span>
8. <span data-ttu-id="296a7-127">Spustelėję **Redaguoti** įveskite naujos laiko registracijos darbuotojo ženklo numerį.</span><span class="sxs-lookup"><span data-stu-id="296a7-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="296a7-128">Lauke **Ženklo ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="296a7-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="296a7-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="296a7-129">Select **Save**.</span></span>
10. <span data-ttu-id="296a7-130">Uždarykite puslapius **Darbuotojo informacija** ir **Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="296a7-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="296a7-131">Priskirkite darbuotoją prie įrenginio grupės.</span><span class="sxs-lookup"><span data-stu-id="296a7-131">Assign worker to device group</span></span>
1. <span data-ttu-id="296a7-132">Eikite į **Gamybos kontrolė > Sąranka > Gamybos vykdymas > Konfigūruoti įrenginių užduoties kortelę**.</span><span class="sxs-lookup"><span data-stu-id="296a7-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="296a7-133">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="296a7-133">Select **Add**.</span></span>
3. <span data-ttu-id="296a7-134">Sąraše pasirinkite norimą vertinimo modelį.</span><span class="sxs-lookup"><span data-stu-id="296a7-134">In the list, select the desired worker.</span></span> <span data-ttu-id="296a7-135">Šiame pavyzdyje pasirinkite **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="296a7-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="296a7-136">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="296a7-136">Select **OK**.</span></span>
5. <span data-ttu-id="296a7-137">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="296a7-137">Select **Edit**.</span></span>
6. <span data-ttu-id="296a7-138">Lauke **Gamybos vienetas** galite nustatyti numatytąjį darbuotojo filtrą.</span><span class="sxs-lookup"><span data-stu-id="296a7-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="296a7-139">Tai užtikrins, kad bus rodomos tik pasirinkto gamybos vieneto gamybos užduotys, kai darbuotojas prisiregistruoja prie įrenginio.</span><span class="sxs-lookup"><span data-stu-id="296a7-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="296a7-140">Įvesti reikšmę.</span><span class="sxs-lookup"><span data-stu-id="296a7-140">Enter the desired value.</span></span>
7. <span data-ttu-id="296a7-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="296a7-141">Close the page.</span></span>

