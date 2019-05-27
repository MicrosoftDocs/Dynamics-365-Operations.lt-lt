---
title: Patvirtinti pardavimo užsakymus
description: Ši procedūra parodo, kaip patvirtinti pardavimo užsakymus.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563999"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="0e5b0-103">Patvirtinti pardavimo užsakymus</span><span class="sxs-lookup"><span data-stu-id="0e5b0-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e5b0-104">Ši procedūra parodo, kaip patvirtinti pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="0e5b0-105">Jums bus parodyta, kaip patvirtinti vieną užsakymą, ir kaip patvirtinti kelis užsakymus vienu kartu.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="0e5b0-106">Šias užduotis paprastai atlieka pardavimo užsakymų tvarkytojas.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="0e5b0-107">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0e5b0-108">Prieš pradėdami įsitikinkite, kad yra keletas atvirų to paties kliento pardavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="0e5b0-109">Jei naudojate USMF, galite naudoti klientą US-027.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="0e5b0-110">Patvirtinti vieną pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="0e5b0-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="0e5b0-111">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="0e5b0-112">Sąraše raskite ir pasirinkite užsakymą, kurį norite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="0e5b0-113">Spustelėkite pardavimo užsakymo numerio nuorodą, kad atidarytumėte pasirinktą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="0e5b0-114">Veiksmų srityje spustelėkite Parduoti.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="0e5b0-115">Spustelėkite „Patvirtinti pardavimo užsakymą“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="0e5b0-116">Išplėskite arba sutraukite skyrių Parametrai.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="0e5b0-117">Įsitikinkite, kad aktyvintas registravimo laukas „Taip“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="0e5b0-118">Nustatykite spausdinimo patvirtinimo parinktį „Taip“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="0e5b0-119">Lauke „Patikrinti kredito limitą“ nurodomas metodas, naudojamas skaičiuojant kliento kredito likutį.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="0e5b0-120">Jis numatytuoju būdu kopijuojamas iš puslapio „Gautinų sumų parametrai“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="0e5b0-121">Jei norite praleisti kredito limito tikrinimą, kai tvirtinate konkretų pardavimo užsakymą, nustatykite „Patikrinti kredito limitą“ reikšmę „Nėra“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="0e5b0-122">Tačiau visada reikėtų žinoti, kad net ir nustačius šiam laukui reikšmę „Nėra“, kredito limitas vis tiek bus tikrinamas, jei kliento bendruosiuose duomenyse bus pasirinkta parinktis „Privalomas kredito limitas“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="0e5b0-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-123">Click OK.</span></span>
9. <span data-ttu-id="0e5b0-124">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-124">Click Yes.</span></span>
10. <span data-ttu-id="0e5b0-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-125">Close the page.</span></span>
11. <span data-ttu-id="0e5b0-126">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="0e5b0-127">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-127">Click Change view.</span></span>
13. <span data-ttu-id="0e5b0-128">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-128">Click Header view.</span></span>
    * <span data-ttu-id="0e5b0-129">Kai užsakymas patvirtinamas, dokumento būsena pakeičiama į „Patvirtinimas“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="0e5b0-130">Veiksmų srityje spustelėkite Parduoti.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="0e5b0-131">Spustelėkite „Pardavimo užsakymo patvirtinimas“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="0e5b0-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="0e5b0-133">Patvirtinti keletą pardavimo užsakymų vienu kartu</span><span class="sxs-lookup"><span data-stu-id="0e5b0-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="0e5b0-134">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Užsakymo patvirtinimas > Patvirtinti pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="0e5b0-135">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-135">Click Select.</span></span>
3. <span data-ttu-id="0e5b0-136">Skirtuko „Diapazonas“ sąraše pasirinkite įrašą su nuoroda į lauką „Kliento sąskaitą“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="0e5b0-137">Lauke Kriterijai spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0e5b0-138">Sąraše raskite ir pasirinkite kliento sąskaitą, turinčią keletą užsakymų, kuriuos norite masiškai patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="0e5b0-139">Jei naudojate USMF, galite pasirinkti sąskaitą US-027.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="0e5b0-140">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-140">Click OK.</span></span>
    * <span data-ttu-id="0e5b0-141">Skirtuke „Apžvalga“ rodomas užsakymų, kurie atitinka užklausos kriterijus, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="0e5b0-142">Jie bus įtraukti į patvirtinimą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="0e5b0-143">Lauke „Suvestinės atnaujinimas“ rodomas parametras, pagal kurį reikia suvesti keletą užsakymų į vieną patvirtinimo dokumentą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="0e5b0-144">Pagal numatytuosius nustatymus parinktis kopijuojama iš nustatymo „Suvestinio atnaujinimo numatytosios reikšmės“, esančio puslapyje „Mokėtinų sumų parametrai“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="0e5b0-145">Lauke „Suminis atnaujinimas“ pasirinkite „Užsakymas“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="0e5b0-146">Norint sukurti suminį atnaujinimą, būtini parametrai SF sąskaita ir valiuta.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="0e5b0-147">Tai reiškia, kad neleidžiama atlikti suminių atnaujinimų, kurių SF sąskaitos ir valiutos skirtingos.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="0e5b0-148">Papildomus parametrus galima nustatyti puslapyje „Suminio atnaujinimo parametrai“, kurį galima pasiekti iš puslapio „Gautinų sumų parametrai“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="0e5b0-149">Lauke „Pardavimo užsakymas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0e5b0-150">Sąraše pasirinkite numerį užsakymo, kurį norite padaryti suminiu užsakymu.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="0e5b0-151">Spustelėkite „Išdėstyti“.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-151">Click Arrange.</span></span>
11. <span data-ttu-id="0e5b0-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-152">Click OK.</span></span>
12. <span data-ttu-id="0e5b0-153">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0e5b0-153">Click OK.</span></span>

