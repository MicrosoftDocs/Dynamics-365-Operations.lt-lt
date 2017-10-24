---
title: "Kliento registravimo šablonai"
description: "Pagal kliento registravimo šablonus valdomas klientų operacijų registravimas į DK."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da750645612c2a0a7650edfd933d707618d9f9ce
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="76662-103">Kliento registravimo šablonai</span><span class="sxs-lookup"><span data-stu-id="76662-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76662-104">Pagal kliento registravimo šablonus valdomas klientų operacijų registravimas į DK.</span><span class="sxs-lookup"><span data-stu-id="76662-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="76662-105">Kliento registravimo šablonai</span><span class="sxs-lookup"><span data-stu-id="76662-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="76662-106">Klientų registravimo profiliai leidžia DK sąskaitas ir dokumentų nuostatas priskirti visiems klientams, klientų grupei arba vienam klientui.</span><span class="sxs-lookup"><span data-stu-id="76662-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="76662-107">Šios nuostatos bus naudojamos kuriant pardavimo užsakymus, laisvos formos SF, mokėjimus grynaisiais pinigais, priminimo laiškus ir delspinigių pažymas.</span><span class="sxs-lookup"><span data-stu-id="76662-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="76662-108">Kai kurių operacijų registravimo šabloną galite pasirinkti tokį, kuris skiriasi nuo šiame puslapyje operacijoms nustatytų registravimo profilių ir yra už juos svarbesnis.</span><span class="sxs-lookup"><span data-stu-id="76662-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="76662-109">Numatytasis registravimo profilis apibrėžiamas „FastTab‟ DK ir PVM, esančiuose Gautinų sumų parametrų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="76662-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="76662-110">Numatytasis registravimo profilis tada automatiškai įtraukiamas naujų dokumentų antraštėje, kur prireikus jį galite pakeisti kitu registravimo profiliu.</span><span class="sxs-lookup"><span data-stu-id="76662-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="76662-111">Registravimo apibrėžčių puslapyje taip pat galite registravimo apibrėžtis susieti su operacijų registravimo tipais.</span><span class="sxs-lookup"><span data-stu-id="76662-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="76662-112">Klientų operacijų registravimą į DK kontroliuoja registravimo apibrėžtys, o ne registravimo profiliai.</span><span class="sxs-lookup"><span data-stu-id="76662-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="76662-113">Registravimo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="76662-113">Creating a posting profile</span></span>
<span data-ttu-id="76662-114">Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį.</span><span class="sxs-lookup"><span data-stu-id="76662-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="76662-115">Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį.</span><span class="sxs-lookup"><span data-stu-id="76662-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="76662-116">Registruojant, tinkamiausias kiekvienos operacijos registravimo profilis randamas pagal toliau nurodytus prioritetus ieškant konkrečiausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.</span><span class="sxs-lookup"><span data-stu-id="76662-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="76662-117">**Sąskaitos kodo** lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="76662-117">**Account code** field value</span></span> | <span data-ttu-id="76662-118">**Sąskaitos / grupės numerio** lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="76662-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="76662-119">Ieškos prioritetas</span><span class="sxs-lookup"><span data-stu-id="76662-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="76662-120">**Lentelė**</span><span class="sxs-lookup"><span data-stu-id="76662-120">**Table**</span></span>                    | <span data-ttu-id="76662-121">Konkretus kliento kodas</span><span class="sxs-lookup"><span data-stu-id="76662-121">Specific customer account</span></span>                       | <span data-ttu-id="76662-122">1</span><span class="sxs-lookup"><span data-stu-id="76662-122">1</span></span>               |
| <span data-ttu-id="76662-123">**Grupė**</span><span class="sxs-lookup"><span data-stu-id="76662-123">**Group**</span></span>                    | <span data-ttu-id="76662-124">Klientų grupė, priskiriama klientui.</span><span class="sxs-lookup"><span data-stu-id="76662-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="76662-125">2</span><span class="sxs-lookup"><span data-stu-id="76662-125">2</span></span>               |
| <span data-ttu-id="76662-126">**Visi**</span><span class="sxs-lookup"><span data-stu-id="76662-126">**All**</span></span>                      | <span data-ttu-id="76662-127">Tuščias</span><span class="sxs-lookup"><span data-stu-id="76662-127">Blank</span></span>                                           | <span data-ttu-id="76662-128">3</span><span class="sxs-lookup"><span data-stu-id="76662-128">3</span></span>               |

<span data-ttu-id="76662-129">Jei norite, kad visų kliento operacijų registravimo profilis būtų tas pats, Sąskaitos kodo lauke nustatykite tik vieną registravimo profilį – Visi.</span><span class="sxs-lookup"><span data-stu-id="76662-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="76662-130">Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="76662-130">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76662-131">Laukas</span><span class="sxs-lookup"><span data-stu-id="76662-131">Field</span></span></th>
<th><span data-ttu-id="76662-132">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="76662-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76662-133"><strong>Registravimo šablonas</strong></span><span class="sxs-lookup"><span data-stu-id="76662-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="76662-134">Įveskite registravimo šablono kodą.</span><span class="sxs-lookup"><span data-stu-id="76662-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="76662-135">Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą kliento balansams nacionaline valiuta ir kitą – kliento balansams užsienio valiuta.</span><span class="sxs-lookup"><span data-stu-id="76662-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="76662-136">Vieną sąskaitą galite pavadinti Nacionalinė, kitą – Užsienio.</span><span class="sxs-lookup"><span data-stu-id="76662-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76662-137"><strong>Aprašymas</strong></span><span class="sxs-lookup"><span data-stu-id="76662-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="76662-138">Įveskite registravimo profilio aprašą.</span><span class="sxs-lookup"><span data-stu-id="76662-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="76662-139">Jis naudojamas tik tada, kai, registravimo profilį peržiūrint šiame puslapyje, norima jį geriau identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="76662-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76662-140"><strong>Sąskaitos kodas</strong></span><span class="sxs-lookup"><span data-stu-id="76662-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="76662-141">Pasirinkite, ar registravimo profilis bus taikomas atskiram klientui, klientų grupei, ar visiems klientams.</span><span class="sxs-lookup"><span data-stu-id="76662-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="76662-142"><strong>Lentelė</strong> – registravimo profilis taikomas vienam klientui.</span><span class="sxs-lookup"><span data-stu-id="76662-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="76662-143">Sąskaitos / grupės numerio lauke pasirinkite kliento sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="76662-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="76662-144"><strong>Grupė</strong> – registravimo profilis taikomas klientų grupei.</span><span class="sxs-lookup"><span data-stu-id="76662-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="76662-145">Sąskaitos / grupės numerio lauke pasirinkite klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="76662-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="76662-146"><strong>Visi</strong> – registravimo profilis taikomas visiems klientams.</span><span class="sxs-lookup"><span data-stu-id="76662-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="76662-147">Sąskaitos / grupės numerio lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="76662-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76662-148"><strong>Sąskaitos/grupės Nr.</strong></span><span class="sxs-lookup"><span data-stu-id="76662-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="76662-149">Jei lauke Sąskaitos kodas pasirinkta Lentelė, pasirinkite kliento, kuris yra susietas su registravimo profiliu, sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="76662-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="76662-150">Jei pasirinkta Grupė, pasirinkite klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="76662-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="76662-151">Jei pasirinkta Visi, šį lauką palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="76662-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76662-152"><strong>Suminė sąskaita</strong></span><span class="sxs-lookup"><span data-stu-id="76662-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="76662-153">Pasirinkite DK sąskaitą, kuri bus naudojama kaip klientų, kurie susieti su registravimo profiliu, suminė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="76662-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76662-154"><strong>Sudengimo sąskaita</strong></span><span class="sxs-lookup"><span data-stu-id="76662-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="76662-155">Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms.</span><span class="sxs-lookup"><span data-stu-id="76662-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="76662-156">Šis laukas bus rodomi tik įgalinus pinigų srauto prognozes.</span><span class="sxs-lookup"><span data-stu-id="76662-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76662-157"><strong>PVM išankstinai apmokėjimai</strong></span><span class="sxs-lookup"><span data-stu-id="76662-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="76662-158">Pasirinkite mokėjimų, gaunamų iš anksto, PVM sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="76662-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76662-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:</span><span class="sxs-lookup"><span data-stu-id="76662-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="76662-160"><strong>Pastaba</strong></span><span class="sxs-lookup"><span data-stu-id="76662-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76662-161">Naudokite Gautinų sumų parametrų puslapį, norėdami nurodyti registravimo profilį, naudotiną, kai mokėjimas pažymimas kaip išankstinis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="76662-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76662-162"><strong>Nuolaidų sąskaitos skolos</strong></span><span class="sxs-lookup"><span data-stu-id="76662-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="76662-163">Pasirinkite DK sąskaitą, skirtą nuolaidų įsipareigojimams.</span><span class="sxs-lookup"><span data-stu-id="76662-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76662-164"><strong>Priminimo laiškų seka</strong></span><span class="sxs-lookup"><span data-stu-id="76662-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="76662-165">Pasirinkite priminimo laiškų sekos identifikatorių, naudotiną su klientais, kuriems priskirtas registravimo profilis.</span><span class="sxs-lookup"><span data-stu-id="76662-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76662-166"><strong>Palūkanų kodas</strong></span><span class="sxs-lookup"><span data-stu-id="76662-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="76662-167">Pasirinkite delspinigių kodą, naudotiną skaičiuojant delspinigius klientams, kuriems priskirtas registravimo profilis.</span><span class="sxs-lookup"><span data-stu-id="76662-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="76662-168">**Lentelių apribojimai**</span><span class="sxs-lookup"><span data-stu-id="76662-168">**Table restrictions**</span></span>

<span data-ttu-id="76662-169">Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="76662-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="76662-170">Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.</span><span class="sxs-lookup"><span data-stu-id="76662-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="76662-171">Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="76662-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="76662-172">Laukas</span><span class="sxs-lookup"><span data-stu-id="76662-172">Field</span></span>                 | <span data-ttu-id="76662-173">Prekės/Paslaugos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="76662-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76662-174">**Sudengimas**</span><span class="sxs-lookup"><span data-stu-id="76662-174">**Settlement**</span></span>        | <span data-ttu-id="76662-175">Pasirinkite šį perjungiklį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą.</span><span class="sxs-lookup"><span data-stu-id="76662-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="76662-176">Jei šis perjungiklis atžymėtas, sudengti operacijas turite rankiniu būdu, naudodami puslapį Sudengti atidarytas operacijas arba puslapį Įvesti klientų mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="76662-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="76662-177">**Pomėgiai**</span><span class="sxs-lookup"><span data-stu-id="76662-177">**Interest**</span></span>          | <span data-ttu-id="76662-178">Pasirinkite šį perjungiklį, jei turėtų būti skaičiuojami klientų sąskaitų, naudojančių šį profilį, nesumokėtų balansų delspinigiai.</span><span class="sxs-lookup"><span data-stu-id="76662-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="76662-179">Jei šis perjungiklis nepažymėtas, šiems klientams delspinigiai nebus skaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="76662-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="76662-180">**Priminimo laiškas**</span><span class="sxs-lookup"><span data-stu-id="76662-180">**Collection letter**</span></span> | <span data-ttu-id="76662-181">Pasirinkite šį perjungiklį, jei turėtų būti generuojami klientų sąskaitų, naudojančių šį profilį, priminimo laiškai.</span><span class="sxs-lookup"><span data-stu-id="76662-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="76662-182">Jei šis perjungiklis nepažymėtas, šiems klientams priminimo laiškai nebus generuojami.</span><span class="sxs-lookup"><span data-stu-id="76662-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="76662-183">**Uždaryti**</span><span class="sxs-lookup"><span data-stu-id="76662-183">**Close**</span></span>             | <span data-ttu-id="76662-184">Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos.</span><span class="sxs-lookup"><span data-stu-id="76662-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="76662-185">Operacija laikoma uždaryta, kai ji yra visiškai sudengta.</span><span class="sxs-lookup"><span data-stu-id="76662-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="76662-186">Daugiau informacijos žr. [Kliento mokėjimų apžvalga](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="76662-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


