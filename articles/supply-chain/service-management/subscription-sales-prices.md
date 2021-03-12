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
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974226"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="6c64c-103">Prenumeratos pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="6c64c-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6c64c-104">Kai kuriate abonementą, pardavimo kainą gaunate iš pardavimo kainos nustatymo, sukurto formoje **Pardavimo kaina (abonementas)**.</span><span class="sxs-lookup"><span data-stu-id="6c64c-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="6c64c-105">Formoje **Pardavimo kaina (abonementas)** galite sukurti pardavimo kainas, skirtas tam tikriems abonementams, arba galite sukurti pardavimo kainas, kurios taikomos plačiau.</span><span class="sxs-lookup"><span data-stu-id="6c64c-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="6c64c-106">Pardavimo kainos, kuri turi būti taikoma abonementui, atveju, laikotarpio kodas bei abonemento valiuta turi būti identiški laikotarpio kodui ir pardavimo kainos valiutai.</span><span class="sxs-lookup"><span data-stu-id="6c64c-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="6c64c-107">Jei abonemento ir pardavimo kainos laikotarpio kodas ir valiuta yra identiški, abonemento pardavimo kainos pasirenkamos remiantis prioritetais, kurie nurodyti toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="6c64c-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="6c64c-108">Tuščias lentelės langelis reiškią tuščią lauką, o X reiškia vertę, kuri lygi vertei, esančiai abonemente, iš kurio sukuriama operacija.</span><span class="sxs-lookup"><span data-stu-id="6c64c-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="6c64c-109">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="6c64c-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="6c64c-110"><strong>Kategorija</strong></span><span class="sxs-lookup"><span data-stu-id="6c64c-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="6c64c-111"><strong>Projekto ID</strong></span><span class="sxs-lookup"><span data-stu-id="6c64c-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="6c64c-112"><strong>Abonementas</strong></span><span class="sxs-lookup"><span data-stu-id="6c64c-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="6c64c-113"><strong>Pardavimo valiuta</strong></span><span class="sxs-lookup"><span data-stu-id="6c64c-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="6c64c-114"><strong>Laikotarpio kodas</strong></span><span class="sxs-lookup"><span data-stu-id="6c64c-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-115">1</span><span class="sxs-lookup"><span data-stu-id="6c64c-115">1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-116">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-116">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-117">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-117">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-118">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-118">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-119">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-119">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-120">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-121">2</span><span class="sxs-lookup"><span data-stu-id="6c64c-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-122">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-122">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-123">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-123">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-124">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-124">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-125">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-126">3</span><span class="sxs-lookup"><span data-stu-id="6c64c-126">3</span></span></p></td>
<td><p><span data-ttu-id="6c64c-127">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-128">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-128">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-129">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-129">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-130">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-131">4</span><span class="sxs-lookup"><span data-stu-id="6c64c-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-132">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-132">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-133">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-133">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-134">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-135">5</span><span class="sxs-lookup"><span data-stu-id="6c64c-135">5</span></span></p></td>
<td><p><span data-ttu-id="6c64c-136">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-136">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-137">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-138">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-138">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-139">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-140">6</span><span class="sxs-lookup"><span data-stu-id="6c64c-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-141">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-142">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-142">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-143">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-144">7</span><span class="sxs-lookup"><span data-stu-id="6c64c-144">7</span></span></p></td>
<td><p><span data-ttu-id="6c64c-145">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-146">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-146">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-147">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-148">8</span><span class="sxs-lookup"><span data-stu-id="6c64c-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="6c64c-149">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-149">X</span></span></p></td>
<td><p><span data-ttu-id="6c64c-150">X</span><span class="sxs-lookup"><span data-stu-id="6c64c-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-151">Kai sukuriamas abonemento mokestis, pardavimo kaina, kuri yra išsamiausia (kaip parodyta anksčiau pateiktoje lentelėje), pažymima kaip abonemento pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="6c64c-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="6c64c-152">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="6c64c-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="6c64c-153">Abonemento pardavimo kainą galite atnaujinti atnaujindami bazinę kainą arba indeksą.</span><span class="sxs-lookup"><span data-stu-id="6c64c-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="6c64c-154">Galite naujinti tam pagal tam tikrą procentinę dalį arba pagal naują vertę.</span><span class="sxs-lookup"><span data-stu-id="6c64c-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="6c64c-155">Abonemento mokesčio pardavimo kainos</span><span class="sxs-lookup"><span data-stu-id="6c64c-155">Subscription fee sales prices</span></span>

<span data-ttu-id="6c64c-156">Kai sukuriate abonemento mokestį, pardavimo kaina yra pagrįsta tam abonementui nustatyta pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="6c64c-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="6c64c-157">Galite arba naudoti bazinę kainą iš abonemento kainų nustatymo, arba sukurti indeksuotas pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="6c64c-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="6c64c-158">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6c64c-158">Example</span></span>

<span data-ttu-id="6c64c-159">Jūs norite nustatyti naujam projektui 9030 nustatyti 500 eurų abonemento pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="6c64c-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="6c64c-160">Formoje **Pardavimo kaina (abonementas)**, kaip nurodyta toliau pateiktoje lentelėje, galite sukurti abonemento pardavimo kainos eilutę.</span><span class="sxs-lookup"><span data-stu-id="6c64c-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="6c64c-161">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="6c64c-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c64c-162">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6c64c-162">Category</span></span></p></th>
<th><p><span data-ttu-id="6c64c-163">Project</span><span class="sxs-lookup"><span data-stu-id="6c64c-163">Project</span></span></p></th>
<th><p><span data-ttu-id="6c64c-164">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="6c64c-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c64c-165">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="6c64c-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c64c-166">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="6c64c-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c64c-167">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6c64c-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-168">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c64c-169">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c64c-170">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="6c64c-170">Month</span></span></p></td>
<td><p><span data-ttu-id="6c64c-171">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-172">500</span><span class="sxs-lookup"><span data-stu-id="6c64c-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-173">Įsidėmėkite, kad laukai **Kategorija** ir **Abonementas** yra tušti.</span><span class="sxs-lookup"><span data-stu-id="6c64c-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="6c64c-174">Tada sukurkite toliau nurodytus abonementus.</span><span class="sxs-lookup"><span data-stu-id="6c64c-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="6c64c-175">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="6c64c-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c64c-176">Project</span><span class="sxs-lookup"><span data-stu-id="6c64c-176">Project</span></span></p></th>
<th><p><span data-ttu-id="6c64c-177">Abonementų grupė</span><span class="sxs-lookup"><span data-stu-id="6c64c-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="6c64c-178">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6c64c-178">Category</span></span></p></th>
<th><p><span data-ttu-id="6c64c-179">Valiuta</span><span class="sxs-lookup"><span data-stu-id="6c64c-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c64c-180">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="6c64c-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-182">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-182">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="6c64c-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-184">SubKat1</span><span class="sxs-lookup"><span data-stu-id="6c64c-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-185">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-186">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="6c64c-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-188">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-188">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="6c64c-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-190">SubKat2</span><span class="sxs-lookup"><span data-stu-id="6c64c-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c64c-191">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-192">Mėnesinis</span><span class="sxs-lookup"><span data-stu-id="6c64c-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-193">Dabar galite sukurti abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1:</span><span class="sxs-lookup"><span data-stu-id="6c64c-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="6c64c-194">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo abonementai** \> **Abonementų grupės**.</span><span class="sxs-lookup"><span data-stu-id="6c64c-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="6c64c-195">Formoje **Abonementų grupės** spustelėkite **Funkcija** \> **Sukurti abonementinį mokestį**.</span><span class="sxs-lookup"><span data-stu-id="6c64c-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="6c64c-196">Formoje **sukurti abonementinį mokestį** įveskite atitinkamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="6c64c-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="6c64c-197">Daugiau informacijos ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="6c64c-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="6c64c-198">Abonementiniai mokesčiai, kurių pardavimo kaina lygi 500 EUR, sukuriami abiejuose abonementuose, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="6c64c-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c64c-199">Projekto data</span><span class="sxs-lookup"><span data-stu-id="6c64c-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-200">Aptarnavimo abonementas</span><span class="sxs-lookup"><span data-stu-id="6c64c-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="6c64c-201">Project</span><span class="sxs-lookup"><span data-stu-id="6c64c-201">Project</span></span></p></th>
<th><p><span data-ttu-id="6c64c-202">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6c64c-202">Category</span></span></p></th>
<th><p><span data-ttu-id="6c64c-203">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="6c64c-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-204">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="6c64c-204">End date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-205">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="6c64c-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c64c-206">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6c64c-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-207">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c64c-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-209">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-209">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-210">SubKat1</span><span class="sxs-lookup"><span data-stu-id="6c64c-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-211">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="6c64c-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-212">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="6c64c-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-213">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-214">500</span><span class="sxs-lookup"><span data-stu-id="6c64c-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-215">2006 08 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="6c64c-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-217">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-217">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-218">SubKat2</span><span class="sxs-lookup"><span data-stu-id="6c64c-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c64c-219">2007 01 01</span><span class="sxs-lookup"><span data-stu-id="6c64c-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-220">2007 03 31</span><span class="sxs-lookup"><span data-stu-id="6c64c-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-221">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-222">500</span><span class="sxs-lookup"><span data-stu-id="6c64c-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-223">Vėliau, jūs galite nuspręsti, kad norite nurodyti projekto 9030 SubKat1 kategorijos pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="6c64c-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="6c64c-224">Todėl jūs turite sukurti naują pardavimo kainų eilutę, kurioje būtų nurodyta 550 EUR pardavimo kaina, skirta projekto 9030 ir SubKat1 mokesčių kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="6c64c-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="6c64c-225">Dabar projekte 9030 pateiktos dvi abonemento pardavimo kainų eilutės, kaip parodyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="6c64c-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="6c64c-226">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="6c64c-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="6c64c-227">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6c64c-227">Category</span></span></p></th>
<th><p><span data-ttu-id="6c64c-228">Project</span><span class="sxs-lookup"><span data-stu-id="6c64c-228">Project</span></span></p></th>
<th><p><span data-ttu-id="6c64c-229">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="6c64c-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c64c-230">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="6c64c-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="6c64c-231">Valiuta</span><span class="sxs-lookup"><span data-stu-id="6c64c-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="6c64c-232">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6c64c-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-233">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c64c-234">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c64c-235">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="6c64c-235">Month</span></span></p></td>
<td><p><span data-ttu-id="6c64c-236">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-237">500</span><span class="sxs-lookup"><span data-stu-id="6c64c-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-238">2007 08 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-239">SubKat1</span><span class="sxs-lookup"><span data-stu-id="6c64c-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-240">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6c64c-241">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="6c64c-241">Month</span></span></p></td>
<td><p><span data-ttu-id="6c64c-242">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-243">550</span><span class="sxs-lookup"><span data-stu-id="6c64c-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-244">Pakartokite pirmiau aprašytą procedūrą, kad sukurtumėte abonemento mokesčius abiems abonementams, esantiems abonementų grupėje Sub1.</span><span class="sxs-lookup"><span data-stu-id="6c64c-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="6c64c-245">Toliau pateiktoje lentelėje nurodytos operacijos, kurios buvo sukurtos kiekvienam abonementui, susietam su abonementų grupe.</span><span class="sxs-lookup"><span data-stu-id="6c64c-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="6c64c-246">Projekto data</span><span class="sxs-lookup"><span data-stu-id="6c64c-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-247">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="6c64c-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6c64c-248">Project</span><span class="sxs-lookup"><span data-stu-id="6c64c-248">Project</span></span></p></th>
<th><p><span data-ttu-id="6c64c-249">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6c64c-249">Category</span></span></p></th>
<th><p><span data-ttu-id="6c64c-250">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="6c64c-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-251">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="6c64c-251">End date</span></span></p></th>
<th><p><span data-ttu-id="6c64c-252">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="6c64c-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6c64c-253">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6c64c-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c64c-254">2007 07 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="6c64c-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-256">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-256">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-257">SubKat1</span><span class="sxs-lookup"><span data-stu-id="6c64c-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="6c64c-258">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="6c64c-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c64c-259">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="6c64c-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c64c-260">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-261">550</span><span class="sxs-lookup"><span data-stu-id="6c64c-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c64c-262">2008 07 28</span><span class="sxs-lookup"><span data-stu-id="6c64c-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="6c64c-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="6c64c-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="6c64c-264">9030</span><span class="sxs-lookup"><span data-stu-id="6c64c-264">9030</span></span></p></td>
<td><p><span data-ttu-id="6c64c-265">SubKat2</span><span class="sxs-lookup"><span data-stu-id="6c64c-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6c64c-266">2008 01 01</span><span class="sxs-lookup"><span data-stu-id="6c64c-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="6c64c-267">2008 03 31</span><span class="sxs-lookup"><span data-stu-id="6c64c-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="6c64c-268">EUR</span><span class="sxs-lookup"><span data-stu-id="6c64c-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="6c64c-269">500</span><span class="sxs-lookup"><span data-stu-id="6c64c-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6c64c-270">Pirmojoje 00020\_135 abonemento operacijoje 550 EUR pardavimo kaina gaunama iš abonemento pardavimo kainos, kuri nustatyta konkretaus projekto ir kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="6c64c-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="6c64c-271">Antrojoje 00021\_135 abonemento operacijoje 500 EUR pardavimo kaina naudojama kaip projekto abonemento pardavimo kaina, kadangi nėra nustatytos kainos 9030 projekto ir SubKat2 kategorijos kombinacijai.</span><span class="sxs-lookup"><span data-stu-id="6c64c-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c64c-272">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6c64c-272">See also</span></span>

[<span data-ttu-id="6c64c-273">Abonemento pardavimo kainų naujinimas ir indeksavimas</span><span class="sxs-lookup"><span data-stu-id="6c64c-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


