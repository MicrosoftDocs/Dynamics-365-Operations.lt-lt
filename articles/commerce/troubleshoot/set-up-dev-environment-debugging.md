---
title: Nustatykite el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina
description: Šioje temoje aiškinama, kaip nustatyti el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina (VM).
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
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019451"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Nustatykite el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti el. prekybos kūrimo aplinką, kad būtų galima derinti su „Tier 1 Retail Server“ virtualiąja mašina (VM).

## <a name="description"></a>aprašymas

„Microsoft Dynamics 365 Commerce” 1 pakopos aplinkos paprastai diegiamos dėl „Commerce Runtime” (CRT) ir elektroninis kasos aparato (EKA) plėtinio kūrimo. Jos yra atskiros aplinkos. Dėl architektūros programinės įrangos nuomos paslaugos (SaaS) jos neapima el. prekybos komponentų.

Kai kuriuose scenarijuose galite norėti patikrinti plėtinių iškvietimus 1 pakopos aplinkoje, kad būtų galima suderinti plėtinius iš el. prekybos komponentų. Bendrųjų instrukcijų ieškokite [Derinimas pagal 1 pakopos „Commerce“ plėtros aplinką](../e-commerce-extensibility/debug-tier-1.md).

Derinant su 1 pakopos aplinka, kadangi svetainė iškviečia kitą „Retail Server“, kelių serverių skambučiai gali sukelti įvairių klaidų, susijusių su turinio saugos strategija.

Toliau pateiktoje iliustracijoje nurodomas klaidos, kuri gali įvykti produkto informacijos puslapyje pasirinkus variantą, pavyzdys.

![Klaida, kai variantas pasirenkamas produkto informacijos puslapyje](media/unhandled-rejection-error.jpg)

Šioje iliustracijoje pateikiamas panašios naršyklės derintuvės įrankių (F12 programavimo įrankių) klaidos pavyzdys. Klaidos pranešime minimi turinio saugos strategijos direktyvos pažeidimai.

![Derintuvės įrankių klaida](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Sprendimas

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Išjungti svetainės turinio saugos strategiją „Commerce“ svetainių daryklėje

1. Pasirinkite svetainę, su kuria dirbate.
1. Pasirinkite **Parametrai**, tada – **Plėtiniai**.
1. Skirtuke **Turinio saugos strategija** pasirinkite **Išjungti turinio saugos strategiją**.
1. Pasirinkite **įrašyti ir publikuoti**.

> [!NOTE]
> Verslo ir vartotojų (B2C) prisijungimas neveikia vietinėje programavimo aplinkoje. Tačiau, jei reikia imituoti vartotojo prisijungimą, galite naudoti svečio pirkimo užbaigimą ar kurti puslapių maketus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo su el. prekybos išplečiamumo internetu kūrimu pradžia](../e-commerce-extensibility/sdk-getting-started.md)

[Turinio saugos strategijos (CSP) valdymas el. prekybos svetainėje](../manage-csp.md)
