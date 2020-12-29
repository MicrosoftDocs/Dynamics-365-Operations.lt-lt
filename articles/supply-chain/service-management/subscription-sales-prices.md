---
title: Prenumeratos pardavimo kainos
description: Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje Pardavimo kaina (abonementas).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433517"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="7ccff-103">Prenumeratos pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="7ccff-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7ccff-104">Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje **Pardavimo kaina (abonementas)**.</span><span class="sxs-lookup"><span data-stu-id="7ccff-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="7ccff-105">Formoje **Pardavimo kaina (abonementas)** galite sukurti pardavimo kainas, skirtas tam tikriems abonementams, arba galite sukurti pardavimo kainas, kurios taikomos plačiau.</span><span class="sxs-lookup"><span data-stu-id="7ccff-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="7ccff-106">Pardavimo kainos, kuri turi būti taikoma abonementui, atveju, laikotarpio kodas bei abonemento valiuta turi būti identiški laikotarpio kodui ir pardavimo kainos valiutai.</span><span class="sxs-lookup"><span data-stu-id="7ccff-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="7ccff-107">Jei abonemento ir pardavimo kainos laikotarpio kodas ir valiuta yra identiški, abonemento pardavimo kainos pasirenkamos remiantis prioritetais, kurie nurodyti toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7ccff-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="7ccff-108">Tuščias lentelės langelis reiškią tuščią lauką, o X reiškia vertę, kuri lygi vertei, esančiai abonemente, iš kurio sukuriama operacija.</span><span class="sxs-lookup"><span data-stu-id="7ccff-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-109">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="7ccff-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="7ccff-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="7ccff-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="7ccff-111"><strong>Projekto ID</strong></span><span class="sxs-lookup"><span data-stu-id="7ccff-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="7ccff-112"><strong>Abonementas</strong></span><span class="sxs-lookup"><span data-stu-id="7ccff-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="7ccff-113"><strong>Pardavimo valiuta</strong></span><span class="sxs-lookup"><span data-stu-id="7ccff-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="7ccff-114"><strong>Laikotarpio kodas</strong></span><span class="sxs-lookup"><span data-stu-id="7ccff-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-115">1</span><span class="sxs-lookup"><span data-stu-id="7ccff-115">1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-116">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-116">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-117">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-117">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-118">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-118">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-119">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-119">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-120">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-121">2</span><span class="sxs-lookup"><span data-stu-id="7ccff-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-122">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-122">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-123">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-123">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-124">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-124">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-125">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-126">3</span><span class="sxs-lookup"><span data-stu-id="7ccff-126">3</span></span></p></td>
<td><p><span data-ttu-id="7ccff-127">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-128">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-128">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-129">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-129">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-130">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-131">4</span><span class="sxs-lookup"><span data-stu-id="7ccff-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-132">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-132">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-133">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-133">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-134">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-135">5</span><span class="sxs-lookup"><span data-stu-id="7ccff-135">5</span></span></p></td>
<td><p><span data-ttu-id="7ccff-136">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-136">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-137">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-138">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-138">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-139">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-140">6</span><span class="sxs-lookup"><span data-stu-id="7ccff-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-141">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-142">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-142">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-143">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-144">7</span><span class="sxs-lookup"><span data-stu-id="7ccff-144">7</span></span></p></td>
<td><p><span data-ttu-id="7ccff-145">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-146">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-146">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-147">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-148">8</span><span class="sxs-lookup"><span data-stu-id="7ccff-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7ccff-149">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-149">X</span></span></p></td>
<td><p><span data-ttu-id="7ccff-150">X</span><span class="sxs-lookup"><span data-stu-id="7ccff-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-151">Kai sukuriamas abonemento mokestis, pardavimo kaina, kuri yra išsamiausia (kaip parodyta anksčiau pateiktoje lentelėje), pažymima kaip abonemento pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7ccff-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="7ccff-152">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="7ccff-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="7ccff-153">Abonemento pardavimo kainą galite atnaujinti atnaujindami bazinę kainą arba indeksą.</span><span class="sxs-lookup"><span data-stu-id="7ccff-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="7ccff-154">Galite naujinti tam pagal tam tikrą procentinę dalį arba pagal naują vertę.</span><span class="sxs-lookup"><span data-stu-id="7ccff-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="7ccff-155">Abonemento mokesčio pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="7ccff-155">Subscription fee sales prices</span></span>

<span data-ttu-id="7ccff-156">Kai sukuriate abonemento mokestį, pardavimo kaina yra pagrįsta tam abonementui nustatyta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7ccff-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="7ccff-157">Galite arba naudoti bazinę kainą iš abonemento kainų nustatymo, arba sukurti indeksuotas pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="7ccff-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="7ccff-158">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7ccff-158">Example</span></span>

<span data-ttu-id="7ccff-159">Jūs norite nustatyti naujam projektui 9030 nustatyti 500 eurų abonemento pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="7ccff-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="7ccff-160">Formoje **Pardavimo kaina (abonementas)**, kaip nurodyta toliau pateiktoje lentelėje, galite sukurti abonemento pardavimo kainos eilutę.</span><span class="sxs-lookup"><span data-stu-id="7ccff-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-161">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="7ccff-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="7ccff-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="7ccff-162">Category</span></span></p></th>
<th><p><span data-ttu-id="7ccff-163">Project</span><span class="sxs-lookup"><span data-stu-id="7ccff-163">Project</span></span></p></th>
<th><p><span data-ttu-id="7ccff-164">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="7ccff-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7ccff-165">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="7ccff-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="7ccff-166">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="7ccff-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7ccff-167">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="7ccff-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-168">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7ccff-169">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7ccff-170">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="7ccff-170">Month</span></span></p></td>
<td><p><span data-ttu-id="7ccff-171">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-172">500</span><span class="sxs-lookup"><span data-stu-id="7ccff-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-173">Įsidėmėkite, kad laukai **Kategorija** ir **Abonementas** yra tušti.</span><span class="sxs-lookup"><span data-stu-id="7ccff-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="7ccff-174">Tada sukurkite toliau nurodytus abonementus.</span><span class="sxs-lookup"><span data-stu-id="7ccff-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-175">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="7ccff-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="7ccff-176">Project</span><span class="sxs-lookup"><span data-stu-id="7ccff-176">Project</span></span></p></th>
<th><p><span data-ttu-id="7ccff-177">Abonementų grupė</span><span class="sxs-lookup"><span data-stu-id="7ccff-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="7ccff-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="7ccff-178">Category</span></span></p></th>
<th><p><span data-ttu-id="7ccff-179">Valiuta</span><span class="sxs-lookup"><span data-stu-id="7ccff-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="7ccff-180">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="7ccff-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-182">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-182">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="7ccff-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-184">SubKat1</span><span class="sxs-lookup"><span data-stu-id="7ccff-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-185">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-186">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="7ccff-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-188">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-188">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="7ccff-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-190">SubKat2</span><span class="sxs-lookup"><span data-stu-id="7ccff-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7ccff-191">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-192">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="7ccff-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-193">Dabar galite sukurti abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1:</span><span class="sxs-lookup"><span data-stu-id="7ccff-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="7ccff-194">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="7ccff-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="7ccff-195">Formoje **Abonementų grupės** spustelėkite **Funkcija** \> **Sukurti abonementinį mokestį**.</span><span class="sxs-lookup"><span data-stu-id="7ccff-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="7ccff-196">Formoje **sukurti abonementinį mokestį** įveskite atitinkamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="7ccff-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="7ccff-197">Daugiau informacijos ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="7ccff-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="7ccff-198">Abonementiniai mokesčiai, kurių pardavimo kaina lygi 500 EUR, sukuriami abiejuose abonementuose, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7ccff-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-199">Projekto data</span><span class="sxs-lookup"><span data-stu-id="7ccff-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-200">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="7ccff-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="7ccff-201">Project</span><span class="sxs-lookup"><span data-stu-id="7ccff-201">Project</span></span></p></th>
<th><p><span data-ttu-id="7ccff-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="7ccff-202">Category</span></span></p></th>
<th><p><span data-ttu-id="7ccff-203">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="7ccff-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-204">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="7ccff-204">End date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-205">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="7ccff-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7ccff-206">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="7ccff-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-207">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="7ccff-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-209">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-209">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-210">SubKat1</span><span class="sxs-lookup"><span data-stu-id="7ccff-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-211">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="7ccff-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-212">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="7ccff-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-213">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-214">500</span><span class="sxs-lookup"><span data-stu-id="7ccff-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-215">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="7ccff-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-217">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-217">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-218">SubKat2</span><span class="sxs-lookup"><span data-stu-id="7ccff-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7ccff-219">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="7ccff-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-220">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="7ccff-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-221">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-222">500</span><span class="sxs-lookup"><span data-stu-id="7ccff-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-223">Vėliau, jūs galite nuspręsti, kad norite nurodyti projekto 9030 SubKat1 kategorijos pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="7ccff-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="7ccff-224">Todėl jūs turite sukurti naują pardavimo kainų eilutę, kurioje būtų nurodyta 550 EUR pardavimo kaina, skirta projekto 9030 ir SubKat1 mokesčių kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="7ccff-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="7ccff-225">Dabar projekte 9030 pateiktos dvi abonemento pardavimo kainų eilutės, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7ccff-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-226">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="7ccff-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="7ccff-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="7ccff-227">Category</span></span></p></th>
<th><p><span data-ttu-id="7ccff-228">Project</span><span class="sxs-lookup"><span data-stu-id="7ccff-228">Project</span></span></p></th>
<th><p><span data-ttu-id="7ccff-229">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="7ccff-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7ccff-230">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="7ccff-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="7ccff-231">Valiuta</span><span class="sxs-lookup"><span data-stu-id="7ccff-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="7ccff-232">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="7ccff-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-233">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7ccff-234">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7ccff-235">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="7ccff-235">Month</span></span></p></td>
<td><p><span data-ttu-id="7ccff-236">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-237">500</span><span class="sxs-lookup"><span data-stu-id="7ccff-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-238">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-239">SubKat1</span><span class="sxs-lookup"><span data-stu-id="7ccff-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-240">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7ccff-241">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="7ccff-241">Month</span></span></p></td>
<td><p><span data-ttu-id="7ccff-242">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-243">550</span><span class="sxs-lookup"><span data-stu-id="7ccff-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-244">Pakartokite pirmiau aprašytą procedūrą, kad sukurtumėte abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1.</span><span class="sxs-lookup"><span data-stu-id="7ccff-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="7ccff-245">Toliau pateiktoje lentelėje nurodytos operacijos, kurios buvo sukurtos kiekvienam abonementui, susietam su abonementų grupe.</span><span class="sxs-lookup"><span data-stu-id="7ccff-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7ccff-246">Projekto data</span><span class="sxs-lookup"><span data-stu-id="7ccff-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-247">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="7ccff-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="7ccff-248">Project</span><span class="sxs-lookup"><span data-stu-id="7ccff-248">Project</span></span></p></th>
<th><p><span data-ttu-id="7ccff-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="7ccff-249">Category</span></span></p></th>
<th><p><span data-ttu-id="7ccff-250">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="7ccff-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-251">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="7ccff-251">End date</span></span></p></th>
<th><p><span data-ttu-id="7ccff-252">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="7ccff-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="7ccff-253">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="7ccff-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ccff-254">2007 07 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="7ccff-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-256">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-256">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-257">SubKat1</span><span class="sxs-lookup"><span data-stu-id="7ccff-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="7ccff-258">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="7ccff-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="7ccff-259">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="7ccff-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="7ccff-260">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-261">550</span><span class="sxs-lookup"><span data-stu-id="7ccff-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ccff-262">2008 07 28</span><span class="sxs-lookup"><span data-stu-id="7ccff-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="7ccff-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="7ccff-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="7ccff-264">9030</span><span class="sxs-lookup"><span data-stu-id="7ccff-264">9030</span></span></p></td>
<td><p><span data-ttu-id="7ccff-265">SubKat2</span><span class="sxs-lookup"><span data-stu-id="7ccff-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="7ccff-266">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="7ccff-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="7ccff-267">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="7ccff-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="7ccff-268">EUR</span><span class="sxs-lookup"><span data-stu-id="7ccff-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="7ccff-269">500</span><span class="sxs-lookup"><span data-stu-id="7ccff-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7ccff-270">Pirmojoje 00020\_135 abonemento operacijoje 550 EUR pardavimo kaina gaunama iš abonemento pardavimo kainos, kuri nustatyta konkretaus projekto ir kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="7ccff-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="7ccff-271">Antrojoje 00021\_135 abonemento operacijoje 500 EUR pardavimo kaina naudojama kaip projekto abonemento pardavimo kaina, kadangi nėra nustatytos kainos 9030 projekto ir SubKat2 kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="7ccff-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ccff-272">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="7ccff-272">See also</span></span>

[<span data-ttu-id="7ccff-273">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="7ccff-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


