---
title: Nustatyti išmokų valdymo parametrus
description: Išmokų valdymo parametrų konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009947"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="00434-103">Nustatyti išmokų valdymo parametrus</span><span class="sxs-lookup"><span data-stu-id="00434-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="00434-104">Jeigu norite nustatyti atostogų planus programoje „Microsoft Dynamics 365 Human Resources“, reikia sukonfigūruoti išmokų valdymo parametrus.</span><span class="sxs-lookup"><span data-stu-id="00434-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="00434-105">Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="00434-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="00434-106">Bendrųjų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="00434-106">Configure general parameters</span></span>

1. <span data-ttu-id="00434-107">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="00434-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="00434-108">Skirtuke **Bendra** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="00434-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="00434-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="00434-109">Field</span></span> | <span data-ttu-id="00434-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="00434-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="00434-111">**Šalis/regionas**</span><span class="sxs-lookup"><span data-stu-id="00434-111">**Country/region**</span></span> | <span data-ttu-id="00434-112">Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="00434-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="00434-113">Pasirinkta šalis rodoma pirma išplečiamajame sąraše.</span><span class="sxs-lookup"><span data-stu-id="00434-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="00434-114">**Registracijos priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="00434-114">**Enrollment reason code**</span></span> | <span data-ttu-id="00434-115">Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją.</span><span class="sxs-lookup"><span data-stu-id="00434-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="00434-116">**Atšaukimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="00434-116">**Cancellation reason code**</span></span> | <span data-ttu-id="00434-117">Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="00434-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="00434-118">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="00434-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="00434-119">Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="00434-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="00434-120">**Pakartotinai atidaryti priežasties kodą**</span><span class="sxs-lookup"><span data-stu-id="00434-120">**Reopen reason code**</span></span> | <span data-ttu-id="00434-121">Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą.</span><span class="sxs-lookup"><span data-stu-id="00434-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="00434-122">Jis rodomas dialogo lange vykdant atšaukimo procesą.</span><span class="sxs-lookup"><span data-stu-id="00434-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="00434-123">Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**.</span><span class="sxs-lookup"><span data-stu-id="00434-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="00434-124">**Gyvenimo įvykio priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="00434-124">**Life event reason code**</span></span> | <span data-ttu-id="00434-125">Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui.</span><span class="sxs-lookup"><span data-stu-id="00434-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="00434-126">**Tarifo pakeitimo priežasties kodas**</span><span class="sxs-lookup"><span data-stu-id="00434-126">**Rate change reason code**</span></span> | <span data-ttu-id="00434-127">Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="00434-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="00434-128">Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="00434-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="00434-129">**Nauja samda tinkama**</span><span class="sxs-lookup"><span data-stu-id="00434-129">**New hire eligible**</span></span> | <span data-ttu-id="00434-130">Nurodo, ar naujos samdos yra tinkamos.</span><span class="sxs-lookup"><span data-stu-id="00434-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="00434-131">**Naujos samdos registracijos laikotarpis**</span><span class="sxs-lookup"><span data-stu-id="00434-131">**New hire enrollment period**</span></span> | <span data-ttu-id="00434-132">Laikotarpis, kuriuo leidžiama naujos samdos registracija.</span><span class="sxs-lookup"><span data-stu-id="00434-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="00434-133">**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje.</span><span class="sxs-lookup"><span data-stu-id="00434-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="00434-134">**Metinis atlyginimo didinimas**</span><span class="sxs-lookup"><span data-stu-id="00434-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="00434-135">Nurodoma, ar automatiškai apskaičiuoti sumą **Metinis išmokų atlyginimas** dalyje **Įdarbinimo išmokų informacija**.</span><span class="sxs-lookup"><span data-stu-id="00434-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="00434-136">Ji grindžiama darbuotojo **pastoviosios atlyginimo dalies mokesčio tarifu**, **valandų vidurkiu** ir **mokėjimo dažnumu**.</span><span class="sxs-lookup"><span data-stu-id="00434-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="00434-137">**Valandų vidurkis** x **Fiksuotas mokėjimo tarifas** x **Mokėjimo dažnumas** (mokėjimo laikotarpių skaičius) = **Metinis išmokų atlyginimas**</span><span class="sxs-lookup"><span data-stu-id="00434-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="00434-138">Jei bet kurios reikšmės laukuose **Valandų vidurkis**, **Pastoviosios atlyginimo dalies mokesčio tarifas** arba **Mokėjimo dažnumas** pasikeičia, sistema automatiškai perskaičiuoja darbuotojo **metinio išmokų atlyginimo** sumą pagal pasikeitusias vertes.</span><span class="sxs-lookup"><span data-stu-id="00434-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="00434-139">Sistema sukuria įrašą **Įsigaliojimo data**, kad būtų galima nustatyti tikslią pasikeitimo datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="00434-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="00434-140">Jei reikia, galite neautomatiškai redaguoti **metinio išmokų atlyginimo** sumą.</span><span class="sxs-lookup"><span data-stu-id="00434-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="00434-141">**Įgalinti gyvenimo įvykiai**</span><span class="sxs-lookup"><span data-stu-id="00434-141">**Life events enabled**</span></span> | <span data-ttu-id="00434-142">Įgalinami gyvenimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="00434-142">Enables life events.</span></span> |
   | <span data-ttu-id="00434-143">**Slėpti pasenusias išmokų formas**</span><span class="sxs-lookup"><span data-stu-id="00434-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="00434-144">Leidžia slėpti pasenusias išmokų formas.</span><span class="sxs-lookup"><span data-stu-id="00434-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="00434-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="00434-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="00434-146">Darbuotojų savitarnos dalies parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="00434-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="00434-147">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="00434-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="00434-148">Skirtuke **Darbuotojų savitarna** įveskite šių laukų reikšmes:</span><span class="sxs-lookup"><span data-stu-id="00434-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="00434-149">Laukas</span><span class="sxs-lookup"><span data-stu-id="00434-149">Field</span></span> | <span data-ttu-id="00434-150">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="00434-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="00434-151">**Išmokos patvirtinimas**</span><span class="sxs-lookup"><span data-stu-id="00434-151">**Benefit verification**</span></span> | <span data-ttu-id="00434-152">Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies.</span><span class="sxs-lookup"><span data-stu-id="00434-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="00434-153">**Automatiškai parinkti gavėjus**</span><span class="sxs-lookup"><span data-stu-id="00434-153">**Auto select designees**</span></span> | <span data-ttu-id="00434-154">Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims.</span><span class="sxs-lookup"><span data-stu-id="00434-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="00434-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="00434-155">Select **Save**.</span></span>
