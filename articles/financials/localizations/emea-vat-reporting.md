---
title: PVM ataskaitos Europoje
description: Šioje temoje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo, skirto kai kurioms Europos šalims, nustatymą ir generavimą.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d3496e0dec51daa640ff80355b9bcc63f8ba7ea2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1513103"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="71e59-103">PVM ataskaitos Europoje</span><span class="sxs-lookup"><span data-stu-id="71e59-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71e59-104">Šioje temoje pateikiama bendra informacija apie pridėtinės vertės mokesčio (PVM) išrašo, skirto kai kurioms Europos šalims, nustatymą ir generavimą.</span><span class="sxs-lookup"><span data-stu-id="71e59-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="71e59-105">Šioje temoje pateikiamas bendras PVM išrašo nustatymo ir generavimo metodas.</span><span class="sxs-lookup"><span data-stu-id="71e59-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="71e59-106">Šį metodą gali bendrai naudoti vartotojai, kurių juridiniai subjektai yra toliau nurodytose šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="71e59-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="71e59-107">Austrija</span><span class="sxs-lookup"><span data-stu-id="71e59-107">Austria</span></span>
-   <span data-ttu-id="71e59-108">Belgija</span><span class="sxs-lookup"><span data-stu-id="71e59-108">Belgium</span></span>
-   <span data-ttu-id="71e59-109">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="71e59-109">Czech Republic</span></span>
-   <span data-ttu-id="71e59-110">Estija</span><span class="sxs-lookup"><span data-stu-id="71e59-110">Estonia</span></span>
-   <span data-ttu-id="71e59-111">Suomija</span><span class="sxs-lookup"><span data-stu-id="71e59-111">Finland</span></span>
-   <span data-ttu-id="71e59-112">Vokietija</span><span class="sxs-lookup"><span data-stu-id="71e59-112">Germany</span></span>
-   <span data-ttu-id="71e59-113">Latvija</span><span class="sxs-lookup"><span data-stu-id="71e59-113">Latvia</span></span>
-   <span data-ttu-id="71e59-114">Lietuva</span><span class="sxs-lookup"><span data-stu-id="71e59-114">Lithuania</span></span>
-   <span data-ttu-id="71e59-115">Olandija</span><span class="sxs-lookup"><span data-stu-id="71e59-115">Netherlands</span></span>
-   <span data-ttu-id="71e59-116">Švedija</span><span class="sxs-lookup"><span data-stu-id="71e59-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="71e59-117">PVM išrašo apžvalga</span><span class="sxs-lookup"><span data-stu-id="71e59-117">VAT statement overview</span></span>
<span data-ttu-id="71e59-118">PVM išrašas pagrįstas PVM operacijų sumomis.</span><span class="sxs-lookup"><span data-stu-id="71e59-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="71e59-119">PVM išrašo generavimo procesas yra PVM apmokėjimo proceso, kuris vykdomas naudojant funkciją Sudengti ir užregistruoti PVM, dalis.</span><span class="sxs-lookup"><span data-stu-id="71e59-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="71e59-120">Ši funkcija apskaičiuoja nurodyto laikotarpio PVM.</span><span class="sxs-lookup"><span data-stu-id="71e59-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="71e59-121">Sudengimo skaičiavimas apima mokesčio operacijos pasirinkto sudengimo laikotarpio užregistruotą PVM.</span><span class="sxs-lookup"><span data-stu-id="71e59-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="71e59-122">PVM išrašo duomenų skaičiavimo procesas pagrįstas ryšiu tarp PVM kodų ir PVM ataskaitų kodų, kai PVM ataskaitų kodai atitinka PVM išrašų langelius (arba XML žymes).</span><span class="sxs-lookup"><span data-stu-id="71e59-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="71e59-123">Reikia nustatyti kiekvieno PVM kodo kiekvieno operacijos tipo PVM ataskaitų kodus, pvz., kaip apmokestinamą pardavimą, apmokestinamus pirkimus, apmokestinamą importą.</span><span class="sxs-lookup"><span data-stu-id="71e59-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="71e59-124">Šio tipo operacijos aprašytos tolesniame šios temos skyriuje PVM ataskaitų PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="71e59-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="71e59-125">Reikia nustatyti kiekvieno PVM ataskaitų kodo konkretų ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="71e59-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="71e59-126">Tuo pat metu PVM kodai yra susiejami su konkrečiu PVM rinkėju per PVM sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="71e59-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="71e59-127">Reikia nustatyti kiekvieno PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="71e59-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="71e59-128">Todėl PVM kodo ataskaitos sąrankoje galima pasirinkti tik PVM ataskaitų kodus su tuo pačiu ataskaitos maketu, kuris nustatytas ir priskirtas PVM rinkėjui PVM kodo PVM sudengimo laikotarpiuose.</span><span class="sxs-lookup"><span data-stu-id="71e59-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="71e59-129">PVM operacija, sugeneruota užregistravus užsakymą arba žurnalą, apima PVM kodą, PVM šaltinį, PVM kryptį ir operacijos sumas (mokesčio bazinę sumą ir mokesčio sumą apskaitos valiuta, PVM valiuta ir operacijos valiuta).</span><span class="sxs-lookup"><span data-stu-id="71e59-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="71e59-130">Atsižvelgiant į mokesčio operacijos atributų derinį, operacijos sumos sudaro bendras PVM kodų nurodytų PVM ataskaitų kodų sumas.</span><span class="sxs-lookup"><span data-stu-id="71e59-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="71e59-131">Tolesnėje iliustracijoje pavaizduotas duomenų ryšys.</span><span class="sxs-lookup"><span data-stu-id="71e59-131">The following illustration shows the data relationship.</span></span>

![diagrama](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="71e59-133">PVM išrašo sąranka</span><span class="sxs-lookup"><span data-stu-id="71e59-133">VAT statement setup</span></span>
<span data-ttu-id="71e59-134">Norėdami generuoti PVM išrašą, turite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="71e59-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="71e59-135">PVM rinkėjų nustatymas PVM ataskaitoms teikti</span><span class="sxs-lookup"><span data-stu-id="71e59-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="71e59-136">Prieš nustatydami PVM ataskaitų kodus, turite pasirinkti tinkamą PVM rinkėjo ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="71e59-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="71e59-137">Puslapio **PVM rinkėjai** dalyje **Bendra** pasirinkite **Ataskaitos maketas**.</span><span class="sxs-lookup"><span data-stu-id="71e59-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="71e59-138">Šis maketas bus naudojamas nustatant PVM ataskaitų kodus.</span><span class="sxs-lookup"><span data-stu-id="71e59-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="71e59-139">PVM ataskaitų kodai</span><span class="sxs-lookup"><span data-stu-id="71e59-139">Sales tax reporting codes</span></span>

<span data-ttu-id="71e59-140">PVM ataskaitų kodai yra langelių kodai PVM išraše arba žymių pavadinimai XML formatu.</span><span class="sxs-lookup"><span data-stu-id="71e59-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="71e59-141">Šie kodai naudojami ataskaitos sumoms sujungti ir paruošti.</span><span class="sxs-lookup"><span data-stu-id="71e59-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="71e59-142">Kai konfigūruojate PVM išrašo elektroninių ataskaitų formatą, bus naudojami galutinių sumų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="71e59-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="71e59-143">PVM ataskaitų kodus galite kurti ir tvarkyti puslapyje **PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="71e59-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="71e59-144">Kiekvienam kodui turite priskirti ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="71e59-144">You must assign each code a report layout.</span></span> <span data-ttu-id="71e59-145">Sukūrę PVM ataskaitų kodus, galite kodus pasirinkti puslapio **PVM kodai** dalyje **Ataskaitų sąranka**.</span><span class="sxs-lookup"><span data-stu-id="71e59-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="71e59-146">PVM kodai, skirti PVM ataskaitos teikti</span><span class="sxs-lookup"><span data-stu-id="71e59-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="71e59-147"> PVM operacijų bazines sumas ir mokesčių sumas galima sujungti PVM išrašo ataskaitų koduose (XML žymės arba deklaracijos langeliai).</span><span class="sxs-lookup"><span data-stu-id="71e59-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="71e59-148">Tai galima nustatyti puslapyje <strong>PVM kodai</strong> susiejant PVM kodų skirtingų operacijų tipų PVM ataskaitų kodus.</span><span class="sxs-lookup"><span data-stu-id="71e59-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="71e59-149">Toliau pateikiamoje lentelėje aprašomi PVM kodų ataskaitų sąrankos operacijų tipai.</span><span class="sxs-lookup"><span data-stu-id="71e59-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="71e59-150">Skaičiuojant įtraukiamos visų šaltinių tipų, išskyrus PVM, operacijos.</span><span class="sxs-lookup"><span data-stu-id="71e59-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71e59-151"><strong>Operacijos tipas</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="71e59-152"><strong>Operacijų ir sumų, kurios bus apskaičiuotos, aprašas operacijos tipe</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-153"><strong>Apmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="71e59-154">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-155">Operacijos data patenka į pasirinktą laikotarpį/</span><span class="sxs-lookup"><span data-stu-id="71e59-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="71e59-156">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-157">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-158"><strong>Neapmokestinamas pardavimas</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="71e59-159">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-160">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-161">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="71e59-162">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-163"><strong>Mokėtinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="71e59-164">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-165">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-166">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-167">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-168"><strong>Apmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-169">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-170">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-171">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-172">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-173"><strong>Neapmokestinamo pardavimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-174">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-175">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-176">Pardavimas yra eksportas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pardavimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="71e59-177">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-178"><strong>PVM pardavimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-179">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-180">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-181">Pardavimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Mokėtinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-182">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-183"><strong>Apmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="71e59-184">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-185">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-186">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-187">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-188"><strong>Neapmokestinami pirkimai</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="71e59-189">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-190">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-191">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="71e59-192">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-193"><strong>Gautinas PVM</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="71e59-194">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-195">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-196">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-197">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-198"><strong>Apmokestinama pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-199">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-200">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-201">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-202">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-203"><strong>PVM pirkimo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-204">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-205">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-206">Pirkimas yra importas (<strong>Mokesčio kryptis</strong> yra <strong>Neapmokestinamas pirkimas</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="71e59-207">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-208"><strong>PVM pirkimo kredito pažymoje</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-209">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-210">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-211">Pirkimas yra vietinis (<strong>Mokesčio kryptis</strong> yra <strong>Gautinas PVM</strong>).</span><span class="sxs-lookup"><span data-stu-id="71e59-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="71e59-212">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-213"><strong>Apmokestinamas importas</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="71e59-214">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-215">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-216"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="71e59-217">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-218"><strong>Korespondentinis apmokėjimas už importą</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="71e59-219">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-220">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-221"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="71e59-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="71e59-222">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-223"><strong>Apmokestinama importo kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-224">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-225">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="71e59-226">e</span><span class="sxs-lookup"><span data-stu-id="71e59-226">e</span></span><li><span data-ttu-id="71e59-227"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="71e59-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="71e59-228">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-229"><strong>Korespondentinio apmokėjimo už importą kredito pažyma</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="71e59-230">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>bazinių mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-231">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-232">Mokesčio kryptis yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="71e59-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="71e59-233">d</span><span class="sxs-lookup"><span data-stu-id="71e59-233">d</span></span><li><span data-ttu-id="71e59-234">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71e59-235"><strong>Naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="71e59-236">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-237">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-238"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="71e59-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="71e59-239">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71e59-240"><strong>Koresp. naudojimo mokestis</strong></span><span class="sxs-lookup"><span data-stu-id="71e59-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="71e59-241">Mokesčių operacijų, kurios tekina toliau nurodytas sąlygas, <strong>mokesčių sumų</strong> atšaukta suma.</span><span class="sxs-lookup"><span data-stu-id="71e59-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="71e59-242">Operacijos data patenka į pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="71e59-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="71e59-243"><strong>Mokesčio kryptis</strong> yra <strong>Naudojimo mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="71e59-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="71e59-244">Operacijos <strong>Mokesčio bazinė suma</strong> arba <strong>Mokesčio suma</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="71e59-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="71e59-245">Ankstesnėje lentelėje laikoma, kad toliau pateikti kriterijai yra patenkinami.</span><span class="sxs-lookup"><span data-stu-id="71e59-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="71e59-246">Mokesčių bazinė suma yra operacijos suma iš lauko **Pradinė suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="71e59-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="71e59-247">Mokesčių suma yra perėjimo suma iš lauko **Faktinė PVM suma apskaitos valiuta**.</span><span class="sxs-lookup"><span data-stu-id="71e59-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="71e59-248">ER modelio ir ataskaitos formato konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="71e59-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="71e59-249">Galite naudoti elektronines ataskaitas (ER), kad sukonfigūruotumėte išrašus ir ataskaitas bei eksportuotumėte duomenis skirtingais elektroniniais formatais nekeisdami X++ kodo.</span><span class="sxs-lookup"><span data-stu-id="71e59-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="71e59-250">Papildoma informacija:</span><span class="sxs-lookup"><span data-stu-id="71e59-250">For additional information:</span></span>

-   [<span data-ttu-id="71e59-251">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="71e59-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="71e59-252">Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="71e59-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="71e59-253">Lokalizavimo reikalavimai – GER konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="71e59-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="71e59-254">PVM išrašų konkrečiai šaliai būdingi ištekliai</span><span class="sxs-lookup"><span data-stu-id="71e59-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="71e59-255">Kiekvienos šalies PVM išrašas turi atitikti šalies teisės reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="71e59-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="71e59-256">Toliau pateiktoje lentelėje nurodytoms šalims priskiriami PVM išrašų iš anksto nustatyti bendrieji modeliai ir formatai.</span><span class="sxs-lookup"><span data-stu-id="71e59-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="71e59-257">Šalis</span><span class="sxs-lookup"><span data-stu-id="71e59-257">Country</span></span>        | <span data-ttu-id="71e59-258">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="71e59-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="71e59-259">Austrija</span><span class="sxs-lookup"><span data-stu-id="71e59-259">Austria</span></span>        |  [<span data-ttu-id="71e59-260">PVM išrašo informacija, skirta Austrijai</span><span class="sxs-lookup"><span data-stu-id="71e59-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="71e59-261">Belgija</span><span class="sxs-lookup"><span data-stu-id="71e59-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="71e59-262">Čekijos Respublika</span><span class="sxs-lookup"><span data-stu-id="71e59-262">Czech Republic</span></span> |  [<span data-ttu-id="71e59-263">PVM išrašo informacija, skirta Čekijos Respublikai</span><span class="sxs-lookup"><span data-stu-id="71e59-263">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="71e59-264">Estija</span><span class="sxs-lookup"><span data-stu-id="71e59-264">Estonia</span></span>        |  [<span data-ttu-id="71e59-265">PVM išrašo informacija, skirta Estijai</span><span class="sxs-lookup"><span data-stu-id="71e59-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="71e59-266">Suomija</span><span class="sxs-lookup"><span data-stu-id="71e59-266">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="71e59-267">Vokietija</span><span class="sxs-lookup"><span data-stu-id="71e59-267">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="71e59-268">Italija</span><span class="sxs-lookup"><span data-stu-id="71e59-268">Italy</span></span>          | [<span data-ttu-id="71e59-269">PVM išrašo informacija, skirta Italijai</span><span class="sxs-lookup"><span data-stu-id="71e59-269">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="71e59-270">Latvija</span><span class="sxs-lookup"><span data-stu-id="71e59-270">Latvia</span></span>         | [<span data-ttu-id="71e59-271">PVM išrašo informacija, skirta Latvijai</span><span class="sxs-lookup"><span data-stu-id="71e59-271">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="71e59-272">Lietuva</span><span class="sxs-lookup"><span data-stu-id="71e59-272">Lithuania</span></span>      | [<span data-ttu-id="71e59-273">PVM išrašo informacija, skirta Lietuvai</span><span class="sxs-lookup"><span data-stu-id="71e59-273">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="71e59-274">Olandija</span><span class="sxs-lookup"><span data-stu-id="71e59-274">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="71e59-275">Švedija</span><span class="sxs-lookup"><span data-stu-id="71e59-275">Sweden</span></span>         |                                                                                 |





