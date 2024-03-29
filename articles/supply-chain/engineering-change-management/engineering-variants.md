---
title: Generuoti inžinerijos produktų variantus
description: Šiame straipsnyje aprašoma, kaip generuoti inžinerijos produktų variantus
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 08feb66dedfa79f5a21a7723a22f3bef883431e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870759"
---
# <a name="generate-variants-for-engineering-products"></a>Generuoti inžinerijos produktų variantus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip generuoti inžinerijos produktų variantus.

## <a name="turn-variant-generation-for-engineering-products-on-or-off"></a>Įjungti arba išjungti inžinerijos produktų varianto generavimą

Šiame straipsnyje aprašyta funkcija reikalauja, kad jūsų sistemai būtų *įjungtas* *ir* inžinerijos produktų funkcijų inžinerijos pakeitimų valdymas, ir variantų generavimas. Išsamesnės informacijos apie šių funkcijų įjungimą ir išjungimą žr. Inžinerinių [pakeitimų valdymo peržiūra](product-engineering-overview.md).

## <a name="generate-one-or-more-new-variants-of-an-engineering-product"></a>Generuoti vieną ar daugiau naujų inžinerijos produkto variantų

Galite sukurti vieną ar daugiau naujų produkto variantų nekopijuojant informacijos iš esamo produkto. Tai naudinga, kai vienu metu reikia sukurti kelis produkto variantus.

Toliau pateiktoje procedūroje pateikiamas pavyzdys, kaip sukurti kelis variantus, kuriuose yra spalvos dimensija.

1. Atidarykite **Išleistų produktų** puslapį (pvz., eikite į **Pakeitimų valdymo inžinerija \> Įprasti \> Išleisti produktai**).
1. Veiksmų juostoje skirtuke atidarykite **Produktas** skirtuką ir iš **Naujas** grupės pasirinkite **Inžinerijos produktas**.
1. Atidaromas **Naujas produktas** dialogo langas. Pasirinkite atitinkamą **Inžinerijos kategoriją**.
1. Jei į pasirinktą inžinerijos kategoriją įtrauktos variantų dimensijos, tuomet galite nustatyti jų vertes. Pavyzdžiui, jei kategorija turi **Spalvos** dimensiją, galite nustatyti ją į *Mėlyną*.
1. Atlikite kitus reikalingus parametrus. Pasirinkite **OK**, kad sukurtumėte produktą.
1. Sukūriamas produkto ir mėlynas V-1 variantas, ir atsidaro naujas produktas.
1. Jei reikia, į variantą įtraukite komplektavimo specifikaciją (KS) ir maršrutą.
1. Veiksmų juostoje, atidarykite **Produkto** skirtuką ir **Produkto šeimininkas** grupėje, pasirinkite **Produkto matmenys**.
1. Atidaromas **Produkto dimensijos** puslapis. Šiame puslapyje yra kiekvienos galimos dimensijos skirtukas. Kiekviename skirtuke pridėkite kiekvienos vertės, kurią palaikote kiekvienai susijusiai dimensijai, eilutę. (Šiame pavyzdyje galite įtraukti eilutes į **Spalva** skirtuką, tokias kaip *Balta*, *Geltona* ir *Žalia*).
1. Uždarykite puslapį ir tada pasirinkite **Išleisto produkto variantai**. Atkreipkite dėmesį, kad atsiranda pirmas jūsų sukurtas variantas (mėlynas V-1).
1. Veiksmų srities skirtuke **Produkto variantas** pasirinkite **Variantų siūlymai**.
1. Variantų **pasiūlymų dialogo** lange atlikite vieną iš šių veiksmų:

    - Dialogo lango viršuje yra kiekvienos galimos dimensijos skyrius. Kiekvienai dimensijai pažymėkite kiekvienos vertės, kurios varianto pasiūlymą norite generuoti, žymės langelį, tada įrankių juostoje **pasirinkite** Siūlyti. Susiję pasiūlymai įtraukiami į skyrių **Siūlomi variantai**.
    - Pasirinkite **Siūlyti viską įrankių** juostoje, norėdami generuoti visų galimų dimensijų verčių derinių variantų pasiūlymus. Susiję pasiūlymai įtraukiami į skyrių **Siūlomi variantai**.

1. Skyriuje **Siūlomi variantai** pažymėkite kiekvieno norimo sukurti varianto žymės langelį. Pasirinkite pasiūlytus variantus ir pasirinkite **Kurti**, norėdami generuoti variantus į inžinerijos įmonę. Šios sąlygos taikomos:

    - Jokie sukurti variantai neturės KS arba maršruto.
    - Šių variantų atributai bus numatytieji gamybos kategorijos atributai ir nebus nukopijuoti iš ankstesnio varianto.

## <a name="generate-a-variant-as-a-copy-of-another-product-variant"></a>Generuokite variantą kaip kito produkto varianto kopiją

Produkto variantą galite sukurti pagal kitą produkto variantą. Komplektavimo specifikacija (KS) ir maršrutas iš šaltinio produkto varianto nukopijuojami į naują variantą. Tai gali būti naudinga retesnėms gamybos produktams, kai gali būti naudinga sukurti KS, remiantis pirmine KS, ir sekti ankstesnio varianto pakeitimus. Norint išlaikyti sekamumą, sistemos įrašai, į kuriuos buvo nukopijuotas variantas, sukuria naują kopiją.

Toliau pateiktoje procedūroje pateikiamas pavyzdys, kaip sukurti naują variantą, į kurį įtrauktos spalvos dimensijos, sukuriant esamo varianto kopiją

1. Atidarykite **Išleistų produktų** puslapį (pvz., eikite į **Pakeitimų valdymo inžinerija \> Įprasti \> Išleisti produktai**).
1. Veiksmų juostoje skirtuke atidarykite **Produktas** skirtuką ir iš **Naujas** grupės pasirinkite **Inžinerijos produktas**.
1. Atidaromas **Naujas produktas** dialogo langas. Pasirinkite atitinkamą **Inžinerijos kategoriją**.
1. Jei į pasirinktą inžinerijos kategoriją įtrauktos variantų dimensijos, tuomet galite nustatyti jų vertes. Pavyzdžiui, jei kategorija turi **Spalvos** dimensiją, galite nustatyti ją į *Mėlyną*.)
1. Atlikite kitus reikalingus parametrus. Pasirinkite **OK**, kad sukurtumėte produktą.
1. Sukūriamas produkto ir mėlynas V-1 variantas, ir atsidaro naujas produktas.
1. Jei reikia, į variantą įtraukite komplektavimo specifikaciją (KS) ir maršrutą.
1. Jei reikia, prie produkto varianto pridėkite požymius.
1. Pridėkite mėlyną V-1 variantą prie inžinerijos keitimo užsakymo.
1. Nustatykite **Poveikį** *Naujam variantui*.
1. Pasirinkite naują spalvos vertę (pvz., *Balta*). Atkreipkite dėmesį, kad bus taikomos toliau nurodytos sąlygos: 
    - Naujas variantas turi KS ir maršrutą, kuris buvo nukopijuotas iš ankstesnio varianto.
    - Naujas variantas turi požymius, nukopijuotus iš ankstesnio varianto.
1. Patvirtinkite keičiamą užsakymą.
1. Apdorokite keičiamą užsakymą. Apdorojus užsakymą, naujasis V-1 variantas bus sukurtas ir išleistas inžinerijos įmonei.
