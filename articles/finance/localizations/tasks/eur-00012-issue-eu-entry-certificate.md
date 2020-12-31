---
title: EUR-00012 ES įrašo sertifikato išdavimas
description: Ši procedūra padės įgalinti ES įrašo sertifikatą, konfigūruoti kliento sąskaitą, kad būtų galima naudoti įrašų sertifikatus ir išduoti sertifikatą.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0091af30b917aab3b8c4572a72a20d8d2d5d52e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408209"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="4c7fc-103">EUR-00012 ES įrašo sertifikato išdavimas</span><span class="sxs-lookup"><span data-stu-id="4c7fc-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="4c7fc-104">Ši procedūra padės įgalinti ES įrašo sertifikatą, konfigūruoti kliento sąskaitą, kad būtų galima naudoti įrašų sertifikatus ir išduoti sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="4c7fc-105">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="4c7fc-106">Įgalinti įrašo sertifikato valdymo funkciją</span><span class="sxs-lookup"><span data-stu-id="4c7fc-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="4c7fc-107">Pasirinkite Gautinos sumos > Nustatymai > Gautinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="4c7fc-108">Spustelėkite skirtuką Siuntos.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="4c7fc-109">Išplėskite skyrių Įrašo sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="4c7fc-110">Lauke Įgalinti įrašo sertifikato valdymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="4c7fc-111">Lauke Įgalinti įrašo sertifikato išdavimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="4c7fc-112">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="4c7fc-113">Sąraše raskite ir pasirinkite Įrašo sertifikato eilutė.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="4c7fc-114">Lauke Numeracijos kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="4c7fc-115">Kliento nustatymas</span><span class="sxs-lookup"><span data-stu-id="4c7fc-115">Set up a customer</span></span>
1. <span data-ttu-id="4c7fc-116">Pasirinkite Gautinos sumos > Klientai > Visi klientai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="4c7fc-117">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4c7fc-118">Pvz., filtruokite lauką Sąskaita naudodami vertę „DE-015“.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="4c7fc-119">Atidarykite kliento sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-119">Open customer account details.</span></span>
4. <span data-ttu-id="4c7fc-120">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-120">Click Edit.</span></span>
5. <span data-ttu-id="4c7fc-121">Išplėskite skyrių SF ir pristatymas.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="4c7fc-122">Lauke Įrašo sertifikatas būtinas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="4c7fc-123">Lauke Išduoti įrašo sertifikatą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="4c7fc-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="4c7fc-125">ES įrašo sertifikato automatinis kūrimas</span><span class="sxs-lookup"><span data-stu-id="4c7fc-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="4c7fc-126">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4c7fc-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-127">Click New.</span></span>
3. <span data-ttu-id="4c7fc-128">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="4c7fc-129">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-129">Click OK.</span></span>
5. <span data-ttu-id="4c7fc-130">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="4c7fc-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-131">Click Save.</span></span>
7. <span data-ttu-id="4c7fc-132">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="4c7fc-133">Spustelėkite Registruoti važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="4c7fc-134">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="4c7fc-135">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="4c7fc-136">Išvalykite žymės langelį Išduoti įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="4c7fc-137">Įrašo sertifikatas gali būti išduotas registruojant važtaraštį arba išrašant užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="4c7fc-138">Palikite atžymėtą žymės langelį Išduoti įrašo sertifikatą, jei norite, kad jis būtų išduotas vėliau.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="4c7fc-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-139">Click OK.</span></span>
13. <span data-ttu-id="4c7fc-140">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-140">Click OK.</span></span>
14. <span data-ttu-id="4c7fc-141">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="4c7fc-142">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-142">Click Invoice.</span></span>
    * <span data-ttu-id="4c7fc-143">Patikrinkite, ar skyriuje Apžvalga pažymėti žymės langeliai Įrašo sertifikatas būtinas ir Išduoti įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="4c7fc-144">Taip pat galite pažymėti žymės langelį Spausdinti įrašo sertifikatą, kad galėtumėte sertifikatą atsispausdinti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="4c7fc-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-145">Click OK.</span></span>
17. <span data-ttu-id="4c7fc-146">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-146">Click OK.</span></span>
18. <span data-ttu-id="4c7fc-147">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="4c7fc-148">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-148">Click Invoice.</span></span>
20. <span data-ttu-id="4c7fc-149">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="4c7fc-150">Spustelėkite Rodyti išduotus įrašų sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="4c7fc-151">Spustelėkite Spausdinti.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-151">Click Print.</span></span>
23. <span data-ttu-id="4c7fc-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-152">Close the page.</span></span>
24. <span data-ttu-id="4c7fc-153">Spustelėkite keisti būseną.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-153">Click Change status.</span></span>
25. <span data-ttu-id="4c7fc-154">Lauke Nauja būsena pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="4c7fc-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-155">Click OK.</span></span>
27. <span data-ttu-id="4c7fc-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="4c7fc-157">ES įrašo sertifikato kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="4c7fc-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="4c7fc-158">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="4c7fc-159">Spustelėkite Kurti įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="4c7fc-160">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-160">Click OK.</span></span>
4. <span data-ttu-id="4c7fc-161">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="4c7fc-162">Spustelėkite Rodyti išduotus įrašų sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="4c7fc-162">Click View issued entry certificates.</span></span>

