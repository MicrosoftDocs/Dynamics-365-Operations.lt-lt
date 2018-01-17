---
title: PVM ataskaitos Europoje
description: "Šioje temoje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo, skirto kai kurioms Europos šalims, nustatymą ir generavimą."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7ce3c0397986ba2281aae7b71d579f3fe5f488ae
ms.openlocfilehash: 415e23190c6d7d12e824a42dec3916a4c3f5bc92
ms.contentlocale: lt-lt
ms.lasthandoff: 12/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="53eb0-103">PVM ataskaitos Europoje</span><span class="sxs-lookup"><span data-stu-id="53eb0-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="53eb0-104">Šioje temoje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo, skirto kai kurioms Europos šalims, nustatymą ir generavimą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="53eb0-105">Šioje temoje pateikiamas bendras PVM išrašo nustatymo ir generavimo metodas.</span><span class="sxs-lookup"><span data-stu-id="53eb0-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="53eb0-106">Šį metodą gali bendrai naudoti vartotojai, kurių juridiniai subjektai yra toliau nurodytose šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="53eb0-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="53eb0-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="53eb0-107">Austria</span></span>
-   <span data-ttu-id="53eb0-108">Belgija</span><span class="sxs-lookup"><span data-stu-id="53eb0-108">Belgium</span></span>
-   <span data-ttu-id="53eb0-109">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="53eb0-109">Czech Republic</span></span>
-   <span data-ttu-id="53eb0-110">Estija</span><span class="sxs-lookup"><span data-stu-id="53eb0-110">Estonia</span></span>
-   <span data-ttu-id="53eb0-111">Suomija</span><span class="sxs-lookup"><span data-stu-id="53eb0-111">Finland</span></span>
-   <span data-ttu-id="53eb0-112">Vokietija</span><span class="sxs-lookup"><span data-stu-id="53eb0-112">Germany</span></span>
-   <span data-ttu-id="53eb0-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="53eb0-113">Latvia</span></span>
-   <span data-ttu-id="53eb0-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="53eb0-114">Lithuania</span></span>
-   <span data-ttu-id="53eb0-115">Olandija</span><span class="sxs-lookup"><span data-stu-id="53eb0-115">Netherlands</span></span>
-   <span data-ttu-id="53eb0-116">Švedija</span><span class="sxs-lookup"><span data-stu-id="53eb0-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="53eb0-117">PVM išrašo apžvalga</span><span class="sxs-lookup"><span data-stu-id="53eb0-117">VAT statement overview</span></span>
<span data-ttu-id="53eb0-118">PVM išrašas pagrįstas PVM operacijų sumomis.</span><span class="sxs-lookup"><span data-stu-id="53eb0-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="53eb0-119">PVM išrašo generavimo procesas yra PVM apmokėjimo proceso, kuris vykdomas naudojant funkciją Sudengti ir užregistruoti PVM, dalis.</span><span class="sxs-lookup"><span data-stu-id="53eb0-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="53eb0-120">Ši funkcija apskaičiuoja nurodyto laikotarpio PVM.</span><span class="sxs-lookup"><span data-stu-id="53eb0-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="53eb0-121">Sudengimo skaičiavimas apima mokesčio operacijos pasirinkto sudengimo laikotarpio užregistruotą PVM.</span><span class="sxs-lookup"><span data-stu-id="53eb0-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="53eb0-122">PVM išrašo duomenų skaičiavimo procesas pagrįstas ryšiu tarp PVM kodų ir PVM ataskaitų kodų, kai PVM ataskaitų kodai atitinka PVM išrašų langelius (arba XML žymes).</span><span class="sxs-lookup"><span data-stu-id="53eb0-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="53eb0-123">Reikia nustatyti kiekvieno PVM kodo kiekvieno operacijos tipo PVM ataskaitų kodus, pvz., kaip apmokestinamą pardavimą, apmokestinamus pirkimus, apmokestinamą importą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="53eb0-124">Šio tipo operacijos aprašytos tolesniame šios temos skyriuje PVM ataskaitų PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="53eb0-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="53eb0-125">Reikia nustatyti kiekvieno PVM ataskaitų kodo konkretų ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="53eb0-126">Tuo pat metu PVM kodai yra susiejami su konkrečiu PVM rinkėju per PVM sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="53eb0-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="53eb0-127">Reikia nustatyti kiekvieno PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="53eb0-128">Todėl PVM kodo ataskaitos sąrankoje galima pasirinkti tik PVM ataskaitų kodus su tuo pačiu ataskaitos maketu, kuris nustatytas ir priskirtas PVM rinkėjui PVM kodo PVM sudengimo laikotarpiuose.</span><span class="sxs-lookup"><span data-stu-id="53eb0-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="53eb0-129">PVM operacija, sugeneruota užregistravus užsakymą arba žurnalą, apima PVM kodą, PVM šaltinį, PVM kryptį ir operacijos sumas (mokesčio bazinę sumą ir mokesčio sumą apskaitos valiuta, PVM valiuta ir operacijos valiuta).</span><span class="sxs-lookup"><span data-stu-id="53eb0-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="53eb0-130">Atsižvelgiant į mokesčio operacijos atributų derinį, operacijos sumos sudaro bendras PVM kodų nurodytų PVM ataskaitų kodų sumas.</span><span class="sxs-lookup"><span data-stu-id="53eb0-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="53eb0-131">Tolesnėje iliustracijoje pavaizduotas duomenų ryšys.</span><span class="sxs-lookup"><span data-stu-id="53eb0-131">The following illustration shows the data relationship.</span></span>

![diagrama](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="53eb0-133">PVM išrašo sąranka</span><span class="sxs-lookup"><span data-stu-id="53eb0-133">VAT statement setup</span></span>
<span data-ttu-id="53eb0-134">Norėdami generuoti PVM išrašą, turite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="53eb0-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="53eb0-135">PVM rinkėjų nustatymas PVM ataskaitoms teikti</span><span class="sxs-lookup"><span data-stu-id="53eb0-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="53eb0-136">Prieš nustatydami PVM ataskaitų kodus, turite pasirinkti tinkamą PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="53eb0-137">Puslapio **PVM rinkėjai** dalyje **Bendra** pasirinkite **Ataskaitos maketas**.</span><span class="sxs-lookup"><span data-stu-id="53eb0-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="53eb0-138">Šis maketas bus naudojamas nustatant PVM ataskaitų kodus.</span><span class="sxs-lookup"><span data-stu-id="53eb0-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="53eb0-139">PVM ataskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="53eb0-139">Sales tax reporting codes</span></span>

<span data-ttu-id="53eb0-140">PVM ataskaitų kodai yra langelių kodai PVM išraše arba žymių pavadinimai XML formatu.</span><span class="sxs-lookup"><span data-stu-id="53eb0-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="53eb0-141">Šie kodai naudojami ataskaitos sumoms sujungti ir paruošti.</span><span class="sxs-lookup"><span data-stu-id="53eb0-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="53eb0-142">Kai konfigūruojate PVM išrašo elektroninių ataskaitų formatą, bus naudojami galutinių sumų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="53eb0-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="53eb0-143">PVM ataskaitų kodus galite kurti ir tvarkyti puslapyje **PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="53eb0-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="53eb0-144">Kiekvienam kodui turite priskirti ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="53eb0-144">You must assign each code a report layout.</span></span> <span data-ttu-id="53eb0-145">Sukūrę PVM ataskaitų kodus, galite kodus pasirinkti puslapio **PVM kodai** dalyje **Ataskaitų sąranka**.</span><span class="sxs-lookup"><span data-stu-id="53eb0-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="53eb0-146">PVM kodai, skirti PVM ataskaitos teikti</span><span class="sxs-lookup"><span data-stu-id="53eb0-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53eb0-147"><strong>Operacijos tipas</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="53eb0-148"><strong>Operacijų ir sumų, kurios bus apskaičiuotos, aprašas operacijos tipe</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-149"><strong>Apmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="53eb0-150">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-151">Operacijos data patenka į pasirinktą laikotarpį/</span><span class="sxs-lookup"><span data-stu-id="53eb0-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="53eb0-152">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-153">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-154"><strong>Neapmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="53eb0-155">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-156">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-157">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-158">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-159"><strong>Mokėtinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="53eb0-160">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-161">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-162">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-163">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-164"><strong>Apmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-165">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-166">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-167">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-168">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-169"><strong>Neapmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-170">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-171">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-172">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-173">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-174"><strong>PVM pardavimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-175">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-176">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-177">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-178">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-179"><strong>Apmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="53eb0-180">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-181">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-182">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-183">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-184"><strong>Neapmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="53eb0-185">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-186">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-187">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-188">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-189"><strong>Gautinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="53eb0-190">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-191">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-192">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-193">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-194"><strong>Apmokestinama pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-195">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-196">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-197">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-198">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-199"><strong>PVM pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-200">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-201">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-202">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-203">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-204"><strong>PVM pirkimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-205">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-206">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-207">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="53eb0-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="53eb0-208">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-209"><strong>Apmokestinamas importas</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="53eb0-210">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-211">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-212"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="53eb0-213">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-214"><strong>Korespondentinis apmokėjimas už importą</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="53eb0-215">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-216">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-217"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="53eb0-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="53eb0-218">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-219"><strong>Apmokestinama importo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-220">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-221">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="53eb0-222">e</span><span class="sxs-lookup"><span data-stu-id="53eb0-222">e</span></span><li><span data-ttu-id="53eb0-223"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="53eb0-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="53eb0-224">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-225"><strong>Korespondentinio apmokėjimo už importą kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="53eb0-226">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-227">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-228">Mokesčio kryptis yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="53eb0-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="53eb0-229">d</span><span class="sxs-lookup"><span data-stu-id="53eb0-229">d</span></span><li><span data-ttu-id="53eb0-230">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53eb0-231"><strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="53eb0-232">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-233">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-234"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="53eb0-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="53eb0-235">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="53eb0-236"><strong>Koresp. naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="53eb0-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="53eb0-237">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="53eb0-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="53eb0-238">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="53eb0-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="53eb0-239"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="53eb0-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="53eb0-240">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="53eb0-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="53eb0-241">Ankstesnėje lentelėje laikoma, kad toliau pateikti kriterijai yra patenkinami.</span><span class="sxs-lookup"><span data-stu-id="53eb0-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="53eb0-242">Mokesčių bazinė suma yra operacijos suma iš lauko **Pradinė suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="53eb0-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="53eb0-243">Mokesčių suma yra perėjimo suma iš lauko **Faktinė PVM suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="53eb0-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="53eb0-244">ER modelio ir ataskaitos formato konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="53eb0-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="53eb0-245">Galite naudoti elektronines ataskaitas (ER), kad sukonfigūruotumėte išrašus ir ataskaitas bei eksportuotumėte duomenis skirtingais elektroniniais formatais nekeisdami X++ kodo.</span><span class="sxs-lookup"><span data-stu-id="53eb0-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="53eb0-246">Papildoma informacija:</span><span class="sxs-lookup"><span data-stu-id="53eb0-246">For additional information:</span></span>

-   [<span data-ttu-id="53eb0-247">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="53eb0-247">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="53eb0-248">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="53eb0-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="53eb0-249">Lokalizavimo reikalavimai – GER konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="53eb0-249">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="53eb0-250">PVM išrašų konkrečiai šaliai būdingi ištekliai</span><span class="sxs-lookup"><span data-stu-id="53eb0-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="53eb0-251">Kiekvienos šalies PVM išrašas turi atitikti šalies teisės reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="53eb0-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="53eb0-252">Toliau pateiktoje lentelėje nurodytoms šalims priskiriami PVM išrašų iš anksto nustatyti bendrieji modeliai ir formatai.</span><span class="sxs-lookup"><span data-stu-id="53eb0-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="53eb0-253">Šalis</span><span class="sxs-lookup"><span data-stu-id="53eb0-253">Country</span></span>        | <span data-ttu-id="53eb0-254">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="53eb0-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="53eb0-255">Austrija</span><span class="sxs-lookup"><span data-stu-id="53eb0-255">Austria</span></span>        |  [<span data-ttu-id="53eb0-256">PVM išrašo informacija, skirta Austrijai</span><span class="sxs-lookup"><span data-stu-id="53eb0-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="53eb0-257">Belgija</span><span class="sxs-lookup"><span data-stu-id="53eb0-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="53eb0-258">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="53eb0-258">Czech Republic</span></span> |  [<span data-ttu-id="53eb0-259">PVM išrašo informacija, skirta Čekijos Respublikai</span><span class="sxs-lookup"><span data-stu-id="53eb0-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="53eb0-260">Estija</span><span class="sxs-lookup"><span data-stu-id="53eb0-260">Estonia</span></span>        |  [<span data-ttu-id="53eb0-261">PVM išrašo informacija, skirta Estijai</span><span class="sxs-lookup"><span data-stu-id="53eb0-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="53eb0-262">Suomija</span><span class="sxs-lookup"><span data-stu-id="53eb0-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="53eb0-263">Vokietija</span><span class="sxs-lookup"><span data-stu-id="53eb0-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="53eb0-264">Italija</span><span class="sxs-lookup"><span data-stu-id="53eb0-264">Italy</span></span>          | [<span data-ttu-id="53eb0-265">PVM išrašo informacija, skirta Italijai</span><span class="sxs-lookup"><span data-stu-id="53eb0-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="53eb0-266">Latvija</span><span class="sxs-lookup"><span data-stu-id="53eb0-266">Latvia</span></span>         | [<span data-ttu-id="53eb0-267">PVM išrašo informacija, skirta Latvijai</span><span class="sxs-lookup"><span data-stu-id="53eb0-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="53eb0-268">Lietuva</span><span class="sxs-lookup"><span data-stu-id="53eb0-268">Lithuania</span></span>      | [<span data-ttu-id="53eb0-269">PVM išrašo informacija, skirta Lietuvai</span><span class="sxs-lookup"><span data-stu-id="53eb0-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="53eb0-270">Olandija</span><span class="sxs-lookup"><span data-stu-id="53eb0-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="53eb0-271">Švedija</span><span class="sxs-lookup"><span data-stu-id="53eb0-271">Sweden</span></span>         |                                                                                 |






