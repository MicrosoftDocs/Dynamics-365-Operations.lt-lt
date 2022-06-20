---
title: Nepasirodo parinktis Įrašyti kitam mokėjimui
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai el. komercijos svetainės tikrinimo puslapyje nebus rodomas mokėjimo būdo žymės langelis Įrašyti mano kitame mokėjime.
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
ms.openlocfilehash: efa04c87f78c376fd00da1b26aedb9e8b428dfa5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871560"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>Nepasirodo parinktis „Įrašyti kitam mokėjimui”

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje **pateikiamos** **trikčių** diagnostikos gairės, kurios gali padėti, kai el. komercijos svetainės tikrinimo puslapyje nebus rodomas mokėjimo būdo žymės langelis Įrašyti mano kitame mokėjime.

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
