---
title: Konfigūruoti vidinės įmonės projekto SF išrašymą
description: Šioje temoje rodoma, kaip nustatyti SF išrašymą tarp dviejų įmonių jūsų organizacijoje.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c89b17c09a4f145b5a4ca9cdd127b4e635447d4b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174448"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="2da62-103">Konfigūruoti vidinės įmonės projekto SF išrašymą</span><span class="sxs-lookup"><span data-stu-id="2da62-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2da62-104">Šioje temoje rodoma, kaip nustatyti SF išrašymą tarp dviejų įmonių jūsų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="2da62-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="2da62-105">Šioje užduotyje naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="2da62-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2da62-106">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Tiekėjai > Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="2da62-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="2da62-107">Sąraše **Visi tiekėjai** raskite ir pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2da62-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="2da62-108">Veiksmų srityje spustelėkite **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="2da62-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="2da62-109">Pažymėkite **Vidinė įmonė**.</span><span class="sxs-lookup"><span data-stu-id="2da62-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="2da62-110">Nustatykite **Aktyvus** kaip **Taip**, kad įjungtumėte vidinės įmonės prekybą.</span><span class="sxs-lookup"><span data-stu-id="2da62-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="2da62-111">Lauke **Kliento įmonė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="2da62-112">Lauke **Mano sąskaita** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="2da62-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2da62-113">Select **Save**.</span></span>
9. <span data-ttu-id="2da62-114">Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="2da62-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="2da62-115">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2da62-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="2da62-116">Pažymėkite skirtuką **Vidinė įmonė**.</span><span class="sxs-lookup"><span data-stu-id="2da62-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="2da62-117">Perkelkite slankiklį į **Taip**, kad įjungtumėte vidinės įmonės išteklių planavimą ir grafiką.</span><span class="sxs-lookup"><span data-stu-id="2da62-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="2da62-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2da62-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="2da62-119">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2da62-119">Select **New**.</span></span>
15. <span data-ttu-id="2da62-120">Lauke **Pasiskolinęs juridinis asmuo** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="2da62-121">Žymės langelyje pažymėkite **Sukauptos pajamos**.</span><span class="sxs-lookup"><span data-stu-id="2da62-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="2da62-122">Lauke **Numatytoji grafiko kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="2da62-123">Lauke **Numatytoji išlaidų kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="2da62-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2da62-124">Select **Save**.</span></span>
20. <span data-ttu-id="2da62-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2da62-125">Close the page.</span></span>
21. <span data-ttu-id="2da62-126">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Registravimas > Didžiosios knygos registravimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="2da62-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="2da62-127">Lauke **Didžiosios knygos sąskaitų tipai** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2da62-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="2da62-128">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2da62-128">Select **New**.</span></span>
24. <span data-ttu-id="2da62-129">Naujos eilutės lauke **Pagrindinė sąskaita** nurodykite pageidaujamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="2da62-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="2da62-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2da62-130">Select **Save**.</span></span>
26. <span data-ttu-id="2da62-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2da62-131">Close the page.</span></span>
27. <span data-ttu-id="2da62-132">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pervedimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="2da62-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="2da62-133">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2da62-133">Select **New**.</span></span>
29. <span data-ttu-id="2da62-134">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="2da62-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="2da62-135">Lauke **Pasiskolinęs juridinis asmuo** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2da62-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="2da62-136">Lauke **Pervedimo kainos modelis** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2da62-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="2da62-137">Lauke **Kainodara** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="2da62-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="2da62-138">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2da62-138">Select **Save**.</span></span>

