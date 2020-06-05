---
title: Parduotuvės parinkiklio modulis
description: Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378213"
---
# <a name="store-selector-module"></a>Parduotuvės parinkiklio modulis

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Parduotuvės parinkiklio modulis naudojamas „pirkti internetu, atsiimti parduotuvėje“ (angl. BOPIS) kliento scenarijui. Čia pateikiamas parduotuvių, kuriose galima atsiimti produktą, sąrašas, kiekvienos parduotuvės darbo valandos ir prekių atsargos.

Parduotuvių parinkiklio moduliui reikalingas produkto konteksto ir paieškos vietos įgalinimas, kad jis galėtų rasti parduotuves. Jei paieškos vietos nėra, ji pagal numatytąsias nuostatas nustato kliento naršyklės vietą, jei klientas duoda tam sutikimą. Modulyje yra įvesties laukas, kurį naudodamas klientas gali įvesti vietą (pašto kodą, miestą, valstiją) ir ieškoti netoliese esančių parduotuvių.

Parduotuvės parinkiklio modulis yra integruotas su „Bing“ žemėlapių geokodavimo programos programavimo sąsaja (API), kad vieta būtų konvertuojama į platumą ir ilgumą. Reikalingas „Bing“ žemėlapių programos programavimo sąsajos (API) raktas, kuris turi būti pridėtas prie puslapio „Bendrieji „Commerce“ parametrai“, esančio „Dynamics 365 Commerce“.

Parduotuvės parinkiklio modulis gali būti pridėtas prie pirkimo langelio modulio, esančio išsamios produkto informacijos puslapyje (PDP), kad būtų galima parodyti parduotuves, kuriose galima atsiimti produktą. Jį taip pat galima pridėti prie krepšelio modulio. Kai parduotuvių parinkiklio modulis pridedamas prie krepšelio modulio, rodomos kiekvieno krepšelio eilutės elemento atsiėmimo parinktys. Be to, su pasirinktiniu kodavimu šį modulį galima pridėti prie kitų puslapių ar modulių plėtiniais ir tinkinimais.

Produktai turi būti sukonfigūruoti su „atsiims klientas“ pristatymo būdu, kad BOPIS scenarijus veiktų. Priešingu atveju modulis nebus rodomas atitinkamuose puslapiuose. Norėdami gauti daugiau informacijos apie tai, kaip sukonfigūruoti pristatymo būdą, žr. [Nustatyti pristatymo būdus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Toliau pateiktame paveikslėlyje vaizduojamas išsamios produkto informacijos puslapyje (PDP) naudojamo parduotuvių parinkiklio modulio pavyzdys.

![Parduotuvės parinkiklio modulio pavyzdys](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Parduotuvės parinkiklio modulio naudojimas „e-Commerce“

- Parduotuvės parinkiklio modulis gali būti naudojamas išsamios informacijos apie gaminį puslapyje (PDP), kad būtų galima ieškoti netoliese esančių parduotuvių, kuriose galima atsiimti produktą.
- Parduotuvės parinkiklio modulis gali būti naudojamas krepšelio puslapyje, kad būtų galima ieškoti netoliese esančių parduotuvių, kuriose galima atsiimti krepšelyje esantį produktą.

## <a name="store-selector-module-properties"></a>Parduotuvės parinkiklio modulio ypatybės

| Ypatybės pavadinimas             | Vertė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Ieškos spindulys | Skaičius | Apibrėžia parduotuvių ieškos spindulį myliomis. Jeigu vertė nenurodyta, naudojamas numatytasis 50 mylių ieškos spindulys.|
|Paslaugos teikimo sąlygos | URL    |  Paslaugų teikimo sąlygų URL, kuris reikalingas „Bing“ žemėlapių paslaugai. |

## <a name="add-a-store-selector-module-to-a-page"></a>Parduotuvės parinkiklio modulio pridėjimas prie puslapio

Parduotuvės parinkiklio moduliui reikalingas produkto kontekstas, todėl jį galima naudoti tik pirkimo langelio ir krepšelio moduliuose. Parduotuvės parinkiklio moduliai neveikia be šių modulių.

- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie pirkimo langelio modulio, žr. [Pirkimo langelio modulis](add-buy-box.md). 
- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie krepšelio modulio, žr. [Krepšelio modulis](add-cart-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Greitai susipažinkite su išsamios produkto informacijos puslapiu (PDP)](quick-tour-pdp.md)

[Greitai susipažinkite su „Krepšelis ir mokėjimas“](quick-tour-cart-checkout.md)

[Nustatyti pristatymo būdus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Jūsų organizacijos „Bing“ žemėlapių valdymas](dev-itpro/manage-bing-maps.md)
