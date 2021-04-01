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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5d17f2ec594901404fcd251e463f293258af051c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237160"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Kainų, nuolaidų, sutarčių ir grąžinimų trikčių diagnostika

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti dirbant su kainomis, nuolaidomis, sutartimis ir grąžinimais.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Negaliu susieti pirkimo sutarties su pirkimo užsakymo eilute po to, kai sukuriamas pirkimo užsakymas.

Pirkimo sutartis turi būti siejama su pirkimo užsakymo eilute, kai pirkimo užsakymas yra kuriamas. Kitu atveju pirkimo užsakymo eilutės negali būti susietos su pirkimo sutarties eilutėmis.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Kokia patikra paleidžia pranešimą „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu”?

Kai pakeičiate siuntimo datą, galite gauti pranešimą, kuriame teigiama: „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu.” Šis pranešimas gaunamas, nes pasikeitus siuntimo datai, gali būti suaktyvinta skirtinga prekybos arba pardavimo sutartis ir tai sukelti kainos keitimą. Siuntimo datos pakeitimas taip pat gali paveikti sandėlio grafikus ir kitą susijusią informaciją.

Pranešimas paleidžiamas, kai pasikeičia bet kuri iš datų arba kai kurie kiti parametrai. Pranešimo paskirtis yra įsitikinti, kad žinote apie kainos pakeitimus, kurie gali kilti dėl šių pasikeitimų.

Pranešimas yra prekybos sutarties vertinimo (TAE) raginimas. Norėdami gauti išsamų aprašą, žr. [Prekybos sutarties vertinimo strategijos](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Pirkimo užsakymo kvite nenurodyti visi mokesčiai.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Puslapio **Įsigijimo ir šaltinio pasirinkimo parametrai** skirtuke **Pristatymas** įsitikinkite, kad parinktis **Generuoti mokesčius produkto gavimo kvite** nustatyta kaip *Taip*.
1. Sukurkite pirkimo užsakymą, apimantį mokesčius.
1. Patvirtinkite pirkimo užsakymą.
1. Gaukite pirkimo užsakymą.
1. Peržiūrėkite bendrąją kvito sumą ir palyginkite ją su numatoma bendrąja suma.
1. Atkreipkite dėmesį, kad ne visi mokesčiai yra įtraukti į pirkimo užsakymo kvitą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Paaiškinimas priklauso nuo to, kaip buvo nustatytos papildomos išlaidos. Norėdami gauti daugiau informacijos apie tai, kaip nustatyti papildomas išlaidas, atitinkančias jūsų poreikius, žr. šiuos internetinio dienoraščio pranešimus: [Užregistruokite papildomas išlaidas produkto gavimo kvito metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Prekybos sutarčių kainos ir nuolaidos netaikomos pardavimo arba pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų valdymą.

### <a name="issue-description"></a>Problemos aprašas

Prekybos sutartys, taikytinos pardavimo arba pirkimo užsakymo eilutėse nėra taikomos eilutėse, kurios importuojamos naudojant duomenų valdymą. Tačiau tos pačios prekybos sutartys yra taikomos pardavimo arba pirkimo užsakymo eilutėms, sukurtoms rankiniu būdu.

### <a name="reason-for-the-issue"></a>Problemos priežastis

Jei pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų tvarkymą, jau yra informacija apie kainą, prekybos sutartis nebus iš naujo įvertinta tose eilutėse. Pavyzdžiui, jei **Eilutės nuolaidos procentas** arba bet kuri iš kainų ir nuolaidų verčių nustatoma eilutei, tada prekybos sutarčių nebus ieškoma toje eilutėje.

### <a name="issue-workaround"></a>Problemos sprendimas

Tikimasi tokio elgesio ir jis yra panašus tiek pardavimo, tiek pirkimo užsakymuose.

Kaip sprendimą, importuokite pirkimo užsakymo eilutes nenurodydami jokios kainos informacijos. Tada bus taikomos prekybos sutartys, o pirkimo užsakymo eilutės bus atnaujintos remiantis apibrėžtomis prekybos sutartimis.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Tiekėjo grąžinimas nėra kaupiamas pagal sąskaitas faktūras.

### <a name="issue-description"></a>Problemos aprašas

Jeigu užregistruotos sąskaitos faktūros turi skirtingus terminus, šios sąskaitos faktūros neatsispindi tiekėjo grąžinimuose, kurie yra sugeneruoti iš jų.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Kaip numatyta, į terminą nėra atsižvelgiama, kai tiekėjo grąžinimas yra skaičiuojamas. Apsvarstykite tinkinti sistemą taip, kad terminas ir ryšys su sąskaita faktūra būtų akivaizdesni faktinio tiekėjo grąžinimo atžvilgiu.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Vienetų kainos pirkimo užsakymuose neskaičiuojamos pagal vienetų konvertavimą.

### <a name="issue-description"></a>Problemos aprašas

Kai pirkimo užsakymo vienetas yra pakeičiamas, prekybos sutarčių kainos nėra perskaičiuojamos pagal vienetų konvertavimo apibrėžimus.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Kainos visada gaunamos iš prekybos sutarčių (arba kitų sistemos kainos parametrų, tokių kaip pardavimo sutartys arba prekių kainos) ir yra nustatomos vienetui.

Jei vienetas pakeičiamas užsakymo eilutėje, sistema ieško naujo vieneto kainos ir pritaiko tą kainą. Jei nerandama vieneto kaina, sistema nepritaiko kainos. Vieneto konvertavimo negalima naudoti kainos perskaičiavimui į kitą vienetą. Teoriškai, vieno langelio dešimties vienetų kaina gali būti ne tokia pat kaip dešimt kartų didesnė kaina už vieno langelio kainą.

### <a name="issue-workaround"></a>Problemos sprendimas

Vienas iš būdų, kaip išspręsti šią problemą, yra įsitikinti, kad yra prekybos sutarčių tiems vienetams, kuriuos tikitės panaudoti prekės užsakymo eilutėse.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Su prekybos sutartimis iškyla valiutos konvertavimo problemos.

Prekybos sutarčių kainos nėra perskaičiuojamos pagal valiutą, kai ji skiriasi nuo pirkimo užsakyme nurodytos valiutos.

Funkcija *Bendroji valiuta* jums leidžia apibrėžti kainas ir nuolaidas tik viena valiuta. Tada galite konvertuoti į kitas valiutas pagal jūsų pareikalavimą. Be to, atlikus konvertavimą, funkcija gali automatiškai taikyti intelektualųjį apvalinimą.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Atidaręs pirkimo sutarties puslapį eilutės rodinio režimu, negaliu individualizuoti puslapio pridedant kainos vieneto lauką eilutės peržiūroje.

Kai kurie bendri sutarčių sistemos laukai negali būti įtraukti į asmeninius nustatymus. Šis apribojimas atsiranda dėl įdiegto duomenų modelio. Todėl negalite suasmeninti **Kainos vieneto** lauko.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>Aukščiausia pirkimo sutarties riba nėra veiksminga pirkimo paraiškoje.

### <a name="issue-description"></a>Problemos aprašas

Kai pirkimo paraiška yra susiejama su pirkimo sutartimi, pirkimo sutarties aukščiausios riba negalioja pirkimo paraiškoje. Numatytoji kainos informacija yra tinkamai įvesta, bet pirkimo paraiškoje galima užsakyti ne tik pirkimo sutarties aukščiausią ribą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Tikimasi tokio elgesio. Kadangi paraiškos ne visada patvirtinamos, kiekis arba suma neturėtų būti rezervuojami pirkimo sutartyje. Todėl neatitinkate pirkimo sutarties aukščiausios ribos.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Prekybos sutartys gali būti kuriamos iš atmestų RFQs. Todėl sistema netrukdo sukurti prekybos sutarčių žurnalų, jei RFQ eilutė nebuvo priimta.

Galite sukurti prekybos sutartis dėl bet kurių atsakymų pasiūlymo patvirtinimui (RFQ), neatsižvelgiant į tai, ar jie buvo priimti ar atmesti. Norėdami gauti daugiau informacijos, žr. [Pasiūlymų patvirtinimų (RFQs) apžvalga](request-quotations.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]