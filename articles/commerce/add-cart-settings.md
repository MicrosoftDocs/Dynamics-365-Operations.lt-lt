---
title: Prekės įtraukimo į krepšelį parametrų taikymas
description: Šioje temoje aprašomi „Įtraukti produktą į krepšelį” parametrai ir tai, kaip juos taikyti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c1d29b84d79ab503580478a1553514ddf992ca46
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637982"
---
# <a name="apply-add-product-to-cart-settings"></a>Prekės įtraukimo į krepšelį parametrų taikymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi **Įtraukti produktą į krepšelį** parametrai ir tai, kaip juos taikyti „Microsoft Dynamics 365 Commerce“.

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
