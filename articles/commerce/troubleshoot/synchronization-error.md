---
title: Užsakymo sinchronizavimo klaida, susijusi su numatytąja mokėjimo tarnyba
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti ištaisyti klaidą, kuri gali įvykti sinchronizuojant internetinį užsakymą.
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021132"
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

[Kredito kortelių nustatymas, autorizacija ir patvirtinimas](../../finance/accounts-receivable/credit-card-authorizations.md)