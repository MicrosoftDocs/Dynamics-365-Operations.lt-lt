---
title: Grąžinimo užsakymo pinigų grąžinimas atmestas
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai atmetamas grąžinimo užsakymo pinigų grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, kuri buvo naudojama atliekant pradinį mokėjimo autorizavimą.
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
ms.openlocfilehash: 8880d72d702758d611755bce48a331e3f2e28ca1b7abf485e8b4f7301317c875
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738629"
---
# <a name="refund-on-a-return-order-is-declined"></a>Grąžinimo užsakymo pinigų grąžinimas atmestas

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai atmetamas grąžinimo užsakymo pinigų grąžinimas, nes SF išrašyti naudojama kredito kortelė skiriasi nuo kortelės, kuri buvo naudojama atliekant pradinį mokėjimo autorizavimą.

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
