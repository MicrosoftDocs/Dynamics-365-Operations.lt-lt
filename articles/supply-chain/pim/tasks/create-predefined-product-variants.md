---
title: Iš anksto apibrėžtų produkto variantų kūrimas
description: Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270485"
---
# <a name="predefined-product-variants"></a>Iš anksto apibrėžti produkto variantai

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Scenarijaus pavyzdys: Iš anksto apibrėžtų produkto variantų kūrimas

Šia procedūra apžvelgiamas bendrojo produkto variantų kūrimas naudojant produkto dimensijų kombinacijas.

### <a name="make-demo-data-available"></a>Demonstracinių duomenų įgalinimas

Šio scenarijaus įgyvendinimui naudojant siūlomas vertes, privalote turėti įdiegtus demo duomenis ir pasirinkti *USMF* juridinį asmenį.

### <a name="step-1-create-a-product-master"></a>1 žingsnis: Bendrojo produkto kūrimas

Norėdami kurti bendrąjį produktą:

1. Eikite į **Produkto informacijos valdymas > Produktai > Bendrieji produktai**.
1. Pasirinkite **Naujas**.
1. Jei **lauke** Produkto numeris dar nerodyti numerio, įveskite vertę. Šį veiksmą atlikti reikia tik jei nenustatyta produktų numeracija šiame lauke.
1. Laukelyje **Produkto pavadinimas** įveskite produkto pavadinimą.
1. Produkto **dimensijų grupės** lauke pasirinkite produkto dimensijų grupę *SizeCol* (Dydis ir spalva).
1. Norėdami **sukurti ir atidaryti naują bendrąjį** produktą, pasirinkite Gerai.

### <a name="step-2-add-product-dimensions"></a>2 žingsnis: Produkto dimensijų įtraukimas

Šiame pavyzdyje parodyta, kaip rankiniu būdu įvesti produkto dimensijų. Taip pat galite pasirinkti dydžių, spalvų ar stilių grupę, kurioje yra jūsų norimos naudoti produkto dimensijų reikšmės.

Norėdami įtraukti produkto dimensijas:

1. Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** dimensijos.
1. Atidarykite **skirtuką Dydis ir** įrankių **juostoje** pasirinkite Naujas, kad įtraukumėte eilutę į tinklelį. Naujoje eilutėje nustatykite šiuos parametrus:
    - **Dydis:** Pasirinkti dydžio vertę.
    - **Pavadinimas** Įveskite pavadinimą dydžiui.
1. Įrankių **juostoje** pasirinkite Naujas ir į tinklelį įtraukite antrą dydį, naudodami naują **dydį** ir **pavadinimą**.
1. Atidarykite **Spalvos** įrankių **juostoje** pasirinkite Naujas, kad įtraukumėte eilutę į tinklelį. Naujoje eilutėje nustatykite šiuos parametrus:
    - **Spalva:** pasirinkite spalvos vertę.
    - **Pavadinimas** Įveskite pavadinimą spalvai.
1. Įrankių **juostoje** pasirinkite Naujas ir į tinklelį įtraukite antrą dydį, naudodami naują **Spalva** ir **pavadinimą**.
1. Pasirinkite **Įrašyti**.
1. Norėdami grįžti į savo naują bendrąjį produktą, uždarykite puslapį.

### <a name="step-3-generate-product-variants"></a>3 žingsnis: Produkto variantų generavimas

> [!NOTE]
> Šiame skyriuje aprašoma, kaip generuoti produktų variantus, *kai neįgalinta* variantų pasiūlymų puslapio patobulinimų funkcija. Informacijos apie tai, kaip generuoti produkto variantus, kai ši funkcija yra pasiekiama, rasite kitame skyriuje.

Norėdami kurti produkto variantus:

1. Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** variantus.
1. Rinkitės **Varianto siūlymus** veiksmų juostoje.
1. Sistema sugeneruoja sąrašą su visomis galimais dydžių ir spalvų deriniais, kuriuos nustatote produktui. Pasirinkite **Žymėti viską įrankių** juostoje.
    - Šiame pavyzdyje pasirinkite visus galimus variantus. Jei norite naudoti tik galimų produkto dimensijų derinių subrinkinį, pasirinkite tik reikiamus žymės langelius.  
1. Pasirinkite **Kurti**.
1. Pasirinkite **Įrašyti**.

## <a name="improved-variant-suggestions"></a>Patobulinti variantų pasiūlymai

Variantų pasiūlymų puslapio patobulinimų funkcija pagerina variantų pasiūlymų puslapį, kad adresuoti našumo ir tinkamumo naudoti problemas įmonėse, kurios turi daug *produkto* dimensijų **derinių**. Patobulintas produkto dimensijų reikšmių pasirinkimo procesas, kurio variantų pasiūlymus būtų galima atlikti greičiau ir paprasčiau identifikuoti bei pateikti atitinkamą produkto variantų rinkinį.

Šią priemonę pridėjo šie patobulinimai:

- **Atidėtas variantų pasiūlymų generavimas: variantų pasiūlymų puslapyje, kai pirmą kartą** jį **atidarote**, nebėra pasiūlymų. Todėl turite tiesiogiai pasirinkti, kurių verčių jums reikia, tada pasirinkti **mygtuką** Siūlyti, kad būtų generuojamos kombinacijos. Taip procesas bus matomas ir interaktyviau.
- **Dimensijų verčių pasirinkimas: kai turite daug dimensijų verčių, paprastai jus domina generuoti variantų pasiūlymus, kuriuose yra tik keletas iš jų (pvz., pristatant naują spalvų arba stilių** rinkinį). Naudodami patobulintą dizainą, galite pasirinkti dimensijų vertes, kurioms norite generuoti produkto variantų pasiūlymus. Tai labai padidina siūlomų variantų tinkamumą ir pagerina sistemos našumą ir vartotojo produktyvumą.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Variantų pasiūlymų puslapio patobulinimų funkcijos įjungimas

Norėdami naudoti *Varianto siūlymo puslapio gerinimų* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Produkto informacijos valdymas*
- **Funkcijos pavadinimas:** *Variantų pasiūlymų puslapio patobulinimai*

### <a name="work-with-the-improved-variant-suggestions"></a>Dirbti su patobulintais variantų pasiūlymais

Norėdami kurti produkto varianto siūlymus, *kai neįgalinta* variantų pasiūlymų puslapio patobulinimų funkcija:

1. Atidaryti arba sukurti bendrąjį produktą ir įtraukti į jį reikiamas produkto dimensijas, kaip aprašyta ankstesniame skyriuje.
1. Kai naujas bendrasis produktas vis dar atidarytas, **veiksmų srityje pasirinkite Produkto** variantus.
1. Rinkitės **Varianto siūlymus** veiksmų juostoje.
1. Pasirinkite vertes, kurias norite naudoti visose dimensijose.
1. Viršutinėje įrankių juostoje pasirinkite **Siūlyti**.
1. Sistema sugeneruoja sąrašą su visomis galimais dydžių ir spalvų deriniais, kuriuos pasirenkate produktui. Siūlomų variantų „FastTab" pažymėkite kiekvieno norimo naudoti produkto dimensijų derinio žymės langelį arba įrankių juostoje pasirinkite Žymėti viską, kad juos **visas** **pasirinktumėte**.  
1. Pasirinkite **Kurti**, jei norite įtraukti variantus į dabartinį bendrąjį produktą.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
