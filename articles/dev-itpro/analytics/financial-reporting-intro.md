---
title: Finansinės ataskaitos
description: „Finance and Operations“ skirtos finansinės ataskaitos suteikia galimybę finansų ir verslo profesionalams kurti, tvarkyti, diegti ir peržiūrėti finansines ataskaitas. Jos nepaiso tradicinių ataskaitų teikimo apribojimų, todėl galite efektyviai kurti įvairių tipų ataskaitas.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae2087cf142fc2670bda3c542b336f12978178a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553908"
---
# <a name="financial-reporting"></a><span data-ttu-id="7d878-104">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="7d878-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d878-105">„Finance and Operations“ skirtos finansinės ataskaitos suteikia galimybę finansų ir verslo profesionalams kurti, tvarkyti, diegti ir peržiūrėti finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="7d878-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="7d878-106">Jos nepaiso tradicinių ataskaitų teikimo apribojimų, todėl galite efektyviai kurti įvairių tipų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="7d878-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="7d878-107">Finansinės ataskaitos palaiko dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7d878-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="7d878-108">Todėl sąskaitos segmentus arba dimensijas galima naudoti iš karto.</span><span class="sxs-lookup"><span data-stu-id="7d878-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="7d878-109">Nereikia jokių papildomų įrankių ar konfigūravimo veiksmų.</span><span class="sxs-lookup"><span data-stu-id="7d878-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="7d878-110">Finansinių ataskaitų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7d878-110">Financial reporting setup</span></span>
<span data-ttu-id="7d878-111">Puslapyje **Finansinių ataskaitų nustatymas** yra visų sistemos finansinių dimensijų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7d878-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="7d878-112">**Didžioji knyga** \> **Didžiosios knygos nustatymas** \> **Finansinių ataskaitų nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="7d878-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="7d878-113">Puslapyje **Finansinių ataskaitų nustatymas** yra du skyriai, kurie nustato duomenis, kuriuos pateikiate finansinėse ataskaitose:</span><span class="sxs-lookup"><span data-stu-id="7d878-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="7d878-114">**Skirtukas Dimensijos**. Kadangi skirtingos įmonės naudoja skirtingas dimensijas ir sąskaitų struktūras, neįmanoma nustatyti tvarkos, kuria vartotojai nori peržiūrėti visas ataskaitų finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7d878-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="7d878-115">Šis puslapis leidžia nustatyti tvarką, kuria norite matyti finansines dimensijas, kai kuriate ir peržiūrite ataskaitą srityje Finansinės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="7d878-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="7d878-116">**Skirtukas Atributai** yra vieta, kur galite pasirinkti, ar norite galimybės naudoti **Tiekėjai** ir **Klientai** kaip filtravimo ir ataskaitų kūrimo atributus.</span><span class="sxs-lookup"><span data-stu-id="7d878-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="7d878-117">Tiekėjo ir kliento ataskaitų kūrimas bus naudingas tik jei registruodami operacijas neįvedate kelių tiekėjų ar klientų viename kvite.</span><span class="sxs-lookup"><span data-stu-id="7d878-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="7d878-118">Tiekėjo ir (arba) kliento pasirinkimas padidins integravimo laiką.</span><span class="sxs-lookup"><span data-stu-id="7d878-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="7d878-119">Finansinių ataskaitų komponentai</span><span class="sxs-lookup"><span data-stu-id="7d878-119">Financial reporting components</span></span>
<span data-ttu-id="7d878-120">Šie finansinių ataskaitų komponentai padeda lengviau kurti, peržiūrėti ir planuoti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="7d878-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="7d878-121">Komponentas</span><span class="sxs-lookup"><span data-stu-id="7d878-121">Component</span></span>        | <span data-ttu-id="7d878-122">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="7d878-122">Functions</span></span> | <span data-ttu-id="7d878-123">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="7d878-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="7d878-124">Ataskaitos dizaino įrankis</span><span class="sxs-lookup"><span data-stu-id="7d878-124">Report Designer</span></span>  | <span data-ttu-id="7d878-125">Ataskaitų kūrimo blokų, kurie sujungiami, kad būtų galima apibrėžti ir generuoti ataskaitą, kūrimas.</span><span class="sxs-lookup"><span data-stu-id="7d878-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="7d878-126">Ataskaitos vedlys padės mažiau patyrusiems vartotojams atliekant projektavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="7d878-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="7d878-127">Patyrę vartotojai gali kurti naujus ataskaitų kūrimo blokus arba modifikuoti esamus kūrimo blokus, kad jie atitiktų jų poreikius.</span><span class="sxs-lookup"><span data-stu-id="7d878-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="7d878-128">Ataskaitų grafikai</span><span class="sxs-lookup"><span data-stu-id="7d878-128">Report schedules</span></span> | <span data-ttu-id="7d878-129">Suplanuoti vieną ataskaitą arba ataskaitų grupė, kad jos būtų generuojamos reguliariai.</span><span class="sxs-lookup"><span data-stu-id="7d878-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="7d878-130">Finansinės ataskaitos generavimas</span><span class="sxs-lookup"><span data-stu-id="7d878-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="7d878-131">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="7d878-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="7d878-132">Funkcija</span><span class="sxs-lookup"><span data-stu-id="7d878-132">Feature</span></span></th>
<th><span data-ttu-id="7d878-133">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7d878-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7d878-134">Ataskaitos dizaino lankstumas</span><span class="sxs-lookup"><span data-stu-id="7d878-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="7d878-135">Kai kuriate ataskaitą, galima naudoti tolesnes ataskaitų dizaino įrankio pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="7d878-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="7d878-136">Įrašyti dimensijų kombinacijas ir dimensijas naudoti kelioms ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="7d878-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="7d878-137">Valdyti, kaip formatuojami ir rodomi dimensijų aprašai.</span><span class="sxs-lookup"><span data-stu-id="7d878-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="7d878-138">Identifikuoti ataskaitų kūrimo blokuose praleistas sąskaitas arba dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7d878-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="7d878-139">Formatuoti besisukančių prognozių antraštes.</span><span class="sxs-lookup"><span data-stu-id="7d878-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7d878-140">Finansinės ataskaitos bendradarbiavimas</span><span class="sxs-lookup"><span data-stu-id="7d878-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="7d878-141">Naudodamiesi toliau nurodytomis funkcijomis galėsite lengviau kurti ir paskirstyti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="7d878-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="7d878-142">Suplanuoti, kad ataskaitos būtų automatiškai generuojamos kiekvieną dieną, kas savaitę, kas mėnesį arba kas metus.</span><span class="sxs-lookup"><span data-stu-id="7d878-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="7d878-143">Eksportuoti į tik skaitymui skirtą XPS formatą, kuris suteikia geresnę dokumento saugą, nes naudojami skatmeniniai parašai.</span><span class="sxs-lookup"><span data-stu-id="7d878-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="7d878-144">Eksportuoti į „Microsoft Excel“ darbalapį.</span><span class="sxs-lookup"><span data-stu-id="7d878-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="7d878-145">Norėdami bendrinti ataskaitas, galite sukurti el. pašto pranešimus, kuriuose yra nuorodos į ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="7d878-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="7d878-146">Interaktyvi ataskaitos peržiūra</span><span class="sxs-lookup"><span data-stu-id="7d878-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="7d878-147">Naudodamiesi interaktyvumo funkcijomis galite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="7d878-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="7d878-148">Pakeisti peržiūrimos ataskaitos datą.</span><span class="sxs-lookup"><span data-stu-id="7d878-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="7d878-149">Pakeisti peržiūrimos ataskaitos valiutą.</span><span class="sxs-lookup"><span data-stu-id="7d878-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="7d878-150">Peržiūrėti ataskaitos naudojant suvestinės rodinį arba išsamų rodinį.</span><span class="sxs-lookup"><span data-stu-id="7d878-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="7d878-151">Įtraukti dimensijų filtrus, siekiant ataskaitos turinį apriboti iki konkrečios dimensijos arba dimensijų derinio.</span><span class="sxs-lookup"><span data-stu-id="7d878-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="7d878-152">Įtraukti atributų filtrus, siekiant ataskaitos turinį apriboti iki konkretaus atributo arba atributų derinio.</span><span class="sxs-lookup"><span data-stu-id="7d878-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="7d878-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7d878-153">Additional resources</span></span>
[<span data-ttu-id="7d878-154">Finansinės ataskaitos generavimas</span><span class="sxs-lookup"><span data-stu-id="7d878-154">Generate a financial report</span></span>](generate-financial-report.md)
