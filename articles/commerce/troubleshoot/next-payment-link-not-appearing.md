---
title: Nepasirodo parinktis Įrašyti kitam mokėjimui
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai el. komercijos svetainės tikrinimo puslapyje nebus rodomas mokėjimo būdo žymės langelis Įrašyti mano kitame mokėjime.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287490"
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
