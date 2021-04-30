---
title: Algalapio darbuotojo adresas
description: Šioje temoje pateikiama informacija ir Algalapio darbuotojo adreso objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882038"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="3c800-103">Algalapio darbuotojo adresas</span><span class="sxs-lookup"><span data-stu-id="3c800-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3c800-104">Šioje temoje pateikiama informacija ir Algalapio darbuotojo adreso objekto užklausos pavyzdys „Dynamics 365 Human Resources“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="3c800-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="3c800-105">Ypatybės</span><span class="sxs-lookup"><span data-stu-id="3c800-105">Properties</span></span>

| <span data-ttu-id="3c800-106">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="3c800-106">Property</span></span><br><span data-ttu-id="3c800-107">**Faktinis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="3c800-107">**Physical name**</span></span><br><span data-ttu-id="3c800-108">**_Tipas_**</span><span class="sxs-lookup"><span data-stu-id="3c800-108">**_Type_**</span></span> | <span data-ttu-id="3c800-109">Naudoti</span><span class="sxs-lookup"><span data-stu-id="3c800-109">Use</span></span> | <span data-ttu-id="3c800-110">Aprašas</span><span class="sxs-lookup"><span data-stu-id="3c800-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3c800-111">**Miestas**</span><span class="sxs-lookup"><span data-stu-id="3c800-111">**City**</span></span><br><span data-ttu-id="3c800-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="3c800-112">mshr_city</span></span><br><span data-ttu-id="3c800-113">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-113">*String*</span></span> | <span data-ttu-id="3c800-114">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-114">Read-only</span></span><br><span data-ttu-id="3c800-115">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-115">Required</span></span> | <span data-ttu-id="3c800-116">Adrese nurodytas miestas.</span><span class="sxs-lookup"><span data-stu-id="3c800-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="3c800-117">**Darbuotojo numeris**</span><span class="sxs-lookup"><span data-stu-id="3c800-117">**Personnel number**</span></span><br><span data-ttu-id="3c800-118">„mshr_personnelnumber”</span><span class="sxs-lookup"><span data-stu-id="3c800-118">mshr_personnelnumber</span></span><br><span data-ttu-id="3c800-119">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-119">*String*</span></span> | <span data-ttu-id="3c800-120">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-120">Read-only</span></span><br><span data-ttu-id="3c800-121">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-121">Required</span></span> | <span data-ttu-id="3c800-122">Unikalus darbuotojo personalo numeris.</span><span class="sxs-lookup"><span data-stu-id="3c800-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="3c800-123">**Šalies regionas**</span><span class="sxs-lookup"><span data-stu-id="3c800-123">**Country region**</span></span><br><span data-ttu-id="3c800-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="3c800-124">mshr_countryregionid</span></span><br><span data-ttu-id="3c800-125">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-125">*String*</span></span> | <span data-ttu-id="3c800-126">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-126">Read-only</span></span><br><span data-ttu-id="3c800-127">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-127">Required</span></span> | <span data-ttu-id="3c800-128">Adrese nurodytas šalies regionas</span><span class="sxs-lookup"><span data-stu-id="3c800-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="3c800-129">**Galioja nuo**</span><span class="sxs-lookup"><span data-stu-id="3c800-129">**Valid from**</span></span><br><span data-ttu-id="3c800-130">„mshr_postaladdressvalidfrom”</span><span class="sxs-lookup"><span data-stu-id="3c800-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="3c800-131">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="3c800-131">*Date Time Offset*</span></span> | <span data-ttu-id="3c800-132">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-132">Read-only</span></span> <br><span data-ttu-id="3c800-133">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-133">Required</span></span> | <span data-ttu-id="3c800-134">Data, nuo kurios galioja adresas.</span><span class="sxs-lookup"><span data-stu-id="3c800-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="3c800-135">**Dirbo adresu**</span><span class="sxs-lookup"><span data-stu-id="3c800-135">**Worked in address**</span></span><br><span data-ttu-id="3c800-136">mshr_isworkedinaddressbr>*„Int32”*</span><span class="sxs-lookup"><span data-stu-id="3c800-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="3c800-137">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-137">Read-only</span></span><br><span data-ttu-id="3c800-138">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-138">Required</span></span> | <span data-ttu-id="3c800-139">Nurodo, ar adresas yra tas, kuriuo dirba darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="3c800-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="3c800-140">**Apygarda**</span><span class="sxs-lookup"><span data-stu-id="3c800-140">**County**</span></span><br><span data-ttu-id="3c800-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="3c800-141">mshr_county</span></span><br><span data-ttu-id="3c800-142">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-142">*String*</span></span> | <span data-ttu-id="3c800-143">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-143">Read-only</span></span><br><span data-ttu-id="3c800-144">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-144">Required</span></span> | <span data-ttu-id="3c800-145">Adrese nurodyta apygarda.</span><span class="sxs-lookup"><span data-stu-id="3c800-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="3c800-146">**Algalapio darbuotojo adreso ID**</span><span class="sxs-lookup"><span data-stu-id="3c800-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="3c800-147">„mshr_payrollworkeraddressentityid”</span><span class="sxs-lookup"><span data-stu-id="3c800-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="3c800-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3c800-148">*GUID*</span></span> | <span data-ttu-id="3c800-149">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-149">Required</span></span><br><span data-ttu-id="3c800-150">Sistemos sugeneruota</span><span class="sxs-lookup"><span data-stu-id="3c800-150">System generated</span></span> | <span data-ttu-id="3c800-151">Sistemos sukurta GUID reikšmė, skirta unikaliai atpažinti adresą.</span><span class="sxs-lookup"><span data-stu-id="3c800-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="3c800-152">**Pirminis laukas**</span><span class="sxs-lookup"><span data-stu-id="3c800-152">**Primary field**</span></span><br><span data-ttu-id="3c800-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3c800-153">mshr_primaryfield</span></span><br><span data-ttu-id="3c800-154">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-154">*String*</span></span> | <span data-ttu-id="3c800-155">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-155">Read-only</span></span><br><span data-ttu-id="3c800-156">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-156">Required</span></span> |  |
| <span data-ttu-id="3c800-157">**Gatvė**</span><span class="sxs-lookup"><span data-stu-id="3c800-157">**Street**</span></span><br><span data-ttu-id="3c800-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="3c800-158">mshr_street</span></span><br><span data-ttu-id="3c800-159">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-159">*String*</span></span> | <span data-ttu-id="3c800-160">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-160">Read-only</span></span><br><span data-ttu-id="3c800-161">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-161">Required</span></span> | <span data-ttu-id="3c800-162">Adrese nurodyta gatvė.</span><span class="sxs-lookup"><span data-stu-id="3c800-162">The street defined for the address.</span></span> |
| <span data-ttu-id="3c800-163">**Galioja iki**</span><span class="sxs-lookup"><span data-stu-id="3c800-163">**Valid to**</span></span><br><span data-ttu-id="3c800-164">„mshr_postaladdressvalidto”</span><span class="sxs-lookup"><span data-stu-id="3c800-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="3c800-165">*Datos ir Laiko poslinkis*</span><span class="sxs-lookup"><span data-stu-id="3c800-165">*Date Time Offset*</span></span> | <span data-ttu-id="3c800-166">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-166">Read-only</span></span> <br><span data-ttu-id="3c800-167">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-167">Required</span></span> | <span data-ttu-id="3c800-168">Data, iki kurios galioja adresas.</span><span class="sxs-lookup"><span data-stu-id="3c800-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="3c800-169">**Vietos ID**</span><span class="sxs-lookup"><span data-stu-id="3c800-169">**Location ID**</span></span><br><span data-ttu-id="3c800-170">mshr_locationidbr>*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="3c800-171">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-171">Read-only</span></span> <br><span data-ttu-id="3c800-172">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-172">Required</span></span> | <span data-ttu-id="3c800-173">Adreso ID.</span><span class="sxs-lookup"><span data-stu-id="3c800-173">The ID for the address.</span></span>  |
| <span data-ttu-id="3c800-174">**Pašto kodas (ZIP)**</span><span class="sxs-lookup"><span data-stu-id="3c800-174">**Postal code**</span></span><br><span data-ttu-id="3c800-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="3c800-175">mshr_zipcode</span></span><br><span data-ttu-id="3c800-176">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-176">*String*</span></span> | <span data-ttu-id="3c800-177">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-177">Read-only</span></span> <br><span data-ttu-id="3c800-178">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-178">Required</span></span> |<span data-ttu-id="3c800-179">Darbuotojui apibrėžtas identifikacijos numeris.</span><span class="sxs-lookup"><span data-stu-id="3c800-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="3c800-180">**Gyveno adresu**</span><span class="sxs-lookup"><span data-stu-id="3c800-180">**Lived in address**</span></span><br><span data-ttu-id="3c800-181">mshr_islivedinaddressbr>*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="3c800-182">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-182">Read-only</span></span><br><span data-ttu-id="3c800-183">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-183">Required</span></span> | <span data-ttu-id="3c800-184">Nurodo, ar adresas yra tas, kuriuo gyvena darbuotojas.</span><span class="sxs-lookup"><span data-stu-id="3c800-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="3c800-185">**Apskritis**</span><span class="sxs-lookup"><span data-stu-id="3c800-185">**State**</span></span><br><span data-ttu-id="3c800-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="3c800-186">mshr_state</span></span><br><span data-ttu-id="3c800-187">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="3c800-187">*String*</span></span> | <span data-ttu-id="3c800-188">Tik skaitomas</span><span class="sxs-lookup"><span data-stu-id="3c800-188">Read-only</span></span><br><span data-ttu-id="3c800-189">Būtina</span><span class="sxs-lookup"><span data-stu-id="3c800-189">Required</span></span> | <span data-ttu-id="3c800-190">Adrese nurodyta valstija.</span><span class="sxs-lookup"><span data-stu-id="3c800-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="3c800-191">Pavyzdinė užklausa</span><span class="sxs-lookup"><span data-stu-id="3c800-191">Example query</span></span>

<span data-ttu-id="3c800-192">**Prašymas**</span><span class="sxs-lookup"><span data-stu-id="3c800-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="3c800-193">**Atsiliepimas**</span><span class="sxs-lookup"><span data-stu-id="3c800-193">**Response**</span></span>

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
