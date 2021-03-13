---
title: Transportavimo mokesčių derinimo valdymas
description: Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014513"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="3ff86-103">Transportavimo mokesčių derinimo valdymas</span><span class="sxs-lookup"><span data-stu-id="3ff86-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ff86-104">Šioje temoje aprašomas transportavimo mokesčių derinimo procesas.</span><span class="sxs-lookup"><span data-stu-id="3ff86-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="3ff86-105">Transportavimo mokesčius galima suderinti neautomatiniu arba automatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3ff86-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="3ff86-106">Norėdami transportavimo mokesčius derinti automatiškai, turite nustatyti pagrindinį auditą ir jame nurodyti kriterijus, pagal kuriuos nustatoma, kurios transportavimo sąskaitos bus derinamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3ff86-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="3ff86-107">Transportavimo mokesčių derinimo procesas</span><span class="sxs-lookup"><span data-stu-id="3ff86-107">The freight reconciliation process</span></span>

<span data-ttu-id="3ff86-108">Transportavimo tarifus skaičiuoja tarifų mechanizmas, kuris yra susijęs su atitinkamu siuntimo vežėju.</span><span class="sxs-lookup"><span data-stu-id="3ff86-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="3ff86-109">Jeigu krovinys yra patvirtintas, sugeneruojama transportavimo sąskaita ir į ją įvedami transportavimo tarifai.</span><span class="sxs-lookup"><span data-stu-id="3ff86-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="3ff86-110">Transportavimo tarifai kaip papildomos išlaidos yra paskiriami atitinkamam šaltinio dokumentui (pirkimo užsakymo, pardavimo užsakymo ir (arba) perdavimo užsakymo), atsižvelgiant į sąranką, naudojamą įprastame atsiskaitymo procese.</span><span class="sxs-lookup"><span data-stu-id="3ff86-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="3ff86-111">Transportavimo mokesčių derinimo procesas (taip pat vadinamas gretinimo procesu) gali prasidėti iškart, kai iš vežėjo gaunama transportavimo SF.</span><span class="sxs-lookup"><span data-stu-id="3ff86-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="3ff86-112">SF galima gauti elektroniniu būdu arba išspausdintą ant popieriaus.</span><span class="sxs-lookup"><span data-stu-id="3ff86-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="3ff86-113">Jei SF gauta išspausdinta ant popieriaus, galite generuoti elektroninę SF, transportavimo sąskaitą naudodami kaip šabloną.</span><span class="sxs-lookup"><span data-stu-id="3ff86-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="3ff86-114">[![Transportavimo mokesčio derinimo procesas](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="3ff86-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="3ff86-115">Neautomatinis derinimas</span><span class="sxs-lookup"><span data-stu-id="3ff86-115">Manual reconciliation</span></span>

<span data-ttu-id="3ff86-116">Jei norite transportavimo mokesčius derinti neautomatiniu būdu, kiekvieną krovinio, kuriam išrašoma SF, SF eilutę turite suderinti su transportavimo sąskaitos eilute arba eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="3ff86-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="3ff86-117">Šis derinimas atliekamas puslapyje **Transportavimo sąskaitos ir SF gretinimas**.</span><span class="sxs-lookup"><span data-stu-id="3ff86-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="3ff86-118">Jei SF eilutės suma nesutampa su transportavimo sąskaitos suma, turite pasirinkti skirtumo suderinimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="3ff86-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="3ff86-119">Jei yra kelios suderinimo priežastys, joms galite padalinti nesuderintą sumą.</span><span class="sxs-lookup"><span data-stu-id="3ff86-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="3ff86-120">Suderinimo priežastis lemia, kaip skirtumo sumos registruojamos DK.</span><span class="sxs-lookup"><span data-stu-id="3ff86-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="3ff86-121">Kai atskaitomas visos SF sumos suderinimas, jis pateikiamas patvirtinti, o tada žurnalas užregistruojamas.</span><span class="sxs-lookup"><span data-stu-id="3ff86-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="3ff86-122">Toliau esančiame paveikslėlyje parodyta, kaip generuoti transportavimo sąskaitą faktūrą ir derinti transportavimo mokesčius.</span><span class="sxs-lookup"><span data-stu-id="3ff86-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="3ff86-123">[![Transportavimo mokesčio derinimo užduotys](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="3ff86-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="3ff86-124">Automatinis derinimas</span><span class="sxs-lookup"><span data-stu-id="3ff86-124">Automatic reconciliation</span></span>

<span data-ttu-id="3ff86-125">Norėdami derinti automatiškai, turite nurodyti derinimo grafiką ir SF bei siuntimo vežėjus, kuriuos reikia naudoti.</span><span class="sxs-lookup"><span data-stu-id="3ff86-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="3ff86-126">SF eilutės ir transportavimo sąskaitos yra derinamos pagal pagrindinio audito sąranką ir transportavimo sąskaitos tipą.</span><span class="sxs-lookup"><span data-stu-id="3ff86-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="3ff86-127">Įvykdę automatinį suderinimą, turite sutvarkyti visas SF, kurių sistemai nepavyko suderinti.</span><span class="sxs-lookup"><span data-stu-id="3ff86-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="3ff86-128">Tada turite šias SF apdoroti neautomatiniu būdu, kad galėtumėte užregistruoti visas mokėjimo SF.</span><span class="sxs-lookup"><span data-stu-id="3ff86-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="3ff86-129">Transportavimo mokesčių sąskaitų ir sąskaitų faktūrų gretinimas naudojant automatinį arba rankinį derinimą</span><span class="sxs-lookup"><span data-stu-id="3ff86-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="3ff86-130">*Gretinimas* yra transportavimo sąskaitų, atitinkančių kiekvieną transportavimo sąskaitą faktūrą, ieškojimo procesas.</span><span class="sxs-lookup"><span data-stu-id="3ff86-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="3ff86-131">Tai galima atlikti sugretinus sąskaitos faktūros eilutes vieną po kito (neautomatinis gretinimas) arba sugretinus visas galimas sąskaitas faktūras iš karto (automatinis gretinimas).</span><span class="sxs-lookup"><span data-stu-id="3ff86-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="3ff86-132">Automatinis gretinimas</span><span class="sxs-lookup"><span data-stu-id="3ff86-132">Auto matching</span></span>

<span data-ttu-id="3ff86-133">Kai kelios transportavimo sąskaitos faktūros gretinamos su ta pačia transportavimo sąskaita, automatinio gretinimo procesas vyksta taip:</span><span class="sxs-lookup"><span data-stu-id="3ff86-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="3ff86-134">Visos nesugretintos transportavimo sąskaitos faktūros rūšiuojamos pagal sumą, pirmiausia – didžiausią sumą.</span><span class="sxs-lookup"><span data-stu-id="3ff86-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="3ff86-135">Transportavimo mokesčių sąskaitos faktūros gretinamos viena po kitos, kol transportavimo sąskaitoje neliks teigiamos sumos.</span><span class="sxs-lookup"><span data-stu-id="3ff86-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="3ff86-136">Atsižvelgiant į pagrindinio audito nustatymą ir likusią transportavimo sąskaitų faktūrų sumą, nustatoma likusi suma.</span><span class="sxs-lookup"><span data-stu-id="3ff86-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="3ff86-137">Rankinis gretinimas</span><span class="sxs-lookup"><span data-stu-id="3ff86-137">Manual matching</span></span>

<span data-ttu-id="3ff86-138">Bus galima sugretinti visas transportavimo sąskaitas, kurių suma teigiama.</span><span class="sxs-lookup"><span data-stu-id="3ff86-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="3ff86-139">Panašiai kaip ir automatiniame gretinime, vartotojas galės sugretinti transportavimo sąskaitas faktūras, turinčias neigiamas sumas, su nevisiškai sugretintomis transportavimo sąskaitomis.</span><span class="sxs-lookup"><span data-stu-id="3ff86-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="3ff86-140">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3ff86-140">Example</span></span>

<span data-ttu-id="3ff86-141">Tarkime, kad turite 1500 sumos transportavimo sąskaitą (FB) ir sukūrėte tris transportavimo sąskaitas faktūras tai transportavimo sąskaitai su viena SF eilute kiekvienai SF su šiais parametrais:</span><span class="sxs-lookup"><span data-stu-id="3ff86-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="3ff86-142">Pradinė transportavimo sąskaita (FB): Suma 1500</span><span class="sxs-lookup"><span data-stu-id="3ff86-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="3ff86-143">1 sąskaita faktūra (Inv1): Suma 1000</span><span class="sxs-lookup"><span data-stu-id="3ff86-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="3ff86-144">2 sąskaita faktūra (Inv2): Suma 600</span><span class="sxs-lookup"><span data-stu-id="3ff86-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="3ff86-145">3 sąskaita faktūra (Inv3): Suma ‑100</span><span class="sxs-lookup"><span data-stu-id="3ff86-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="3ff86-146">Automatinio gretinimo rezultatas</span><span class="sxs-lookup"><span data-stu-id="3ff86-146">Automatic matching result</span></span>

<span data-ttu-id="3ff86-147">Automatinis gretinimas bus vykdomas tokia tvarka:</span><span class="sxs-lookup"><span data-stu-id="3ff86-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="3ff86-148">Išrūšiuos visas transportavimo sąskaitas faktūras mažėjimo tvarka pagal sumą: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="3ff86-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="3ff86-149">Sugretins Inv1 su FB.</span><span class="sxs-lookup"><span data-stu-id="3ff86-149">Match Inv1 with FB.</span></span> <span data-ttu-id="3ff86-150">Inv1 turi 1000 sugretinta, o FB turi likusią 500 sumą, todėl būsena nustatoma kaip *Iš dalies sugretinta*.</span><span class="sxs-lookup"><span data-stu-id="3ff86-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="3ff86-151">Sugretins Inv2 su FB.</span><span class="sxs-lookup"><span data-stu-id="3ff86-151">Match Inv2 with FB.</span></span> <span data-ttu-id="3ff86-152">Inv2 turi 500 sugretinta, o FB turi likusį 0, todėl būsena nustatoma kaip *Pilnai sugretinta*.</span><span class="sxs-lookup"><span data-stu-id="3ff86-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="3ff86-153">Kadangi FB dabar yra visiškai sugretinta, Inv3 nebus apdorota.</span><span class="sxs-lookup"><span data-stu-id="3ff86-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="3ff86-154">Rankinio gretinimo rezultatas</span><span class="sxs-lookup"><span data-stu-id="3ff86-154">Manual matching result</span></span>

<span data-ttu-id="3ff86-155">Neautomatinio gretinimo rezultatai skiriasi atsižvelgiant į gretinimo tvarką, kaip pavaizduota tolesnio pavyzdžio atvejuose.</span><span class="sxs-lookup"><span data-stu-id="3ff86-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="3ff86-156">Rankinio gretinimo 1 atvejis</span><span class="sxs-lookup"><span data-stu-id="3ff86-156">Manual matching case 1</span></span>

<span data-ttu-id="3ff86-157">Vienas šio pavyzdžio rankinio gretinimo būdas yra elgtis taip:</span><span class="sxs-lookup"><span data-stu-id="3ff86-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="3ff86-158">Sugretinti FB su Inv1.</span><span class="sxs-lookup"><span data-stu-id="3ff86-158">Match FB with Inv1.</span></span> <span data-ttu-id="3ff86-159">FB turi likusią 500 sumą, todėl būsena yra nustatoma kaip *Iš dalies sugretinta*.</span><span class="sxs-lookup"><span data-stu-id="3ff86-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="3ff86-160">Sugretins Inv2 su FB.</span><span class="sxs-lookup"><span data-stu-id="3ff86-160">Match Inv2 with FB.</span></span> <span data-ttu-id="3ff86-161">Inv2 turi 500 sugretinta, o FB turi likusį 0, todėl būsena nustatoma kaip *Pilnai sugretinta*.</span><span class="sxs-lookup"><span data-stu-id="3ff86-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="3ff86-162">Kai Inv3 gretinsite neautomatiniu būdu, nerasite jokių nesugretintų transportavimo sąskaitų.</span><span class="sxs-lookup"><span data-stu-id="3ff86-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="3ff86-163">Iš esmės šis atvejis yra toks pat, kaip ir automatiniame gretinime</span><span class="sxs-lookup"><span data-stu-id="3ff86-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="3ff86-164">Rankinio gretinimo 2 atvejis</span><span class="sxs-lookup"><span data-stu-id="3ff86-164">Manual matching case 2</span></span>

<span data-ttu-id="3ff86-165">Kitas šio pavyzdžio rankinio gretinimo būdas yra elgtis taip:</span><span class="sxs-lookup"><span data-stu-id="3ff86-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="3ff86-166">Sugretinti Inv3 su FB.</span><span class="sxs-lookup"><span data-stu-id="3ff86-166">Match Inv3 with FB.</span></span> <span data-ttu-id="3ff86-167">Dabar FB turi likusią 1600 sumą, kuri yra tokia pati, kaip iš 1500 atimti neigiamą 100 sumą.</span><span class="sxs-lookup"><span data-stu-id="3ff86-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="3ff86-168">Tiek FB, tiek Inv3 sugretintas kiekis yra -100.</span><span class="sxs-lookup"><span data-stu-id="3ff86-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="3ff86-169">Sugretinti Inv1 ir Inv 2 su FB vieną po kito.</span><span class="sxs-lookup"><span data-stu-id="3ff86-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="3ff86-170">FB yra visiškai sugretinta.</span><span class="sxs-lookup"><span data-stu-id="3ff86-170">FB is fully matched.</span></span>

<span data-ttu-id="3ff86-171">Kaip rodo šis pavyzdys, transportavimo sąskaitos faktūrų su neigiamomis sumomis gretinimą reikia atlikti tik rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3ff86-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="3ff86-172">Taip užtikrinsite, kad visada galima sugretinti transportavimo sąskaitas faktūras, turinčias neigiamas sumas, su nevisiškai sugretintomis transportavimo sąskaitomis, kas leidžia valdyti gretinimo seką.</span><span class="sxs-lookup"><span data-stu-id="3ff86-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>
