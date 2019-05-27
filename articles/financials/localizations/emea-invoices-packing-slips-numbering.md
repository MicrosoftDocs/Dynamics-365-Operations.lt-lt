---
title: SF ir važtaraščių numeravimas (Latvija ir Lietuva)
description: Šioje temoje paaiškinama, kaip nustatyti SF bei važtaraščių numeraciją ir kaip nustatyti automatinio dokumento numeravimo diapazonus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, NumberSequenceTableListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 268484
ms.search.region: Latvia, Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f0650bbcd51397ce3eade895bfcafff7a2a59518
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538131"
---
# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a><span data-ttu-id="1419d-103">SF ir važtaraščių numeravimas (Latvija ir Lietuva)</span><span class="sxs-lookup"><span data-stu-id="1419d-103">Invoice and packing slip numbering for Latvia and Lithuania</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1419d-104">Šioje temoje paaiškinama, kaip nustatyti SF bei važtaraščių numeraciją ir kaip nustatyti automatinio dokumento numeravimo diapazonus.</span><span class="sxs-lookup"><span data-stu-id="1419d-104">This topic explains how to set up number sequences for invoices and packing slips, and how to set up self-numbering ranges for documents.</span></span>

<span data-ttu-id="1419d-105">Jei juridinio subjekto pagrindinis adresas yra Latvijoje arba Lietuvoje, galite nustatyti sąlyginę SF ir važtaraščių numeravimo funkciją, pagrįstą priskirtu vartotoju arba vartotojų grupe.</span><span class="sxs-lookup"><span data-stu-id="1419d-105">For legal entities that have a primary address in Latvia or Lithuania, you can set up conditional numbering for invoices and packing slips that is based on the assigned user or user group.</span></span>

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a><span data-ttu-id="1419d-106">SF ir važtaraščių numeracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="1419d-106">Set up number sequences for invoices and packing slips</span></span>
<span data-ttu-id="1419d-107">Galite nustatyti unikalias dokumentų numeracijas, skirtas bendrųjų duomenų įrašams ir operacijų įrašams.</span><span class="sxs-lookup"><span data-stu-id="1419d-107">You can set up unique document number sequences for master data records and transaction records.</span></span> <span data-ttu-id="1419d-108">Jei jūsų šalies ar regiono mokesčių rinkėjai jūsų organizacijai priskiria specifinę dokumentų numeraciją arba formatą, galite numeraciją susieti su dokumento tipu.</span><span class="sxs-lookup"><span data-stu-id="1419d-108">If the tax authorities for your country or region assign your organization a specific document number sequence or format, you can associate the number sequence with a document type.</span></span> <span data-ttu-id="1419d-109">Kiekvieną dokumentų numeraciją galite priskirti vartotojui arba vartotojų grupei.</span><span class="sxs-lookup"><span data-stu-id="1419d-109">You can assign each document number sequence to a user or user group.</span></span> <span data-ttu-id="1419d-110">Tokiu būtu tik pasirinktas vartotojas arba vartotojų grupė gali priskirti sekos numerius dokumentui.</span><span class="sxs-lookup"><span data-stu-id="1419d-110">In this way, only the designated user or user group can assign the numbers in the series to a document.</span></span> <span data-ttu-id="1419d-111">SF ir važtaraščių numeracijas galite nustatyti puslapyje **SF numeravimo nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="1419d-111">You can set up number sequences for invoices and packing slips on the **Invoice numbering setup** page.</span></span> <span data-ttu-id="1419d-112">(Spustelėkite **Organizacijos administravimas** &gt; **Numeracijos** &gt; **SF numeravimo nustatymas**.) Naudokite tolesnėje lentelėje pateiktą informaciją, kad užpildytumėte puslapio **SF numeravimo nustatymas** laukus.</span><span class="sxs-lookup"><span data-stu-id="1419d-112">(Click **Organization administration** &gt; **Number sequences** &gt; **Invoice numbering setup**.) Use the information in the following table to complete the fields on the **Invoice numbering setup** page.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1419d-113">Laukas</span><span class="sxs-lookup"><span data-stu-id="1419d-113">Field</span></span></th>
<th><span data-ttu-id="1419d-114">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1419d-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1419d-115">Numeravimas</span><span class="sxs-lookup"><span data-stu-id="1419d-115">Numbering</span></span></td>
<td><span data-ttu-id="1419d-116">Įveskite dokumentų numeracijos priešvardį.</span><span class="sxs-lookup"><span data-stu-id="1419d-116">Enter the prefix for the document number sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1419d-117">Modulis</span><span class="sxs-lookup"><span data-stu-id="1419d-117">Module</span></span></td>
<td><span data-ttu-id="1419d-118">Pasirinkite modulį, kuris naudos numerių seką.</span><span class="sxs-lookup"><span data-stu-id="1419d-118">Select the module that will use the number series.</span></span> <span data-ttu-id="1419d-119">Pasirinktas modulis nustato, kokias parinktis galima pasirinkti lauke <strong>Tipas</strong>.</span><span class="sxs-lookup"><span data-stu-id="1419d-119">The module that you select determines the options that are available in the <strong>Type</strong> field.</span></span> <span data-ttu-id="1419d-120">Jei tvarkote kliento SF ir kliento važtaraščius, šiame lauke pasirinkite <strong>Pardavimas</strong>.</span><span class="sxs-lookup"><span data-stu-id="1419d-120">For customer invoices and customer packing slips, select <strong>Sales</strong> in this field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1419d-121">Numeracijos kodas</span><span class="sxs-lookup"><span data-stu-id="1419d-121">Number sequence code</span></span></td>
<td><span data-ttu-id="1419d-122">Pasirinkite duomenų srities, kuriai numerių seka taikoma, numeracijos kodą.</span><span class="sxs-lookup"><span data-stu-id="1419d-122">Select the number sequence code for the data area where the number series is applied.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1419d-123">Tipas</span><span class="sxs-lookup"><span data-stu-id="1419d-123">Type</span></span></td>
<td><span data-ttu-id="1419d-124">Pasirinkite, ar numeracija taikoma SF, ar važtaraščiams.</span><span class="sxs-lookup"><span data-stu-id="1419d-124">Select whether the number sequence applies to invoices or packing slips.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1419d-125">Sąskaitos kodas</span><span class="sxs-lookup"><span data-stu-id="1419d-125">Account code</span></span></td>
<td><span data-ttu-id="1419d-126">Pasirinkite, kaip numerių seka taikoma SF.</span><span class="sxs-lookup"><span data-stu-id="1419d-126">Select how the number series is applied to invoices.</span></span> <span data-ttu-id="1419d-127">Galimos toliau nurodytos pasirinktys:</span><span class="sxs-lookup"><span data-stu-id="1419d-127">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="1419d-128"><strong>Lentelė</strong> – numerių seką gali naudoti tik lauke <strong>Kodas</strong> pasirinktas vartotojas.</span><span class="sxs-lookup"><span data-stu-id="1419d-128"><strong>Table</strong> – The number series is available only to the user that is selected in the <strong>Code</strong> field.</span></span></li>
<li><span data-ttu-id="1419d-129"><strong>Grupė</strong> – numerių seką gali naudoti lauke <strong>Kodas</strong> pasirinkta vartotojų grupė.</span><span class="sxs-lookup"><span data-stu-id="1419d-129"><strong>Group</strong> – The number series is available to the user group that is selected in the <strong>Code</strong> field.</span></span></li>
<li><span data-ttu-id="1419d-130"><strong>Visi</strong> – numerių seką gali naudoti visi vartotojai.</span><span class="sxs-lookup"><span data-stu-id="1419d-130"><strong>All</strong> – The number series is available to all users.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1419d-131">Kodas</span><span class="sxs-lookup"><span data-stu-id="1419d-131">Code</span></span></td>
<td><span data-ttu-id="1419d-132">Pasirinkite vartotojo arba vartotojų grupės, kuriai numerių seka priskirta SF sunumeruoti, ID.</span><span class="sxs-lookup"><span data-stu-id="1419d-132">Select the ID of the user or user group that the number series is assigned to for invoice numbering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1419d-133">Paskutinė data</span><span class="sxs-lookup"><span data-stu-id="1419d-133">Last date</span></span></td>
<td><span data-ttu-id="1419d-134">Diena, kurią numerių seka buvo paskutinį kartą atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="1419d-134">The date that the number series was last updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1419d-135">Tęsti</span><span class="sxs-lookup"><span data-stu-id="1419d-135">Continue</span></span></td>
<td><span data-ttu-id="1419d-136">Pasirinktie šią parinktį, kad ieškotumėte numerių sekos, kuri priskirta pasirinktam vartotojui arba vartotojų grupei.</span><span class="sxs-lookup"><span data-stu-id="1419d-136">Select this option to search for number series that are assigned to the selected user or user group.</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-document-self-numbering-ranges"></a><span data-ttu-id="1419d-137">Automatinio dokumento numeravimo diapazonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1419d-137">Set up document self-numbering ranges</span></span>
<span data-ttu-id="1419d-138">Galite priskirti konkrečias numerių sekas SF ir važtaraščiams, kurie yra generuojami moduliuose **Gautinos sumos**, **Mokėtinos sumos**, **Atsargų valdymas** ir **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="1419d-138">You can assign specific number sequences to invoices and packing slips that are generated in the **Accounts receivable**, **Accounts payable**, **Inventory management**, and **Project management and accounting** modules.</span></span> <span data-ttu-id="1419d-139">Taip pat galite nurodyti atskiras numeracijas ir priskirti skirtingiems vartotojams ir vartotojų grupėms, klientų ir tiekėjų grupėms arba sandėliams.</span><span class="sxs-lookup"><span data-stu-id="1419d-139">You can also specify individual number sequences for different users and user groups, customer groups and vendor groups, or warehouses.</span></span> <span data-ttu-id="1419d-140">Norėdami nustatyti kliento SF ir tiekėjo SF numeracijas, naudokite puslapį **Skaitiklių valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1419d-140">To set up number sequences for customer invoices and vendor invoices, use the **Counters management** page.</span></span> <span data-ttu-id="1419d-141">(Spustelėkite **Organizacijos administravimas** &gt; **Numeracijos** &gt; **Skaitiklių valdymas**.) Numeraciją galite nustatyti pagal vartotoją ar vartotojų grupę arba pagal konkrečias klientų grupes ir tiekėjų grupes.</span><span class="sxs-lookup"><span data-stu-id="1419d-141">(Click **Organization administration** &gt; **Number sequences** &gt; **Counters management**.) You can define the number sequence by user or user group, or for specific customer groups and vendor groups.</span></span> <span data-ttu-id="1419d-142">Naudokite tolesnėje lentelėje pateiktą informaciją, kad užpildytumėte laukus puslapyje **Skaitiklių valdymas**.</span><span class="sxs-lookup"><span data-stu-id="1419d-142">Use the information in the following table to complete the fields on the **Counters management** page.</span></span>

| <span data-ttu-id="1419d-143">Laukas</span><span class="sxs-lookup"><span data-stu-id="1419d-143">Field</span></span>          | <span data-ttu-id="1419d-144">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1419d-144">Description</span></span>                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1419d-145">Modulis</span><span class="sxs-lookup"><span data-stu-id="1419d-145">Module</span></span>         | <span data-ttu-id="1419d-146">Pasirinkite modulį, kuriam taikoma pasirinkta numeracija.</span><span class="sxs-lookup"><span data-stu-id="1419d-146">Select the module that the selected number sequence applies to.</span></span>                                                                                 |
| <span data-ttu-id="1419d-147">Sąskaitos kodas</span><span class="sxs-lookup"><span data-stu-id="1419d-147">Account code</span></span>   | <span data-ttu-id="1419d-148">Pasirinkite, ar numeracijos kodas taikomas visiems pasirinkto modulio įrašams, ar konkrečiai modulio grupei.</span><span class="sxs-lookup"><span data-stu-id="1419d-148">Select whether the number sequence code applies to all records in the selected module or to a specific group in the module.</span></span>                     |
| <span data-ttu-id="1419d-149">Kodas</span><span class="sxs-lookup"><span data-stu-id="1419d-149">Code</span></span>           | <span data-ttu-id="1419d-150">Pasirinkite pasirinkto modulio kodą.</span><span class="sxs-lookup"><span data-stu-id="1419d-150">Select the code for the selected module.</span></span> <span data-ttu-id="1419d-151">**Pastaba.** Lauką **Kodas** galima naudoti tik jei lauke **Sąskaitos kodas** pasirinkta parinktis **Grupė**.</span><span class="sxs-lookup"><span data-stu-id="1419d-151">**Note:** The **Code** field is available only if **Group** is selected in the **Account code** field.</span></span> |
| <span data-ttu-id="1419d-152">Tipas</span><span class="sxs-lookup"><span data-stu-id="1419d-152">Type</span></span>           | <span data-ttu-id="1419d-153">Pasirinkite dokumento tipą, kurį reikia numeruoti: **SF** arba **Važtaraštis**.</span><span class="sxs-lookup"><span data-stu-id="1419d-153">Select the type of document to number: **Invoice** or **Packing slip**.</span></span>                                                                         |
| <span data-ttu-id="1419d-154">Automatinis numeravimas</span><span class="sxs-lookup"><span data-stu-id="1419d-154">Auto numbering</span></span> | <span data-ttu-id="1419d-155">Pažymėkite šią parinktį, jei norite dokumentui numerį priskirti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1419d-155">Select this option to automatically assign a number to a document.</span></span> <span data-ttu-id="1419d-156">Galite neautomatiškai pažymėti arba atžymėti šią parinktį atskiriems dokumentams.</span><span class="sxs-lookup"><span data-stu-id="1419d-156">You can manually select or clear this option for individual documents.</span></span>       |

<span data-ttu-id="1419d-157">Daugiau informacijos apie tai, kaip neautomatiškai numeruoti SF ir važtaraščius, žr. [Pardavimo užsakymų SF ID redagavimas](emea-edit-invoice-id-sales-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1419d-157">For information about how to manually number invoices and packing slips, see [Edit invoice ID on Sales orders](emea-edit-invoice-id-sales-orders.md).</span></span>

## <a name="affected-processes"></a><span data-ttu-id="1419d-158">Paveikti procesai</span><span class="sxs-lookup"><span data-stu-id="1419d-158">Affected processes</span></span>
<span data-ttu-id="1419d-159">Toliau pateiktų dokumentų antraštės atnaujinamos naudojant SF ir važtaraščių numeraciją.</span><span class="sxs-lookup"><span data-stu-id="1419d-159">The headers of the following documents are updated with invoice and packing slip numbering:</span></span>

-   <span data-ttu-id="1419d-160">Pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="1419d-160">Sales orders</span></span>
-   <span data-ttu-id="1419d-161">Pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="1419d-161">Purchase orders</span></span>
-   <span data-ttu-id="1419d-162">Laisvos formos sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="1419d-162">Free text invoices</span></span>
-   <span data-ttu-id="1419d-163">Projekto SF pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="1419d-163">Project invoice proposals</span></span>

<span data-ttu-id="1419d-164">Kai registruojate toliau nurodytus dokumentus, galite pasirinkti konkrečia numeraciją lauke **Numeravimas**.</span><span class="sxs-lookup"><span data-stu-id="1419d-164">When you post the following documents, you can select a specific number sequence in the **Numbering** field:</span></span>

-   <span data-ttu-id="1419d-165">Pardavimo važtaraštis</span><span class="sxs-lookup"><span data-stu-id="1419d-165">Sales packing slip</span></span>
-   <span data-ttu-id="1419d-166">Pardavimo registravimo SF</span><span class="sxs-lookup"><span data-stu-id="1419d-166">Sales posting invoice</span></span>
-   <span data-ttu-id="1419d-167">Pirkimo registravimo produkto gavimo dokumentas</span><span class="sxs-lookup"><span data-stu-id="1419d-167">Purchasing posting product receipt</span></span>
-   <span data-ttu-id="1419d-168">Pirkimo tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="1419d-168">Purchasing vendor invoices</span></span>
-   <span data-ttu-id="1419d-169">Registruoti projekto SF pasiūlymus</span><span class="sxs-lookup"><span data-stu-id="1419d-169">Post project invoice proposals</span></span>
-   <span data-ttu-id="1419d-170">Registruoti laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="1419d-170">Post free text invoice</span></span>

<span data-ttu-id="1419d-171">Be to, toliau nurodytos formos pateikiamos lauke **Dokumentai atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="1419d-171">Additionally, forms below are supplemented by the **Documents to update** field:</span></span>

-   <span data-ttu-id="1419d-172">Pirkimo tiekėjo SF forma</span><span class="sxs-lookup"><span data-stu-id="1419d-172">Purchasing Vendor invoices form,</span></span>
-   <span data-ttu-id="1419d-173">Pardavimo važtaraščio registravimo forma</span><span class="sxs-lookup"><span data-stu-id="1419d-173">Sales Packing slip posting form,</span></span>
-   <span data-ttu-id="1419d-174">Pardavimo registravimo SF forma</span><span class="sxs-lookup"><span data-stu-id="1419d-174">Sales Posting invoice form,</span></span>
-   <span data-ttu-id="1419d-175">Pirkimo registravimo produkto gavimo dokumento forma</span><span class="sxs-lookup"><span data-stu-id="1419d-175">Purchasing Posting product receipt form.</span></span>

<span data-ttu-id="1419d-176">Laukas **Dokumentai naujinti** turi įtakos puslapių **Važtaraščių žurnalas** ir **SF žurnalas** lauko **Dokumento būsena** rodiniui.</span><span class="sxs-lookup"><span data-stu-id="1419d-176">The “**Documents to update**” field influences on the “**Document status**” field in “**Packing slip journal**” and "**Invoice Journal**".</span></span> <span data-ttu-id="1419d-177">Kai kuriamas **Važtaraštis** lauko **Dokumento būsena** vertė yra **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="1419d-177">On **Packing slip** creation, the “**Document status**” field value is equal to “**None**”.</span></span> <span data-ttu-id="1419d-178">Jei lauke **Dokumentai naujinti** buvo pasirinktas bet koks **Važtaraštis**, tada jo **Dokumento būsena** bus **Sugadintas**, o **važtaraščio** **Dokumento būsena** toje vietoje, kurioje jis buvo sukurtas, bus **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="1419d-178">If any **Packing slip** was chosen in field “**Documents to update**” then its “**Document status**” would be “**Broken**” and the “**Document status**” of **Packing slip** where it was done will be “**Canceled**”.</span></span>



