---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą programose „Finance and Operations“ ir „Dataverse“.
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
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685514"
---
# <a name="switch-between-vendor-designs"></a>Perjungti iš vieno tiekėjo dizaino į kitą

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas 

Jei nuspręsite naudoti objektą **Klientas**, kad galėtumėte išsaugoti tipo **Organizacija** tiekėjus, o objektą **Kontaktas**, kad galėtumėte išsaugoti tipo **Asmuo** tiekėjus, sukonfigūruokite toliau nurodytas darbo eigas. Priešingu atveju ši konfigūracija nebūtina.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Tipo Organizacija tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas lentelėje Klientai
+ Tiekėjų kūrimas lentelėje Tiekėjai
+ Tiekėjų naujinimas lentelėje Klientai
+ Tiekėjų naujinimas lentelėje Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Klientai**. Tada pasirinkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.

    ![Tiekėjų kūrimas darbo eigos proceso lentelėje Klientai](media/create_process.png)

2. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas lentelėje Klientai**. Tada pasirinkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus.
3. Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Tiekėjai**.
4. Sukurkite darbo eigos procesą objektui **Klientas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas lentelėje Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.

    ![Mygtukas „Konvertuoti į foninę darbo eigą“](media/background_workflow.png)

6. Aktyvinkite lentelėms **Klientas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Klientas** ir galėtumėte saugoti tipo **Organizacija** informaciją tiekėjams.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Tipo Asmuo tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
+ Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai
+ Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
+ Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga valdo objekto **Kontaktai** kūrimo scenarijų.
2. Sukurkite darbo eigos procesą objektui **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga valdo objekto **Kontaktai** naujinimo scenarijų.
3. Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai**.
4. Sukurkite darbo eigos procesą objektui **Kontaktas** ir pasirinkite šabloną **Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.
6. Aktyvinkite lentelėms **Kontaktas** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti objektą **Kontaktas** ir galėtumėte saugoti tipo **Asmuo** informaciją tiekėjams.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]