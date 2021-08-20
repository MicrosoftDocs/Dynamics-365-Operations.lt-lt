---
title: Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai pardavimo užsakymo puslapyje sinchronizavus užsakymą rodomas klaidos pranešimas.
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
ms.openlocfilehash: 03bcbedb12b95a00141d27e9a93186a7fa7dabba70147177524f604dd10ed252
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750677"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>Klaida „Mokėjimo tipas turi būti kredito kortelė” pardavimo užsakymo puslapyje

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai pardavimo užsakymo puslapyje sinchronizavus užsakymą rodomas klaidos pranešimas.

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
