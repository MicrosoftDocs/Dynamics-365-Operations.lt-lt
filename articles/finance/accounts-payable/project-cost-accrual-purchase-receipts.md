---
title: Projekto išlaidų kaupimas pirkimo kvituose
description: Šioje temoje aprašoma, kaip sukauptas projekto išlaidas pirkimo kvituose galima sekti naudojant „Microsoft“ „Dynamics 365 Finance“.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a930b4921a29d5ce561ce0e958733f0c3261b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445949"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="b7b5d-103">Projekto išlaidų kaupimas pirkimo kvituose</span><span class="sxs-lookup"><span data-stu-id="b7b5d-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b5d-104">Šioje temoje aprašoma, kaip sukauptas projekto išlaidas pirkimo kvituose galima sekti naudojant „Microsoft“ „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="b7b5d-105">Projekto SF dažnai gaunamos vėliau negu gaunamos prekės ir paslaugos, o tai gali turėti didelės įtakos pagrindiniams projekto efektyvumo indikatoriams (KPI).</span><span class="sxs-lookup"><span data-stu-id="b7b5d-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="b7b5d-106">Svarbu turėti galimybę sekti šias finansinių ir projekto ataskaitų operacijas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="b7b5d-107">Tai pavaizduota toliau pateiktame scenarijaus pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="b7b5d-108">„Contoso Consulting“ pradėjo naują debesies diegimo projektą.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="b7b5d-109">Sukuriamas pirkimo užsakymas pirkti kompiuterį projektui.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="b7b5d-110">Kompiuteris kainuos 1500 dol., o diegimo paslaugos kainuos 150 dol.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="b7b5d-111">Tiekėjas pristatė ir įdiegė kompiuterį, bet „Contoso Consulting“ sąskaitos faktūros dar negavo.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="b7b5d-112">Prieš pateikiant sąskaitą faktūrą projekto vadovas norėtų matyti sukauptas 1650 dol. vertės projekto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="b7b5d-113">Ši kaina taip pat turi būti nurodoma įmonės mėnesio pabaigos finansinėse ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="b7b5d-114">Pateikiant ataskaitas sukauptos išlaidos turi būti įrašomos finansiniu lygmeniu ir projekto lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="b7b5d-115">Gali būti sekamas prekės ir įsigijimo kategorijų produkto kvito finansinis naujinimas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="b7b5d-116">Jeigu sekate prekių naujinimą, puslapyje **Mokėtinos sumos parametrai** pasirinkite parinktį **Registruoti produkto kvitus didžiojoje knygoje**.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="b7b5d-117">[![Mokėtinų sumų parametrų puslapis](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="b7b5d-118">Jeigu sekate įsigijimo kategorijų naujinimą, puslapyje **Kategorijos strategijos taisyklė** pasirinkite strategijas **Pirkimas**, o po to pasirinkite kiekvienos įsigijimo kategorijos parinktį **Kaupti pirkimo gavimo išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="b7b5d-119">[![Kategorijos strategijos taisyklės puslapis](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="b7b5d-120">Sąskaitos **Pirkimo išlaidos, kurioms neišrašyta SF** ir **Pirkimo kaupimas**, esančios dalyje **Registravimo nustatymas**, bus naudojamos registruojant su produkto kvitu susietus kvitus.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="b7b5d-121">Naudodami tą patį scenarijų pažiūrėkime, kokią įtaką produkto kvito užregistravimas turės didžiajai knygai ir projekto informacijai.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="b7b5d-122">**1 veiksmas:** Sukurti ir patvirtinti naują projekto pirkimo užsakymą, kad jame būtų nurodyta 1500 dol. vertės kompiuterio pirkimo suma ir 150 dol. vertės diegimo paslaugos.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="b7b5d-123">[![Naujo pirkimo užsakymo kūrimas](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="b7b5d-124">Patvirtinus pirkimo užsakymą sukuriamos projekto fiksuotos savikainos operacijos.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="b7b5d-125">[![Operacijos sukurtos](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="b7b5d-126">Fiksuotos savikainos operacijų lauke nustatomas lauko **Operacijos kilmė** parametras **Pirkimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="b7b5d-127">Sukūrus ir patvirtinus pirkimo užsakymą projekto operacijos nesukuriamos.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="b7b5d-128">**2 veiksmas:** Tiekiamos prekės, teikiamos paslaugos ir užregistruojamas produkto kvitas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="b7b5d-129">Registruojant produkto kvitą sukuriamas ir užregistruojamas didžiosios knygos kvitas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="b7b5d-130">Kvite nurodomas pirkimo išlaidų, sąskaitos, kuriai neišrašyta SF, ir kredito pirkimo kaupimo sąskaitos debetas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="b7b5d-131">[![Kvitų operacijos](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b7b5d-132">Registruojant produkto kvitą bus naudojamas įsigijimo kategorijoms ir produktams skirtas registravimo nustatymas, o ne projekto kategorijoms skirtas registravimo nustatymas.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="b7b5d-133">Norint, kad būtų rodomas teisingas pirkimo kaupimų finansinis poveikis, šį nustatymą reikia sulygiuoti.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="b7b5d-134">Puslapyje **Įsigijimo kategorija** įsigijimo kategorijas galima susieti su projekto kategorijomis.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="b7b5d-135">[![Įsigijimo kategorijos puslapis](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="b7b5d-136">**3 veiksmas:** Kurti tiekėjo SF juodraštį.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="b7b5d-137">Registruojant produkto kvitą projekto informacija nepakeičiama.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="b7b5d-138">Kaip problemos apėjimo būdą tiekėjo sąskaitos faktūros juodraštį galite sukurti iš karto užregistravę pirkimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="b7b5d-139">Eikite į puslapį **Pirkimo užsakymas** &gt; **SF skirtukas** &gt; **Kurti** &gt; **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="b7b5d-140">Taip sukuriamas laukiančios SF dokumentas, kurį naudojant atnaujinama projekto informacija.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="b7b5d-141">Sukūrus tiekėjo SF juodraštį sukuriamos laukiančios projekto operacijos.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="b7b5d-142">[![Laukiančios projekto operacijos](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="b7b5d-143">Puslapyje **Fiksuota savikaina** atliekant 1 veiksmą sukurti įrašai bus uždaryti ir bus sukurti nauji įrašai, kuriuose nurodomi iš laukiančios tiekėjo sąskaitos faktūros gauti išlaidų įsipareigojimai.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="b7b5d-144">Bus nustatyta fiksuotos savikainos lauko **Operacijos kilmė** parinktis **Tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="b7b5d-145">[![Fiksuotos savikainos puslapis](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="b7b5d-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="b7b5d-146">Kol nebus gauta faktinė tiekėjo SF, tiekėjo SF ir toliau bus laukiančios būsenos.</span><span class="sxs-lookup"><span data-stu-id="b7b5d-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



