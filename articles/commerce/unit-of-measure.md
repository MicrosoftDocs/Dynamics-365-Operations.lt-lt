---
title: Taikyti matavimo vieneto parametrus
description: Šioje temoje aptariami atsargų matavimo vienetų nustatymai ir aprašoma, kaip juos taikyti programoje „Microsoft Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 076d4a68362dbf11c5fcf223a836f075d07e27a3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350333"
---
# <a name="apply-unit-of-measure-settings"></a>Taikyti matavimo vieneto parametrus

[!include [banner](includes/banner.md)]

Šioje temoje aptariami atsargų matavimo vienetų nustatymai ir aprašoma, kaip juos taikyti programoje „Microsoft Microsoft Dynamics 365 Commerce“.

Produktą galima parduoti skirtingais vienetais, pvz., „kiekviena," „pora" ir „tuzinas". „Commerce Headquarters" galima nurodyti produkto pardavimo matavimo vienetą, kuris rodomas el. komercijos svetainėje. Pavyzdžiui, jei mažmenininkas parduoda produktą ir individualiai, ir tuzinais, turimi matavimo vienetai gali būti rodomi kartu su kita informacija apie produktą.

Toliau pateiktame pavyzdyje parodytas produkto pardavimo vienetas pagal matavimo **vienetą** „Commerce Headquarters" konfigūruotas.

![Produkto, sukonfigūruotas naudojant matavimo vienetą „Commerce Headquarters”, pavyzdys.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Galima naudoti „Commerce" 10.0.19 versijos leidimą, siekiant pritaikyti ir rodyti matavimo vienetą.

## <a name="unit-of-measure-settings"></a>Matavimo vieneto parametrai

Matavimo vieneto ekrano parametrai apibrėžti „Commerce Site Builder", prie **svetainės \> parametrų \> plėtinių produktų rodymo matavimo vienetas**. Yra trys palaikomi parametrai:

- **Nerodyti** – kai šis parametras pasirinktas, el. komercijos svetainėje nebus rodomas produkto matavimo vienetas. Tai numatytasis elgesys.
- **Rodyti produkto pirkimo patirties puslapyje – pasirinkus šį parametrą, matavimo vienetas rodomas produkto duomenyse, krepšelyje, išregistravimo, užsakymo retrospektyvos ir užsakymo** informacijos puslapiuose.
- **Rodyti produktų naršymo ir pirkimo patirtį – pasirinkus šį parametrą, matavimo vienetas rodomas produktų pirkimo patirties puslapiuose ir produktų** naršymo patirties metu. Kaip šių veiksmų dalis rodoma ieškos rezultatų ir produktų rinkinio moduliuose.

> [!IMPORTANT]
> Matavimo vienetų rodymo parametrai galimi pagal „Commerce" 10.0.19 versiją. Jei atnaujinate iš senesnės „Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Dėl nurodymų, žr. [SDK ir modulio bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Moduliai, naudojanti matavimo vieneto parametrus

Moduliuose, kuriuose naudojami matavimo vienetų parametrai, yra pirkimo dėžės, pageidavimų sąrašo, krepšelio, krepšelio piktogramos, ieškos rezultatų konteinerio, produktų rinkinio, tikrinimo ir užsakymo informacijos moduliai.

Toliau pateiktame pavyzdyje produkto informacijos puslapis (PDP) rodo produkto matavimo **vienetą** (lt).

![PDP, kuriame rodomas matavimo vienetas, pavyzdys.](./media/Productunit-PDP.png)

Toliau pateiktame pavyzdyje produkto surinkimo modulis rodo produkto matavimo **vienetą** (lt).

![Produkto surinkimo mudlis, kuriame rodomas matavimo vienetas, pavyzdys.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Sąskaitos valdymo puslapiai ir moduliai](account-management.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
