---
title: Algalapio darbuotojo adresas
description: Šioje temoje pateikiama informacija ir Algalapio darbuotojo adreso objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020710"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="71911-103">Algalapio darbuotojo adresas</span><span class="sxs-lookup"><span data-stu-id="71911-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="71911-104">Šioje temoje pateikiama informacija ir Algalapio darbuotojo adreso objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="71911-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="71911-105">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="71911-105">Properties</span></span>

| <span data-ttu-id="71911-106">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="71911-106">Property</span></span><br><span data-ttu-id="71911-107">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="71911-107">**Physical name**</span></span><br><span data-ttu-id="71911-108">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="71911-108">**_Type_**</span></span> | <span data-ttu-id="71911-109">Naudoti</span><span class="sxs-lookup"><span data-stu-id="71911-109">Use</span></span> | <span data-ttu-id="71911-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="71911-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="71911-111">**Miestas**</span><span class="sxs-lookup"><span data-stu-id="71911-111">**City**</span></span><br><span data-ttu-id="71911-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="71911-112">mshr_city</span></span><br><span data-ttu-id="71911-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-113">*String*</span></span> | <span data-ttu-id="71911-114">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-114">Read-only</span></span><br><span data-ttu-id="71911-115">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-115">Required</span></span> | <span data-ttu-id="71911-116">Adrese nurodytas miestas.</span><span class="sxs-lookup"><span data-stu-id="71911-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="71911-117">**Darbuotojo numeris**</span><span class="sxs-lookup"><span data-stu-id="71911-117">**Personnel number**</span></span><br><span data-ttu-id="71911-118">„mshr_personnelnumber”</span><span class="sxs-lookup"><span data-stu-id="71911-118">mshr_personnelnumber</span></span><br><span data-ttu-id="71911-119">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-119">*String*</span></span> | <span data-ttu-id="71911-120">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-120">Read-only</span></span><br><span data-ttu-id="71911-121">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-121">Required</span></span> | <span data-ttu-id="71911-122">Unikalus darbuotojo personalo numeris.</span><span class="sxs-lookup"><span data-stu-id="71911-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="71911-123">**Šalies regionas**</span><span class="sxs-lookup"><span data-stu-id="71911-123">**Country region**</span></span><br><span data-ttu-id="71911-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="71911-124">mshr_countryregionid</span></span><br><span data-ttu-id="71911-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-125">*String*</span></span> | <span data-ttu-id="71911-126">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-126">Read-only</span></span><br><span data-ttu-id="71911-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-127">Required</span></span> | <span data-ttu-id="71911-128">Adrese nurodytas šalies regionas</span><span class="sxs-lookup"><span data-stu-id="71911-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="71911-129">**Galioja nuo**</span><span class="sxs-lookup"><span data-stu-id="71911-129">**Valid from**</span></span><br><span data-ttu-id="71911-130">„mshr_postaladdressvalidfrom”</span><span class="sxs-lookup"><span data-stu-id="71911-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="71911-131">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="71911-131">*Date Time Offset*</span></span> | <span data-ttu-id="71911-132">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-132">Read-only</span></span> <br><span data-ttu-id="71911-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-133">Required</span></span> | <span data-ttu-id="71911-134">Data, nuo kurios galioja adresas.</span><span class="sxs-lookup"><span data-stu-id="71911-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="71911-135">**Dirbo adresu**</span><span class="sxs-lookup"><span data-stu-id="71911-135">**Worked in address**</span></span><br><span data-ttu-id="71911-136">mshr_isworkedinaddressbr>*„Int32”*</span><span class="sxs-lookup"><span data-stu-id="71911-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="71911-137">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-137">Read-only</span></span><br><span data-ttu-id="71911-138">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-138">Required</span></span> | <span data-ttu-id="71911-139">Nurodo, ar adresas yra tas, kuriuo dirba darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="71911-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="71911-140">**Apygarda**</span><span class="sxs-lookup"><span data-stu-id="71911-140">**County**</span></span><br><span data-ttu-id="71911-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="71911-141">mshr_county</span></span><br><span data-ttu-id="71911-142">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-142">*String*</span></span> | <span data-ttu-id="71911-143">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-143">Read-only</span></span><br><span data-ttu-id="71911-144">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-144">Required</span></span> | <span data-ttu-id="71911-145">Adrese nurodyta apygarda.</span><span class="sxs-lookup"><span data-stu-id="71911-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="71911-146">**Algalapio darbuotojo adreso ID**</span><span class="sxs-lookup"><span data-stu-id="71911-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="71911-147">„mshr_payrollworkeraddressentityid”</span><span class="sxs-lookup"><span data-stu-id="71911-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="71911-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="71911-148">*GUID*</span></span> | <span data-ttu-id="71911-149">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-149">Required</span></span><br><span data-ttu-id="71911-150">Sistemos sugeneruota</span><span class="sxs-lookup"><span data-stu-id="71911-150">System generated</span></span> | <span data-ttu-id="71911-151">Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti adresą.</span><span class="sxs-lookup"><span data-stu-id="71911-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="71911-152">**Pirminis laukas**</span><span class="sxs-lookup"><span data-stu-id="71911-152">**Primary field**</span></span><br><span data-ttu-id="71911-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="71911-153">mshr_primaryfield</span></span><br><span data-ttu-id="71911-154">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-154">*String*</span></span> | <span data-ttu-id="71911-155">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-155">Read-only</span></span><br><span data-ttu-id="71911-156">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-156">Required</span></span> |  |
| <span data-ttu-id="71911-157">**Gatvė**</span><span class="sxs-lookup"><span data-stu-id="71911-157">**Street**</span></span><br><span data-ttu-id="71911-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="71911-158">mshr_street</span></span><br><span data-ttu-id="71911-159">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-159">*String*</span></span> | <span data-ttu-id="71911-160">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-160">Read-only</span></span><br><span data-ttu-id="71911-161">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-161">Required</span></span> | <span data-ttu-id="71911-162">Adrese nurodyta gatvė.</span><span class="sxs-lookup"><span data-stu-id="71911-162">The street defined for the address.</span></span> |
| <span data-ttu-id="71911-163">**Galioja iki**</span><span class="sxs-lookup"><span data-stu-id="71911-163">**Valid to**</span></span><br><span data-ttu-id="71911-164">„mshr_postaladdressvalidto”</span><span class="sxs-lookup"><span data-stu-id="71911-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="71911-165">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="71911-165">*Date Time Offset*</span></span> | <span data-ttu-id="71911-166">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-166">Read-only</span></span> <br><span data-ttu-id="71911-167">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-167">Required</span></span> | <span data-ttu-id="71911-168">Data, iki kurios galioja adresas.</span><span class="sxs-lookup"><span data-stu-id="71911-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="71911-169">**Vietos ID**</span><span class="sxs-lookup"><span data-stu-id="71911-169">**Location ID**</span></span><br><span data-ttu-id="71911-170">mshr_locationidbr>*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="71911-171">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-171">Read-only</span></span> <br><span data-ttu-id="71911-172">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-172">Required</span></span> | <span data-ttu-id="71911-173">Adreso ID.</span><span class="sxs-lookup"><span data-stu-id="71911-173">The ID for the address.</span></span>  |
| <span data-ttu-id="71911-174">**Pašto kodas (ZIP)**</span><span class="sxs-lookup"><span data-stu-id="71911-174">**Postal code**</span></span><br><span data-ttu-id="71911-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="71911-175">mshr_zipcode</span></span><br><span data-ttu-id="71911-176">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-176">*String*</span></span> | <span data-ttu-id="71911-177">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-177">Read-only</span></span> <br><span data-ttu-id="71911-178">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-178">Required</span></span> |<span data-ttu-id="71911-179">Darbuotojui apibrėžtas identifikacijos numeris.</span><span class="sxs-lookup"><span data-stu-id="71911-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="71911-180">**Gyveno adresu**</span><span class="sxs-lookup"><span data-stu-id="71911-180">**Lived in address**</span></span><br><span data-ttu-id="71911-181">mshr_islivedinaddressbr>*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="71911-182">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-182">Read-only</span></span><br><span data-ttu-id="71911-183">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-183">Required</span></span> | <span data-ttu-id="71911-184">Nurodo, ar adresas yra tas, kuriuo gyvena darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="71911-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="71911-185">**Apskritis**</span><span class="sxs-lookup"><span data-stu-id="71911-185">**State**</span></span><br><span data-ttu-id="71911-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="71911-186">mshr_state</span></span><br><span data-ttu-id="71911-187">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71911-187">*String*</span></span> | <span data-ttu-id="71911-188">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="71911-188">Read-only</span></span><br><span data-ttu-id="71911-189">Būtina</span><span class="sxs-lookup"><span data-stu-id="71911-189">Required</span></span> | <span data-ttu-id="71911-190">Adrese nurodyta valstija.</span><span class="sxs-lookup"><span data-stu-id="71911-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="71911-191">Pavyzdinė užklausa</span><span class="sxs-lookup"><span data-stu-id="71911-191">Example query</span></span>

<span data-ttu-id="71911-192">**Prašymas**</span><span class="sxs-lookup"><span data-stu-id="71911-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="71911-193">**Atsiliepimas**</span><span class="sxs-lookup"><span data-stu-id="71911-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
