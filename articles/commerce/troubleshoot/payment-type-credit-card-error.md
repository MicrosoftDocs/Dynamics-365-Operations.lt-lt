---
title: Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai pardavimo užsakymo puslapyje, sinchronizuojant užsakymą, rodomas klaidos pranešimas.
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
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285638"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai pardavimo užsakymo puslapyje, sinchronizuojant užsakymą, rodomas klaidos pranešimas.

## <a name="description"></a>Aprašymas

Kai sinchronizavę užsakymą atidarote pardavimo užsakymo puslapį, gaunate tokį klaidos pranešimą: „Mokėjimo tipas turi būti kredito kortelė, nes nurodytas kredito kortelės numeris.“

![Klaida Mokėjimo tipas turi būti kredito kortelė.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Nustatyti mokėjimo tipą „Commerce Headquarters”

1. Pasirinkite **Gautinos sumos \> Mokėjimų sąranka \> Mokėjimo sąlygos**.
1. Kairiojoje naršymo srityje pasirinkite mokėjimo sąlygas.
1. Lauke **Mokėjimo tipas** patikrinkite, ar pasirinkta **Kredito kortelė**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pardavimo ir mokėjimų internetu registravimas](../tasks/posting-online-sales-payments.md)
