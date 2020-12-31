---
title: Klientų skirstymo pagal terminus ataskaita
description: Ataskaita Klientų skirstymas pagal terminus nurodo iš klientų gautinus balansus, surūšiuotus pagal datos intervalą arba skirstymo pagal terminus laikotarpį.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/15/2020
ms.locfileid: "4446160"
---
# <a name="customer-aging-report"></a><span data-ttu-id="0dca3-103">Klientų skirstymo pagal terminus ataskaita</span><span class="sxs-lookup"><span data-stu-id="0dca3-103">Customer aging report</span></span> 

<span data-ttu-id="0dca3-104">Ataskaita **Klientų skirstymas pagal terminus** nurodo iš klientų gautinus balansus, surūšiuotus pagal datos intervalą arba skirstymo pagal terminus laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0dca3-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="0dca3-105">Kai generuojate šią ataskaitą, rodomi toliau pateikti numatytieji parametrai.</span><span class="sxs-lookup"><span data-stu-id="0dca3-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="0dca3-106">Šiuos parametrus galite naudoti norėdami filtruoti duomenis, kurie bus rodomi ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="0dca3-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="0dca3-107">Daugiau informacijos žr. [Mokėjimų priežiūros nustatymas](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="0dca3-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0dca3-108">Laukas</span><span class="sxs-lookup"><span data-stu-id="0dca3-108">Field</span></span></p></th>
<th><p><span data-ttu-id="0dca3-109">Aprašas</span><span class="sxs-lookup"><span data-stu-id="0dca3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-110"><strong>Atsiskaitymo klasifikacija</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-111">Pasirinkite vieną ar kelias atsiskaitymo klasifikacijas, kurias norite įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="0dca3-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="0dca3-112">**Pastaba:** šis valdiklis galimas tik tada, kai pasirinktas <STRONG>viešojo sektoriaus</STRONG> konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="0dca3-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-113"><strong>Įtraukti operacijų be atsiskaitymo klasifikacijos</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-114">Jei šis žymės langelis pasirinktas, ataskaitoje bus rodomos visos operacijos, neturinčios joms priskirtos atsiskaitymo klasifikacijos.</span><span class="sxs-lookup"><span data-stu-id="0dca3-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="0dca3-115">**Pastaba:** šis valdiklis galimas tik tada, kai pasirinktas <STRONG>viešojo sektoriaus</STRONG> konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="0dca3-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-116"><strong>Skirstymas pagal terminus nuo</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-117">Įveskite datą, naudojamą dabartiniame skirstymo pagal terminus rinkinyje.</span><span class="sxs-lookup"><span data-stu-id="0dca3-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-118"><strong>Balansas nuo</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-119">Įveskite datą, kurios klientų balansus norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="0dca3-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="0dca3-120">Ji dar vadinama operacijų galutine data.</span><span class="sxs-lookup"><span data-stu-id="0dca3-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-121"><strong>Pradžios data</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-122">Įveskite datą, patenkančią į pirmojo laikotarpio intervalą arba skirstymo pagal terminus intervalą, kuri bus įtraukta į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="0dca3-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-123"><strong>Kriterijai</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-124">Pasirinkite datos tipą, kuriuo remiantis bus kuriama ataskaita.</span><span class="sxs-lookup"><span data-stu-id="0dca3-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="0dca3-125"><strong>Operacijos data</strong> – operacijų registravimo data.</span><span class="sxs-lookup"><span data-stu-id="0dca3-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="0dca3-126">Pavyzdžiui, tai gali būti SF data, kuri yra termino skaičiavimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="0dca3-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="0dca3-127"><strong>Terminas</strong> – operacijų terminas, sukuriamas pagal mokėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="0dca3-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="0dca3-128"><strong>Dokumento data</strong> – vartotojo nurodyta dokumento data, pagal kurią skaičiuojamas terminas.</span><span class="sxs-lookup"><span data-stu-id="0dca3-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-129"><strong>Skirstymo pagal terminus laikotarpio apibrėžimas</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-130">Pasirinkite skirstymo pagal terminus laikotarpio apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="0dca3-130">Select an aging period definition.</span></span> <span data-ttu-id="0dca3-131">Laukas <strong>Intervalas</strong> nenaudojamas, jei pasirenkate skirstymo pagal terminus laikotarpio apibrėžimą.</span><span class="sxs-lookup"><span data-stu-id="0dca3-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="0dca3-132">Skirstymo pagal terminus laikotarpio apibrėžimų, kuriuose yra daugiau nei šeši skirstymo pagal terminus laikotarpiai, negalima naudoti spausdintoje ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="0dca3-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="0dca3-133">**Pastaba:** skirstymo pagal terminus laikotarpius galite nustatyti pyslapyje <STRONG>Skirstymo pagal terminus laikotarpio apibrėžimai</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0dca3-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-134"><strong>Spausdinti skirstymo pagal terminus laikotarpio apibrėžimą</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-135">Pasirinkite <strong>Taip</strong>, jei norite kiekvieno skirstymo pagal terminus laikotarpio stulpelio, esančio ataskaitoje, viršuje įterpti skirstymo pagal terminus laikotarpių apibrėžimus.</span><span class="sxs-lookup"><span data-stu-id="0dca3-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="0dca3-136">Pasirinkite <strong>Ne</strong>, norėdami spausdinti ataskaitą be stulpelių antraščių.</span><span class="sxs-lookup"><span data-stu-id="0dca3-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-137"><strong>Intervalas</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-138">Nurodykite laikotarpį, kuris bus naudojamas, įvedę kiekvieno laikotarpio dienos ar mėnesio vienetų skaičių.</span><span class="sxs-lookup"><span data-stu-id="0dca3-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="0dca3-139">Pvz., norėdami peržiūrėti skirstymo pagal terminus informaciją pagal savaitę, šiame lauke įveskite 7 ir pasirinkite <strong>Diena</strong> lauke <strong>Diena / mėnuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="0dca3-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="0dca3-140">**Pastaba:** jūsų šiame lauke įvesta informacija naudojama tik jei nesate pasirinkę skirstymo pagal terminus laikotarpio apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="0dca3-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="0dca3-141">Kitu atveju spausdinimo kryptis nurodoma skirstymo pagal terminus laikotarpio apibrėžime.</span><span class="sxs-lookup"><span data-stu-id="0dca3-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-142"><strong>Diena / mėnuo</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-143">Pasirinkite vienetą <strong>Diena</strong> arba <strong>Mėnuo</strong>, kuris bus naudojamas laikotarpiui apibrėžti, lauke <strong>Intervalas</strong>.</span><span class="sxs-lookup"><span data-stu-id="0dca3-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-144"><strong>Spausdinimo kryptis</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-145">Pasirinkite, kokių laikotarpių balansus skaičiuoti ir skirstymo pagal terminus ataskaitą spausdinti – buvusių ar būsimų.</span><span class="sxs-lookup"><span data-stu-id="0dca3-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="0dca3-146">Datos įvertinamos atsižvelgiant į datą, kuri pasirinkta lauke <strong>Balansas nuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="0dca3-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="0dca3-147">Pasirinkite <strong>Atgal</strong>, kad būtų rodoma buvusių laikotarpių informacija.</span><span class="sxs-lookup"><span data-stu-id="0dca3-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="0dca3-148">Pasirinkite <strong>Pirmyn</strong>, kad būtų rodoma būsimų laikotarpių informacija.</span><span class="sxs-lookup"><span data-stu-id="0dca3-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="0dca3-149">
  
<STRONG>Pastaba:</STRONG> jūsų šiame lauke įvesta informacija naudojama tik jei nesate pasirinkę skirstymo pagal terminus laikotarpio apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="0dca3-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-150"><strong>Išsamiai</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-151">Pasirinkite, kad būtų pateiktos operacijos, įtrauktos į ataskaitoje nurodytus balansus.</span><span class="sxs-lookup"><span data-stu-id="0dca3-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-152"><strong>Įtraukti sumas operacijos valiuta</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-153">Pasirinkite, kad būtų įtrauktos sumos operacijos valiuta ir sumos apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="0dca3-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="0dca3-154">Jei šis žymės langelis nepasirinktas, sumos ataskaitoje rodomos tik apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="0dca3-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-155"><strong>Neigiamas balansas</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-156">Pasirinkite, kad būtų įtrauktos kliento sąskaitos, kurių balansai yra neigiami.</span><span class="sxs-lookup"><span data-stu-id="0dca3-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dca3-157"><strong>Neįtraukti sąskaitų su nuliniu balansu</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-158">Pasirinkite, kad nebūtų įtrauktos kliento sąskaitos, kurių balansai yra nuliniai.</span><span class="sxs-lookup"><span data-stu-id="0dca3-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0dca3-159"><strong>Mokėjimo padėties nustatymas</strong></span><span class="sxs-lookup"><span data-stu-id="0dca3-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="0dca3-160">Pasirinkite, kad būtų rodomi nesudengti mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="0dca3-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="0dca3-161">Jie rodomi pirmame ataskaitos stulpelyje.</span><span class="sxs-lookup"><span data-stu-id="0dca3-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

