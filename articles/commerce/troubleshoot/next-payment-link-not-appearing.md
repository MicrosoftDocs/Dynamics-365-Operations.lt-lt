---
title: Nepasirodo parinktis Įrašyti kitam mokėjimui
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke Mokėjimo būdas neatsiranda žymės lankelis Įrašyti kitam mokėjimui.
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
ms.openlocfilehash: 4887cde3e4243ae7a4da6402782e69e780ae20331ed80df63ba1239ef5187e41
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769276"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Nepasirodo parinktis „Įrašyti kitam mokėjimui”

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai el. prekybos svetainės pirkimo užbaigimo puslapio lauke **Mokėjimo būdas** neatsiranda žymės lankelis **Įrašyti kitam mokėjimui**.

## <a name="description"></a>Aprašymas

Žymės langelis **Įrašyti kitam mokėjimui** nerodomas el. prekybos svetainės pirkimo užbaigimo puslapio sekcijoje **Mokėjimo būdas**.

Šioje iliustracijoje pateikiamas pirkimo užbaigimo puslapio, kuriame yra žymės langelis **Įrašyti kitam mokėjimui**, pavyzdys.

![Žymės langelis „Įrašyti kitam mokėjimui” mokėjimo modulyje.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Patikrinkite, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”

Norėdami patikrinti, ar „Dynamics 365 Payment Connector“, skirta „Adyen“, tinkamai sukonfigūruota „Commerce Headquarters”, atlikite šiuos veiksmus.

1. Eikite į **„Retail” ir „Commerce” \> Kanalai \> Interneto parduotuvės**.
1. Pasirinkite internetinę parduotuvę.
1. Įsitikinkite, kad „FastTab” **Mokėjimo sąskaitos** laukas **Leisti įrašyti el. prekybos mokėjimo informaciją** nustatytas į **Teisinga**.

![Leisti įrašyti mokėjimo informaciją „Commerce Headquarters” elektroninės prekybos lauke.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Papildomi ištekliai

[Mokėjimo modulis](../payment-module.md)

[Internetinių mokėjimo priemonių įrašymas naudojant „Adyen“ jungtį](../dev-itpro/adyen-connector-listPI.md)
