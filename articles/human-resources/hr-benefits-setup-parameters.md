---
title: Nustatykite Priedų valdymą ir Darbuotojo savitarnos parametrus visoms įmonėms
description: Konfigūruokite parametrus naudų valdymui ir darbuotojo savitarnai „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692702"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="cb102-103">Nustatykite Priedų valdymą ir Darbuotojo savitarnos parametrus visoms įmonėms</span><span class="sxs-lookup"><span data-stu-id="cb102-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="cb102-104">Prieš tai, kai nustatysite priedų planus „Microsoft Dynamics 365 Human Resources“, turite sukonfigūruoti Priedų valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="cb102-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="cb102-105">Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="cb102-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="cb102-106">Bendrųjų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cb102-106">Configure general parameters</span></span>

1. <span data-ttu-id="cb102-107">**Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cb102-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="cb102-108">Skirtuke **Išmokų valdymas** įveskite toliau pateiktų laukų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="cb102-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="cb102-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="cb102-109">Field</span></span> | <span data-ttu-id="cb102-110">aprašymas</span><span class="sxs-lookup"><span data-stu-id="cb102-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cb102-111">**Šalis/regionas**</span><span class="sxs-lookup"><span data-stu-id="cb102-111">**Country/region**</span></span> | <span data-ttu-id="cb102-112">Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="cb102-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="cb102-113">Pasirinkta šalis rodoma pirma išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="cb102-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="cb102-114">**Registracijos priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="cb102-114">**Enrollment reason code**</span></span> | <span data-ttu-id="cb102-115">Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją.</span><span class="sxs-lookup"><span data-stu-id="cb102-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="cb102-116">**Atšaukimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="cb102-116">**Cancellation reason code**</span></span> | <span data-ttu-id="cb102-117">Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="cb102-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="cb102-118">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="cb102-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="cb102-119">Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="cb102-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="cb102-120">**Pakartotinai atidaryti priežasties kodą**</span><span class="sxs-lookup"><span data-stu-id="cb102-120">**Reopen reason code**</span></span> | <span data-ttu-id="cb102-121">Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="cb102-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="cb102-122">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="cb102-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="cb102-123">Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="cb102-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="cb102-124">**Gyvenimo įvykio priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="cb102-124">**Life event reason code**</span></span> | <span data-ttu-id="cb102-125">Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="cb102-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="cb102-126">**Tarifo pakeitimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="cb102-126">**Rate change reason code**</span></span> | <span data-ttu-id="cb102-127">Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="cb102-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="cb102-128">Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="cb102-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="cb102-129">**Metinis išmokų atlyginimas**</span><span class="sxs-lookup"><span data-stu-id="cb102-129">**Benefits annual salary**</span></span> | <span data-ttu-id="cb102-130">Leidžia jums nustatyti **Metinės išmokos naudos** sumą darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="cb102-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="cb102-131">Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatydami padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą.</span><span class="sxs-lookup"><span data-stu-id="cb102-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="cb102-132">**Nauja samda tinkama**</span><span class="sxs-lookup"><span data-stu-id="cb102-132">**New hire eligible**</span></span> | <span data-ttu-id="cb102-133">Nurodo, ar naujos samdos yra tinkamos.</span><span class="sxs-lookup"><span data-stu-id="cb102-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="cb102-134">**Naujos samdos registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="cb102-134">**New hire enrollment period**</span></span> | <span data-ttu-id="cb102-135">Laikotarpis, kuriuo leidžiama naujos samdos registracija.</span><span class="sxs-lookup"><span data-stu-id="cb102-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="cb102-136">**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje.</span><span class="sxs-lookup"><span data-stu-id="cb102-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="cb102-137">**Numatytasis mokėjimo dažnumas**</span><span class="sxs-lookup"><span data-stu-id="cb102-137">**Default pay frequency**</span></span> | <span data-ttu-id="cb102-138">Nustatytasis mokėjimo dažnumas naudotinas, kai yra įtraukiami nauji darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="cb102-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="cb102-139">**Įgalinti gyvenimo įvykiai**</span><span class="sxs-lookup"><span data-stu-id="cb102-139">**Life events enabled**</span></span> | <span data-ttu-id="cb102-140">Įgalinami gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="cb102-140">Enables life events.</span></span> |
   | <span data-ttu-id="cb102-141">**Slėpti pasenusias išmokų formas**</span><span class="sxs-lookup"><span data-stu-id="cb102-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="cb102-142">Leidžia slėpti pasenusias išmokų formas.</span><span class="sxs-lookup"><span data-stu-id="cb102-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="cb102-143">**Išmokos patvirtinimas**</span><span class="sxs-lookup"><span data-stu-id="cb102-143">**Benefit verification**</span></span> | <span data-ttu-id="cb102-144">Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies.</span><span class="sxs-lookup"><span data-stu-id="cb102-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="cb102-145">**Automatiškai parinkti gavėjus**</span><span class="sxs-lookup"><span data-stu-id="cb102-145">**Auto select designees**</span></span> | <span data-ttu-id="cb102-146">Nurodo, ar automatiškai pasirinkti priklausinius ir naudos gavėjus pagal jų tinkamumą plano parinktims.</span><span class="sxs-lookup"><span data-stu-id="cb102-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="cb102-147">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cb102-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="cb102-148">Konfigūruoti darbuotojo savitarnos parametrus</span><span class="sxs-lookup"><span data-stu-id="cb102-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="cb102-149">**Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="cb102-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="cb102-150">Skirtuke **Išmokų valdymas** įveskite toliau pateiktų laukų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="cb102-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="cb102-151">Laukas</span><span class="sxs-lookup"><span data-stu-id="cb102-151">Field</span></span> | <span data-ttu-id="cb102-152">Aprašas</span><span class="sxs-lookup"><span data-stu-id="cb102-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cb102-153">**Išmokos patvirtinimas**</span><span class="sxs-lookup"><span data-stu-id="cb102-153">**Benefit verification**</span></span> | <span data-ttu-id="cb102-154">Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies.</span><span class="sxs-lookup"><span data-stu-id="cb102-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="cb102-155">**Automatiškai parinkti gavėjus**</span><span class="sxs-lookup"><span data-stu-id="cb102-155">**Auto select designees**</span></span> | <span data-ttu-id="cb102-156">Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims.</span><span class="sxs-lookup"><span data-stu-id="cb102-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="cb102-157">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cb102-157">Select **Save**.</span></span>


