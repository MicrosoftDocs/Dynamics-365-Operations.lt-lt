---
title: Finansinių ataskaitų dizaino įrankio ataskaitų aprašai
description: Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus. Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848346"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="77d19-105">Finansinių ataskaitų dizaino įrankio ataskaitų aprašai</span><span class="sxs-lookup"><span data-stu-id="77d19-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77d19-106">Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus.</span><span class="sxs-lookup"><span data-stu-id="77d19-106">This article provides information about report definitions.</span></span> <span data-ttu-id="77d19-107">Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas.</span><span class="sxs-lookup"><span data-stu-id="77d19-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="77d19-108">Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="77d19-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="77d19-109">Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas.</span><span class="sxs-lookup"><span data-stu-id="77d19-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="77d19-110">Ataskaitos apibrėžtis taip pat teikia papildomų parinkčių ir nuostatų, kuriuos naudodami galite tinkinti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="77d19-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="77d19-111">Apibrėžę eilučių aprašus ir stulpelių aprašus, turite juos sujungti į ataskaitos aprašą.</span><span class="sxs-lookup"><span data-stu-id="77d19-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="77d19-112">Šiuo metu taip pat nustatomi kiti aprašų aspektai, pavyzdžiui, išsamumo lygis ir ataskaitos data.</span><span class="sxs-lookup"><span data-stu-id="77d19-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="77d19-113">Tada galite įrašyti ir generuoti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="77d19-113">You can then save and generate a report.</span></span> <span data-ttu-id="77d19-114">Finansinės ataskaitos siūlo tokius išsamumo lygius.</span><span class="sxs-lookup"><span data-stu-id="77d19-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="77d19-115">Finansinis</span><span class="sxs-lookup"><span data-stu-id="77d19-115">Financial</span></span>
- <span data-ttu-id="77d19-116">Finansinis ir Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="77d19-116">Financial and Account</span></span>
- <span data-ttu-id="77d19-117">Finansinis, Sąskaitos ir Operacijos</span><span class="sxs-lookup"><span data-stu-id="77d19-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="77d19-118">Tačiau atsižvelgiant į tai, kaip duomenys saugomi sistemoje „Microsoft Dynamics ERP“, ataskaitose gali nebūti operacijos informacijos.</span><span class="sxs-lookup"><span data-stu-id="77d19-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="77d19-119">Ataskaitos aprašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="77d19-119">Create a report definition</span></span>
1. <span data-ttu-id="77d19-120">Ataskaitų konstruktoriuje, meniu **Failas**, spustelėkite **Naujas**, ir tada pasirinkite **Ataskaitos aprašas**.</span><span class="sxs-lookup"><span data-stu-id="77d19-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="77d19-121">Nurodyti atitinkamą informaciją skirtukuose **Ataskaita**, **Išeiga ir paskirstymas**, **Antraštės ir poraštės** ir **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="77d19-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="77d19-122">Ataskaitos aprašo turinys</span><span class="sxs-lookup"><span data-stu-id="77d19-122">Contents of a report definition</span></span>
<span data-ttu-id="77d19-123">Toliau pateikiamoje lentelėje aprašomi ataskaitos aprašo skirtukai ir kaip naudojama informacija.</span><span class="sxs-lookup"><span data-stu-id="77d19-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="77d19-124">Tabuliavimo ženklas</span><span class="sxs-lookup"><span data-stu-id="77d19-124">Tab</span></span></th>
<th><span data-ttu-id="77d19-125">Aprašas</span><span class="sxs-lookup"><span data-stu-id="77d19-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="77d19-126">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="77d19-126">Report</span></span></td>
<td><span data-ttu-id="77d19-127">Ataskaitos kūrimas, konfigūravimas arba esamos ataskaitos modifikavimas.</span><span class="sxs-lookup"><span data-stu-id="77d19-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77d19-128">Išeiga ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="77d19-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="77d19-129">Pakeiskite ataskaitos išeigos tipą ir paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="77d19-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77d19-130">Antraštės ir poraštės</span><span class="sxs-lookup"><span data-stu-id="77d19-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="77d19-131">Apibrėžkite ir suformatuokite ataskaitos antraštes ir poraštes.</span><span class="sxs-lookup"><span data-stu-id="77d19-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="77d19-132">Pavyzdžiui, galite pridėti prie antraštės arba poraštės teksto arba vaizdų.</span><span class="sxs-lookup"><span data-stu-id="77d19-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="77d19-133">Finansinės ataskaitos palaiko .bmp, .jpg ir .png vaizdų failus.</span><span class="sxs-lookup"><span data-stu-id="77d19-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="77d19-134">Taip pat galite pridėti automatinio teksto kodų kitai informacijai įterpti pavyzdžiui, įmonės pavadinimą, ataskaitos pavadinimą arba puslapio numerį.</span><span class="sxs-lookup"><span data-stu-id="77d19-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="77d19-135">Parametrai</span><span class="sxs-lookup"><span data-stu-id="77d19-135">Settings</span></span></td>
<td><span data-ttu-id="77d19-136">Nurodykite ataskaitos aprašo parametrus, pavyzdžiui, šiuos parametrus.</span><span class="sxs-lookup"><span data-stu-id="77d19-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="77d19-137">Formatavimas ir sumos apvalinimas</span><span class="sxs-lookup"><span data-stu-id="77d19-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="77d19-138">Informacijos ataskaitų formatas</span><span class="sxs-lookup"><span data-stu-id="77d19-138">Format detail reports</span></span></li>
<li><span data-ttu-id="77d19-139">Ataskaitų medžių formatas</span><span class="sxs-lookup"><span data-stu-id="77d19-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="77d19-140">Išimčių ataskaitos generavimas</span><span class="sxs-lookup"><span data-stu-id="77d19-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="77d19-141">Valiutos konvertavimo nurodymas</span><span class="sxs-lookup"><span data-stu-id="77d19-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="77d19-142">Tarpinė suma ir sąskaitos informacijos filtravimas</span><span class="sxs-lookup"><span data-stu-id="77d19-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="77d19-143">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="77d19-143">Additional resources</span></span>

[<span data-ttu-id="77d19-144">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="77d19-144">Financial reporting</span></span>](financial-reporting-intro.md)
