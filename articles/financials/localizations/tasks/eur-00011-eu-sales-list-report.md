---
title: EUR-00011, ES pardavimo sąrašo ataskaitos generavimas.
description: Ši procedūra padeda generuoti ES pardavimų sąrašo ataskaitą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a9a1aeeec4ea22f1153e32254f64c6b7f365a8c
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848864"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="ffb30-103">EUR-00011, ES pardavimo sąrašo ataskaitos generavimas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffb30-104">Ši procedūra padeda generuoti ES pardavimų sąrašo ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="ffb30-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="ffb30-105">Tai apima ES vidaus prekybos operacijų perkėlimą į ES pardavimų sąrašą ir ataskaitos vykdymą.</span><span class="sxs-lookup"><span data-stu-id="ffb30-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="ffb30-106">Ši procedūra taip pat apima ES vidaus prekybos operacijos kūrimą demonstraciniais tikslais.</span><span class="sxs-lookup"><span data-stu-id="ffb30-106">This  procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="ffb30-107">Daugiau informacijos apie ES pardavimo sąrašų ataskaitas, įskaitant būtinąsias sąlygas, žr. „Dynamics 365 for Finance and Operations“ žinyne.</span><span class="sxs-lookup"><span data-stu-id="ffb30-107">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="ffb30-108">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="ffb30-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="ffb30-109">Procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF ir dėl to kaip šalies / regiono pavyzdį naudojant Vokietiją.</span><span class="sxs-lookup"><span data-stu-id="ffb30-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="ffb30-110">Procedūroje taip pat kaip ES šalies / regiono pavyzdys naudojama Portugalija.</span><span class="sxs-lookup"><span data-stu-id="ffb30-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="ffb30-111">Prieš atlikdami šią procedūrą, turite sukonfigūruoti ES pardavimų sąrašo ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="ffb30-112">Ši procedūra skirta buhalteriams.</span><span class="sxs-lookup"><span data-stu-id="ffb30-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="ffb30-113">Kurti ES vidaus pardavimo operaciją demonstraciniais tikslais</span><span class="sxs-lookup"><span data-stu-id="ffb30-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="ffb30-114">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="ffb30-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="ffb30-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-115">Click New.</span></span>
3. <span data-ttu-id="ffb30-116">Lauke Kliento sąskaita įveskite „PRT-001“.</span><span class="sxs-lookup"><span data-stu-id="ffb30-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="ffb30-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-117">Click OK.</span></span>
5. <span data-ttu-id="ffb30-118">Lauke „Prekės numeris“ įveskite „D0001“.</span><span class="sxs-lookup"><span data-stu-id="ffb30-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="ffb30-119">Išplėskite skyrių Eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="ffb30-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="ffb30-120">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="ffb30-121">Lauke Prekės PVM grupė įveskite 'VISAS'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="ffb30-122">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffb30-122">Click Add line.</span></span>
10. <span data-ttu-id="ffb30-123">Lauke „Prekės numeris“ įveskite „D0003“.</span><span class="sxs-lookup"><span data-stu-id="ffb30-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="ffb30-124">Lauke Prekės PVM grupė įveskite 'RAUDONA'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="ffb30-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-125">Click Save.</span></span>
13. <span data-ttu-id="ffb30-126">Veiksmų srityje spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="ffb30-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="ffb30-127">Spustelėkite Sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="ffb30-127">Click Invoice.</span></span>
15. <span data-ttu-id="ffb30-128">Išplėskite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="ffb30-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="ffb30-129">Lauke Kiekis pasirinkite Visi.</span><span class="sxs-lookup"><span data-stu-id="ffb30-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="ffb30-130">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="ffb30-131">Lauke SF data nustatykite datą '01/11/2016'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="ffb30-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-132">Click OK.</span></span>
20. <span data-ttu-id="ffb30-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="ffb30-134">Perkelti ES vidaus prekybos operacijas į ES pardavimų sąrašą</span><span class="sxs-lookup"><span data-stu-id="ffb30-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="ffb30-135">Eikite į Mokestis > Deklaracijos > Užsienio prekyba > ES pardavimų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="ffb30-136">Spustelėkite Perkelti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-136">Click Transfer.</span></span>
3. <span data-ttu-id="ffb30-137">Lauke Prekė pasirinkę Taip perkelsite prekės operacijas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="ffb30-138">Lauke Paslauga pasirinkę Taip perkelsite paslaugos operacijas.</span><span class="sxs-lookup"><span data-stu-id="ffb30-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="ffb30-139">Taip pat galite nurodyti papildomus filtrus ES vidaus prekybos operacijoms perkelti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="ffb30-140">Spustelėkite Perkelti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-140">Click Transfer.</span></span>
    * <span data-ttu-id="ffb30-141">Patvirtinkite, kad ES vidaus pardavimo operacija sėkmingai perkelta į ES pardavimo sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ffb30-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="ffb30-142">Generuoti ES pardavimo sąrašo ataskaitą</span><span class="sxs-lookup"><span data-stu-id="ffb30-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="ffb30-143">Spustelėkite Ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="ffb30-143">Click Reporting.</span></span>
2. <span data-ttu-id="ffb30-144">Lauke Ataskaitinis laikotarpis pasirinkite 'Mėnesinis'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="ffb30-145">Lauke Pradžios data nustatykite datą '01/01/2016'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="ffb30-146">Lauke Generuoti failą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ffb30-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="ffb30-147">Lauke Generuoti ataskaitą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ffb30-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="ffb30-148">Lauke Failo pavadinimas įveskite 'EUSalesList'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="ffb30-149">Lauke Ataskaitos failo pavadinimas įveskite 'EUSalesList'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="ffb30-150">Lauke ES pardavimo sąrašo registracijos ID įveskite '123'..</span><span class="sxs-lookup"><span data-stu-id="ffb30-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="ffb30-151">Šis laukas galimas tik Vokietijai.</span><span class="sxs-lookup"><span data-stu-id="ffb30-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="ffb30-152">Be to, galite nurodyti papildomus norimus įtraukti į ataskaitą filtrus ES vidaus prekybos operacijoms.</span><span class="sxs-lookup"><span data-stu-id="ffb30-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="ffb30-153">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-153">Click OK.</span></span>
    * <span data-ttu-id="ffb30-154">Patikrinkite, ar laikinieji langai rodomi patvirtinti, ir kad failas ir kontrolės ataskaita atsisiunčiami.</span><span class="sxs-lookup"><span data-stu-id="ffb30-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="ffb30-155">Pažymėti ES pardavimų sąrašo eilutes kaip Paskelbtas</span><span class="sxs-lookup"><span data-stu-id="ffb30-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="ffb30-156">Spustelėkite Žymėti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-156">Click Mark.</span></span>
2. <span data-ttu-id="ffb30-157">Spustelėkite Pažymėti kaip baigtus.</span><span class="sxs-lookup"><span data-stu-id="ffb30-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="ffb30-158">Sąraše pasirinkite lauko SF data eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffb30-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="ffb30-159">Lauke Kriterijai įveskite '01/01/2016... 01/31/2016'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="ffb30-160">Sąraše pasirinkite lauko Ataskaitos būsena eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffb30-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="ffb30-161">Lauke Kriterijai pasirinkite 'Įtraukta'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="ffb30-162">Be to, galite nurodyti papildomus norimus pažymėti kaip Paskelbtus filtrus ES vidaus prekybos operacijoms.</span><span class="sxs-lookup"><span data-stu-id="ffb30-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="ffb30-163">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-163">Click OK.</span></span>
8. <span data-ttu-id="ffb30-164">Lauke Pasirinkimas pasirinkite 'Ataskaita paruošta'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="ffb30-165">Pažymėti ES pardavimų sąrašo eilutes kaip Uždarytas</span><span class="sxs-lookup"><span data-stu-id="ffb30-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="ffb30-166">Spustelėkite Žymėti.</span><span class="sxs-lookup"><span data-stu-id="ffb30-166">Click Mark.</span></span>
2. <span data-ttu-id="ffb30-167">Spustelėkite Pažymėti kaip uždarytus.</span><span class="sxs-lookup"><span data-stu-id="ffb30-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="ffb30-168">Sąraše pažymėkite lauko SF data eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffb30-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="ffb30-169">Lauke Kriterijai įveskite '01/01/2016... 01/31/2016'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="ffb30-170">Sąraše pažymėkite lauko Ataskaitos būsena eilutę.</span><span class="sxs-lookup"><span data-stu-id="ffb30-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="ffb30-171">Lauke Kriterijai pasirinkite 'Ataskaita paruošta'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-171">In the Criteria field, select ‘Reported’.</span></span>
    * <span data-ttu-id="ffb30-172">Be to, galite nurodyti papildomus norimus pažymėti kaip Uždarytus filtrus ES vidaus prekybos operacijoms.</span><span class="sxs-lookup"><span data-stu-id="ffb30-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="ffb30-173">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffb30-173">Click OK.</span></span>
8. <span data-ttu-id="ffb30-174">Lauke Pasirinkimas pasirinkite 'Uždaryta'.</span><span class="sxs-lookup"><span data-stu-id="ffb30-174">In the Selection field, select 'Closed'.</span></span>

