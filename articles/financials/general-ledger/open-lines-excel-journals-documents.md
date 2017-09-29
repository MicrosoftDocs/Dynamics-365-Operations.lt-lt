---
title: "Žurnalo eilučių ir dokumentų publikavimas iš „Excel“"
description: "Šioje temoje aiškinama, kaip įvesti ir publikuoti bendrųjų žurnalų eilutes iš „Microsoft Excel“. Pateikiama informacija apie įvairius šablonus, kuriuos galite naudoti, priklausomai nuo įvedamų operacijų tipo."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e30b8d01dc398c91bb7ade7ebb48301ae2e9189
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="publish-journal-lines-and-documents-from-excel"></a><span data-ttu-id="60dea-104">Žurnalo eilučių ir dokumentų publikavimas iš „Excel“</span><span class="sxs-lookup"><span data-stu-id="60dea-104">Publish journal lines and documents from Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="60dea-105">Šioje temoje aiškinama, kaip įvesti ir publikuoti bendrųjų žurnalų eilutes iš „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="60dea-105">This topic explains how to enter and publish lines for general journals from Microsoft Excel.</span></span> <span data-ttu-id="60dea-106">Pateikiama informacija apie įvairius šablonus, kuriuos galite naudoti, priklausomai nuo įvedamų operacijų tipo.</span><span class="sxs-lookup"><span data-stu-id="60dea-106">It includes information about the various templates that you can use, depending on the type of transactions that you're entering.</span></span>

<span data-ttu-id="60dea-107">Vartotojai gali įvesti ir publikuoti finansinių žurnalų eilutes iš „Microsoft Excel“.</span><span class="sxs-lookup"><span data-stu-id="60dea-107">Users can enter and publish lines for financial journals from Microsoft Excel.</span></span> <span data-ttu-id="60dea-108">Vartotojui sukūrus žurnalą naudojant mygtuką **Atidaryti eilutes programoje „Excel“** rodomi galimi naudoti šablonai.</span><span class="sxs-lookup"><span data-stu-id="60dea-108">After a user creates a journal, the **Open lines in Excel** button displays the templates that are available.</span></span> <span data-ttu-id="60dea-109">Šablonai sukurti taip, kad palaikytų tam tikrus scenarijus, tačiau žurnale palaikomi ne visi sąskaitos tipo deriniai.</span><span class="sxs-lookup"><span data-stu-id="60dea-109">Templates are designed to support specific scenarios, however not every combination of account type is supported in the journal.</span></span> <span data-ttu-id="60dea-110">Šioje lentelėje rodomi galimi naudoti šablonai ir jų palaikomi sąskaitų tipai.</span><span class="sxs-lookup"><span data-stu-id="60dea-110">The following table shows the templates that are available and the account types which they support.</span></span>
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60dea-111">**Šablonas**</span><span class="sxs-lookup"><span data-stu-id="60dea-111">**Template**</span></span>             | <span data-ttu-id="60dea-112">**Palaikomi sąskaitų tipai**</span><span class="sxs-lookup"><span data-stu-id="60dea-112">**Supported account types**</span></span>                                                                                             | <span data-ttu-id="60dea-113">**Kaip prieiti prie šablono**</span><span class="sxs-lookup"><span data-stu-id="60dea-113">**How to access the template**</span></span>                                                          |
| <span data-ttu-id="60dea-114">Didžiosios knygos žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="60dea-114">Ledger journal lines</span></span>     | <span data-ttu-id="60dea-115">Sąskaita: didžioji knyga, klientas, tiekėjas, banko korespondentinė sąskaita: didžioji knyga, klientas, tiekėjas, banko vidinė įmonė palaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-115">Account: Ledger, Customer, Vendor, Bank Offset account: Ledger, Customer, Vendor, Bank Intercompany is supported.</span></span>       | <span data-ttu-id="60dea-116">Pagrindinis žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-116">General journal</span></span>                                                                         |
| <span data-ttu-id="60dea-117">SF registras</span><span class="sxs-lookup"><span data-stu-id="60dea-117">Invoice register</span></span>         | <span data-ttu-id="60dea-118">Sąskaita: tiekėjo korespondentinė sąskaita: didžiosios knygos vidinė įmonė nepalaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-118">Account: Vendor Offset account: Ledger Intercompany isn't supported.</span></span>                                                    | <span data-ttu-id="60dea-119">Mokėtinų sumų sąskaitos faktūros registras</span><span class="sxs-lookup"><span data-stu-id="60dea-119">AP invoice register</span></span>                                                                     |
| <span data-ttu-id="60dea-120">SF žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-120">Invoice journal</span></span>          | <span data-ttu-id="60dea-121">Sąskaitos: tiekėjo korespondentinė sąskaita: didžiosios knygos vidinė įmonė palaikomos.</span><span class="sxs-lookup"><span data-stu-id="60dea-121">Accounts: Vendor Offset account: Ledger Intercompany is supported.</span></span>                                                      | <span data-ttu-id="60dea-122">AP SF žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-122">AP invoice journal</span></span>                                                                      |
| <span data-ttu-id="60dea-123">Tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="60dea-123">Vendor invoice</span></span>           |                                                                                                                         | <span data-ttu-id="60dea-124">Tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="60dea-124">Vendor invoice</span></span>                                                                          |
| <span data-ttu-id="60dea-125">Kliento SF žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-125">Customer invoice journal</span></span> | <span data-ttu-id="60dea-126">Sąskaita: kliento korespondentinė sąskaita: didžiosios knygos vidinė įmonė palaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-126">Account: Customer Offset account: Ledger Intercompany is supported.</span></span>                                                     | <span data-ttu-id="60dea-127">Pagrindinis žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-127">General journal</span></span>                                                                         |
| <span data-ttu-id="60dea-128">Laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="60dea-128">Free text invoice</span></span>        |                                                                                                                         | <span data-ttu-id="60dea-129">Puslapyje **Laisvos formos SF** spustelėkite **Atidaryti naudojant „Excel“** („Microsoft Office“ piktograma).</span><span class="sxs-lookup"><span data-stu-id="60dea-129">On the **Free text invoice** page, click **Open in Excel** (the Microsoft Office icon).</span></span> |
| <span data-ttu-id="60dea-130">Ilgalaikio turto žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-130">Fixed assets journal</span></span>     | <span data-ttu-id="60dea-131">Priskirti turtą didžiajai knygai, bankui, klientui arba tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="60dea-131">Asset to ledger, bank, customer, or vendor.</span></span> <span data-ttu-id="60dea-132">Vidinė įmonė nepalaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-132">Intercompany isn't supported.</span></span>                                               | <span data-ttu-id="60dea-133">Ilgalaikio turto žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-133">Fixed asset journal</span></span>                                                                     |
| <span data-ttu-id="60dea-134">Tiekėjo mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-134">Vendor payment journal</span></span>   | <span data-ttu-id="60dea-135">Sąskaita: tiekėjo korespondentinė sąskaita: didžioji knyga, banko vidinė įmonė palaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-135">Account: Vendor Offset account: Ledger, Bank Intercompany is supported.</span></span>                                                 | <span data-ttu-id="60dea-136">Tiekėjo mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-136">Vendor payment journal</span></span>                                                                  |
| <span data-ttu-id="60dea-137">Kliento mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-137">Customer payment journal</span></span> | <span data-ttu-id="60dea-138">Sąskaita: kliento korespondentinė sąskaita: didžioji knyga, banko vidinė įmonė palaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-138">Account: Customer Offset account: Ledger, Bank Intercompany is supported.</span></span>                                               | <span data-ttu-id="60dea-139">Kliento mokėjimų žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-139">Customer payment journal</span></span>                                                                |
| <span data-ttu-id="60dea-140">Projekto išlaidų žurnalas</span><span class="sxs-lookup"><span data-stu-id="60dea-140">Project expense journal</span></span>  | <span data-ttu-id="60dea-141">Sąskaita: projektas, didžioji knyga, klientas, tiekėjo korespondentinė sąskaita: projektas, didžioji knyga, klientas, tiekėjo vidinė įmonė palaikoma.</span><span class="sxs-lookup"><span data-stu-id="60dea-141">Account: Project, Ledger, Customer, Vendor Offset account: Project, Ledger, Customer, Vendor Intercompany is supported.</span></span> | <span data-ttu-id="60dea-142">Bendrojo žurnalo išlaidos (dalyje Projekto valdymas ir apskaita)</span><span class="sxs-lookup"><span data-stu-id="60dea-142">General journal Expense (under Project management and accounting)</span></span>                       |

<span data-ttu-id="60dea-143">Kai eilutės publikuojamos, jos įvertinamos, kad būtų įsitikinama, ar jos atitinka finansiniuose žurnaluose nustatytas taisykles.</span><span class="sxs-lookup"><span data-stu-id="60dea-143">When the lines are published, they are validated to make sure that they comply with the rules that are set up in the financial journals.</span></span> <span data-ttu-id="60dea-144">Kai eilutės paskelbtos, vartotojai gali redaguoti arba registruoti kvitus iš „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“.</span><span class="sxs-lookup"><span data-stu-id="60dea-144">After the lines are published, users can edit or post the vouchers from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="60dea-145">Norint į šabloną įtraukti finansinių dimensijų, reikalingi papildomi pokyčiai.</span><span class="sxs-lookup"><span data-stu-id="60dea-145">To add financial dimensions to a template, additional changes are required.</span></span> <span data-ttu-id="60dea-146">Daugiau informacijos ieškokite [Dimensijų įtraukimas į „Microsoft Excel“ šabloną](/dynamics365/unified-operations/dev-itpro/financial/add-dimensions-excel-templates).</span><span class="sxs-lookup"><span data-stu-id="60dea-146">For additional information, see [Add dimensions to the Microsoft Excel template](/dynamics365/unified-operations/dev-itpro/financial/add-dimensions-excel-templates).</span></span> <span data-ttu-id="60dea-147">Kai dimensijos įtraukiamos į objektą, jas galima matyti naudojant „Excel“ kūrimo įrankį ir jas galima įtraukti į šabloną.</span><span class="sxs-lookup"><span data-stu-id="60dea-147">After dimensions are added to the entity, they are available in the Excel designer and can be added to the template.</span></span>





