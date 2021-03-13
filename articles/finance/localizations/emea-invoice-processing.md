---
title: SF apdorojimas
description: Šioje temoje pateikiama informacijos apie sąskaitų faktūrų apdorojimą Rytų Europoje.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia, Italy
ms.author: epopov
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9dcc6c4d886f34429b48a9beec458ff341e43db4
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018647"
---
# <a name="invoice-processing"></a><span data-ttu-id="8a249-103">SF apdorojimas</span><span class="sxs-lookup"><span data-stu-id="8a249-103">Invoice processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a249-104">Šioje temoje trumpai aprašomi keli konkrečių šalių scenarijai, pvz., ES vidaus pridėtinės vertės mokestis (PVM) ir atidėtas mokestis.</span><span class="sxs-lookup"><span data-stu-id="8a249-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="8a249-105">Sąskaitų faktūrų išrašymo procesui taikomi kai kurių Europos šalių teisiniai reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="8a249-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="8a249-106">Šioje temoje taip pat pateikiama informacijos apie tai, kaip šiose šalyse apdorojamos klientų ir tiekėjų sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="8a249-106">This topic also provides information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="8a249-107">Scenarijus</span><span class="sxs-lookup"><span data-stu-id="8a249-107">Scenario</span></span></th>
<th><span data-ttu-id="8a249-108">Šalys</span><span class="sxs-lookup"><span data-stu-id="8a249-108">Countries</span></span></th>
<th><span data-ttu-id="8a249-109">Funkcijų pakeitimų aprašas</span><span class="sxs-lookup"><span data-stu-id="8a249-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8a249-110">PVM gautinų sumų ir mokėtinų sumų datos</span><span class="sxs-lookup"><span data-stu-id="8a249-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="8a249-111">Čekija, Lenkija</span><span class="sxs-lookup"><span data-stu-id="8a249-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="8a249-112">Prekes perkant iš Europos Sąjungos (ES) šalių, taikomas įsipareigojimas PVM įvertinti patiems.</span><span class="sxs-lookup"><span data-stu-id="8a249-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-113">Mokėtiną PVM reikia sumokėti per PVM laikotarpį, kuriuo išduota sąskaita faktūra (dokumento data).</span><span class="sxs-lookup"><span data-stu-id="8a249-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="8a249-114">Gautino PVM negalima atskaityti prieš gaunant dokumentą (PVM registro data).</span><span class="sxs-lookup"><span data-stu-id="8a249-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="8a249-115">Kad būtų galima taikyti šį scenarijų, reikia sukonfigūruoti tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="8a249-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-116">Puslapyje <strong>Mokėtinų sumų parametrai</strong> įjunkite parametrus <strong>ES vidaus PVM</strong> ir <strong>ES vidaus PVM dokumento data</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="8a249-117">Nustatykite du PVM kodus, vieną – su teigiamu PVM procentu ir vieną – su neigiamu.</span><span class="sxs-lookup"><span data-stu-id="8a249-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="8a249-118">Nustatykite PVM grupę, kurioje būtų tiek teigiami, tiek neigiami PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="8a249-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="8a249-119">Neigiamo PVM kodo parametrą <strong>ES vidaus PVM</strong> nustatykite kaip <strong>Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="8a249-120">Sėkmingai tai nustačius, perkant bus registruojamos dvi tolesnės PVM operacijos.</span><span class="sxs-lookup"><span data-stu-id="8a249-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-121">Teigiama operacija su <strong>gautino PVM</strong> kryptimi ir PVM registro data, lygia sąskaitos faktūros registravimo puslapyje nurodytai datai.</span><span class="sxs-lookup"><span data-stu-id="8a249-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="8a249-122">Neigiama operacija su <strong>mokėtino PVM</strong> kryptimi ir PVM registro data, lygia dokumento datai.</span><span class="sxs-lookup"><span data-stu-id="8a249-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="8a249-123">Modifikuokite pardavimo dokumento datą.</span><span class="sxs-lookup"><span data-stu-id="8a249-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="8a249-124">Visos Rytų Europos šalys</span><span class="sxs-lookup"><span data-stu-id="8a249-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="8a249-125">Galite modifikuoti projekto sąskaitos faktūros lauką <strong>Dokumento data</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="8a249-126">Ši data rodoma išspausdintoje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="8a249-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="8a249-127">Laukas <strong>Dokumento data</strong> taip pat yra puslapiuose <strong>Registravimo sąskaita faktūra</strong> ir <strong>Laisvos formos sąskaita faktūra</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="8a249-128">Užregistravus sąskaitą faktūrą, dokumento data rodoma jos antraštėje.</span><span class="sxs-lookup"><span data-stu-id="8a249-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8a249-129">Valiutų kursų dokumento data</span><span class="sxs-lookup"><span data-stu-id="8a249-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="8a249-130">Lenkija, Vengrija, Čekijos Respublika, Italija</span><span class="sxs-lookup"><span data-stu-id="8a249-130">Poland, Hungary, Czech Republic, Italy</span></span></td>
<td>
<p><span data-ttu-id="8a249-131">Teisės aktuose nurodytos skirtingos taisyklės, taikomos renkantis verslo operacijoms tinkamus valiutų kursus.</span><span class="sxs-lookup"><span data-stu-id="8a249-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="8a249-132">Puslapiuose <strong>Gautinų sumų parametrai</strong> ir <strong>Mokėtinų sumų parametrai</strong> esančiame lauke <strong>Valiutos kurso data</strong> galite pasirinkti datą, kurią reikia naudoti su sumomis skaičiuojant apskaitos valiutą pirkimo ir pardavimo dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="8a249-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="8a249-133">Kai įvedami duomenys, sistema pagal šį parametrą gauna operacijos valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="8a249-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="8a249-134">Italijoje ši funkcija taikoma tik modulyje Mokėtinos sumos.</span><span class="sxs-lookup"><span data-stu-id="8a249-134">For Italy, this functionality is only applicable in the Accounts payable module.</span></span> <span data-ttu-id="8a249-135">Mokėtinų sumų parametruose vartotojas gali pasirinkti <strong>registravimo datą</strong> arba <strong>dokumento datą</strong> lauke <strong>Valiutos kurso data</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-135">In the Accounts payable parameters, a user can select <strong>Posting date</strong> or <strong>Document date</strong> in the <strong>Exchange rate date</strong> field.</span></span>   </blockquote>
<blockquote>[!NOTE]<br><span data-ttu-id="8a249-136">Kai lauką <strong>Valiutos kurso data</strong> nustatote kaip <strong>Dokumento data (tik ES prekybai)</strong>, sistema naudoja PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="8a249-136">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="8a249-137">PVM grupės skirtuke <strong>Bendra</strong> yra parametras <strong>ES prekyba</strong>. Jei PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Taip</strong> ir jei ši PVM grupė nurodyta dokumento antraštėje, sistema valiutos kursą gauna pagal dokumento datą.</span><span class="sxs-lookup"><span data-stu-id="8a249-137">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="8a249-138">Jei šios PVM grupės parinktis <strong>ES prekyba</strong> nustatyta kaip <strong>Ne</strong>, sistema valiutos kursą gauna pagal dokumento registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="8a249-138">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="8a249-139">Prekybos datų, PVM registro datų ir dokumentų bei PVM datų valdymas</span><span class="sxs-lookup"><span data-stu-id="8a249-139">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="8a249-140">Lenkija, Vengrija, Čekija</span><span class="sxs-lookup"><span data-stu-id="8a249-140">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="8a249-141">Pardavimo datą ir dokumento gavimo datą būtina nurodyti teikiant PVM ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="8a249-141">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-142">Pardavimo data – tai operacijos įvykdymo data modulyje Gautinos sumos.</span><span class="sxs-lookup"><span data-stu-id="8a249-142">The sales date is the fulfillment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="8a249-143">Dokumento gavimo data – tai data, kuri parodo teisę reikalauti PVM atskaitymo modulyje Mokėtinos sumos.</span><span class="sxs-lookup"><span data-stu-id="8a249-143">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="8a249-144">Kiekviename gautame dokumente audito tikslais nurodyta data.</span><span class="sxs-lookup"><span data-stu-id="8a249-144">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="8a249-145">Į Vengrijos datų terminų funkcijas, Čekijos įvykdymo datų funkcijas ir Lenkijos PVM registravimo datų funkcijas įtrauktas mokesčių informacijos ataskaitų reikalavimas, paremtas data, kuri skiriasi nuo registravimo datos.</span><span class="sxs-lookup"><span data-stu-id="8a249-145">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="8a249-146">Laukas <strong>PVM registro data</strong> palaiko šį reikalavimą ir yra rodomas daugiau nei 20-yje puslapių.</span><span class="sxs-lookup"><span data-stu-id="8a249-146">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="8a249-147">Šie puslapiai – tai žurnalai, pardavimo užsakymai, pirkimo užsakymai, laisvos formos sąskaitos faktūros, tiekėjų sąskaitų faktūrų žurnalai ir projektų sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="8a249-147">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="8a249-148">Kai atnaujinate ar registruojate dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data įtraukiama į puslapius, pvz., klientų ir tiekėjų sąskaitų faktūrų žurnalų puslapius.</span><span class="sxs-lookup"><span data-stu-id="8a249-148">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="8a249-149">Konkrečiai Čekijoje, jei PVM registravimas atidedamas, registravimo metu laukas <strong>PVM registro data</strong> gali būti tuščias.</span><span class="sxs-lookup"><span data-stu-id="8a249-149">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="8a249-150">Kitu atveju laukas yra privalomas ir jį reikia užpildyti.</span><span class="sxs-lookup"><span data-stu-id="8a249-150">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="8a249-151">Datos tikrinimo parametrus galima nustatyti puslapyje <strong>PVM grupės</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-151">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-152">Parametrai <strong>PVM registro pildymo data</strong> ir <strong>Pardavimo datos pildymas</strong> naudojami kaip numatytasis atitinkamų datų pildymo būdas.</span><span class="sxs-lookup"><span data-stu-id="8a249-152">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="8a249-153">Taip pat galima naudoti rankinės įvesties ir kelis automatinės įvesties būdus.</span><span class="sxs-lookup"><span data-stu-id="8a249-153">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="8a249-154">Laukas <strong>Privaloma pardavimo data</strong> nurodo, ar, prieš registruojant pardavimo sąskaitą faktūrą, reikia įvesti pardavimo datą.</span><span class="sxs-lookup"><span data-stu-id="8a249-154">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="8a249-155">Puslapyje <strong>PVM registro operacijos</strong> galite užpildyti tuščius registruotų mokesčių operacijų PVM registro datų laukus.</span><span class="sxs-lookup"><span data-stu-id="8a249-155">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8a249-156">PVM registravimo datos, į kurias įtraukti atidėti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="8a249-156">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="8a249-157">Vengrija</span><span class="sxs-lookup"><span data-stu-id="8a249-157">Hungary</span></span></td>
<td>
<p><span data-ttu-id="8a249-158">Pagal Vengrijos mokesčių įstatymų reikalavimus sąskaitas faktūras reikia sukurti jų įvykdymo metu arba ne vėliau kaip per 15 dienų po įvykdymo.</span><span class="sxs-lookup"><span data-stu-id="8a249-158">Hungary tax regulations require that invoices be created at either the time of fulfillment or no later than 15 days after fulfillment.</span></span></p>
<p><span data-ttu-id="8a249-159">Įvykdymo data yra užsakytų paslaugų suteikimo data arba užsakytų prekių pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="8a249-159">The fulfillment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="8a249-160">Atnaujinant ar registruojant dokumentus, visi mokesčiai registruojami naudojant atitinkamą PVM registro datą, o data rodoma atitinkamuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="8a249-160">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="8a249-161">Be to, pagal reikalavimus, nuolat teikiant paslaugas, pvz., nuomos, konsultavimo ar šildymo, PVM turi atitikti tolesnius kriterijus.</span><span class="sxs-lookup"><span data-stu-id="8a249-161">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-162">PVM sąskaitos faktūros dieną turi būti registruojamas paskirtoje DK sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="8a249-162">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="8a249-163">PVM termino dieną turi būti perkeltas iš specialių sąskaitų į gautino arba mokėtino PVM sąskaitą ir jį reikia įtraukti į PVM ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="8a249-163">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="8a249-164">Kad galėtumėte įvykdyti šiuos reikalavimus, didžiosios knygos registravimus galite perkelti į atidėtų gaunamų mokesčių sąskaitą ir atidėtų išmokamų mokesčių sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="8a249-164">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="8a249-165">Tačiau pirmiausia turite įvykdyti tolesnes būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="8a249-165">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="8a249-166">Didžiosios knygos registravimo grupėse nustatyti atidėto mokėtino PVM ir atidėto gautino PVM DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="8a249-166">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="8a249-167">Įjungti prekių PVM grupių parametrą <strong>Atidėtas PVM</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-167">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="8a249-168">Privaloma PVM data</span><span class="sxs-lookup"><span data-stu-id="8a249-168">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="8a249-169">Lenkija</span><span class="sxs-lookup"><span data-stu-id="8a249-169">Poland</span></span></td>
<td>
<p><span data-ttu-id="8a249-170">Galite reikalauti, kad PVM registro data būtų įtraukta į pirkimo ir pardavimo operacijų įrašus.</span><span class="sxs-lookup"><span data-stu-id="8a249-170">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="8a249-171">Todėl PVM registro datą galima užfiksuoti prieš užregistruojant operaciją.</span><span class="sxs-lookup"><span data-stu-id="8a249-171">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="8a249-172">Naudojant šią funkciją galima išvengti situacijos, kai laikotarpio pabaigoje reikia tvarkyti kelias operacijas.</span><span class="sxs-lookup"><span data-stu-id="8a249-172">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="8a249-173">Lauką <strong>PVM registro data</strong> galite padaryti privalomą registruojant klientų ar tiekėjų operacijas.</span><span class="sxs-lookup"><span data-stu-id="8a249-173">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="8a249-174">Norėdami šį lauką padaryti privalomą, įjunkite susijusios kliento ar tiekėjo sąskaitos parinktį <strong>Būtina nurodyti PVM datą</strong>.</span><span class="sxs-lookup"><span data-stu-id="8a249-174">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>
