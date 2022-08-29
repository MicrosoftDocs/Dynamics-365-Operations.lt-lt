---
title: Sutikimo dėl slapukų modulis
description: Šiame straipsnyje aprašomi sutikimo sutikimai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8ca4cc1ffcf8229589591dce6e4666b78bba3890
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276273"
---
# <a name="cookie-consent-module"></a>Sutikimo dėl slapukų modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi sutikimo sutikimai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Sutikimo dėl slapukų modulis paragina svetainės vartotojus leisti naudoti slapukus bet kurioje funkcijoje ar modulyje, kurie naudoja naršyklės slapukus. Sutikimas reikalingas pirmą kartą, kai svetainės vartotojas naršo svetainę naujo naršyklės seanso metu. Gavus sutikimą pradedama sekti, o svetainės vartotojo daugiau nebus prašoma pateikti sutikimo. Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .

Jei svetainės vartotojo sutikimo naudoti slapukus negaunama, bet kokios funkcijos ir moduliai, naudojantys sutikimą dėl slapukų, puslapyje nebus atvaizduoti. Pavyzdžiui, pirkimo užbaigimo modulis, „Social Share” modulis ir pirmenybinės parduotuvės funkcija reikalauja sutikimo naudoti slapukus ir nebus atvaizduoti, jei svetainės vartotojo sutikimas nebus gaunamas. 

Sutikimo dėl slapukų modulį galima konfigūruoti puslapio antraštės fragmente, kad jį būtų galima taikyti įkeliant puslapį. Sutikimo dėl slapukų modulyje turi būti aiškus pranešimas, informuojantis svetainės vartotoją apie slapukų naudojimą svetainėje ir pateikiantis saitą su svetainės privatumo puslapiu.

Toliau pateiktoje iliustracijoje pabrėžiamas sutikimo dėl slapukų pranešimo, kuriame yra saitas su svetainės privatumo strategijos puslapiu, rodomu svetainės puslapio antraštėje, pavyzdys.
![Sutikimo dėl slapukų modulio pavyzdys.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Sutikimo dėl slapukų modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | Aprašas |
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
