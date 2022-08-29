---
title: Taikyti matavimo vieneto parametrus
description: Šiame straipsnyje aprašomi matavimo vienetų parametrai ir aprašoma, kaip juos taikyti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 7a7be6395a8bfce38e84f850bd792f358941c18a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275577"
---
# <a name="apply-unit-of-measure-settings"></a>Taikyti matavimo vieneto parametrus

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi matavimo vienetų parametrai ir aprašoma, kaip juos taikyti Microsoft Dynamics 365 Commerce.

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
