---
title: "Tiekėjų registravimo šablonai"
description: "Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bf37ff484323fb05a35419889f2f89ab124fb27
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="c35a9-103">Tiekėjų registravimo šablonai</span><span class="sxs-lookup"><span data-stu-id="c35a9-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c35a9-104">Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK.</span><span class="sxs-lookup"><span data-stu-id="c35a9-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="c35a9-105">Tiekėjų registravimo šablonai</span><span class="sxs-lookup"><span data-stu-id="c35a9-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="c35a9-106">Tiekėjų registravimo profiliai leidžia DK sąskaitas ir dokumentų nuostatas priskirti visiems tiekėjams, tiekėjų grupei arba vienam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="c35a9-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="c35a9-107">Šios nuostatos bus naudojamos kuriant pirkimo užsakymus, tiekėjo SF ir mokėjimus grynaisiais pinigais.</span><span class="sxs-lookup"><span data-stu-id="c35a9-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="c35a9-108">Kai kurių operacijų registravimo profilį galite pasirinkti tokį, kuris skiriasi nuo šiame puslapyje operacijoms nustatytų registravimo profilių ir yra už juos svarbesnis.</span><span class="sxs-lookup"><span data-stu-id="c35a9-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="c35a9-109">Numatytasis registravimo profilis apibrėžiamas „FastTab‟ DK ir PVM, esančiuose Mokėtinų sumų parametrų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c35a9-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="c35a9-110">Numatytasis registravimo profilis tada automatiškai įtraukiamas naujų dokumentų antraštėje, kur prireikus jį galite pakeisti kitu registravimo profiliu.</span><span class="sxs-lookup"><span data-stu-id="c35a9-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="c35a9-111">Registravimo apibrėžčių puslapyje taip pat galite registravimo apibrėžtis susieti su operacijų registravimo tipais.</span><span class="sxs-lookup"><span data-stu-id="c35a9-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="c35a9-112">Tiekėjų operacijų registravimą į DK kontroliuoja registravimo apibrėžtys, o ne registravimo profiliai.</span><span class="sxs-lookup"><span data-stu-id="c35a9-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="c35a9-113">Registravimo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="c35a9-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="c35a9-114">**Nustatymas**</span><span class="sxs-lookup"><span data-stu-id="c35a9-114">**Setup**</span></span>

<span data-ttu-id="c35a9-115">Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį.</span><span class="sxs-lookup"><span data-stu-id="c35a9-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="c35a9-116">Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį.</span><span class="sxs-lookup"><span data-stu-id="c35a9-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="c35a9-117">Registruojant, tinkamiausias kiekvienos operacijos registravimo profilis randamas pagal toliau nurodytus prioritetus ieškant konkrečiausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.</span><span class="sxs-lookup"><span data-stu-id="c35a9-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="c35a9-118">**Sąskaitos kodo** lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c35a9-118">**Account code** field value</span></span> | <span data-ttu-id="c35a9-119">**Sąskaitos / grupės numerio** lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c35a9-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="c35a9-120">Ieškos prioritetas</span><span class="sxs-lookup"><span data-stu-id="c35a9-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="c35a9-121">**Lentelė**</span><span class="sxs-lookup"><span data-stu-id="c35a9-121">**Table**</span></span>                    | <span data-ttu-id="c35a9-122">Konkreti tiekėjo sąskaita</span><span class="sxs-lookup"><span data-stu-id="c35a9-122">Specific vendor account</span></span>                     | <span data-ttu-id="c35a9-123">1</span><span class="sxs-lookup"><span data-stu-id="c35a9-123">1</span></span>               |
| <span data-ttu-id="c35a9-124">**Grupė**</span><span class="sxs-lookup"><span data-stu-id="c35a9-124">**Group**</span></span>                    | <span data-ttu-id="c35a9-125">tiekėjų grupė, priskirta tiekėjui</span><span class="sxs-lookup"><span data-stu-id="c35a9-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="c35a9-126">2</span><span class="sxs-lookup"><span data-stu-id="c35a9-126">2</span></span>               |
| <span data-ttu-id="c35a9-127">**Visi**</span><span class="sxs-lookup"><span data-stu-id="c35a9-127">**All**</span></span>                      | <span data-ttu-id="c35a9-128">Tuščias</span><span class="sxs-lookup"><span data-stu-id="c35a9-128">Blank</span></span>                                       | <span data-ttu-id="c35a9-129">3</span><span class="sxs-lookup"><span data-stu-id="c35a9-129">3</span></span>               |

<span data-ttu-id="c35a9-130">Jei norite, kad visų tiekėjo operacijų registravimo profilis būtų tas pats, Sąskaitos kodo lauke nustatykite tik vieną registravimo profilį – Visi.</span><span class="sxs-lookup"><span data-stu-id="c35a9-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="c35a9-131">Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c35a9-131">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c35a9-132">Laukas</span><span class="sxs-lookup"><span data-stu-id="c35a9-132">Field</span></span></th>
<th><span data-ttu-id="c35a9-133">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c35a9-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c35a9-134"><strong>Registravimo šablonas</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="c35a9-135">Įveskite registravimo šablono kodą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="c35a9-136">Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą tiekėjo balansams nacionaline valiuta ir kitą – tiekėjo balansams užsienio valiuta.</span><span class="sxs-lookup"><span data-stu-id="c35a9-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="c35a9-137">Vieną sąskaitą galite pavadinti Nacionalinė, kitą – Užsienio.</span><span class="sxs-lookup"><span data-stu-id="c35a9-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c35a9-138"><strong>Aprašymas</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="c35a9-139">Įveskite registravimo profilio aprašą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c35a9-140"><strong>Sąskaitos kodas</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="c35a9-141">Nurodykite, ar registravimo profilis taikomas konkrečiam tiekėjui, tiekėjų grupei ar visiems tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="c35a9-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="c35a9-142"><strong>Lentelė</strong> – registravimo profilis taikomas vienam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="c35a9-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="c35a9-143">Sąskaitos / grupės numerio lauke pasirinkite tiekėjo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="c35a9-144"><strong>Grupė</strong> – registravimo profilis taikomas tiekėjų grupei.</span><span class="sxs-lookup"><span data-stu-id="c35a9-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="c35a9-145">Sąskaitos / grupės numerio lauke pasirinkite tiekėjų grupę.</span><span class="sxs-lookup"><span data-stu-id="c35a9-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="c35a9-146"><strong>Visi</strong> – registravimo profilis taikomas visiems tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="c35a9-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="c35a9-147">Sąskaitos / grupės numerio lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="c35a9-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c35a9-148"><strong>Sąskaitos/grupės Nr.</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="c35a9-149">Jei lauke Sąskaitos kodas pasirinkta Lentelė, pasirinkite tiekėjo, kuris yra susietas su registravimo profiliu, sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="c35a9-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="c35a9-150">Jei pasirinkta Grupė, pasirinkite tiekėjų grupę.</span><span class="sxs-lookup"><span data-stu-id="c35a9-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="c35a9-151">Jei pasirinkta Visi, šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="c35a9-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c35a9-152"><strong>Suminė sąskaita</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="c35a9-153">Pasirinkite DK sąskaitą, kuri bus naudojama kaip tiekėjų, su kuriais susijęs registravimo profilis, suminę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c35a9-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:</span><span class="sxs-lookup"><span data-stu-id="c35a9-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="c35a9-155"><strong>Pastaba</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c35a9-156">Jei DK parametrų puslapyje pasirinktas perjungiklis Naudoti registravimo apibrėžtis, vietoj suminės sąskaitos naudojama tiekėjų SF operacijų registravimo apibrėžtis.</span><span class="sxs-lookup"><span data-stu-id="c35a9-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c35a9-157"><strong>Sudengimo sąskaita</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="c35a9-158">Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms.</span><span class="sxs-lookup"><span data-stu-id="c35a9-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="c35a9-159">Šį lauką galima naudoti tik kai įgalintas pinigų srauto prognozavimas.</span><span class="sxs-lookup"><span data-stu-id="c35a9-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c35a9-160"><strong>PVM išankstinai apmokėjimai</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="c35a9-161">Pasirinkite PVM mokėjimų, gaunamų iš anksto, sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c35a9-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:</span><span class="sxs-lookup"><span data-stu-id="c35a9-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="c35a9-163"><strong>Pastaba</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c35a9-164">Registravimo profilis, naudojamas, kai mokėjimas pažymimas kaip išankstinis mokėjimas, pasirenkamas lauke Registravimo profilis su išankstinio mokėjimo žurnalo kvitu, esančiame Mokėtinų sumų parametrų puslapio srityje DK ir PVM.</span><span class="sxs-lookup"><span data-stu-id="c35a9-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c35a9-165"><strong>Atvykimas</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="c35a9-166">Pasirinkite DK sąskaitą, kurioje bus registruojama informacija apie nepatvirtintas tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="c35a9-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="c35a9-167">Informacija įvedama į SF registro žurnalą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="c35a9-168">Pavyzdžiui, gavus SF SF registre, naudotojas apie tiekėjo SF įveda labai bendrą informaciją.</span><span class="sxs-lookup"><span data-stu-id="c35a9-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="c35a9-169">Užregistravus SF registrą, operacijos registruojamos sąskaitoje, kuri įvesta čia ir lauke Korespondentinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="c35a9-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="c35a9-170">Patvirtinus SF, skola perkeliama iš sąskaitos Gavimas į tiekėjo suminę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c35a9-171"><strong>Koresp. sąskaita</strong></span><span class="sxs-lookup"><span data-stu-id="c35a9-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="c35a9-172">Pasirinkite DK sąskaitą, kuri naudojama norint padengti nepatvirtintas tiekėjo SF, kurios atnaujinamos naudojant SF registrą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="c35a9-173">Korespondentinė sąskaita veikia kaip gavimo sąskaitose užregistruotų operacijų korespondentinė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="c35a9-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="c35a9-174">Todėl sąskaitoje yra tiekėjo pirkimų, kurie dar nepatvirtinti.</span><span class="sxs-lookup"><span data-stu-id="c35a9-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="c35a9-175">**Lentelių apribojimai**</span><span class="sxs-lookup"><span data-stu-id="c35a9-175">**Table restrictions**</span></span>

<span data-ttu-id="c35a9-176">Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="c35a9-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="c35a9-177">Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.</span><span class="sxs-lookup"><span data-stu-id="c35a9-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="c35a9-178">Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c35a9-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="c35a9-179">Laukas</span><span class="sxs-lookup"><span data-stu-id="c35a9-179">Field</span></span>          | <span data-ttu-id="c35a9-180">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c35a9-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c35a9-181">**Sudengimas**</span><span class="sxs-lookup"><span data-stu-id="c35a9-181">**Settlement**</span></span> | <span data-ttu-id="c35a9-182">Pasirinkite šią parinktį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą.</span><span class="sxs-lookup"><span data-stu-id="c35a9-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="c35a9-183">Jei ši parinktis atžymėta, sudengti operacijas turite rankiniu būdu, naudodami puslapį Sudengti atidarytas operacijas.</span><span class="sxs-lookup"><span data-stu-id="c35a9-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="c35a9-184">**Atšaukti**</span><span class="sxs-lookup"><span data-stu-id="c35a9-184">**Cancel**</span></span>     | <span data-ttu-id="c35a9-185">Pasirinkite šią parinktį, jei norite atšaukti operacijas, kurių registravimo profilis yra šis.</span><span class="sxs-lookup"><span data-stu-id="c35a9-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="c35a9-186">**Uždaryti**</span><span class="sxs-lookup"><span data-stu-id="c35a9-186">**Close**</span></span>      | <span data-ttu-id="c35a9-187">Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos.</span><span class="sxs-lookup"><span data-stu-id="c35a9-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="c35a9-188">Operacija laikoma uždaryta, kai ji yra visiškai sudengta.</span><span class="sxs-lookup"><span data-stu-id="c35a9-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






