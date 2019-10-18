---
title: Laiko ir lankomumo valdymo planavimas dalyje Mažmeninė prekyba
description: Šioje temoje aprašomi scenarijai, palaikomi modulyje laiko ir lankomumo valdymas programoje „Dynamics 365 Retail“.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d541de550df41b7d4616492960bd4f2aae46d45e
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024988"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="6fcd1-103">Laiko ir lankomumo valdymo planavimas dalyje Mažmeninė prekyba</span><span class="sxs-lookup"><span data-stu-id="6fcd1-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6fcd1-104">Šioje temoje aprašomi scenarijai, palaikomi modulyje laiko ir lankomumo valdymas programoje „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-104">This topic describes the scenarios that are supported for time and attendance management in Dynamics 365 Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="6fcd1-105">Valdyti darbininko nustatymą ir planavimą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="6fcd1-106"> pradinė konfigūracija</span><span class="sxs-lookup"><span data-stu-id="6fcd1-106">Initial configuration</span></span>

- <span data-ttu-id="6fcd1-107">Paleiskite konfigūracijos vedlį.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="6fcd1-108">Registruokite darbuotojus kaip laiko registracijos darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="6fcd1-109">Planuokite darbuotojų grafikus</span><span class="sxs-lookup"><span data-stu-id="6fcd1-109">Plan worker schedules</span></span>

- <span data-ttu-id="6fcd1-110">Taikykite šablonus naudodami darbo planuotoją.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="6fcd1-111">Daugiau informacijos žr. [Šablonų taikymas naudojant darbo planuotoją](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fcd1-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="6fcd1-112">Informacijos apie konfigūravimo veiksmus žr. [Laiko ir buvimo darbe nustatymas](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fcd1-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="6fcd1-113">Konkretus mažmeninės prekybos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="6fcd1-113">Retail-specific configuration</span></span>

- <span data-ttu-id="6fcd1-114">Įjunkite laikrodžio funkcijų šabloną darbuotojams, kuriems norite leisti laiko registravimus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="6fcd1-115">Spustelėkite **EKA funkcijų šablonai** &gt; **Funkcijos** &gt; **EKA laiko registravimai** &gt; **Įjungti laiko registravimus**.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="6fcd1-116">Sukonfigūruokite elektroninio kasos aparato (EKA) teisių grupes, kad leistumėte teisę Peržiūrėti laikrodžio įrašus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="6fcd1-117">Naudodamas šią teisę vartotojas gali peržiūrėti kitų parduotuvės (ir bet kurios kitos parduotuvės, su kuria vartotojas susietas per adresų knygelę) darbuotojų laikrodžio registravimus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="6fcd1-118">Galite įjungti šią teisę vadovo vaidmeniui, bet ne kasininko vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="6fcd1-119">Spustelėkite **EKA teisių grupės** &gt; **Peržiūrėti laikrodžio įrašus**.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="6fcd1-120">Registracijos laikas</span><span class="sxs-lookup"><span data-stu-id="6fcd1-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="6fcd1-121">Kasininko ir ne kasininko laiko registravimai</span><span class="sxs-lookup"><span data-stu-id="6fcd1-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="6fcd1-122">EKA</span><span class="sxs-lookup"><span data-stu-id="6fcd1-122">On POS:</span></span>

    - <span data-ttu-id="6fcd1-123">Atėjimo į darbą operacijos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-123">Clock-in operations:</span></span>

        - <span data-ttu-id="6fcd1-124">Prisijunkite naudodami ne stalčiaus operaciją arba naują pamainą.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="6fcd1-125">Pasirinkite laikrodžio operaciją.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="6fcd1-126">Pasirinkite norimą operaciją.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-126">Select a desired operation:</span></span>

            - <span data-ttu-id="6fcd1-127">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-127">Clock-in</span></span>
            - <span data-ttu-id="6fcd1-128">Darbo pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-128">Break for Work</span></span>
            - <span data-ttu-id="6fcd1-129">Pietų pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-129">Break for Lunch</span></span>
            - <span data-ttu-id="6fcd1-130">Išėjimas iš darbo</span><span class="sxs-lookup"><span data-stu-id="6fcd1-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="6fcd1-131">Dabartinė būsena</span><span class="sxs-lookup"><span data-stu-id="6fcd1-131">Current state</span></span></th>
        <th><span data-ttu-id="6fcd1-132">Galimos operacijos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="6fcd1-133">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="6fcd1-134">Darbo pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-134">Break for Work</span></span></li>
        <li><span data-ttu-id="6fcd1-135">Pietų pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="6fcd1-136">Išėjimas iš darbo</span><span class="sxs-lookup"><span data-stu-id="6fcd1-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="6fcd1-137">Darbo pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-137">Break for Work</span></span></td>
        <td><span data-ttu-id="6fcd1-138">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="6fcd1-139">Pietų pertrauka</span><span class="sxs-lookup"><span data-stu-id="6fcd1-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="6fcd1-140">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="6fcd1-141">Išėjimas iš darbo</span><span class="sxs-lookup"><span data-stu-id="6fcd1-141">Clock-out</span></span></td>
        <td><span data-ttu-id="6fcd1-142">Atėjimas į darbą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="6fcd1-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="6fcd1-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="6fcd1-144">Peržiūrėkite patvirtinimo pranešimą ir patikrinkite, ar dabartinis veiklos laikas yra teisingas.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="6fcd1-145">Registracijos žurnalas</span><span class="sxs-lookup"><span data-stu-id="6fcd1-145">Logbook:</span></span>

    - <span data-ttu-id="6fcd1-146">Spustelėkite **Registracijos žurnalas** laikrodžio veiklai peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="6fcd1-147">Naudokite laiko filtrus, norėdami pasirinkti skirtingus laiko langus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="6fcd1-148">Jei dirbate keliose parduotuvių vietose, matysite savo laiko registravimus visose parduotuvėse, kuriose įrašėte laiką.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="6fcd1-149">Galite naudoti parduotuvių filtrą, norėdami peržiūrėti pasirinktos parduotuvės laiko registravimus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="6fcd1-150">Skirtingos laiko juostos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-150">Different time zones:</span></span>

    - <span data-ttu-id="6fcd1-151">Jei peržiūrite kitos vietos laiką (naudodami kasininko registracijos žurnalą arba vadovo vaidmens scenarijaus parinktį **Peržiūrėti laiko įrašus**) ir ta vieta yra kitoje laiko juostoje, rodomi laiko įrašai yra konvertuojami į jūsų vietos laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="6fcd1-152">Pvz., jūs esate dviejų parduotuvių (Arizonoje ir Nevadoje) vadovas.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="6fcd1-153">Kasininkas registruoja atėjimą į darbą 9:00</span><span class="sxs-lookup"><span data-stu-id="6fcd1-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="6fcd1-154">Arizonos laiku.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-154">in Arizona.</span></span> <span data-ttu-id="6fcd1-155">Tuo metu Nevadoje yra 8:00.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="6fcd1-156">Todėl, jei esate Nevados parduotuvėje ir pažiūrite laiko registravimo įrašus, laiko registravimas pažymėtas 8:00.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="6fcd1-157">Peržiūrėti darbuotojų laiko registravimą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="6fcd1-158">Darbuotojų laiko registravimų peržiūra ir filtravimas pagal parduotuvę arba veiklos tipą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="6fcd1-159">EKA</span><span class="sxs-lookup"><span data-stu-id="6fcd1-159">On POS:</span></span>

- <span data-ttu-id="6fcd1-160">Pasirinkite **Peržiūrėti laikrodžio įrašus**.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="6fcd1-161">Galite matyti visų darbuotojų, kurie priskirti toms pačioms parduotuvėms, kaip ir jūs, laikrodžio registravimus.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="6fcd1-162">Galite naudoti veiklos tipo ir parduotuvės filtrus laiko registravimams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="6fcd1-163">Apdoroti ir valdyti darbuotojų laiko registravimą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-163">Process and manage time registrations</span></span>

<span data-ttu-id="6fcd1-164">„Retail“ vartotojas turi laikytis darbo eigos, kai skaičiuoja, tvirtina ir perkelia laiko registravimus į algalapį.</span><span class="sxs-lookup"><span data-stu-id="6fcd1-164">A Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="6fcd1-165">Pirminės operacijos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-165">Primary operations</span></span>

- <span data-ttu-id="6fcd1-166">Skaičiuoti</span><span class="sxs-lookup"><span data-stu-id="6fcd1-166">Calculate</span></span>
- <span data-ttu-id="6fcd1-167">Patvirtinti</span><span class="sxs-lookup"><span data-stu-id="6fcd1-167">Approve</span></span>
- <span data-ttu-id="6fcd1-168">Pateikti į algalapį</span><span class="sxs-lookup"><span data-stu-id="6fcd1-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="6fcd1-169">Kitos įprastos operacijos</span><span class="sxs-lookup"><span data-stu-id="6fcd1-169">Other common operations</span></span>

- <span data-ttu-id="6fcd1-170">Masinis išėjimas iš darbo</span><span class="sxs-lookup"><span data-stu-id="6fcd1-170">Bulk Clock-out</span></span>
- <span data-ttu-id="6fcd1-171">Registruoti neatvykimą</span><span class="sxs-lookup"><span data-stu-id="6fcd1-171">Register Absence</span></span>

<span data-ttu-id="6fcd1-172">Daugiau informacijos apie tai, kaip apdoroti laiko ir buvimo darbe registravimus, žr. [Laiko ir buvimo darbe registravimų apdorojimas](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="6fcd1-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
