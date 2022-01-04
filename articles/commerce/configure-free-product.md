---
title: Produkto, kuris bus perkamas nemokamai, konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti produktą, kad jį būtų galima nemokamai įsigyti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 760b97a895758073c8ffd1209be4a5f7df0f13a8
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919455"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Produkto, kuris bus perkamas nemokamai, konfigūravimas

[!include [banner](includes/banner.md)]


Šioje temoje aprašoma, kaip sukonfigūruoti produktą, kad jį būtų galima nemokamai įsigyti „Microsoft Dynamics 365 Commerce“.

## <a name="configure-the-product"></a>Produktų paieškos konfigūravimas

Norėdami parduoti produktą „Dynamics 365 Commerce“ nemokamai, jo kainą turite nustatyti kaip 0 (nulį). Be to, turite sukonfigūruoti produkto **nulinės kainos tinkamą** parametrą.

Norėdami „Commerce Headquarters" **sukonfigūruoti parametrą** Nulinė kaina galioja, atlikite šiuos veiksmus.

1. Eikite į **Mažmeną ir komerciją \> Produktai ir kategirjos \> Išleisti produktai pagal kategorijas**.
1. Eikite į produktą, kurį norite parduoti nemokamai. 
1. Produktų puslapio **Commerce** skyriuje nustatykite parinktį **Nulinė kaina** tinkama kaip **Taip**.

Šiame pavyzdyje pateikiamas produkto pavyzdys, kai nustatyta **nulinės kainos leistina** pasirinktis kaip **Taip**.

![Produkto, kai parinktis Nulinė kaina tinkama nustatyta kaip Taip, pavyzdys.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Funkcijų šablono interneto parduotuvės konfigūravimas

Kad būtų galima apdoroti laisvas operacijas, turite sukonfigūruoti **leisti tikrinti be mokėjimo parametro** jūsų interneto parduotuvėje, kad būtų leidžiama atlikti operacijas, kurios neturi mokėjimų. Informacijos apie tai, kaip sukurti funkcijų šablonus, [ieškokite Interneto funkcijų šablono kūrimas](online-functionality-profile.md).

Norėdami „Commerce Headquarters" **Leisti išregistruoti su mokėjimais** Nulinė kaina galioja, atlikite šiuos veiksmus.

1. Eikite į **Mažmena ir komercija \> Kanalo nustatymai \> Interneto parduotuvės nustatymai**.
1. Parduotuvės funkcijų šablono puslapyje dalyje srityje **Išregistravimas**, nustatykite **Leisti tikrinti be mokėjimų kaip** parinktį į **Taip**.

Šioje iliustracijoje pateikiamas interneto parduotuvės šablono pavyzdys, kur nustatyta **Leisti tikrinti be mokėjimo** parinktį į **Taip**.

![Šioje iliustracijoje pateikiamas interneto parduotuvės šablono pavyzdys, kur nustatyta Leisti tikrinti be mokėjimo parinktį į Taip.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Mažmeninės prekybos pardavimo kainų valdymas](price-management.md)

[Internetinių funkcijų šablono kūrimas](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
