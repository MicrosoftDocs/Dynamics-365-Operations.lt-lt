---
title: Generuoti inžinerijos produktų variantus
description: Šioje temoje aprašoma, kaip generuoti inžinerijos produktų variantus
author: t-benebo
ms.date: 06/08/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 57eda6a833df6ff8e91c006bbc5096554eff6c503a8b7ba2bd0b13e2f8e98f56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766159"
---
# <a name="generate-variants-for-engineering-products"></a>Generuoti inžinerijos produktų variantus

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip generuoti inžinerijos produktų variantus.

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
1. Uždarykite puslapį ir pasirinkite **Išleisto produkto variantai**. Atsikreipkite dėmesį, kad atsiranda pirmas sukurtas variantas (baltas V-1).
1. Pasirinkite **Variantų pasiūlymai**.
1. Sistema siūlo variantus su sukurtomis spalvų vertėmis (pvz., balta V-1, geltona V-1 ir žalia V-1).
1. Pasirinkite pasiūlytus variantus ir pasirinkite **OK**, norėdami paleisti variantus į inžinerijos įmonę. Atkreipkite dėmesį, kad bus taikomos toliau nurodytos sąlygos: 
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
