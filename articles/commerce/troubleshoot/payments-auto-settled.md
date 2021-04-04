---
title: Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai mokėjimas sudengtas „Adyen” portale iš karto po užsakymo pateikimo, net jei nebuvo išrašyta pardavimo užsakymo SF arba jis nebuvo išsiųstas.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585447"
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

    ![Fiksavimo delsos parametras „Adyen” portale](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Papildomi ištekliai

[„Adyen“ mokėjimo fiksavimas](https://docs.adyen.com/point-of-sale/capturing-payments)

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](../dev-itpro/adyen-connector.md)

[„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas](https://docs.adyen.com/plugins/microsoft-dynamics)
