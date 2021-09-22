---
title: Įsigijimas DUK
description: Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus (DUK) apie „Supply Chain Management“ tiekimas produkto informacijos valdymo funkciją.
author: kamaybac
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 09c99b88bc47609158805cdba1291ae462cda178
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477041"
---
# <a name="procurement-faq"></a>Įsigijimas DUK

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami atsakymai į dažnai užduodamus klausimus (DUK) apie „Supply Chain Management“ tiekimas produkto informacijos valdymo funkciją.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Ar galima rodyti tik savo sukurtus pirkimo užsakymus?

Šiuo metu ši funkcija negalima.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Ar galiu rezervuoti atsargas ir sukurti operacijas su užregistruotomis atsargomis pirkimo užsakyme?

### <a name="issue-description"></a>Problemos aprašas

Net kai pirkimo užsakymo prekių būsena yra *Registruota*, jūs vis tiek galite rezervuoti atsargas. Kitaip tariant, galite sukurti operacijas su užregistruotomis atsargomis.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Sukurkite pirkimo užsakymą.
2. Užregistruokite pirkimo užsakymo eilutę.
3. Atkreipkite dėmesį, kad galite generuoti rezervavimus arba operacijas su užregistruotomis atsargomis.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Tikimasi, kad užregistruotos prekės faktiškai atvyko į sandėlį arba į atsargas ir todėl jas galima rezervuoti.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Ar galima rasti vartotoją, kuris atšaukė pirkimo užsakymą?

Ši informacija sekama tik tada, kai pirkimo užsakymui taikomas pakeitimų valdymas. Jei naudojate keitimų valdymą, galite matyti, kas pateikė pakeitimą (atšaukimą) ir kas jį patvirtino.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Kodėl negalima susieti pirkimo sutarties su esamu pirkimo užsakymu?

Pirkimo sutartis turi būti siejama su pirkimo užsakymo eilute, kai pirkimo užsakymas yra kuriamas. Kitu atveju pirkimo užsakymo eilutės negali būti susietos su pirkimo sutarties eilutėmis.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Kokia patikra paleidžia pranešimą „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu”?

Kai pakeičiate siuntimo datą, galite gauti pranešimą, kuriame teigiama: „Atnaujinti kainas ir nuolaidas, įvestas rankiniu būdu arba išoriniu dokumentu.” Šis pranešimas gaunamas, nes pasikeitus siuntimo datai, gali būti suaktyvinta skirtinga prekybos arba pardavimo sutartis ir tai sukelti kainos keitimą. Siuntimo datos pakeitimas taip pat gali paveikti sandėlio grafikus ir kitą susijusią informaciją.

Pranešimas paleidžiamas, kai pasikeičia bet kuri iš datų arba kai kurie kiti parametrai. Pranešimo paskirtis yra įsitikinti, kad žinote apie kainos pakeitimus, kurie gali kilti dėl šių pasikeitimų.

Pranešimas yra prekybos sutarties vertinimo (TAE) raginimas. Norėdami gauti išsamų aprašą, žr. [Prekybos sutarties vertinimo strategijos](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Kodėl negaliu registruoti daugiau nei vienos pirkimo užsakymo eilutės, kuriai priklauso kategorija pagrįstos prekės, SF?

Kiekis yra privalomas, jei norite registruoti SF. Todėl, jei visam eilutės kiekiui, kuriam SF išrašyta, yra išrašoma tik dalinė suma, ant kitos SF likusios sumos išrašyti negalėsite.
