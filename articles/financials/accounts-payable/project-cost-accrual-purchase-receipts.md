---
title: Projekto išlaidų kaupimas pirkimo kvituose
description: Šioje temoje aprašoma, kaip sukauptas projekto išlaidas iš pirkimo kvitų galima sekti naudojant „Microsoft Dynamics 365 for Finance and Operations“.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc822652abbba68f094fe5b8a65f796165a92c4c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "340435"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="fc2a0-103">Projekto išlaidų kaupimas pirkimo kvituose</span><span class="sxs-lookup"><span data-stu-id="fc2a0-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc2a0-104">Šioje temoje aprašoma, kaip sukauptas projekto išlaidas iš pirkimo kvitų galima sekti naudojant „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="fc2a0-105">Projekto SF dažnai gaunamos vėliau negu gaunamos prekės ir paslaugos, o tai gali turėti didelės įtakos pagrindiniams projekto efektyvumo indikatoriams (KPI).</span><span class="sxs-lookup"><span data-stu-id="fc2a0-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="fc2a0-106">Svarbu turėti galimybę sekti šias finansinių ir projekto ataskaitų operacijas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="fc2a0-107">Tai pavaizduota toliau pateiktame scenarijaus pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="fc2a0-108">„Contoso Consulting“ pradėjo naują debesies diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="fc2a0-109">Sukuriamas pirkimo užsakymas pirkti kompiuterį projektui.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="fc2a0-110">Kompiuteris kainuos 1500 dol., o diegimo paslaugos kainuos 150 dol.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="fc2a0-111">Tiekėjas pristatė ir įdiegė kompiuterį, bet „Contoso Consulting“ sąskaitos faktūros dar negavo.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="fc2a0-112">Prieš pateikiant sąskaitą faktūrą projekto vadovas norėtų matyti sukauptas 1650 dol. vertės projekto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="fc2a0-113">Ši kaina taip pat turi būti nurodoma įmonės mėnesio pabaigos finansinėse ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="fc2a0-114">Pateikiant ataskaitas sukauptos išlaidos turi būti įrašomos finansiniu lygmeniu ir projekto lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="fc2a0-115">Naudojant „Finance and Operations“ gali būti sekamas prekės ir įsigijimo kategorijų produkto kvito finansinis naujinimas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="fc2a0-116">Jeigu sekate prekių naujinimą, puslapyje **Mokėtinos sumos parametrai** pasirinkite parinktį **Registruoti produkto kvitus didžiojoje knygoje**.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="fc2a0-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="fc2a0-118">Jeigu sekate įsigijimo kategorijų naujinimą, puslapyje **Kategorijos strategijos taisyklė** pasirinkite strategijas **Pirkimas**, o po to pasirinkite kiekvienos įsigijimo kategorijos parinktį **Kaupti pirkimo gavimo išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="fc2a0-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="fc2a0-120">Sąskaitos **Pirkimo išlaidos, kurioms neišrašyta SF** ir **Pirkimo kaupimas**, esančios dalyje **Registravimo nustatymas**, bus naudojamos registruojant su produkto kvitu susietus kvitus.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="fc2a0-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="fc2a0-122">Naudodami tą patį scenarijų pažiūrėkime, kokią įtaką produkto kvito užregistravimas turės didžiajai knygai ir projekto informacijai.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="fc2a0-123">**1 veiksmas:** Sukurti ir patvirtinti naują projekto pirkimo užsakymą, kad jame būtų nurodyta 1500 dol. vertės kompiuterio pirkimo suma ir 150 dol. vertės diegimo paslaugos.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="fc2a0-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="fc2a0-125">Patvirtinus pirkimo užsakymą sukuriamos projekto fiksuotos savikainos operacijos.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="fc2a0-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="fc2a0-127">Fiksuotos savikainos operacijų lauke nustatomas lauko **Operacijos kilmė** parametras **Pirkimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="fc2a0-128">Sukūrus ir patvirtinus pirkimo užsakymą projekto operacijos nesukuriamos.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="fc2a0-129">**2 veiksmas:** Tiekiamos prekės, teikiamos paslaugos ir užregistruojamas produkto kvitas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="fc2a0-130">Registruojant produkto kvitą sukuriamas ir užregistruojamas didžiosios knygos kvitas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="fc2a0-131">Kvite nurodomas pirkimo išlaidų, sąskaitos, kuriai neišrašyta SF, ir kredito pirkimo kaupimo sąskaitos debetas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="fc2a0-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="fc2a0-133">Registruojant produkto kvitą bus naudojamas įsigijimo kategorijoms ir produktams skirtas registravimo nustatymas, o ne projekto kategorijoms skirtas registravimo nustatymas.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="fc2a0-134">Norint, kad būtų rodomas teisingas pirkimo kaupimų finansinis poveikis, šį nustatymą reikia sulygiuoti.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="fc2a0-135">Puslapyje **Įsigijimo kategorija** įsigijimo kategorijas galima susieti su projekto kategorijomis.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="fc2a0-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="fc2a0-137">**3 veiksmas:** Kurti tiekėjo SF juodraštį.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="fc2a0-138">Jei naudojamas sprendimas „Finance and Operations“, registruojant produkto kvitą projekto informacija nepakeičiama.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="fc2a0-139">Kaip problemos apėjimo būdą tiekėjo sąskaitos faktūros juodraštį galite sukurti iš karto užregistravę pirkimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="fc2a0-140">Eikite į puslapį **Pirkimo užsakymas** &gt; **SF skirtukas** &gt; **Kurti** &gt; **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="fc2a0-141">Taip sukuriamas laukiančios SF dokumentas, kurį naudojant atnaujinama projekto informacija.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="fc2a0-142">Sukūrus tiekėjo SF juodraštį sukuriamos laukiančios projekto operacijos.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="fc2a0-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="fc2a0-144">Puslapyje **Fiksuota savikaina** atliekant 1 veiksmą sukurti įrašai bus uždaryti ir bus sukurti nauji įrašai, kuriuose nurodomi iš laukiančios tiekėjo sąskaitos faktūros gauti išlaidų įsipareigojimai.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="fc2a0-145">Bus nustatyta fiksuotos savikainos lauko **Operacijos kilmė** parinktis **Tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="fc2a0-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="fc2a0-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="fc2a0-147">Kol nebus gauta faktinė tiekėjo SF, tiekėjo SF ir toliau bus laukiančios būsenos.</span><span class="sxs-lookup"><span data-stu-id="fc2a0-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



