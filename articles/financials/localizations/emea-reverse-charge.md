---
title: "Atvirkštinio mokesčio PVM"
description: "Šioje temoje paaiškinama, kaip nustatyti atvirkštinio mokesčio pridėtinės vertės mokestį (PVM) Europos šalyse ir Saudo Arabijoje."
author: epodkolz
manager: AnnBe
ms.date: 04/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 64518e72dd66961108ff905981cd0405355ed130
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="reverse-charge-vat"></a><span data-ttu-id="2a5e1-103">Atvirkštinio mokesčio PVM</span><span class="sxs-lookup"><span data-stu-id="2a5e1-103">Reverse charge VAT</span></span>


[!INCLUDE [banner](../includes/banner.md)]


<span data-ttu-id="2a5e1-104">Šioje temoje aprašomas bendrasis atvirkštinio apmokestinimo pridėtinės vertės mokesčiu (PVM) nustatymo metodas Saudo Arabijoje ir Europos šalyse.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia and European countries.</span></span>

<span data-ttu-id="2a5e1-105">Atvirkštinis apmokestinimas yra mokesčio schema, kuri atsakomybę už apskaitą ir PVM ataskaitas perkelia nuo pardavėjo prekių ir (arba) paslaugų pirkėjui.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="2a5e1-106">Todėl savo PVM išraše prekių ir (arba) paslaugų gavėjai praneša ir mokėtiną PVM (atlikdami pardavėjo vaidmenį), ir gautiną PVM (atlikdami pirkėjo vaidmenį).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="2a5e1-107">Kai kuriose šalyse ar regionuose atvirkštinio apmokestinimo schema taikoma tik tam tikroms prekėms ir (arba) paslaugoms ir yra papildomų sąlygų arba pardavimo sumų ribinių verčių.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="2a5e1-108">Kitose šalyse ar regionuose PVM mokėjimo atsakomybė priklauso nuo tiekėjo ir pirkėjo būsenos.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="2a5e1-109">Jei pirkėjas turi sumokėti PVM, tai turi būti aiškiai pažymėta tiekėjo išduotoje SF.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="2a5e1-110">Pvz., SF turi būti žodžiai „atvirkštinis mokestis“ ir turi būti nurodyta, kurios pareigos apmokestinamos pagal atvirkštinio mokesčio schemą.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="2a5e1-111">Norėdami taikyti atvirkštinį mokestį, turite atlikti toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="2a5e1-112">Nustatyti PVM kodus</span><span class="sxs-lookup"><span data-stu-id="2a5e1-112">Set up sales tax codes</span></span>
<span data-ttu-id="2a5e1-113">Pardavimo ir pirkimo operacijoms rekomenduojame naudoti atskirus PVM kodus.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="2a5e1-114"><strong>Pardavimo PVM kodas</strong></span><span class="sxs-lookup"><span data-stu-id="2a5e1-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="2a5e1-115">Sukurkite atvirkštinio mokesčio pardavimo operacijų PVM kodą (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM kodai</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="2a5e1-116"><strong>Pirkimo PVM kodas</strong></span><span class="sxs-lookup"><span data-stu-id="2a5e1-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="2a5e1-117">Sukurkite teigiamus ir neigiamus pirkimo atvirkštinio mokesčio PVM kodus (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM kodai</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="2a5e1-118">Sukurkite teigiamos reikšmės PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="2a5e1-119">Sukurkite neigiamos reikšmės PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="2a5e1-120">Nustatykite funkcijos <strong>Leisti neigiamą PVM procentą</strong> parinktį <strong>Taip</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="2a5e1-121">Turite priskirti neigiamą PVM kodą prekės PVM grupei, o po to tą PVM grupę priskirti prekėms, kurios yra atvirkštinio PVM subjektas.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="2a5e1-122">Daugiau informacijos ieškokite kitame skyriuje &quot;PVM grupių ir prekių PVM grupių nustatymas&quot;.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="2a5e1-123">Nustatyti PVM grupes ir prekių PVM grupes</span><span class="sxs-lookup"><span data-stu-id="2a5e1-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="2a5e1-124">Pardavimo ir pirkimo operacijoms rekomenduojame naudoti atskiras PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="2a5e1-125"><strong>Pardavimo PVM grupės</strong></span><span class="sxs-lookup"><span data-stu-id="2a5e1-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="2a5e1-126">Sukurkite atvirkštinio mokesčio pardavimo operacijų PVM grupę (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM grupės</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="2a5e1-127">Šios grupės skirtuke <strong>Sąranka</strong> įtraukite atvirkštinio mokesčio PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="2a5e1-128">Pažymėkite PVM kodo žymės langelius <strong>Neapmokestinama</strong> ir <strong>Atvirkštinis mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a5e1-129"><strong>Pirkimo PVM grupės</strong></span><span class="sxs-lookup"><span data-stu-id="2a5e1-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="2a5e1-130">Sukurkite atvirkštinio mokesčio pirkimo operacijų PVM grupę (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM grupės</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="2a5e1-131">Skirtuke <strong>Sąranka</strong> į šią grupę įtraukite ir teigiamus, ir neigiamus PVM kodus.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="2a5e1-132">Pažymėkite neigiamos reikšmės PVM kodo žymės langelį <strong>Atvirkštinis mokestis</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2a5e1-133"><strong>Prekės PVM grupės</strong></span><span class="sxs-lookup"><span data-stu-id="2a5e1-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="2a5e1-134">Sukurkite arba atnaujinkite prekės PVM grupę, kuriai priskirtas neigiamos reikšmės PVM kodas (<strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>Prekės PVM grupės</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a5e1-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="2a5e1-135">Numatytąją prekės PVM grupę turite priskirti tiems produktams ir kategorijoms, kurioms taikomas atvirkštinis mokestis.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="2a5e1-136">Atvirkštinio apmokestinimo grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="2a5e1-136">Set up reverse charge groups</span></span>
<span data-ttu-id="2a5e1-137">Puslapyje **Atvirkštinio apmokestinimo prekių grupės** (**Mokestis** &gt; **Sąranka** &gt; **PVM** &gt; **Atvirkštinio apmokestinimo prekių grupės**) galite nurodyti produktų, paslaugų arba atskirų prekių, paslaugų, kurioms gali būti taikomas atvirkštinis apmokestinimas, grupes.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="2a5e1-138">Nurodykite kiekvienos atvirkštinio apmokestinimo prekių grupės prekių, prekių grupių bei pardavimų ir (arba) pirkimų kategorijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="2a5e1-139">Atvirkštinio apmokestinimo taisyklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="2a5e1-139">Set up reverse charge rules</span></span>
<span data-ttu-id="2a5e1-140">Puslapyje **Atvirkštinio apmokestinimo taisyklės** (**Mokestis** &gt; **Sąranka** &gt; **PVM** &gt; **Atvirkštinio apmokestinimo taisyklės**) galite nustatyti pirkimo ir pardavimo tikslais naudojamas tinkamumo taisykles.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="2a5e1-141">Galite sukonfigūruoti atvirkštinio mokesčio taikymo taisyklių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="2a5e1-142">Nustatykite šiuos kiekvienos taisyklės laukus:</span><span class="sxs-lookup"><span data-stu-id="2a5e1-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="2a5e1-143">**Dokumento tipas** – pasirinkite **Pirkimo užsakymas**, **Tiekėjo SF žurnalas**, **Pardavimo užsakymas**, **Laisvos formos SF**, **Kliento SF žurnalas** ir (arba) **Tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="2a5e1-144">**Partnerio šalies / regiono tipas** – pasirinkite **Vietinis**, **ES** arba **Užsienio**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="2a5e1-145">Arba, jeigu taisyklė gali būti taikoma visiems prekybos partneriams, nepriklausomai nuo jų šalies ar regiono adreso, pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="2a5e1-146">**Vietinis pristatymo adresas** – pažymėkite šį žymės langelį, jei norite taikyti taisyklę visoms į tą pačią šalį ar regioną pristatomoms prekėms.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="2a5e1-147">Pasirinkus dokumentų tipus **Tiekėjo SF žurnalas** ir **Kliento SF žurnalas** šio žymės langelio pažymėti negalima.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="2a5e1-148">**Atvirkštinio apmokestinimo prekių grupė** – pasirinkite grupę, kuriai gali būti taikoma taisyklė.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="2a5e1-149">**Ribinės vertės suma** – SF atvirkštinio apmokestinimo schema taikoma tik tada, jei prekių ir (arba) paslaugų, kurios įtrauktos į atvirkštinio apmokestinimo prekių grupę vertė viršija limitą, kurį nurodote čia.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="2a5e1-150">Laukus **Galioja nuo** ir **Galiojimo data** taip pat galite naudoti norėdami nurodyti laikotarpį, kada galioja taisyklė.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="2a5e1-151">Be to, galite nurodyti, ar, jei bus patenkinta tos dokumento eilutės sąlyga, bus rodomas pranešimas ir ar bus atnaujinta dokumento eilutėje nurodyta numatytoji atvirkštinio apmokestinimo PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="2a5e1-152">Galimos toliau nurodytos pasirinktys:</span><span class="sxs-lookup"><span data-stu-id="2a5e1-152">The following options are available:</span></span>

- <span data-ttu-id="2a5e1-153">**Nė vienas iš atvejų** – dokumento eilutė neatnaujinama.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="2a5e1-154">**Raginti** – rodomas pranešimas, raginantis patvirtinti, kad galima taikyti atvirkštinio apmokestinimo mokestį.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="2a5e1-155">**Nustatyti** – dokumento eilutė atnaujinama be papildomų pranešimų.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="2a5e1-156">Numatytųjų parametrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2a5e1-156">Set up default parameters</span></span>
<span data-ttu-id="2a5e1-157">Norėdami įgalinti atvirkštinio mokesčio PVM funkciją, puslapio **DK parametrai** skirtuke **Atvirkštinis apmokestinimas** nustatykite funkcijos **Įgalinti atvirkštinį apmokestinimą** parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="2a5e1-158">Laukuose **Pirkimo užsakymų PVM grupė** ir **Pardavimo užsakymų PVM grupė** pasirinkite numatytąsias PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="2a5e1-159">Kai patenkinama atvirkštinio mokesčio taikymo sąlyga, pardavimo arba pirkimo užsakymo eilutės atnaujinamos nurodant šias PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="2a5e1-160">Pardavimo SF atvirkštinis apmokestinimas</span><span class="sxs-lookup"><span data-stu-id="2a5e1-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="2a5e1-161">Pagal atvirkštinio apmokestinimo schemą atliekamiems pardavimamas pardavėjas PVM mokesčio netaiko.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="2a5e1-162">Tačiau SF nurodomos abi prekės, kurioms taikytinas atvirkštinio apmokestinimo PVM, bei bendra atvirkštinio PVM suma.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="2a5e1-163">Užregistravus atvirkštinio apmokestinimo pardavimo SF, PVM operacijos pažymimos mokesčių nuoroda **Mokėtinas PVM** bei nulinio PVM mokesčio nuoroda ir pažymimas žymės langelis **Atvirkštinis apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="2a5e1-164">Pirkimo SF atvirkštinis apmokestinimas</span><span class="sxs-lookup"><span data-stu-id="2a5e1-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="2a5e1-165">Kai pirkimai atliekami pagal atvirkštinio apmokestinimo schemą, atvirkštinio apmokestinimo SF gavęs pirkėjas PVM apskaitos tikslais yra ir pirkėjas, ir pardavėjas.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="2a5e1-166">Užregistravus atvirkštinio apmokestinimo pirkimo SF sukuriamos dvi PVM operacijos.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="2a5e1-167">Viena operacija pažymėta mokesčių nuoroda **Gautinas PVM**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="2a5e1-168">Kita operacija pažymėta mokesčių nuoroda **Mokėtinas PVM** ir pažymėtas žymės langelis **Atvirkštinis apmokestinimas**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="2a5e1-169">Toliau pateiktoje ekrano kopijoje vienos operacijos kryptis yra **Gautinas PVM**, o kitos – **mokėtinas PVM**.</span><span class="sxs-lookup"><span data-stu-id="2a5e1-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![Užregistruotas PVM](media/apac-sau-posted-sales-tax.png)

