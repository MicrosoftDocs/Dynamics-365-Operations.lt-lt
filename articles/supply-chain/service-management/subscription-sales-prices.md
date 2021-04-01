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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242306"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="96cff-103">Prenumeratos pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="96cff-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="96cff-104">Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje **Pardavimo kaina (abonementas)**.</span><span class="sxs-lookup"><span data-stu-id="96cff-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="96cff-105">Formoje **Pardavimo kaina (abonementas)** galite sukurti pardavimo kainas, skirtas tam tikriems abonementams, arba galite sukurti pardavimo kainas, kurios taikomos plačiau.</span><span class="sxs-lookup"><span data-stu-id="96cff-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="96cff-106">Pardavimo kainos, kuri turi būti taikoma abonementui, atveju, laikotarpio kodas bei abonemento valiuta turi būti identiški laikotarpio kodui ir pardavimo kainos valiutai.</span><span class="sxs-lookup"><span data-stu-id="96cff-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="96cff-107">Jei abonemento ir pardavimo kainos laikotarpio kodas ir valiuta yra identiški, abonemento pardavimo kainos pasirenkamos remiantis prioritetais, kurie nurodyti toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="96cff-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="96cff-108">Tuščias lentelės langelis reiškią tuščią lauką, o X reiškia vertę, kuri lygi vertei, esančiai abonemente, iš kurio sukuriama operacija.</span><span class="sxs-lookup"><span data-stu-id="96cff-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="96cff-109">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="96cff-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="96cff-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="96cff-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="96cff-111"><strong>Projekto ID</strong></span><span class="sxs-lookup"><span data-stu-id="96cff-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="96cff-112"><strong>Abonementas</strong></span><span class="sxs-lookup"><span data-stu-id="96cff-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="96cff-113"><strong>Pardavimo valiuta</strong></span><span class="sxs-lookup"><span data-stu-id="96cff-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="96cff-114"><strong>Laikotarpio kodas</strong></span><span class="sxs-lookup"><span data-stu-id="96cff-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-115">1</span><span class="sxs-lookup"><span data-stu-id="96cff-115">1</span></span></p></td>
<td><p><span data-ttu-id="96cff-116">X</span><span class="sxs-lookup"><span data-stu-id="96cff-116">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-117">X</span><span class="sxs-lookup"><span data-stu-id="96cff-117">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-118">X</span><span class="sxs-lookup"><span data-stu-id="96cff-118">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-119">X</span><span class="sxs-lookup"><span data-stu-id="96cff-119">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-120">X</span><span class="sxs-lookup"><span data-stu-id="96cff-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-121">2</span><span class="sxs-lookup"><span data-stu-id="96cff-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-122">X</span><span class="sxs-lookup"><span data-stu-id="96cff-122">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-123">X</span><span class="sxs-lookup"><span data-stu-id="96cff-123">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-124">X</span><span class="sxs-lookup"><span data-stu-id="96cff-124">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-125">X</span><span class="sxs-lookup"><span data-stu-id="96cff-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96cff-126">3</span><span class="sxs-lookup"><span data-stu-id="96cff-126">3</span></span></p></td>
<td><p><span data-ttu-id="96cff-127">X</span><span class="sxs-lookup"><span data-stu-id="96cff-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-128">X</span><span class="sxs-lookup"><span data-stu-id="96cff-128">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-129">X</span><span class="sxs-lookup"><span data-stu-id="96cff-129">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-130">X</span><span class="sxs-lookup"><span data-stu-id="96cff-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-131">4</span><span class="sxs-lookup"><span data-stu-id="96cff-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-132">X</span><span class="sxs-lookup"><span data-stu-id="96cff-132">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-133">X</span><span class="sxs-lookup"><span data-stu-id="96cff-133">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-134">X</span><span class="sxs-lookup"><span data-stu-id="96cff-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96cff-135">5</span><span class="sxs-lookup"><span data-stu-id="96cff-135">5</span></span></p></td>
<td><p><span data-ttu-id="96cff-136">X</span><span class="sxs-lookup"><span data-stu-id="96cff-136">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-137">X</span><span class="sxs-lookup"><span data-stu-id="96cff-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-138">X</span><span class="sxs-lookup"><span data-stu-id="96cff-138">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-139">X</span><span class="sxs-lookup"><span data-stu-id="96cff-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-140">6</span><span class="sxs-lookup"><span data-stu-id="96cff-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-141">X</span><span class="sxs-lookup"><span data-stu-id="96cff-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-142">X</span><span class="sxs-lookup"><span data-stu-id="96cff-142">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-143">X</span><span class="sxs-lookup"><span data-stu-id="96cff-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96cff-144">7</span><span class="sxs-lookup"><span data-stu-id="96cff-144">7</span></span></p></td>
<td><p><span data-ttu-id="96cff-145">X</span><span class="sxs-lookup"><span data-stu-id="96cff-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-146">X</span><span class="sxs-lookup"><span data-stu-id="96cff-146">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-147">X</span><span class="sxs-lookup"><span data-stu-id="96cff-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-148">8</span><span class="sxs-lookup"><span data-stu-id="96cff-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="96cff-149">X</span><span class="sxs-lookup"><span data-stu-id="96cff-149">X</span></span></p></td>
<td><p><span data-ttu-id="96cff-150">X</span><span class="sxs-lookup"><span data-stu-id="96cff-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-151">Kai sukuriamas abonemento mokestis, pardavimo kaina, kuri yra išsamiausia (kaip parodyta anksčiau pateiktoje lentelėje), pažymima kaip abonemento pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="96cff-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="96cff-152">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="96cff-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="96cff-153">Abonemento pardavimo kainą galite atnaujinti atnaujindami bazinę kainą arba indeksą.</span><span class="sxs-lookup"><span data-stu-id="96cff-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="96cff-154">Galite naujinti tam pagal tam tikrą procentinę dalį arba pagal naują vertę.</span><span class="sxs-lookup"><span data-stu-id="96cff-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="96cff-155">Abonemento mokesčio pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="96cff-155">Subscription fee sales prices</span></span>

<span data-ttu-id="96cff-156">Kai sukuriate abonemento mokestį, pardavimo kaina yra pagrįsta tam abonementui nustatyta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="96cff-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="96cff-157">Galite arba naudoti bazinę kainą iš abonemento kainų nustatymo, arba sukurti indeksuotas pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="96cff-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="96cff-158">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="96cff-158">Example</span></span>

<span data-ttu-id="96cff-159">Jūs norite nustatyti naujam projektui 9030 nustatyti 500 eurų abonemento pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="96cff-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="96cff-160">Formoje **Pardavimo kaina (abonementas)**, kaip nurodyta toliau pateiktoje lentelėje, galite sukurti abonemento pardavimo kainos eilutę.</span><span class="sxs-lookup"><span data-stu-id="96cff-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="96cff-161">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="96cff-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="96cff-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96cff-162">Category</span></span></p></th>
<th><p><span data-ttu-id="96cff-163">Project</span><span class="sxs-lookup"><span data-stu-id="96cff-163">Project</span></span></p></th>
<th><p><span data-ttu-id="96cff-164">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="96cff-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="96cff-165">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="96cff-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="96cff-166">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="96cff-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="96cff-167">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="96cff-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-168">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="96cff-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96cff-169">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96cff-170">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="96cff-170">Month</span></span></p></td>
<td><p><span data-ttu-id="96cff-171">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-172">500</span><span class="sxs-lookup"><span data-stu-id="96cff-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-173">Įsidėmėkite, kad laukai **Kategorija** ir **Abonementas** yra tušti.</span><span class="sxs-lookup"><span data-stu-id="96cff-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="96cff-174">Tada sukurkite toliau nurodytus abonementus.</span><span class="sxs-lookup"><span data-stu-id="96cff-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="96cff-175">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="96cff-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="96cff-176">Project</span><span class="sxs-lookup"><span data-stu-id="96cff-176">Project</span></span></p></th>
<th><p><span data-ttu-id="96cff-177">Abonementų grupė</span><span class="sxs-lookup"><span data-stu-id="96cff-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="96cff-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96cff-178">Category</span></span></p></th>
<th><p><span data-ttu-id="96cff-179">Valiuta</span><span class="sxs-lookup"><span data-stu-id="96cff-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="96cff-180">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="96cff-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="96cff-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-182">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-182">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="96cff-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="96cff-184">SubKat1</span><span class="sxs-lookup"><span data-stu-id="96cff-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="96cff-185">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-186">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="96cff-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="96cff-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-188">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-188">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="96cff-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="96cff-190">SubKat2</span><span class="sxs-lookup"><span data-stu-id="96cff-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="96cff-191">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-192">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="96cff-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-193">Dabar galite sukurti abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1:</span><span class="sxs-lookup"><span data-stu-id="96cff-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="96cff-194">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="96cff-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="96cff-195">Formoje **Abonementų grupės** spustelėkite **Funkcija** \> **Sukurti abonementinį mokestį**.</span><span class="sxs-lookup"><span data-stu-id="96cff-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="96cff-196">Formoje **sukurti abonementinį mokestį** įveskite atitinkamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="96cff-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="96cff-197">Daugiau informacijos ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="96cff-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="96cff-198">Abonementiniai mokesčiai, kurių pardavimo kaina lygi 500 EUR, sukuriami abiejuose abonementuose, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="96cff-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="96cff-199">Projekto data</span><span class="sxs-lookup"><span data-stu-id="96cff-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="96cff-200">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="96cff-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="96cff-201">Project</span><span class="sxs-lookup"><span data-stu-id="96cff-201">Project</span></span></p></th>
<th><p><span data-ttu-id="96cff-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96cff-202">Category</span></span></p></th>
<th><p><span data-ttu-id="96cff-203">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="96cff-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="96cff-204">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="96cff-204">End date</span></span></p></th>
<th><p><span data-ttu-id="96cff-205">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="96cff-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="96cff-206">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="96cff-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-207">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="96cff-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="96cff-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="96cff-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-209">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-209">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-210">SubKat1</span><span class="sxs-lookup"><span data-stu-id="96cff-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="96cff-211">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="96cff-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-212">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="96cff-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-213">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-214">500</span><span class="sxs-lookup"><span data-stu-id="96cff-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-215">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="96cff-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="96cff-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="96cff-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-217">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-217">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-218">SubKat2</span><span class="sxs-lookup"><span data-stu-id="96cff-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="96cff-219">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="96cff-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-220">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="96cff-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-221">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-222">500</span><span class="sxs-lookup"><span data-stu-id="96cff-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-223">Vėliau, jūs galite nuspręsti, kad norite nurodyti projekto 9030 SubKat1 kategorijos pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="96cff-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="96cff-224">Todėl jūs turite sukurti naują pardavimo kainų eilutę, kurioje būtų nurodyta 550 EUR pardavimo kaina, skirta projekto 9030 ir SubKat1 mokesčių kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="96cff-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="96cff-225">Dabar projekte 9030 pateiktos dvi abonemento pardavimo kainų eilutės, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="96cff-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="96cff-226">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="96cff-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="96cff-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96cff-227">Category</span></span></p></th>
<th><p><span data-ttu-id="96cff-228">Project</span><span class="sxs-lookup"><span data-stu-id="96cff-228">Project</span></span></p></th>
<th><p><span data-ttu-id="96cff-229">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="96cff-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="96cff-230">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="96cff-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="96cff-231">Valiuta</span><span class="sxs-lookup"><span data-stu-id="96cff-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="96cff-232">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="96cff-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-233">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="96cff-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96cff-234">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96cff-235">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="96cff-235">Month</span></span></p></td>
<td><p><span data-ttu-id="96cff-236">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-237">500</span><span class="sxs-lookup"><span data-stu-id="96cff-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-238">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="96cff-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-239">SubKat1</span><span class="sxs-lookup"><span data-stu-id="96cff-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="96cff-240">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="96cff-241">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="96cff-241">Month</span></span></p></td>
<td><p><span data-ttu-id="96cff-242">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-243">550</span><span class="sxs-lookup"><span data-stu-id="96cff-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-244">Pakartokite pirmiau aprašytą procedūrą, kad sukurtumėte abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1.</span><span class="sxs-lookup"><span data-stu-id="96cff-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="96cff-245">Toliau pateiktoje lentelėje nurodytos operacijos, kurios buvo sukurtos kiekvienam abonementui, susietam su abonementų grupe.</span><span class="sxs-lookup"><span data-stu-id="96cff-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="96cff-246">Projekto data</span><span class="sxs-lookup"><span data-stu-id="96cff-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="96cff-247">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="96cff-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="96cff-248">Project</span><span class="sxs-lookup"><span data-stu-id="96cff-248">Project</span></span></p></th>
<th><p><span data-ttu-id="96cff-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="96cff-249">Category</span></span></p></th>
<th><p><span data-ttu-id="96cff-250">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="96cff-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="96cff-251">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="96cff-251">End date</span></span></p></th>
<th><p><span data-ttu-id="96cff-252">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="96cff-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="96cff-253">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="96cff-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96cff-254">2007 07 28</span><span class="sxs-lookup"><span data-stu-id="96cff-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="96cff-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="96cff-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-256">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-256">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-257">SubKat1</span><span class="sxs-lookup"><span data-stu-id="96cff-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="96cff-258">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="96cff-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="96cff-259">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="96cff-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="96cff-260">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-261">550</span><span class="sxs-lookup"><span data-stu-id="96cff-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96cff-262">2008 07 28</span><span class="sxs-lookup"><span data-stu-id="96cff-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="96cff-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="96cff-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="96cff-264">9030</span><span class="sxs-lookup"><span data-stu-id="96cff-264">9030</span></span></p></td>
<td><p><span data-ttu-id="96cff-265">SubKat2</span><span class="sxs-lookup"><span data-stu-id="96cff-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="96cff-266">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="96cff-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="96cff-267">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="96cff-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="96cff-268">EUR</span><span class="sxs-lookup"><span data-stu-id="96cff-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="96cff-269">500</span><span class="sxs-lookup"><span data-stu-id="96cff-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="96cff-270">Pirmojoje 00020\_135 abonemento operacijoje 550 EUR pardavimo kaina gaunama iš abonemento pardavimo kainos, kuri nustatyta konkretaus projekto ir kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="96cff-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="96cff-271">Antrojoje 00021\_135 abonemento operacijoje 500 EUR pardavimo kaina naudojama kaip projekto abonemento pardavimo kaina, kadangi nėra nustatytos kainos 9030 projekto ir SubKat2 kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="96cff-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="96cff-272">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="96cff-272">See also</span></span>

[<span data-ttu-id="96cff-273">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="96cff-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]