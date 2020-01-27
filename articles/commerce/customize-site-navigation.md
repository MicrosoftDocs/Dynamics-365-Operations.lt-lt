---
title: Svetainės naršymo tinkinimas
description: Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 642cb5c145dec68631eb9ab27d926ba8ab75c59b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914915"
---
# <a name="customize-site-navigation"></a>Svetainės naršymo tinkinimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti tinkintą interneto naršymo hierarchiją, kad būtų galima tvarkyti savo „Microsoft Dynamics 365 Commerce“ svetainėje naršomas prekes.

## <a name="overview"></a>Peržiūrėti

Internetinėse vitrinose paprastai klientai gali atrasti ir naršyti produktus, naršydami per produktų kategorijas. Šią galimybę paprastai teikiama skirtukais puslapio viršuje arba naršymo juosta kairėje pusėje. „Dynamics 365 Commerce“ galite kurti ir valdyti savo hierarchinę, kategorijų naršymo ir į įvairias kategorijas įtrauktų produktų, struktūrą.

## <a name="create-a-retail-channel-navigation-hierarchy"></a>Mažmeninės prekybos kanalų naršymo hierarchijos kūrimas

Norėdami sukurti mažmeninės prekybos kanalų naršymo hierarchiją, atlikite šiuos veiksmus.

1. Eikite į **„Retail“ \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.
1. Pasirinkite **Kategorijų hierarchijos** ir pasirinkite **Nauja**.
1. Pavadinkite hierarchiją.

    > [!NOTE]
    > Jūsų kuriama pagrindinė kategorija yra šakninis kategorijos mazgas. Ji nebus rodoma jūsų svetainėje. Norėdami sukurti kategorijų hierarchiją, kurioje jūsų svetainėje rodomas vienas aukščiausio lygio mazgas, sukurkite ir pavadinkite kategoriją kaip šakninės kategorijos antrinį elementą.

1. Pasirinkite **Naujas kategorijos mazgas** ir pavadinkite kategoriją.
1. Toliau kurkite pirmines ir antrines kategorijas, kaip jums reikia.

Dabar galite priskirti produktus kiekvienai kategorijai, kurią sukūrėte pagal aukščiausio lygio kategoriją.

## <a name="customize-the-order-of-categories"></a>Kategorijų tvarkos tinkinimas

Pagal numatytuosius parametrus, jūsų nustatytos kategorijos svetainėje bus rodomos abėcėlės tvarka. Tačiau, taip pat galite tinkinti kategorijų rodymo tvarką.

## <a name="assign-a-category-hierarchy-type"></a>Kategorijų hierarchijos tipo priskyrimas

1. Eikite į **„Retail“ \> Produktai ir kategorijos \> Kategorijų ir produktų valdymas**.
1. Pasirinkite **Kategorijų hierarchijos**.
1. Veiksmų srities skirtuko **Kategorijų hierarchija** grupėje **Nustatyti** pasirinkite **Susieti hierarchijos tipą**.
1. Pasirinkite **Naujas**.
1. Lauke **Kategorijų hierarchijos tipas** pasirinkite **Mažmeninės prekybos kanalo naršymo hierarchija**.
1. Lauke **Kategorijų hierarchija** pasirinkite kanalo naršymo hierarchiją, kurią sukūrėte anksčiau.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Naujų ar atnaujintų naršymo hierarchijų publikavimas

Norėdami, kad jūsų naršymo hierarchija būtų pasiekiama jūsų internetinėje vitrinoje, atlikite šiuos veiksmus.

1. Eikite į **„Retail“ \> Kanalo sąranka \> Kanalo kategorijų ir produktų atributai**.
1. Kairėje esančiame medyje pasirinkite savo internetinę parduotuvę.
1. Pasirinkite **Publikuoti kanalo naujinimus**.
1. Eikite į **Mažmeninė prekyba \> Mažmeninės prekybos IT \> Paskirstymo grafikas**.
1. Sąraše raskite ir pasirinkite **Užduotis 1040**.
1. Pasirinkite **Vykdyti dabar**.
1. Pakartokite 5 ir 6 veiksmus, skirtus užduotims 1070 ir 1150.

## <a name="show-categories-on-your-site"></a>Kategorijų rodymas jūsų svetainėje

Norėdami savo kategorijų hierarchiją rodyti savo internetinėje vitrinoje, turite įtraukti naršymo meniu modulį į atitinkamas šablono ar fragmento vietas. Tada naršymo meniu modulis rodys naršymo hierarchiją, jei savo mažmeninės prekybos naršymo hierarchiją publikavote kanale, su kuriuo yra susieta jūsų svetainė.

> [!NOTE]
> Naršymo meniu modulis, įtrauktas į parduotuvės darbo pradžios rinkinį, leidžia vartotojams pereiti tik į kategorijas, kurios neturi subkategorijų. Jei jūsų klientai turėtų galėti pereiti į kategorijas, kurios turi subkategorijas, turite tinkinti naršymo meniu modulį.

## <a name="add-custom-navigation-options"></a>Pasirinktinių naršymo parinkčių įtraukimas

Naršymo meniu galite pridėti naršymo parinktis, kurios nepriklauso jūsų produktų kategorijų hierarchijai. Pavyzdžiui, produktų kategorijų sąrašo pabaigoje galite pridėti elementą **Susisiekite su mumis**, kuris nurodo kontaktinį puslapį, kurį sukūrėte savo svetainei.

Norėdami į naršymo meniu įtraukti pasirinktines naršymo parinktis, atlikite šiuos veiksmus.

1. Norimame tinkinti šablone ar fragmente pasirinkite naršymo meniu modulį.
1. Ypatybių srityje, skirtuke **Duomenys**, pasirinkite **Įtraukti elementą**, kad sukurtumėte naują turinio valdymo sistemos (TVS) naršymo elementą.
1. Įveskite saito tekstą ir URL.
1. 2 ir 3 veiksmus pakartokite, kad įtrauktumėte daugiau pasirinktinių naršymo parinkčių.
1. Kai baigsite, įrašykite šabloną ar fragmentą ir jį įrašykite ir atrakinkite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su fragmentais](work-with-fragments.md)

[Darbas su moduliais](work-with-modules.md)

[Kurti puslapio URL](create-page-url.md)

[Darbas su publikavimo grupėmis](publish-groups.md)
