---
title: Konfigūruoti finansinių duomenų bendrinimą tarp įmonių
description: Šia procedūra rodoma, kaip konfigūruoti, įgalinti, patikrinti ir išspręsti konfliktus bendrinant duomenis tarp įmonių.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551035"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="b0896-103">Konfigūruoti finansinių duomenų bendrinimą tarp įmonių</span><span class="sxs-lookup"><span data-stu-id="b0896-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0896-104">Šia procedūra rodoma, kaip konfigūruoti, įgalinti, patikrinti ir išspręsti konfliktus bendrinant duomenis tarp įmonių.</span><span class="sxs-lookup"><span data-stu-id="b0896-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="b0896-105">Joje naudojama USMF įmonė ir finansinių duomenų bendrinimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="b0896-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="b0896-106">Norint atlikti šį užduoties vediklį, reikia AX platformos 7.1 arba naujesnės versijos.</span><span class="sxs-lookup"><span data-stu-id="b0896-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="b0896-107">Pasirinkite Sistemos administravimas > Darbo sritys > Duomenų valdymas.</span><span class="sxs-lookup"><span data-stu-id="b0896-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="b0896-108">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="b0896-108">Click Import.</span></span>
3. <span data-ttu-id="b0896-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0896-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b0896-110">Lauke Šaltinio duomenų formatas pasirinkite paketo tipą.</span><span class="sxs-lookup"><span data-stu-id="b0896-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="b0896-111">Spustelėkite Nusiųsti.</span><span class="sxs-lookup"><span data-stu-id="b0896-111">Click Upload.</span></span> <span data-ttu-id="b0896-112">Pereikite į finansinių duomenų bendrinimo šablono paketo failo vietą ir pasirinkite tą failą.</span><span class="sxs-lookup"><span data-stu-id="b0896-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="b0896-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b0896-113">Click Save.</span></span>
6. <span data-ttu-id="b0896-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b0896-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b0896-115">Pasirinkite ką tik sukurtą duomenų bendrinimo strategiją.</span><span class="sxs-lookup"><span data-stu-id="b0896-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="b0896-116">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="b0896-116">Click Import.</span></span>
8. <span data-ttu-id="b0896-117">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="b0896-117">Click Close.</span></span>
9. <span data-ttu-id="b0896-118">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-118">Refresh the page.</span></span>
10. <span data-ttu-id="b0896-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-119">Close the page.</span></span>
11. <span data-ttu-id="b0896-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-120">Close the page.</span></span>
12. <span data-ttu-id="b0896-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-121">Close the page.</span></span>
13. <span data-ttu-id="b0896-122">Pasirinkite Sistemos administravimas > Nustatymas > Konfigūruoti duomenų bendrinimą tarp įmonių.</span><span class="sxs-lookup"><span data-stu-id="b0896-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="b0896-123">Sąraše raskite ir pasirinkite Mokėjimo dienos.</span><span class="sxs-lookup"><span data-stu-id="b0896-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="b0896-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b0896-124">Click Add.</span></span>
16. <span data-ttu-id="b0896-125">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b0896-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="b0896-126">Lauke Įmonė įveskite„USSI‟.</span><span class="sxs-lookup"><span data-stu-id="b0896-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="b0896-127">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="b0896-127">Click Add.</span></span>
19. <span data-ttu-id="b0896-128">Lauke Įmonė įveskite„USMF‟.</span><span class="sxs-lookup"><span data-stu-id="b0896-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="b0896-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b0896-129">Click Save.</span></span>
21. <span data-ttu-id="b0896-130">Spustelėkite Įgalinti.</span><span class="sxs-lookup"><span data-stu-id="b0896-130">Click Enable.</span></span>
22. <span data-ttu-id="b0896-131">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b0896-131">Click Yes.</span></span>
23. <span data-ttu-id="b0896-132">Spustelėkite Ieškoti bendrinimo problemų.</span><span class="sxs-lookup"><span data-stu-id="b0896-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="b0896-133">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b0896-133">Click Yes.</span></span>
25. <span data-ttu-id="b0896-134">Spustelėkite Atnaujinti lauko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b0896-134">Click Update field value.</span></span>
26. <span data-ttu-id="b0896-135">Spustelėkite Naudoti reikšmę iš 1-osios įmonės.</span><span class="sxs-lookup"><span data-stu-id="b0896-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="b0896-136">Atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-136">Refresh the page.</span></span>
28. <span data-ttu-id="b0896-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b0896-137">Close the page.</span></span>

