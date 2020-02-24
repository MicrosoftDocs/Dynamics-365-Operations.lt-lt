---
title: Atostogų ir neatvykimų tipų konfigūravimas
description: Darbuotojams skiriamų atostogų tipų nustatymas „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1748ec2a888a50af9b9260720dfd439adc4686f9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009978"
---
# <a name="configure-leave-and-absence-types"></a><span data-ttu-id="fe806-103">Atostogų ir neatvykimų tipų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="fe806-103">Configure leave and absence types</span></span>

<span data-ttu-id="fe806-104">Atostogų tipai programoje „Dynamics 365 Human Resources“ apibrėžia neatvykimų, kuriuos gali nurodyti darbuotojai, tipus.</span><span class="sxs-lookup"><span data-stu-id="fe806-104">Leave types in Dynamics 365 Human Resources define the types of absences that employees can report.</span></span> <span data-ttu-id="fe806-105">Galite pritaikyti atostogų tipus atsižvelgdami į savo organizacijos poreikius.</span><span class="sxs-lookup"><span data-stu-id="fe806-105">You can tailor leave types according to the needs of your organization.</span></span> <span data-ttu-id="fe806-106">Atostogų tipų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="fe806-106">Examples of leave types include:</span></span>

- <span data-ttu-id="fe806-107">Apmokamos atostogos (PTO)</span><span class="sxs-lookup"><span data-stu-id="fe806-107">Paid time off (PTO)</span></span>
- <span data-ttu-id="fe806-108">Neapmokamos atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-108">Unpaid leave</span></span>
- <span data-ttu-id="fe806-109">Apmokėtos atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-109">Paid vacation</span></span>
- <span data-ttu-id="fe806-110">Nedarbingumo atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-110">Sick leave</span></span>
- <span data-ttu-id="fe806-111">Nedarbingumo atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-111">Medical leave</span></span>
- <span data-ttu-id="fe806-112">Šeimos atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-112">Family leave</span></span>
- <span data-ttu-id="fe806-113">Trumpalaikė negalia</span><span class="sxs-lookup"><span data-stu-id="fe806-113">Short-term disability</span></span>
- <span data-ttu-id="fe806-114">Netekties atostogos</span><span class="sxs-lookup"><span data-stu-id="fe806-114">Bereavement leave</span></span>

## <a name="add-a-leave-type"></a><span data-ttu-id="fe806-115">Įtraukti atostogų tipą</span><span class="sxs-lookup"><span data-stu-id="fe806-115">Add a leave type</span></span>

1. <span data-ttu-id="fe806-116">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="fe806-116">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="fe806-117">Dalyje **Sąranka**pasirinkite **Atostogų ir neatvykimų tipai**.</span><span class="sxs-lookup"><span data-stu-id="fe806-117">Under **Setup**, select **Leave and absence types**.</span></span>

3. <span data-ttu-id="fe806-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fe806-118">Select **New**.</span></span>

4. <span data-ttu-id="fe806-119">Įveskite atostogų tipo pavadinimą dalyje **Tipas**, pasirinkite darbo eigą dalyje **Darbo eigos ID** ir įveskite aprašą dalyje **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="fe806-119">Enter a name for the leave type under **Type**, select a workflow from **Workflow ID**, and enter a description under **Description**.</span></span>

5. <span data-ttu-id="fe806-120">Dalies **Bendra** išplečiamajame sąraše **Kategorija** pasirinkite **Nėra**, **Suplanuota** arba **Nesuplanuota**.</span><span class="sxs-lookup"><span data-stu-id="fe806-120">In **General**, select **None**, **Scheduled**, or **Unscheduled** from the **Category** dropdown.</span></span>

6. <span data-ttu-id="fe806-121">Išplečiamajame sąraše **Pajamų kodas** pasirinkite pajamų kodą.</span><span class="sxs-lookup"><span data-stu-id="fe806-121">Select an earning code from the **Earning code** dropdown.</span></span>

7. <span data-ttu-id="fe806-122">Dalyje **Būtina nurodyti priežasties kodą** pasirinkite, ar norite, kad būtų būtina nurodyti priežasties kodą.</span><span class="sxs-lookup"><span data-stu-id="fe806-122">Under **Reason code required**, choose whether you want to require a reason code.</span></span> <span data-ttu-id="fe806-123">Jeigu norite, kad būtų būtina nurodyti priežasčių kodus, galbūt jums reikės juos pridėti.</span><span class="sxs-lookup"><span data-stu-id="fe806-123">If you want to require reason codes, you might need to add them.</span></span> <span data-ttu-id="fe806-124">Dalyje **Priežasčių kodai** pasirinkite **Pridėti**, pasirinkite priežasties kodą, tada pasirinkite prie jo esantį žymės langelį **Įgalinta**.</span><span class="sxs-lookup"><span data-stu-id="fe806-124">Under **Reason codes**, select **Add**, select a reason code, and then select the **Enabled** checkbox next to it.</span></span>

8. <span data-ttu-id="fe806-125">Dalyje **Riboti prieigą prie pasirinktų vaidmenų** pasirinkite, ar norite riboti prieigą.</span><span class="sxs-lookup"><span data-stu-id="fe806-125">Under **Restrict access to selected roles**, choose whether you want to restrict access.</span></span> <span data-ttu-id="fe806-126">Tada pasirinkite saugos vaidmenis dalyje **Šio atostogų tipo saugos vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="fe806-126">Then select the security roles under **Security roles for this leave type**.</span></span> <span data-ttu-id="fe806-127">Saugos vaidmenys nustatyti darbo eigoje, kurią pasirinkote dalyje **Darbo eigos ID** anksčiau šios procedūros metu.</span><span class="sxs-lookup"><span data-stu-id="fe806-127">The security roles are defined in the workflow you selected under **Workflow ID** earlier in this procedure.</span></span>

9. <span data-ttu-id="fe806-128">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fe806-128">Select **Save**.</span></span>

## <a name="configure-preview-features"></a><span data-ttu-id="fe806-129">Peržiūros funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="fe806-129">Configure preview features</span></span>

<span data-ttu-id="fe806-130">Jeigu įgalinote atostogų ir neatvykimų peržiūros funkcijas, jums reikės konfigūruoti ir jų parametrus.</span><span class="sxs-lookup"><span data-stu-id="fe806-130">If you've enabled preview features for Leave and absence, you need to configure settings for them, too.</span></span>

[!include [banner](includes/preview-feature-leave-absence.md)]

1. <span data-ttu-id="fe806-131">Atostogų tipo apvalinimo parinkčių nustatymas.</span><span class="sxs-lookup"><span data-stu-id="fe806-131">Set rounding options for the leave type.</span></span> <span data-ttu-id="fe806-132">Parinktys yra tokios: **Nėra**, **Į didesnę reikšmę**, **Į mažesnę reikšmę** ir **Į artimiausią reikšmę**.</span><span class="sxs-lookup"><span data-stu-id="fe806-132">Options include **None**, **Up**, **Down**, and **Nearest**.</span></span> <span data-ttu-id="fe806-133">Taip pat galite nustatyti atostogų tipo apvalinimo tikslumą.</span><span class="sxs-lookup"><span data-stu-id="fe806-133">You can also set rounding precision for the leave type.</span></span>

2. <span data-ttu-id="fe806-134">Atostogų tipo lauko **Šventinių dienų koregavimas** nustatymas.</span><span class="sxs-lookup"><span data-stu-id="fe806-134">Set **Holiday correction** for the leave type.</span></span> <span data-ttu-id="fe806-135">Pasirinkus šią parinktį, „Human Resources“ naudoja šventinių dienų, kurios būna darbo dienomis, skaičių, kad nustatytų, kaip kaupti atostogas šiam atostogų tipui.</span><span class="sxs-lookup"><span data-stu-id="fe806-135">When you select this option, Human Resources uses the number of holidays that fall on a work day to determine how to accrue time off for the leave type.</span></span> <span data-ttu-id="fe806-136">Pavyzdžiui, jei Kalėdos yra pirmadienį, „Human Resources“ atims vieną dieną iš atostogų tipo, kai apdoros kaupimus.</span><span class="sxs-lookup"><span data-stu-id="fe806-136">For example, if Christmas Day falls on a Monday, Human Resources will subtract one day from the leave type when processing accruals.</span></span>

   <span data-ttu-id="fe806-137">Nustatote šventine dienas darbo laiko kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="fe806-137">You set holidays in the working time calendar.</span></span> <span data-ttu-id="fe806-138">Daugiau informacijos žr. skyriuje [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)</span><span class="sxs-lookup"><span data-stu-id="fe806-138">For more information, see [Create a working time calendar](hr-leave-and-absence-working-time-calendar.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="fe806-139">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="fe806-139">See also</span></span>

- [<span data-ttu-id="fe806-140">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="fe806-140">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="fe806-141">Atostogų ir neatvykimų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe806-141">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)
- [<span data-ttu-id="fe806-142">Darbo laiko kalendoriaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe806-142">Create a working time calendar</span></span>](hr-leave-and-absence-working-time-calendar.md)