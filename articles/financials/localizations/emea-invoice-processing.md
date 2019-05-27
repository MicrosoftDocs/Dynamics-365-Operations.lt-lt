---
title: SF apdorojimas
description: Šioje temoje pateikiama informacijos apie sąskaitų faktūrų apdorojimą Rytų Europoje.
author: v-kikozl
manager: AnnBe
ms.date: 07/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-kikozl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7b8279531d932a1c3cac75d2f72766475465345a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1538124"
---
# <a name="invoice-processing"></a><span data-ttu-id="3632f-103">SF apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3632f-103">Invoice processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3632f-104">Šioje temoje trumpai aprašomi keli konkrečių šalių scenarijai, pvz., ES vidaus pridėtinės vertės mokestis (PVM) ir atidėtas mokestis.</span><span class="sxs-lookup"><span data-stu-id="3632f-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="3632f-105">Sąskaitų faktūrų išrašymo procesui taikomi kai kurių Europos šalių teisiniai reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="3632f-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="3632f-106">Šioje temoje taip pat pateikiama informacijos apie tai, kaip šiose šalyse apdorojamos klientų ir tiekėjų sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="3632f-106">This topic provides also an information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="3632f-107">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="3632f-107">Scenario</span></span></th>
<th><span data-ttu-id="3632f-108">Šalys</span><span class="sxs-lookup"><span data-stu-id="3632f-108">Countries</span></span></th>
<th><span data-ttu-id="3632f-109">Funkcijų pakeitimų aprašas</span><span class="sxs-lookup"><span data-stu-id="3632f-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3632f-110"> PVM gautinų sumų ir mokėtinų sumų datos</span><span class="sxs-lookup"><span data-stu-id="3632f-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="3632f-111">Čekija, Lenkija</span><span class="sxs-lookup"><span data-stu-id="3632f-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="3632f-112">Prekes perkant iš Europos Sąjungos (ES) šalių, taikomas įsipareigojimas PVM įvertinti patiems.</span><span class="sxs-lookup"><span data-stu-id="3632f-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-113">Mokėtiną PVM reikia sumokėti per PVM laikotarpį, kuriuo išduota sąskaita faktūra (dokumento data).</span><span class="sxs-lookup"><span data-stu-id="3632f-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="3632f-114">Gautino PVM negalima atskaityti prieš gaunant dokumentą (PVM registro data).</span><span class="sxs-lookup"><span data-stu-id="3632f-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="3632f-115">Kad būtų galima taikyti šį scenarijų, reikia sukonfigūruoti tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="3632f-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-116">Puslapyje <strong>Mokėtinų sumų parametrai</strong> įjunkite parametrus <strong>ES vidaus PVM</strong> ir <strong>ES vidaus PVM dokumento data</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="3632f-117">Nustatykite du PVM kodus, vieną – su teigiamu PVM procentu ir vieną – su neigiamu.</span><span class="sxs-lookup"><span data-stu-id="3632f-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="3632f-118">Nustatykite PVM grupę, kurioje būtų tiek teigiami, tiek neigiami PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="3632f-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="3632f-119">Neigiamo PVM kodo parametrą <strong>ES vidaus PVM</strong> nustatykite kaip <strong>Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="3632f-120">Sėkmingai tai nustačius, perkant bus registruojamos dvi tolesnės PVM operacijos.</span><span class="sxs-lookup"><span data-stu-id="3632f-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-121">Teigiama operacija su <strong>gautino PVM</strong> kryptimi ir PVM registro data, lygia sąskaitos faktūros registravimo puslapyje nurodytai datai.</span><span class="sxs-lookup"><span data-stu-id="3632f-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="3632f-122">Neigiama operacija su <strong>mokėtino PVM</strong> kryptimi ir PVM registro data, lygia dokumento datai.</span><span class="sxs-lookup"><span data-stu-id="3632f-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3632f-123">Modifikuokite pardavimo dokumento datą.</span><span class="sxs-lookup"><span data-stu-id="3632f-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="3632f-124">Visos Rytų Europos šalys</span><span class="sxs-lookup"><span data-stu-id="3632f-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="3632f-125">Galite modifikuoti projekto sąskaitos faktūros lauką <strong>Dokumento data</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="3632f-126">Ši data rodoma išspausdintoje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="3632f-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="3632f-127">Laukas <strong>Dokumento data</strong> taip pat yra puslapiuose <strong>Registravimo sąskaita faktūra</strong> ir <strong>Laisvos formos sąskaita faktūra</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="3632f-128">Užregistravus sąskaitą faktūrą, dokumento data rodoma jos antraštėje.</span><span class="sxs-lookup"><span data-stu-id="3632f-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3632f-129">Valiutų kursų dokumento data</span><span class="sxs-lookup"><span data-stu-id="3632f-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="3632f-130">Lenkija, Vengrija, Čekija</span><span class="sxs-lookup"><span data-stu-id="3632f-130">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="3632f-131">Teisės aktuose nurodytos skirtingos taisyklės, taikomos renkantis verslo operacijoms tinkamus valiutų kursus.</span><span class="sxs-lookup"><span data-stu-id="3632f-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="3632f-132">Puslapiuose <strong>Gautinų sumų parametrai</strong> ir <strong>Mokėtinų sumų parametrai</strong> esančiame lauke <strong>Valiutos kurso data</strong> galite pasirinkti datą, kurią reikia naudoti su sumomis skaičiuojant apskaitos valiutą pirkimo ir pardavimo dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="3632f-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="3632f-133">Kai įvedami duomenys, sistema pagal šį parametrą gauna operacijos valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="3632f-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="3632f-134">Kai lauką <strong>Valiutos kurso data</strong> nustatote kaip <strong>Dokumento data (tik ES prekybai)</strong>, sistema naudoja PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="3632f-134">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="3632f-135">PVM grupės skirtuke <strong>Bendra</strong> yra parametras <strong>ES prekyba</strong>. Jei PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Taip</strong> ir jei ši PVM grupė nurodyta dokumento antraštėje, sistema valiutos kursą gauna pagal dokumento datą.</span><span class="sxs-lookup"><span data-stu-id="3632f-135">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="3632f-136">Jei šios PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Ne</strong>, sistema valiutos kursą gauna pagal dokumento registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="3632f-136">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="3632f-137">Prekybos datų, PVM registro datų ir dokumentų bei PVM datų valdymas</span><span class="sxs-lookup"><span data-stu-id="3632f-137">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="3632f-138">Lenkija, Vengrija, Čekija</span><span class="sxs-lookup"><span data-stu-id="3632f-138">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="3632f-139">Pardavimo datą ir dokumento gavimo datą būtina nurodyti teikiant PVM ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="3632f-139">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-140">Pardavimo data – tai operacijos įvykdymo data modulyje Gautinos sumos.</span><span class="sxs-lookup"><span data-stu-id="3632f-140">The sales date is the fulfilment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="3632f-141">Dokumento gavimo data – tai data, kuri parodo teisę reikalauti PVM atskaitymo modulyje Mokėtinos sumos.</span><span class="sxs-lookup"><span data-stu-id="3632f-141">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="3632f-142">Kiekviename gautame dokumente audito tikslais nurodyta data.</span><span class="sxs-lookup"><span data-stu-id="3632f-142">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="3632f-143">Į Vengrijos datų terminų funkcijas, Čekijos įvykdymo datų funkcijas ir Lenkijos PVM registravimo datų funkcijas įtrauktas mokesčių informacijos ataskaitų reikalavimas, paremtas data, kuri skiriasi nuo registravimo datos.</span><span class="sxs-lookup"><span data-stu-id="3632f-143">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="3632f-144">Laukas <strong>PVM registro data</strong> palaiko šį reikalavimą ir yra rodomas daugiau nei 20-yje puslapių.</span><span class="sxs-lookup"><span data-stu-id="3632f-144">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="3632f-145">Šie puslapiai – tai žurnalai, pardavimo užsakymai, pirkimo užsakymai, laisvos formos sąskaitos faktūros, tiekėjų sąskaitų faktūrų žurnalai ir projektų sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="3632f-145">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="3632f-146">Kai atnaujinate ar registruojate dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data įtraukiama į puslapius, pvz., klientų ir tiekėjų sąskaitų faktūrų žurnalų puslapius.</span><span class="sxs-lookup"><span data-stu-id="3632f-146">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="3632f-147">Konkrečiai Čekijoje, jei PVM registravimas atidedamas, registravimo metu laukas <strong>PVM registro data</strong> gali būti tuščias.</span><span class="sxs-lookup"><span data-stu-id="3632f-147">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="3632f-148">Kitu atveju laukas yra privalomas ir jį reikia užpildyti.</span><span class="sxs-lookup"><span data-stu-id="3632f-148">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="3632f-149">Datos tikrinimo parametrus galima nustatyti puslapyje <strong>PVM grupės</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-149">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-150">Parametrai <strong>PVM registro pildymo data</strong> ir <strong>Pardavimo datos pildymas</strong> naudojami kaip numatytasis atitinkamų datų pildymo būdas.</span><span class="sxs-lookup"><span data-stu-id="3632f-150">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="3632f-151">Taip pat galima naudoti rankinės įvesties ir kelis automatinės įvesties būdus.</span><span class="sxs-lookup"><span data-stu-id="3632f-151">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="3632f-152">Laukas <strong>Privaloma pardavimo data</strong> nurodo, ar, prieš registruojant pardavimo sąskaitą faktūrą, reikia įvesti pardavimo datą.</span><span class="sxs-lookup"><span data-stu-id="3632f-152">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="3632f-153">Puslapyje <strong>PVM registro operacijos</strong> galite užpildyti tuščius registruotų mokesčių operacijų PVM registro datų laukus.</span><span class="sxs-lookup"><span data-stu-id="3632f-153">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3632f-154">PVM registravimo datos, į kurias įtraukti atidėti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="3632f-154">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="3632f-155">Vengrija</span><span class="sxs-lookup"><span data-stu-id="3632f-155">Hungary</span></span></td>
<td>
<p><span data-ttu-id="3632f-156">Pagal Vengrijos mokesčių įstatymų reikalavimus sąskaitas faktūras reikia sukurti jų įvykdymo metu arba ne vėliau kaip per 15 dienų po įvykdymo.</span><span class="sxs-lookup"><span data-stu-id="3632f-156">Hungary tax regulations require that invoices be created at either the time of fulfilment or no later than 15 days after fulfilment.</span></span></p>
<p><span data-ttu-id="3632f-157">Įvykdymo data yra užsakytų paslaugų suteikimo data arba užsakytų prekių pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="3632f-157">The fulfilment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="3632f-158">Atnaujinant ar registruojant dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data rodoma atitinkamuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="3632f-158">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="3632f-159">Be to, pagal reikalavimus, nuolat teikiant paslaugas, pvz., nuomos, konsultavimo ar šildymo, PVM turi atitikti tolesnius kriterijus.</span><span class="sxs-lookup"><span data-stu-id="3632f-159">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-160">PVM sąskaitos faktūros dieną turi būti registruojamas paskirtoje DK sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="3632f-160">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="3632f-161">PVM termino dieną turi būti perkeltas iš specialių sąskaitų į gautino arba mokėtino PVM sąskaitą ir jį reikia įtraukti į PVM ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3632f-161">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="3632f-162">Kad galėtumėte įvykdyti šiuos reikalavimus, didžiosios knygos registravimus galite perkelti į atidėtų gaunamų mokesčių sąskaitą ir atidėtų išmokamų mokesčių sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3632f-162">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="3632f-163">Tačiau pirmiausia turite įvykdyti tolesnes būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="3632f-163">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="3632f-164">Didžiosios knygos registravimo grupėse nustatyti atidėto mokėtino PVM ir atidėto gautino PVM DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="3632f-164">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="3632f-165">Įjungti prekių PVM grupių parametrą <strong>Atidėtas PVM</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-165">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="3632f-166"> Privaloma PVM data</span><span class="sxs-lookup"><span data-stu-id="3632f-166">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="3632f-167">Lenkija</span><span class="sxs-lookup"><span data-stu-id="3632f-167">Poland</span></span></td>
<td>
<p><span data-ttu-id="3632f-168">Galite reikalauti, kad PVM registro data būtų įtraukta į pirkimo ir pardavimo operacijų įrašus.</span><span class="sxs-lookup"><span data-stu-id="3632f-168">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="3632f-169">Todėl PVM registro datą galima užfiksuoti prieš užregistruojant operaciją.</span><span class="sxs-lookup"><span data-stu-id="3632f-169">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="3632f-170">Naudojant šią funkciją galima išvengti situacijos, kai laikotarpio pabaigoje reikia tvarkyti kelias operacijas.</span><span class="sxs-lookup"><span data-stu-id="3632f-170">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="3632f-171">Lauką <strong>PVM registro data</strong> galite padaryti privalomą registruojant klientų ar tiekėjų operacijas.</span><span class="sxs-lookup"><span data-stu-id="3632f-171">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="3632f-172">Norėdami šį lauką padaryti privalomą, įjunkite susijusios kliento ar tiekėjo sąskaitos parinktį <strong>Būtina nurodyti PVM datą</strong>.</span><span class="sxs-lookup"><span data-stu-id="3632f-172">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>
