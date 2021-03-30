---
title: Krovinio kūrimo darbo sritis
description: Ši tema aprašo, kaip dirbti su krovinio kūrimo darbo sritimi.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247243"
---
# <a name="load-building-workbench"></a>Krovinio kūrimo darbo sritis

Krovinio kūrimo darbo sritis leidžia jums taikyti krovinio kūrimo strategijas kuriant krovinius.

## <a name="create-a-load-building-strategy"></a>Sukurkite krovinio kūrimo strategiją

Naudojate krovinio kūrimo strategijas automatiniu būdu sukurti krovinius. Ši funkcija gali būti naudinga tolesnėse situacijose:

- Jei reguliariai sunčiate konkretų produktų rinkinį, krovinio strategijos padės sutaupyti laiko, nes jums nereikės sukurti to paties krovinio kas kartą.
- Jei norite išvengti pusiau pilnų krovinių siekiant maksimizuoti efektyvumą, krovinio strategijos gali padėti užpildyti kiekvieną krovinį kaip įmanoma labiau.

Krovinio kūrimo strategijos klasė pavadinimu `TMSLoadBuildingVolumeStrategy` suteikia krovinio kūrimo strategiją pavadinimu *Apimtimi pagrįsta krovinio kūrimo strategija*. Naudojant šią strategiją galima naudoti maksimalias aukščio ir svorio reikšmes, nurodytas krovinio šablone, arba galima nepaisyti parametrų įvedant naujas reikšmes. Ši strategija yra tik strategija įtraukta nestandartiniu būdu. (Nepaisant to, galite turėti tinkintas strategijas.)

Norėdami naudoti nestandartinę *Apimtimi grįsta krovinio kūrimo strategiją* strategiją pasirinkite **Krovinio kūrimo strategijos** laukelį **Krovinio kūrimo darbo srities** puslapyje (**Gabenimo valdymas &gt; Planavimas &gt; Krovinio kūrimo darbo strategija**).

Norėdami sukurti krovinio kūrimo strategiją, atlikite šiuos žingsnius.

1. Eikite į **Gabenimo valdymas &gt; Nustatymai &gt; Krovinio kūrimas &gt; Krovinio kūrimo strategijos**.
1. Veiksmų juostoje pasirinkite **Sukurti klasės sąrašą** tam, kad įsitikintumėte, kad turite naujausias esamų klasių versijas.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Įveskite unikalų strategijos pavadinimą, pasirinkite krovinio kūrimo strategijos klasę jam ir įveskite aprašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Parametrai**.
1. Puslapyje **Krovinio kūrimo strategijos parametrai** puslapyje rinkitės **Apimties talpa** sąraše ir tada **Vertės** laujelyje įveskite krovinio bendros apimties pajėgumo procentą, kuris turi būti taikomas naujai krovinio kūrimo strategijai.
1. Pasirinkite **Krovinio pajėgumas** sąraše ir tada **Vertės** laukelyje įveskite krovinio bendro svorio pajėgumo procentą, kuris turi būti taikomas naujai krovinio kūrimo strategijai.
1. Uždarykite **Krovinio kūrimo strategijos parametrų** puslapį.
1. Uždarykite **Krovinio kūrimo strategijų parametrų** puslapį.

Dabar galite priskirti krovinio kūrimo strategiją tam, kad sukurtumėte krovinio šabloną. Kitu atveju, galite naudoti jį tiesiogiai krovinio planavimo darbo srtiyje.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Naudokite krovinio kūrimo strategiją krovinio kūrimo darbo srityje

1. Eikite į **Gabenimo valdymas &gt; Planavimas &gt; Krovinio kūrimo darbo sritis**.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Pasirinkite strategiją **Krovinio kūrimo strategijos** laukelyje.
    - Jei nustatote krovinio kūrimo šabloną ir jai priskiriate krovinio kūrimo strategiją, veiksmų juostoje, **Valdyti šablonus** skirtuke, rinkitės **Taikyti šabloną**. Tada **Taikyti krovinio kūrimo šabloną** iškrentančiame teksto laukelyje pasirinkite šabloną **Krovinio kūrimo šablono pavadinimo** laukelyje.

1. „FastTab“ **Krovinio šablonų seka** pasirinktie vieną ar daugiau [krovinio šablonų](load-template.md). Darbo sritis bandys priderinti krovinį prie šių talpyklų tipų čia nurodyta seka. Dažniausiai, galite padėti mažiausias talpyklas sąrašo viršuje, kad užtikrintumėte, jog mažiausias galimas konteineris yra pasirinktas pirma.
1. Veiksmų juosoje rinkitės **Siūlyti krovinius**.
1. Peržiūrėkite siūlomus krovinius ir krovinių eilutes.
1. Veiksmų juostoje rinkitės **Kurti krovinius** tam, kad sukurtumėte krovinius pagrįstus šaltinio dokumentų linijoje **Siūlomų krovinių linijų** „FastTab“.
1. Uždarykite **Krovinio kūrimo darbo srities** puslapį.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]