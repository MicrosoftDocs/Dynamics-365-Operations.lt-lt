---
title: Konvertavimo nustatymas pardavimo užsakymo būsenos laukams
description: Šioje temoje aiškinama, kaip nustatyti dvigubo rašymo pardavimo užsakymo būsenos laukus.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: dce4b6310e2f6d31a115302efa7fbc132799e48f
ms.sourcegitcommit: 4ba10abe5be8a21b95370cd970a622e954970984
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829290"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="dc318-103">Konvertavimo nustatymas pardavimo užsakymo būsenos laukams</span><span class="sxs-lookup"><span data-stu-id="dc318-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc318-104">Laukai, kurie nurodo pardavimo užsakymo būseną, turi skirtingas išvardijimo vertes „Microsoft Dynamics 365 Supply Chain Management” ir „Dynamics 365 sales” programose.</span><span class="sxs-lookup"><span data-stu-id="dc318-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="dc318-105">Būtini papildomi nustatymai, norint konvertuoti šiuos laukus dvigubam rašymui.</span><span class="sxs-lookup"><span data-stu-id="dc318-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="dc318-106">„Supply Chain Management“ laukai</span><span class="sxs-lookup"><span data-stu-id="dc318-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="dc318-107">„Supply Chain Management“ du laukai perteikia pardavimo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="dc318-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="dc318-108">Laukai, kuriuos reikia susieti, yra **Būsena** ir **Dokumento būsena**.</span><span class="sxs-lookup"><span data-stu-id="dc318-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="dc318-109">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="dc318-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="dc318-110">Ši būsena rodoma užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="dc318-110">This status is shown on the order header.</span></span>

<span data-ttu-id="dc318-111">**Būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="dc318-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="dc318-112">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-112">Open Order</span></span>
- <span data-ttu-id="dc318-113">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-113">Delivered</span></span>
- <span data-ttu-id="dc318-114">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-114">Invoiced</span></span>
- <span data-ttu-id="dc318-115">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-115">Cancelled</span></span>

<span data-ttu-id="dc318-116">**Dokumento būsenos** išvardijimas nurodo vėliausią dokumentą, sugeneruotą užsakymui.</span><span class="sxs-lookup"><span data-stu-id="dc318-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="dc318-117">Pavyzdžiui, jei užsakymas patvirtintas, šis dokumentas yra pardavimo užsakymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="dc318-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="dc318-118">Jei pardavimo užsakymas yra dalinai išrašyta SF, o tada likusi eilutė patvirtinama, dokumento būsena lieka **SF**, nes vėliau vykstančiame procese SF sugeneruojama.</span><span class="sxs-lookup"><span data-stu-id="dc318-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="dc318-119">**Dokumento būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="dc318-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="dc318-120">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="dc318-120">Confirmation</span></span>
- <span data-ttu-id="dc318-121">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="dc318-121">Picking List</span></span>
- <span data-ttu-id="dc318-122">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="dc318-122">Packing Slip</span></span>
- <span data-ttu-id="dc318-123">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="dc318-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="dc318-124">Pardavimo laukai</span><span class="sxs-lookup"><span data-stu-id="dc318-124">Fields in Sales</span></span>

<span data-ttu-id="dc318-125">Pardavimuose du laukai nurodo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="dc318-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="dc318-126">Laukai, kuriuos reikia konvertuoti, yra **Būsena** ir **Apdorojimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="dc318-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="dc318-127">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="dc318-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="dc318-128">Jam būdingos šios reikšmės:</span><span class="sxs-lookup"><span data-stu-id="dc318-128">It has the following values:</span></span>

- <span data-ttu-id="dc318-129">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-129">Active</span></span>
- <span data-ttu-id="dc318-130">Pateikta</span><span class="sxs-lookup"><span data-stu-id="dc318-130">Submitted</span></span>
- <span data-ttu-id="dc318-131">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="dc318-131">Fulfilled</span></span>
- <span data-ttu-id="dc318-132">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-132">Invoiced</span></span>
- <span data-ttu-id="dc318-133">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-133">Cancelled</span></span>

<span data-ttu-id="dc318-134">**Apdorojimo būsenos** išvardijimas buvo įvestas tam, kad būseną būtų galima tiksliau susieti su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="dc318-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="dc318-135">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="dc318-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="dc318-136">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="dc318-136">Processing Status</span></span>   | <span data-ttu-id="dc318-137">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="dc318-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="dc318-138">Dokumento būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="dc318-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="dc318-139">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-139">Active</span></span>              | <span data-ttu-id="dc318-140">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-140">Open Order</span></span>                        | <span data-ttu-id="dc318-141">None</span><span class="sxs-lookup"><span data-stu-id="dc318-141">None</span></span>                                       |
| <span data-ttu-id="dc318-142">Pritarta</span><span class="sxs-lookup"><span data-stu-id="dc318-142">Confirmed</span></span>           | <span data-ttu-id="dc318-143">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-143">Open Order</span></span>                        | <span data-ttu-id="dc318-144">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="dc318-144">Confirmation</span></span>                               |
| <span data-ttu-id="dc318-145">Paimta</span><span class="sxs-lookup"><span data-stu-id="dc318-145">Picked</span></span>              | <span data-ttu-id="dc318-146">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-146">Open Order</span></span>                        | <span data-ttu-id="dc318-147">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="dc318-147">Picking List</span></span>                               |
| <span data-ttu-id="dc318-148">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-148">Partially Delivered</span></span> | <span data-ttu-id="dc318-149">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-149">Open Order</span></span>                        | <span data-ttu-id="dc318-150">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="dc318-150">Packing Slip</span></span>                               |
| <span data-ttu-id="dc318-151">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-151">Delivered</span></span>           | <span data-ttu-id="dc318-152">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-152">Delivered</span></span>                         | <span data-ttu-id="dc318-153">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="dc318-153">Packing Slip</span></span>                               |
| <span data-ttu-id="dc318-154">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-154">Partially Invoiced</span></span>  | <span data-ttu-id="dc318-155">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-155">Delivered</span></span>                         | <span data-ttu-id="dc318-156">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="dc318-156">Invoice</span></span>                                    |
| <span data-ttu-id="dc318-157">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-157">Invoiced</span></span>            | <span data-ttu-id="dc318-158">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-158">Invoiced</span></span>                          | <span data-ttu-id="dc318-159">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="dc318-159">Invoice</span></span>                                    |
| <span data-ttu-id="dc318-160">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-160">Cancelled</span></span>           | <span data-ttu-id="dc318-161">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-161">Cancelled</span></span>                         | <span data-ttu-id="dc318-162">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="dc318-162">Not applicable</span></span>                             |

<span data-ttu-id="dc318-163">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas tarp pardavimų ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="dc318-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="dc318-164">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="dc318-164">Processing Status</span></span>   | <span data-ttu-id="dc318-165">Būsena pardavimuose</span><span class="sxs-lookup"><span data-stu-id="dc318-165">Status in Sales</span></span> | <span data-ttu-id="dc318-166">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="dc318-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="dc318-167">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-167">Active</span></span>              | <span data-ttu-id="dc318-168">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-168">Active</span></span>          | <span data-ttu-id="dc318-169">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-169">Open Order</span></span>                        |
| <span data-ttu-id="dc318-170">Pritarta</span><span class="sxs-lookup"><span data-stu-id="dc318-170">Confirmed</span></span>           | <span data-ttu-id="dc318-171">Pateikta</span><span class="sxs-lookup"><span data-stu-id="dc318-171">Submitted</span></span>       | <span data-ttu-id="dc318-172">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-172">Open Order</span></span>                        |
| <span data-ttu-id="dc318-173">Paimta</span><span class="sxs-lookup"><span data-stu-id="dc318-173">Picked</span></span>              | <span data-ttu-id="dc318-174">Pateikta</span><span class="sxs-lookup"><span data-stu-id="dc318-174">Submitted</span></span>       | <span data-ttu-id="dc318-175">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-175">Open Order</span></span>                        |
| <span data-ttu-id="dc318-176">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-176">Partially Delivered</span></span> | <span data-ttu-id="dc318-177">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-177">Active</span></span>          | <span data-ttu-id="dc318-178">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-178">Open Order</span></span>                        |
| <span data-ttu-id="dc318-179">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-179">Partially Invoiced</span></span>  | <span data-ttu-id="dc318-180">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="dc318-180">Active</span></span>          | <span data-ttu-id="dc318-181">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="dc318-181">Open Order</span></span>                        |
| <span data-ttu-id="dc318-182">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-182">Partially Invoiced</span></span>  | <span data-ttu-id="dc318-183">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="dc318-183">Fulfilled</span></span>       | <span data-ttu-id="dc318-184">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="dc318-184">Delivered</span></span>                         |
| <span data-ttu-id="dc318-185">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-185">Invoiced</span></span>            | <span data-ttu-id="dc318-186">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-186">Invoiced</span></span>        | <span data-ttu-id="dc318-187">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="dc318-187">Invoiced</span></span>                          |
| <span data-ttu-id="dc318-188">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-188">Cancelled</span></span>           | <span data-ttu-id="dc318-189">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-189">Cancelled</span></span>       | <span data-ttu-id="dc318-190">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="dc318-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="dc318-191">Sąranka</span><span class="sxs-lookup"><span data-stu-id="dc318-191">Setup</span></span>

<span data-ttu-id="dc318-192">Norėdami nustatyti pardavimo užsakymo būsenos laukų konvertavimą, turite įgalinti **IsSOPIntegravimasĮjungtas** ir **isVartotojoIntegravimas** atributus.</span><span class="sxs-lookup"><span data-stu-id="dc318-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="dc318-193">Norėdami įgalinti **IsSOPIntegravimasĮjungtas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc318-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="dc318-194">Žiniatinklio naršyklėje eikite į `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="dc318-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="dc318-195">Pakeiskite **\<test-name\>** savo įmonės saitu į pardavimus.</span><span class="sxs-lookup"><span data-stu-id="dc318-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="dc318-196">Atidarytame puslapyje suraskite **OrganizacijosID** ir atkreipkite dėmesį į vertę.</span><span class="sxs-lookup"><span data-stu-id="dc318-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizacijos ID radimas](media/sales-map-orgid.png)

3. <span data-ttu-id="dc318-198">Dalyje Pardavimai atsidarykite naršyklės konsolę ir vykdykite šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="dc318-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="dc318-199">Naudokite **OrganizacijosID** vertę nuo 2 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="dc318-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![„JavaScript” kodas naršyklės konsolėje](media/sales-map-script.png)

4. <span data-ttu-id="dc318-201">Patikrinkite, ar **IsSOPIntegravimasĮjungtas** yra nustatytas kaip **teisingas**.</span><span class="sxs-lookup"><span data-stu-id="dc318-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="dc318-202">Naudokite URL, kurį nurodėte 1 veiksme, kad patikrintumėte vertę.</span><span class="sxs-lookup"><span data-stu-id="dc318-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegravimasĮjungtas yra nustatytas kaip teisingas.](media/sales-map-integration-enabled.png)

<span data-ttu-id="dc318-204">Norėdami įgalinti **isVartotojoIntegravimas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dc318-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="dc318-205">Dalyje Pardavimai eikite į **Parametras \> Tinkinimas \> Tinkinti sistemą**, pasirinkite **Vartotojo objektas** ir tada atidarykite **Forma \> Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="dc318-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Vartotojo formos atidarymas](media/sales-map-user.png)

2. <span data-ttu-id="dc318-207">Laukų naršyklėje suraskite **Integravimo vartotojo režimas** ir du kartus spustelėkite jį, kad įtrauktumėte į formą.</span><span class="sxs-lookup"><span data-stu-id="dc318-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="dc318-208">Įrašykite savo pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="dc318-208">Save your change.</span></span>

    ![Integravimo vartotojo režimo lauko įtraukimas į formą](media/sales-map-field-explorer.png)

3. <span data-ttu-id="dc318-210">Dalyje Pardavimai eikite į **Parametras \> Sauga \> Vartotojai** ir pakeiskite rodinį iš **Įgalinti vartotojai** į **Taikomosios programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="dc318-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Rodinio keitimas iš „Įgalinti vartotojai” į „Taikomosios programos vartotojai”](media/sales-map-enabled-users.png)

4. <span data-ttu-id="dc318-212">Pasirinkite du **DviguboRašymo VartotojoIntegravimas** įrašus.</span><span class="sxs-lookup"><span data-stu-id="dc318-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Taikomosios programos vartotojų sąrašas](media/sales-map-user-mode.png)

5. <span data-ttu-id="dc318-214">Pakeiskite **Integravimo vartotojo režimo** lauko reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dc318-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Integravimo vartotojo režimo lauko reikšmės pakeitimas](media/sales-map-user-mode-yes.png)

<span data-ttu-id="dc318-216">Dabar Jūsų pardavimo užsakymai yra susieti.</span><span class="sxs-lookup"><span data-stu-id="dc318-216">Your sales orders are now mapped.</span></span>
