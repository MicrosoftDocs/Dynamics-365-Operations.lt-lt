---
title: Algalapio pastoviosios atlyginimo dalies planas
description: Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021301"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="46ae3-103">Algalapio pastoviosios atlyginimo dalies planas</span><span class="sxs-lookup"><span data-stu-id="46ae3-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="46ae3-104">Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="46ae3-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="46ae3-105">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="46ae3-105">Properties</span></span>

| <span data-ttu-id="46ae3-106">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="46ae3-106">Property</span></span><br><span data-ttu-id="46ae3-107">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-107">**Physical name**</span></span><br><span data-ttu-id="46ae3-108">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="46ae3-108">**_Type_**</span></span> | <span data-ttu-id="46ae3-109">Naudoti</span><span class="sxs-lookup"><span data-stu-id="46ae3-109">Use</span></span> | <span data-ttu-id="46ae3-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="46ae3-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="46ae3-111">**Darbuotojo ID**</span><span class="sxs-lookup"><span data-stu-id="46ae3-111">**Employee ID**</span></span><br><span data-ttu-id="46ae3-112">„mshr_fk_employee_id_value”</span><span class="sxs-lookup"><span data-stu-id="46ae3-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="46ae3-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="46ae3-113">*GUID*</span></span> | <span data-ttu-id="46ae3-114">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-114">Read-only</span></span><br><span data-ttu-id="46ae3-115">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-115">Required</span></span><br><span data-ttu-id="46ae3-116">Išorinis raktas: „mshr_Employee_id of mshr_payrollemployeeentity entity”</span><span class="sxs-lookup"><span data-stu-id="46ae3-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="46ae3-117">Darbuotojo ID</span><span class="sxs-lookup"><span data-stu-id="46ae3-117">Employee ID</span></span> |
| <span data-ttu-id="46ae3-118">**Užmokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-118">**Pay rate**</span></span><br><span data-ttu-id="46ae3-119">„mshr_payrate”</span><span class="sxs-lookup"><span data-stu-id="46ae3-119">mshr_payrate</span></span><br><span data-ttu-id="46ae3-120">*Dešimtainis*</span><span class="sxs-lookup"><span data-stu-id="46ae3-120">*Decimal*</span></span> | <span data-ttu-id="46ae3-121">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-121">Read-only</span></span><br><span data-ttu-id="46ae3-122">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-122">Required</span></span> | <span data-ttu-id="46ae3-123">Pastoviosios atlyginimo dalies plane apibrėžtas darbo užmokesčio tarifas.</span><span class="sxs-lookup"><span data-stu-id="46ae3-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="46ae3-124">**Plano ID**</span><span class="sxs-lookup"><span data-stu-id="46ae3-124">**Plan ID**</span></span><br><span data-ttu-id="46ae3-125">„mshr_planid”</span><span class="sxs-lookup"><span data-stu-id="46ae3-125">mshr_planid</span></span><br><span data-ttu-id="46ae3-126">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="46ae3-126">*String*</span></span> | <span data-ttu-id="46ae3-127">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-127">Read-only</span></span><br><span data-ttu-id="46ae3-128">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-128">Required</span></span> |<span data-ttu-id="46ae3-129">Nurodo atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="46ae3-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="46ae3-130">**Galioja nuo**</span><span class="sxs-lookup"><span data-stu-id="46ae3-130">**Valid from**</span></span><br><span data-ttu-id="46ae3-131">„mshr_validfrom”</span><span class="sxs-lookup"><span data-stu-id="46ae3-131">mshr_validfrom</span></span><br><span data-ttu-id="46ae3-132">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="46ae3-132">*Date Time Offset*</span></span> |  <span data-ttu-id="46ae3-133">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-133">Read-only</span></span><br><span data-ttu-id="46ae3-134">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-134">Required</span></span> |<span data-ttu-id="46ae3-135">Data, nuo kurios galioja darbuotojo pastovioji atlyginimo dalis.</span><span class="sxs-lookup"><span data-stu-id="46ae3-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="46ae3-136">**Algalapio pastoviosios atlyginimo dalies objektas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="46ae3-137">„mshr_payrollfixedcompensationplanentityid”</span><span class="sxs-lookup"><span data-stu-id="46ae3-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="46ae3-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="46ae3-138">*GUID*</span></span> | <span data-ttu-id="46ae3-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-139">Required</span></span><br><span data-ttu-id="46ae3-140">Sugeneruota sistemos</span><span class="sxs-lookup"><span data-stu-id="46ae3-140">Sytem generated</span></span> | <span data-ttu-id="46ae3-141">Sistemos sukurta GUID vertė siekiant unikaliai atpažinti atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="46ae3-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="46ae3-142">**Mokėjimų dažnumas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-142">**Pay frequency**</span></span><br><span data-ttu-id="46ae3-143">„mshr_payfrequency”</span><span class="sxs-lookup"><span data-stu-id="46ae3-143">mshr_payfrequency</span></span><br><span data-ttu-id="46ae3-144">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="46ae3-144">*String*</span></span> | <span data-ttu-id="46ae3-145">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-145">Read-only</span></span><br><span data-ttu-id="46ae3-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-146">Required</span></span> |<span data-ttu-id="46ae3-147">Dažnumas, kuriuo bus mokama darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="46ae3-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="46ae3-148">**Galioja iki**</span><span class="sxs-lookup"><span data-stu-id="46ae3-148">**Valid to**</span></span><br><span data-ttu-id="46ae3-149">„mshr_validto”</span><span class="sxs-lookup"><span data-stu-id="46ae3-149">mshr_validto</span></span><br><span data-ttu-id="46ae3-150">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="46ae3-150">*Date Time Offset*</span></span> | <span data-ttu-id="46ae3-151">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-151">Read-only</span></span> <br><span data-ttu-id="46ae3-152">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-152">Required</span></span> | <span data-ttu-id="46ae3-153">Data, iki kurios galioja darbuotojo pastovioji atlyginimo dalis.</span><span class="sxs-lookup"><span data-stu-id="46ae3-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="46ae3-154">**Pareigų ID**</span><span class="sxs-lookup"><span data-stu-id="46ae3-154">**Position ID**</span></span><br><span data-ttu-id="46ae3-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="46ae3-155">mshr_positionid</span></span><br><span data-ttu-id="46ae3-156">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="46ae3-156">*String*</span></span> | <span data-ttu-id="46ae3-157">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-157">Read-only</span></span> <br><span data-ttu-id="46ae3-158">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-158">Required</span></span> | <span data-ttu-id="46ae3-159">Pareigų ID, susietas su darbuotoju ir pastoviosios atlyginimo dalies plano registracija.</span><span class="sxs-lookup"><span data-stu-id="46ae3-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="46ae3-160">**Valiuta**</span><span class="sxs-lookup"><span data-stu-id="46ae3-160">**Currency**</span></span><br><span data-ttu-id="46ae3-161">„mshr_currency”</span><span class="sxs-lookup"><span data-stu-id="46ae3-161">mshr_currency</span></span><br><span data-ttu-id="46ae3-162">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="46ae3-162">*String*</span></span> | <span data-ttu-id="46ae3-163">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-163">Read-only</span></span> <br><span data-ttu-id="46ae3-164">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-164">Required</span></span> |<span data-ttu-id="46ae3-165">Valiuta, apibrėžta pastoviosios atlyginimo dalies planui</span><span class="sxs-lookup"><span data-stu-id="46ae3-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="46ae3-166">**Personalo numeris**</span><span class="sxs-lookup"><span data-stu-id="46ae3-166">**Personnel number**</span></span><br><span data-ttu-id="46ae3-167">„mshr_personnelnumber”</span><span class="sxs-lookup"><span data-stu-id="46ae3-167">mshr_personnelnumber</span></span><br><span data-ttu-id="46ae3-168">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="46ae3-168">*String*</span></span> | <span data-ttu-id="46ae3-169">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="46ae3-169">Read-only</span></span><br><span data-ttu-id="46ae3-170">Būtina</span><span class="sxs-lookup"><span data-stu-id="46ae3-170">Required</span></span> |<span data-ttu-id="46ae3-171">Unikalus darbuotojo personalo numeris.</span><span class="sxs-lookup"><span data-stu-id="46ae3-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="46ae3-172">**Užklausa**</span><span class="sxs-lookup"><span data-stu-id="46ae3-172">**Query**</span></span>

<span data-ttu-id="46ae3-173">**Prašymas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="46ae3-174">**Atsiliepimas**</span><span class="sxs-lookup"><span data-stu-id="46ae3-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
