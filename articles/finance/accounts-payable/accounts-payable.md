---
title: Mokėtinų sumų pagrindinis puslapis
description: Šioje temoje apžvelgiamas modulis Mokėtinos sumos.
author: sunfzam
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "21901"
- intro-internal
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ce768ecaa668f2c69d6753401eaa145b6fddc5ec
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595292"
---
# <a name="accounts-payable-home-page"></a>Mokėtinų sumų pagrindinis puslapis

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas modulis Mokėtinos sumos. 

Tiekėjų sąskaitas faktūras galite įvesti rankiniu būdu arba jas gauti elektroniniu būdu, naudodami duomenų objektą. Kai sąskaitos faktūros įvestos arba gautos, jas peržiūrėti ir patvirtinti galite naudodami sąskaitų faktūrų patvirtinimo žurnalą arba puslapyje **Tiekėjo sąskaita faktūra**. Naudodami SF gretinimo funkciją, tiekėjo SF strategijas ir darbo eigą, galite automatizuoti peržiūros procesą, kad tam tikrus kriterijus atitinkančios SF būtų automatiškai patvirtintos, o likusios SF būtų pažymimos, kad jas peržiūrėtų įgaliotas vartotojas.

**Verslo procesai**

[![Verslo procesų diagrama.](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Mokėtinų sumų nustatymas

Nustatykite tiekėjų grupes, tiekėjus, registravimo šablonus, įvairias mokėjimo parinktis ir su tiekėjais, mokesčiais, pristatymais bei paskirties vietomis susijusius parametrus, paprastuosius vekselius ir kito tipo mokėtinų sumų informaciją. 

[Mokėtinų sumų konfigūravimo apžvalga](accounts-payable-overview.md)

[Apskaitos paskirstymai ir papildomos knygos žurnalo įrašai, skirti tiekėjo SF](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Mokėtinų sumų ir gautinų sumų užsienio valiutos kurso pasikeitimas](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Tiekėjo sąskaitų faktūrų konfigūravimas

Naudokite modulį Mokėtinos sumos, norėdami sekti sąskaitas faktūras ir siunčiamas išlaidas tiekėjui.

[Mokėtinų sumų SF gretinimo apžvalga](accounts-payable-invoice-matching.md)

[Tiekėjų registravimo šablonai](vendor-posting-profiles.md)

[Mokėtinų sumų SF gretinimo patvirtinimo nustatymas](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Trišalės atitikimo strategijos](three-way-matching-policies.md)

[SF gretinimas ir vidinės įmonės pirkimo užsakymai](invoice-matching-intercompany-purchase-orders.md)

[Nesutapimų šalinimo gretinant SF bendrąsias sumas apžvalga](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Numatytosios korespondentinės sąskaitos tiekėjo sąskaitų faktūrų žurnalams ir sąskaitų faktūrų patvirtinimo žurnalams](default-offset-accounts-vendor-invoice-journals.md)

[SF patvirtinimai mobiliąja programa](mobile-invoice-approvals.md)

[Tiekėjo bendradarbiavimo SF išrašymo darbo sritis](vendor-portal-invoicing-workspace.md)

[Tiekėjo sąskaitų faktūrų automatizavimas](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Tiekėjo mokėjimų konfigūravimas 

Priskirkite sistemos nustatytą mokėjimo tipą, pavyzdžiui, čekį, elektroninį mokėjimą arba paprastąjį vekselį, bet kuriam vartotojo nustatytam mokėjimo būdui. Mokėjimo tipai yra pasirinktiniai, bet jie naudingi tikrinant elektroninius mokėjimus ir kai norite greitai nuspręsti, kuris mokėjimo tipas naudojamas. 

[Tiekėjo mokėjimų darbo sritis](vendor-payments-workspace.md)

[Tiekėjo mokėjimo mokesčių nustatymas](tasks/define-vendor-payment-fees.md)

[Tiekėjo mokėjimo sąlygų nustatymas](tasks/define-vendor-payment-terms.md)

[Teigiamo mokėjimo apžvalga](positive-pay-overview.md)

[Teigiamų mokėjimų failų nustatymas ir generavimas](set-up-generate-positive-pay-files.md)

[Tiekėjo mokėjimų kūrimas naudojant mokėjimo pasiūlymą](create-vendor-payments-payment-proposal.md)

[Tiekėjų dalinės sumos mokėjimai](vendor-payments-partial-amount.md)

[Nuolaidos, kuri yra didesnė už apskaičiuotą tiekėjo mokėjimo nuolaidą, pritaikymas](take-discount-more-calculated-discount-vendor-payment.md)

[Mokėjimo nuolaidos taikymas ne mokėjimo nuolaidos laikotarpiu](take-cash-discount-outside-cash-discount-timeframe.md)

[Elektroninės ataskaitos tiekėjo čekių pavyzdžiai](electronic-reporting-sample-vendor-checks.md)

[Tiekėjo mokėjimo atšaukimas](reverse-vendor-payment.md)

[Išankstinio mokėjimo sąskaitos faktūros ir išankstiniai mokėjimai](prepayments-invoices-vs-prepayments.md)

[Centralizuoti modulio Mokėtinos sumos mokėjimai](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Sudengimai

Tolesnėse temose pateikiama informacijos apie sudengimus. Sudengimas – tai mokėjimų sudengimo su sąskaitomis faktūromis procesas. 

[Sudengimo konfigūravimas](../cash-bank-management/configure-settlement.md)

[Dalinis tiekėjo mokėjimas sudengiamas prieš nuolaidos datą, kai paskutinis mokėjimas atliekamas po nuolaidos datos](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Dalinio tiekėjo mokėjimo, kuriam taikomos tiekėjo kredito pažymų nuolaidos, sudengimas](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Dalinio tiekėjo mokėjimo su keliais nuolaidos laikotarpiais sudengimas](settle-partial-vendor-payment-multiple-discount-periods.md)

[Sudengiamas dalinis tiekėjo mokėjimas ir visas paskutinis mokėjimas prieš nuolaidos datą](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Vienas kvitas su keliais kliento arba tiekėjo įrašais](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Papildomi ištekliai

#### <a name="whats-new-and-in-development"></a>Kas nauja ir kuriama

Norėdami pamatyti, kokios naujos funkcijos planuojamos, eikite į tinklalapį [„Microsoft Dynamics 365” leidimo planai](/dynamics365/release-plans/). 

#### <a name="blogs"></a>Tinklaraščiai

Galite rasti nuomonių, naujienų ir kitos informacijos apie modulį Mokėtinos sumos ir kitus sprendimus [„Microsoft Dynamics 365“ tinklaraštyje](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ir [„Microsoft Dynamics 365 Finance“ – finansai“ tinklaraštyje](https://community.dynamics.com/365/financeandoperations/b/financials).

„[Microsoft Dynamics Operations“ partnerių bendruomenės tinklaraštis](https://community.dynamics.com/partner/b/operationspartnercommunityblog) – tai vienas išteklius, kuriame „Microsoft Dynamics‟ partneriai gali sužinoti, kas nauja ir kokios yra „Dynamics 365“ tendencijos.

#### <a name="community-blogs"></a>Bendruomenės tinklaraščiai

[Kaip tvarkyti mokėtinas sumas sprendime „Dynamics 365 Finance”](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Užduočių vedliai
Programoje papildoma pagalba prieinama kaip užduočių vedliai. Norėdami pasiekti užduočių vedlius, bet kuriame puslapyje spustelėkite mygtuką Žinynas.

#### <a name="videos"></a>Vaizdo įrašai

Peržiūrėkite mokomuosius vaizdo įrašus, kuriuos dabar galite rasti [„Microsoft Dynamics 365‟ „YouTube‟ kanale](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
