---
title: 'EUR-00002: ES vidaus operacijos pakrovimo adreso nurodymas'
description: Šioje procedūroje parodoma, kaip nustatyti pakrovimo adresą, skirtą ES vidaus prekybos operacijai.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6eea2a905a59842b6f39c5b1e1c78ae6801b28e0
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852732"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="a364b-103">EUR-00002: ES vidaus operacijos pakrovimo adreso nurodymas</span><span class="sxs-lookup"><span data-stu-id="a364b-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a364b-104">Šioje procedūroje parodoma, kaip nustatyti pakrovimo adresą, skirtą ES vidaus prekybos operacijai.</span><span class="sxs-lookup"><span data-stu-id="a364b-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="a364b-105">Pavyzdžiui, Vokietijos įmonės užsisako prekių iš tiekėjo, kurio darbo adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="a364b-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="a364b-106">Šis tiekėjas turi sandėlį Italijoje ir siunčia prekes iš ten.</span><span class="sxs-lookup"><span data-stu-id="a364b-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="a364b-107">Šis pristatymas turi būti pateiktas „Intrastat“ ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="a364b-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="a364b-108">Tokia pati procedūra gali būti taikoma kliento grąžinimams.</span><span class="sxs-lookup"><span data-stu-id="a364b-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="a364b-109">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="a364b-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="a364b-110">Užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="a364b-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="a364b-111">Prieš atlikdami šią procedūrą, turite sukonfigūruoti „Intrastat“ ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a364b-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="a364b-112">Ši procedūra skirta buhalteriams.</span><span class="sxs-lookup"><span data-stu-id="a364b-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="a364b-113">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="a364b-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="a364b-114">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a364b-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a364b-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a364b-115">Click New.</span></span>
3. <span data-ttu-id="a364b-116">Įveskite arba pasirinkite reikšmę</span><span class="sxs-lookup"><span data-stu-id="a364b-116">Enter or select a value</span></span>
    * <span data-ttu-id="a364b-117">Pavyzdžiui, pasirinkite DE-001.</span><span class="sxs-lookup"><span data-stu-id="a364b-117">For example, select DE-001.</span></span> <span data-ttu-id="a364b-118">Šio tiekėjo darbo adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="a364b-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="a364b-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a364b-119">Click OK.</span></span>
5. <span data-ttu-id="a364b-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a364b-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="a364b-121">Lauke Prekės numeris įveskite arba pasirinkite reikšmę D0001.</span><span class="sxs-lookup"><span data-stu-id="a364b-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="a364b-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a364b-122">Click Save.</span></span>
8. <span data-ttu-id="a364b-123">Veiksmų srityje spustelėkite Gauti.</span><span class="sxs-lookup"><span data-stu-id="a364b-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="a364b-124">Spustelėkite Transportavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="a364b-124">Click Transportation details.</span></span>
10. <span data-ttu-id="a364b-125">Lauke Pakrovimo data ir laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="a364b-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="a364b-126">Spustelėkite Įtraukti adresą.</span><span class="sxs-lookup"><span data-stu-id="a364b-126">Click Add address.</span></span>
12. <span data-ttu-id="a364b-127">Spustelėkite Naujas ir sukurkite naują adresą, kurio paskirtis yra Pakrovimas.</span><span class="sxs-lookup"><span data-stu-id="a364b-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="a364b-128">Lauke Pavadinimas arba aprašas įveskite Italijos.</span><span class="sxs-lookup"><span data-stu-id="a364b-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="a364b-129">Pasirinkite reikšmę Pakrovimas.</span><span class="sxs-lookup"><span data-stu-id="a364b-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="a364b-130">Atminkite, kad adreso paskirtis turi būti Pakrovimas.</span><span class="sxs-lookup"><span data-stu-id="a364b-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="a364b-131">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę ITA.</span><span class="sxs-lookup"><span data-stu-id="a364b-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="a364b-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a364b-132">Click Save.</span></span>
17. <span data-ttu-id="a364b-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a364b-133">Close the page.</span></span>
18. <span data-ttu-id="a364b-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a364b-134">Click Save.</span></span>
    * <span data-ttu-id="a364b-135">Patikrinkite, ar pakrovimo adresas teisingas.</span><span class="sxs-lookup"><span data-stu-id="a364b-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="a364b-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a364b-136">Close the page.</span></span>
20. <span data-ttu-id="a364b-137">Veiksmų srityje spustelėkite Pirkti.</span><span class="sxs-lookup"><span data-stu-id="a364b-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="a364b-138">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a364b-138">Click Confirm.</span></span>
22. <span data-ttu-id="a364b-139">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="a364b-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="a364b-140">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="a364b-140">Click Invoice.</span></span>
24. <span data-ttu-id="a364b-141">Lauke Numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a364b-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="a364b-142">Įveskite datą lauke Sąskaitos faktūros data.</span><span class="sxs-lookup"><span data-stu-id="a364b-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="a364b-143">Spustelėkite Numatyt. iš: gavimo dokumento kiekio, kad atidarytumėte išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="a364b-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="a364b-144">Lauke Numatytasis eilučių kiekis pasirinkite Užsakytas kiekis.</span><span class="sxs-lookup"><span data-stu-id="a364b-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="a364b-145">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a364b-145">Click OK.</span></span>
29. <span data-ttu-id="a364b-146">Spustelėkite Transportavimo informacija.</span><span class="sxs-lookup"><span data-stu-id="a364b-146">Click Transportation details.</span></span>
    * <span data-ttu-id="a364b-147">Įsitikinkite, kad prekės buvo atgabentos iš Italijos.</span><span class="sxs-lookup"><span data-stu-id="a364b-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="a364b-148">Jei reikia, galite redaguoti pakrovimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="a364b-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="a364b-149">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a364b-149">Close the page.</span></span>
31. <span data-ttu-id="a364b-150">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="a364b-150">Click Post.</span></span>
32. <span data-ttu-id="a364b-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a364b-151">Close the page.</span></span>
33. <span data-ttu-id="a364b-152">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a364b-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="a364b-153">Spustelėkite Perkelti.</span><span class="sxs-lookup"><span data-stu-id="a364b-153">Click Transfer.</span></span>
35. <span data-ttu-id="a364b-154">Lauke Tiekėjo SF pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a364b-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="a364b-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a364b-155">Click OK.</span></span>
37. <span data-ttu-id="a364b-156">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="a364b-156">Click the General tab.</span></span>
    * <span data-ttu-id="a364b-157">Raskite naujai sukurtą eilutę ir patikrinkite, ar siuntėjas prekes išsiuntė iš Italijos.</span><span class="sxs-lookup"><span data-stu-id="a364b-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  

