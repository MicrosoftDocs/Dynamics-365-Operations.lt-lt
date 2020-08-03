---
title: Nustatyti išmokų valdymo parametrus
description: Išmokų valdymo parametrų konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599361"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="f88e2-103">Išmokų valdymo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f88e2-103">Set Benefits management parameters</span></span>

<span data-ttu-id="f88e2-104">Jeigu norite nustatyti atostogų planus programoje „Microsoft Dynamics 365 Human Resources“, reikia sukonfigūruoti išmokų valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="f88e2-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="f88e2-105">Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="f88e2-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="f88e2-106">Bendrųjų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f88e2-106">Configure general parameters</span></span>

1. <span data-ttu-id="f88e2-107">**Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="f88e2-108">Skirtuke **Bendra** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f88e2-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="f88e2-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="f88e2-109">Field</span></span> | <span data-ttu-id="f88e2-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="f88e2-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f88e2-111">**Šalis/regionas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-111">**Country/region**</span></span> | <span data-ttu-id="f88e2-112">Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="f88e2-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="f88e2-113">Pasirinkta šalis rodoma pirma išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="f88e2-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="f88e2-114">**Registracijos priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-114">**Enrollment reason code**</span></span> | <span data-ttu-id="f88e2-115">Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją.</span><span class="sxs-lookup"><span data-stu-id="f88e2-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="f88e2-116">**Atšaukimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-116">**Cancellation reason code**</span></span> | <span data-ttu-id="f88e2-117">Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="f88e2-118">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="f88e2-119">Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="f88e2-120">**Pakartotinai atidaryti priežasties kodą**</span><span class="sxs-lookup"><span data-stu-id="f88e2-120">**Reopen reason code**</span></span> | <span data-ttu-id="f88e2-121">Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="f88e2-122">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="f88e2-123">Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="f88e2-124">**Gyvenimo įvykio priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-124">**Life event reason code**</span></span> | <span data-ttu-id="f88e2-125">Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="f88e2-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="f88e2-126">**Tarifo pakeitimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-126">**Rate change reason code**</span></span> | <span data-ttu-id="f88e2-127">Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="f88e2-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="f88e2-128">Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="f88e2-129">**Metinis išmokų atlyginimas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-129">**Benefits annual salary**</span></span> | <span data-ttu-id="f88e2-130">Leidžia jums nustatyti **Metinės išmokos naudos** sumą darbuotojui. </span><span class="sxs-lookup"><span data-stu-id="f88e2-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="f88e2-131">Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatant padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą.</span><span class="sxs-lookup"><span data-stu-id="f88e2-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="f88e2-132">**Nauja samda tinkama**</span><span class="sxs-lookup"><span data-stu-id="f88e2-132">**New hire eligible**</span></span> | <span data-ttu-id="f88e2-133">Nurodo, ar naujos samdos yra tinkamos.</span><span class="sxs-lookup"><span data-stu-id="f88e2-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="f88e2-134">**Naujos samdos registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="f88e2-134">**New hire enrollment period**</span></span> | <span data-ttu-id="f88e2-135">Laikotarpis, kuriuo leidžiama naujos samdos registracija.</span><span class="sxs-lookup"><span data-stu-id="f88e2-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="f88e2-136">**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje.</span><span class="sxs-lookup"><span data-stu-id="f88e2-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="f88e2-137">**Numatytasis mokėjimo dažnumas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-137">**Default pay frequency**</span></span> | <span data-ttu-id="f88e2-138">Nustatytasis mokėjimo dažnumas naudotinas, kai yra įtraukiami nauji darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="f88e2-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="f88e2-139">**Įgalinti gyvenimo įvykiai**</span><span class="sxs-lookup"><span data-stu-id="f88e2-139">**Life events enabled**</span></span> | <span data-ttu-id="f88e2-140">Įgalinami gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="f88e2-140">Enables life events.</span></span> |
   | <span data-ttu-id="f88e2-141">**Slėpti pasenusias išmokų formas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="f88e2-142">Leidžia slėpti pasenusias išmokų formas.</span><span class="sxs-lookup"><span data-stu-id="f88e2-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="f88e2-143">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="f88e2-144">Darbuotojų savitarnos dalies parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f88e2-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="f88e2-145">**Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="f88e2-146">Skirtuke **Darbuotojų savitarna** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f88e2-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="f88e2-147">Laukas</span><span class="sxs-lookup"><span data-stu-id="f88e2-147">Field</span></span> | <span data-ttu-id="f88e2-148">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="f88e2-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f88e2-149">**Išmokos patvirtinimas**</span><span class="sxs-lookup"><span data-stu-id="f88e2-149">**Benefit verification**</span></span> | <span data-ttu-id="f88e2-150">Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies.</span><span class="sxs-lookup"><span data-stu-id="f88e2-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="f88e2-151">**Automatiškai parinkti gavėjus**</span><span class="sxs-lookup"><span data-stu-id="f88e2-151">**Auto select designees**</span></span> | <span data-ttu-id="f88e2-152">Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims.</span><span class="sxs-lookup"><span data-stu-id="f88e2-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="f88e2-153">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f88e2-153">Select **Save**.</span></span>
