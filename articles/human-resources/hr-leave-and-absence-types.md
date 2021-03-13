---
title: Atostogų ir neatvykimų tipų konfigūravimas
description: Darbuotojams skiriamų atostogų tipų nustatymas „Dynamics 365 Human Resources“.
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115081"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="66491-103">Atostogų ir neatvykimų tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="66491-103">Configure leave and absence types</span></span>

<span data-ttu-id="66491-104">Atostogų tipai programoje „Dynamics 365 Human Resources“ apibrėžia neatvykimų, kuriuos gali nurodyti darbuotojai, tipus.</span><span class="sxs-lookup"><span data-stu-id="66491-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="66491-105">Galite pritaikyti atostogų tipus atsižvelgdami į savo organizacijos poreikius.</span><span class="sxs-lookup"><span data-stu-id="66491-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="66491-106">Atostogų tipų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="66491-106">Examples of leave types include:</span></span>

- <span data-ttu-id="66491-107">Apmokamos atostogos (PTO)</span><span class="sxs-lookup"><span data-stu-id="66491-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="66491-108">Neapmokamos atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-108">Unpaid leave</span></span>
- <span data-ttu-id="66491-109">Apmokėtos atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-109">Paid vacation</span></span>
- <span data-ttu-id="66491-110">Nedarbingumo atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-110">Sick leave</span></span>
- <span data-ttu-id="66491-111">Nedarbingumo atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-111">Medical leave</span></span>
- <span data-ttu-id="66491-112">Šeimos atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-112">Family leave</span></span>
- <span data-ttu-id="66491-113">Trumpalaikė negalia</span><span class="sxs-lookup"><span data-stu-id="66491-113">Short-term disability</span></span>
- <span data-ttu-id="66491-114">Netekties atostogos</span><span class="sxs-lookup"><span data-stu-id="66491-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="66491-115">Įtraukti atostogų tipą</span><span class="sxs-lookup"><span data-stu-id="66491-115">Add a leave type</span></span>

1. <span data-ttu-id="66491-116">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="66491-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="66491-117">Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų tipai**.</span><span class="sxs-lookup"><span data-stu-id="66491-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="66491-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="66491-118">Select **New**.</span></span>

4. <span data-ttu-id="66491-119">Įveskite atostogų tipo pavadinimą dalyje **Tipas**, pasirinkite darbo eigą dalyje **Darbo eigos ID** ir įveskite aprašą dalyje **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="66491-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="66491-120">Dalies **Bendra** išplečiamajame sąraše **Kategorija** pasirinkite **Nėra**, **Suplanuota** arba **Nesuplanuota**.</span><span class="sxs-lookup"><span data-stu-id="66491-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="66491-121">Išplečiamajame sąraše **Pajamų kodas** pasirinkite pajamų kodą.</span><span class="sxs-lookup"><span data-stu-id="66491-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="66491-122">Dalyje **Būtina nurodyti priežasties kodą** pasirinkite, ar norite, kad būtų būtina nurodyti priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="66491-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="66491-123">Jeigu norite, kad būtų būtina nurodyti priežasčių kodus, galbūt jums reikės juos pridėti.</span><span class="sxs-lookup"><span data-stu-id="66491-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="66491-124">Dalyje **Priežasčių kodai** pasirinkite **Pridėti**, pasirinkite priežasties kodą, tada pasirinkite prie jo esantį žymės langelį **Įgalinta**.</span><span class="sxs-lookup"><span data-stu-id="66491-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="66491-125">Dalyje **Riboti prieigą prie pasirinktų vaidmenų** pasirinkite, ar norite riboti prieigą.</span><span class="sxs-lookup"><span data-stu-id="66491-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="66491-126">Tada pasirinkite saugos vaidmenis dalyje **Šio atostogų tipo saugos vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="66491-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="66491-127">Saugos vaidmenys nustatyti darbo eigoje, kurią pasirinkote dalyje **Darbo eigos ID** anksčiau šios procedūros metu.</span><span class="sxs-lookup"><span data-stu-id="66491-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="66491-128">Srityje **Kalendoriaus spalva** pasirinkite, kokia spalva bus naudojama šiam atostogų tipui atostogų ir neatvykimų kalendoriuose.</span><span class="sxs-lookup"><span data-stu-id="66491-128">Under **Calendar color**, choose what color to display on leave and absence calendars for this leave type.</span></span> 

10. <span data-ttu-id="66491-129">Dalyje **Suspendavimo ryšiai** pasirinkite, ar norite, kad šis atostogų tipas suspenduotų kitą atostogų tipą, ar jį suspenduotų kitas atostogų tipas.</span><span class="sxs-lookup"><span data-stu-id="66491-129">Under **Suspension relations**, choose if you want to have this leave type either suspend another leave type or be suspended by another leave type.</span></span> <span data-ttu-id="66491-130">Kai atostogų prašymas bus pateiktas suspendavimo atostogų tipui, jam bus automatiškai sukurtos suspendavimo atostogos.</span><span class="sxs-lookup"><span data-stu-id="66491-130">When a leave of absence request is submitted for the suspending leave type, a leave suspension will automatically be created for the suspended leave type.</span></span> 

10. <span data-ttu-id="66491-131">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="66491-131">Select **Save**.</span></span>

## <a name="configure-leave-type-rules"></a><span data-ttu-id="66491-132">Atostogų tipo taisyklių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="66491-132">Configure leave type rules</span></span>

1. <span data-ttu-id="66491-133">Atostogų tipo apvalinimo parinkčių nustatymas.</span><span class="sxs-lookup"><span data-stu-id="66491-133">Set rounding options for the leave type.</span></span> <span data-ttu-id="66491-134">Parinktys yra tokios: **Nėra**, **Į didesnę reikšmę**, **Į mažesnę reikšmę** ir **Į artimiausią reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="66491-134">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="66491-135">Taip pat galite nustatyti atostogų tipo apvalinimo tikslumą.</span><span class="sxs-lookup"><span data-stu-id="66491-135">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="66491-136">Atostogų tipo lauko **Šventinių dienų koregavimas** nustatymas.</span><span class="sxs-lookup"><span data-stu-id="66491-136">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="66491-137">Pasirinkus šią parinktį, „Human Resources“ naudoja šventinių dienų, kurios būna darbo dienomis, skaičių, kad nustatytų, kaip kaupti atostogas šiam atostogų tipui.</span><span class="sxs-lookup"><span data-stu-id="66491-137">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="66491-138">Pavyzdžiui, jei Kalėdos yra pirmadienį, „Human Resources“ atims vieną dieną iš atostogų tipo, kai apdoros kaupimus.</span><span class="sxs-lookup"><span data-stu-id="66491-138">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="66491-139">Nustatote šventine dienas darbo laiko kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="66491-139">You set holidays in the working time calendar.</span></span> <span data-ttu-id="66491-140">Daugiau informacijos žr. skyriuje [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="66491-140">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>
   
 3. <span data-ttu-id="66491-141">Nustatykite **Perkeliamų atostogų tipą** atostogų tipui.</span><span class="sxs-lookup"><span data-stu-id="66491-141">Set **Carry-forward leave type** for the leave type.</span></span> <span data-ttu-id="66491-142">Pasirinkus šią parinktį, visi perkeliami likučiai bus perkelti į nurodytą atostogų tipą.</span><span class="sxs-lookup"><span data-stu-id="66491-142">When you select this option, any carry-forward balances will be transferred to the specified leave type.</span></span> <span data-ttu-id="66491-143">Perkeliamų atostogų tipas taip pat turi būti nurodytas atostogų plane.</span><span class="sxs-lookup"><span data-stu-id="66491-143">The carry-forward leave type also needs to be included in the leave and absence plan.</span></span> 
 
 4. <span data-ttu-id="66491-144">Apibrėžkite **Galiojimo taisykles** atostogų tipui.</span><span class="sxs-lookup"><span data-stu-id="66491-144">Define **Expiration rules** for the leave type.</span></span> <span data-ttu-id="66491-145">Konfigūruodami šią parinktį, galite pasirinkti dienų ar mėnesių vienetą ir nustatyti galiojimo pabaigos trukmę.</span><span class="sxs-lookup"><span data-stu-id="66491-145">When you configure this option, you can choose the unit of days or months and set the duration for the expiry.</span></span> <span data-ttu-id="66491-146">Taip pat galite nustatyti galiojimo taisyklės įsigaliojimo datą.</span><span class="sxs-lookup"><span data-stu-id="66491-146">You can also set the effective date of the expiration rule.</span></span> <span data-ttu-id="66491-147">Visi galiojimo pabaigos metu esantys atostogų likučiai bus atimami iš atostogų tipo ir bus įtraukti į atostogų likutį.</span><span class="sxs-lookup"><span data-stu-id="66491-147">Any leave balances that exist at the time of expiry will be subtracted from the leave type and will be reflected in the leave balance.</span></span> 
 
 
## <a name="see-also"></a><span data-ttu-id="66491-148">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="66491-148">See also</span></span>

- [<span data-ttu-id="66491-149">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="66491-149">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="66491-150">Atostogų ir neatvykimų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="66491-150">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="66491-151">Darbo laiko kalendoriaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="66491-151">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)
- [<span data-ttu-id="66491-152">Atostogų sustabdymas</span><span class="sxs-lookup"><span data-stu-id="66491-152">Suspend leave</span></span>](hr-leave-and-absence-suspend-leave.md)

