---
title: Atsargų parametrų taikymas
description: Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: f57f1f941fe0c0c70394d1ecbf8d88a13c7a3682fdfa8b5439a4f3830f616876
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765271"
---
# <a name="apply-inventory-settings"></a>Atsargų parametrų taikymas

[!include [banner](includes/banner.md)]

Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.

Atsargų parametrai nurodo, ar atsargos turi būti patikrintos prieš įtraukiant produktus į krepšelį. Jie taip pat apibrėžia su atsargomis susijusius prekybos pranešimus, pvz., „Sandėlyje“ ir „Liko vos keli“. Šie parametrai užtikrina, kad produkto nepavyktų įsigyti, jei jo atsargos pasibaigė.

„Dynamics 365 Commerce“ pateikiamas turimų produktų atsargų kiekis. Norėdami gauti daugiau informacijos apie tai, kaip apskaičiuojamas turimų atsargų pasiekiamumas, žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).

Svetainės kūrimo priemonėje „Commerce“ galima nustatyti produkto ar kategorijos atsargų ribines vertes ir diapazonus. Jos nustato, ar atsargos gali būti klasifikuojamos kaip „yra atsargų“, „mažai atsargų“ arba „nebėra atsargų“. Jei reikia išsamios informacijos, žr. [Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md).

> [!NOTE]
> Atsargų ribų ir diapazonų palaikymas yra prieinamas „Dynamics 365 Commerce“ 10.0.12 leidime.

## <a name="inventory-settings"></a>Atsargų parametrai

Programoje „Commerce“ atsargų parametrai apibrėžiami **Svetainės parametrai \> Plėtiniai \> Atsargų valdymas** svetainės kūrimo priemonėje. Yra penki atsargų parametrai, iš kurių vienas yra pasenęs (nerekomenduojamas):

- **Įjungti atsargų tikrinimą programoje** – Šis nustatymas įjungia gaminio inventoriaus patikrinimą. Tada pirkimo langelio, krepšelio ir atsiėmimo parduotuvėje moduliai patikrina produkto atsargas ir leidžia įtraukti produktą į krepšelį, tik jei yra atsargų.
- **Atsargų lygio pagrindas** – šis parametras nurodo, kaip apskaičiuojamas atsargų lygis. Galimos reikšmės: **Iš viso pasiekiama**, **Fiziškai pasiekiama** ir **Pasibaigusių atsargų slenkstis**. Programoje „Commerce“ galima nustatyti kiekvieno produkto ir kategorijos atsargų ribinę vertę ir diapazonus. Atsargų API pateikia produkto atsargų informaciją, skirtą ypatybėms **Iš viso pasiekiama** ir **Fiziškai pasiekiama**. Mažmenininkas sprendžia, ar **Iš viso pasiekiama** arba **Fiziškai pasiekiama** reikšmės turėtų būti naudojamos atsargų kiekiui ir atitinkamiems diapazonams esančių ir nesančių atsargų būsenai nustatyti.

    Parametro **Atsargų lygio pagrindas** reikšmė **Pasibaigusių atsargų slenkstis** yra pasenusi (senstelėjusi), nebenaudojama reikšmė. Ją pasirinkus, atsargų skaičius nustatomas pagal reikšmės **Iš viso pasiekiama** rezultatus, bet slenkstį apibrėžia toliau aprašytas skaitinis parametras **Pasibaigusių atsargų slenkstis**. Šis slenksčio nustatymas taikomas visiems produktams visame e-komercijos saite. Jei atsargos mažesnės už ribinę vertę, laikoma, kad produkto atsargos pasibaigusios. Priešingu atveju laikoma, kad jo atsargų yra. Reikšmės **Pasibaigusių atsargų slenkstis** galimybės yra ribotos ir nerekomenduojame jų naudoti 10.0.12 ir naujesnėje versijoje.

- **Kelių sandėlių atsargų lygis – šis parametras leidžia apskaičiuoti atsargų lygį pagal numatytąjį** sandėlį arba kelis sandėlius. Pasirinktis **Pagal atskirą** sandėlį apskaičiuos atsargų lygius pagal numatytąjį sandėlį. Arba el. komercijos svetainė gali nurodyti kelis sandėlius, kad būtų lengviau įvykdyti. Tokiu atveju **parinktis Pagal siuntimo ir paėmimo sandėlių suvestinę** naudojama nurodant atsargas. Pavyzdžiui, kai klientas perka prekę ir kaip pristatymo būdą pasirenka "siuntimas", prekę galima siųsti iš bet kurio įvykdymo grupės sandėlio, turimo atsargų. Produkto informacijos puslapyje (PDP) bus rodomas pranešimas "Atsargose", skirtas siuntai, jei įvykdymo grupėje yra siuntimo sandėlių atsargų. 

> [!IMPORTANT] 
> Kelių **sandėlių parametrų atsargų lygis** pasiekiamas naudojant „Commerce" 10.0.19 versiją. Jei atnaujinate iš senesnės „Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Dėl nurodymų, žr. [SDK ir modulio bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

- **Atsargų diapazonai** – šis parametras apibrėžia atsargų diapazonus, kurie bus rodomi dėl svetainės moduliuose. Jis taikomas tik tuo atveju, jei reikšmės **Iš viso pasiekiama** arba **Fiziškai pasiekiama** pasirinktos parametrui **Atsargų lygio pagrindas**. Galimos vertės yra **Visos**, **Mažai ir nebėra** ir **Nebėra**.

    - Pasirinkus **Visos** bus rodomi pranešimai apie visus atsargų diapazonus nuo „yra atsargų“ (pranešimas „Yra“) iki „nebėra atsargų“ (pranešimas „nebėra atsargų“).
    - Pasirinkus **Mažai ir nebėra** bus rodomi pranešimai apie visus atsargų diapazonus, išskyrus „yra atsargų“ (pranešimas „Yra“).
    - Pasirinkus **Nėra atsargų**, bus rodomas tik pranešimas „Nėra atsargų“.

- **Pasibaigusių atsargų slenkstis** – Šis senas skaitinis parametras įsigalios tik tada, jei reikšmė **Pasibaigusių atsargų slenkstis** pasirenkama parametrui **Atsargų lygio pagrindas**.

> [!IMPORTANT] 
> Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime. Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json. Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-inventory-settings"></a>Moduliai, kurie naudoja atsargų parametrus

Pirkimo langelis, pageidavimų sąrašas, parduotuvės parinkiklis, krepšelis ir krepšelio piktogramos moduliai naudoja atsargų parametrus, kad būtų rodomi atsargų diapazonai ir pranešimai.

Šiame pavyzdyje PDP rodo atsargų („Turima") pranešimą.

![PDP modulio su atsargų pranešimu, pavyzdys.](./media/pdp-InStock.png)

Šiame pavyzdyje PDP rodo atsargų („Pasibaigė") pranešimą.

![PDP modulio su pasibaigusių atsargų pranešimu, pavyzdys.](./media/pdp-outofstock.png)

Šiame pavyzdyje vežimėlis rodo atsargų („Turima") pranešimą.

![Krepšelio modulio su atsargų pranešimu, pavyzdys.](./media/cart-instock.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Sąskaitos valdymo puslapiai ir moduliai](account-management.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
