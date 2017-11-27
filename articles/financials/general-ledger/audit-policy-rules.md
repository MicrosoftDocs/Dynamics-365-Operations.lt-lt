---
title: "Audito strategijos taisyklės"
description: "Norėdami įvertinti išlaidų ataskaitas, tiekėjo SF ir pirkimo užsakymus ir įsitikinti, kad jie atitinka jūsų kuriamas strategijos taisyklės, galite naudoti audito strategijas. Visos su audito strategija susietos taisyklės vykdomos paketiniu režimu pagal jūsų nurodytą grafiką.  Kiekviena strategijos taisyklė yra strategijos taisyklės tipo egzempliorius. Vienu metu gali būti aktyvi tik viena strategijos taisyklės tipo strategijos taisyklė."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04217e162090720d2a48c96aa9356cea2dbfa230
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-rules"></a><span data-ttu-id="e401a-106">Audito strategijos taisyklės</span><span class="sxs-lookup"><span data-stu-id="e401a-106">Audit policy rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e401a-107">Norėdami įvertinti išlaidų ataskaitas, tiekėjo SF ir pirkimo užsakymus ir įsitikinti, kad jie atitinka jūsų kuriamas strategijos taisyklės, galite naudoti audito strategijas.</span><span class="sxs-lookup"><span data-stu-id="e401a-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="e401a-108">Visos su audito strategija susietos taisyklės vykdomos paketiniu režimu pagal jūsų nurodytą grafiką.</span><span class="sxs-lookup"><span data-stu-id="e401a-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="e401a-109">Kiekviena strategijos taisyklė yra strategijos taisyklės tipo egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="e401a-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="e401a-110">Vienu metu gali būti aktyvi tik viena strategijos taisyklės tipo strategijos taisyklė.</span><span class="sxs-lookup"><span data-stu-id="e401a-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="e401a-111">Užklausos ir užklausų tipai</span><span class="sxs-lookup"><span data-stu-id="e401a-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="e401a-112">Kai kuriate audito strategijos taisyklę, pirmiausia pasirenkate strategijos taisyklės tipą.</span><span class="sxs-lookup"><span data-stu-id="e401a-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="e401a-113">Strategijos taisyklės tipas nurodo programos objektų medžio (AOT) užklausą, kuri turi būti naudojama kaip pradinis strategijos taisyklės kūrimo taškas.</span><span class="sxs-lookup"><span data-stu-id="e401a-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="e401a-114">Jis taip pat nurodo naudotiną strategijos taisyklės užklausos tipą.</span><span class="sxs-lookup"><span data-stu-id="e401a-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="e401a-115">Užklausa nurodo šaltinio dokumentą, kurį įvertina strategijos taisyklė.</span><span class="sxs-lookup"><span data-stu-id="e401a-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="e401a-116">Ji taip pat apibrėžia šaltinio dokumento laukus, nurodančius juridinį subjektą ir datą, kurie bus naudojami pasirinkus dokumentus auditui atlikti.</span><span class="sxs-lookup"><span data-stu-id="e401a-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="e401a-117">Užklausos tipas valdo numatytuosius laukus užklausos puslapyje ir audito strategijos taisyklių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e401a-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="e401a-118">Toliau pateiktoje lentelėje nurodyti galimi audito strategijos taisyklių užklausų tipai.</span><span class="sxs-lookup"><span data-stu-id="e401a-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e401a-119">Užklausos tipas</span><span class="sxs-lookup"><span data-stu-id="e401a-119">Query type</span></span></th>
<th><span data-ttu-id="e401a-120">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="e401a-120">Purpose</span></span></th>
<th><span data-ttu-id="e401a-121">Daugiau informacijos</span><span class="sxs-lookup"><span data-stu-id="e401a-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e401a-122">Sąlyginis</span><span class="sxs-lookup"><span data-stu-id="e401a-122">Conditional</span></span></td>
<td><span data-ttu-id="e401a-123">Įvertinti šaltinio dokumento atributus pagal nurodytas vertes.</span><span class="sxs-lookup"><span data-stu-id="e401a-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e401a-124">Agreguoti</span><span class="sxs-lookup"><span data-stu-id="e401a-124">Aggregate</span></span></td>
<td><span data-ttu-id="e401a-125">Įvertinti kelis šaltinio dokumentus arba šaltinio dokumento eilutes pagal strategijos taisyklę sudedant skaitines vertes.</span><span class="sxs-lookup"><span data-stu-id="e401a-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e401a-126">Pavyzdžio ėmimas</span><span class="sxs-lookup"><span data-stu-id="e401a-126">Sampling</span></span></td>
<td><span data-ttu-id="e401a-127">Atsitiktine tvarka pasirinkti nurodytą šaltinio dokumentų procentinį dydį strategijos pažeidimams įvertinti.</span><span class="sxs-lookup"><span data-stu-id="e401a-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="e401a-128">Kai pasirenkate šią parinktį, naudokite audito strategijos taisyklių puslapį, nurodydami, kiek procentų dokumentų reikia atsitiktine tvarka pasirinkti auditui.</span><span class="sxs-lookup"><span data-stu-id="e401a-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e401a-129">Dublikatas</span><span class="sxs-lookup"><span data-stu-id="e401a-129">Duplicate</span></span></td>
<td><span data-ttu-id="e401a-130">Įvertinti šaltinio dokumentus, siekiant nustatyti, ar nurodytuose jų laukuose yra įrašų dublikatų.</span><span class="sxs-lookup"><span data-stu-id="e401a-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="e401a-131">Kai pasirenkate šią parinktį, naudokite audito strategijos taisyklių puslapį, kad nurodytumėte, kiek dienų įtraukti į dokumentų pasirinkimo datų intervalo pradžią, kai įvertinama, ar dokumentuose nėra įrašų dublikatų.</span><span class="sxs-lookup"><span data-stu-id="e401a-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e401a-132">Sąrašo ieška</span><span class="sxs-lookup"><span data-stu-id="e401a-132">List search</span></span></td>
<td><span data-ttu-id="e401a-133">Įvertinti šaltinio dokumentus, ar juose yra konkrečių objektų.</span><span class="sxs-lookup"><span data-stu-id="e401a-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="e401a-134">Šakninis užklausos dokumentas apibrėžia dokumentą, kurio auditas atliekamas.</span><span class="sxs-lookup"><span data-stu-id="e401a-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="e401a-135">Užklausa turi būti sąrašo užklausa, apimanti nuorodą į „dirpartytable“ lentelę.</span><span class="sxs-lookup"><span data-stu-id="e401a-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="e401a-136">Šią parinktį galima naudoti tik su toliau nurodytomis AOT užklausomis.</span><span class="sxs-lookup"><span data-stu-id="e401a-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="e401a-137"><span class="ui">AuditPolicyExpenseList</span> (Išlaidų ataskaitoje stebimi darbuotojai)</span><span class="sxs-lookup"><span data-stu-id="e401a-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="e401a-138"><span class="ui">AuditPolicyPurchList</span> (Pirkimo užsakyme stebimi tiekėjai)</span><span class="sxs-lookup"><span data-stu-id="e401a-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="e401a-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Tiekėjo SF stebimi tiekėjai)</span><span class="sxs-lookup"><span data-stu-id="e401a-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="e401a-140">Kai pasirenkate šią parinktį, nurodykite stebimus objektus audito strategijos taisyklių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e401a-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e401a-141">Raktažodžių ieška</span><span class="sxs-lookup"><span data-stu-id="e401a-141">Keyword search</span></span></td>
<td><span data-ttu-id="e401a-142">Įvertinti šaltinio dokumentus, siekiant nustatyti, ar juose yra tam tikrų žodžių.</span><span class="sxs-lookup"><span data-stu-id="e401a-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="e401a-143">Kai pasirenkate šią parinktį, įveskite žodžius, kurių reikia ieškoti audito strategijos taisyklių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e401a-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="e401a-144">Audito strategijos taisyklių puslapyje taip pat yra parinkčių, leidžiančių nurodyti lenteles ir laukus, kuriuos norite įvertinti pagal įvestus žodžius.</span><span class="sxs-lookup"><span data-stu-id="e401a-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="e401a-145">Bendri parametrai</span><span class="sxs-lookup"><span data-stu-id="e401a-145">Common parameters</span></span>
<span data-ttu-id="e401a-146">Visos tam tikros audito strategijos taisyklės bendrai naudoja tuos pačius paketinius parametrus ir tą patį dokumentų pasirinkimo datų intervalą.</span><span class="sxs-lookup"><span data-stu-id="e401a-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="e401a-147">Šie parametrai strategijai nurodomi puslapyje „Papildomos parinktys“.</span><span class="sxs-lookup"><span data-stu-id="e401a-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="see-also"></a><span data-ttu-id="e401a-148">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="e401a-148">See also</span></span>
--------

<span data-ttu-id="e401a-149">[Audito strategijos pažeidimai ir atvejai](audit-policy-violations-cases.md)
[Apibrėžti šaltinio dokumento audito strategijas](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="e401a-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>



