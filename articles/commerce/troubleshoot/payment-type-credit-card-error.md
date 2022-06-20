---
title: Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai pardavimo užsakymo puslapyje, sinchronizuojant užsakymą, rodomas klaidos pranešimas.
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
ms.openlocfilehash: 794317a84a8a0ff205ac1b6a5caa6ef1cf098ea3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905348"
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
