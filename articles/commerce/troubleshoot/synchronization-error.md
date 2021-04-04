---
title: Užsakymo sinchronizavimo klaida, susijusi su numatytąja mokėjimo tarnyba
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti ištaisyti klaidą, kuri gali įvykti sinchronizuojant internetinį užsakymą.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585441"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Užsakymo sinchronizavimo klaida, susijusi su numatytąja mokėjimo tarnyba

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti ištaisyti klaidą, kuri gali įvykti sinchronizuojant internetinį užsakymą.

## <a name="description"></a>aprašymas

Kai sinchronizuojate internetinį užsakymą, gaunate šį klaidos pranešimą: „Norint apdoroti kredito kortelės operacijas, turi būti nustatyta numatytoji mokėjimo tarnyba.”

![Trūkstamos numatytosios mokėjimo tarnybos klaida](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Patvirtinti arba nustatyti numatytąją mokėjimo tarnybą „Commerce Headquarters”

Norėdami patvirtinti arba nustatyti numatytąją mokėjimo tarnybą „Commerce Headquarters”, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Mokėjimų sąranka \> Mokėjimo tarnybos**.
1. Įsitikinkite, kad vienos mokėjimo tarnybos parinktis **Numatytasis naujų kredito kortelių procesorius** nustatyta į **Taip**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kredito kortelių nustatymas, autorizacija ir patvirtinimas](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
