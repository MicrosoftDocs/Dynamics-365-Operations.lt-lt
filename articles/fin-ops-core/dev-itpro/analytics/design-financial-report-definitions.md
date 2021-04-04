---
title: Finansinių ataskaitų dizaino įrankio ataskaitų aprašai
description: Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 073df430892e01d4842b2af147b0ae2765b1c66a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570347"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="c4ab8-103">Finansinių ataskaitų dizaino įrankio ataskaitų aprašai</span><span class="sxs-lookup"><span data-stu-id="c4ab8-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4ab8-104">Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-104">This article provides information about report definitions.</span></span> <span data-ttu-id="c4ab8-105">Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="c4ab8-106">Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="c4ab8-107">Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="c4ab8-108">Ataskaitos apibrėžtis taip pat teikia papildomų parinkčių ir nuostatų, kuriuos naudodami galite tinkinti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="c4ab8-109">Apibrėžę eilučių aprašus ir stulpelių aprašus, turite juos sujungti į ataskaitos aprašą.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="c4ab8-110">Šiuo metu taip pat nustatomi kiti aprašų aspektai, pavyzdžiui, išsamumo lygis ir ataskaitos data.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="c4ab8-111">Tada galite įrašyti ir generuoti ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-111">You can then save and generate a report.</span></span> <span data-ttu-id="c4ab8-112">Finansinės ataskaitos siūlo tokius išsamumo lygius.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="c4ab8-113">Finansinis</span><span class="sxs-lookup"><span data-stu-id="c4ab8-113">Financial</span></span>
- <span data-ttu-id="c4ab8-114">Finansinis ir Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="c4ab8-114">Financial and Account</span></span>
- <span data-ttu-id="c4ab8-115">Finansinis, Sąskaitos ir Operacijos</span><span class="sxs-lookup"><span data-stu-id="c4ab8-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="c4ab8-116">Tačiau atsižvelgiant į tai, kaip duomenys saugomi sistemoje „Microsoft Dynamics ERP“, ataskaitose gali nebūti operacijos informacijos.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="c4ab8-117">Ataskaitos aprašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-117">Create a report definition</span></span>
1. <span data-ttu-id="c4ab8-118">Ataskaitų konstruktoriuje, meniu **Failas**, spustelėkite **Naujas**, ir tada pasirinkite **Ataskaitos aprašas**.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="c4ab8-119">Nurodyti atitinkamą informaciją skirtukuose **Ataskaita**, **Išeiga ir paskirstymas**, **Antraštės ir poraštės** ir **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="c4ab8-120">Ataskaitos aprašo turinys</span><span class="sxs-lookup"><span data-stu-id="c4ab8-120">Contents of a report definition</span></span>
<span data-ttu-id="c4ab8-121">Toliau pateikiamoje lentelėje aprašomi ataskaitos aprašo skirtukai ir kaip naudojama informacija.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c4ab8-122">Tabuliavimo ženklas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-122">Tab</span></span></th>
<th><span data-ttu-id="c4ab8-123">Aprašas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c4ab8-124">Ataskaita</span><span class="sxs-lookup"><span data-stu-id="c4ab8-124">Report</span></span></td>
<td><span data-ttu-id="c4ab8-125">Ataskaitos kūrimas, konfigūravimas arba esamos ataskaitos modifikavimas.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4ab8-126">Išeiga ir paskirstymas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="c4ab8-127">Pakeiskite ataskaitos išeigos tipą ir paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4ab8-128">Antraštės ir poraštės</span><span class="sxs-lookup"><span data-stu-id="c4ab8-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="c4ab8-129">Apibrėžkite ir suformatuokite ataskaitos antraštes ir poraštes.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="c4ab8-130">Pavyzdžiui, galite pridėti prie antraštės arba poraštės teksto arba vaizdų.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="c4ab8-131">Finansinės ataskaitos palaiko .bmp, .jpg ir .png vaizdų failus.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="c4ab8-132">Taip pat galite pridėti automatinio teksto kodų kitai informacijai įterpti pavyzdžiui, įmonės pavadinimą, ataskaitos pavadinimą arba puslapio numerį.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4ab8-133">Parametrai</span><span class="sxs-lookup"><span data-stu-id="c4ab8-133">Settings</span></span></td>
<td><span data-ttu-id="c4ab8-134">Nurodykite ataskaitos aprašo parametrus, pavyzdžiui, šiuos parametrus.</span><span class="sxs-lookup"><span data-stu-id="c4ab8-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="c4ab8-135">Formatavimas ir sumos apvalinimas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="c4ab8-136">Informacijos ataskaitų formatas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-136">Format detail reports</span></span></li>
<li><span data-ttu-id="c4ab8-137">Ataskaitų medžių formatas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="c4ab8-138">Išimčių ataskaitos generavimas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="c4ab8-139">Valiutos konvertavimo nurodymas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="c4ab8-140">Tarpinė suma ir sąskaitos informacijos filtravimas</span><span class="sxs-lookup"><span data-stu-id="c4ab8-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="c4ab8-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c4ab8-141">Additional resources</span></span>

[<span data-ttu-id="c4ab8-142">Finansinės ataskaitos</span><span class="sxs-lookup"><span data-stu-id="c4ab8-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]