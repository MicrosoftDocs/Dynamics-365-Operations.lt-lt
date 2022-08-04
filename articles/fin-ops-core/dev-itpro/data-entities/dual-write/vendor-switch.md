---
title: Perjungimas iš vieno tiekėjo dizaino į kitą
description: Šiame straipsnyje aprašoma, kaip perjungti tiekėjo duomenų integravimą tarp finansų ir operacijų programėlių ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 5a1b3a6049e7e31e7e5bdcf690a766ecea8dc4b1
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112341"
---
# <a name="switch-between-vendor-designs"></a>Perjungimas iš vieno tiekėjo dizaino į kitą

[!include [banner](../../includes/banner.md)]





## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas 

Jei nuspręsite naudoti **Paskyra** lentelę, kad galėtumėte išsaugoti tipo **Organizacija** tiekėjus, o lentelę **Kontaktai**, kad galėtumėte išsaugoti tipo **Asmuo** tiekėjus, sukonfigūruokite toliau nurodytas darbo eigas. Priešingu atveju ši konfigūracija nebūtina.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a>Tipo Organizacija tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas lentelėje Klientai
+ Tiekėjų kūrimas lentelėje Tiekėjai
+ Tiekėjų naujinimas lentelėje Klientai
+ Tiekėjų naujinimas lentelėje Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Paskyros**. Tada pasirinkite **Gerai**. Šioje darbo eigoje tvarkomas lentelės **Paskyra** tiekėjų kūrimo scenarijus.

    ![Tiekėjų kūrimas darbo eigos proceso lentelėje Klientai.](media/create_process.png)

2. Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Atnaujinti tiekėjus lentelėje Paskyros**. Tada pasirinkite **Gerai**. Šioje darbo eigoje tvarkomas lentelės **Paskyra** tiekėjų naujinimo scenarijus.
3. Sukurkite darbo eigos procesą lentelei **Paskyra** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas lentelėje Tiekėjai**.
4. Sukurkite darbo eigos procesą lentelei **Paskyra** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų atnaujinimas lentelėje Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.

    ![Mygtukas „Konvertuoti į foninę darbo eigą“.](media/background_workflow.png)

6. Aktyvinkite lentelėms **Paskyra** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti lentelę **Paskyra** ir galėtumėte saugoti tipo **Organizacija** informaciją tiekėjams.

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a>Tipo Asmuo tiekėjams naudokite išplėstinį tiekėjo dizainą

**„Dynamics365FinanceExtended“** sprendimų pakete yra toliau nurodyti darbo eigos proceso šablonai. Sukurkite darbo eigą kiekvienam šablonui.

+ Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai
+ Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai
+ Tiekėjų naujinimas tipo Asmuo lentelėje Kontaktai
+ Tiekėjų naujinimas tipo Asmuo lentelėje Tiekėjai

Norėdami sukurti naujus darbo eigos procesus, naudojant darbo eigos proceso šablonus, atlikite toliau nurodytus veiksmus.

1. Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga tvarko lentelės **Kontaktai** tiekėjų kūrimo scenarijų.
2. Sukurkite darbo eigos procesą lentelei **Tiekėjas** ir pasirinkite darbo eigos proceso šabloną **Tiekėjų atnaujinimas tipo Asmuo lentelėje Kontaktai**. Tada pasirinkite **Gerai**. Ši darbo eiga tvarko lentelės **Kontaktai** teikėjų atnaujinimo scenarijų.
3. Sukurkite darbo eigos procesą lentelei **Kontaktai** ir pasirinkite šabloną **Tiekėjų kūrimas tipo Asmuo lentelėje Tiekėjai**.
4. Sukurkite darbo eigos procesą lentelei **Kontaktai** ir pasirinkite šabloną **Tiekėjų atnaujinimas tipo Asmuo lentelėje Tiekėjai**.
5. Priklausomai nuo poreikių, darbo eigas galite konfigūruoti kaip realaus laiko arba foninę darbo eigą. Norėdami sukonfigūruoti darbo eigą kaip foninę darbo eigą, pasirinkite **Konvertuoti į foninę darbo eigą**.
6. Aktyvinkite lentelėms **Kontaktai** ir **Tiekėjas** sukurtas darbo eigas, kad pradėtumėte naudoti lentelę **Kontaktai** ir galėtumėte saugoti tipo **Asmuo** informaciją tiekėjams.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
