---
title: Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020816"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.

## <a name="description"></a>aprašymas

Mygtukas **Paimti** neatsiranda krepšelio arba produkto informacijos puslapyje.

Šioje iliustracijoje pateikiamas puslapio, kuriame yra mygtukas **Paimti**, pavyzdys.

![Mygtukas Paimti](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Įgalinti BOPIS plėtinį „Commerce” svetainių daryklėje

Norėdami įgalinti plėtinį „Pirkti internetu, paimti parduotuvėje” (BOPIS) „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.

1. Pasirinkite jūsų svetainę.
1. Pasirinkite **Svetainės parametrai**, tada – **Plėtiniai**.
1. Įsitikinkite, kad parinktis **Išjungti BOPIS** išvalyta.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Pristatymo būdų konfigūravimas „Commerce Headquarters”

Norėdami konfigūruoti pristatymo būdus „Commerce Headquarters“, atlikite šiuos žingsnius.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Pristatymo būdai**.
1. Įsitikinkite, kad sukurtas pristatymo būdas **Kliento paėmimas** ir jam priskirti produktai bei adresai.
1. Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.
1. Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.
1. Įsitikinkite, kad **Pristatymo paėmimo būdas** tinkamai sukonfigūruotas.

### <a name="configure-customer-orders-payments"></a>Kliento užsakymų mokėjimų konfigūravimas

Norėdami konfigūruoti kliento užsakymų mokėjimus „Commerce Headquarters“, atlikite šiuos veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.
1. Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.
1. „FastTab” **Mokėjimai** įsitikinkite, kad laukai **Mokėjimo sąlygos** ir **Mokėjimo būdas** nustatyti teisingai.

## <a name="additional-resources"></a>Papildomi ištekliai

[BOPIS konfigūravimas](../cpe-bopis.md)

[Įjungti keletą paėmimo pristatymo režimų kliento užsakymams](../multiple-pickup-modes.md)

[Daugiakanaliai „Commerce“ užsakymų mokėjimai](../dev-itpro/commerce-payments.md)

[Parduotuvės išrinkiklio modulis](../store-selector.md)
