---
title: Nustatyti išmokų valdymo parametrus
description: Išmokų valdymo parametrų konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429993"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="60919-103">Išmokų valdymo parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="60919-103">Set Benefits management parameters</span></span>

<span data-ttu-id="60919-104">Jeigu norite nustatyti atostogų planus programoje „Microsoft Dynamics 365 Human Resources“, reikia sukonfigūruoti išmokų valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="60919-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="60919-105">Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="60919-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="60919-106">Bendrųjų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="60919-106">Configure general parameters</span></span>

1. <span data-ttu-id="60919-107">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="60919-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="60919-108">Skirtuke **Bendra** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="60919-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="60919-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="60919-109">Field</span></span> | <span data-ttu-id="60919-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="60919-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="60919-111">**Šalis/regionas**</span><span class="sxs-lookup"><span data-stu-id="60919-111">**Country/region**</span></span> | <span data-ttu-id="60919-112">Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="60919-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="60919-113">Pasirinkta šalis rodoma pirma išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="60919-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="60919-114">**Registracijos priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="60919-114">**Enrollment reason code**</span></span> | <span data-ttu-id="60919-115">Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją.</span><span class="sxs-lookup"><span data-stu-id="60919-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="60919-116">**Atšaukimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="60919-116">**Cancellation reason code**</span></span> | <span data-ttu-id="60919-117">Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="60919-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="60919-118">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="60919-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="60919-119">Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="60919-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="60919-120">**Pakartotinai atidaryti priežasties kodą**</span><span class="sxs-lookup"><span data-stu-id="60919-120">**Reopen reason code**</span></span> | <span data-ttu-id="60919-121">Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="60919-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="60919-122">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="60919-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="60919-123">Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="60919-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="60919-124">**Gyvenimo įvykio priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="60919-124">**Life event reason code**</span></span> | <span data-ttu-id="60919-125">Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="60919-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="60919-126">**Tarifo pakeitimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="60919-126">**Rate change reason code**</span></span> | <span data-ttu-id="60919-127">Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="60919-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="60919-128">Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="60919-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="60919-129">**Nauja samda tinkama**</span><span class="sxs-lookup"><span data-stu-id="60919-129">**New hire eligible**</span></span> | <span data-ttu-id="60919-130">Nurodo, ar naujos samdos yra tinkamos.</span><span class="sxs-lookup"><span data-stu-id="60919-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="60919-131">**Naujos samdos registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="60919-131">**New hire enrollment period**</span></span> | <span data-ttu-id="60919-132">Laikotarpis, kuriuo leidžiama naujos samdos registracija.</span><span class="sxs-lookup"><span data-stu-id="60919-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="60919-133">**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje.</span><span class="sxs-lookup"><span data-stu-id="60919-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="60919-134">**Įgalinti gyvenimo įvykiai**</span><span class="sxs-lookup"><span data-stu-id="60919-134">**Life events enabled**</span></span> | <span data-ttu-id="60919-135">Įgalinami gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="60919-135">Enables life events.</span></span> |
   | <span data-ttu-id="60919-136">**Slėpti pasenusias išmokų formas**</span><span class="sxs-lookup"><span data-stu-id="60919-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="60919-137">Leidžia slėpti pasenusias išmokų formas.</span><span class="sxs-lookup"><span data-stu-id="60919-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="60919-138">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="60919-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="60919-139">Darbuotojų savitarnos dalies parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="60919-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="60919-140">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="60919-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="60919-141">Skirtuke **Darbuotojų savitarna** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="60919-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="60919-142">Laukas</span><span class="sxs-lookup"><span data-stu-id="60919-142">Field</span></span> | <span data-ttu-id="60919-143">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="60919-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="60919-144">**Išmokos patvirtinimas**</span><span class="sxs-lookup"><span data-stu-id="60919-144">**Benefit verification**</span></span> | <span data-ttu-id="60919-145">Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies.</span><span class="sxs-lookup"><span data-stu-id="60919-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="60919-146">**Automatiškai parinkti gavėjus**</span><span class="sxs-lookup"><span data-stu-id="60919-146">**Auto select designees**</span></span> | <span data-ttu-id="60919-147">Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims.</span><span class="sxs-lookup"><span data-stu-id="60919-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="60919-148">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="60919-148">Select **Save**.</span></span>
