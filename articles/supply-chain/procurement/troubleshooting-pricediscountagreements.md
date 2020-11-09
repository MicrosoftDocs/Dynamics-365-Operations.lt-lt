---
title: Kainų, nuolaidų, sutarčių ir grąžinimų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su kainomis, nuolaidomis, sutartimis ir grąžinimais.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018218"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="b9275-103">Kainų, nuolaidų, sutarčių ir grąžinimų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="b9275-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="b9275-104">Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su kainomis, nuolaidomis, sutartimis ir grąžinimais.</span><span class="sxs-lookup"><span data-stu-id="b9275-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="b9275-105">Negaliu susieti pirkimo sutarties su pirkimo užsakymo eilute po to, kai sukuriamas pirkimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="b9275-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="b9275-106">Pirkimo sutartis turi būti siejama su pirkimo užsakymo eilute, kai pirkimo užsakymas yra kuriamas.</span><span class="sxs-lookup"><span data-stu-id="b9275-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="b9275-107">Kitu atveju pirkimo užsakymo eilutės negali būti susietos su pirkimo sutarties eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="b9275-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="b9275-108">Kokia patikra paleidžia pranešimą „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu”?</span><span class="sxs-lookup"><span data-stu-id="b9275-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="b9275-109">Kai pakeičiate siuntimo datą, galite gauti pranešimą, kuriame teigiama: „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu.”</span><span class="sxs-lookup"><span data-stu-id="b9275-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="b9275-110">Šis pranešimas gaunamas, nes pasikeitus siuntimo datai, gali būti suaktyvinta skirtinga prekybos arba pardavimo sutartis ir tai sukelti kainos keitimą.</span><span class="sxs-lookup"><span data-stu-id="b9275-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="b9275-111">Siuntimo datos pakeitimas taip pat gali paveikti sandėlio grafikus ir kitą susijusią informaciją.</span><span class="sxs-lookup"><span data-stu-id="b9275-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="b9275-112">Pranešimas paleidžiamas, kai pasikeičia bet kuri iš datų arba kai kurie kiti parametrai.</span><span class="sxs-lookup"><span data-stu-id="b9275-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="b9275-113">Pranešimo paskirtis yra įsitikinti, kad žinote apie kainos pakeitimus, kurie gali kilti dėl šių pasikeitimų.</span><span class="sxs-lookup"><span data-stu-id="b9275-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="b9275-114">Pranešimas yra prekybos sutarties vertinimo (TAE) raginimas.</span><span class="sxs-lookup"><span data-stu-id="b9275-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="b9275-115">Norėdami gauti išsamų aprašą, žr. [Prekybos sutarties vertinimo strategijos](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="b9275-115">For a full description, see [Trade agreement evaluation policies](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="b9275-116">Pirkimo užsakymo kvite nenurodyti visi mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="b9275-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="b9275-117">Problemos atkūrimas</span><span class="sxs-lookup"><span data-stu-id="b9275-117">Reproduce the issue</span></span>

<span data-ttu-id="b9275-118">Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.</span><span class="sxs-lookup"><span data-stu-id="b9275-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="b9275-119">Puslapio **Įsigijimo ir šaltinio pasirinkimo parametrai** skirtuke **Pristatymas** įsitikinkite, kad parinktis **Generuoti mokesčius produkto gavimo kvite** nustatyta kaip *Taip*.</span><span class="sxs-lookup"><span data-stu-id="b9275-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="b9275-120">Sukurkite pirkimo užsakymą, apimantį mokesčius.</span><span class="sxs-lookup"><span data-stu-id="b9275-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="b9275-121">Patvirtinkite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b9275-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="b9275-122">Gaukite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b9275-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="b9275-123">Peržiūrėkite bendrąją kvito sumą ir palyginkite ją su numatoma bendrąja suma.</span><span class="sxs-lookup"><span data-stu-id="b9275-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="b9275-124">Atkreipkite dėmesį, kad ne visi mokesčiai yra įtraukti į pirkimo užsakymo kvitą.</span><span class="sxs-lookup"><span data-stu-id="b9275-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b9275-125">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="b9275-125">Issue resolution</span></span>

<span data-ttu-id="b9275-126">Paaiškinimas priklauso nuo to, kaip buvo nustatytos papildomos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="b9275-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="b9275-127">Norėdami gauti daugiau informacijos apie tai, kaip nustatyti papildomas išlaidas, atitinkančias jūsų poreikius, žr. šiuos internetinio dienoraščio pranešimus: [Užregistruokite papildomas išlaidas produkto gavimo kvito metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="b9275-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="b9275-128">Prekybos sutarčių kainos ir nuolaidos netaikomos pardavimo arba pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="b9275-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b9275-129">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="b9275-129">Issue description</span></span>

<span data-ttu-id="b9275-130">Prekybos sutartys, taikytinos pardavimo arba pirkimo užsakymo eilutėse nėra taikomos eilutėse, kurios importuojamos naudojant duomenų valdymą.</span><span class="sxs-lookup"><span data-stu-id="b9275-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="b9275-131">Tačiau tos pačios prekybos sutartys yra taikomos pardavimo arba pirkimo užsakymo eilutėms, sukurtoms rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="b9275-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="b9275-132">Problemos priežastis</span><span class="sxs-lookup"><span data-stu-id="b9275-132">Reason for the issue</span></span>

<span data-ttu-id="b9275-133">Jei pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų tvarkymą, jau yra informacija apie kainą, prekybos sutartis nebus iš naujo įvertinta tose eilutėse.</span><span class="sxs-lookup"><span data-stu-id="b9275-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="b9275-134">Pavyzdžiui, jei **Eilutės nuolaidos procentas** arba bet kuri iš kainų ir nuolaidų verčių nustatoma eilutei, tada prekybos sutarčių nebus ieškoma toje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b9275-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="b9275-135">Problemos sprendimas</span><span class="sxs-lookup"><span data-stu-id="b9275-135">Issue workaround</span></span>

<span data-ttu-id="b9275-136">Tikimasi tokio elgesio ir jis yra panašus tiek pardavimo, tiek pirkimo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="b9275-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="b9275-137">Kaip sprendimą, importuokite pirkimo užsakymo eilutes nenurodydami jokios kainos informacijos.</span><span class="sxs-lookup"><span data-stu-id="b9275-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="b9275-138">Tada bus taikomos prekybos sutartys, o pirkimo užsakymo eilutės bus atnaujintos remiantis apibrėžtomis prekybos sutartimis.</span><span class="sxs-lookup"><span data-stu-id="b9275-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="b9275-139">Tiekėjo grąžinimas nėra kaupiamas pagal sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="b9275-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b9275-140">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="b9275-140">Issue description</span></span>

<span data-ttu-id="b9275-141">Jeigu užregistruotos sąskaitos faktūros turi skirtingus terminus, šios sąskaitos faktūros neatsispindi tiekėjo grąžinimuose, kurie yra sugeneruoti iš jų.</span><span class="sxs-lookup"><span data-stu-id="b9275-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b9275-142">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="b9275-142">Issue resolution</span></span>

<span data-ttu-id="b9275-143">Kaip numatyta, į terminą nėra atsižvelgiama, kai tiekėjo grąžinimas yra skaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="b9275-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="b9275-144">Apsvarstykite tinkinti sistemą taip, kad terminas ir ryšys su sąskaita faktūra būtų akivaizdesni faktinio tiekėjo grąžinimo atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="b9275-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="b9275-145">Vienetų kainos pirkimo užsakymuose neskaičiuojamos pagal vienetų konvertavimą.</span><span class="sxs-lookup"><span data-stu-id="b9275-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b9275-146">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="b9275-146">Issue description</span></span>

<span data-ttu-id="b9275-147">Kai pirkimo užsakymo vienetas yra pakeičiamas, prekybos sutarčių kainos nėra perskaičiuojamos pagal vienetų konvertavimo apibrėžimus.</span><span class="sxs-lookup"><span data-stu-id="b9275-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b9275-148">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="b9275-148">Issue resolution</span></span>

<span data-ttu-id="b9275-149">Kainos visada gaunamos iš prekybos sutarčių (arba kitų sistemos kainos parametrų, tokių kaip pardavimo sutartys arba prekių kainos) ir yra nustatomos vienetui.</span><span class="sxs-lookup"><span data-stu-id="b9275-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="b9275-150">Jei vienetas pakeičiamas užsakymo eilutėje, sistema ieško naujo vieneto kainos ir pritaiko tą kainą.</span><span class="sxs-lookup"><span data-stu-id="b9275-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="b9275-151">Jei nerandama vieneto kaina, sistema nepritaiko kainos.</span><span class="sxs-lookup"><span data-stu-id="b9275-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="b9275-152">Vieneto konvertavimo negalima naudoti kainos perskaičiavimui į kitą vienetą.</span><span class="sxs-lookup"><span data-stu-id="b9275-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="b9275-153">Teoriškai, vieno langelio dešimties vienetų kaina gali būti ne tokia pat kaip dešimt kartų didesnė kaina už vieno langelio kainą.</span><span class="sxs-lookup"><span data-stu-id="b9275-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="b9275-154">Problemos sprendimas</span><span class="sxs-lookup"><span data-stu-id="b9275-154">Issue workaround</span></span>

<span data-ttu-id="b9275-155">Vienas iš būdų, kaip išspręsti šią problemą, yra įsitikinti, kad yra prekybos sutarčių tiems vienetams, kuriuos tikitės panaudoti prekės užsakymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="b9275-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="b9275-156">Su prekybos sutartimis iškyla valiutos konvertavimo problemos.</span><span class="sxs-lookup"><span data-stu-id="b9275-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="b9275-157">Prekybos sutarčių kainos nėra perskaičiuojamos pagal valiutą, kai ji skiriasi nuo pirkimo užsakyme nurodytos valiutos.</span><span class="sxs-lookup"><span data-stu-id="b9275-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="b9275-158">Funkcija *Bendroji valiuta* jums leidžia apibrėžti kainas ir nuolaidas tik viena valiuta.</span><span class="sxs-lookup"><span data-stu-id="b9275-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="b9275-159">Tada galite konvertuoti į kitas valiutas pagal jūsų pareikalavimą.</span><span class="sxs-lookup"><span data-stu-id="b9275-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="b9275-160">Be to, atlikus konvertavimą, funkcija gali automatiškai taikyti intelektualųjį apvalinimą.</span><span class="sxs-lookup"><span data-stu-id="b9275-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="b9275-161">Atidaręs pirkimo sutarties puslapį eilutės rodinio režimu, negaliu individualizuoti puslapio pridedant kainos vieneto lauką eilutės peržiūroje.</span><span class="sxs-lookup"><span data-stu-id="b9275-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="b9275-162">Kai kurie bendri sutarčių sistemos laukai negali būti įtraukti į asmeninius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b9275-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="b9275-163">Šis apribojimas atsiranda dėl įdiegto duomenų modelio.</span><span class="sxs-lookup"><span data-stu-id="b9275-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="b9275-164">Todėl negalite suasmeninti **Kainos vieneto** lauko.</span><span class="sxs-lookup"><span data-stu-id="b9275-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="b9275-165">Aukščiausia pirkimo sutarties riba nėra veiksminga pirkimo paraiškoje.</span><span class="sxs-lookup"><span data-stu-id="b9275-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b9275-166">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="b9275-166">Issue description</span></span>

<span data-ttu-id="b9275-167">Kai pirkimo paraiška yra susiejama su pirkimo sutartimi, pirkimo sutarties aukščiausios riba negalioja pirkimo paraiškoje.</span><span class="sxs-lookup"><span data-stu-id="b9275-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="b9275-168">Numatytoji kainos informacija yra tinkamai įvesta, bet pirkimo paraiškoje galima užsakyti ne tik pirkimo sutarties aukščiausią ribą.</span><span class="sxs-lookup"><span data-stu-id="b9275-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b9275-169">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="b9275-169">Issue resolution</span></span>

<span data-ttu-id="b9275-170">Tikimasi tokio elgesio.</span><span class="sxs-lookup"><span data-stu-id="b9275-170">This behavior is expected.</span></span> <span data-ttu-id="b9275-171">Kadangi paraiškos ne visada patvirtinamos, kiekis arba suma neturėtų būti rezervuojami pirkimo sutartyje.</span><span class="sxs-lookup"><span data-stu-id="b9275-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="b9275-172">Todėl neatitinkate pirkimo sutarties aukščiausios ribos.</span><span class="sxs-lookup"><span data-stu-id="b9275-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="b9275-173">Prekybos sutartys gali būti kuriamos iš atmestų RFQs.</span><span class="sxs-lookup"><span data-stu-id="b9275-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="b9275-174">Todėl sistema netrukdo sukurti prekybos sutarčių žurnalų, jei RFQ eilutė nebuvo priimta.</span><span class="sxs-lookup"><span data-stu-id="b9275-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="b9275-175">Galite sukurti prekybos sutartis dėl bet kurių atsakymų pasiūlymo patvirtinimui (RFQ), neatsižvelgiant į tai, ar jie buvo priimti ar atmesti.</span><span class="sxs-lookup"><span data-stu-id="b9275-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="b9275-176">Norėdami gauti daugiau informacijos, žr. [Pasiūlymų patvirtinimų (RFQs) apžvalga](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="b9275-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>

