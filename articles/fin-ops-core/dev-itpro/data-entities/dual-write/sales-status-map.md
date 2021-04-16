---
title: Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti dvigubo rašymo pardavimo užsakymo būsenos stulpelius.
author: dasani-madipalli
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
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750719"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a><span data-ttu-id="29199-103">Pardavimo užsakymo būsenos stulpelių susiejimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="29199-103">Set up the mapping for the sales order status columns</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29199-104">Stulpeliai, nurodantys pardavimo užsakymo būseną, turi skirtingas išvardijimo vertes „Microsoft Dynamics 365 Supply Chain Management” ir „Dynamics 365 sales” programose.</span><span class="sxs-lookup"><span data-stu-id="29199-104">The columns that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="29199-105">Būtini papildomi nustatymai, norint susieti stulpelius dvigubame rašyme.</span><span class="sxs-lookup"><span data-stu-id="29199-105">Additional setup is required to map these columns in dual-write.</span></span>

## <a name="columns-in-supply-chain-management"></a><span data-ttu-id="29199-106">„Supply Chain Management“ stulpeliai</span><span class="sxs-lookup"><span data-stu-id="29199-106">columns in Supply Chain Management</span></span>

<span data-ttu-id="29199-107">„Supply Chain Management“ dviejuose stulpeliuose nurodoma pardavimo užsakymo būsena.</span><span class="sxs-lookup"><span data-stu-id="29199-107">In Supply Chain Management, two columns reflect the status of the sales order.</span></span> <span data-ttu-id="29199-108">Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Dokumento būsena**.</span><span class="sxs-lookup"><span data-stu-id="29199-108">The columns that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="29199-109">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="29199-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="29199-110">Ši būsena rodoma užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="29199-110">This status is shown on the order header.</span></span>

<span data-ttu-id="29199-111">**Būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="29199-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="29199-112">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-112">Open Order</span></span>
- <span data-ttu-id="29199-113">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-113">Delivered</span></span>
- <span data-ttu-id="29199-114">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-114">Invoiced</span></span>
- <span data-ttu-id="29199-115">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-115">Cancelled</span></span>

<span data-ttu-id="29199-116">**Dokumento būsenos** išvardijimas nurodo vėliausią dokumentą, sugeneruotą užsakymui.</span><span class="sxs-lookup"><span data-stu-id="29199-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="29199-117">Pavyzdžiui, jei užsakymas patvirtintas, šis dokumentas yra pardavimo užsakymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="29199-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="29199-118">Jei pardavimo užsakymas yra dalinai išrašyta SF, o tada likusi eilutė patvirtinama, dokumento būsena lieka **SF**, nes vėliau vykstančiame procese SF sugeneruojama.</span><span class="sxs-lookup"><span data-stu-id="29199-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="29199-119">**Dokumento būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="29199-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="29199-120">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="29199-120">Confirmation</span></span>
- <span data-ttu-id="29199-121">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="29199-121">Picking List</span></span>
- <span data-ttu-id="29199-122">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="29199-122">Packing Slip</span></span>
- <span data-ttu-id="29199-123">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="29199-123">Invoice</span></span>

## <a name="columns-in-sales"></a><span data-ttu-id="29199-124">Pardavimų stulpeliai</span><span class="sxs-lookup"><span data-stu-id="29199-124">columns in Sales</span></span>

<span data-ttu-id="29199-125">Pardavimuose du stulpeliai nurodo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="29199-125">In Sales, two columns indicate the status of the order.</span></span> <span data-ttu-id="29199-126">Stulpeliai, kuriuos reikia susieti, pateikiami **Būsena** ir **Apdorojimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="29199-126">The columns that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="29199-127">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="29199-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="29199-128">Jam būdingos šios reikšmės:</span><span class="sxs-lookup"><span data-stu-id="29199-128">It has the following values:</span></span>

- <span data-ttu-id="29199-129">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-129">Active</span></span>
- <span data-ttu-id="29199-130">Pateikta</span><span class="sxs-lookup"><span data-stu-id="29199-130">Submitted</span></span>
- <span data-ttu-id="29199-131">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="29199-131">Fulfilled</span></span>
- <span data-ttu-id="29199-132">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-132">Invoiced</span></span>
- <span data-ttu-id="29199-133">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-133">Cancelled</span></span>

<span data-ttu-id="29199-134">**Apdorojimo būsenos** išvardijimas buvo įvestas tam, kad būseną būtų galima tiksliau susieti su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="29199-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="29199-135">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="29199-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="29199-136">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="29199-136">Processing Status</span></span>   | <span data-ttu-id="29199-137">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="29199-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="29199-138">Dokumento būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="29199-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="29199-139">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-139">Active</span></span>              | <span data-ttu-id="29199-140">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-140">Open Order</span></span>                        | <span data-ttu-id="29199-141">None</span><span class="sxs-lookup"><span data-stu-id="29199-141">None</span></span>                                       |
| <span data-ttu-id="29199-142">Pritarta</span><span class="sxs-lookup"><span data-stu-id="29199-142">Confirmed</span></span>           | <span data-ttu-id="29199-143">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-143">Open Order</span></span>                        | <span data-ttu-id="29199-144">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="29199-144">Confirmation</span></span>                               |
| <span data-ttu-id="29199-145">Paimta</span><span class="sxs-lookup"><span data-stu-id="29199-145">Picked</span></span>              | <span data-ttu-id="29199-146">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-146">Open Order</span></span>                        | <span data-ttu-id="29199-147">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="29199-147">Picking List</span></span>                               |
| <span data-ttu-id="29199-148">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-148">Partially Delivered</span></span> | <span data-ttu-id="29199-149">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-149">Open Order</span></span>                        | <span data-ttu-id="29199-150">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="29199-150">Packing Slip</span></span>                               |
| <span data-ttu-id="29199-151">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-151">Delivered</span></span>           | <span data-ttu-id="29199-152">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-152">Delivered</span></span>                         | <span data-ttu-id="29199-153">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="29199-153">Packing Slip</span></span>                               |
| <span data-ttu-id="29199-154">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-154">Partially Invoiced</span></span>  | <span data-ttu-id="29199-155">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-155">Delivered</span></span>                         | <span data-ttu-id="29199-156">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="29199-156">Invoice</span></span>                                    |
| <span data-ttu-id="29199-157">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-157">Invoiced</span></span>            | <span data-ttu-id="29199-158">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-158">Invoiced</span></span>                          | <span data-ttu-id="29199-159">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="29199-159">Invoice</span></span>                                    |
| <span data-ttu-id="29199-160">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-160">Cancelled</span></span>           | <span data-ttu-id="29199-161">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-161">Cancelled</span></span>                         | <span data-ttu-id="29199-162">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="29199-162">Not applicable</span></span>                             |

<span data-ttu-id="29199-163">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas tarp pardavimų ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="29199-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="29199-164">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="29199-164">Processing Status</span></span>   | <span data-ttu-id="29199-165">Būsena pardavimuose</span><span class="sxs-lookup"><span data-stu-id="29199-165">Status in Sales</span></span> | <span data-ttu-id="29199-166">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="29199-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="29199-167">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-167">Active</span></span>              | <span data-ttu-id="29199-168">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-168">Active</span></span>          | <span data-ttu-id="29199-169">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-169">Open Order</span></span>                        |
| <span data-ttu-id="29199-170">Pritarta</span><span class="sxs-lookup"><span data-stu-id="29199-170">Confirmed</span></span>           | <span data-ttu-id="29199-171">Pateikta</span><span class="sxs-lookup"><span data-stu-id="29199-171">Submitted</span></span>       | <span data-ttu-id="29199-172">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-172">Open Order</span></span>                        |
| <span data-ttu-id="29199-173">Paimta</span><span class="sxs-lookup"><span data-stu-id="29199-173">Picked</span></span>              | <span data-ttu-id="29199-174">Pateikta</span><span class="sxs-lookup"><span data-stu-id="29199-174">Submitted</span></span>       | <span data-ttu-id="29199-175">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-175">Open Order</span></span>                        |
| <span data-ttu-id="29199-176">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-176">Partially Delivered</span></span> | <span data-ttu-id="29199-177">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-177">Active</span></span>          | <span data-ttu-id="29199-178">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-178">Open Order</span></span>                        |
| <span data-ttu-id="29199-179">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-179">Partially Invoiced</span></span>  | <span data-ttu-id="29199-180">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="29199-180">Active</span></span>          | <span data-ttu-id="29199-181">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="29199-181">Open Order</span></span>                        |
| <span data-ttu-id="29199-182">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-182">Partially Invoiced</span></span>  | <span data-ttu-id="29199-183">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="29199-183">Fulfilled</span></span>       | <span data-ttu-id="29199-184">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="29199-184">Delivered</span></span>                         |
| <span data-ttu-id="29199-185">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-185">Invoiced</span></span>            | <span data-ttu-id="29199-186">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-186">Invoiced</span></span>        | <span data-ttu-id="29199-187">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="29199-187">Invoiced</span></span>                          |
| <span data-ttu-id="29199-188">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-188">Cancelled</span></span>           | <span data-ttu-id="29199-189">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-189">Cancelled</span></span>       | <span data-ttu-id="29199-190">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="29199-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="29199-191">Sąranka</span><span class="sxs-lookup"><span data-stu-id="29199-191">Setup</span></span>

<span data-ttu-id="29199-192">Norėdami nustatyti pardavimo užsakymo būsenos stulpelių susiejimą, turite įgalinti **IsSOPIntegrationEnabled** ir **isIntegrationUser** atributus.</span><span class="sxs-lookup"><span data-stu-id="29199-192">To set up the mapping for the sales order status columns, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="29199-193">Norėdami įgalinti **IsSOPIntegravimasĮjungtas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="29199-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="29199-194">Žiniatinklio naršyklėje eikite į `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="29199-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="29199-195">Pakeiskite **\<test-name\>** savo įmonės saitu į pardavimus.</span><span class="sxs-lookup"><span data-stu-id="29199-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="29199-196">Atidarytame puslapyje suraskite **OrganizacijosID** ir atkreipkite dėmesį į vertę.</span><span class="sxs-lookup"><span data-stu-id="29199-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizacijos ID radimas](media/sales-map-orgid.png)

3. <span data-ttu-id="29199-198">Dalyje Pardavimai atsidarykite naršyklės konsolę ir vykdykite šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="29199-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="29199-199">Naudokite **OrganizacijosID** vertę nuo 2 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="29199-199">Use the **organizationid** value from step 2.</span></span>

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

4. <span data-ttu-id="29199-201">Patikrinkite, ar **IsSOPIntegravimasĮjungtas** yra nustatytas kaip **teisingas**.</span><span class="sxs-lookup"><span data-stu-id="29199-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="29199-202">Naudokite URL, kurį nurodėte 1 veiksme, kad patikrintumėte vertę.</span><span class="sxs-lookup"><span data-stu-id="29199-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegravimasĮjungtas yra nustatytas kaip teisingas.](media/sales-map-integration-enabled.png)

<span data-ttu-id="29199-204">Norėdami įgalinti **isVartotojoIntegravimas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="29199-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="29199-205">Dalyje Pardavimai eikite į **Parametrai \> Tinkinimas \> Tinkinti sistemą**, pasirinkite **Vartotojo lentelė** ir tada atidarykite **Forma \> Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="29199-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User table**, and then open **Form \> User**.</span></span>

    ![Vartotojo formos atidarymas](media/sales-map-user.png)

2. <span data-ttu-id="29199-207">Laukų naršyklėje suraskite **Integravimo vartotojo režimas** ir du kartus spustelėkite jį, kad įtrauktumėte į formą.</span><span class="sxs-lookup"><span data-stu-id="29199-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="29199-208">Įrašykite savo pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="29199-208">Save your change.</span></span>

    ![Vartotojo režimo stulpelio integravimo į formą pridėjimas](media/sales-map-field-explorer.png)

3. <span data-ttu-id="29199-210">Dalyje Pardavimai eikite į **Parametras \> Sauga \> Vartotojai** ir pakeiskite rodinį iš **Įgalinti vartotojai** į **Taikomosios programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="29199-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Rodinio keitimas iš „Įgalinti vartotojai” į „Taikomosios programos vartotojai”](media/sales-map-enabled-users.png)

4. <span data-ttu-id="29199-212">Pasirinkite du **DviguboRašymo VartotojoIntegravimas** įrašus.</span><span class="sxs-lookup"><span data-stu-id="29199-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Taikomosios programos vartotojų sąrašas](media/sales-map-user-mode.png)

5. <span data-ttu-id="29199-214">Pakeiskite vertę į **Integravimo vartotojo režimas** stulpelį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="29199-214">Change the value of the **Integration user mode** column to **Yes**.</span></span>

    ![Integravimo vartotojo režimo stulpelio vertės pakeitimas](media/sales-map-user-mode-yes.png)

<span data-ttu-id="29199-216">Dabar Jūsų pardavimo užsakymai yra susieti.</span><span class="sxs-lookup"><span data-stu-id="29199-216">Your sales orders are now mapped.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]