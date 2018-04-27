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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: afcc2ea8c0ca3a5877b44fd758aec9d2caf92d92
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="923c8-103">PVM ataskaitos Europoje</span><span class="sxs-lookup"><span data-stu-id="923c8-103">VAT reporting for Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="923c8-104">Šioje temoje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo, skirto kai kurioms Europos šalims, nustatymą ir generavimą.</span><span class="sxs-lookup"><span data-stu-id="923c8-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="923c8-105">Šioje temoje pateikiamas bendras PVM išrašo nustatymo ir generavimo metodas.</span><span class="sxs-lookup"><span data-stu-id="923c8-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="923c8-106">Šį metodą gali bendrai naudoti vartotojai, kurių juridiniai subjektai yra toliau nurodytose šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="923c8-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="923c8-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="923c8-107">Austria</span></span>
-   <span data-ttu-id="923c8-108">Belgija</span><span class="sxs-lookup"><span data-stu-id="923c8-108">Belgium</span></span>
-   <span data-ttu-id="923c8-109">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="923c8-109">Czech Republic</span></span>
-   <span data-ttu-id="923c8-110">Estija</span><span class="sxs-lookup"><span data-stu-id="923c8-110">Estonia</span></span>
-   <span data-ttu-id="923c8-111">Suomija</span><span class="sxs-lookup"><span data-stu-id="923c8-111">Finland</span></span>
-   <span data-ttu-id="923c8-112">Vokietija</span><span class="sxs-lookup"><span data-stu-id="923c8-112">Germany</span></span>
-   <span data-ttu-id="923c8-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="923c8-113">Latvia</span></span>
-   <span data-ttu-id="923c8-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="923c8-114">Lithuania</span></span>
-   <span data-ttu-id="923c8-115">Olandija</span><span class="sxs-lookup"><span data-stu-id="923c8-115">Netherlands</span></span>
-   <span data-ttu-id="923c8-116">Švedija</span><span class="sxs-lookup"><span data-stu-id="923c8-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="923c8-117">PVM išrašo apžvalga</span><span class="sxs-lookup"><span data-stu-id="923c8-117">VAT statement overview</span></span>
<span data-ttu-id="923c8-118">PVM išrašas pagrįstas PVM operacijų sumomis.</span><span class="sxs-lookup"><span data-stu-id="923c8-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="923c8-119">PVM išrašo generavimo procesas yra PVM apmokėjimo proceso, kuris vykdomas naudojant funkciją Sudengti ir užregistruoti PVM, dalis.</span><span class="sxs-lookup"><span data-stu-id="923c8-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="923c8-120">Ši funkcija apskaičiuoja nurodyto laikotarpio PVM.</span><span class="sxs-lookup"><span data-stu-id="923c8-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="923c8-121">Sudengimo skaičiavimas apima mokesčio operacijos pasirinkto sudengimo laikotarpio užregistruotą PVM.</span><span class="sxs-lookup"><span data-stu-id="923c8-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="923c8-122">PVM išrašo duomenų skaičiavimo procesas pagrįstas ryšiu tarp PVM kodų ir PVM ataskaitų kodų, kai PVM ataskaitų kodai atitinka PVM išrašų langelius (arba XML žymes).</span><span class="sxs-lookup"><span data-stu-id="923c8-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="923c8-123">Reikia nustatyti kiekvieno PVM kodo kiekvieno operacijos tipo PVM ataskaitų kodus, pvz., kaip apmokestinamą pardavimą, apmokestinamus pirkimus, apmokestinamą importą.</span><span class="sxs-lookup"><span data-stu-id="923c8-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="923c8-124">Šio tipo operacijos aprašytos tolesniame šios temos skyriuje PVM ataskaitų PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="923c8-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="923c8-125">Reikia nustatyti kiekvieno PVM ataskaitų kodo konkretų ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="923c8-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="923c8-126">Tuo pat metu PVM kodai yra susiejami su konkrečiu PVM rinkėju per PVM sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="923c8-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="923c8-127">Reikia nustatyti kiekvieno PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="923c8-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="923c8-128">Todėl PVM kodo ataskaitos sąrankoje galima pasirinkti tik PVM ataskaitų kodus su tuo pačiu ataskaitos maketu, kuris nustatytas ir priskirtas PVM rinkėjui PVM kodo PVM sudengimo laikotarpiuose.</span><span class="sxs-lookup"><span data-stu-id="923c8-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="923c8-129">PVM operacija, sugeneruota užregistravus užsakymą arba žurnalą, apima PVM kodą, PVM šaltinį, PVM kryptį ir operacijos sumas (mokesčio bazinę sumą ir mokesčio sumą apskaitos valiuta, PVM valiuta ir operacijos valiuta).</span><span class="sxs-lookup"><span data-stu-id="923c8-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="923c8-130">Atsižvelgiant į mokesčio operacijos atributų derinį, operacijos sumos sudaro bendras PVM kodų nurodytų PVM ataskaitų kodų sumas.</span><span class="sxs-lookup"><span data-stu-id="923c8-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="923c8-131">Tolesnėje iliustracijoje pavaizduotas duomenų ryšys.</span><span class="sxs-lookup"><span data-stu-id="923c8-131">The following illustration shows the data relationship.</span></span>

![diagrama](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="923c8-133">PVM išrašo sąranka</span><span class="sxs-lookup"><span data-stu-id="923c8-133">VAT statement setup</span></span>
<span data-ttu-id="923c8-134">Norėdami generuoti PVM išrašą, turite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="923c8-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="923c8-135">PVM rinkėjų nustatymas PVM ataskaitoms teikti</span><span class="sxs-lookup"><span data-stu-id="923c8-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="923c8-136">Prieš nustatydami PVM ataskaitų kodus, turite pasirinkti tinkamą PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="923c8-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="923c8-137">Puslapio **PVM rinkėjai** dalyje **Bendra** pasirinkite **Ataskaitos maketas**.</span><span class="sxs-lookup"><span data-stu-id="923c8-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="923c8-138">Šis maketas bus naudojamas nustatant PVM ataskaitų kodus.</span><span class="sxs-lookup"><span data-stu-id="923c8-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="923c8-139">PVM ataskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="923c8-139">Sales tax reporting codes</span></span>

<span data-ttu-id="923c8-140">PVM ataskaitų kodai yra langelių kodai PVM išraše arba žymių pavadinimai XML formatu.</span><span class="sxs-lookup"><span data-stu-id="923c8-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="923c8-141">Šie kodai naudojami ataskaitos sumoms sujungti ir paruošti.</span><span class="sxs-lookup"><span data-stu-id="923c8-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="923c8-142">Kai konfigūruojate PVM išrašo elektroninių ataskaitų formatą, bus naudojami galutinių sumų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="923c8-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="923c8-143">PVM ataskaitų kodus galite kurti ir tvarkyti puslapyje **PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="923c8-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="923c8-144">Kiekvienam kodui turite priskirti ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="923c8-144">You must assign each code a report layout.</span></span> <span data-ttu-id="923c8-145">Sukūrę PVM ataskaitų kodus, galite kodus pasirinkti puslapio **PVM kodai** dalyje **Ataskaitų sąranka**.</span><span class="sxs-lookup"><span data-stu-id="923c8-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="923c8-146">PVM kodai, skirti PVM ataskaitos teikti</span><span class="sxs-lookup"><span data-stu-id="923c8-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="923c8-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>PVM kodų</strong> puslapis.</span><span class="sxs-lookup"><span data-stu-id="923c8-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="923c8-148">Toliau pateikiamoje lentelėje aprašomi PVM kodų ataskaitų sąrankos operacijų tipai.</span><span class="sxs-lookup"><span data-stu-id="923c8-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="923c8-149">Skaičiuojant įtraukiamos visų šaltinių tipų, išskyrus PVM, operacijos.</span><span class="sxs-lookup"><span data-stu-id="923c8-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="923c8-150"><strong>Operacijos tipas</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="923c8-151"><strong>Operacijų ir sumų, kurios bus apskaičiuotos, aprašas operacijos tipe</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-152"><strong>Apmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="923c8-153">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-154">Operacijos data patenka į pasirinktą laikotarpį/</span><span class="sxs-lookup"><span data-stu-id="923c8-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="923c8-155">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-156">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-157"><strong>Neapmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="923c8-158">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-159">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-160">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="923c8-161">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-162"><strong>Mokėtinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="923c8-163">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-164">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-165">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-166">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-167"><strong>Apmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-168">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-169">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-170">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-171">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-172"><strong>Neapmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-173">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-174">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-175">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="923c8-176">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-177"><strong>PVM pardavimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-178">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-179">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-180">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-181">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-182"><strong>Apmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="923c8-183">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-184">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-185">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-186">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-187"><strong>Neapmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="923c8-188">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-189">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-190">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="923c8-191">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-192"><strong>Gautinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="923c8-193">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-194">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-195">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-196">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-197"><strong>Apmokestinama pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-198">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-199">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-200">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-201">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-202"><strong>PVM pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-203">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-204">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-205">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="923c8-206">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-207"><strong>PVM pirkimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-208">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-209">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-210">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="923c8-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="923c8-211">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-212"><strong>Apmokestinamas importas</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="923c8-213">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-214">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-215"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="923c8-216">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-217"><strong>Korespondentinis apmokėjimas už importą</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="923c8-218">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-219">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-220"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="923c8-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="923c8-221">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-222"><strong>Apmokestinama importo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-223">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-224">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="923c8-225">e</span><span class="sxs-lookup"><span data-stu-id="923c8-225">e</span></span><li><span data-ttu-id="923c8-226"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="923c8-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="923c8-227">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-228"><strong>Korespondentinio apmokėjimo už importą kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="923c8-229">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-230">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-231">Mokesčio kryptis yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="923c8-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="923c8-232">d</span><span class="sxs-lookup"><span data-stu-id="923c8-232">d</span></span><li><span data-ttu-id="923c8-233">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="923c8-234"><strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="923c8-235">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-236">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-237"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="923c8-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="923c8-238">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="923c8-239"><strong>Koresp. naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="923c8-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="923c8-240">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="923c8-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="923c8-241">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="923c8-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="923c8-242"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="923c8-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="923c8-243">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="923c8-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="923c8-244">Ankstesnėje lentelėje laikoma, kad toliau pateikti kriterijai yra patenkinami.</span><span class="sxs-lookup"><span data-stu-id="923c8-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="923c8-245">Mokesčių bazinė suma yra operacijos suma iš lauko **Pradinė suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="923c8-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="923c8-246">Mokesčių suma yra perėjimo suma iš lauko **Faktinė PVM suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="923c8-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="923c8-247">ER modelio ir ataskaitos formato konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="923c8-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="923c8-248">Galite naudoti elektronines ataskaitas (ER), kad sukonfigūruotumėte išrašus ir ataskaitas bei eksportuotumėte duomenis skirtingais elektroniniais formatais nekeisdami X++ kodo.</span><span class="sxs-lookup"><span data-stu-id="923c8-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="923c8-249">Papildoma informacija:</span><span class="sxs-lookup"><span data-stu-id="923c8-249">For additional information:</span></span>

-   [<span data-ttu-id="923c8-250">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="923c8-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="923c8-251">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="923c8-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="923c8-252">Lokalizavimo reikalavimai – GER konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="923c8-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="923c8-253">PVM išrašų konkrečiai šaliai būdingi ištekliai</span><span class="sxs-lookup"><span data-stu-id="923c8-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="923c8-254">Kiekvienos šalies PVM išrašas turi atitikti šalies teisės reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="923c8-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="923c8-255">Toliau pateiktoje lentelėje nurodytoms šalims priskiriami PVM išrašų iš anksto nustatyti bendrieji modeliai ir formatai.</span><span class="sxs-lookup"><span data-stu-id="923c8-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="923c8-256">Šalis</span><span class="sxs-lookup"><span data-stu-id="923c8-256">Country</span></span>        | <span data-ttu-id="923c8-257">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="923c8-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="923c8-258">Austrija</span><span class="sxs-lookup"><span data-stu-id="923c8-258">Austria</span></span>        |  [<span data-ttu-id="923c8-259">PVM išrašo informacija, skirta Austrijai</span><span class="sxs-lookup"><span data-stu-id="923c8-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="923c8-260">Belgija</span><span class="sxs-lookup"><span data-stu-id="923c8-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="923c8-261">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="923c8-261">Czech Republic</span></span> |  [<span data-ttu-id="923c8-262">PVM išrašo informacija, skirta Čekijos Respublikai</span><span class="sxs-lookup"><span data-stu-id="923c8-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="923c8-263">Estija</span><span class="sxs-lookup"><span data-stu-id="923c8-263">Estonia</span></span>        |  [<span data-ttu-id="923c8-264">PVM išrašo informacija, skirta Estijai</span><span class="sxs-lookup"><span data-stu-id="923c8-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="923c8-265">Suomija</span><span class="sxs-lookup"><span data-stu-id="923c8-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="923c8-266">Vokietija</span><span class="sxs-lookup"><span data-stu-id="923c8-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="923c8-267">Italija</span><span class="sxs-lookup"><span data-stu-id="923c8-267">Italy</span></span>          | [<span data-ttu-id="923c8-268">PVM išrašo informacija, skirta Italijai</span><span class="sxs-lookup"><span data-stu-id="923c8-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="923c8-269">Latvija</span><span class="sxs-lookup"><span data-stu-id="923c8-269">Latvia</span></span>         | [<span data-ttu-id="923c8-270">PVM išrašo informacija, skirta Latvijai</span><span class="sxs-lookup"><span data-stu-id="923c8-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="923c8-271">Lietuva</span><span class="sxs-lookup"><span data-stu-id="923c8-271">Lithuania</span></span>      | [<span data-ttu-id="923c8-272">PVM išrašo informacija, skirta Lietuvai</span><span class="sxs-lookup"><span data-stu-id="923c8-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="923c8-273">Olandija</span><span class="sxs-lookup"><span data-stu-id="923c8-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="923c8-274">Švedija</span><span class="sxs-lookup"><span data-stu-id="923c8-274">Sweden</span></span>         |                                                                                 |






