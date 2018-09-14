--- 
title: "Konfigūruoti darbuotoją naudojant mobilųjį užduoties įrenginį"
description: "Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="67cf8-103">Konfigūruoti darbuotoją naudojant mobilųjį užduoties įrenginį</span><span class="sxs-lookup"><span data-stu-id="67cf8-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67cf8-104">Ši procedūra nurodo, kaip priskirti tinkamas roles darbuotojo vartotojo abonementui, tada įgalinti darbuotoją atlikti darbo laiko kontrolės registraciją.</span><span class="sxs-lookup"><span data-stu-id="67cf8-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="67cf8-105">Priskirti vaidmenis vartotojo abonementui</span><span class="sxs-lookup"><span data-stu-id="67cf8-105">Assign roles to user account</span></span>
1. <span data-ttu-id="67cf8-106">Pasirinkite Sistemos administravimas > Vartotojai > Vartotojai.</span><span class="sxs-lookup"><span data-stu-id="67cf8-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="67cf8-107">Naudokite Spartųjį filtrą darbuotojo vardui filtruoti, kai vartotojo abonementas yra susietas su mašinų operatorius vaidmeniu.</span><span class="sxs-lookup"><span data-stu-id="67cf8-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="67cf8-108">Demonstraciniuose duomenyse vardas yra Shannon.</span><span class="sxs-lookup"><span data-stu-id="67cf8-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="67cf8-109">Pažymėkite vartotojo abonemento įrašą.</span><span class="sxs-lookup"><span data-stu-id="67cf8-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="67cf8-110">Sąraše spustelėję nuorodą „Pavadinimas“ pasirinktoje eilutėje peržiūrėkite vartotojo abonemento informaciją.</span><span class="sxs-lookup"><span data-stu-id="67cf8-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="67cf8-111">Medyje pasirinkite 'vaidmenys \ mašinos operatorius'.</span><span class="sxs-lookup"><span data-stu-id="67cf8-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="67cf8-112">Uždarykite vartotojo abonemento informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-112">Close the user account details page.</span></span>
7. <span data-ttu-id="67cf8-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="67cf8-114">Konfigūruokite darbuotojo abonementą.</span><span class="sxs-lookup"><span data-stu-id="67cf8-114">Configure worker account.</span></span>
1. <span data-ttu-id="67cf8-115">Pasirinkite Personalas > Darbuotojai > Darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="67cf8-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="67cf8-116">Naudokite Spartųjį filtrą darbuotojo vardui filtruoti, kai vartotojo abonementas yra susietas su mašinų operatorius vaidmeniu.</span><span class="sxs-lookup"><span data-stu-id="67cf8-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="67cf8-117">Demonstraciniuose duomenyse vardas yra Shannon.</span><span class="sxs-lookup"><span data-stu-id="67cf8-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="67cf8-118">Pažymėkite vartotojo abonemento įrašą.</span><span class="sxs-lookup"><span data-stu-id="67cf8-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="67cf8-119">Sąraše spustelėję nuorodą „Pavadinimas“ pasirinktoje eilutėje peržiūrėkite vartotojo abonemento informaciją.</span><span class="sxs-lookup"><span data-stu-id="67cf8-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="67cf8-120">Spustelėkite skirtuką Užimtumas.</span><span class="sxs-lookup"><span data-stu-id="67cf8-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="67cf8-121">Išplėskite Laiko registravimo „FastTab“ ir registracijos terminaluose spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="67cf8-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="67cf8-122">Spustelėkite Suaktyvinti registravimo terminaluose.</span><span class="sxs-lookup"><span data-stu-id="67cf8-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="67cf8-123">Lauke Skaičiavimo grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="67cf8-124">Lauke Numatytoji skaičiavimo grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="67cf8-125">Lauke Patvirtinimo grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="67cf8-126">Lauke Standartinis profilis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="67cf8-127">Lauke Profilio grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="67cf8-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="67cf8-128">Click OK.</span></span>
14. <span data-ttu-id="67cf8-129">Spustelėję Redaguoti įveskite naujos laiko registracijos darbuotojo ženklo numerį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="67cf8-130">Lauke Ženklo ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="67cf8-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="67cf8-131">Click Save.</span></span>
17. <span data-ttu-id="67cf8-132">Naudokite nuorodą „SaveRecord“.</span><span class="sxs-lookup"><span data-stu-id="67cf8-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="67cf8-133">Uždarykite darbuotojo informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-133">Close the worker details page.</span></span>
19. <span data-ttu-id="67cf8-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="67cf8-135">Priskirkite darbuotoją prie įrenginio grupės.</span><span class="sxs-lookup"><span data-stu-id="67cf8-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="67cf8-136">Pasirinkite Gamybos kontrolė > Nustatymas > Gamybos vykdymas > Konfigūruoti užduoties kortelę įrenginiams.</span><span class="sxs-lookup"><span data-stu-id="67cf8-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="67cf8-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="67cf8-137">Click Add.</span></span>
3. <span data-ttu-id="67cf8-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="67cf8-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="67cf8-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="67cf8-139">Click OK.</span></span>
5. <span data-ttu-id="67cf8-140">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="67cf8-140">Click Edit.</span></span>
6. <span data-ttu-id="67cf8-141">Lauke Gamybos vienetas galite nustatyti numatytąjį darbuotojo filtrą.</span><span class="sxs-lookup"><span data-stu-id="67cf8-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="67cf8-142">Tai užtikrins, kad bus rodomos tik pasirinkto gamybos vieneto gamybos užduotys, kai darbuotojas prisiregistruoja prie įrenginio.</span><span class="sxs-lookup"><span data-stu-id="67cf8-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="67cf8-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67cf8-143">Close the page.</span></span>


