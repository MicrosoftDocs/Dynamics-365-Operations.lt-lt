---
title: Nepasirodo parinktis Įrašyti kitam mokėjimui
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke Mokėjimo būdas neatsiranda žymės lankelis Įrašyti kitam mokėjimui.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801704"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Nepasirodo parinktis „Įrašyti kitam mokėjimui”

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke **Mokėjimo būdas** neatsiranda žymės lankelis **Įrašyti kitam mokėjimui**.

## <a name="description"></a>Aprašymas

Žymės langelis **Įrašyti kitam mokėjimui** nerodomas el. prekybos svetainės pirkimo užbaigimo puslapio sekcijoje **Mokėjimo būdas**.

Šioje iliustracijoje pateikiamas pirkimo užbaigimo puslapio, kuriame yra žymės langelis **Įrašyti kitam mokėjimui**, pavyzdys.

![Žymės langelis „Įrašyti kitam mokėjimui” mokėjimo modulyje](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Patikrinkite, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”

Norėdami patikrinti, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”, atlikite šiuos veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> Kanalai \> Interneto parduotuvės**.
1. Pasirinkite internetinę parduotuvę.
1. Įsitikinkite, kad „FastTab” **Mokėjimo sąskaitos** laukas **Leisti įrašyti el. prekybos mokėjimo informaciją** nustatytas į **Teisinga**.

![Leisti įrašyti mokėjimo informaciją „Commerce Headquarters” el. prekybos lauke](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Papildomi ištekliai

[Mokėjimo modulis](../payment-module.md)

[Internetinių mokėjimo priemonių įrašymas naudojant „Adyen“ jungtį](../dev-itpro/adyen-connector-listPI.md)
