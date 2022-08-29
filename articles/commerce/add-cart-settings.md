---
title: Prekės įtraukimo į krepšelį parametrų taikymas
description: Šiame straipsnyje aprašomi parametrai Įtraukti produktą į krepšelį ir aprašoma, kaip juos taikyti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277033"
---
# <a name="apply-add-product-to-cart-settings"></a>Prekės įtraukimo į krepšelį parametrų taikymas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi **produkto į krepšelio** parametrus įtraukimas ir aprašoma, kaip juos taikyti Microsoft Dynamics 365 Commerce.

Skirtingos darbo eigos yra palaikomos, kai produktas įtraukiamas į krepšelį „Dynamics 365 Commerce” elektroninės prekybos svetainėje. Pavyzdžiui, svetainės vartotojas gali būti perkeltas į krepšelio puslapį. Kitu atveju vartotojas gali likti dabartiniame puslapyje, bet gauti pranešimą, patvirtinantį, kad produktas įtrauktas į krepšelį.

Siekiant palaikyti skirtingas darbo eigas, laukas **Įtraukti produktą į krepšelį** yra galimas **Parametrai \> Plėtiniai** „Commerce” svetainių generatoriuje. Norėdami įdiegti atitinkamą darbo eigą, pasirinkite vieną iš šių parametrų parinkčių:

- **Pereiti į krepšelio puslapį** – kai vartotojai prideda prekę į krepšelį, jie yra siunčiami į krepšelio puslapį.
- **Rodyti pranešimą** – kai vartotojai prideda prekę į krepšelį, jie gauna patvirtinimo pranešimą ir gali tęsti naršymą produkto išsamios informacijos (PDP) puslapyje.
- **Rodyti mažą krepšelį** – kai vartotojai įtraukia prekę į krepšelį, rodomas mažo krepšelio turinys. Vartotojai gali peržiūrėti visas krepšelyje esančias prekes ir pereiti į apmokėjimą, jei jie pasiruošę.
- **Rodyti pranešimą naudojant pranešimų modulį** – kai vartotojai įtraukia prekę į krepšelį, pranešimų modulis naudojamas patvirtinimo pranešimui rodyti. Tam, kad ši parametro parinktis veiktų, pranešimų modulis turi būti įtrauktas į puslapio antraštę.
- **Nepereiti į krepšelio puslapį** – kai vartotojai prideda prekę į krepšelį, jie lieka dabartiniame puslapyje.

Šioje iliustracijoje pateikiamas **Įtraukti produktą į krepšelį** parametro parinkčių svetainės generatoriuje pavyzdys.

![Produkto pridėjimo į krepšelį parametro parinkčių svetainės generatoriuje pavyzdys](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **Įtraukti produktą į vežimėlį** svetainės nustatymai yra prieinami 10.0.11 „Dynamics 365 Commerce“ versijos leidime. Jeigu jūs atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti „appsettings.json” failą. Daugiau informacijos apie tai, kaip atnaujinti „appsettings.json” failą, rasite [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Parametrų parinktis **Rodyti mažą krepšelį** galima 10.0.20 „Dynamics 365 Commerce” versijos leidime. Jeigu jūs atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti „appsettings.json” failą. Daugiau informacijos apie tai, kaip atnaujinti „appsettings.json” failą, rasite [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Toliau pateiktoje iliustracijoje parodytas „Fabrikam“ puslapyje esančio patvirtinimo pranešimo „Įtraukta į krepšelį“ pavyzdys.

![„Fabrikam“ puslapyje esančio patvirtinimo pranešimo „Įtraukta į krepšelį“ pavyzdys](./media/ecommerce-addtocart-notifications.PNG)

Toliau pateiktoje iliustracijoje parodytas „Adventure Works“ puslapyje esančio patvirtinimo pranešimo „Įtraukta į krepšelį“ pavyzdys.

![„Adventure Works“ puslapyje esančio patvirtinimo pranešimo „Įtraukta į krepšelį“ pavyzdys](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)
