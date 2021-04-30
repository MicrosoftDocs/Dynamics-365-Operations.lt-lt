---
title: Algalapio pastoviosios atlyginimo dalies planas
description: Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
manager: tfehr
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882041"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="88581-103">Algalapio pastoviosios atlyginimo dalies planas</span><span class="sxs-lookup"><span data-stu-id="88581-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88581-104">Šioje temoje pateikiama informacija ir Algalapio pastoviosios atlyginimo dalies plano objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="88581-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="88581-105">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="88581-105">Properties</span></span>

| <span data-ttu-id="88581-106">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="88581-106">Property</span></span><br><span data-ttu-id="88581-107">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="88581-107">**Physical name**</span></span><br><span data-ttu-id="88581-108">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="88581-108">**_Type_**</span></span> | <span data-ttu-id="88581-109">Naudoti</span><span class="sxs-lookup"><span data-stu-id="88581-109">Use</span></span> | <span data-ttu-id="88581-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="88581-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="88581-111">**Darbuotojo ID**</span><span class="sxs-lookup"><span data-stu-id="88581-111">**Employee ID**</span></span><br><span data-ttu-id="88581-112">„mshr_fk_employee_id_value”</span><span class="sxs-lookup"><span data-stu-id="88581-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="88581-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="88581-113">*GUID*</span></span> | <span data-ttu-id="88581-114">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-114">Read-only</span></span><br><span data-ttu-id="88581-115">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-115">Required</span></span><br><span data-ttu-id="88581-116">Išorinis raktas: „mshr_Employee_id of mshr_payrollemployeeentity entity”</span><span class="sxs-lookup"><span data-stu-id="88581-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="88581-117">Darbuotojo ID</span><span class="sxs-lookup"><span data-stu-id="88581-117">Employee ID</span></span> |
| <span data-ttu-id="88581-118">**Užmokesčio tarifas**</span><span class="sxs-lookup"><span data-stu-id="88581-118">**Pay rate**</span></span><br><span data-ttu-id="88581-119">„mshr_payrate”</span><span class="sxs-lookup"><span data-stu-id="88581-119">mshr_payrate</span></span><br><span data-ttu-id="88581-120">*Dešimtainis*</span><span class="sxs-lookup"><span data-stu-id="88581-120">*Decimal*</span></span> | <span data-ttu-id="88581-121">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-121">Read-only</span></span><br><span data-ttu-id="88581-122">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-122">Required</span></span> | <span data-ttu-id="88581-123">Pastoviosios atlyginimo dalies plane apibrėžtas darbo užmokesčio tarifas.</span><span class="sxs-lookup"><span data-stu-id="88581-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="88581-124">**Plano ID**</span><span class="sxs-lookup"><span data-stu-id="88581-124">**Plan ID**</span></span><br><span data-ttu-id="88581-125">„mshr_planid”</span><span class="sxs-lookup"><span data-stu-id="88581-125">mshr_planid</span></span><br><span data-ttu-id="88581-126">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="88581-126">*String*</span></span> | <span data-ttu-id="88581-127">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-127">Read-only</span></span><br><span data-ttu-id="88581-128">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-128">Required</span></span> |<span data-ttu-id="88581-129">Nurodo atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="88581-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="88581-130">**Galioja nuo**</span><span class="sxs-lookup"><span data-stu-id="88581-130">**Valid from**</span></span><br><span data-ttu-id="88581-131">„mshr_validfrom”</span><span class="sxs-lookup"><span data-stu-id="88581-131">mshr_validfrom</span></span><br><span data-ttu-id="88581-132">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="88581-132">*Date Time Offset*</span></span> |  <span data-ttu-id="88581-133">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-133">Read-only</span></span><br><span data-ttu-id="88581-134">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-134">Required</span></span> |<span data-ttu-id="88581-135">Data, nuo kurios galioja darbuotojo pastovioji atlyginimo dalis.</span><span class="sxs-lookup"><span data-stu-id="88581-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="88581-136">**Algalapio pastoviosios atlyginimo dalies objektas**</span><span class="sxs-lookup"><span data-stu-id="88581-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="88581-137">„mshr_payrollfixedcompensationplanentityid”</span><span class="sxs-lookup"><span data-stu-id="88581-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="88581-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="88581-138">*GUID*</span></span> | <span data-ttu-id="88581-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-139">Required</span></span><br><span data-ttu-id="88581-140">Sugeneruota sistemos</span><span class="sxs-lookup"><span data-stu-id="88581-140">Sytem generated</span></span> | <span data-ttu-id="88581-141">Sistemos sukurta GUID vertė siekiant unikaliai atpažinti atlyginimo dalies planą.</span><span class="sxs-lookup"><span data-stu-id="88581-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="88581-142">**Mokėjimų dažnumas**</span><span class="sxs-lookup"><span data-stu-id="88581-142">**Pay frequency**</span></span><br><span data-ttu-id="88581-143">„mshr_payfrequency”</span><span class="sxs-lookup"><span data-stu-id="88581-143">mshr_payfrequency</span></span><br><span data-ttu-id="88581-144">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="88581-144">*String*</span></span> | <span data-ttu-id="88581-145">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-145">Read-only</span></span><br><span data-ttu-id="88581-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-146">Required</span></span> |<span data-ttu-id="88581-147">Dažnumas, kuriuo bus mokama darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="88581-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="88581-148">**Galioja iki**</span><span class="sxs-lookup"><span data-stu-id="88581-148">**Valid to**</span></span><br><span data-ttu-id="88581-149">„mshr_validto”</span><span class="sxs-lookup"><span data-stu-id="88581-149">mshr_validto</span></span><br><span data-ttu-id="88581-150">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="88581-150">*Date Time Offset*</span></span> | <span data-ttu-id="88581-151">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-151">Read-only</span></span> <br><span data-ttu-id="88581-152">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-152">Required</span></span> | <span data-ttu-id="88581-153">Data, iki kurios galioja darbuotojo pastovioji atlyginimo dalis.</span><span class="sxs-lookup"><span data-stu-id="88581-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="88581-154">**Pareigų ID**</span><span class="sxs-lookup"><span data-stu-id="88581-154">**Position ID**</span></span><br><span data-ttu-id="88581-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="88581-155">mshr_positionid</span></span><br><span data-ttu-id="88581-156">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="88581-156">*String*</span></span> | <span data-ttu-id="88581-157">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-157">Read-only</span></span> <br><span data-ttu-id="88581-158">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-158">Required</span></span> | <span data-ttu-id="88581-159">Pareigų ID, susietas su darbuotoju ir pastoviosios atlyginimo dalies plano registracija.</span><span class="sxs-lookup"><span data-stu-id="88581-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="88581-160">**Valiuta**</span><span class="sxs-lookup"><span data-stu-id="88581-160">**Currency**</span></span><br><span data-ttu-id="88581-161">„mshr_currency”</span><span class="sxs-lookup"><span data-stu-id="88581-161">mshr_currency</span></span><br><span data-ttu-id="88581-162">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="88581-162">*String*</span></span> | <span data-ttu-id="88581-163">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-163">Read-only</span></span> <br><span data-ttu-id="88581-164">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-164">Required</span></span> |<span data-ttu-id="88581-165">Valiuta, apibrėžta pastoviosios atlyginimo dalies planui</span><span class="sxs-lookup"><span data-stu-id="88581-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="88581-166">**Personalo numeris**</span><span class="sxs-lookup"><span data-stu-id="88581-166">**Personnel number**</span></span><br><span data-ttu-id="88581-167">„mshr_personnelnumber”</span><span class="sxs-lookup"><span data-stu-id="88581-167">mshr_personnelnumber</span></span><br><span data-ttu-id="88581-168">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="88581-168">*String*</span></span> | <span data-ttu-id="88581-169">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="88581-169">Read-only</span></span><br><span data-ttu-id="88581-170">Būtina</span><span class="sxs-lookup"><span data-stu-id="88581-170">Required</span></span> |<span data-ttu-id="88581-171">Unikalus darbuotojo personalo numeris.</span><span class="sxs-lookup"><span data-stu-id="88581-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="88581-172">**Užklausa**</span><span class="sxs-lookup"><span data-stu-id="88581-172">**Query**</span></span>

<span data-ttu-id="88581-173">**Prašymas**</span><span class="sxs-lookup"><span data-stu-id="88581-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="88581-174">**Atsiliepimas**</span><span class="sxs-lookup"><span data-stu-id="88581-174">**Response**</span></span>

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
