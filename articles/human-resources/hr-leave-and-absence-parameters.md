---
title: Atostogų ir neatvykimų parametrų konfigūravimas
description: Žmogiškųjų išteklių parametrų, skirtų atostogoms ir neatvykimams, nustatymas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056857"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="dcb57-103">Atostogų ir neatvykimų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dcb57-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dcb57-104">Prieš nustatant atostogų ir neatvykimų planus „Dynamics 365 Human Resources“, naudinga patikrinti visus susijusius žmogiškųjų išteklių parametrų nustatymus, įskaitant:</span><span class="sxs-lookup"><span data-stu-id="dcb57-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="dcb57-105">Atostogų užklausų numeraciją</span><span class="sxs-lookup"><span data-stu-id="dcb57-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="dcb57-106">Nedarbingumo dėl ligos ar slaugymo akto (FMLA) parametrus</span><span class="sxs-lookup"><span data-stu-id="dcb57-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="dcb57-107">Darbuotojo atostogų ir neatvykimų užklausų savitarnos parametrus</span><span class="sxs-lookup"><span data-stu-id="dcb57-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="dcb57-108">Atostogų ir neatvykimų parametrai</span><span class="sxs-lookup"><span data-stu-id="dcb57-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="dcb57-109">Peržiūrėti ir keisti žmogiškųjų išteklių parametrus</span><span class="sxs-lookup"><span data-stu-id="dcb57-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="dcb57-110">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dcb57-111">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="dcb57-112">Skirtuke **Numeracija** patikrinkite **numeracijos kodą**, skirtą **atostogų užklausos ID**, ir pakeiskite, jeigu reikia.</span><span class="sxs-lookup"><span data-stu-id="dcb57-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="dcb57-113">Šiuo parametru nustatoma seka, naudojama automatiškai priskirti ID atostogų užklausoms.</span><span class="sxs-lookup"><span data-stu-id="dcb57-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="dcb57-114">Skirtuke **FMLA** patikrinkite FMLA parametrus ir pakeiskite, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="dcb57-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="dcb57-115">Skirtuke **Darbuotojo savitarna** nurodykite, ar vadybininkai savo darbuotojų vardu gali įvesti atostogų ir neatvykimų užklausas.</span><span class="sxs-lookup"><span data-stu-id="dcb57-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="dcb57-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="dcb57-117">Atostogų ir nebuvo darbe peržiūra visose įmonėse šiuo metu yra išankstinėje peržiūroje.</span><span class="sxs-lookup"><span data-stu-id="dcb57-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="dcb57-118">Jums reikės įjungti jį savo **Smėlio dėžės** aplinkoje, kad matytumėte parinktį atostogoms ir nebuvimui darbe.</span><span class="sxs-lookup"><span data-stu-id="dcb57-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="dcb57-119">Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="dcb57-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="dcb57-120">Peržiūrėti ir keisti žmogiškųjų išteklių bendrintus parametrus</span><span class="sxs-lookup"><span data-stu-id="dcb57-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="dcb57-121">Puslapyje **Personalo valdymas** rinkitės **Nuorodų** skirtuką.</span><span class="sxs-lookup"><span data-stu-id="dcb57-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dcb57-122">Skyriuje **Nustatymai**, Rinkitės **žmogiškųjų išteklių bendrinti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="dcb57-123">Skirtuke **Papildoma prieiga** rinkitės **Taip** norėdami **Įjungti kryžminę įmonės atostogų peržiūrą** tam, kad atostogos būtų matomos visose įmonėse.</span><span class="sxs-lookup"><span data-stu-id="dcb57-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="dcb57-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="dcb57-125">Peržiūrėti ir keisti atostogų ir neatvykimų parametrus</span><span class="sxs-lookup"><span data-stu-id="dcb57-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="dcb57-126">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dcb57-127">Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="dcb57-128">Skirtuke **Bendra** nustatykite tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="dcb57-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="dcb57-129">Nustatykite **Atostogų ir neatvykimų vienetas** į valandas arba dienas.</span><span class="sxs-lookup"><span data-stu-id="dcb57-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="dcb57-130">Jei nustatėte dienas, galite pasirinkti **Įjungti pusės dienos apibrėžtį**, kad darbuotojai galėtų pasirinkti pirmąją ar antrą dienos pusę prašymuose išleisti iš darbo.</span><span class="sxs-lookup"><span data-stu-id="dcb57-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="dcb57-131">Pasirinkite **Paslaugos įsigaliojimo datos mėnesiai**, kad nustatytumėte, kada atostogų planų, naudojančių darbo mėnesius, kaupimo tarifai įsigalios.</span><span class="sxs-lookup"><span data-stu-id="dcb57-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="dcb57-132">Pasirinkite **Balanso skaičiavimas** rodyti balansams nuo šiandien arba nuo kaupimo laikotarpio.</span><span class="sxs-lookup"><span data-stu-id="dcb57-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="dcb57-133">Jei pasirinksite **Šiandienos balansas**, balansas rodys visus šiandienos kaupimus, koregavimus ir užklausas.</span><span class="sxs-lookup"><span data-stu-id="dcb57-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="dcb57-134">Jei pasirinksite **Kaupimo laikotarpio balansas**, balansas rodys visus kaupimo laikotarpio, nustatyto pagal atostogų plano dažnumą, kaupimus, koregavimus ir užklausas.</span><span class="sxs-lookup"><span data-stu-id="dcb57-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="dcb57-135">Nustatykite pradžios laiką paketinės užduoties galiojimo pabaigai perkelti.</span><span class="sxs-lookup"><span data-stu-id="dcb57-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="dcb57-136">Pasirinkite **Taip** dalyse **Leisti darbuotojams pirkti atostogas** ir **Leisti darbuotojams parduoti atostogas**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="dcb57-137">Jei pasirinksite **Taip** šioms parinktims, galite kurti atostogų pirkimo ir pardavimo strategijas ir įgalinti darbuotojus pateikti atostogų pirkimo ir pardavimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="dcb57-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="dcb57-138">Kalendoriaus parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dcb57-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="dcb57-139">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dcb57-140">Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="dcb57-141">Skirtuke **Kalendorius** keiskite kalendoriaus parametrus, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="dcb57-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="dcb57-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dcb57-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcb57-143">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="dcb57-143">See also</span></span>

- [<span data-ttu-id="dcb57-144">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="dcb57-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]