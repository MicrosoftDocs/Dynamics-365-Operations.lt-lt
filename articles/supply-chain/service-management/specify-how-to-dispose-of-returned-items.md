---
title: Nustatymas, kaip išmesti grąžintas prekes
description: Nustatykite,, kaip išmesti grąžintas prekes.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6fcdfec083aeb9c58d63f6e03542758e4d07e4d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "325071"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="33a77-103">Nustatymas, kaip išmesti grąžintas prekes</span><span class="sxs-lookup"><span data-stu-id="33a77-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="33a77-104">Rengiant grąžinimo užsakymą būtina nurodyti grąžinimo priežasties kodą, taip nustatant, kodėl produktas grąžinamas.</span><span class="sxs-lookup"><span data-stu-id="33a77-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="33a77-105">Taip pat būtina nurodyti perdavimo kodą ir perdavimo veiksmą, taip nurodant, kokius veiksmus reikia atlikti su grąžinamu produktu.</span><span class="sxs-lookup"><span data-stu-id="33a77-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="33a77-106">Perdavimo kodas gali būti taikomas, kai kuriate grąžinimo užsakymą, registruojate prekės gavimą arba prekės gavimo važtaraščio atnaujinimą ir sulaikymo užsakymo pabaigą.</span><span class="sxs-lookup"><span data-stu-id="33a77-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="33a77-107">Galite nurodyti bet kuriuos perdavimo kodus, būtinus verslo procesams palaikyti.</span><span class="sxs-lookup"><span data-stu-id="33a77-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="33a77-108">Šioje lentelėje pateikti kodai, pagal kuriuos paprastai priskiriamas grąžinamos prekės perdavimas.</span><span class="sxs-lookup"><span data-stu-id="33a77-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33a77-109">Perdavimo tipas</span><span class="sxs-lookup"><span data-stu-id="33a77-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="33a77-110">Bendrasis kodas</span><span class="sxs-lookup"><span data-stu-id="33a77-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="33a77-111">Aprašas</span><span class="sxs-lookup"><span data-stu-id="33a77-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33a77-112">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="33a77-113">SC</span><span class="sxs-lookup"><span data-stu-id="33a77-113">SC</span></span></p></td>
<td><p><span data-ttu-id="33a77-114">Nurašyti / Sunaikinti</span><span class="sxs-lookup"><span data-stu-id="33a77-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-115">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="33a77-116">DC</span><span class="sxs-lookup"><span data-stu-id="33a77-116">DC</span></span></p></td>
<td><p><span data-ttu-id="33a77-117">Paaukoti labdarai</span><span class="sxs-lookup"><span data-stu-id="33a77-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-118">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="33a77-119">TD</span><span class="sxs-lookup"><span data-stu-id="33a77-119">TD</span></span></p></td>
<td><p><span data-ttu-id="33a77-120">Trečiosios šalies turto realizavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-121">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="33a77-122">SL</span><span class="sxs-lookup"><span data-stu-id="33a77-122">SL</span></span></p></td>
<td><p><span data-ttu-id="33a77-123">Turto išgelbėjimas</span><span class="sxs-lookup"><span data-stu-id="33a77-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-124">Likvidavimas</span><span class="sxs-lookup"><span data-stu-id="33a77-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="33a77-125">TS</span><span class="sxs-lookup"><span data-stu-id="33a77-125">TS</span></span></p></td>
<td><p><span data-ttu-id="33a77-126">Trečiosios šalies turto pardavimas (antrinė rinka)</span><span class="sxs-lookup"><span data-stu-id="33a77-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-127">Remontuoti / Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="33a77-128">RW</span><span class="sxs-lookup"><span data-stu-id="33a77-128">RW</span></span></p></td>
<td><p><span data-ttu-id="33a77-129">Perdirbti</span><span class="sxs-lookup"><span data-stu-id="33a77-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-130">Remontuoti / Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="33a77-131">RF</span><span class="sxs-lookup"><span data-stu-id="33a77-131">RF</span></span></p></td>
<td><p><span data-ttu-id="33a77-132">Perdaryti / Atnaujinti</span><span class="sxs-lookup"><span data-stu-id="33a77-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-133">Remontuoti / Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="33a77-134">MD</span><span class="sxs-lookup"><span data-stu-id="33a77-134">MD</span></span></p></td>
<td><p><span data-ttu-id="33a77-135">Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-136">Remontuoti / Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="33a77-137">RP</span><span class="sxs-lookup"><span data-stu-id="33a77-137">RP</span></span></p></td>
<td><p><span data-ttu-id="33a77-138">Remontas</span><span class="sxs-lookup"><span data-stu-id="33a77-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-139">Remontuoti / Modifikuoti</span><span class="sxs-lookup"><span data-stu-id="33a77-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="33a77-140">RV</span><span class="sxs-lookup"><span data-stu-id="33a77-140">RV</span></span></p></td>
<td><p><span data-ttu-id="33a77-141">Grąžinti tiekėjui</span><span class="sxs-lookup"><span data-stu-id="33a77-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-142">Kita</span><span class="sxs-lookup"><span data-stu-id="33a77-142">Other</span></span></p></td>
<td><p><span data-ttu-id="33a77-143">AI</span><span class="sxs-lookup"><span data-stu-id="33a77-143">AI</span></span></p></td>
<td><p><span data-ttu-id="33a77-144">Naudoti taip, kaip yra</span><span class="sxs-lookup"><span data-stu-id="33a77-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-145">Kita</span><span class="sxs-lookup"><span data-stu-id="33a77-145">Other</span></span></p></td>
<td><p><span data-ttu-id="33a77-146">RS</span><span class="sxs-lookup"><span data-stu-id="33a77-146">RS</span></span></p></td>
<td><p><span data-ttu-id="33a77-147">Perparduoti</span><span class="sxs-lookup"><span data-stu-id="33a77-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-148">Kita</span><span class="sxs-lookup"><span data-stu-id="33a77-148">Other</span></span></p></td>
<td><p><span data-ttu-id="33a77-149">EX</span><span class="sxs-lookup"><span data-stu-id="33a77-149">EX</span></span></p></td>
<td><p><span data-ttu-id="33a77-150">Keitimas</span><span class="sxs-lookup"><span data-stu-id="33a77-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-151">Kita</span><span class="sxs-lookup"><span data-stu-id="33a77-151">Other</span></span></p></td>
<td><p><span data-ttu-id="33a77-152">MS</span><span class="sxs-lookup"><span data-stu-id="33a77-152">MS</span></span></p></td>
<td><p><span data-ttu-id="33a77-153">Įvairios</span><span class="sxs-lookup"><span data-stu-id="33a77-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="33a77-154">Nurodydami kiekvieną perdavimo kodą turite pasirinkite perdavimo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="33a77-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="33a77-155">Perdavimo veiksmas apibrėžia su perdavimo kodu susietus fizinius ir finansinius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="33a77-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="33a77-156">Pvz., perdavimo veiksmas gali nurodyti, kokie fiziniai veiksmai turi būti atlikti su grąžinta preke, koks finansinis poveikis bus patirtas dėl grąžintos prekės, taip pat, ar prekę reikia pakeisti ir nusiųsti klientui.</span><span class="sxs-lookup"><span data-stu-id="33a77-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="33a77-157">Atsižvelgdami į verslo poreikius, galite nurodyti bet kokį perdavimo kodų skaičių, bet yra tik šeši galimi perdavimo veiksmai.</span><span class="sxs-lookup"><span data-stu-id="33a77-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="33a77-158">Šioje lentelėje pateikti perdavimo veiksmai ir jų aprašai.</span><span class="sxs-lookup"><span data-stu-id="33a77-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33a77-159">Perdavimo veiksmas</span><span class="sxs-lookup"><span data-stu-id="33a77-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="33a77-160">aprašymas</span><span class="sxs-lookup"><span data-stu-id="33a77-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33a77-161"><strong>Kreditas</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-162">Grąžinti prekę į atsargas ir suteikti klientui kreditą.</span><span class="sxs-lookup"><span data-stu-id="33a77-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-163"><strong>Tik kreditas</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-164">Suteikti klientui kreditą jam nereikalaujant ir nesitikint, kad prekė bus grąžinta.</span><span class="sxs-lookup"><span data-stu-id="33a77-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-165"><strong>Nurašyta</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-166">Nurašyti prekę į atliekas ir suteikti klientui kreditą.</span><span class="sxs-lookup"><span data-stu-id="33a77-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-167"><strong>Keitimas ir kreditas</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-168">Grąžinti prekę į atsargas, sukurti keitimo užsakymą ir suteikti klientui kreditą.</span><span class="sxs-lookup"><span data-stu-id="33a77-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33a77-169"><strong>Keitimas ir nurašymas</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-170">Nurašyti prekę į atliekas, sukurti keitimo užsakymą ir suteikti klientui kreditą.</span><span class="sxs-lookup"><span data-stu-id="33a77-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33a77-171"><strong>Grąžinti klientui</strong></span><span class="sxs-lookup"><span data-stu-id="33a77-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="33a77-172">Atmesti grąžintą prekę ir grąžinti ją klientui.</span><span class="sxs-lookup"><span data-stu-id="33a77-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="33a77-173">Pasirinkite sulaikymo užsakymo perdavimo kodą</span><span class="sxs-lookup"><span data-stu-id="33a77-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="33a77-174">Spustelėkite **Atsargų valdymas** \> **Periodinis** \> **Kokybės valdymas** \> **Sulaikymo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="33a77-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="33a77-175">Skirtuko **Apžvalga** lauke **Perdavimo kodas** pasirinkite jau egzistuojančio sulaikymo užsakymo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="33a77-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="33a77-176">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="33a77-176">See also</span></span>

<span data-ttu-id="33a77-177">[Sulaikymo užsakymas (forma)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="33a77-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="33a77-178">[Perdavimo kodai (forma)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="33a77-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


