---
title: Algalapio informacija pareigoms
description: Šioje temoje pateikiama Algalapio išsamios informacijos, skirtos Pareigų objektui, užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056785"
---
# <a name="payroll-position"></a><span data-ttu-id="f4736-103">Algalapio pareigos</span><span class="sxs-lookup"><span data-stu-id="f4736-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f4736-104">Šioje temoje pateikiama Algalapio išsamios informacijos, skirtos Pareigų objektui, užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="f4736-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="f4736-105">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="f4736-105">Properties</span></span>

| <span data-ttu-id="f4736-106">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="f4736-106">Property</span></span><br><span data-ttu-id="f4736-107">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="f4736-107">**Physical name**</span></span><br><span data-ttu-id="f4736-108">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="f4736-108">**_Type_**</span></span> | <span data-ttu-id="f4736-109">Naudoti</span><span class="sxs-lookup"><span data-stu-id="f4736-109">Use</span></span> | <span data-ttu-id="f4736-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="f4736-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f4736-111">**Įprastos darbo valandos per metus**</span><span class="sxs-lookup"><span data-stu-id="f4736-111">**Annual regular hours**</span></span><br><span data-ttu-id="f4736-112">„annualregularhours”</span><span class="sxs-lookup"><span data-stu-id="f4736-112">annualregularhours</span></span><br><span data-ttu-id="f4736-113">*Dešimtainis*</span><span class="sxs-lookup"><span data-stu-id="f4736-113">*Decimal*</span></span> | <span data-ttu-id="f4736-114">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-114">Read-only</span></span><br><span data-ttu-id="f4736-115">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-115">Required</span></span> | <span data-ttu-id="f4736-116">Pareigoms nustatytos įprastos darbo valandos per metus.</span><span class="sxs-lookup"><span data-stu-id="f4736-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="f4736-117">**Išsamios algalapio pareigų informacijos objekto ID**</span><span class="sxs-lookup"><span data-stu-id="f4736-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="f4736-118">„payrollpositiondetailsentityid”</span><span class="sxs-lookup"><span data-stu-id="f4736-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="f4736-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="f4736-119">*Guid*</span></span> | <span data-ttu-id="f4736-120">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-120">Required</span></span><br><span data-ttu-id="f4736-121">Sugeneruota sistemos.</span><span class="sxs-lookup"><span data-stu-id="f4736-121">System generated.</span></span> | <span data-ttu-id="f4736-122">Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti poziciją.</span><span class="sxs-lookup"><span data-stu-id="f4736-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="f4736-123">**Pirminis laukas**</span><span class="sxs-lookup"><span data-stu-id="f4736-123">**Primary field**</span></span><br><span data-ttu-id="f4736-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f4736-124">mshr_primaryfield</span></span><br><span data-ttu-id="f4736-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4736-125">*String*</span></span> | <span data-ttu-id="f4736-126">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-126">Required</span></span><br><span data-ttu-id="f4736-127">Sistemos sugeneruota</span><span class="sxs-lookup"><span data-stu-id="f4736-127">System generated</span></span> |  |
| <span data-ttu-id="f4736-128">**Darbo pareigų ID reikšmė**</span><span class="sxs-lookup"><span data-stu-id="f4736-128">**Position job ID value**</span></span><br><span data-ttu-id="f4736-129">„_mshr_fk_positionjob_id_value”</span><span class="sxs-lookup"><span data-stu-id="f4736-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="f4736-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f4736-130">*GUID*</span></span> | <span data-ttu-id="f4736-131">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-131">Read-only</span></span><br><span data-ttu-id="f4736-132">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-132">Required</span></span><br><span data-ttu-id="f4736-133">Išorinis raktas: „mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity”</span><span class="sxs-lookup"><span data-stu-id="f4736-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="f4736-134">Darbo ID yra susietas su pareigomis.</span><span class="sxs-lookup"><span data-stu-id="f4736-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="f4736-135">**Pastovios atlyginimo dalies plano ID reikšmė**</span><span class="sxs-lookup"><span data-stu-id="f4736-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="f4736-136">„_mshr_fk_fixedcompplan_id_value”</span><span class="sxs-lookup"><span data-stu-id="f4736-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="f4736-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f4736-137">*GUID*</span></span> | <span data-ttu-id="f4736-138">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-138">Read-only</span></span><br><span data-ttu-id="f4736-139">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-139">Required</span></span><br><span data-ttu-id="f4736-140">Išorinis raktas: „mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity”</span><span class="sxs-lookup"><span data-stu-id="f4736-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="f4736-141">Pastovios atlyginimo dalies plano ID yra susietas su pareigomis.</span><span class="sxs-lookup"><span data-stu-id="f4736-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="f4736-142">**Mokėjimų ciklo ID**</span><span class="sxs-lookup"><span data-stu-id="f4736-142">**Pay cycle ID**</span></span><br><span data-ttu-id="f4736-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="f4736-143">mshr_primaryfield</span></span><br><span data-ttu-id="f4736-144">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4736-144">*String*</span></span> | <span data-ttu-id="f4736-145">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-145">Read-only</span></span><br><span data-ttu-id="f4736-146">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-146">Required</span></span> | <span data-ttu-id="f4736-147">Pareigose apibrėžtas mokėjimo ciklas.</span><span class="sxs-lookup"><span data-stu-id="f4736-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="f4736-148">**Apmokėta juridinio subjekto**</span><span class="sxs-lookup"><span data-stu-id="f4736-148">**Paid by legal entity**</span></span><br><span data-ttu-id="f4736-149">„paidbylegalentity”</span><span class="sxs-lookup"><span data-stu-id="f4736-149">paidbylegalentity</span></span><br><span data-ttu-id="f4736-150">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4736-150">*String*</span></span> | <span data-ttu-id="f4736-151">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-151">Read-only</span></span><br><span data-ttu-id="f4736-152">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-152">Required</span></span> | <span data-ttu-id="f4736-153">Pareigose apibrėžtas juridinis subjektas, atsakingas už apmokėjimus.</span><span class="sxs-lookup"><span data-stu-id="f4736-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="f4736-154">**Pareigų ID**</span><span class="sxs-lookup"><span data-stu-id="f4736-154">**Position ID**</span></span><br><span data-ttu-id="f4736-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="f4736-155">mshr_positionid</span></span><br><span data-ttu-id="f4736-156">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="f4736-156">*String*</span></span> | <span data-ttu-id="f4736-157">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-157">Read-only</span></span><br><span data-ttu-id="f4736-158">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-158">Required</span></span> | <span data-ttu-id="f4736-159">Pareigų ID.</span><span class="sxs-lookup"><span data-stu-id="f4736-159">The ID of the position.</span></span> |
| <span data-ttu-id="f4736-160">**Galioja iki**</span><span class="sxs-lookup"><span data-stu-id="f4736-160">**Valid to**</span></span><br><span data-ttu-id="f4736-161">„validto”</span><span class="sxs-lookup"><span data-stu-id="f4736-161">validto</span></span><br><span data-ttu-id="f4736-162">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="f4736-162">*Date Time Offset*</span></span> | <span data-ttu-id="f4736-163">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-163">Read-only</span></span><br><span data-ttu-id="f4736-164">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-164">Required</span></span> |<span data-ttu-id="f4736-165">Data, nuo kurios galioja išsami informacija apie pareigas.</span><span class="sxs-lookup"><span data-stu-id="f4736-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="f4736-166">**Galioja nuo**</span><span class="sxs-lookup"><span data-stu-id="f4736-166">**Valid from**</span></span><br><span data-ttu-id="f4736-167">„validfrom”</span><span class="sxs-lookup"><span data-stu-id="f4736-167">validfrom</span></span><br><span data-ttu-id="f4736-168">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="f4736-168">*Date Time Offset*</span></span> | <span data-ttu-id="f4736-169">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="f4736-169">Read-only</span></span><br><span data-ttu-id="f4736-170">Būtina</span><span class="sxs-lookup"><span data-stu-id="f4736-170">Required</span></span> |<span data-ttu-id="f4736-171">Data, iki kurios galioja išsami informacija apie pareigas.</span><span class="sxs-lookup"><span data-stu-id="f4736-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="f4736-172">**Užklausa**</span><span class="sxs-lookup"><span data-stu-id="f4736-172">**Query**</span></span>

<span data-ttu-id="f4736-173">**Prašymas**</span><span class="sxs-lookup"><span data-stu-id="f4736-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="f4736-174">**Atsiliepimas**</span><span class="sxs-lookup"><span data-stu-id="f4736-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
