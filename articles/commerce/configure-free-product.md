---
title: Produkto, kuris bus perkamas nemokamai, konfigūravimas
description: Šiame straipsnyje aprašoma, kaip sukonfigūruoti produktą, kad jį būtų galima nemokamai pirkti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280370"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Produkto, kuris bus perkamas nemokamai, konfigūravimas

[!include [banner](includes/banner.md)]


Šiame straipsnyje aprašoma, kaip sukonfigūruoti produktą, kad jį būtų galima nemokamai pirkti Microsoft Dynamics 365 Commerce.

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
