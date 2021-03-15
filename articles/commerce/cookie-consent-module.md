---
title: Sutikimo dėl slapukų modulis
description: Šioje temoje aprašomi sutikimo naudoti slapukus moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993530"
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

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md) 

[Slapukų atitiktis](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]