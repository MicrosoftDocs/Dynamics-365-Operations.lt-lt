---
title: Grąžinimo užsakymo pinigų grąžinimas atmestas
description: Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai atmetamas grąžinimo užsakymo grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, naudojamos originalaus mokėjimo autorizavimo metu.
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
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268238"
---
# <a name="refund-on-a-return-order-is-declined"></a>Grąžinimo užsakymo pinigų grąžinimas atmestas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai atmetamas grąžinimo užsakymo grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, naudojamos originalaus mokėjimo autorizavimo metu.

## <a name="description"></a>Aprašymas

Pinigų grąžinimas atmetamas, kai grąžinimo užsakymo SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, naudotos atliekant pradinį mokėjimo autorizavimą. Gaunate toliau nurodytą klaidos pranešimą: „Kai kurių mokėjimų būsena nėra tinkama registruoti. Prieš išrašydami SF, iš naujo patikrinkite visų mokėjimų būsenas.”

Mokėjimo autorizavimo informacijoje rasite toliau nurodytą klaidos pranešimą: „Adyen“ šliuzas SendRequest() nepavyko, būsena „InternalServerError“.22144; Iš „Adyen” grąžintas tuščias atsakymas.(22001);”

![Klaida Grąžinimo užsakymo pinigų grąžinimas atmestas.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Sprendimas

### <a name="enable-blind-returns-in-adyen"></a>Įgalinti anoniminius „Adyen” grąžinimus

Norėdami įgalinti anoniminius grąžinimus, atlikite veiksmus, pateiktus [„Dynamics 365 Payment Connector“, skirtos „Adyen“, trikčių šalinimas](adyen-support.md), norėdami susisiekti su „Adyen“ palaikymo komanda ir pateikti užklausą, kad jūsų „Adyen“ prekybininko sąskaitoje būtų įjungti anoniminiai grąžinimai.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“](../dev-itpro/adyen-connector.md)

[„Adyen Payment Connector“, skirtos „Dynamics 365“, nustatymas](https://docs.adyen.com/plugins/microsoft-dynamics)
