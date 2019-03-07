---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2019 m. sausio 11 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent Core HR“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305499"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="d9878-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2019 m. sausio 11 d.)</span><span class="sxs-lookup"><span data-stu-id="d9878-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9878-104">**8.1.2100 versija**</span><span class="sxs-lookup"><span data-stu-id="d9878-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="d9878-105">Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="d9878-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="d9878-106">Pakeitimai</span><span class="sxs-lookup"><span data-stu-id="d9878-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="d9878-107">Atostogų užklausų tikrinimas prognozuojant turimą balansą</span><span class="sxs-lookup"><span data-stu-id="d9878-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="d9878-108">Šiame leidime atlikti pakeitimai suteikia galimybę darbuotojams teikti ateities atostogų užklausas nesumažinus savo esamo balanso.</span><span class="sxs-lookup"><span data-stu-id="d9878-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="d9878-109">Ateityje pateikus užklausas bus naudojamos standartinės darbo eigos.</span><span class="sxs-lookup"><span data-stu-id="d9878-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="d9878-110">Daugiau informacijos žr. [Nedarbo laiko kaupimas pagal pradirbtas valandas](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="d9878-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="d9878-111">Prognozuojamo atostogų balanso peržiūra darbo srityse ESS ir Žmonės</span><span class="sxs-lookup"><span data-stu-id="d9878-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="d9878-112">Ši funkcija personalo skyriui, vadovams ir darbuotojams leidžia peržiūrėti būsimų atostogų laikotarpių balansus.</span><span class="sxs-lookup"><span data-stu-id="d9878-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="d9878-113">Darbuotojai ateities balansus gali peržiūrėti darbo srityje **Darbuotojų savitarna**, o personalo skyrius gali pasiekti tą pačią informaciją naudodamas darbo sritį **Žmonės**.</span><span class="sxs-lookup"><span data-stu-id="d9878-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="d9878-114">Atostogų balansų keitimo pranešimai</span><span class="sxs-lookup"><span data-stu-id="d9878-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="d9878-115">Atostogų balansai rodys esamą darbuotojų balansą.</span><span class="sxs-lookup"><span data-stu-id="d9878-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="d9878-116">Ateities balansai pateikiami darbo srityse **Darbuotojų savitarna** ir **Žmonės** įvedus datą, kad būtų apskaičiuotas prognozuojamas balansas.</span><span class="sxs-lookup"><span data-stu-id="d9878-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="d9878-117">Patobulintas naršymas – prognozuojamus balansus galima peržiūrėti toliau nurodytose srityse.</span><span class="sxs-lookup"><span data-stu-id="d9878-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="d9878-118">Kortelėje **Atostogos**, darbo srityje **Aarbuotojų savitarna**.</span><span class="sxs-lookup"><span data-stu-id="d9878-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="d9878-119">Kortelėje **Atostogos ir neatvykimas**, darbo srityje **Vadovų savitarna**.</span><span class="sxs-lookup"><span data-stu-id="d9878-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="d9878-120">Puslapyje **Atostogos ir neatvykimas**, darbo srityje **Žmonės**.</span><span class="sxs-lookup"><span data-stu-id="d9878-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="d9878-121">Leisti dešimtaines dalis kintamųjų atlyginimo dalių planuose (grynųjų pinigų planai)</span><span class="sxs-lookup"><span data-stu-id="d9878-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="d9878-122">Dabar kintamosios grynųjų pinigų premijoms ir planams priskirta papildoma sumų funkcija, kuri perrašo reikšmes naudodama dešimtainius skaitmenis.</span><span class="sxs-lookup"><span data-stu-id="d9878-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="d9878-123">Negalima pakeisti datų kintamosios atlyginimo dalies registracijose įrašius planą</span><span class="sxs-lookup"><span data-stu-id="d9878-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="d9878-124">Šis pakeitimas leidžia atnaujinti plano pabaigos datą (pratęstą arba praėjusią) įrašius planą.</span><span class="sxs-lookup"><span data-stu-id="d9878-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="d9878-125">Vis dar galite aktyvinti arba išjungti planus nepriklausomai nuo pradžios ir pabaigos datų.</span><span class="sxs-lookup"><span data-stu-id="d9878-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="d9878-126">Algalapio informacija pasiekiama priskyrus atlyginimų administratoriaus saugos vaidmenį</span><span class="sxs-lookup"><span data-stu-id="d9878-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="d9878-127">Algalapio administratoriaus vaidmuo atnaujintas ir dabar jam priskirta prieiga prie algalapio informacijos užklausos kūrimo metu.</span><span class="sxs-lookup"><span data-stu-id="d9878-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="d9878-128">Darbuotojų savitarnos, pareigų hierarchijos išklotinės detalizavimui nepavyksta gauti pirminio mazgo</span><span class="sxs-lookup"><span data-stu-id="d9878-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="d9878-129">Atlikti pakeitimai siekiant pašalinti klaidą, kuri kildavo įtraukiant pareigų hierarchiją į naujas darbo sritis ir naršant organizacijos struktūroje.</span><span class="sxs-lookup"><span data-stu-id="d9878-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="d9878-130">Naujas tikrinimo pranešimas, kai naudojama personalo numeracija</span><span class="sxs-lookup"><span data-stu-id="d9878-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="d9878-131">Atliktas pakeitimas siekiant paaiškinti, kokia problema kyla, kai jūs pasamdote darbuotoją ir naudojamas kitas personalo numeris.</span><span class="sxs-lookup"><span data-stu-id="d9878-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="d9878-132">Darbuotojų savitarnos darbo sritis pasirenkama kaip pradinis pradžios puslapis</span><span class="sxs-lookup"><span data-stu-id="d9878-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="d9878-133">Kai darbo sritis **Darbuotojų savitarna** pasirenkama kaip vartotojo pradinis pradžios puslapis ir tam vartotojui nėra priskirtas darbuotojo vaidmuo, sistema nukreips į numatytąją ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="d9878-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="d9878-134">Atleidimo priežasties kodas atnaujina pareigų priskyrimo įrašą</span><span class="sxs-lookup"><span data-stu-id="d9878-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="d9878-135">Atleidimo priežasties kodas dabar atnaujins pareigų priskyrimą, kaidarbuotojas atleidžiamas ir pareigos nutraukiamos.</span><span class="sxs-lookup"><span data-stu-id="d9878-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
