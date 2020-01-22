---
title: Sistemos nukreiptas klasterio paėmimas
description: Šioje temoje apžvelgiamas sistemos nukreiptas klasterio paėmimas „ Microsoft Dynamics 365 Supply Chain Management“.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c3b23a5d3b77bae89e4845bdff4ab20f95c46497
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917861"
---
# <a name="system-directed-cluster-picking"></a>Sistemos nukreiptas klasterio paėmimas

[!include [banner](../includes/banner.md)]

Klasterio paėmimas yra vieneto paėmimo procesas, kuris leidžia paimti prekes keletui užsakymų vienu metu, grupuojant juos į paėmimo klasterius. Tada paėmimo vietą teks aplankyti tik vieną kartą. Paprastai ši funkcija naudojama paimant nedidelius užsakymus arba kiekius, kurie yra mažesni už atvejo kiekius.

Kai nustatytas sistemos nukreiptas klasterio paėmimas, galima paimti darbo antraščių klasterius, remiantis sistemos sukurtu klasteriu. Sistema paima užsakymų klasterius, kurių vietų skaičius neviršija klasterio šablone nurodyto skaičiaus. Todėl galite paimti keletą užsakymų tuo pačiu metu, nekurdami klasterio rankiniu būdu.

Sistemos nukreiptas klasterio paėmimas – tai klasterių kūrimo rankiniu būdu, kai klasterio šablonas naudojamas klasteriui kurti, alternatyva. Prieš pradedant naudoti klasterio šabloną, jame reikia apibrėžti keletą su sąranka susijusių eilučių.

- **Vietų skaičius** atitinka užsakymų, kurie bus įtraukti į klasterį, skaičių. Todėl jis atitinka krepšių skaičių.
- **Skaidyti klasterį** nustato, kada klasterį reikia suskaidyti.
- **Generuoti klasterio ID** kontroliuoja, ar klasterio ID bus sugeneruotas sistemos, ar įvestas vartotojo.
- **Rūšiavimo patikros tipas** nustato, ar reikia atlikti vietų tikrinimą.

Naujas mobiliojo įrenginio meniu elementas naudojamas atliekant sistemos nukreiptą klasterio paėmimą. Klasterio šablono ID turi būti nurodytas nustatant parinktį **Nukreipė**. Be to, pagal sistemos nukreiptą užklausų tvarką galima grupuoti užsakymus pagal konkrečius įmonės kriterijus. Todėl galite dar labiau optimizuoti darbo užsakymų priskyrimą, nurodydami pritaikytus rūšiavimo kriterijus sistemos nukreiptoje užklausų tvarkoje.

Atlikus sistemos nukreiptą klasterio paėmimą, sandėlio darbininkams pateikiamas klasteris, kuriame paėmimo užsakymai iš anksto priskirti klasterio vietoms. Todėl darbininkai gali pradėti paimti prekę keletui darbo užsakymų, apsilankydami paėmimo vietoje tik vieną kartą. Sistemos nukreipto klasterio paėmimo procesas sutampa su vartotojo nukreipto klasterio paėmimo procesu.

## <a name="set-up-system-directed-cluster-picking"></a>Sistemos nukreipto klasterio paėmimo sąranka

### <a name="create-cluster-profiles"></a>Klasterių šablonų kūrimas

Klasterių šablonai kontroliuoja, kaip sistema sukuria kiekvieną klasterį. Jei reikia skirtingų klasterių, kiekvienam mobiliojo įrenginio meniu elementui reikia sukurti atskirą klasterio šabloną.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.
2. Pasirinkite **Naujas**.
3. Lauke **Klasterio šablono ID** įveskite **2 vietos**.
4. Lauke **Pavadinimas** įveskite **2 vietos**.
5. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Generuoti klasterio ID:** nustatykite šios parinkties vertę **Taip**. Ši pasirinktis nustato, ar sistema automatiškai sukuria klasterio ID, ar vartotojas jį sukuria paėmimo pradžioje.
    - **Aktyvinti vietas:** nustatykite šios parinkties vertę **Taip**. Ši pasirinktis nustato, ar vietų pavadinimai generuojami automatiškai, atsižvelgiant į vietų pavadinimų sąranką. Jei nustatyta šios parinkties vertė **Ne**, naudojamas vietos numerio lentelės ID.
    - **Vietų skaičius:** įveskite **2**. Šiame lauke nustatomas didžiausias vietų, kurias galima įtraukti į klasterį, skaičius (t. y., didžiausias dėžių, krepšių ir t. t. skaičius).
    - **Vietos pavadinimas:** pasirinkite **Skaitinis**, kad vietoms būtų suteikiami pavadinimai naudojant numerius iš eilės. Jei pasirinksite **Abėcėlė**, vietoms bus suteikiami pavadinimai abėcėlės tvarka.
    - **Skaidyti klasterį:** pasirinkite **Dėti**. Šiame lauke nustatoma, kada klasteris skaidomas.
    - **Rūšiavimo patikros tipas:** pasirinkite **Vietos nuskaitymas**. Šiame lauke nustatoma, ar tikrinamas dėjimo į vietą veiksmas.

6. „FastTab“ **Klasterių rūšiavimas** galite nustatyti rūšiavimo kriterijus, sukurdami naują eilutę ir nustatydami toliau pateikiamus laukus.

    - **Eilės numeris:** šiame lauke nustatoma eilė, pagal kurią sistema rūšiuoja. Vertė įvedama automatiškai, bet galite ją pakeisti pagal poreikį.
    - **Lauko pavadinimas:** pasirinkite **WMSLocationId**. Šiame lauke nustatomas laukas, kuris eilutėje naudojamas rūšiavimo kriterijams nustatyti.
    - **Rūšiavimas:** pasirinkite **Didėjimo tvarka**. Šiame lauke apibrėžiama, ar rūšiuojama didėjimo, ar mažėjimo tvarka.

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

Norėdami sukurti naują mobiliojo įrenginio meniu elementą sistemos nukreiptam klasterio paėmimui atlikti ir susieti klasterio šablono ID su mobiliojo įrenginio meniu elementu, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
2. Pasirinkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite **SD klasteris**.
4. Lauke **Pavadinimas** įveskite **SD klasteris**.
5. Lauke **Režimas** pasirinkite **Darbas**.
6. Nustatykite pasirinkties **Naudoti esamą darbą** padėtį **Taip**.
7. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Nukreipė:** pasirinkite **Sistemos nurodyta**.
    - **Generuoti numerio lentelę:** nustatykite šios parinkties vertę **Taip**.
    - **Klasterio šablono ID**: pasirinkite **2 vietos**.

8. „FastTab“ **Darbo klasės** nustatykite tinkamą darbo klasę šiam mobiliojo įrenginio meniu elementui, nustatydami toliau pateikiamus laukus.

    - **Darbo klasės ID:** įsitikinkite, kad įvesta **Pardavimas**.
    - **Darbo užsakymo ID:** įsitikinkite, kad įvesta **Pardavimo užsakymai**.

9. Norėdami nurodyti naują sistemos nurodytą darbo sekos užklausą, atlikite toliau pateikiamus veiksmus.

    1. Pasirinkite **Naujas**.
    2. Lauke **Eilės numeris** įveskite **1**.
    3. Lauke **Aprašas** pasirinkite **Darbo prioritetas – Darbo ID**.

10. Meniu pasirinkite **Redaguoti užklausą**.
11. Skirtuke **Rūšiavimas** nustatykite toliau nurodytus laukus.

    - **Lentelė:** pasirinkite **Darbas**.
    - **Išvestinė lentelė:** pasirinkite **Darbas**.
    - **Laukas:** pasirinkite **Darbo prioritetas**.
    - **Ieškos kryptis:** pasirinkite **Didėjimo tvarka**.
    - **Lentelė:** pasirinkite **Darbas**.
    - **Išvestinė lentelė:** pasirinkite **Darbas**.
    - **Laukas:** pasirinkite **Darbo ID**.
    - **Ieškos kryptis:** pasirinkite **Didėjimo tvarka**.

Sistema dabar rūšiuos darbo ID klasteryje, pirmiausia pagal darbo prioritetą, paskui pagal darbo ID.

### <a name="set-up-a-mobile-device-menu"></a>Mobiliojo įrenginio meniu nustatymas

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
2. Įtraukite meniu elementą, kurį ką tik sukūrėte, į norimą meniu.

## <a name="example"></a>Pavyzdys

### <a name="create-picking-work"></a>Paėmimo darbo kūrimas

Kad galėtumėte nustatyti sistemos nukreiptą klasterio paėmimą, turite sukurti tinkamą siuntimo darbą. Anksčiau sukurtame klasterio profilyje nurodytos dvi klasterio vietos. Todėl turite sukurti bent du darbo ID.

1. Eikite į **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
3. Lauke **Kliento sąskaita** pasirinkite bet kurį klientą.
4. „FastTab“ **Bendra** lauke **Sandėlis** pasirinkite sandėlį **62**.
5. Pasirinkite **Gerai**.
6. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę**.
7. Lauke **Prekės numeris** pasirinkite **A0001**.
8. Lauke **Kiekis** įveskite **1**.
9. Pasirinkite **Įtraukti eilutę**, kad įtrauktumėte antrą eilutę.
10. Lauke **Prekės numeris** pasirinkite **A0002**.
11. Lauke **Kiekis** įveskite **3**.
12. Pakartokite 2–6 veiksmus.
13. Lauke **Prekės numeris** pasirinkite **A0001**.
14. Lauke **Kiekis** įveskite **4**.
15. Pasirinkite **Įtraukti eilutę**, kad įtrauktumėte antrą eilutę.
16. Lauke **Prekės numeris** pasirinkite **A0002**.
17. Lauke **Kiekis** įveskite **2**.

Rezervuokite atsargas ir pateikite jas į sandėlį. Sukuriami du skirtingi darbo ID. Kiekviename darbo ID yra dvi paėmimo eilutės.

### <a name="run-the-mobile-device-flow"></a>Mobiliojo įrenginio srauto vykdymas

1. Mobiliajame įrenginyje pasirinkite meniu, kuriame yra naujas mobiliojo įrenginio meniu elementas.
2. Pasirinkite meniu elementą **SD klasteris** ir inicijuokite paėmimą. Sukuriamas klasteris ir prie jo pridedami du darbo ID, kuriuos sukūrėte anksčiau. Jei sukūrėte daugiau kaip du darbo ID, į klasterį įtraukiami tik pirmieji du. Atkreipkite dėmesį, kad darbo ID įtraukiami į klasterį didėjimo tvarka, kaip nurodyta užklausos sąrankoje.

    > [!NOTE]
    > Naujas klasteris sukuriamas automatiškai, tik jei anksčiau buvo sukurta pakankamai papildomų darbo ID. Priešingu atveju rodomas šis pranešimas: „Nepakanka darbo klasteriui“.

    Pasirinkus meniu, rodomas pirmas paėmimo ekranas. Sistema sujungia visas atitinkančias paėmimo eilutes iš dviejų darbo ID ir nukreipia jus į paėmimo vietą vieną kartą, kad galėtumėte įvykdyti abu užsakymus vienu paėmimu. Šis procesas atliekamas taip pat, kaip ir vartotojo nukreiptas klasterio paėmimo procesas.

3. Patvirtinkite pirmą paėmimą. Paskui turite įvesti vietos pavadinimą, kad patvirtintumėte, jog prekės buvo padėtos į tinkamą vietą.
4. Kartokite šį procesą, kol visos prekės bus paimtos ir padėtos į tinkamą vietą.
5. Paskutinis mobiliajame įrenginyje atliktinas veiksmas yra padėti klasterį į galutinę vietą. Patvirtinus šią padėjimo operaciją, klasteris uždaromas ir skaidomas, atsižvelgiant į vertę, kurią nustatėte klasterio šablono lauke **Skaidyti klasterį**. Darbo ID taip pat yra uždaromi.
6. Mobiliajame įrenginyje rodomas pranešimas „Klasteris baigtas“.
