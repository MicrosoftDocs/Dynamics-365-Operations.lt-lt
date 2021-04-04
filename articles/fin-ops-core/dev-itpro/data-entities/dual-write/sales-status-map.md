---
title: Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti dvigubo rašymo pardavimo užsakymo būsenos stulpelius.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: ecf26a2a697fa4d0485c1904041692a6c10ce9c3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560414"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="0e3af-103">Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0e3af-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e3af-104">Stulpeliai, nurodantys pardavimo užsakymo būseną, turi skirtingas išvardijimo vertes „Microsoft Dynamics 365 Supply Chain Management” ir „Dynamics 365 sales” programose.</span><span class="sxs-lookup"><span data-stu-id="0e3af-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="0e3af-105">Būtini papildomi nustatymai, norint susieti stulpelius dvigubame rašyme.</span><span class="sxs-lookup"><span data-stu-id="0e3af-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="0e3af-106">„Supply Chain Management“ stulpeliai</span><span class="sxs-lookup"><span data-stu-id="0e3af-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="0e3af-107">„Supply Chain Management“ dviejuose stulpeliuose nurodoma pardavimo užsakymo būsena.</span><span class="sxs-lookup"><span data-stu-id="0e3af-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="0e3af-108">Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Dokumento būsena**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="0e3af-109">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="0e3af-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0e3af-110">Ši būsena rodoma užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="0e3af-110">This status is shown on the order header.</span></span>

<span data-ttu-id="0e3af-111">**Būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0e3af-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0e3af-112">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-112">Open Order</span></span>
- <span data-ttu-id="0e3af-113">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-113">Delivered</span></span>
- <span data-ttu-id="0e3af-114">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-114">Invoiced</span></span>
- <span data-ttu-id="0e3af-115">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-115">Cancelled</span></span>

<span data-ttu-id="0e3af-116">**Dokumento būsenos** išvardijimas nurodo vėliausią dokumentą, sugeneruotą užsakymui.</span><span class="sxs-lookup"><span data-stu-id="0e3af-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="0e3af-117">Pavyzdžiui, jei užsakymas patvirtintas, šis dokumentas yra pardavimo užsakymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="0e3af-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="0e3af-118">Jei pardavimo užsakymas yra dalinai išrašyta SF, o tada likusi eilutė patvirtinama, dokumento būsena lieka **SF**, nes vėliau vykstančiame procese SF sugeneruojama.</span><span class="sxs-lookup"><span data-stu-id="0e3af-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="0e3af-119">**Dokumento būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0e3af-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="0e3af-120">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="0e3af-120">Confirmation</span></span>
- <span data-ttu-id="0e3af-121">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="0e3af-121">Picking List</span></span>
- <span data-ttu-id="0e3af-122">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="0e3af-122">Packing Slip</span></span>
- <span data-ttu-id="0e3af-123">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="0e3af-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="0e3af-124">Pardavimų stulpeliai</span><span class="sxs-lookup"><span data-stu-id="0e3af-124">columns in Sales</span></span>

<span data-ttu-id="0e3af-125">Pardavimuose du stulpeliai nurodo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="0e3af-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="0e3af-126">Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Apdorojimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="0e3af-127">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="0e3af-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="0e3af-128">Jam būdingos šios reikšmės:</span><span class="sxs-lookup"><span data-stu-id="0e3af-128">It has the following values:</span></span>

- <span data-ttu-id="0e3af-129">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-129">Active</span></span>
- <span data-ttu-id="0e3af-130">Pateikta</span><span class="sxs-lookup"><span data-stu-id="0e3af-130">Submitted</span></span>
- <span data-ttu-id="0e3af-131">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-131">Fulfilled</span></span>
- <span data-ttu-id="0e3af-132">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-132">Invoiced</span></span>
- <span data-ttu-id="0e3af-133">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-133">Cancelled</span></span>

<span data-ttu-id="0e3af-134">**Apdorojimo būsenos** išvardijimas buvo įvestas tam, kad būseną būtų galima tiksliau susieti su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0e3af-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="0e3af-135">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0e3af-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="0e3af-136">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="0e3af-136">Processing Status</span></span>   | <span data-ttu-id="0e3af-137">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="0e3af-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="0e3af-138">Dokumento būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="0e3af-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="0e3af-139">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-139">Active</span></span>              | <span data-ttu-id="0e3af-140">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-140">Open Order</span></span>                        | <span data-ttu-id="0e3af-141">None</span><span class="sxs-lookup"><span data-stu-id="0e3af-141">None</span></span>                                       |
| <span data-ttu-id="0e3af-142">Pritarta</span><span class="sxs-lookup"><span data-stu-id="0e3af-142">Confirmed</span></span>           | <span data-ttu-id="0e3af-143">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-143">Open Order</span></span>                        | <span data-ttu-id="0e3af-144">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="0e3af-144">Confirmation</span></span>                               |
| <span data-ttu-id="0e3af-145">Paimta</span><span class="sxs-lookup"><span data-stu-id="0e3af-145">Picked</span></span>              | <span data-ttu-id="0e3af-146">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-146">Open Order</span></span>                        | <span data-ttu-id="0e3af-147">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="0e3af-147">Picking List</span></span>                               |
| <span data-ttu-id="0e3af-148">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-148">Partially Delivered</span></span> | <span data-ttu-id="0e3af-149">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-149">Open Order</span></span>                        | <span data-ttu-id="0e3af-150">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="0e3af-150">Packing Slip</span></span>                               |
| <span data-ttu-id="0e3af-151">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-151">Delivered</span></span>           | <span data-ttu-id="0e3af-152">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-152">Delivered</span></span>                         | <span data-ttu-id="0e3af-153">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="0e3af-153">Packing Slip</span></span>                               |
| <span data-ttu-id="0e3af-154">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-154">Partially Invoiced</span></span>  | <span data-ttu-id="0e3af-155">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-155">Delivered</span></span>                         | <span data-ttu-id="0e3af-156">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="0e3af-156">Invoice</span></span>                                    |
| <span data-ttu-id="0e3af-157">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-157">Invoiced</span></span>            | <span data-ttu-id="0e3af-158">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-158">Invoiced</span></span>                          | <span data-ttu-id="0e3af-159">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="0e3af-159">Invoice</span></span>                                    |
| <span data-ttu-id="0e3af-160">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-160">Cancelled</span></span>           | <span data-ttu-id="0e3af-161">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-161">Cancelled</span></span>                         | <span data-ttu-id="0e3af-162">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="0e3af-162">Not applicable</span></span>                             |

<span data-ttu-id="0e3af-163">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas tarp pardavimų ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0e3af-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="0e3af-164">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="0e3af-164">Processing Status</span></span>   | <span data-ttu-id="0e3af-165">Būsena pardavimuose</span><span class="sxs-lookup"><span data-stu-id="0e3af-165">Status in Sales</span></span> | <span data-ttu-id="0e3af-166">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="0e3af-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="0e3af-167">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-167">Active</span></span>              | <span data-ttu-id="0e3af-168">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-168">Active</span></span>          | <span data-ttu-id="0e3af-169">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-169">Open Order</span></span>                        |
| <span data-ttu-id="0e3af-170">Pritarta</span><span class="sxs-lookup"><span data-stu-id="0e3af-170">Confirmed</span></span>           | <span data-ttu-id="0e3af-171">Pateikta</span><span class="sxs-lookup"><span data-stu-id="0e3af-171">Submitted</span></span>       | <span data-ttu-id="0e3af-172">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-172">Open Order</span></span>                        |
| <span data-ttu-id="0e3af-173">Paimta</span><span class="sxs-lookup"><span data-stu-id="0e3af-173">Picked</span></span>              | <span data-ttu-id="0e3af-174">Pateikta</span><span class="sxs-lookup"><span data-stu-id="0e3af-174">Submitted</span></span>       | <span data-ttu-id="0e3af-175">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-175">Open Order</span></span>                        |
| <span data-ttu-id="0e3af-176">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-176">Partially Delivered</span></span> | <span data-ttu-id="0e3af-177">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-177">Active</span></span>          | <span data-ttu-id="0e3af-178">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-178">Open Order</span></span>                        |
| <span data-ttu-id="0e3af-179">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-179">Partially Invoiced</span></span>  | <span data-ttu-id="0e3af-180">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="0e3af-180">Active</span></span>          | <span data-ttu-id="0e3af-181">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="0e3af-181">Open Order</span></span>                        |
| <span data-ttu-id="0e3af-182">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-182">Partially Invoiced</span></span>  | <span data-ttu-id="0e3af-183">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-183">Fulfilled</span></span>       | <span data-ttu-id="0e3af-184">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="0e3af-184">Delivered</span></span>                         |
| <span data-ttu-id="0e3af-185">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-185">Invoiced</span></span>            | <span data-ttu-id="0e3af-186">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-186">Invoiced</span></span>        | <span data-ttu-id="0e3af-187">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="0e3af-187">Invoiced</span></span>                          |
| <span data-ttu-id="0e3af-188">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-188">Cancelled</span></span>           | <span data-ttu-id="0e3af-189">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-189">Cancelled</span></span>       | <span data-ttu-id="0e3af-190">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="0e3af-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="0e3af-191">Sąranka</span><span class="sxs-lookup"><span data-stu-id="0e3af-191">Setup</span></span>

<span data-ttu-id="0e3af-192">Norėdami nustatyti pardavimo užsakymo būsenos stulpelių susiejimą, turite įgalinti **IsSOPIntegrationEnabled** ir **isIntegrationUser** atributus.</span><span class="sxs-lookup"><span data-stu-id="0e3af-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="0e3af-193">Norėdami įgalinti **IsSOPIntegravimasĮjungtas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e3af-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0e3af-194">Žiniatinklio naršyklėje eikite į `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="0e3af-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="0e3af-195">Pakeiskite **\<test-name\>** savo įmonės saitu į pardavimus.</span><span class="sxs-lookup"><span data-stu-id="0e3af-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="0e3af-196">Atidarytame puslapyje suraskite **OrganizacijosID** ir atkreipkite dėmesį į vertę.</span><span class="sxs-lookup"><span data-stu-id="0e3af-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizacijos ID radimas](media/sales-map-orgid.png)

3. <span data-ttu-id="0e3af-198">Dalyje Pardavimai atsidarykite naršyklės konsolę ir vykdykite šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="0e3af-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="0e3af-199">Naudokite **OrganizacijosID** vertę nuo 2 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="0e3af-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![„JavaScript” kodas naršyklės konsolėje](media/sales-map-script.png)

4. <span data-ttu-id="0e3af-201">Patikrinkite, ar **IsSOPIntegravimasĮjungtas** yra nustatytas kaip **teisingas**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="0e3af-202">Naudokite URL, kurį nurodėte 1 veiksme, kad patikrintumėte vertę.</span><span class="sxs-lookup"><span data-stu-id="0e3af-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegravimasĮjungtas yra nustatytas kaip teisingas.](media/sales-map-integration-enabled.png)

<span data-ttu-id="0e3af-204">Norėdami įgalinti **isVartotojoIntegravimas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0e3af-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="0e3af-205">Dalyje Pardavimai eikite į **Parametrai \> Tinkinimas \> Tinkinti sistemą**, pasirinkite **Vartotojo lentelė** ir tada atidarykite **Forma \> Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Vartotojo formos atidarymas](media/sales-map-user.png)

2. <span data-ttu-id="0e3af-207">Laukų naršyklėje suraskite **Integravimo vartotojo režimas** ir du kartus spustelėkite jį, kad įtrauktumėte į formą.</span><span class="sxs-lookup"><span data-stu-id="0e3af-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="0e3af-208">Įrašykite savo pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="0e3af-208">Save your change.</span></span>

    ![Vartotojo režimo stulpelio integravimo į formą pridėjimas](media/sales-map-field-explorer.png)

3. <span data-ttu-id="0e3af-210">Dalyje Pardavimai eikite į **Parametras \> Sauga \> Vartotojai** ir pakeiskite rodinį iš **Įgalinti vartotojai** į **Taikomosios programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Rodinio keitimas iš „Įgalinti vartotojai” į „Taikomosios programos vartotojai”](media/sales-map-enabled-users.png)

4. <span data-ttu-id="0e3af-212">Pasirinkite du **DviguboRašymo VartotojoIntegravimas** įrašus.</span><span class="sxs-lookup"><span data-stu-id="0e3af-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Taikomosios programos vartotojų sąrašas](media/sales-map-user-mode.png)

5. <span data-ttu-id="0e3af-214">Pakeiskite vertę į **Integravimo vartotojo režimas** stulpelį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0e3af-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Integravimo vartotojo režimo stulpelio vertės pakeitimas](media/sales-map-user-mode-yes.png)

<span data-ttu-id="0e3af-216">Dabar Jūsų pardavimo užsakymai yra susieti.</span><span class="sxs-lookup"><span data-stu-id="0e3af-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]