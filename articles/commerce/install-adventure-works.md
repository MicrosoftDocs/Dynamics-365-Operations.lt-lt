---
title: „Adventure Works“ temos diegimas
description: Šiame straipsnyje aprašoma, kaip įdiegti Adventure Works temą Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274292"
---
# <a name="install-the-adventure-works-theme"></a>„Adventure Works“ temos diegimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įdiegti Adventure Works temą Microsoft Dynamics 365 Commerce. 

> [!IMPORTANT]
> „Adventure Works” tema ir moduliai galimi 10.0.20 „Dynamics 365 Commerce” versijos leidime. Jie yra galimi iš „Microsoft AppSource”.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš įdiegdami „Adventure Works” temą, privalote turėti „Dynamics 365 Commerce” aplinką (10.0.20 arba naujesnė „Commerce” versija), kuri apima „Retail Cloud Scale Unit” (RCSU), „Commerce” programinės įrangos kūrimo rinkinį internetu (SDK) ir „Commerce” modulių biblioteką. Informacijos, kaip įdiegti "Commerce SDK" ir modulių biblioteką, žr [. Nustatyti programavimo aplinką](e-commerce-extensibility/setup-dev-environment.md). 

## <a name="installation-steps"></a>Įdiegimo veiksmai

### <a name="install-the-adventure-works-theme-in-your-application"></a>Įdiekite „Adventure Works” temą savo programoje

„Adventure Works” temos paketas yra galimas **„dynamics365-commerce”** sklaidos kanale kaip **„@msdyn365-commerce-theme/adventureworks-theme-kit”**. Tačiau, nors „Adventure Works” temos paketas yra šios sklaidos kanalo dalis, jo vardų sritis yra skirtinga. Todėl norėdami pridėti vardų srities registro įrašus, turite atlikti šiuos veiksmus.

1. Atnaujinkite **„.npmrc”** failą, kad jame būtų šis registro įrašas (jei įrašas dar nėra įtrauktas):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. Atnaujinkite **„.yarnrc”** failą, kad jame būtų šis registro įrašas (jei įrašas dar nėra įtrauktas):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
Norėdami įdiegti paketą vietinėje aplinkoje, `yarn add THEME_PACKAGE@VERSION` vykdykite komandą iš komandinės eilutės, **kur THEME_PACKAGE** yra temos paketas (@msdyn365-commerce-theme/adventureworks-theme-kit), **o VERSIJA** yra naudojamos modulių bibliotekos versijos numeris. Svarbu, kad temos paketo ir modulių bibliotekos versijos atitiktų. Norėdami rasti tinkamą naudoti modulio bibliotekos versijos numerį, atidarykite failą package.json **ir skyriuje Priklausomybės raskite paleidimo** **paketo** vertę. Toliau pateiktame pavyzdyje failas package.json naudoja modulių bibliotekos 9.32 Dynamics 365 Commerce versiją, kuri susieja su 10.0.22 versija.  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

Toliau pavyzdyje parodyta, kaip vykdyti komandą `yarn add`, norint įtraukti Adventure Works temos 9.32 versiją. Komanda automatiškai atnaujina paketo.json failą, kad jis būtų priklausomas nuo priklausomybę.

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

Norėdami gauti daugiau informacijos apie modulių bibliotekos versijos atnaujinimą, žr. [SDK ir modulių bibliotekos naujinimus](e-commerce-extensibility/sdk-updates.md). 

> [!IMPORTANT]
> - Temos versija turi atitikti modulių bibliotekos versiją, kad užtikrintumėte tokį funkcijų veikimą, kokio tikimasi. 
> - Mažiausia „Commerce” modulių bibliotekos ir SDK versija turėtų būti 10.0.20 (9.31). 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Įtraukite šriftų failus „Adventure Works” temai

Įdiegus „Adventure Works” temą savo programoje, turite pridėti jai reikalingus šrifto failus. Norėdami atlikti šį veiksmą, nukopijuokite visus šrifto failus iš **„\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts”** į partnerio programos viešo katalogo kelią **„\public\webfonts”**.

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Nustatykite išteklius „Adventure Works” temai

Kitas veiksmas yra atnaujinti reikalingus numatytuosius temos išteklius. Norėdami atlikti šį veiksmą, nukopijuokite turinį iš global.json failo po **„\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules”** į partnerio programos global.json failą po **„\src\resources\modules”**. Jei nėra **„\src\resources”** paskirties katalogo, jį visą galima nukopijuoti iš **„\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks”** šaltinio katalogo į **„\src”** paskirties katalogą.

### <a name="pull-updates-and-validate-the-theme"></a>Gaukite naujinimus ir patikrinkite temą

Informacijos apie tai, kaip gauti naujausią SDK, modulių biblioteką ir kitus priklausomumo naujinimus, rasite [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#pull-updates) skyriuje „Gauti naujinimus”.

Gavę naujausias priklausomybes, galite vykdyti **paleidimo** komandą, kad pradėtumėte mazgo serverį savo programavimo aplinkoje ir išbandytumėte naują „Adventure Works” temą. Naršykite programą vietoje naudodami užklausos eilutės parametrą `?theme=adventureworks` (pavyzdžiui, `https://localhost:4000/?theme=adventureworks`).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Adventure works” tema](adventure-works-theme.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
