---
title: Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai mokėjimas sudengtas „Adyen” portale iš karto po užsakymo pateikimo, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.
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
ms.openlocfilehash: cc5167be43cccfd024ffdc65eb5f4dcac7e187288522d95be2385f8e7fdf106e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718652"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai mokėjimas sudengtas „Adyen” portale iš karto po užsakymo pateikimo, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.

## <a name="description"></a>Aprašymas

Po užsakymo pateikimo mokėjimas iš karto sudengiamas „Adyen” portale, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.

## <a name="resolution"></a>Sprendimas

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Konfigūruoti el. prekybos mokėjimų rankinį fiksavimą „Adyen” portale

Norėdami konfigūruoti el. prekybos mokėjimų rankinį fiksavimą „Adyen” portale, atlikite šiuos veiksmus.

1. Prisijunkite prie „Adyen” portalo.
1. Viršutiniame dešiniajame kampe pasirinkite savo el. prekybos kanalo prekybininko sąskaitą.
1. Viršutinėje naršymo juostoje pasirinkite **Sąskaita**, tada – **Parametrai**.
1. Lauke **Fiksavimo delsa** pasirinkite **Rankinis**.

    ![Fiksavimo delsos parametras „Adyen” portale.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Papildomi ištekliai

[„Adyen“ mokėjimo fiksavimas](https://docs.adyen.com/point-of-sale/capturing-payments)

[„Dynamics 365 Payment Connector“, skirta sprendimui „Adyen“](../dev-itpro/adyen-connector.md)

[„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas](https://docs.adyen.com/plugins/microsoft-dynamics)
