--- 
title: "Konfigūruoti vidinės įmonės projekto SF išrašymą"
description: "Šioje procedūroje parodoma, kaip nustatyti projekto SF tarp dviejų įmonių jūsų organizacijoje."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2018

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="dbfae-103">Konfigūruoti vidinės įmonės projekto SF išrašymą</span><span class="sxs-lookup"><span data-stu-id="dbfae-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbfae-104">Šioje procedūroje parodoma, kaip nustatyti projekto SF tarp dviejų įmonių jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="dbfae-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="dbfae-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="dbfae-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dbfae-106">Pasirinkite Mokėtinos sumos > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="dbfae-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="dbfae-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="dbfae-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dbfae-108">Veiksmų srityje spustelėkite „Bendra“.</span><span class="sxs-lookup"><span data-stu-id="dbfae-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="dbfae-109">Spustelėkite Vidinė įmonė.</span><span class="sxs-lookup"><span data-stu-id="dbfae-109">Click Intercompany.</span></span>
5. <span data-ttu-id="dbfae-110">Norėdami įgalinti vidinės įmonės prekybą, būseną Aktyvus nustatykite Taip.</span><span class="sxs-lookup"><span data-stu-id="dbfae-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="dbfae-111">Lauke Kliento įmonė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="dbfae-112">Lauke Mano sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="dbfae-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="dbfae-113">Click Save.</span></span>
9. <span data-ttu-id="dbfae-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-114">Close the page.</span></span>
10. <span data-ttu-id="dbfae-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-115">Close the page.</span></span>
11. <span data-ttu-id="dbfae-116">Eikite į Projektų valdymas ir apskaita > Nustatymas > Projektų valdymo ir apskaitos parametrai.</span><span class="sxs-lookup"><span data-stu-id="dbfae-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="dbfae-117">Spustelėkite skirtuką Vidinė įmonė.</span><span class="sxs-lookup"><span data-stu-id="dbfae-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="dbfae-118">Norėdami įgalinti vidinės įmonės išteklių planavimą ir tabelius, slankiklį perkelkite į Taip.</span><span class="sxs-lookup"><span data-stu-id="dbfae-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="dbfae-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="dbfae-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dbfae-120">Click New.</span></span>
16. <span data-ttu-id="dbfae-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="dbfae-122">Lauke Besiskolinantis juridinis subjektas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="dbfae-123">Pažymėkite žymės langelį Kaupti įplaukas.</span><span class="sxs-lookup"><span data-stu-id="dbfae-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="dbfae-124">Lauke Numatytoji grafiko kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="dbfae-125">Lauke Numatytoji išlaidų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="dbfae-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="dbfae-126">Click Save.</span></span>
22. <span data-ttu-id="dbfae-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-127">Close the page.</span></span>
23. <span data-ttu-id="dbfae-128">Eikite į Projektų valdymas ir apskaita > Nustatymas > Registravimas > Registravimo DK nustatymai.</span><span class="sxs-lookup"><span data-stu-id="dbfae-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="dbfae-129">Lauke DK sąskaitų tipai pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="dbfae-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dbfae-130">Click New.</span></span>
26. <span data-ttu-id="dbfae-131">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="dbfae-132">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="dbfae-133">Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="dbfae-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="dbfae-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="dbfae-134">Click Save.</span></span>
30. <span data-ttu-id="dbfae-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-135">Close the page.</span></span>
31. <span data-ttu-id="dbfae-136">Eikite į Projektų valdymas ir apskaita > Nustatymas > Kainos > Perkėlimo kaina.</span><span class="sxs-lookup"><span data-stu-id="dbfae-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="dbfae-137">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dbfae-137">Click New.</span></span>
33. <span data-ttu-id="dbfae-138">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="dbfae-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="dbfae-139">Lauke Besiskolinantis juridinis subjektas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dbfae-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="dbfae-140">Lauke Kainos perkėlimo modelis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="dbfae-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="dbfae-141">Lauke Kainos įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="dbfae-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="dbfae-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="dbfae-142">Click Save.</span></span>


