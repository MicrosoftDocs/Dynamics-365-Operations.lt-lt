---
title: Sutikimo dėl slapukų modulis
description: Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761411"
---
# <a name="cookie-consent-module"></a>Sutikimo dėl slapukų modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūra

Sutikimo dėl slapukų modulis paragina svetainės vartotojus leisti naudoti slapukus bet kurioje funkcijoje ar modulyje, kurie naudoja naršyklės slapukus. Sutikimas reikalingas pirmą kartą, kai svetainės vartotojas naršo svetainę naujo naršyklės seanso metu. Gavus sutikimą pradedama sekti, o svetainės vartotojo daugiau nebus prašoma pateikti sutikimo. Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .

Jei svetainės vartotojo sutikimo naudoti slapukus negaunama, bet kokios funkcijos ir moduliai, naudojantys sutikimą dėl slapukų, puslapyje nebus atvaizduoti. Pavyzdžiui, pirkimo užbaigimo modulis, „Social Share” modulis ir pirmenybinės parduotuvės funkcija reikalauja sutikimo naudoti slapukus ir nebus atvaizduoti, jei svetainės vartotojo sutikimas nebus gaunamas. 

Sutikimo dėl slapukų modulį galima konfigūruoti puslapio antraštės fragmente, kad jį būtų galima taikyti įkeliant puslapį. Sutikimo dėl slapukų modulyje turi būti aiškus pranešimas, informuojantis svetainės vartotoją apie slapukų naudojimą svetainėje ir pateikiantis saitą su svetainės privatumo puslapiu.

Toliau pateiktoje iliustracijoje pabrėžiamas sutikimo dėl slapukų pranešimo, kuriame yra saitas su svetainės privatumo strategijos puslapiu, rodomu svetainės puslapio antraštėje, pavyzdys.
![Sutikimo dėl slapukų modulio pavyzdys](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Sutikimo dėl slapukų modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Raiškusis tekstas                  | Raiškusis tekstas | Nurodo raiškiojo teksto pranešimą svetainės vartotojams, kad svetainė naudoja naršyklės slapukus ir kad vartotojai turėtų sutikti su slapukų naudojimu, norėdami, jog svetainė būtų visiškai funkcionali. |
| Saitai | URL | Vienas ar daugiau saitų gali būti įtraukti į svetainės privatumo puslapį, aprašantį svetainėje naudojamų slapukų tipą. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Sutikimo dėl slapukų modulio įtraukimas į svetainės puslapius

Norint įtraukti sutikimo dėl slapukų modulį į kelis svetainės puslapius, jį galima įtraukti į bendrai naudojamą puslapio antraštės fragmentą. Po to, kai antraštės fragmentas bus įtrauktas į visus svetainės puslapius, sutikimo dėl slapukų pranešimas bus automatiškai vaizduojamas pirmą kartą, kai svetainės vartotojas pereis į bet kurį svetainės puslapį.

Daugiau informacijos apie antraščių fragmentus ir modulius žr. [Antraštės modulis](author-header-module.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md) 

[Slapukų atitiktis](cookie-compliance.md)
