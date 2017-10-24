---
title: Kurti kliento SF
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="9492a-102">Kurti kliento SF</span><span class="sxs-lookup"><span data-stu-id="9492a-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9492a-103">**Kliento SF pardavimo užsakymui** yra sąskaita, susijusi su pardavimu ir kurią organizacija pateikia klientui.</span><span class="sxs-lookup"><span data-stu-id="9492a-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="9492a-104">Šis kliento SF tipas kuriamas remiantis pardavimo užsakymu, į kurį įeina užsakymo eilutės ir prekių numeriai.</span><span class="sxs-lookup"><span data-stu-id="9492a-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="9492a-105">Prekių numeriai yra nurodyti ir užregistruoti didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="9492a-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="9492a-106">Kliento SF pardavimo užsakymui skirtų papildomos knygos žurnalo įrašų nėra.</span><span class="sxs-lookup"><span data-stu-id="9492a-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="9492a-107">Daugiau informacijos žr. [Kurti pardavimo užsakymų sąskaitas faktūras](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="9492a-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="9492a-108">**Laisvos formos SF** nėra susijusi su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="9492a-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="9492a-109">Joje pateikiamos užsakymo eilutės, kuriose yra DK sąskaitos, laisvo pobūdžio aprašai ir pardavimo suma, kuriuos įvedate.</span><span class="sxs-lookup"><span data-stu-id="9492a-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="9492a-110">Į šios rūšies SF prekės numerio įvesti negalite.</span><span class="sxs-lookup"><span data-stu-id="9492a-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="9492a-111">Turite įvesti atitinkamą PVM informaciją.</span><span class="sxs-lookup"><span data-stu-id="9492a-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="9492a-112">Pagrindinė pardavimo sąskaita nurodoma kiekvienoje SF eilutėje, kurią paskirstyti į kelias DK sąskaitas galite **Laisvos formos SF** puslapyje spustelėdami **Paskirstyti sumas**.</span><span class="sxs-lookup"><span data-stu-id="9492a-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="9492a-113">Be to, kliento balansas suminėje sąskaitoje regisruojamas iš naudojamo laisvos formos SF registravimo profilio.</span><span class="sxs-lookup"><span data-stu-id="9492a-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="9492a-114">Norėdami gauti daugiau informacijos, žr. </span><span class="sxs-lookup"><span data-stu-id="9492a-114">For more information see:</span></span>

[<span data-ttu-id="9492a-115">Kurti laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="9492a-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="9492a-116">Kurti laisvos formos šabloną</span><span class="sxs-lookup"><span data-stu-id="9492a-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="9492a-117">Priskirti klientui laisvos formos SF šabloną</span><span class="sxs-lookup"><span data-stu-id="9492a-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="9492a-118">Generuoti ir registruoti pasikartojančias laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="9492a-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="9492a-119">**Išankstinė SF** yra tokia sąskaita, kuri parengiama kaip faktinių sąskaitos sumų įvertinimas, prieš užregistruojant sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="9492a-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="9492a-120">Galite išspausdinti arba kliento SF pardavimo užsakymui, arba laisvos formos sąskaitos faktūros išankstinę sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="9492a-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="9492a-121">Registruoti ir spausdinti atskiras kliento SF, kurios paremtos pardavimo užsakymais</span><span class="sxs-lookup"><span data-stu-id="9492a-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="9492a-122">Naudodami šį procesą galite sukurti sąskaitą faktūrą, grindžiamą pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="9492a-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="9492a-123">To gali prireikti, jei nuspręsite išrašyti klientui sąskaitą faktūrą prieš pristatydami prekes arba suteikdami paslaugas.</span><span class="sxs-lookup"><span data-stu-id="9492a-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="9492a-124">Kai registruojate sąskaitą faktūrą, **SF likučio** kiekis kiekvienai prekei atnaujinamas nurodant bendruosius SF kiekius iš pasirinkto pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="9492a-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="9492a-125">Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**.</span><span class="sxs-lookup"><span data-stu-id="9492a-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="9492a-126">Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="9492a-127">Peržiūrėti pardavimo užsakymų būseną galite sąrašo puslapyje **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="9492a-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="9492a-128">Sąrašo puslapyje **Atidarytos klientų SF** galite peržiūrėti savo registruotas sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="9492a-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="9492a-129">Registruoti ir spausdinti atskiras klientų SF, kurios paremtos važtaraščiais ir data</span><span class="sxs-lookup"><span data-stu-id="9492a-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="9492a-130">Šią procedūrą naudokite, kai užregistruotas vienas ar keli pardavimo užsakymo važtaraščiai.</span><span class="sxs-lookup"><span data-stu-id="9492a-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="9492a-131">Kliento SF grindžiama šiais važtaraščiais ir atspindi juose nurodytus kiekius.</span><span class="sxs-lookup"><span data-stu-id="9492a-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="9492a-132">SF finansinė informacija yra paremta informacija, įvesta jums registruojant SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="9492a-133">Galima sukurti kliento SF, kuri paremta važtaraščio eilutės prekėmis, išsiųstomis iki dabar, net jei dar ne visos konkretaus pardavimo užsakymo prekės yra išsiųstos.</span><span class="sxs-lookup"><span data-stu-id="9492a-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="9492a-134">Tai galite atlikti jei, pavyzdžiui, jūsų juridinis subjektas per mėnesį vienam klientui išduoda vieną SF, kurioje pateikiama informacija apie visus siuntinius, išsiųstus tą mėnesį.</span><span class="sxs-lookup"><span data-stu-id="9492a-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="9492a-135">Kiekvienas važtaraštis reiškia iš dalies arba visiškai atliktą pardavimo užsakymo prekių pristatymą.</span><span class="sxs-lookup"><span data-stu-id="9492a-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="9492a-136">Jums užregistravus SF, **SF likučio** kiekis kiekvienai prekei yra atnaujinamas bendra pristatytų kiekių iš pasirinktų važtaraščių suma.</span><span class="sxs-lookup"><span data-stu-id="9492a-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="9492a-137">Jei visų prekių **SF likučio** kiekis ir **Pristatymo likučio** kiekis pardavimo užsakyme yra 0 (nulis), pardavimo užsakymo būsena pakeičiama į **SF išrašyta**.</span><span class="sxs-lookup"><span data-stu-id="9492a-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="9492a-138">Jeigu **SF likučio** kiekis nėra 0 (nulis), pardavimo užsakymo būsena lieka nepakitusi ir galima įvesti papildomas SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="9492a-139">Atsargų operacijos yra atnaujinamos SF numeriu, o būsena pardavimo užsakymo lauke **Eilutės būsena** pakeičiama į **SF išrašyta**.</span><span class="sxs-lookup"><span data-stu-id="9492a-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="9492a-140">Pardavimo užsakymų būseną peržiūrėkite sąrašo puslapyje **Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="9492a-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="9492a-141">Konsoliduoti pardavimo užsakymus arba važtaraščius, norint juos registruoti</span><span class="sxs-lookup"><span data-stu-id="9492a-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="9492a-142">Šį procesą naudokite, kai vienam ar keliems pardavimo užsakymams galima išrašyti SF, ir norite juos konsoliduoti į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="9492a-143">**Pardavimo užsakymo** sąrašo puslapyje galite pasirinkti kelias SF ir tada joms konsoliduoti naudoti **Generuoti SF**.</span><span class="sxs-lookup"><span data-stu-id="9492a-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="9492a-144">Puslapyje **SF registravimas** galite pakeisti **Suminio užsakymo** nustatymą, kad būtų sumuojama pagal užsakymo numerį (kai yra keli vieno pardavimo užsakymo važtaraščiai) arba pagal SF sąskaitą (kai yra keli vienos SF sąskaitos pardavimo užsakymai).</span><span class="sxs-lookup"><span data-stu-id="9492a-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="9492a-145">Naudokite mygtuką **Išdėstyti**, kad pardavimo užsakymus pagal **Suminio užsakymo** parametrus konsoliduotumėte į vieną SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="9492a-146">Papildomos nuostatos, keičiančios registravimo veikseną</span><span class="sxs-lookup"><span data-stu-id="9492a-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="9492a-147">Toliau nurodyti laukai keičia registravimo proceso veikseną.</span><span class="sxs-lookup"><span data-stu-id="9492a-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9492a-148">Laukas</span><span class="sxs-lookup"><span data-stu-id="9492a-148">Field</span></span></th>
<th><span data-ttu-id="9492a-149">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9492a-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9492a-150">Kiekis</span><span class="sxs-lookup"><span data-stu-id="9492a-150">Quantity</span></span></td>
<td><span data-ttu-id="9492a-151">Pasirinkite kiekius, kuriais grindžiamas dokumentų registravimas.</span><span class="sxs-lookup"><span data-stu-id="9492a-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="9492a-152">Prieinamos parinktys skiriasi – jos priklauso nuo registruojamo dokumento tipo, pvz., važtaraščio ar SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="9492a-153"><strong>Pristatyti dabar</strong> – pasirinkti visus kiekius, kurie įvesti į lauką <strong>Pristatyti dabar</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="9492a-154">Naudokite šią parinktį, jei norite patvirtinti ar pristatyti dalinį užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9492a-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="9492a-155"><strong>Paimti</strong> – pasirinkti visus kiekius, kurie paimti.</span><span class="sxs-lookup"><span data-stu-id="9492a-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="9492a-156"><strong>Visi</strong> – pasirinkti visus pardavimo užsakymų kiekius, kurie dar neatnaujinti pagal dabartinio dokumento tipą.</span><span class="sxs-lookup"><span data-stu-id="9492a-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="9492a-157"><strong>Važtaraštis</strong> – pasirinkti visus kiekius, kurie atnaujinti pagal važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="9492a-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="9492a-158"><strong>Paimtas kiekis ir atsargose nelaikomi produktai</strong> – pasirinkti visus kiekius, kurie paimti ir visus produktų kiekius, kurie nelaikomi atsargose.</span><span class="sxs-lookup"><span data-stu-id="9492a-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-159">Registravimas</span><span class="sxs-lookup"><span data-stu-id="9492a-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="9492a-160">Norėdami į žurnalą įtraukti pardavimo užsakymą, pasirinkite šią parinktį.</span><span class="sxs-lookup"><span data-stu-id="9492a-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="9492a-161">Norėdami spausdinti išankstinį pardavimo užsakymą, panaikinkite šios parinkties žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="9492a-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="9492a-162"><strong>Pastaba.</strong> Jei susitarėte dėl mokėjimo grafiko, išankstiniame pardavimo užsakyme mokėjimo grafikas nerodomas.</span><span class="sxs-lookup"><span data-stu-id="9492a-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="9492a-163">Mokėjimo grafikai rodomi tik faktiniuose pardavimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="9492a-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9492a-164">Vėlesnis pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="9492a-164">Late selection</span></span></td>
<td><span data-ttu-id="9492a-165">Pažymėkite šią parinktį, jei norite pasirinktą užklausą taikyti vėliau.</span><span class="sxs-lookup"><span data-stu-id="9492a-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="9492a-166">Ši pasirinktis naudojama su paketinėmis užduotimis.</span><span class="sxs-lookup"><span data-stu-id="9492a-166">This option is used for batch jobs.</span></span> <span data-ttu-id="9492a-167">Užklausa vykdoma paleidus paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9492a-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-168">Mažinti kiekį</span><span class="sxs-lookup"><span data-stu-id="9492a-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="9492a-169">Pasirinkite šią parinktį, kad užregistravus dokumentą būtų automatiškai sumažinamas pristatytas kiekis – tuomet pristatytas kiekis bus lygus turimoms atsargoms.</span><span class="sxs-lookup"><span data-stu-id="9492a-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9492a-170">Spausdinti</span><span class="sxs-lookup"><span data-stu-id="9492a-170">Print</span></span></td>
<td><span data-ttu-id="9492a-171">Pasirinkite, kada reikia spausdinti dokumentus.</span><span class="sxs-lookup"><span data-stu-id="9492a-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="9492a-172"><strong>Dabart.</strong> – dokumentus spausdinti atnaujinus kiekvieną SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="9492a-173"><strong>Vėliau</strong> – dokumentus spausdinti, kai atnaujinamos visos SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="9492a-174">
<strong>Pastaba.</strong> Lauką <strong>Spausdinti</strong> galėsite naudoti tik pasirinkę parinktį <strong>Spausdinti SF</strong>, <strong>Spausdinti patvirtinimą</strong>, <strong>Spausdinti išrinkimo dokumentą</strong> arba <strong>Spausdinti važtaraštį</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="9492a-175">Pavyzdžiui, puslapyje <strong>Rūšiavimas pagal formas</strong> turite nustatyti sistemą, kad informacija būtų rūšiuojama pagal SF sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="9492a-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="9492a-176">Tada galite pasirinkti parinktį <strong>Vėliau</strong>, kad būtų spausdinami pagal SF sąskaitą surūšiuotame pakete esantys dokumentai.</span><span class="sxs-lookup"><span data-stu-id="9492a-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="9492a-177">Kitu atveju dokumentai spausdinami neužbaigus apdorojimo proceso ir nėra surūšiuojami puslapyje <strong>Rūšiavimas pagal formas</strong> nurodyta tvarka.</span><span class="sxs-lookup"><span data-stu-id="9492a-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-178">Spausdinti SF</span><span class="sxs-lookup"><span data-stu-id="9492a-178">Print invoice</span></span></td>
<td><span data-ttu-id="9492a-179">Pažymėkite šią parinktį, kad būtų spausdinama SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-179">Select this option to print the invoice.</span></span> <span data-ttu-id="9492a-180">Jei ši parinktis yra išjungta, spausdinti SF galite jos neregistravę.</span><span class="sxs-lookup"><span data-stu-id="9492a-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9492a-181">Siųsti el. laišką</span><span class="sxs-lookup"><span data-stu-id="9492a-181">Send e-mail</span></span></td>
<td><span data-ttu-id="9492a-182">Pasirinkite šią parinktį, norėdami klientui pardavimo užsakymo SF siųsti kaip el. laiško priedą, ją užregistravus.</span><span class="sxs-lookup"><span data-stu-id="9492a-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="9492a-183">Priedai siunčiami kaip PDF ir XML failai.</span><span class="sxs-lookup"><span data-stu-id="9492a-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="9492a-184">Ši parinktis galima tik tada, jei <strong>Elektroninių SF parametrų</strong> puslapyje pasirenkate parinktį <strong>Įgalinti CFD (elektronines SF)</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="9492a-185"><strong>Pastaba.</strong> (MEX) Šis valdiklis pasiekiamas tik juridiniams subjektams, kurių pagrindinis adresas yra Meksikoje.</span><span class="sxs-lookup"><span data-stu-id="9492a-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-186">Naudoti spausdinimo valdymo paskirtį</span><span class="sxs-lookup"><span data-stu-id="9492a-186">Use print management destination</span></span></td>
<td><span data-ttu-id="9492a-187">Pasirinkite šią parinktį, norėdami naudoti operacijos, dokumento ar modulio spausdinimo nuostatas, nurodytas <strong>Spausdinimo valdymo sąrankos</strong> puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9492a-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9492a-188">Tikrinti kredito limitą</span><span class="sxs-lookup"><span data-stu-id="9492a-188">Check credit limit</span></span></td>
<td><span data-ttu-id="9492a-189">Pasirinkite informaciją, kuri turėtų būti analizuojama tikrinant kredito limitą.</span><span class="sxs-lookup"><span data-stu-id="9492a-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="9492a-190"><strong>Nėra</strong> – nereikalaujama tikrinti kredito limito.</span><span class="sxs-lookup"><span data-stu-id="9492a-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="9492a-191"><strong>Balansas</strong> – kredito limitas tikrinamas pagal kliento balansą.</span><span class="sxs-lookup"><span data-stu-id="9492a-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="9492a-192"><strong>Balansas + važtaraštis arba produkto gavimo kvitas</strong> – kredito limitas tikrinamas pagal kliento balansą ir pristatymus.</span><span class="sxs-lookup"><span data-stu-id="9492a-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="9492a-193"><strong>Balansas + visi</strong> – Kredito limitas tikrinamas pagal kliento balansą, pristatymus ir atvirus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="9492a-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-194">Kredito koregavimas</span><span class="sxs-lookup"><span data-stu-id="9492a-194">Credit correction</span></span></td>
<td><span data-ttu-id="9492a-195">Pasirinkite šią parinktį, kad kvitų operacijose kredito pažyma būtų rodoma kaip debetas.</span><span class="sxs-lookup"><span data-stu-id="9492a-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9492a-196">Kredituoti likusį kiekį</span><span class="sxs-lookup"><span data-stu-id="9492a-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="9492a-197">Pasirinkite šią parinktį, jei registruojant kredito pažymą norite palikti likusį užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="9492a-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="9492a-198">Jei šios parinkties žymės langelis išvalomas, likęs kiekis nustatomas 0 (nuliu).</span><span class="sxs-lookup"><span data-stu-id="9492a-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9492a-199">Suminis atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="9492a-199">Summary update for</span></span></td>
<td><span data-ttu-id="9492a-200">Pasirinkite, kaip turėtų būti apibendrinami keli pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="9492a-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="9492a-201"><strong>Niekaip</strong> – pardavimo užsakymų neapibendrinti.</span><span class="sxs-lookup"><span data-stu-id="9492a-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="9492a-202">Pavyzdžiui, bus sukurta atskira kiekvieno pardavimo užsakymo SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="9492a-203"><strong>SF sąskaita</strong> – visus pasirinktus užsakymus apibendrinti pagal kriterijus, nustatytus puslapyje <strong>Suminio atnaujinimo parametrai</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="9492a-204"><strong>Užsakymas</strong> – pasirinktą užsakymų intervalą apibendrinti į vieną jūsų nurodytą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9492a-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="9492a-205">Užsakymai apibendrinami pagal kriterijus, nustatytus puslapyje <strong>Suminio atnaujinimo parametrai</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="9492a-206">Jei pasirenkate šią parinktį, lauke <strong>Pardavimo užsakymas</strong> turite pasirinkti reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9492a-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="9492a-207"><strong>Automatinis sumavimas</strong> – jei <strong>Suminio atnaujinimo</strong> puslapyje nurodyti suminiai atnaujinimai, visus pasirinktus užsakymus sumuoti pagal kriterijus, nustatytus <strong>Suminio atnaujinimo parametrų</strong> puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9492a-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="9492a-208">Jei suminiai atnaujinimai nenurodyti, užsakymas registruojamas atskirai.</span><span class="sxs-lookup"><span data-stu-id="9492a-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="9492a-209"><strong>Važtaraštis</strong> – pasirinktą užsakymų intervalą sumuoti į vieną kiekvieno važtaraščio SF.</span><span class="sxs-lookup"><span data-stu-id="9492a-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="9492a-210">Šią parinktį galima naudoti, tik jei lauke <strong>Kiekis</strong> pasirinkta <strong>Važtaraštis</strong>.</span><span class="sxs-lookup"><span data-stu-id="9492a-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






