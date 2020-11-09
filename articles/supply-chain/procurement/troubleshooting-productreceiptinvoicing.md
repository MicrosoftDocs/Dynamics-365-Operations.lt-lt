---
title: Gavimo dokumentų ir sąskaitos faktūros (SF) išrašymo trikčių šalinimas
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su gavimo dokumentais ir SF išrašymu.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
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
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018634"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>Gavimo dokumentų ir sąskaitos faktūros (SF) išrašymo trikčių šalinimas

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su gavimo dokumentais ir SF išrašymu.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Negaliu registruoti daugiau nei vienos pirkimo užsakymo eilutės, kuriai priklauso kategorija pagrįstos prekės, SF.

Kiekis yra privalomas, jei norite registruoti SF. Todėl, jei visam eilutės kiekiui, kuriam SF išrašyta, yra išrašoma tik dalinė suma, ant kitos SF likusios sumos išrašyti negalėsite.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Pirkimo užsakymo patvirtinimo metu gaunu klaidos pranešimą „Objekto nuoroda nenustatyta”, arba parodoma išimtis „Iškvietimo paskirties vieta pranešė apie išimtį” tiekėjo SF registravimo metu.

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis* , eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>Negaliu konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą.

Negalite konsoliduoti kelių gavimo dokumentų į vieną pirkimo užsakymą, jei skirtingų gavimo dokumentų eilučių apskaitos datos skiriasi.

Šioje situacijoje, ankstesnėse „Microsoft Dynamics 365 Supply Chain Management” versijose, konsolidavimas buvo leistinas. Tačiau ši praktika yra linkusi į klaidą. Sukuriamų pirkimo užsakymo eilučių apskaitos data neturėtų skirtis nuo gavimo dokumento eilučių, kur buvo sukurtos šios pirkimo užsakymo eilutės, apskaitos datos. (Pirkimo užsakymo eilučių apskaitos data sutampa su pirkimo užsakymo antraštės apskaitos data.) Todėl kelių gavimo dokumentų konsolidavimas į vieną pirkimo užsakymą nebeleidžiamas.

Apskaitos data naudojama, pvz., biudžeto lėšų rezervavimui ir biudžeto rezervavimui. Todėl ji turi būti laikoma perėjimo iš gavimo dokumento į pirkimo užsakymą metu.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>Atšaukiant gavimo dokumentus, operacijos gali būti registruojamos laikinai sustabdytoje DK sąskaitoje.

### <a name="issue-description"></a>Problemos aprašas

Jei gavimo dokumentas yra atšauktas, sistema leidžia operacijas užregistruoti laikinai sustabdytose DK sąskaitose, net jei pagrindinės sąskaitos yra sustabdytos.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. **Mokėtinų sumų parametrai** puslapyje, skirtuke **Bendra** , įsitikinkite, kad parinktis **Gavimo dokumentą registruoti DK** nustatyta kaip *Taip*.
1. Sukurkite pirkimo užsakymą ir pridėkite užsakymo eilutę, kurioje yra kiekis lygus *1000* vienam produktui.
1. Patvirtinkite pirkimo užsakymą.
1. Užregistruokite gavimo dokumentą ir patikrinkite kvitus.
1. Sustabdykite atitinkamas pagrindines sąskaitas, *200140* ir *140200*.
1. Atšaukite užregistruotą gavimo dokumentą.
1. Atkreipkite dėmesį, kad operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Operacijos gali būti registruojamos laikinai sustabdytose DK sąskaitose, kai atšaukiami gavimo dokumentai, nes toks veikimo būdas leidžia atlikti teisingus registravimus.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>Produkto gavimo kvito numeris sunaudotas, net jei produkto gavimo metu nesukuriamas joks fin. kvitas.

Jei pasirinktis **Sukaupti įsipareigojimus gavimo dokumente** prekės modelių grupei nustatyta kaip *Ne* , didžiojoje knygoje nebus vykdomi jokie registravimai. Tačiau faktinis įvykis bus įrašytas papildomos knygos apskaitos tikslais, o tam įvykiui būtinas kvito numeris. Šis kvito numeris yra numeris, nurodomas atsargų operacijose.

Rekomenduojame nustatyti pasirinktį **Sukaupti įsipareigojimus gavimo dokumente** kaip *Taip* , kaip ir aprašyta šiame tinklaraščio įraše: [Registruoti pap. išlaidas produkto gavimo metu](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>„Registruoti DK mokesčių sąskaitoje” parametras nėra įjungtas.

### <a name="issue-description"></a>Problemos aprašas

Ši problema atsiranda, kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF** , esančiame **Mokėtinų sumų parametrai** puslapyje.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
1. **SF** skirtuke nustatykite pasirinktį **Registruoti DK mokesčių sąskaitoje** kaip *Taip*.
1. Eikite į **Atsargų valdymas \> Sąranka \> Registravimas \> Registravimas**.
1. **Pirkimo užsakymas** skirtuke įsitikinkite, kad panaikinote visas produkto pirkimo išlaidų eilutes.
1. Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Sukurkite pirkimo užsakymą. **Tiekėjo sąskaita** lauke pasirinkite *1001 Acme biuro reikmenys*.
1. Pridėkite pirkimo užsakymo eilutę, kuriai nustatyti šie parametrai:

    - **Prekės numeris:** *D0011 lazerinis projektorius*
    - **Vieta:** *1*
    - **Sandėlis:** *11*
    - **Kiekis:** *4*

1. Veiksmų srities skirtuke **Pirkimas** , grupėje **Veiksmas** , pasirinkite **Patvirtinti**.
1. Veiksmų srities skirtuke **Gauti** , grupėje **Generuoti** , pasirinkite **Gavimo dokumentas**.
1. Dialogo lange **Registruojamas gavimo dokumentas** , lauke **Gavimo dokumentas** , įveskite pasirinktinį numerį ir pasirinkite **Gerai**.
1. Veiksmų srities skirtuke **SF** , esančiame grupėje **Generuoti** , pasirinkite **SF**.
1. Lauke **Numeris** įveskite pasirinktinį numerį kaip SF numerį.
1. Atnaujinkite gretinimo būseną ir registruokite.
1. Atkreipkite dėmesį, kad kai generuojate SF iš pirkimo užsakymo, dabar gausite šią klaidą: „Produkto pirkimo išlaidų operacijos tipui sąskaitos numerio nėra.”

### <a name="issue-resolution"></a>Problemos paaiškinimas

Tai priklauso nuo SF ir SF grupių parametrų nustatymų. Norėdami gauti daugiau informacijos, žr. šį tinklaraščio įrašą: [Pirkimo mokesčio ir atsargų nuokrypio apskaita](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
