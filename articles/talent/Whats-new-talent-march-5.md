---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 5 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2019
ms.locfileid: "782953"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="45586-103">Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. kovo 5 d.)</span><span class="sxs-lookup"><span data-stu-id="45586-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="45586-104">Šioje temoje aprašomos naujos ir pakeistos „Talent“ funkcijos</span><span class="sxs-lookup"><span data-stu-id="45586-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="45586-105">„Attract“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="45586-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="45586-106">„Attract“ parinkčių rinkinių išplėtimas</span><span class="sxs-lookup"><span data-stu-id="45586-106">Extending option sets in Attract</span></span>

<span data-ttu-id="45586-107">„Attract“ yra daug laukų, kurie yra „Common Data Service“ (CDS) parinkčių rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="45586-107">In Attract, there are multiple fields that are option sets within the Common Data Service (CDS).</span></span> <span data-ttu-id="45586-108">Pristatytos naujos galimybės išplėsti parinkčių rinkinius, pradedant nuo laukų **Atmetimo priežastis**, **Įdarbinimo tipas** ir **Stažo tipas**.</span><span class="sxs-lookup"><span data-stu-id="45586-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="45586-109">Norint naudoti darbo registravimo „LinkedIn“ funkciją, reikalingi puslapio **Darbo informacija** laukai **Įdarbinimo tipas** ir **Stažo tipas**.</span><span class="sxs-lookup"><span data-stu-id="45586-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="45586-110">Numatytąsias šių laukų reikšmes palaiko „LinkedIn“ ir jos rodomos, kai darbas registruojamas.</span><span class="sxs-lookup"><span data-stu-id="45586-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="45586-111">Jei registruojate darbus „LinkedIn“ ir modifikuojate esamas tų laukų parinkčių rinkinių reikšmes, darbas bus užregistruotas, bet „LinkedIn“ nerodys pasirinktinių laukų **Įdarbinimo tipas** ir **Stažo tipas** reikšmių.</span><span class="sxs-lookup"><span data-stu-id="45586-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="45586-112">Supažindinimo pakeitimai</span><span class="sxs-lookup"><span data-stu-id="45586-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="45586-113">Supažindinimo komandų privati peržiūra</span><span class="sxs-lookup"><span data-stu-id="45586-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="45586-114">Dabar galite lengvai bendrinti ir bendrai tvarkyti šablonus visoje savo organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="45586-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="45586-115">Daugiau informacijos žr. [Geriausios praktikos bendrinimas savo organizacijoje naudojant supažindinimo komandas](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="45586-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="45586-116">Priėmėjų rezervavimo ženklų privati peržiūra</span><span class="sxs-lookup"><span data-stu-id="45586-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="45586-117">Savo šablonus galite išplėsti priskirdami veiklas vaidmenims, o ne asmenims.</span><span class="sxs-lookup"><span data-stu-id="45586-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="45586-118">Tada vaidmenys priskiriami asmenims vadovo kūrimo metu.</span><span class="sxs-lookup"><span data-stu-id="45586-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="45586-119">Daugiau informacijos žr. [Vadovo administravimo supaprastinimas priskiriant veiklas vaidmenims](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="45586-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="45586-120">„Core HR“ pakeitimai</span><span class="sxs-lookup"><span data-stu-id="45586-120">Changes in Core HR</span></span>
<span data-ttu-id="45586-121">**8.1.2178 versija**</span><span class="sxs-lookup"><span data-stu-id="45586-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="45586-122">Sukonfigūruokite darbo eigą, kad automatiškai patvirtintumėte, arba atlikite darbo eigą, kai yra personalo arba eilutės vadovas pateikia ar atnaujina nedarbo laiko užklausas</span><span class="sxs-lookup"><span data-stu-id="45586-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="45586-123">Įtrauktos naujos darbo eigų sąlygos, kad nedarbo laiko užklausos būtų automatiškai patvirtinamos, jei jas pateikė darbuotojo vadovas arba personalo darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="45586-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="45586-124">Vienas būdas, kaip naudoti šią automatinio patvirtinimo darbo eigoje funkciją, yra įjungti automatinį veiksmą darbo eigos patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="45586-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="45586-125">Toliau pateiktos įtrauktos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="45586-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="45586-126">Pateikė – naudojama siekiant patikrinti vartotojo, kuris pateikė užklausą į darbo eigą, sistemos vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="45586-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="45586-127">Kieno vardu pateikta – naudojama siekiant patikrinti, ar nedarbo laiko užklausa buvo pateikta darbininko, susieto su užklausa, vardu.</span><span class="sxs-lookup"><span data-stu-id="45586-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="45586-128">Pateikė personalas – naudojama siekiant patikrinti, ar sistemos vartotojo, kuris pateikė užklausą į darbo eigą, vaidmuo yra Personalo darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="45586-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="45586-129">Pateikė vadovas – naudojama siekiant patikrinti, ar vartotojas, kuris pateikė nedarbo laiko užklausą į darbo eigą, yra su užklausa susieto darbininko eilutės hierarchijos vadovas.</span><span class="sxs-lookup"><span data-stu-id="45586-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="45586-130">Būsimų pareigų priskyrimų darbuotojų pastoviosios atlyginimo dalies įjungimas</span><span class="sxs-lookup"><span data-stu-id="45586-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="45586-131">Darbuotojai įprastai prisijungia prie organizacijos nustatant pradžios datą ateityje.</span><span class="sxs-lookup"><span data-stu-id="45586-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="45586-132">Šis pakeitimas suteikia galimybę nustatyti darbuotojų, kuriems priskirtos pareigos ateityje, pastoviąją atlyginimo dalį.</span><span class="sxs-lookup"><span data-stu-id="45586-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="45586-133">Redaguojant pareigas pareigų algalapio laukai yra nenurodyti</span><span class="sxs-lookup"><span data-stu-id="45586-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="45586-134">Atlikus šį pakeitimą, kai teikiama esamų pareigų pakeitimų užklausa, algalapio laukuose bus nustatomos esamos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="45586-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="45586-135">Kiti įvairūs klaidų ištaisymai</span><span class="sxs-lookup"><span data-stu-id="45586-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="45586-136">Kiti smulkūs klaidų ištaisymai yra įtraukti į šį leidimą.</span><span class="sxs-lookup"><span data-stu-id="45586-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-cds-for-apps"></a><span data-ttu-id="45586-137">Naujovinimas į „CDS for Apps“</span><span class="sxs-lookup"><span data-stu-id="45586-137">Upgrade to CDS for Apps</span></span>
<span data-ttu-id="45586-138">Terminas, iki kurio galima naujovinti į „CDS for Apps“, sparčiai artėja.</span><span class="sxs-lookup"><span data-stu-id="45586-138">Deadlines to upgrade to CDS for Apps are quickly approaching.</span></span> <span data-ttu-id="45586-139">Prisijunkite prie „PowerApps“ administravimo centro ir sužinokite, ar jūsų duomenų bazę reikia naujovint.</span><span class="sxs-lookup"><span data-stu-id="45586-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="45586-140">Daugiau informacijos apie galutinius terminus ir reikiamus naujovinimo veiksmus žr. [Naujovinimas į „Common Data Service for Apps“](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="45586-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="45586-141">Jau greitai</span><span class="sxs-lookup"><span data-stu-id="45586-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="45586-142">Išplėstinės kompensacijos sauga (fiksuota ir kintama)</span><span class="sxs-lookup"><span data-stu-id="45586-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="45586-143">Daugelyje organizacijų kompensacijų ir išmokų vadovai gali pasiekti tik tam tikrus kompensacijų įrašus, pvz., vadovams arba tam tikrų regionų darbuotojams skirtus įrašus.</span><span class="sxs-lookup"><span data-stu-id="45586-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="45586-144">Atlikus šį pakeitimą, galite valdyti ir tvarkyti kompensacijų planus, skirtus skirtingoms darbuotojų grupėms jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="45586-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="45586-145">Fiksuotam ir kintamam planams galima priskirti saugos vaidmenis – tokiu būdu nustatysite prieigą prie planų ir darbuotojų duomenų, susijusių su planais, pvz., pajamų arba premijų įrašai.</span><span class="sxs-lookup"><span data-stu-id="45586-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="45586-146">Tik asmenys, kuriems priskirti reikiami vaidmenys, galės apdoroti tų darbuotojų kompensaciją.</span><span class="sxs-lookup"><span data-stu-id="45586-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="45586-147">Platformos „update 24“</span><span class="sxs-lookup"><span data-stu-id="45586-147">Platform update 24</span></span>
<span data-ttu-id="45586-148">Papildomos informacijos apie 24 platformos naujinimą žr. [Kas nauja arba pakeista „Finance and Operations“ 24 platformos naujinime (2019 m. kovo mėn.)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="45586-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
