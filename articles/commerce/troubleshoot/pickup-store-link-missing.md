---
title: Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės paėmimo parinktis nepasirodo krepšelio puslapyje arba produkto informacijos puslapiuose.
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
ms.openlocfilehash: 88367e13b4d079edb0816e301901828b65c437ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900313"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės paėmimo parinktis nepasirodo krepšelio puslapyje arba produkto informacijos puslapiuose.

## <a name="description"></a>aprašymas

Mygtukas **Paimti** neatsiranda krepšelio arba produkto informacijos puslapyje.

Šioje iliustracijoje pateikiamas puslapio, kuriame yra mygtukas **Paimti**, pavyzdys.

![Mygtukas Paimti.](media/pickup-button-missing.jpg)

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
