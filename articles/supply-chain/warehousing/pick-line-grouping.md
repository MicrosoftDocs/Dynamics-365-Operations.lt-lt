---
title: Paėmimo eilutės grupavimas
description: Šioje temoje pateikiama paėmimo eilutės grupavimo apžvalga.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215604"
---
# <a name="pick-line-grouping"></a>Paėmimo eilutės grupavimas

[!include [banner](../includes/banner.md)]

Vykdant paėmimo eilutės grupavimą, keletą darbo eilučių, kuriose yra ta pati prekė ir vieta, galima sujungti į vieną paėmimą, kuris pateikiamas vartotojui mobiliajame įrenginyje. Todėl sandėlio darbininkai gali gauti kuo naudingesnes instrukcijas, tačiau išlaikomas ir būtinas darbo eilučių atskyrimas sistemoje (pavyzdžiui, skirtingų konteinerių ir užsakymų atveju).

## <a name="set-up-pick-line-grouping"></a>Paėmimo eilutės grupavimo nustatymas

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai** ir sukurkite naują meniu elementą, pavadintą **Pardavimo grupės eilutės išrinkimas – vartotojo nurodyta**.
2. Dalyje **Mobiliojo įrenginio meniu elementai** nustatykite toliau pateikiamas vertes.

    - Lauke **Meniu elemento pavadinimas** įveskite **Pardavimo paėmimas - grupės eilutė**.
    - Lauke **Pavadinimas** įveskite **Pardavimo paėmimas - grupės eilutė**.
    - Lauke **Režimas** pasirinkite **Darbas**.
    - Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Taip**.

3. „FastTab“ **Bendra** galite nustatyti toliau pateikiamas vertes.

    - Lauke **Nukreipė** pasirinkite **Vartotojo nurodyta**.
    - Nustatykite parinkties **Generuoti numerio lentelę** vertę **Taip**.
    - Nustatykite parinkties **Grupinis paėmimas** vertę **Taip**.

4. „FastTab“ **Darbo klasės** atlikite toliau pateikiamus veiksmus, kad sukonfigūruotumėte mobiliojo įrenginio meniu elemento tinkamas darbo klases.

    1. Pasirinkite **Naujas**.
    2. Lauke **Darbo klasės ID** pasirinkite **Pardavimas** arba **PrdU paėmimas**, atsižvelgiant į sandėlį, kurį naudosite.
    3. Lauke **Darbo užsakymo tipas** pasirinkite **Pardavimo užsakymai**.

### <a name="set-up-a-mobile-device-menu"></a>Mobiliojo įrenginio meniu nustatymas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**. 
1. Įtraukite meniu elementą, kurį ką tik sukūrėte, į norimą meniu.

### <a name="set-up-a-work-template"></a>Darbo šablono nustatymas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Raskite darbo šabloną, kuris turėtų būti naudojamas atliekant šią funkciją. Šiame pavyzdyje pasirinkite standartinį **51 Paimti į etapą** „Contoso“ darbo šabloną.
1. Meniu pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Rūšiavimas** pasirinkite **Įtraukti**, tada nustatykite toliau pateikiamas vertes.

    - Lauke **Lentelė** pasirinkite **Laikinos darbo operacijos**.
    - Lauke **Išvestinė lentelė** pasirinkite **Laikinos darbo operacijos**.
    - Lauke **Laukas** pasirinkite **Prekės numeris**.
    - Lauke **Ieškos kryptis** pasirinkite **Didėjimo tvarka**.

> [!NOTE]
> Norint, kad paėmimo eilutės grupavimo funkcija veiktų, darbo eilutės turi būti surūšiuotos pagal prekės ID. Jei eilutės, kuriose yra tos pačios prekės, nepateikiamos viena po kitos, jos nebus grupuojamos.

## <a name="example"></a>Pavyzdys

### <a name="create-picking-work"></a>Paėmimo darbo kūrimas

Kad galėtumėte nustatyti paėmimo eilutės grupavimą, turite sukurti tinkamą siuntimo darbą.

1. Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą. 
3. Lauke **Kliento sąskaita** pasirinkite bet kurį klientą. 
4. „FastTab“ **Bendra** lauke **Sandėlis** pasirinkite **51**. Tada pasirinkite **Gerai**.
5. Dalyje **Pardavimo užsakymo eilutės** įtraukite toliau pateikiamas šešias eilutes.

    - **1 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**. Lauke **Kiekis** įveskite **3**.
    - **2 eilutė.** Lauke **Prekės numeris** pasirinkite **M9201**. Lauke **Kiekis** įveskite **3**. 
    - **3 eilutė.** Lauke **Prekės numeris** pasirinkite **M9202**. Lauke **Kiekis** įveskite **2**. 
    - **4 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**. Lauke **Kiekis** įveskite **1**. 
    - **5 eilutė.** Lauke **Prekės numeris** pasirinkite **M9200**. Lauke **Kiekis** įveskite **3**.
    - **6 eilutė.** Lauke **Prekės numeris** pasirinkite **M9202**. Lauke **Kiekis** įveskite **7**. 

    Toliau pateikiama kiekvienos prekės bendro kiekio suvestinė.

    - **Prekė M9200:** 7 vienetai
    - **Prekė M9201:** 3 vienetai
    - **Prekė M9202:** 9 vienetai

6. Prieš perduodami užsakymus į sandėlį, turite įsitikinti, kad paėmimo vietose pakanka atsargų visoms prekėms visuose užsakymuose pateikti. Patikrinkite parametrą **Vietos nurodymas**, kad nustatytumėte paėmimo vietas, naudojamas pardavimo užsakymo paėmimui atlikti.
7. Rezervuokite atsargas ir pateikite jas į sandėlį. Sukuriamas darbo ID, kuriame yra šešios eilutės. Eilutės rūšiuojamos pagal prekės numerį.

### <a name="run-the-mobile-device-flow"></a>Mobiliojo įrenginio srauto vykdymas

1. Mobiliajame įrenginyje pasirinkite meniu, kuriame yra naujas mobiliojo įrenginio meniu elementas.
1. Pasirinkite meniu elementą **Pardavimo paėmimas – grupės eilutė** ir inicijuokite paėmimą.

    Pasirinkę meniu ir įvedę darbo ID, pamatysite paėmimo veiksmą, kurį vykdant visos prekės M9200 paėmimo eilutės grupuojamos. Gaunate nurodymą paimti prekės M9200 7 vienetus.

1. Patvirtinkite paėmimo veiksmą. 
1. Perėję į atliekamo darbo kliento ekraną, pastebėsite, kad visos trys prekės M9200 paėmimo eilutės buvo uždarytos vienu metu.

    Pateikiama 4 darbo eilutė.

1. Patvirtinkite paėmimo veiksmą.

    Per paskutinį paėmimo veiksmą mobiliajame įrenginyje sujungiamos dvi paskutinės darbo užsakymo paėmimo eilutės.

1. Atlikite paėmimo veiksmą prekės M9202 9 vienetų atžvilgiu.
1. Patvirtinkite padėjimo veiksmą ir visas papildomas paėmimo / padėjimo poras, kad užbaigtumėte darbą.

> [!NOTE]
> - Darbo eilutes galima grupuoti tik tuo atveju, jei jos pateikiamos iš eilės.
> - Toliau nurodytos funkcijos nepalaikomos.
>
>    - Esamo svorio prekės. Jei darbe yra esamo svorio prekių, prieš pradėdami paėmimą matote klaidos pranešimą.
>    - Vienetų paėmimo patvirtinimas.
>    - Darbo eilutės, kuriose nebaigtas papildymo darbas.
>    - Viršytas paėmimo kiekis.
