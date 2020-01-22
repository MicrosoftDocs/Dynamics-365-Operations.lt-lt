---
title: Darbas su moduliais
description: Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914799"
---
# <a name="work-with-modules"></a>Darbas su moduliais

Šioje temoje aprašoma, kaip ir kada naudoti modulius programoje „Microsoft Dynamics 365 Commerce“.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Moduliai yra loginiai kūrimo blokai, kurie sudaro puslapio struktūrą, o jų paskirtis ir taikymo sritys yra įvairios. Kai kurie moduliai yra aukšto lygio konteineriai, o jų vienintelė paskirtis – laikyti ir organizuoti kitus modulius (antrinius modulius). Kitų modulių, pvz., paprasto vaizdų išdėstymo modulio, paskirtis yra labai konkreti. Kiti moduliai, pvz., karuselės modulis, patenka tarp šių dviejų kategorijų.

Pagal numatytuosius nustatymus jūsų „Dynamics 365 Commerce“ svetainėje yra darbo pradžios rinkinio modulių biblioteka, kuri leidžia įgyvendinti pagrindinius el. prekybos scenarijus. Tiesiog naudodami šiuos modulius greičiausiai galėsite sukurti visapusišką el. prekybos svetainę. Tačiau galbūt norėsite šiuos modulius tinkinti arba kurti naujus pasirinktinius modulius konkretiems poreikiams. Jei norite kurti pasirinktinius modulius, galite naudoti modulių kūrimo programinės įrangos kūrimo rinkinį (SDK), kuris padės sukurti pasirinktinių modulių biblioteką.

## <a name="container-modules-and-slots"></a>Konteinerio moduliai ir vietos

Kaip minėta anksčiau, kai kurie moduliai yra skirti laikyti antrinius modulius. Šie moduliai vadinami *konteineriais* ir leidžia naudoti įdėtųjų modulių hierarchijas. Konteinerio moduliai apima *vietas*. Vietos naudojamos antrinių modulių maketui ir paskirčiai konteineryje tvarkyti. Pavyzdys – pagrindinis puslapio konteinerio modulis (bet kurio puslapio aukščiausio lygio modulis), kuriame nustatytos kelios svarbios vietos.

- Antraštės vieta
- Pagrindinės dalies vieta
- Poraštės vieta

Modulio kūrėjas apibrėžia šias vietas ir nustato, kuriuos antrinius modulius ir kiek antrinių modulių galima tiesiogiai įdėti jų viduje. Pavyzdžiui, antraštės vieta gali palaikyti tik vieną tipo **Antraštės modulis** modulį, o pagrindinės dalies vieta gali palaikyti neribotą skaičių bet kokio tipo modulių (išskyrus kitus puslapio konteinerio modulius).

Naudodami kūrimo įrankius puslapių autoriai neprivalo iš anksto žinoti, kuriuos modulius galima įdėti į kiekvieną vietą arba kurių modulių įdėti negalima. Kai puslapių autoriai pasirenka vietą ir bando pasirinkti modulį, kurį nori į šią vietą įtraukti, jie matys modulio tipų, kurie toje vietoje palaikomi, filtruotą rodinį.

## <a name="content-modules"></a>Turinio moduliai

Turinio moduliuose yra turinio ir medijos elementų, pvz., teksto (pvz., antraščių, pastraipų ir saitų) arba turto nuorodų (pavyzdžiui, vaizdų, vaizdo įrašų ir PDF failų). Įprastų turinio modulių tipų pavyzdžiai – **Pagrindinė reklaminė juosta**, **Ypatybė** ir **Reklaminė juosta**. Šių trijų tipų moduliuose gali būti teksto arba medijos, ir jiems nereikia jokių antrinių modulių, kad kokią nors informaciją būtų galima padaryti matoma puslapyje.

Dauguma įprastų, kasdienių puslapių ir turinio kūrimo užduočių apima turinio modulius, visų pirma todėl, kad šie moduliai apibrėžia faktinį turinį, kuris generuojamas jų pirminio konteinerio moduliuose. Yra daug turinio modulių ir jie paprastai yra paskutinės dalys, kurias įtrauksite į puslapio įdėtųjų modulių hierarchiją.

Toliau pateiktoje iliustracijoje parodyta, kaip moduliai yra įdėti į pirminio konteinerio modulio vietas.

![Modulių įdėjimas](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modulių įtraukimas arba pašalinimas

Tolesnėse procedūrose aprašoma, kaip įtraukti modulių arba juos pašalinti

### <a name="add-a-module"></a>Modulio įtraukimas

Norėdami modulį įtraukti į vietą arba konteinerį puslapyje, atlikite šiuos veiksmus.

1. Struktūros srityje kairėje pasirinkite konteinerį arba vietą, į kuriuos galima įtraukti antrinį modulį.

    > [!NOTE]
    > Modulių dizaino įrankyje nustatytas modulių, kuriuos galima įtraukti į konkrečią modulio vietą, tipų sąrašas. Tada šablonų autoriai gali patikslinti leidžiamų modulių parinktis, kad būtų užtikrintas visų puslapių, kurie kuriami naudojant konkretų šabloną, nuoseklus ieškos modulio optimizavimas (SEO) ir kūrimo efektyvumas.

1. Pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Įtraukti modulį**. Rodomas dialogo langas **Įtraukti modulį**. Šis dialogo langas automatiškai filtruojamas taip, kad jame būtų rodomi tik tie moduliai, kurie palaikomi pasirinktame konteineryje arba vietoje. Modulių sąrašas nustatomas pagal puslapio šabloną arba konteinerio modulio aprašą.

    > [!NOTE]
    > Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti modulį** nepasiekiama.

1. Dialogo lange raskite ir pasirinkite modulį, kurį norite įtraukti į puslapį.

    > [!TIP]
    > **Ypatybės** ir **Pagrindinės reklaminės juostos** modulių tipai yra tinkami pradedantiesiems.

1. Pasirinkite **Gerai**, kad pasirinktą modulį įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.

### <a name="remove-a-module"></a>Modulio šalinimas

Norėdami modulį pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.

1. Struktūros srityje kairėje šalia modulio, kurį norite pašalinti, pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite šiukšliadėžės mygtuką.
1. Kai būsite paraginti patvirtinti, kad norite pašalinti modulį, pasirinkite **Gerai**.

## <a name="configure-modules"></a>Modulių konfigūravimas

Tolesnėse procedūrose aprašoma, kaip konfigūruoti turinio ir konteinerio modulius.

### <a name="configure-a-content-module"></a>Turinio modulio konfigūravimas

Norėdami konfigūruoti turinio modulį puslapyje, atlikite šiuos veiksmus.

1. Kairėje pusėje esančioje struktūros srityje pasirinkite turinio modulio tipą (pvz, **Ypatybė**, **Pagrindinė reklaminė juosta** arba **Reklaminė juosta**).
1. Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.
1. Jei ypatybių srityje yra skyrius **Duomenų konfigūracija**, jį spustelėkite, kad išplėstumėte. Priešingu atveju pereikite į 5 veiksmą.
1. Jei rodomas mygtukas **Įtraukti duomenų šaltinį**, jį spustelėkite ir pasirinkite turinio elementus, kuriuos norite įtraukti.
1. Įveskite visų būtinų arba pageidaujamų modulio valdiklių parametrus.
1. Pasirinkite **Įrašyti**.

### <a name="configure-a-container-module"></a>Konteinerio modulio konfigūravimas

Norėdami konfigūruoti konteinerio modulį puslapyje, atlikite šiuos veiksmus.

1. Savo puslapyje pasirinkite konteinerio modulį (pavyzdžiui, karuselės arba nepastovaus konteinerio modulį).
1. Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.
1. Struktūros srityje kairėje šalia konteinerio arba bet kokių konteineryje esančių vietų pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį**. Tada į pasirinktą konteinerį įtraukite antrinių modulių. Norėdami gauti daugiau informacijos, žr. pirmiau šioje temoje aprašytą procedūrą [Modulio įtraukimas](#add-a-module).
1. Jei pirminiame konteineryje yra keli tos pačios kilmės antriniai moduliai, galite pakeisti jų rodymo pirminiame konteineryje tvarką. Pasirinkite modulio daugtaškio mygtuką, tada naudokite rodyklės aukštyn arba rodyklės žemyn mygtukus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su fragmentais](work-with-fragments.md)

[Konteinerio modulio įtraukimas į puslapį](add-container-module.md)

[Turinio išdėstymo modulių įtraukimas į puslapį](add-content-placement-modules.md)

[Darbas su publikavimo grupėmis](publish-groups.md)

