---
title: Pardavimo komisinių registravimas
description: Šioje temoje paaiškinta, kaip apskaičiuojami ir registruojami pardavimo komisiniai.
author: omulvad
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db27255c74c55b10680594ad23424253e4c3f79e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867058"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="4d26e-103">Pardavimo komisinių registravimas</span><span class="sxs-lookup"><span data-stu-id="4d26e-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d26e-104">Šioje temoje paaiškinta, kaip apskaičiuojami ir registruojami pardavimo komisiniai.</span><span class="sxs-lookup"><span data-stu-id="4d26e-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="4d26e-105">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="4d26e-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4d26e-106">Prieš paleisdami šį vadovą, paleiskite vadovą pavadinimu „Pardavimo komisinių taisyklių nustatymas“, kad įsitikintumėte, jog turite visus reikalingus komisinių skaičiavimo nustatymus.</span><span class="sxs-lookup"><span data-stu-id="4d26e-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="4d26e-107">Atkreipkite dėmesį į savo pasirinktus komisinių proceso kliento ir prekės numerius ir naudokite juos, kai šiame vadove jūsų bus paprašyta sukurti pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="4d26e-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="4d26e-108">Pardavimo užsakymo, suteikiančio pardavėjui teisę gauti komisinius, sąskaitos faktūros išrašymas</span><span class="sxs-lookup"><span data-stu-id="4d26e-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="4d26e-109">Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="4d26e-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-110">Select **New**.</span></span>
3. <span data-ttu-id="4d26e-111">Lauke **Kliento sąskaita** išplečiamajame meniu pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4d26e-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="4d26e-112">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-112">Select **OK**.</span></span>
5. <span data-ttu-id="4d26e-113">Veiksmų srityje pasirinkite**Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="4d26e-114">Pasirinkite **Keisti rodinį**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-114">Select **Change view**.</span></span>
7. <span data-ttu-id="4d26e-115">Pasirinkite **Antraštės rodinys**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-115">Select **Header view**.</span></span>
8. <span data-ttu-id="4d26e-116">Išplėskite skyrių **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="4d26e-117">Lauko **Pardavimo grupė** reikšmė nurodo grupę, kuriai priskirtas vienas arba daugiau pardavimo atstovų.</span><span class="sxs-lookup"><span data-stu-id="4d26e-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="4d26e-118">Grupėje esantys žmonės išrašius užsakymo sąskaitą faktūrą gaus komisinius pagal iš anksto nustatytus tarifus ir paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="4d26e-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="4d26e-119">Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.</span><span class="sxs-lookup"><span data-stu-id="4d26e-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="4d26e-120">Pardavimo grupė taip pat nukopijuojama į pardavimo užsakymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="4d26e-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="4d26e-121">Galite ją pakeisti, kad ji skirtųsi nuo antraštėje ir (arba) tarp eilučių nurodytos grupės.</span><span class="sxs-lookup"><span data-stu-id="4d26e-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="4d26e-122">Lauko **Komisinių grupė** reikšmė nurodo grupę, kurią sukūrėte dėl vieno arba daugiau klientų, kad galėtumėte sekti komisinius.</span><span class="sxs-lookup"><span data-stu-id="4d26e-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="4d26e-123">Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.</span><span class="sxs-lookup"><span data-stu-id="4d26e-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="4d26e-124">Veiksmų srityje pasirinkite**Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="4d26e-125">Pasirinkite **Keisti rodinį**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-125">Select **Change view**.</span></span>
11. <span data-ttu-id="4d26e-126">Pasirinkite **Eilutės rodinys**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-126">Select **Line view**.</span></span>
12. <span data-ttu-id="4d26e-127">Lauko **Prekės numeris** išplečiamajame meniu pasirinkite prekę, kurios komisinius nustatėte.</span><span class="sxs-lookup"><span data-stu-id="4d26e-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="4d26e-128">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="4d26e-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="4d26e-129">Atkreipkite dėmesį į eilutės dalį Grynoji suma.</span><span class="sxs-lookup"><span data-stu-id="4d26e-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="4d26e-130">Joje nurodomos pardavimo įplaukos, kurios, šiuo atveju, yra komisinių skaičiavimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="4d26e-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="4d26e-131">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-131">Select **Save**.</span></span>
15. <span data-ttu-id="4d26e-132">Veiksmų srityje pasirinkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="4d26e-133">Pasirinkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="4d26e-134">Išplėskite skyrių **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="4d26e-135">Lauke **Kiekis** pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="4d26e-136">Lauke **Registravimas** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="4d26e-137">Pasirinkite **Gerai**, tada kitoje srityje – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="4d26e-138">Operacijos registravimas gali užtrukti apie minutę.</span><span class="sxs-lookup"><span data-stu-id="4d26e-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="4d26e-139">Palaukite, kol apdorojimas baigsis ir neuždarykite puslapio.</span><span class="sxs-lookup"><span data-stu-id="4d26e-139">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="4d26e-140">Registruotų pardavimo komisinių peržiūra</span><span class="sxs-lookup"><span data-stu-id="4d26e-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="4d26e-141">Veiksmų srityje pasirinkite **Sąskaita faktūra**, o tada vėl pasirinkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="4d26e-142">Veiksmų srityje pasirinkite **Sąskaita faktūra**, tada pasirinkite **Komisinių operacijos**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="4d26e-143">Skirtuke **Apžvalga** rodomos eilutės, nurodančios pardavimo atstovams, susietiems su pardavimo užsakymu, už kurį išrašyta sąskaita faktūra, mokėtinas komisinių sumas.</span><span class="sxs-lookup"><span data-stu-id="4d26e-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="4d26e-144">Peržiūrėkime išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="4d26e-144">Let's review the details.</span></span>  
    - <span data-ttu-id="4d26e-145">Jei naudojote vadovą „Pardavimo komisinių taisyklių nustatymas“ **Pardavimo komisinių** grupei nustatyti, yra du pardavėjai, kurie gaus pardavimo komisinius, ir komisiniai abiems pardavėjams padalijami po lygiai.</span><span class="sxs-lookup"><span data-stu-id="4d26e-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="4d26e-146">Šiame pavyzdyje komisinių suma apskaičiuojama kaip pardavimo įplaukų procentinė dalis (užsakymo eilutės grynoji suma).</span><span class="sxs-lookup"><span data-stu-id="4d26e-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="4d26e-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d26e-147">Close the page.</span></span>
4. <span data-ttu-id="4d26e-148">Pasirinkite **Kvitas**.</span><span class="sxs-lookup"><span data-stu-id="4d26e-148">Select **Voucher**.</span></span> <span data-ttu-id="4d26e-149">Galite peržiūrėti komisinių sumų, kurios užregistruotos iš anksto numatytų komisinių išlaidų ir mokėtinų komisinių sąskaitose, kvitų operacijas.</span><span class="sxs-lookup"><span data-stu-id="4d26e-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

