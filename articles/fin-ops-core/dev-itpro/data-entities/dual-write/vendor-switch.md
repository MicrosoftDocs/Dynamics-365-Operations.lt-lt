---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą programose „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 21f48574d34b810c8ca554a55f1c063893a34b4d
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416814"
---
# <a name="switch-between-vendor-designs"></a>Perjungimas iš vieno tiekėjo dizaino į kitą

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



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