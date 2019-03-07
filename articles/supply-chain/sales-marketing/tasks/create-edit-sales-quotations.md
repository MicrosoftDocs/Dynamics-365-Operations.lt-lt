---
title: Kurti ir redaguoti pardavimo pasiūlymus
description: Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "343632"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="9e531-103">Kurti ir redaguoti pardavimo pasiūlymus</span><span class="sxs-lookup"><span data-stu-id="9e531-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e531-104">Ši procedūra parodo, kaip sukurti ir atnaujinti pardavimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="9e531-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="9e531-105">Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="9e531-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="9e531-106">Kurti pardavimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="9e531-106">Create a sales quotation</span></span>
1. <span data-ttu-id="9e531-107">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="9e531-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="9e531-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="9e531-108">Click New.</span></span>
3. <span data-ttu-id="9e531-109">Lauke Sąskaitos tipas pasirinkite 'Potencialus klientas'.</span><span class="sxs-lookup"><span data-stu-id="9e531-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="9e531-110">Lauke Potencialus klientas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9e531-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="9e531-111">Išplėskite skyrių Bendra.</span><span class="sxs-lookup"><span data-stu-id="9e531-111">Expand the General section.</span></span>
    * <span data-ttu-id="9e531-112">Todėl, kad pasiūlymą kurti pasirinkote iš srities Pardavimas ir rinkodara, tipas automatiškai nustatomas į Pardavimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="9e531-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="9e531-113">Norėdami sukurti projekto pasiūlymą, turite jį pasiekti iš modulio Projektų valdymas ir apskaita.</span><span class="sxs-lookup"><span data-stu-id="9e531-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="9e531-114">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e531-114">Click OK.</span></span>
    * <span data-ttu-id="9e531-115">Laukai ir veiksmai pasiūlymo eilutėse yra labai panašūs į esančius pardavimo užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="9e531-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="9e531-116">Kaip ir pardavimo užsakymus, pasiūlymus galima sukurti tam tikrai prekei arba, kai prekės numeris nežinomas arba jo nėra pasiūlymo kūrimo metu, pasiūlymus galima kurti pardavimo kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="9e531-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="9e531-117">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9e531-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="9e531-118">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="9e531-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="9e531-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-119">Close the page.</span></span>
10. <span data-ttu-id="9e531-120">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9e531-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9e531-121">Jei yra eilutėje pasirinktos prekės galiojančių prekybos sutarčių, taikomos kainos ir nuolaidos automatiškai nukopijuojamos į pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="9e531-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="9e531-122">Įsitikinkite, kad lauke Vieneto kaina yra vertė, taip pat, jei norite, galite įvesti nuolaidos vertes.</span><span class="sxs-lookup"><span data-stu-id="9e531-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="9e531-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="9e531-123">Click Save.</span></span>
12. <span data-ttu-id="9e531-124">Srityje Veiksmas spustelėkite Pardavimo pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="9e531-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="9e531-125">Spustelėkite Sumos.</span><span class="sxs-lookup"><span data-stu-id="9e531-125">Click Totals.</span></span>
14. <span data-ttu-id="9e531-126">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e531-126">Click OK.</span></span>
15. <span data-ttu-id="9e531-127">Spustelėkite eilutę Pardavimo pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="9e531-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="9e531-128">Spustelėkite Kainos.</span><span class="sxs-lookup"><span data-stu-id="9e531-128">Click Prices.</span></span>
    * <span data-ttu-id="9e531-129">Puslapyje Paleisti kainos modeliavimą galite eksperimentuoti koreguodami pasiūlymo numatomas įplaukas arba pelningumą pagal norimą vieneto kainą, nuolaidos sumą, nuolaidos procentą, bendrąją sumą, maržą arba kontribucijos maržą.</span><span class="sxs-lookup"><span data-stu-id="9e531-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="9e531-130">Kai jus tenkina tiksliniai skaičiai, galite pasiūlymą taikyti pasiūlymo eilutei ir jos su kaina susiję laukai bus atitinkamai atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="9e531-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="9e531-131">Galite sukurti tiek kainos modeliavimų, kiek norite.</span><span class="sxs-lookup"><span data-stu-id="9e531-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="9e531-132">Spustelėjus Naujas, kainų sąlygos iš dabartinio pasiūlymo eilutės nukopijuojamos į puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="9e531-133">Tada galite keisti vertes bet kuriame su kaina susijusiame lauke į tikslines.</span><span class="sxs-lookup"><span data-stu-id="9e531-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="9e531-134">Pakeitus vieną iš laukų, bus suaktyvintas perskaičiavimas ir kituose laukuose.</span><span class="sxs-lookup"><span data-stu-id="9e531-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="9e531-135">Norint, kad sistema skaičiuoti pardavimo maržą ir kontribucijos maržą, turi būti žinoma produkto vieneto savikaina.</span><span class="sxs-lookup"><span data-stu-id="9e531-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="9e531-136">Naudodami skirtuką Modeliuotos kainos matysite išsamų pradinių kainų, siūlomų pakeitimų ir jų poveikio pasiūlymo sumos rodinį.</span><span class="sxs-lookup"><span data-stu-id="9e531-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="9e531-137">Paprastai, kai modeliuojant nustatoma nauja suma ir ji taikoma pasiūlymo eilutei, sistema perskaičiuoja ir įveda naują vertę lauke Vieneto kaina.</span><span class="sxs-lookup"><span data-stu-id="9e531-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="9e531-138">Jei modeliavimas pagrįstas nauja marža arba nauja kontribucijos marža, atnaujinamas laukas Grynoji suma, o Vieneto kaina yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="9e531-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="9e531-139">Abiem atvejais bus panaikintos bet kokios nuolaidos, prieš modeliavimą buvusios pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9e531-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="9e531-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-140">Close the page.</span></span>
18. <span data-ttu-id="9e531-141">Veiksmų srityje spustelėkite Pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="9e531-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="9e531-142">Spustelėkite Siųsti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="9e531-142">Click Send quotation.</span></span>
20. <span data-ttu-id="9e531-143">Lauke Spausdinti pasiūlymą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9e531-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="9e531-144">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e531-144">Click OK.</span></span>
    * <span data-ttu-id="9e531-145">Ataskaitą sugeneruoti gali užtrukti minutę.</span><span class="sxs-lookup"><span data-stu-id="9e531-145">The report may take a minute to generate.</span></span> <span data-ttu-id="9e531-146">Neuždarykite puslapio, kol tai nebus padaryta.</span><span class="sxs-lookup"><span data-stu-id="9e531-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="9e531-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="9e531-148">Atnaujinti pardavimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="9e531-148">Update a sales quotation</span></span>
1. <span data-ttu-id="9e531-149">Veiksmų srityje spustelėkite Vykdymas.</span><span class="sxs-lookup"><span data-stu-id="9e531-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="9e531-150">Spustelėkite Konvertuoti į klientą.</span><span class="sxs-lookup"><span data-stu-id="9e531-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="9e531-151">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9e531-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="9e531-152">Spustelėkite Tikrinti.</span><span class="sxs-lookup"><span data-stu-id="9e531-152">Click Check.</span></span>
    * <span data-ttu-id="9e531-153">Įsitikinkite, kad matote pranešimą, kuriame teigiama, kad įvestą sąskaitos numerį galima naudoti.</span><span class="sxs-lookup"><span data-stu-id="9e531-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="9e531-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e531-154">Click OK.</span></span>
    * <span data-ttu-id="9e531-155">Dabar sistema sukūrė naują kliento sąskaitą potencialiam pasiūlymo klientui.</span><span class="sxs-lookup"><span data-stu-id="9e531-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="9e531-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-156">Close the page.</span></span>
7. <span data-ttu-id="9e531-157">Veiksmų srityje spustelėkite Vykdymas.</span><span class="sxs-lookup"><span data-stu-id="9e531-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="9e531-158">Spustelėkite Patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9e531-158">Click Confirm.</span></span>
9. <span data-ttu-id="9e531-159">Lauke Priežastis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="9e531-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="9e531-160">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9e531-160">Click OK.</span></span>
11. <span data-ttu-id="9e531-161">Veiksmų srityje spustelėkite Bendra.</span><span class="sxs-lookup"><span data-stu-id="9e531-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="9e531-162">Spustelėkite Pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="9e531-162">Click Sales orders.</span></span>
13. <span data-ttu-id="9e531-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9e531-163">Close the page.</span></span>

