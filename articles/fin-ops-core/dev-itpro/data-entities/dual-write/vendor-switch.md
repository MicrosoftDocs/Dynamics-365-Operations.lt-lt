---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą programose „Finance and Operations“ ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997557"
---
# <a name="switch-between-vendor-designs"></a>Perjungti iš vieno tiekėjo dizaino į kitą

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas 

Jei nuspręsite naudoti objektą **Klientas** , kad galėtumėte išsaugoti tipo **Organizacija** tiekėjus, o objektą **Kontaktas** , kad galėtumėte išsaugoti tipo **Asmuo** tiekėjus, sukonfigūruokite toliau nurodytas darbo eigas. Priešingu atveju ši konfigūracija nebūtina.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Tipo Organizacija tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas objekte Klientai
+ Tiekėjų kūrimas objekte Tiekėjai
+ Tiekėjų naujinimas objekte Klientai
+ Tiekėjų naujinimas objekte Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas objekte Klientai**. Tada pasirinkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.

    ![Tiekėjų kūrimas darbo eigos proceso objekte Klientas](media/create_process.png)

2. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas objekte Klientai**. Tada pasirinkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus.
3. Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas objekte Tiekėjai**.
4. Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas objekte Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.

    ![Mygtukas „Konvertuoti į foninę darbo eigą“](media/background_workflow.png)

6. Aktyvinkite objektams **Klientas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Klientas** ir galėtumėte saugoti tipo **Organizacija** informaciją tiekėjams.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Tipo Asmuo tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas tipo Asmuo objekte Tiekėjai
+ Tiekėjų kūrimas tipo Asmuo objekte Kontaktai
+ Tiekėjų naujinimas tipo Asmuo objekte Kontaktai
+ Tiekėjų naujinimas tipo Asmuo objekte Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas tipo Asmuo objekte Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga valdo objekto **Kontaktai** kūrimo scenarijų.
2. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas tipo Asmuo objekte Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga valdo objekto **Kontaktai** naujinimo scenarijų.
3. Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų kūrimas tipo Asmuo objekte Tiekėjai**.
4. Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų naujinimas tipo Asmuo objekte Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.
6. Aktyvinkite objektams **Kontaktas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Kontaktas** ir galėtumėte saugoti tipo **Asmuo** informaciją tiekėjams.
