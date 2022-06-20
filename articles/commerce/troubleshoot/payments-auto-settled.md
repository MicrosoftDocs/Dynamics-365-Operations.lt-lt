---
title: Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimas yra sudengtas Adyen portale iš karto po užsakymo pateikimo, net jei pardavimo užsakymui nebuvo išrašyta SF arba jis išsiųstas.
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
ms.openlocfilehash: c01a2fda54e198a43fa84ae83686fc1701958b6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890274"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Mokėjimai automatiškai sudengiami prieš išrašant užsakymų SF arba juos išsiunčiant

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai mokėjimas yra sudengtas Adyen portale iš karto po užsakymo pateikimo, net jei pardavimo užsakymui nebuvo išrašyta SF arba jis išsiųstas.

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
