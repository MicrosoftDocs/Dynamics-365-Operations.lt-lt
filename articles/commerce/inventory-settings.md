---
title: Atsargų parametrų taikymas
description: Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7d25fd62efca52dd2d60ed3435104c3507a1d19
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817614"
---
# <a name="apply-inventory-settings"></a>Atsargų parametrų taikymas

[!include [banner](includes/banner.md)]

Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Atsargų parametrai nurodo, ar atsargos turi būti patikrintos prieš įtraukiant produktus į krepšelį. Jie taip pat apibrėžia su atsargomis susijusius prekybos pranešimus, pvz., „Sandėlyje“ ir „Liko vos keli“. Šie parametrai užtikrina, kad produkto nepavyktų įsigyti, jei jo atsargos pasibaigė.

„Dynamics 365 Commerce“ pateikiamas turimų produktų atsargų kiekis. Norėdami gauti daugiau informacijos apie tai, kaip apskaičiuojamas turimų atsargų pasiekiamumas, žr [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).

Svetainės kūrimo priemonėje „Commerce“ galima nustatyti produkto ar kategorijos atsargų ribines vertes ir diapazonus. Jos nustato, ar atsargos gali būti klasifikuojamos kaip „yra atsargų“, „mažai atsargų“ arba „nebėra atsargų“. Jei reikia išsamios informacijos, žr. [Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md).

> [!NOTE]
> Atsargų ribų ir diapazonų palaikymas yra prieinamas „Dynamics 365 Commerce“ 10.0.12 leidime.

## <a name="inventory-settings"></a>Atsargų parametrai

Programoje „Commerce“ atsargų parametrai apibrėžiami **Svetainės parametrai \> Plėtiniai \> Atsargų valdymas** svetainės kūrimo priemonėje. Yra keturi atsargų parametrai, iš kurių vienas yra pasenęs (nerekomenduojamas):

- **Įjungti atsargų tikrinimą programoje** – šis parametras įjungia produkto atsargų tikrinimą. Tada pirkimo langelio, krepšelio ir atsiėmimo parduotuvėje moduliai patikrina produkto atsargas ir leidžia įtraukti produktą į krepšelį, tik jei yra atsargų.
- **Atsargų lygio pagrindas** – šis parametras nurodo, kaip apskaičiuojamas atsargų lygis. Galimos reikšmės: **Iš viso pasiekiama**, **Fiziškai pasiekiama**ir **Pasibaigusių atsargų slenkstis**. Programoje „Commerce“ galima nustatyti kiekvieno produkto ir kategorijos atsargų ribinę vertę ir diapazonus. Atsargų API pateikia produkto atsargų informaciją, skirtą ypatybėms **Iš viso pasiekiama** ir **Fiziškai pasiekiama**. Mažmenininkas sprendžia, ar **Iš viso pasiekiama** arba **Fiziškai pasiekiama** reikšmės turėtų būti naudojamos atsargų kiekiui ir atitinkamiems diapazonams esančių ir nesančių atsargų būsenai nustatyti.

    Parametro **Atsargų lygio pagrindas** reikšmė **Pasibaigusių atsargų slenkstis** yra pasenusi (senstelėjusi), nebenaudojama reikšmė. Ją pasirinkus, atsargų skaičius nustatomas pagal reikšmės **Iš viso pasiekiama** rezultatus, bet slenkstį apibrėžia toliau aprašytas skaitinis parametras **Pasibaigusių atsargų slenkstis**. Šis slenksčio parametras taikomas visiems el. prekybos svetainės produktams. Jei atsargos mažesnės už ribinę vertę, laikoma, kad produkto atsargos pasibaigusios. Priešingu atveju laikoma, kad jo atsargų yra. Reikšmės **Pasibaigusių atsargų slenkstis** galimybės yra ribotos ir nerekomenduojame jų naudoti 10.0.12 ir naujesnėje versijoje.

- **Atsargų diapazonai** – šis parametras apibrėžia atsargų diapazonus, kurie bus rodomi dėl svetainės moduliuose. Jis taikomas tik tuo atveju, jei reikšmės **Iš viso pasiekiama** arba **Fiziškai pasiekiama** pasirinktos parametrui **Atsargų lygio pagrindas**. Galimos vertės yra **Visos**, **Mažai ir nebėra** ir **Nebėra**.

    - Pasirinkus **Visos** bus rodomi pranešimai apie visus atsargų diapazonus nuo „yra atsargų“ (pranešimas „Yra“) iki „nebėra atsargų“ (pranešimas „nebėra atsargų“).
    - Pasirinkus **Mažai ir nebėra** bus rodomi pranešimai apie visus atsargų diapazonus, išskyrus „yra atsargų“ (pranešimas „Yra“).
    - Pasirinkus **Nėra atsargų**, bus rodomas tik pranešimas „Nėra atsargų“.

- **Pasibaigusių atsargų slenkstis** – Šis senas skaitinis parametras įsigalios tik tada, jei reikšmė **Pasibaigusių atsargų slenkstis** pasirenkama parametrui **Atsargų lygio pagrindas**.

> [!IMPORTANT] 
> Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduliai, kurie naudoja atsargų parametrus

Pirkimo langelis, pageidavimų sąrašas, parduotuvės parinkiklis, krepšelis ir krepšelio piktogramos moduliai naudoja atsargų parametrus, kad būtų rodomi atsargų diapazonai ir pranešimai.

Toliau pateiktame paveikslėlyje parodytas produkto informacijos puslapis (PDP), kuriame pateikiamas pranešimas, kad atsargų yra („Yra“).

![PDP modulio su atsargų pranešimu, pavyzdys](./media/pdp-InStock.png)

Toliau pateiktame paveikslėlyje rodomas PDP puslapis, kuriame pateikiamas pranešimas „Nėra atsargų“.

![PDP modulio su pasibaigusių atsargų pranešimu, pavyzdys](./media/pdp-outofstock.png)

Toliau pateiktame paveikslėlyje rodomas krepšelis, kuriame pateikiamas pranešimas, kad atsargų yra („Yra“).

![Krepšelio modulio su atsargų pranešimu, pavyzdys](./media/cart-instock.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Sąskaitos valdymo puslapiai ir moduliai](account-management.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)
