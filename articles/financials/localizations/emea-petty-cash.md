---
title: Smulkios išlaidos (skirta Rytų Europai)
description: Šioje temoje pateikiama informacija apie smulkių išlaidų funkciją, kuri vartotojams Estijoje, Lietuvoje, Čekijos Respublikoje,Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje suteikia galimybę sistemoje nurodyti grynųjų pinigų operacijas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 07be1241bd971ed1823e38e094451304c0fa59a7
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538128"
---
# <a name="petty-cash-for-eastern-europe"></a><span data-ttu-id="67397-103">Smulkios išlaidos (skirta Rytų Europai)</span><span class="sxs-lookup"><span data-stu-id="67397-103">Petty cash for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67397-104">Šioje temoje pateikiama informacija apie smulkių išlaidų funkciją, kuri vartotojams Estijoje, Lietuvoje, Čekijos Respublikoje,Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje suteikia galimybę sistemoje nurodyti grynųjų pinigų operacijas.</span><span class="sxs-lookup"><span data-stu-id="67397-104">This topic provides information about the petty cash functionality that lets users in Estonia, Lithuania, Czech Republic, Hungary, Latvia, Poland, and Russia reflect cash operations in the system.</span></span>

<span data-ttu-id="67397-105">Smulkių išlaidų funkciją galite naudoti norėdami automatizuoti grynųjų pinigų gavimo ir išlaidų operacijas, pirminių dokumentų kūrimą ir susijusių ataskaitų spausdinimą.</span><span class="sxs-lookup"><span data-stu-id="67397-105">You can use the petty cash functionality to automate operations for receipts and expenditures of cash, the creation of primary documents, and the printing of related reports.</span></span> <span data-ttu-id="67397-106">Smulkių išlaidų funkcija suteikia galimybę atlikti toliau nurodytas operacijas.</span><span class="sxs-lookup"><span data-stu-id="67397-106">The petty cash functionality lets you perform the following operations:</span></span>

-   <span data-ttu-id="67397-107">Sukurti turimo grynųjų pinigų turto gavimo iš išlaidų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-107">Account the receipt and expenditure of available cash assets.</span></span>
-   <span data-ttu-id="67397-108">Generuoti tipines grynųjų pinigų formas: grynųjų pinigų kompensacijos kvitus, grynųjų pinigų išmokėjimo kvitus ir grynųjų pinigų kvitų registracijos žurnalą.</span><span class="sxs-lookup"><span data-stu-id="67397-108">Generate typical cash forms: Cash reimbursement slips, Cash disbursement slips, and a Journal of registration for cash slips.</span></span>
-   <span data-ttu-id="67397-109">Valdyti didžiausią grynųjų pinigų sumą, leidžiamą atliekant operacijas su klientais, tiekėjais ir t. t.</span><span class="sxs-lookup"><span data-stu-id="67397-109">Control the maximum cash amount that is allowed for operations with customers, vendors, and so on.</span></span>
-   <span data-ttu-id="67397-110">Sistemoje nurodyti grynųjų pinigų operacijas įvairiomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="67397-110">Reflect cash operations in various currencies in the system.</span></span>
-   <span data-ttu-id="67397-111">Konvertuoti grynųjų pinigų operacijų sumas užsienio valiuta į numatytąją valiutą ir pateikti apskaitos ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="67397-111">Convert the amounts of cash operations in foreign currency to the default currency to provide accounting reporting.</span></span>
-   <span data-ttu-id="67397-112">Generuoti **kasos knygos** ir kasininko darbo ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="67397-112">Generate a **Cash book** report and a cashier’s report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="67397-113">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="67397-113">Prerequisites</span></span>
<span data-ttu-id="67397-114">Norėdami naudoti smulkių išlaidų funkciją, turite atlikti toliau nurodytas būtinas užduotis.</span><span class="sxs-lookup"><span data-stu-id="67397-114">Before you can use the petty cash functionality, you must complete the following prerequisites:</span></span>

-   <span data-ttu-id="67397-115">Nustatyti grynųjų pinigų sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="67397-115">Set up cash accounts.</span></span>
-   <span data-ttu-id="67397-116">Nustatyti grynųjų pinigų registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="67397-116">Set up cash posting profiles.</span></span>
-   <span data-ttu-id="67397-117">Nustatyti grynųjų pinigų dokumentų numeravimo numeracijas.</span><span class="sxs-lookup"><span data-stu-id="67397-117">Set up number sequences for cash document numbering.</span></span>
-   <span data-ttu-id="67397-118">Nustatyti grynųjų pinigų ir banko valdymo parametrų numatytąsias vertes.</span><span class="sxs-lookup"><span data-stu-id="67397-118">Set up default values for Cash and bank management parameters.</span></span>
-   <span data-ttu-id="67397-119">Nustatyti grynųjų pinigų žurnalų pavadinimus DK.</span><span class="sxs-lookup"><span data-stu-id="67397-119">Set up cash journal names in General ledger.</span></span>

### <a name="set-up-cash-accounts"></a><span data-ttu-id="67397-120">Nustatyti grynųjų pinigų sąskaitas</span><span class="sxs-lookup"><span data-stu-id="67397-120">Set up cash accounts</span></span>

<span data-ttu-id="67397-121">Norėdami nustatyti grynųjų pinigų sąskaitą, atidarykite **Grynųjų pinigų valdymas** &gt; **Banko sąskaitos** &gt; **Grynųjų pinigų sąskaitos** ir įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-121">To set up a Cash, open **Cash and bank management** &gt; **Bank accounts** &gt; **Cash accounts**, and enter the following information.</span></span>

| <span data-ttu-id="67397-122">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-122">Field</span></span>                 | <span data-ttu-id="67397-123">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-123">Description</span></span>                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67397-124">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="67397-124">Cash</span></span>                  | <span data-ttu-id="67397-125">Įveskite kodą grynųjų pinigų sąskaitai (grynieji pinigai) identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="67397-125">Enter a code to identify the cash account (cash).</span></span>                                                                    |
| <span data-ttu-id="67397-126">Vardas</span><span class="sxs-lookup"><span data-stu-id="67397-126">Name</span></span>                  | <span data-ttu-id="67397-127">Įveskite grynųjų pinigų sąskaitos aprašą.</span><span class="sxs-lookup"><span data-stu-id="67397-127">Enter a description of the cash account.</span></span>                                                                             |
| <span data-ttu-id="67397-128">Valiuta</span><span class="sxs-lookup"><span data-stu-id="67397-128">Currency</span></span>              | <span data-ttu-id="67397-129">Pasirinkite grynųjų pinigų operacijų numatytosios valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-129">Select the default currency code for cash transactions.</span></span>                                                              |
| <span data-ttu-id="67397-130">Numeracijų grupė</span><span class="sxs-lookup"><span data-stu-id="67397-130">Number sequence group</span></span> | <span data-ttu-id="67397-131">Jei grynųjų pinigų dokumentų numeravimas turi skirtis nuo parametruose nurodyto numeravimo, įveskite kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-131">If the numbering of cash documents must differ from the numbering that is specified in the parameters, enter a code.</span></span> |
| <span data-ttu-id="67397-132">Daugiau valiutų</span><span class="sxs-lookup"><span data-stu-id="67397-132">More currencies</span></span>       | <span data-ttu-id="67397-133">Pažymėkite šį žymės langelį, norėdami leisti registruoti valiutas, kurios skiriasi nuo apskaitos valiutos.</span><span class="sxs-lookup"><span data-stu-id="67397-133">Select this check box to allow currencies that differ from the accounting currency to be posted.</span></span>                     |
| <span data-ttu-id="67397-134">Neigiami grynieji</span><span class="sxs-lookup"><span data-stu-id="67397-134">Negative cash</span></span>         | <span data-ttu-id="67397-135">Pažymėkite šį žymės langelį, norėdami leisti neigiamus balansus bet kokia valiuta.</span><span class="sxs-lookup"><span data-stu-id="67397-135">Select this check box to allow negative cash balances in any currency.</span></span>                                               |

<span data-ttu-id="67397-136">Norėdami nustatyti grynųjų pinigų sąskaitos grynųjų pinigų balanso kontrolės taisykles, nustatykite grynųjų pinigų sąskaitą ir tada veiksmų srities skirtuko **Grynųjų pinigų sąskaita** grupėje **Balanso limitas** spustelėkite **Balanso limitas**.</span><span class="sxs-lookup"><span data-stu-id="67397-136">To set up cash balance control rules for a cash account, select the cash account, and then, on the Action Pane, on the **Cash account** tab, in the **Balance limit** group, click **Balance limit**.</span></span> <span data-ttu-id="67397-137">Įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-137">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-138">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-138">Field</span></span></th>
<th><span data-ttu-id="67397-139">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-140">Valiutos tipas</span><span class="sxs-lookup"><span data-stu-id="67397-140">Currency type</span></span></td>
<td><span data-ttu-id="67397-141">Pasirinkite valiutos tipą.</span><span class="sxs-lookup"><span data-stu-id="67397-141">Select the type of currency:</span></span>
<ul>
<li><span data-ttu-id="67397-142"><strong>Apskaitos valiuta</strong> – naudokite pagrindinės įmonės valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-142"><strong>Accounting currency</strong> – Use the basic company currency code.</span></span></li>
<li><span data-ttu-id="67397-143"><strong>Nurodyta valiuta</strong> – naudokite valiutos kodą, kuris skiriasi nuo pagrindinės įmonės valiutos kodo.</span><span class="sxs-lookup"><span data-stu-id="67397-143"><strong>Indicated currency</strong> – Use a currency code that differs from the basic company currency code.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-144">Valiuta</span><span class="sxs-lookup"><span data-stu-id="67397-144">Currency</span></span></td>
<td><span data-ttu-id="67397-145">Jei lauke <strong>Valiutos tipas</strong> pasirinkote <strong>Nurodyta valiuta</strong>, pasirinkite valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-145">If you selected <strong>Indicated currency</strong> in the <strong>Currency type</strong> field, select a currency code.</span></span> <span data-ttu-id="67397-146">Šio lauko naudoti negalima, jei lauke <strong>Valiutos tipas</strong> pasirinkote <strong>Apskaitos valiuta</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-146">This field is unavailable if you selected <strong>Accounting currency</strong> in the <strong>Currency type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-147">Balanso limito tipas</span><span class="sxs-lookup"><span data-stu-id="67397-147">Balance limit type</span></span></td>
<td><span data-ttu-id="67397-148">Pasirinkti vieną galimų verčių.</span><span class="sxs-lookup"><span data-stu-id="67397-148">Select one of the available values:</span></span>
<ul>
<li><span data-ttu-id="67397-149"><strong>Didžiausia</strong> – grynųjų pinigų balansas negali viršyti grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodytos sumos (viršutinė riba).</span><span class="sxs-lookup"><span data-stu-id="67397-149"><strong>Maximum</strong> – The cash balance should not be allowed to exceed the <strong>Balance limit</strong> amount for the cash account (upper bound).</span></span></li>
<li><span data-ttu-id="67397-150"><strong>Mažiausia</strong> – grynųjų pinigų balansas negali būti mažesnis nei grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodyta suma (apatinė riba).</span><span class="sxs-lookup"><span data-stu-id="67397-150"><strong>Minimum</strong> – The cash balance should not be allowed to go below the <strong>Balance limit</strong> amount for the cash account (bottom bound).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-151">Tikrinti balanso limitą</span><span class="sxs-lookup"><span data-stu-id="67397-151">Check balance limit</span></span></td>
<td><span data-ttu-id="67397-152">Pasirinkite, kas bus atliekama grynųjų pinigų dokumentų tvirtinimo proceso metu, jei grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodyta suma viršijama.</span><span class="sxs-lookup"><span data-stu-id="67397-152">Select what occurs during the approval process for cash documents if the <strong>Balance limit</strong> amount for the cash account is exceeded:</span></span>
<ul>
<li><span data-ttu-id="67397-153"><strong>Leisti</strong> – limitą galima viršyti.</span><span class="sxs-lookup"><span data-stu-id="67397-153"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="67397-154"><strong>Įspėjimas</strong> – limitą galima viršyti, bet vartotojui rodomas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="67397-154"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="67397-155">Grynųjų pinigų dokumentas patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="67397-155">The cash document is confirmed or approved.</span></span></li>
<li><span data-ttu-id="67397-156"><strong>Klaida</strong> – limito viršyti negalima.</span><span class="sxs-lookup"><span data-stu-id="67397-156"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="67397-157">Vartotojui rodomas klaidos pranešimas, o grynųjų pinigų dokumentas nėra patvirtinamas.</span><span class="sxs-lookup"><span data-stu-id="67397-157">The user receives an error message, and the cash document isn&#39;t confirmed or approved.</span></span></li>
</ul>
<span data-ttu-id="67397-158">Daugiau informacijos apie grynųjų pinigų dokumentų tvirtinimo procesą žr. tolesniame šios temos skyriuje &quot;Grynųjų pinigų tvirtinimas ir registravimas&quot;.</span><span class="sxs-lookup"><span data-stu-id="67397-158">For more information about the approval process for cash documents, see the &quot;Cash transaction approval and posting&quot; section, later in this topic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-159">Balanso limitas</span><span class="sxs-lookup"><span data-stu-id="67397-159">Balance limit</span></span></td>
<td><span data-ttu-id="67397-160">Įveskite grynųjų pinigų sąskaitos balanso limitą.</span><span class="sxs-lookup"><span data-stu-id="67397-160">Enter a limit for the cash account balance.</span></span> <span data-ttu-id="67397-161">Suma turi būti rodoma jūsų nurodyta valiuta.</span><span class="sxs-lookup"><span data-stu-id="67397-161">The amount should be in the currency that you specified.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a><span data-ttu-id="67397-162">Grynųjų pinigų registravimo šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="67397-162">Set up cash posting profiles</span></span>

<span data-ttu-id="67397-163">Grynųjų pinigų registravimo šablonai apibrėžia registravimą DK.</span><span class="sxs-lookup"><span data-stu-id="67397-163">Cash posting profiles define postings to the general ledger.</span></span> <span data-ttu-id="67397-164">Norėdami nustatyti grynųjų pinigų registravimo šabloną, atidarykite **Grynųjų pinigų** **ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų registravimo šablonai** ir pasirinkite arba sukurkite registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="67397-164">To set up a cash posting profile, go to **Cash** **and bank management** &gt; **Setup** &gt; **Cash posting profiles**, and select or create a posting profile.</span></span> <span data-ttu-id="67397-165">Įveskite toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-165">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-166">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-166">Field</span></span></th>
<th><span data-ttu-id="67397-167">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-168">Galioja</span><span class="sxs-lookup"><span data-stu-id="67397-168">Valid for</span></span></td>
<td><span data-ttu-id="67397-169">Nurodykite, ar registravimo šablonas taikomas konkrečiai grynųjų pinigų sąskaitai ar visoms grynųjų pinigų sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="67397-169">Select whether the posting profile applies to a specific cash account or all cash accounts:</span></span>
<ul>
<li><span data-ttu-id="67397-170"><strong>Lentelė</strong> – jei yra registravimo šablono eilutė, skirta grynųjų pinigų sąskaitai, ta eilutė naudojama registruojant grynųjų pinigų operaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-170"><strong>Table</strong> – If there is a posting profile line for the cash account, that line is used for cash transaction posting.</span></span></li>
<li><span data-ttu-id="67397-171"><strong>Visi</strong> – nėra registravimo šablono eilutės, skirtos grynųjų pinigų sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="67397-171"><strong>All</strong> – There is no posting profile line for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-172">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="67397-172">Cash</span></span></td>
<td><span data-ttu-id="67397-173">Jei lauke <strong>Galioja</strong> pasirinkote parinktį <strong>Lentelė</strong>, nurodykite grynųjų pinigų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-173">If you selected <strong>Table</strong> in the <strong>Valid for</strong> field, specify the cash account.</span></span> <span data-ttu-id="67397-174">Šis laukas lieka neužpildytas, jei lauke <strong>Galioja</strong> pasirinkote parinktį <strong>Visi</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-174">This field remains blank if you selected <strong>All</strong> in the <strong>Valid for</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-175">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="67397-175">Ledger account</span></span></td>
<td><span data-ttu-id="67397-176">Įveskite DK sąskaitos numerį, kuris bus naudojamas grynųjų pinigų sąskaitos suminė sąskaita.</span><span class="sxs-lookup"><span data-stu-id="67397-176">Enter the number of the ledger account to use as the summary account for the cash account.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a><span data-ttu-id="67397-177">Grynųjų pinigų dokumentų numeracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="67397-177">Set up number sequences for cash documents</span></span>

<span data-ttu-id="67397-178">Norėdami nustatyti grynųjų pinigų dokumentų numeracijas, atidarykite **Grynųjų pinigų valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="67397-178">To set up number sequences for cash documents, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="67397-179">Skirtuke **Numeracija** nurodykite numeracijos kodus, skirtus dokumentams **Grynųjų pinigų kompensacijos kvitai**, **Grynųjų pinigų išmokėjimo kvitai**, **Grynųjų pinigų koregavimo kvitas** ir **Derinimas dėl valiutos kurso** bei **Grynųjų pinigų ataskaitos numeris**.</span><span class="sxs-lookup"><span data-stu-id="67397-179">On the **Number sequence** tab, specify number sequence codes for the **Cash reimbursement slips**, **Cash disbursement slips**, **Cash correction voucher**, and **Exchange adjustment** documents, and for **Cash report number**.</span></span>

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a><span data-ttu-id="67397-180">Grynųjų pinigų ir banko valdymo parametrų numatytųjų verčių nustatymas</span><span class="sxs-lookup"><span data-stu-id="67397-180">Set up default values for Cash and bank management parameters</span></span>

<span data-ttu-id="67397-181">Norėdami nustatyti smulkių išlaidų funkcijos grynųjų pinigų ir banko valdymo parametrų numatytąsias vertes, atidarykite **Grynųjų pinigų valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="67397-181">To set up default values for Cash and bank management parameters for the petty cash functionality, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="67397-182">Skirtuke **Grynieji pinigai** įveskite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-182">On the **Cash** tab, enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-183">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-183">Field</span></span></th>
<th><span data-ttu-id="67397-184">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-185">Grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="67397-185">Cash</span></span></td>
<td><span data-ttu-id="67397-186">Pasirinkite numatytąją žurnalų grynųjų pinigų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-186">Select the default cash account in journals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-187">Grynųjų registravimas</span><span class="sxs-lookup"><span data-stu-id="67397-187">Cash posting</span></span></td>
<td><span data-ttu-id="67397-188">Įveskite numatytąjį grynųjų pinigų registravimo šabloną, naudojamą, jei joks kitas registravimo šablonas nenurodytas.</span><span class="sxs-lookup"><span data-stu-id="67397-188">Enter the default cash posting profile that is used if no other posting profile is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-189">Panaudotų kvitų kontrolė</span><span class="sxs-lookup"><span data-stu-id="67397-189">Check for voucher used</span></span></td>
<td><span data-ttu-id="67397-190">Pasirinkite, kas bus atliekama, jei tikrinant grynųjų pinigų dokumento numerį rasti pasikartojantys numeriai.</span><span class="sxs-lookup"><span data-stu-id="67397-190">Select what occurs if duplicate numbers are found during the check of the cash document number:</span></span>
<ul>
<li><span data-ttu-id="67397-191">Neleisti dubliuoti</span><span class="sxs-lookup"><span data-stu-id="67397-191">Reject duplicate</span></span></li>
<li><span data-ttu-id="67397-192">Neleisti daryti kopijų finansiniuose metuose</span><span class="sxs-lookup"><span data-stu-id="67397-192">Reject copies within fiscal year</span></span></li>
<li><span data-ttu-id="67397-193">Leisti dubliavimą</span><span class="sxs-lookup"><span data-stu-id="67397-193">Accept duplicates</span></span></li>
<li><span data-ttu-id="67397-194">Perspėjimas apie dublikatus</span><span class="sxs-lookup"><span data-stu-id="67397-194">Warn in case of duplicates</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-195">Tikrinti operacijų limitą</span><span class="sxs-lookup"><span data-stu-id="67397-195">Check operations limit</span></span></td>
<td><span data-ttu-id="67397-196">Nurodykite, kad nutinka, jei viršijama operacijų su sąveikos objektais riba.</span><span class="sxs-lookup"><span data-stu-id="67397-196">Specify what occurs if the limit for operations with counteragents is exceeded:</span></span>
<ul>
<li><span data-ttu-id="67397-197"><strong>Leisti</strong> – limitą galima viršyti.</span><span class="sxs-lookup"><span data-stu-id="67397-197"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="67397-198"><strong>Įspėjimas</strong> – limitą galima viršyti, bet vartotojui rodomas įspėjimas.</span><span class="sxs-lookup"><span data-stu-id="67397-198"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="67397-199">Operacija užregistruota.</span><span class="sxs-lookup"><span data-stu-id="67397-199">The operation is posted.</span></span></li>
<li><span data-ttu-id="67397-200"><strong>Klaida</strong> – limito viršyti negalima.</span><span class="sxs-lookup"><span data-stu-id="67397-200"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="67397-201">Vartotojui rodomas klaidos pranešimas, o operacija nėra registruojama.</span><span class="sxs-lookup"><span data-stu-id="67397-201">The user receives an error message, and the operation isn&#39;t posted.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-202">Tikrinimo metodas</span><span class="sxs-lookup"><span data-stu-id="67397-202">Validation method</span></span></td>
<td><span data-ttu-id="67397-203">Pasirinkite tikrinimo metodą, naudojamą limitą viršijančioms operacijų sumoms kontroliuoti.</span><span class="sxs-lookup"><span data-stu-id="67397-203">Select the validation method that is used to control exceeded limit amounts for operations:</span></span>
<ul>
<li><span data-ttu-id="67397-204"><strong>Operacija</strong> – atliekamas kiekvienos operacijos tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="67397-204"><strong>Operation</strong> – Validation is done per transaction</span></span></li>
<li><span data-ttu-id="67397-205"><strong>Sutartis</strong> – atliekamas kiekvienos operacijos, turinčios nurodytą sutartį su sąveikos objektu, tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="67397-205"><strong>Agreement</strong> – Validation is done per transaction that has a specified contract with a counteragent.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-206">Operacijų limitas</span><span class="sxs-lookup"><span data-stu-id="67397-206">Operations limit</span></span></td>
<td><span data-ttu-id="67397-207">Įveskite didžiausią sumą, leidžiamą operacijose, kurios turi sąveikos objektų grynaisiais.</span><span class="sxs-lookup"><span data-stu-id="67397-207">Enter the maximum amount that is allowed for operations with counteragents in cash.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-208">Registravimas ankstesne data</span><span class="sxs-lookup"><span data-stu-id="67397-208">Posting on earlier date</span></span></td>
<td><span data-ttu-id="67397-209">Pažymėkite šį žymės langelį, kad leistumėte registruoti grynųjų pinigų operacijas ankstesne nei vėliausios grynųjų pinigų operacijos data.</span><span class="sxs-lookup"><span data-stu-id="67397-209">Select this check box to enable cash transactions to be posted before the last date of the cash transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-210">Dimensijos</span><span class="sxs-lookup"><span data-stu-id="67397-210">Dimensions</span></span></td>
<td><span data-ttu-id="67397-211">Įveskite dimensijas laukuose <strong>Padalinio kodas</strong>, <strong>Analizės kodas</strong> ir <strong>Paskirties kodas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-211">Enter dimensions in the <strong>Department code</strong>, <strong>Analytical code</strong>, and <strong>Purpose code</strong> fields.</span></span> <span data-ttu-id="67397-212">Ši informacija bus nurodyta grynųjų pinigų dokumentų spausdinimo formoje.</span><span class="sxs-lookup"><span data-stu-id="67397-212">The printing form for cash documents will reflect this information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-213">Naudoti patvirtinimo būseną</span><span class="sxs-lookup"><span data-stu-id="67397-213">Use confirm status</span></span></td>
<td><span data-ttu-id="67397-214">Pažymėkite šį žymės langelį , kad būtų naudojama papildoma būsena <strong>patvirtinta</strong>, kai patvirtinate grynųjų pinigų dokumentus.</span><span class="sxs-lookup"><span data-stu-id="67397-214">Select this check box to use an additional status, <strong>Confirmed</strong>, during the approval process for cash documents.</span></span> <span data-ttu-id="67397-215">(Daugiau informacijos žr. skyriuje &quot;Grynųjų pinigų operacijų tvirtinimas ir registravimas&quot;.)</span><span class="sxs-lookup"><span data-stu-id="67397-215">(For more information, see the &quot;Cash transaction approval and posting&quot; section.)</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a><span data-ttu-id="67397-216">Grynųjų pinigų žurnalų pavadinimų nustatymas DK</span><span class="sxs-lookup"><span data-stu-id="67397-216">Set up cash journal names in General ledger</span></span>

<span data-ttu-id="67397-217">Norėdami kurti grynųjų pinigų operacijų registravimo žurnalą, atidarykite **DK** &gt; **Žurnalo sąranka** &gt; **Žurnalų pavadinimai** ir sukurkite naują įrašą.</span><span class="sxs-lookup"><span data-stu-id="67397-217">To create a journal for cash transaction posting, go to **General ledger** &gt; **Journal setup** &gt; **Journal names**, and create a new record.</span></span> <span data-ttu-id="67397-218">Lauke **Žurnalo tipas** nurodykite **Grynieji pinigai**.</span><span class="sxs-lookup"><span data-stu-id="67397-218">In the **Journal type** field, specify **Cash**.</span></span> <span data-ttu-id="67397-219">Pagal poreikį nustatykite kitus numatytuosius žurnalo parametrus.</span><span class="sxs-lookup"><span data-stu-id="67397-219">Define other default journal parameters as you require.</span></span>

## <a name="daily-cash-operations-via-a-slip-journal"></a><span data-ttu-id="67397-220">Kasdienės grynųjų pinigų operacijos naudojant važtaraščių žurnalą</span><span class="sxs-lookup"><span data-stu-id="67397-220">Daily cash operations via a Slip journal</span></span>
<span data-ttu-id="67397-221">Jei norite kurti grynųjų pinigų dokumentą naudodami važtaraščių žurnalą, atidarykite **Grynųjų pinigų ir banko valdymas** &gt; **Grynųjų pinigų operacijos** &gt; **Važtaraščių žurnalas** ir sukurkite naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="67397-221">To create a cash document via a Slip journal, go to **Cash and bank management** &gt; **Cash transactions** &gt; **Slip journal**, and create a new journal.</span></span> <span data-ttu-id="67397-222">Veiksmų srityje spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="67397-222">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="67397-223">Įtraukite naują eilutę ir įveskite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-223">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-224">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-224">Field</span></span></th>
<th><span data-ttu-id="67397-225">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-225">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-226">Data</span><span class="sxs-lookup"><span data-stu-id="67397-226">Date</span></span></td>
<td><span data-ttu-id="67397-227">Įveskite operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="67397-227">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-228">Paskyra</span><span class="sxs-lookup"><span data-stu-id="67397-228">Account</span></span></td>
<td><span data-ttu-id="67397-229">Pasirinkite grynųjų pinigų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-229">Select the cash account.</span></span> <span data-ttu-id="67397-230">Pagal numatytuosius parametrus grynųjų pinigų sąskaita nurodoma grynųjų pinigų ir banko valdymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="67397-230">By default, a cash account is specified in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-231">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-231">Description</span></span></td>
<td><span data-ttu-id="67397-232">Įveskite operacijos paaiškinamąjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="67397-232">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-233">Debetas Kreditas</span><span class="sxs-lookup"><span data-stu-id="67397-233">Debit Credit</span></span></td>
<td><span data-ttu-id="67397-234">Įveskite grynųjų pinigų dokumento sumą viename iš šių laukų.</span><span class="sxs-lookup"><span data-stu-id="67397-234">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="67397-235"><strong>Debetas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų kvitus ir grynųjų pinigų kompensacijos kvitą.</span><span class="sxs-lookup"><span data-stu-id="67397-235"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="67397-236"><strong>Kreditas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų išlaidas ir grynųjų pinigų kompensacijos kvitą.</span><span class="sxs-lookup"><span data-stu-id="67397-236"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-237">Korespondentinės sąskaitos tipas Korespondentinė sąskaita</span><span class="sxs-lookup"><span data-stu-id="67397-237">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="67397-238">Pasirinkite korespondentinės sąskaitos tipą ir korespondentinės sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="67397-238">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-239">Valiuta</span><span class="sxs-lookup"><span data-stu-id="67397-239">Currency</span></span></td>
<td><span data-ttu-id="67397-240">Pasirinkite operacijos valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-240">Select the code for the transaction currency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-241">Kvitas</span><span class="sxs-lookup"><span data-stu-id="67397-241">Voucher</span></span></td>
<td><span data-ttu-id="67397-242">Šis laukas užpildomas automatiškai, atsižvelgiant į žurnalo sąranką.</span><span class="sxs-lookup"><span data-stu-id="67397-242">This field is filled in automatically, based on the journal setup.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-243">Užsakymo numeris</span><span class="sxs-lookup"><span data-stu-id="67397-243">Order number</span></span></td>
<td><span data-ttu-id="67397-244">Jei nenustatyta jokia kita grynųjų pinigų sąskaitos numeracija, šis laukas užpildomas automatiškai, atsižvelgiant į parametruose nurodytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="67397-244">If no other number sequence is set up for the cash account, this field is filled in automatically, based on the number sequence that is specified in the parameters.</span></span> <span data-ttu-id="67397-245">Pagal poreikį šiame lauke galite neautomatiškai įvesti užsakymo numerį.</span><span class="sxs-lookup"><span data-stu-id="67397-245">You can manually enter an order number in this field as you require.</span></span> <span data-ttu-id="67397-246">Siekiant užtikrinti grynųjų pinigų dokumentų numeravimo nuoseklumą, taikoma ši kontrolė: grynųjų pinigų dokumento, kurio operacijos data ankstesnė, numeris negali būti didesnis nei grynųjų pinigų dokumento, kurio operacijos data vėlesnė, numerį.</span><span class="sxs-lookup"><span data-stu-id="67397-246">To prevent inconsistence in cash document numbering, the following control is applied: the number of a cash document that has an earlier date of operation can&#39;t be higher than number of a cash document that has a later date of operation.</span></span> <span data-ttu-id="67397-247">Jei ši kontrolė jums nereikalinga, grynųjų pinigų ir banko valdymo parametruose pažymėkite žymės langelį <strong>Registravimas ankstesne data</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-247">If you don&#39;t require this control, select the <strong>Posting on earlier date</strong> check box in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-248">Patvirtinimo būsena</span><span class="sxs-lookup"><span data-stu-id="67397-248">Approval status</span></span></td>
<td><span data-ttu-id="67397-249">Pradinė operacijos būsena yra <strong>Nėra</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-249">The first transaction status is <strong>None</strong>.</span></span> <span data-ttu-id="67397-250">Daugiau informacijos apie tai, kaip nustatyti operacijos būseną, žr. skyriuje &quot;Grynųjų pinigų operacijų tvirtinimas ir registravimas&quot;.</span><span class="sxs-lookup"><span data-stu-id="67397-250">For information about how to set the transaction status, See the &quot;Cash transaction approval and posting&quot; section.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-251">Dokumento tipas </span><span class="sxs-lookup"><span data-stu-id="67397-251">Document type</span></span></td>
<td><span data-ttu-id="67397-252">Šis skirtuko <strong>Grynųjų pinigų užsakymas</strong> laukas užpildomas automatiškai, atsižvelgiant į įvestą grynųjų pinigų dokumento sumą.</span><span class="sxs-lookup"><span data-stu-id="67397-252">This field on the <strong>Cash order</strong> tab is filled in automatically, based on the amount that you entered for the cash document:</span></span>
<ul>
<li><span data-ttu-id="67397-253"><strong>Grynųjų pinigų kompensacijos kvitas</strong> – ši vertė naudojama, jei sumą įvedėte grynųjų pinigų sąskaitos lauke <strong>Debetas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-253"><strong>Cash reimbursement slip</strong> – This value is used if you entered an amount in the <strong>Debit</strong> field for the cash account.</span></span></li>
<li><span data-ttu-id="67397-254"><strong>Grynųjų pinigų išmokėjimo kvitas</strong> – ši vertė naudojama, jei sumą įvedėte grynųjų pinigų sąskaitos lauke <strong>Kreditas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-254"><strong>Cash disbursement slip</strong> – This value is used if you entered an amount in the <strong>Credit</strong> field for the cash account</span></span></li>
<li><span data-ttu-id="67397-255"><strong>Pataisymas</strong> – įvedėte neigiamą sumą grynųjų pinigų sąskaitos lauke <strong>Debetas</strong> arba <strong>Kreditas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-255"><strong>Correction</strong> – You entered a negative amount in either the <strong>Debit</strong> field or the <strong>Credit</strong> field for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-256">PVM grupė</span><span class="sxs-lookup"><span data-stu-id="67397-256">Sales tax group</span></span></td>
<td><span data-ttu-id="67397-257">Nurodykite PVM grupę, naudojamą operacijos mokesčiams skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="67397-257">Specify a sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-258">Prekės PVM grupė</span><span class="sxs-lookup"><span data-stu-id="67397-258">Item sales tax group</span></span></td>
<td><span data-ttu-id="67397-259">Nurodykite prekės PVM grupę, naudojamą operacijos mokesčiams skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="67397-259">Specify an item sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-260">Priežastis</span><span class="sxs-lookup"><span data-stu-id="67397-260">Reason</span></span></td>
<td><span data-ttu-id="67397-261">Skirtuke <strong>Grynųjų pinigų užsakymas</strong> įveskite tekstą, aprašantį operacijos subjektą.</span><span class="sxs-lookup"><span data-stu-id="67397-261">On the <strong>Cash order</strong> tab, enter text that describes the transaction subject.</span></span> <span data-ttu-id="67397-262">Šis tekstas bus spausdinamas grynųjų pinigų kvito ataskaitos formoje.</span><span class="sxs-lookup"><span data-stu-id="67397-262">This text will be printed on the cash slip reporting form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-263">Dokumento data</span><span class="sxs-lookup"><span data-stu-id="67397-263">Document Date</span></span></td>
<td><span data-ttu-id="67397-264">Įveskite pradinio dokumento, kuris yra operacijos priežastis (pvz., išankstinės ataskaitos, SF arba užsakymo), aprašą, numerį ir datą.</span><span class="sxs-lookup"><span data-stu-id="67397-264">Enter the description, number, and date of the primary document that is the reason for the transaction (for example, advance reports, invoice, or order).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-265">Atstovo tipas</span><span class="sxs-lookup"><span data-stu-id="67397-265">Representative type</span></span></td>
<td><span data-ttu-id="67397-266">Šiame lauke galima naudoti toliau nurodytas vertes.</span><span class="sxs-lookup"><span data-stu-id="67397-266">This field can have the following values:</span></span>
<ul>
<li><span data-ttu-id="67397-267"><strong>Darbuotojas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas darbuotojų sąrašas, jei laukas <strong>Korespondentinė sąskaita</strong> nustatytas į parinktį <strong>DK</strong> arba <strong>Bankas</strong>, arba sąveikos objekto kontaktinių asmenų sąrašas, jei laukas <strong>Korespondentinė sąskaita</strong> nustatytas į parinktį <strong>Klientas</strong> arba <strong>Tiekėjas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-267"><strong>Worker</strong> – The <strong>Representative</strong> lookup contains a list of employees if the <strong>Offset account</strong> field is set to <strong>Ledger</strong> or <strong>Bank</strong>, or a list of the counteragent&#39;s contact persons if the <strong>Offset account</strong> field is set to <strong>Customer</strong> or <strong>Vendor</strong>.</span></span> <span data-ttu-id="67397-268">Norėdami nustatyti atstovus, pasirinkite <strong>Pagrindinis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Kontaktai</strong> &gt; <strong>Kontaktinis asmuo</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-268">To set up representatives, go to <strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Contact person</strong>.</span></span></li>
<li><span data-ttu-id="67397-269"><strong>Kita</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas kitų klientų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="67397-269"><strong>Other</strong> – The <strong>Representative</strong> lookup contains a list of other clients.</span></span> <span data-ttu-id="67397-270">Norėdami nustatyti gavėjus, kurių nėra lentelėje <strong>Klientai</strong> arba <strong>Tiekėjai</strong>, pasirinkite <strong>DK</strong> &gt; <strong>Gavėjai</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-270">To set up receivers who don&#39;t appear in the <strong>Customers</strong> or <strong>Vendors</strong> table, go to <strong>General ledger</strong> &gt; <strong>Receivers</strong>.</span></span> <span data-ttu-id="67397-271">Šį tipą galima naudoti tik Latvijoje.</span><span class="sxs-lookup"><span data-stu-id="67397-271">This type is available only for Latvia.</span></span> <span data-ttu-id="67397-272">(Turi būti suaktyvinta konfigūracija <strong>CSELatvia</strong>.)</span><span class="sxs-lookup"><span data-stu-id="67397-272">(The <strong>CSELatvia</strong> configuration key should be enabled.)</span></span></li>
<li><span data-ttu-id="67397-273"><strong>Tiekėjas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas tiekėjų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="67397-273"><strong>Vendor</strong> – The <strong>Representative</strong> lookup contains a list of vendors.</span></span> <span data-ttu-id="67397-274">Norėdami nustatyti tiekėjus, pasirinkite <strong>Mokėtinos sumos</strong> &gt; <strong>Tiekėjai</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-274">To set up vendors, go to <strong>Accounts payable</strong> &gt; <strong>Vendors</strong>.</span></span></li>
<li><span data-ttu-id="67397-275"><strong>Klientas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas klientų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="67397-275"><strong>Customer</strong> – The <strong>Representative</strong> lookup contains a list of customers.</span></span> <span data-ttu-id="67397-276">Norėdami nustatyti klientus, pasirinkite <strong>Gautinos sumos</strong> &gt; <strong>Klientai</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-276">To set up customers, go to <strong>Accounts receivable</strong> &gt; <strong>Customers</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-277">Atstovas</span><span class="sxs-lookup"><span data-stu-id="67397-277">Representative</span></span></td>
<td><span data-ttu-id="67397-278">Pasirinkite atstovą, kurio tipą nurodėte lauke <strong>Atstovo tipas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-278">Select a representative of the type that you specified in the <strong>Representative type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-279">Asmens vardas</span><span class="sxs-lookup"><span data-stu-id="67397-279">Name of person</span></span></td>
<td><span data-ttu-id="67397-280">Šis laukas užpildomas automatiškai, atsižvelgiant laukus <strong>Korespondentinė sąskaita</strong> ir <strong>Atstovas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-280">This field is filled in automatically, based on the <strong>Offset account</strong> and <strong>Representative</strong> fields.</span></span> <span data-ttu-id="67397-281">Ši informacija bus nurodyta grynųjų pinigų kvitų spausdinimo formoje.</span><span class="sxs-lookup"><span data-stu-id="67397-281">The printing form for cash slips will reflect this information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-282">Tapatybės kortelė</span><span class="sxs-lookup"><span data-stu-id="67397-282">Identity card</span></span></td>
<td><span data-ttu-id="67397-283">Šis laukas užpildomas automatiškai, atsižvelgiant į kontaktinio asmens (atstovo) tapatybės kortelės duomenis.</span><span class="sxs-lookup"><span data-stu-id="67397-283">This field is filled in automatically, based on the identity card data for the contact person (representative).</span></span> <span data-ttu-id="67397-284">Jei laukas <strong>Korespondentinės sąskaitos tipas</strong> nustatytas į parinktį <strong>Avanso turėtojas</strong>, o laukas <strong>Korespondentinė sąskaita</strong> nustatytas į darbuotojo numerį, grynųjų pinigų gavimas arba išlaidos gali būti priskiriamos darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="67397-284">If the <strong>Offset account type</strong> field is set to <strong>Advance holder</strong>, and the <strong>Offset account</strong> field is set to an employee number, cash receipts or expenditures can be done from or to the employee.</span></span> <span data-ttu-id="67397-285">Šiuo atveju laukas <strong>Tapatybės kortelė</strong> užpildomas automatiškai naudojant tapatybės kortelės duomenis iš lentelės <strong>Darbuotojai</strong> (<strong>Personalo apskaita</strong> &gt; <strong>Darbuotojų lentelė</strong>).</span><span class="sxs-lookup"><span data-stu-id="67397-285">In this case the <strong>Identity card</strong> field is filled in automatically by using data for the identity card from the <strong>Employee</strong> table (<strong>Staff accounting</strong> &gt; <strong>Employee table</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-286">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="67397-286">Purpose</span></span></td>
<td><span data-ttu-id="67397-287">Lentelėje <strong>Paskirtis</strong> nurodykite vieną arba daugiau operacijos sumos paskirties kodų.</span><span class="sxs-lookup"><span data-stu-id="67397-287">In the <strong>Purpose</strong> table, define one or more destination codes for the transaction amount.</span></span> <span data-ttu-id="67397-288">Pasirinkite paskirties kodą lauke <strong>Paskirtis</strong> ir įveskite paaiškinimą lauke <strong>Operacijos tekstas</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-288">Select a destination code in the <strong>Purpose</strong> field, and enter an explanation in the <strong>Transaction text</strong> field.</span></span> <span data-ttu-id="67397-289">Lauke <strong>Suma</strong> įveskite sumą operacijos valiuta.</span><span class="sxs-lookup"><span data-stu-id="67397-289">In the <strong>Amount</strong> field, enter an amount in the transaction currency.</span></span> <span data-ttu-id="67397-290">Lauke <strong>Procentas</strong> rodomas paskirties sumos ir bendros operacijos sumos koeficientas procentais.</span><span class="sxs-lookup"><span data-stu-id="67397-290">The <strong>Percent</strong> field shows, as a percentage, the ratio of the destination amount to the total transaction amount.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-291">Likutis</span><span class="sxs-lookup"><span data-stu-id="67397-291">Remainder</span></span></td>
<td><span data-ttu-id="67397-292">Apskaičiuojama likusi suma.</span><span class="sxs-lookup"><span data-stu-id="67397-292">The remaining amount that is calculated.</span></span> <span data-ttu-id="67397-293">Atkreipkite dėmesį, kad visą operacijos sumą reikia priskirti paskirties kodams.</span><span class="sxs-lookup"><span data-stu-id="67397-293">Note that the whole transaction amount must be assigned to destination codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-294">Tarnautojai</span><span class="sxs-lookup"><span data-stu-id="67397-294">Officials</span></span></td>
<td><span data-ttu-id="67397-295">Skirtuke <strong>Tarnautojai</strong> nurodykite atsakingų asmenų (Direktorius, Vyr. buhalteris ir Kasininkas) vardus ir pavardes.</span><span class="sxs-lookup"><span data-stu-id="67397-295">On the <strong>Officials</strong> tab, specify the names and titles for responsible persons: Director, Chief accountant, and Cashier.</span></span> <span data-ttu-id="67397-296">Lauko <strong>Pareigos</strong> vertės nustatomos pagal tarnautojų nustatymą puslapio <strong>Tarnautojai</strong> skirtukuose <strong>Bendra</strong> ir <strong>DK</strong> (<strong>Pagrindinis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Kontaktai</strong> &gt; <strong>Tarnautojai</strong>).</span><span class="sxs-lookup"><span data-stu-id="67397-296">The <strong>Position</strong> values are determined by the setup of officials on the <strong>General</strong> and <strong>Ledger</strong> tabs of the <strong>Officials</strong> page (<strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Officials</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-297">Išankstinis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="67397-297">Prepayment</span></span></td>
<td><span data-ttu-id="67397-298">Pasirinkite šį žymės langelį, jei operacija yra išankstinis mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="67397-298">Select this check box if the transaction is a prepayment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-299">Registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="67397-299">Posting profile</span></span></td>
<td><span data-ttu-id="67397-300">Įveskite grynųjų pinigų sąskaitos registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="67397-300">Enter the posting profile for the cash account.</span></span> <span data-ttu-id="67397-301">Pagal numatytuosius parametrus naudojamas grynųjų pinigų ir banko valdymo parametruose nurodytas registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="67397-301">By default, the posting profile that is specified in the Cash and bank management parameters is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-302">Koresp. registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="67397-302">Offset posting profile</span></span></td>
<td><span data-ttu-id="67397-303">Įveskite pasirinktos korespondentinės sąskaitos registravimo šabloną.</span><span class="sxs-lookup"><span data-stu-id="67397-303">Enter the posting profile for the selected offset account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-304">Bendra suma</span><span class="sxs-lookup"><span data-stu-id="67397-304">Total amount</span></span></td>
<td><span data-ttu-id="67397-305">Puslapio apačioje esančios laukų grupės <strong>Bendra suma</strong> lauke <strong>Komp.</strong> rodoma bendra apskaičiuota visų grynųjų pinigų kompensacijos kvitų, įvestų dabartiniame žurnale, suma, o lauke <strong>Išm.</strong> rodoma bendra visų grynųjų pinigų išmokėjimo kvitų suma.</span><span class="sxs-lookup"><span data-stu-id="67397-305">In the <strong>Total amount</strong> field group at the bottom of the page, the <strong>Reimb</strong> field shows the total that is calculated for all Cash reimbursement slips that are entered in the current journal, and the <strong>Disb</strong> field shows the total for all Cash disbursement slips.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="67397-306">Norėdami patikrinti žurnalo įrašus, veiksmų srityje spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="67397-306">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="daily-cash-operations-via-a-general-journal"></a><span data-ttu-id="67397-307">Kasdienės grynųjų pinigų operacijos naudojant bendrąjį žurnalą</span><span class="sxs-lookup"><span data-stu-id="67397-307">Daily cash operations via a General journal</span></span>
<span data-ttu-id="67397-308">Jei norite kurti grynųjų pinigų operaciją naudodami bendrąjį žurnalą, atidarykite **DK** &gt; **Žurnalo įrašai** &gt; **Bendrieji žurnalai** ir sukurkite naują žurnalą.</span><span class="sxs-lookup"><span data-stu-id="67397-308">To create a cash transaction via a General journal, go to **General ledger** &gt; **Journal entries** &gt; **General journals**, and create a new journal.</span></span> <span data-ttu-id="67397-309">Veiksmų srityje spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="67397-309">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="67397-310">Įtraukite naują eilutę ir įveskite tolesnę informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-310">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-311">Laukas</span><span class="sxs-lookup"><span data-stu-id="67397-311">Field</span></span></th>
<th><span data-ttu-id="67397-312">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-312">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-313">Data</span><span class="sxs-lookup"><span data-stu-id="67397-313">Date</span></span></td>
<td><span data-ttu-id="67397-314">Įveskite operacijos datą.</span><span class="sxs-lookup"><span data-stu-id="67397-314">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-315">Kodo tipas</span><span class="sxs-lookup"><span data-stu-id="67397-315">Account type</span></span></td>
<td><span data-ttu-id="67397-316">Pasirinkite <strong>Smulkios išlaidos</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-316">Select <strong>Petty cash</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-317">Paskyra</span><span class="sxs-lookup"><span data-stu-id="67397-317">Account</span></span></td>
<td><span data-ttu-id="67397-318">Pasirinkite grynųjų pinigų sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="67397-318">Select the cash account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-319">Operacijos tekstas</span><span class="sxs-lookup"><span data-stu-id="67397-319">Transaction text</span></span></td>
<td><span data-ttu-id="67397-320">Įveskite operacijos paaiškinamąjį tekstą.</span><span class="sxs-lookup"><span data-stu-id="67397-320">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-321">Debetas Kreditas</span><span class="sxs-lookup"><span data-stu-id="67397-321">Debit Credit</span></span></td>
<td><span data-ttu-id="67397-322">Įveskite grynųjų pinigų dokumento sumą viename iš šių laukų.</span><span class="sxs-lookup"><span data-stu-id="67397-322">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="67397-323"><strong>Debetas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų kvitus ir grynųjų pinigų kompensacijos kvitą.</span><span class="sxs-lookup"><span data-stu-id="67397-323"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="67397-324"><strong>Kreditas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų išlaidas ir grynųjų pinigų kompensacijos kvitą.</span><span class="sxs-lookup"><span data-stu-id="67397-324"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-325">Korespondentinės sąskaitos tipas Korespondentinė sąskaita</span><span class="sxs-lookup"><span data-stu-id="67397-325">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="67397-326">Pasirinkite korespondentinės sąskaitos tipą ir korespondentinės sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="67397-326">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-327">Valiuta</span><span class="sxs-lookup"><span data-stu-id="67397-327">Currency</span></span></td>
<td><span data-ttu-id="67397-328">Pasirinkite operacijos valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="67397-328">Select the code for the transaction currency.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="67397-329">Skirtuke **SF** galite nurodyti pasirinktos sąskaitos ir korespondentinės sąskaitos registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="67397-329">On the **Invoice** tab, you can specify posting profiles for the selected account and offset account.</span></span> <span data-ttu-id="67397-330">Jei užregistruota operacija yra išankstinis mokėjimas, skirtuke **Mokėjimas** pažymėkite žymės langelį **Išankstinis mokėjimas**. Laukų grupėje **Atstovas** užpildykite laukus, kaip tai atlikote važtaraščių žurnalo eilutėse, kad spausdintumėte ataskaitą **Grynieji pinigai**.</span><span class="sxs-lookup"><span data-stu-id="67397-330">If the registered transaction is a prepayment, select the **Prepayment** check box on the **Payment** tab. In the **Representative** field group, fill in the fields as you did for the Slip journal lines to print on the **Cash** report.</span></span> <span data-ttu-id="67397-331">Norėdami patikrinti žurnalo įrašus, veiksmų srityje spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="67397-331">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="cash-transaction-approval-and-posting"></a><span data-ttu-id="67397-332">Grynųjų pinigų operacijos tvirtinimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="67397-332">Cash transaction approval and posting</span></span>
<span data-ttu-id="67397-333">Galima taikyti šias grynųjų pinigų operacijų būsenas: **Nėra**, **Patikrinta**, **Patvirtinta** ir **Atmesta**.</span><span class="sxs-lookup"><span data-stu-id="67397-333">For cash transactions, the following statuses can be applied: **None**, **Confirmed**, **Approved**, and **Rejected**.</span></span> <span data-ttu-id="67397-334">Skirtuko **Grynieji pinigai** „FastTab“ **Tvirtinimas** (**Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**) parametras **Naudoti patvirtinimo būseną** suteikia galimybę suaktyvinti dvi papildomas būsenas: **Patvirtinta** ir **Atmesta**.</span><span class="sxs-lookup"><span data-stu-id="67397-334">A **Use confirm status** parameter on the **Approval** FastTab of the **Cash** tab at **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters** lets you activate two additional statuses: **Confirmed** and **Rejected**.</span></span> <span data-ttu-id="67397-335">Tvirtinimas yra tinkamas, kai grynųjų pinigų dokumentai išduodami, o grynųjų pinigų gavimas arba išlaidos padalijamos dviem darbuotojams: buhalteriui ir kasininkui.</span><span class="sxs-lookup"><span data-stu-id="67397-335">Confirmation is appropriate when cash documents are issued, and cash receipts or expenditures are shared between two employees: accountant and cashier.</span></span> <span data-ttu-id="67397-336">Funkcija **Iš naujo nustatyti būseną** keičia dabartinę operacijos būseną.</span><span class="sxs-lookup"><span data-stu-id="67397-336">The **Reset status** function changes the current transaction status.</span></span> <span data-ttu-id="67397-337">**Patvirtinta** tampa **Patikrinta**, o **Patikrinta** tampa **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="67397-337">**Approved** becomes **Confirmed**, and **Confirmed** becomes **None**.</span></span> <span data-ttu-id="67397-338">Grynųjų pinigų žurnalo įrašus galima redaguoti tik kai būsena yra **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="67397-338">Cash journal entries can be edited only when the status is **None**.</span></span> <span data-ttu-id="67397-339">Grynųjų pinigų operacijas galima atmesti tik kai operacijos būsena yra **Patikrinta** .</span><span class="sxs-lookup"><span data-stu-id="67397-339">Cash transactions can be rejected only if the transaction status is **Confirmed**.</span></span> <span data-ttu-id="67397-340">Atmesti grynųjų pinigų dokumentai įtraukiami į ataskaitą **Grynųjų pinigų dokumentų registracijos žurnalas**, bet jie nėra nurodyti ataskaitoje **Kasos knyga**.</span><span class="sxs-lookup"><span data-stu-id="67397-340">Rejected cash documents are included on the **Journal of registration of cash documents** report, but they aren't reflected on the **Cash book** report.</span></span> <span data-ttu-id="67397-341">Norėdami patvirtinti operaciją, pasirinkite atitinkamą važtaraščių žurnalo eilutę ir tada spustelėkite **Dokumentų tvirtinimas** &gt; **Tvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="67397-341">To confirm a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Confirm**.</span></span> <span data-ttu-id="67397-342">Sugeneruojamas užsakymo numeris, atsižvelgiant į nurodytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="67397-342">An order number is generated, based on the specified number sequence.</span></span> <span data-ttu-id="67397-343">Operacijos būsena pasikeičia į **Patvirtinta** ir žurnalo eilutės redaguoti nebegalima.</span><span class="sxs-lookup"><span data-stu-id="67397-343">The transaction status is changed to **Confirmed**, and you can no longer edit the journal line.</span></span> <span data-ttu-id="67397-344">Grynųjų pinigų sąskaitos balansas lieka nepakitęs.</span><span class="sxs-lookup"><span data-stu-id="67397-344">The cash account balance remains unchanged.</span></span> <span data-ttu-id="67397-345">Norėdami atmesti grynųjų pinigų dokumentą, spustelėkite **Dokumentų tvirtinimas** &gt; **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="67397-345">To reject a cash document, click **Documents approval** &gt; **Reject**.</span></span> <span data-ttu-id="67397-346">Šią parinktį galima taikyti tik būsenos **Patvirtinta** dokumentams.</span><span class="sxs-lookup"><span data-stu-id="67397-346">This option is available only for documents that have **Confirmed** status.</span></span> <span data-ttu-id="67397-347">Norėdami patvirtinti operaciją, pasirinkite atitinkamą važtaraščių žurnalo eilutę ir tada spustelėkite **Dokumentų tvirtinimas** &gt; **Tvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="67397-347">To approve a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Approve**.</span></span> <span data-ttu-id="67397-348">Būsena **Patvirtinta** nurodo, grynųjų pinigų lėšos yra gautos arba išleistos.</span><span class="sxs-lookup"><span data-stu-id="67397-348">The **Approved** status indicates that cash funds are received or expended.</span></span> <span data-ttu-id="67397-349">Grynųjų pinigų balansas pakeistas.</span><span class="sxs-lookup"><span data-stu-id="67397-349">The cash balance is changed.</span></span> <span data-ttu-id="67397-350">Grynųjų pinigų operaciją galima registruoti.</span><span class="sxs-lookup"><span data-stu-id="67397-350">The cash transaction can be posted.</span></span> <span data-ttu-id="67397-351">Norėdami atšaukti būseną **Patvirtinta** ir iš naujo nustatyti būseną **Nėra**, spustelėkite **Dokumentų tvirtinimas** &gt; **Iš naujo nustatyti būseną**.</span><span class="sxs-lookup"><span data-stu-id="67397-351">To cancel an **Approved** status and reset the status to **None**, click **Documents approval** &gt; **Reset status**.</span></span> <span data-ttu-id="67397-352">Galima registruoti tik patvirtintas grynųjų pinigų operacijas.</span><span class="sxs-lookup"><span data-stu-id="67397-352">Only approved cash transactions can be posted.</span></span> <span data-ttu-id="67397-353">Norėdami registruoti žurnalą, spustelėkite **Registruoti** &gt; **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="67397-353">To post a journal, click **Post** &gt; **Post**.</span></span>

## <a name="print-a-cash-order"></a><span data-ttu-id="67397-354">Grynųjų pinigų užsakymo spausdinimas</span><span class="sxs-lookup"><span data-stu-id="67397-354">Print a cash order</span></span>
<span data-ttu-id="67397-355">Norėdami spausdinti grynųjų pinigų užsakymą, pasirinkite važtaraščių žurnalo eilutę ir tada veiksmų srityje spustelėkite **Spausdinti** &gt; **Grynųjų pinigų užsakymo ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="67397-355">To print a cash order, select a Slip journal line, and then, on the Action Pane, click **Print** &gt; **Cash order report**.</span></span> <span data-ttu-id="67397-356">Sistema sugeneruoja grynųjų pinigų kompensacijos kvito arba grynųjų pinigų išmokėjimo kvito spausdinimo formą, atsižvelgiant į tai, suma įvesta pasirinktos eilutės lauke **Debetas**, ar lauke **Kreditas**.</span><span class="sxs-lookup"><span data-stu-id="67397-356">The system generates a printing form for either a Cash reimbursement slip or a Cash disbursement slip, depending on whether an amount is entered in the **Debit** field the or **Credit** field for the selected line:</span></span>

-   <span data-ttu-id="67397-357">Jei suma įvesta lauke **Debetas**: grynųjų pinigų kompensacijos kvitas</span><span class="sxs-lookup"><span data-stu-id="67397-357">If there is an amount in the **Debit** field: Cash reimbursement slip</span></span>
-   <span data-ttu-id="67397-358">Jei suma įvesta lauke **Kreditas**: grynųjų pinigų išmokėjimo kvitas</span><span class="sxs-lookup"><span data-stu-id="67397-358">If there is an amount in the **Credit** field: Cash disbursement slip</span></span>

<span data-ttu-id="67397-359">Važtaraščių žurnalo eilutes, kurių būsena **Patikrinta**, **Patvirtinta** arba **Atmesta**, galima spausdinti.</span><span class="sxs-lookup"><span data-stu-id="67397-359">Slip journal lines that have **Confirmed**, **Approved**, or **Rejected** status can be printed.</span></span> <span data-ttu-id="67397-360">Taip pat galite spausdinti grynųjų pinigų užsakymo dokumentus pasirinkę **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Grynųjų pinigų užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="67397-360">You can also print cash order documents at **Cash and bank management** &gt; **Inquires and reports** &gt; **Cash order**.</span></span>

## <a name="periodic-tasks"></a><span data-ttu-id="67397-361">Periodinės užduotys</span><span class="sxs-lookup"><span data-stu-id="67397-361">Periodic tasks</span></span>
<span data-ttu-id="67397-362">Toliau nurodytas užduotis galima atlikti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="67397-362">The following tasks can be performed at **Cash and bank management** &gt; **Periodic tasks**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67397-363">Periodinė užduotis</span><span class="sxs-lookup"><span data-stu-id="67397-363">Periodic task</span></span></th>
<th><span data-ttu-id="67397-364">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67397-365">Tikrinti balanso limitą</span><span class="sxs-lookup"><span data-stu-id="67397-365">Check balance limit</span></span></td>
<td><span data-ttu-id="67397-366">Patikrinkite pasirinktos grynųjų pinigų sąskaitos balansą nurodytą dieną ir pateikite rezultatą informaciniame pranešime.</span><span class="sxs-lookup"><span data-stu-id="67397-366">Check the balance for the selected cash account on the specified date, and show the result in an information message.</span></span> <span data-ttu-id="67397-367">Skaičiuojant balansą įtraukiamos tik patvirtintos operacijos.</span><span class="sxs-lookup"><span data-stu-id="67397-367">Only approved transactions can be counted in the balance calculation.</span></span> <span data-ttu-id="67397-368">Operacijos, kurios pažymėtos kaip <strong>Atlyginimams</strong>, neįtraukiamos.</span><span class="sxs-lookup"><span data-stu-id="67397-368">Transactions that are marked as <strong>For payroll</strong> aren&#39;t considered.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-369">Grynųjų balanso perskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="67397-369">Cash balance recalculation</span></span></td>
<td><span data-ttu-id="67397-370">Naudokite šią užduotį, norėdami įsitikinti, grynųjų pinigų sąskaitų DK balansai neviršija grynųjų pinigų balanso.</span><span class="sxs-lookup"><span data-stu-id="67397-370">Use this task to make sure that the ledger balances for cash accounts fit the cash balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-371">Grynųjų pinigų ataskaitos kūrimas (skirta tik Lenkijai)</span><span class="sxs-lookup"><span data-stu-id="67397-371">Cash report creation (for Poland only)</span></span></td>
<td><span data-ttu-id="67397-372">Sukurkite <strong>grynųjų pinigų</strong> ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-372">Create a <strong>Cash</strong> report.</span></span> <span data-ttu-id="67397-373"><strong>Grynųjų pinigų</strong> ataskaitos numeris sugeneruojamas pagal lauke <strong>Ataskaitos numeris</strong> nustatytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="67397-373">The <strong>Cash</strong> report number is generated based on the number sequence that is set up for <strong>Report number</strong>.</span></span> <span data-ttu-id="67397-374">Užduoties dialogo lango lauke <strong>Pabaigos data</strong> nurodykite vėliausią dieną, iki kurios atliktos operacijos įtraukiamos į <strong>grynųjų pinigų</strong> ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="67397-374">In the dialog box for the task, in the <strong>To date</strong>, specify the last date for which cash transactions should be counted for the <strong>Cash</strong> report.</span></span> <span data-ttu-id="67397-375">Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte papildomus grynųjų pinigų operacijų pasirinkimo ribojimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="67397-375">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify additional criteria to limit the selection of cash transactions.</span></span> <span data-ttu-id="67397-376">Šie kriterijai gali apimti grynųjų pinigų sąskaitos numerius ir valiutų kodus.</span><span class="sxs-lookup"><span data-stu-id="67397-376">These criteria can include cash account numbers and currency codes.</span></span> <span data-ttu-id="67397-377">Lauke <strong>Sukūrė</strong> pasirinkite už ataskaitos kūrimą atsakingą vartotoją.</span><span class="sxs-lookup"><span data-stu-id="67397-377">In the <strong>Create by</strong> field, select the user who is responsible for report creation.</span></span> <span data-ttu-id="67397-378">Norėdami peržiūrėti kuriamą <strong>grynųjų pinigų</strong> ataskaitą, naudokite puslapio <strong>Grynųjų pinigų sąskaitos</strong> mygtuką <strong>Grynųjų pinigų ataskaitos</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-378">To view the <strong>Cash</strong> report that is created, use the <strong>Cash reports</strong> button on the <strong>Cash accounts</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67397-379">Grynieji pinigai – derinimo dėl valiutos kurso FIFO ir LIFO (skirta tik Lenkijai)</span><span class="sxs-lookup"><span data-stu-id="67397-379">Cash - Exchange adjustment FIFO and LIFO (for Poland only)</span></span></td>
<td><span data-ttu-id="67397-380">Apskaičiuokite derinimą dėl valiutos kurso pagal Lenkijoje taikomus standartus.</span><span class="sxs-lookup"><span data-stu-id="67397-380">Calculate the exchange adjustment per Polish standards.</span></span> <span data-ttu-id="67397-381">Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte grynųjų pinigų sąskaitą, kurios užduotį norite vykdyti.</span><span class="sxs-lookup"><span data-stu-id="67397-381">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="67397-382">Pasirinkite žymės langelį <strong>Perskaičiavimas</strong>, norėdami visiškai perskaičiuoti visų atvirų laikotarpių derinimo dėl valiutos kurso skirtumą.</span><span class="sxs-lookup"><span data-stu-id="67397-382">Select the <strong>Recalculation</strong> check box to do a full recalculation of the exchange adjustment difference for all open periods.</span></span> <span data-ttu-id="67397-383">Toliau parodoma, kai skaičiuojamas derinimas dėl valiutos kurso, kai naudojami metodai „pirmasis į, pirmasis iš“ (FIFO) ir „paskutinysis į, pirmasis iš“ (LIFO).</span><span class="sxs-lookup"><span data-stu-id="67397-383">Here is how the exchange adjustment is calculated when the first in, first out (FIFO) and last in, first out (LIFO) methods are used:</span></span>
<ul>
<li><span data-ttu-id="67397-384"><strong>FIFO metodas</strong> – sistema ieško išlaidų operacijos, kurios operacijos data ankstesnė (mažesnis užsakymo numeris) ir sudengia ją naudodama gavimo operaciją, kurios operacijos data ankstesnė (mažesnis užsakymo numeris).</span><span class="sxs-lookup"><span data-stu-id="67397-384"><strong>FIFO method</strong> – The system searches for an expenditure transaction that has an earlier transaction date (smaller order number) and settles it with a receipt transaction that has an earlier transaction date (smaller order number).</span></span></li>
<li><span data-ttu-id="67397-385"><strong>LIFO metodas</strong> – sistema ieško išlaidų operacijos, kurios operacijos data vėlesnė (didesnis užsakymo numeris) ir sudengia ją naudodama gavimo operaciją, kurios operacijos data vėlesnė (didesnis užsakymo numeris).</span><span class="sxs-lookup"><span data-stu-id="67397-385"><strong>LIFO method</strong> – The system searches for an expenditure transaction that has a later transaction date (larger order number) and settles it with a receipt transaction that has a later transaction date (larger order number).</span></span></li>
</ul>
<span data-ttu-id="67397-386">Sudengta suma nurodoma puslapio <strong>Grynųjų pinigų operacija</strong> lauke <strong>Sudengta valiuta</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-386">The settled amount is reflected in the <strong>Settled currency</strong> field on the <strong>Cash transaction</strong> page.</span></span> <span data-ttu-id="67397-387">Jei nustatytas derinimo dėl valiutos kurso skirtumas, suma rodoma lauke <strong>Derinimo dėl valiutos kurso suma</strong>, o dokumento tipo <strong>Valiutos kursų skirtumas</strong> operacija sugeneruojama lentelėje <strong>Grynųjų pinigų operacija</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-387">If there is an exchange adjustment difference, the amount is reflected in the <strong>Exchange adjustment amount</strong> field, and a transaction of the <strong>Exchange rate difference</strong> document type is generated in the <strong>Cash transaction</strong> table.</span></span> <span data-ttu-id="67397-388">Pelno / nuostolių operacijų DK sąskaitos nustatomos lentelėje <strong>Valiuta</strong> (<strong>Valiutos kurso finansinis pelnas</strong> ir <strong>Valiutos kurso finansiniai nuostoliai</strong>).</span><span class="sxs-lookup"><span data-stu-id="67397-388">Ledger accounts for profit/loss transactions are set in the <strong>Currency</strong> table (<strong>Exchange rate financial profit</strong> and <strong>Exchange rate financial loss</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67397-389">Užsienio valiutos kurso pasikeitimas – grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="67397-389">Foreign currency revaluation - Cash</span></span></td>
<td><span data-ttu-id="67397-390">Naudokite šią užduotį, kad ataskaitos dieną balansas numatytąja valiuta būtų pakankamas, kai operacijos įvedamos užsienio valiutomis.</span><span class="sxs-lookup"><span data-stu-id="67397-390">Use this task to have an adequate balance in the default currency on the reporting date when the operations are entered in foreign currencies.</span></span> <span data-ttu-id="67397-391">Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte grynųjų pinigų sąskaitą, kurios užduotį norite vykdyti.</span><span class="sxs-lookup"><span data-stu-id="67397-391">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="67397-392">Užduoties dialogo lange naudokite laukus <strong>Iš valiutos</strong> ir <strong>Į valiutą</strong>, kad nurodytumėte operacijos valiutas.</span><span class="sxs-lookup"><span data-stu-id="67397-392">In the dialog box for the task, use the <strong>From currency</strong> and <strong>To Currency</strong> fields to specify transaction currencies.</span></span> <span data-ttu-id="67397-393">Sistema palygina sumą valiuta, kuri buvo konvertuota naudojant valiutos kursą pasirinktą dieną, su suma numatytąja valiuta.</span><span class="sxs-lookup"><span data-stu-id="67397-393">The system compares the amount in the currency that was converted by using exchange rate on the selected date with the amount in the default currency.</span></span> <span data-ttu-id="67397-394">Abiejų sumų skirtumas (neįskaitant ankstesnio derinimo dėl valiutos kurso) yra apskaičiuotas derinimas dėl valiutos kurso.</span><span class="sxs-lookup"><span data-stu-id="67397-394">The difference between the two amounts (excluding the previous exchange adjustment) is the calculated exchange adjustment.</span></span> <span data-ttu-id="67397-395">Ši užduotis sukuria patvirtintą grynųjų pinigų operaciją, kurios tipas <strong>Derinimas dėl valiutos kurso</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-395">This task creates an approved cash transaction of the <strong>Exchange adjustment</strong> type.</span></span> <span data-ttu-id="67397-396">DK operacija suformuojama naudojant grynųjų pinigų DK sąskaitą ir DK sąskaitą, nurodytą lentelės <strong>Valiuta</strong> lauke <strong>Nerealizuotas pelnas</strong> arba <strong>Nerealizuoti nuostoliai</strong>.</span><span class="sxs-lookup"><span data-stu-id="67397-396">The ledger transaction is formed by using the ledger account for cash and the ledger account that is specified in <strong>Unrealized profit</strong> or <strong>Unrealized loss</strong> in the <strong>Currency</strong> table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a><span data-ttu-id="67397-397">Užklausos ir ataskaitos</span><span class="sxs-lookup"><span data-stu-id="67397-397">Inquiries and reports</span></span>

| <span data-ttu-id="67397-398">Užklausa arba ataskaita</span><span class="sxs-lookup"><span data-stu-id="67397-398">Inquiry or report</span></span>                             | <span data-ttu-id="67397-399">aprašymas</span><span class="sxs-lookup"><span data-stu-id="67397-399">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67397-400">Grynųjų pinigų operacijų rodinys</span><span class="sxs-lookup"><span data-stu-id="67397-400">Cash transactions view</span></span>                        | <span data-ttu-id="67397-401">Tvarkydami važtaraščių žurnalo eilutę, naudokite veiksmų mygtuką **Užklausos**, kad peržiūrėtumėte DK operacijas, grynųjų pinigų balansą ir kitą informaciją.</span><span class="sxs-lookup"><span data-stu-id="67397-401">For a Slip journal line, use the **Inquiries** button on the Action Pane to view ledger transactions, the cash balance, and other information.</span></span>                                                                                  |
| <span data-ttu-id="67397-402">Operacija grynaisiais</span><span class="sxs-lookup"><span data-stu-id="67397-402">Cash transaction</span></span>                              | <span data-ttu-id="67397-403">Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Grynųjų pinigų operacijos**, kad peržiūrėtumėte grynųjų pinigų operacijas.</span><span class="sxs-lookup"><span data-stu-id="67397-403">Go to **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash transactions** to view cash transactions.</span></span> <span data-ttu-id="67397-404">Naudokite funkciją **Filtras**, kad nurodytumėte papildomus grynųjų pinigų operacijų pasirinkimo ribojimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="67397-404">Use the **Filter** function to specify additional criteria to limit the selection of cash transactions.</span></span> |
| <span data-ttu-id="67397-405">Registravimo žurnalas (skirta Estijai, Rusijai)</span><span class="sxs-lookup"><span data-stu-id="67397-405">Journal of registration (for Estonia, Russia)</span></span> | <span data-ttu-id="67397-406">Ataskaitoje, kurią galima peržiūrėti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Registravimo žurnalas**, nurodomi visi išduoti grynųjų pinigų kompensavimo ir grynųjų pinigų išmokėjimo kvitai.</span><span class="sxs-lookup"><span data-stu-id="67397-406">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Journal of registration** reflects all cash reimbursement and cash disbursement slips that have been issued.</span></span>                                   |
| <span data-ttu-id="67397-407">Kasos knyga (skirta Latvijai, Lietuvai, Rusijai)</span><span class="sxs-lookup"><span data-stu-id="67397-407">Cash book (for Latvia, Lithuania, Russia)</span></span>     | <span data-ttu-id="67397-408">Ataskaitoje, kurią galima peržiūrėti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Kasos knygos ataskaita**, nurodomi faktiniai grynųjų pinigų lėšų perkėlimai (gavimai ir išlaidos).</span><span class="sxs-lookup"><span data-stu-id="67397-408">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash book report** reflects actual cash fund movements (receipts and expenditures).</span></span>                                                            |





