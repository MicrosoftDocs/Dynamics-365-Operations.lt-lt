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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4455385"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="15666-103">Konvertavimo nustatymas pardavimo užsakymo būsenos laukams</span><span class="sxs-lookup"><span data-stu-id="15666-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15666-104">Laukai, kurie nurodo pardavimo užsakymo būseną, turi skirtingas išvardijimo vertes „Microsoft Dynamics 365 Supply Chain Management” ir „Dynamics 365 sales” programose.</span><span class="sxs-lookup"><span data-stu-id="15666-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="15666-105">Būtini papildomi nustatymai, norint konvertuoti šiuos laukus dvigubam rašymui.</span><span class="sxs-lookup"><span data-stu-id="15666-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="15666-106">„Supply Chain Management“ laukai</span><span class="sxs-lookup"><span data-stu-id="15666-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="15666-107">„Supply Chain Management“ du laukai perteikia pardavimo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="15666-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="15666-108">Laukai, kuriuos reikia susieti, yra **Būsena** ir **Dokumento būsena**.</span><span class="sxs-lookup"><span data-stu-id="15666-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="15666-109">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="15666-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="15666-110">Ši būsena rodoma užsakymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="15666-110">This status is shown on the order header.</span></span>

<span data-ttu-id="15666-111">**Būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="15666-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="15666-112">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-112">Open Order</span></span>
- <span data-ttu-id="15666-113">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-113">Delivered</span></span>
- <span data-ttu-id="15666-114">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-114">Invoiced</span></span>
- <span data-ttu-id="15666-115">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-115">Cancelled</span></span>

<span data-ttu-id="15666-116">**Dokumento būsenos** išvardijimas nurodo vėliausią dokumentą, sugeneruotą užsakymui.</span><span class="sxs-lookup"><span data-stu-id="15666-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="15666-117">Pavyzdžiui, jei užsakymas patvirtintas, šis dokumentas yra pardavimo užsakymo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="15666-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="15666-118">Jei pardavimo užsakymas yra dalinai išrašyta SF, o tada likusi eilutė patvirtinama, dokumento būsena lieka **SF**, nes vėliau vykstančiame procese SF sugeneruojama.</span><span class="sxs-lookup"><span data-stu-id="15666-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="15666-119">**Dokumento būsenos** išvardijimas turi šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="15666-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="15666-120">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="15666-120">Confirmation</span></span>
- <span data-ttu-id="15666-121">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="15666-121">Picking List</span></span>
- <span data-ttu-id="15666-122">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="15666-122">Packing Slip</span></span>
- <span data-ttu-id="15666-123">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15666-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="15666-124">Pardavimo laukai</span><span class="sxs-lookup"><span data-stu-id="15666-124">Fields in Sales</span></span>

<span data-ttu-id="15666-125">Pardavimuose du laukai nurodo užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="15666-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="15666-126">Laukai, kuriuos reikia konvertuoti, yra **Būsena** ir **Apdorojimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="15666-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="15666-127">**Būsenos** išvardijimas nurodo bendrąją užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="15666-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="15666-128">Jam būdingos šios reikšmės:</span><span class="sxs-lookup"><span data-stu-id="15666-128">It has the following values:</span></span>

- <span data-ttu-id="15666-129">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-129">Active</span></span>
- <span data-ttu-id="15666-130">Pateikta</span><span class="sxs-lookup"><span data-stu-id="15666-130">Submitted</span></span>
- <span data-ttu-id="15666-131">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="15666-131">Fulfilled</span></span>
- <span data-ttu-id="15666-132">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-132">Invoiced</span></span>
- <span data-ttu-id="15666-133">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-133">Cancelled</span></span>

<span data-ttu-id="15666-134">**Apdorojimo būsenos** išvardijimas buvo įvestas tam, kad būseną būtų galima tiksliau susieti su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="15666-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="15666-135">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="15666-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="15666-136">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="15666-136">Processing Status</span></span>   | <span data-ttu-id="15666-137">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="15666-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="15666-138">Dokumento būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="15666-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="15666-139">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-139">Active</span></span>              | <span data-ttu-id="15666-140">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-140">Open Order</span></span>                        | <span data-ttu-id="15666-141">None</span><span class="sxs-lookup"><span data-stu-id="15666-141">None</span></span>                                       |
| <span data-ttu-id="15666-142">Pritarta</span><span class="sxs-lookup"><span data-stu-id="15666-142">Confirmed</span></span>           | <span data-ttu-id="15666-143">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-143">Open Order</span></span>                        | <span data-ttu-id="15666-144">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="15666-144">Confirmation</span></span>                               |
| <span data-ttu-id="15666-145">Paimta</span><span class="sxs-lookup"><span data-stu-id="15666-145">Picked</span></span>              | <span data-ttu-id="15666-146">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-146">Open Order</span></span>                        | <span data-ttu-id="15666-147">Išrinkimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="15666-147">Picking List</span></span>                               |
| <span data-ttu-id="15666-148">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-148">Partially Delivered</span></span> | <span data-ttu-id="15666-149">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-149">Open Order</span></span>                        | <span data-ttu-id="15666-150">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="15666-150">Packing Slip</span></span>                               |
| <span data-ttu-id="15666-151">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-151">Delivered</span></span>           | <span data-ttu-id="15666-152">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-152">Delivered</span></span>                         | <span data-ttu-id="15666-153">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="15666-153">Packing Slip</span></span>                               |
| <span data-ttu-id="15666-154">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-154">Partially Invoiced</span></span>  | <span data-ttu-id="15666-155">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-155">Delivered</span></span>                         | <span data-ttu-id="15666-156">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15666-156">Invoice</span></span>                                    |
| <span data-ttu-id="15666-157">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-157">Invoiced</span></span>            | <span data-ttu-id="15666-158">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-158">Invoiced</span></span>                          | <span data-ttu-id="15666-159">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="15666-159">Invoice</span></span>                                    |
| <span data-ttu-id="15666-160">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-160">Cancelled</span></span>           | <span data-ttu-id="15666-161">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-161">Cancelled</span></span>                         | <span data-ttu-id="15666-162">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="15666-162">Not applicable</span></span>                             |

<span data-ttu-id="15666-163">Toliau pateikiamoje lentelėje rodomas **Apdorojimo būsenos** konvertavimas tarp pardavimų ir „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="15666-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="15666-164">Apdorojimo būsena</span><span class="sxs-lookup"><span data-stu-id="15666-164">Processing Status</span></span>   | <span data-ttu-id="15666-165">Būsena pardavimuose</span><span class="sxs-lookup"><span data-stu-id="15666-165">Status in Sales</span></span> | <span data-ttu-id="15666-166">Būsena „Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="15666-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="15666-167">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-167">Active</span></span>              | <span data-ttu-id="15666-168">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-168">Active</span></span>          | <span data-ttu-id="15666-169">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-169">Open Order</span></span>                        |
| <span data-ttu-id="15666-170">Pritarta</span><span class="sxs-lookup"><span data-stu-id="15666-170">Confirmed</span></span>           | <span data-ttu-id="15666-171">Pateikta</span><span class="sxs-lookup"><span data-stu-id="15666-171">Submitted</span></span>       | <span data-ttu-id="15666-172">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-172">Open Order</span></span>                        |
| <span data-ttu-id="15666-173">Paimta</span><span class="sxs-lookup"><span data-stu-id="15666-173">Picked</span></span>              | <span data-ttu-id="15666-174">Pateikta</span><span class="sxs-lookup"><span data-stu-id="15666-174">Submitted</span></span>       | <span data-ttu-id="15666-175">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-175">Open Order</span></span>                        |
| <span data-ttu-id="15666-176">Iš dalies pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-176">Partially Delivered</span></span> | <span data-ttu-id="15666-177">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-177">Active</span></span>          | <span data-ttu-id="15666-178">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-178">Open Order</span></span>                        |
| <span data-ttu-id="15666-179">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-179">Partially Invoiced</span></span>  | <span data-ttu-id="15666-180">Aktyvūs</span><span class="sxs-lookup"><span data-stu-id="15666-180">Active</span></span>          | <span data-ttu-id="15666-181">Atviras užsakymas</span><span class="sxs-lookup"><span data-stu-id="15666-181">Open Order</span></span>                        |
| <span data-ttu-id="15666-182">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-182">Partially Invoiced</span></span>  | <span data-ttu-id="15666-183">Įvykdyta</span><span class="sxs-lookup"><span data-stu-id="15666-183">Fulfilled</span></span>       | <span data-ttu-id="15666-184">Pristatyta</span><span class="sxs-lookup"><span data-stu-id="15666-184">Delivered</span></span>                         |
| <span data-ttu-id="15666-185">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-185">Invoiced</span></span>            | <span data-ttu-id="15666-186">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-186">Invoiced</span></span>        | <span data-ttu-id="15666-187">Išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="15666-187">Invoiced</span></span>                          |
| <span data-ttu-id="15666-188">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-188">Cancelled</span></span>           | <span data-ttu-id="15666-189">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-189">Cancelled</span></span>       | <span data-ttu-id="15666-190">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="15666-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="15666-191">Sąranka</span><span class="sxs-lookup"><span data-stu-id="15666-191">Setup</span></span>

<span data-ttu-id="15666-192">Norėdami nustatyti pardavimo užsakymo būsenos laukų konvertavimą, turite įgalinti **IsSOPIntegravimasĮjungtas** ir **isVartotojoIntegravimas** atributus.</span><span class="sxs-lookup"><span data-stu-id="15666-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="15666-193">Norėdami įgalinti **IsSOPIntegravimasĮjungtas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="15666-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="15666-194">Žiniatinklio naršyklėje eikite į `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span><span class="sxs-lookup"><span data-stu-id="15666-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="15666-195">Pakeiskite **\<test-name\>** savo įmonės saitu į pardavimus.</span><span class="sxs-lookup"><span data-stu-id="15666-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="15666-196">Atidarytame puslapyje suraskite **OrganizacijosID** ir atkreipkite dėmesį į vertę.</span><span class="sxs-lookup"><span data-stu-id="15666-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![Organizacijos ID radimas](media/sales-map-orgid.png)

3. <span data-ttu-id="15666-198">Dalyje Pardavimai atsidarykite naršyklės konsolę ir vykdykite šį scenarijų.</span><span class="sxs-lookup"><span data-stu-id="15666-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="15666-199">Naudokite **OrganizacijosID** vertę nuo 2 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="15666-199">Use the **organizationid** value from step 2.</span></span>

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

4. <span data-ttu-id="15666-201">Patikrinkite, ar **IsSOPIntegravimasĮjungtas** yra nustatytas kaip **teisingas**.</span><span class="sxs-lookup"><span data-stu-id="15666-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="15666-202">Naudokite URL, kurį nurodėte 1 veiksme, kad patikrintumėte vertę.</span><span class="sxs-lookup"><span data-stu-id="15666-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegravimasĮjungtas yra nustatytas kaip teisingas.](media/sales-map-integration-enabled.png)

<span data-ttu-id="15666-204">Norėdami įgalinti **isVartotojoIntegravimas** atributą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="15666-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="15666-205">Dalyje Pardavimai eikite į **Parametras \> Tinkinimas \> Tinkinti sistemą**, pasirinkite **Vartotojo objektas** ir tada atidarykite **Forma \> Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="15666-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![Vartotojo formos atidarymas](media/sales-map-user.png)

2. <span data-ttu-id="15666-207">Laukų naršyklėje suraskite **Integravimo vartotojo režimas** ir du kartus spustelėkite jį, kad įtrauktumėte į formą.</span><span class="sxs-lookup"><span data-stu-id="15666-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="15666-208">Įrašykite savo pakeitimą.</span><span class="sxs-lookup"><span data-stu-id="15666-208">Save your change.</span></span>

    ![Integravimo vartotojo režimo lauko įtraukimas į formą](media/sales-map-field-explorer.png)

3. <span data-ttu-id="15666-210">Dalyje Pardavimai eikite į **Parametras \> Sauga \> Vartotojai** ir pakeiskite rodinį iš **Įgalinti vartotojai** į **Taikomosios programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="15666-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![Rodinio keitimas iš „Įgalinti vartotojai” į „Taikomosios programos vartotojai”](media/sales-map-enabled-users.png)

4. <span data-ttu-id="15666-212">Pasirinkite du **DviguboRašymo VartotojoIntegravimas** įrašus.</span><span class="sxs-lookup"><span data-stu-id="15666-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![Taikomosios programos vartotojų sąrašas](media/sales-map-user-mode.png)

5. <span data-ttu-id="15666-214">Pakeiskite **Integravimo vartotojo režimo** lauko reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="15666-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![Integravimo vartotojo režimo lauko reikšmės pakeitimas](media/sales-map-user-mode-yes.png)

<span data-ttu-id="15666-216">Dabar Jūsų pardavimo užsakymai yra susieti.</span><span class="sxs-lookup"><span data-stu-id="15666-216">Your sales orders are now mapped.</span></span>
