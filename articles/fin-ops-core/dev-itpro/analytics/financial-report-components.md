---
title: Finansinės ataskaitos komponentai
description: Šiame straipsnyje aprašoma, kaip ataskaitų aprašų komponentai (arba kūrimo blokai) naudojami finansinėse ataskaitose.
author: aprilolson
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.form: FinancialReports
ms.openlocfilehash: 66430f81bd3d1efe126dfb29fa9c6a093716f90e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802721"
---
# <a name="financial-report-components"></a>Finansinių ataskaitų komponentai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip ataskaitų aprašų komponentai (arba kūrimo blokai) naudojami finansinėse ataskaitose. Šie kūrimo blokai apima eilučių aprašus, stulpelių aprašus ir ataskaitų medžio aprašus. Šiame straipsnyje aiškinama, kaip išdėstyti ir užrakinti kūrimo blokus.

Finansinių ataskaitų dizaino įrankio suskaidyti informaciją į mažiausius komponentus ar kūrimo blokus ir tada komponentus pagal poreikį maišyti ir derinti. Todėl jūsų ataskaitos formatavimas atskiria nuo jūsų finansinių duomenų,  Microsoft Dynamics ataskaitos dizainą galima pakeisti nekeiskite finansinių duomenų 365 finansuose. Naudodami šį kūrimo bloko metodą galite sujungti tekstą, sumas ir skaičiavimus ir sukurti reikiamas ataskaitas. Be to, šis lankstumas skatina kūrybiškumą, nes galite lengviau skirtingais būdais peržiūrėti operacijas. Atskiri ataskaitos aprašo kūrimo blokai panašūs į trimatę skaičiuoklę, bet turi daugiau galios. Ataskaitos apraše nurodomas eilutės aprašas, stulpelio aprašas ir ataskaitoje naudojamas pasirinktinis medžio aprašas. Jame taip pat pateikiama informacija apie tai, kur saugoti sugeneruotą ataskaitą ir kaip ją formatuoti.

## <a name="building-blocks-of-a-report"></a>Ataskaitos kūrimo blokai

| Kūrimo blokas            | aprašymas | Daugiau informacijos |
|---------------------------|-------------|----------------------|
| Eilutės apibrėžimas            | Ataskaitos eilutės apraše apibūdinamos aprašomosios eilutės (pavyzdžiui, atlyginimai arba pardavimai). Jame taip pat pateikiamos segmentų reikšmės arba dimensijos, kuriose yra kiekvienos eilutės elemento reikšmės ir jis apima eilutės formatavimą ir skaičiavimus. | [Eilutės apibrėžimai](row-definitions-financial-reporting.md) |
| Stulpelio aprašas         | Stulpelio apraše nurodomas laikotarpis, kuris turi būti naudojamas išskleidžiant duomenis iš finansinių dimensijų. Jis taip pat apima stulpelio formatavimą ir skaičiavimus. | [Stulpelių apibrėžimai](column-definitions-financial-reports.md) |
| Ataskaitų medžio apibrėžimas | Ataskaitų medžio apibrėžimas panašus į organizacijos struktūros diagramą. Jame yra atskiri ataskaitų vienetai, kurie atitinka kiekvieną diagramos langelį. Vienetai gali būti atskiri finansinių duomenų padaliniai arba aukštesnio lygio vienetai, kurie apibendrina duomenis iš kitų ataskaitų vienetų. | [Ataskaitų medžio apibrėžimai](financial-reporting-tree-definitions.md) |
| Ataskaitos aprašas         | Ataskaitos apraše naudojamas eilutės apibrėžimas, stulpelio apibrėžimas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio apibrėžimas. Jame taip pat pateikiamos papildomos parinktys ir parametrai, kuriuos galite naudoti ataskaitai tinkinti. | [Ataskaitos aprašas](design-financial-report-definitions.md) |

Jei ataskaitas kuriate pirmą kartą, naudinga naudoti ataskaitų vedlį, kad galėtumėte greitai sukurti ataskaitos aprašą, kurį vėliau galėsite tinkinti. Jei turite ataskaitų kūrimo patirties ir kurdami ataskaitas norite daugiau lankstumo, galite sujungti naujus arba esamus kūrimo blokus ir sukurti naują ataskaitos aprašą. Norėdami sukurti kokybiškas ataskaitas, jūs neturite visiškai suprasti visų galimų ataskaitos aprašo parinkčių. Kai susipažinsite su ataskaitų kūrimu, galite išplėsti savo ataskaitų apibrėžimus, kad galėtumėte pasinaudoti sudėtingesnėmis funkcijomis. Sukūrę pagrindinę ataskaitą galite tinkinti ataskaitos aprašą ir bet kuriuos ataskaitos aprašo blokus.

## <a name="organize-the-building-blocks"></a>Kūrimo blokų tvarkymas
Norėdami sisteminti savo ataskaitų dizaino įrankio kūrimo blokus, naudokite aplankus. Visi aplankai surūšiuoti pagal juose nurodomą kūrimo bloko tipą. Pavyzdžiui, visi aplankai, kuriuose yra eilučių apibrėžimai, yra ataskaitų **dizaino** įrankio eilutės apibrėžimų srityje.

### <a name="create-a-folder"></a>Kurti aplanką

1. Ataskaitų konstruktoriuje pasirinkite kūrimo bloko, kad būtų galima tvarkyti naršymo srityje, tipą. Pavyzdžiui, norėdami rūšiuoti eilutės apibrėžimą, spustelėkite **Eilučių apibrėžimai**.
2. Naršymo srityje pasirinkite esamą aplanką, pagal kurį bus sukurtas naujas aplankas, o tada atlikite vieną iš tolesnių veiksmų.

    - Dešiniuoju pelės mygtuku spustelėkite pirminį aplanką, tada spustelėkite **Naujas aplankas**.
    - Pasirinkite pirminį aplanką, spustelėkite **Failas**, tada spustelėkite **Naujas aplankas**.

3. Kai pasirodo naujas aplankas, įveskite naujo aplanko pavadinimą ir paspauskite **Enter**.

## <a name="lock-a-building-block"></a>Užrakinti kūrimo bloką
Norėdami apsaugoti ir užrakinti kūrimo bloką, galite sukurti slaptažodį. Tai padarius ataskaitos komponentui pridedamas saugumo lygis, tačiau visa sistema neapsaugoma. Slaptažodžiu galima geriau apsaugoti kūrimo bloko informaciją, kuri yra svarbi jūsų mėnesio pabaigos ataskaitų procesui. Kūrimo bloką gali užrakinti bet kurio vaidmens vartotojas. Tačiau kiti vartotojai visada turės tik skaitymo prieigą prie užrakinto komponento. Vartotojai gali atidaryti, keisti ir įrašyti užrakintą komponentą nauju pavadinimu. Administratoriaus vaidmenį turintis vartotojas visada gali pasiekti ir keisti užrakintą kūrimo bloką.

1. Ataskaitų konstruktoriuje atidarykite ataskaitos komponentą, kad būtų galima užrakinti, pvz., eilutės apibrėžimą, stulpelio apibrėžimą, ataskaitos aprašą arba ataskaitų medžio apibrėžimą.
2. Meniu **Įrankiai** spustelėkite **Apsaugoti / panaikinti apsaugą**. Taip pat galite spustelėti įrankių juostos (spynos) piktogramą **Apsaugoti / panaikinti apsaugą**.
3. Dialogo lange **Apsaugoti** įveskite ir patvirtinkite slaptažodį, o tada spustelėkite **Gerai**. Kai atviras kūrimo blokas užrakinamas, įrankių juostos užrakto piktograma paryškinama.

Norėdami atrakinti užrakintą kūrimo bloką, atidarykite kūrimo bloką ir įrankių juostoje spustelėkite piktogramą **Apsaugoti / panaikinti apsaugą**. Arba meniu **Įrankiai** spustelėkite **Panaikinti apsaugą**.

## <a name="building-block-groups"></a>Kūrimo blokų grupės

Kūrimo blokai yra jūsų sukurti ataskaitos eilučių apibrėžimai, stulpelių apibrėžimai, ataskaitų medžio apibrėžimai ir ataskaitų aprašai. Kūrimo blokų grupės yra apibrėžimų ir dimensijų rinkiniai.

### <a name="view-a-building-block-group"></a>Kūrimo blokų grupės peržiūra

Galite peržiūrėti visus kūrimo bloko grupei priskirtus kūrimo blokus. Kūrimo bloko grupę taip pat galite eksportuoti arba importuoti.

1. Ataskaitų konstruktoriuje, meniu **Įmonė**, spustelėkite Kūrimo **blokų grupės**.
2. Kūrimo blokų **grupių dialogo** lange pasirinkite, norimą peržiūrėti kūrimo bloką.
3. Spustelėkite **Rodyti,** jei norite atidaryti **dialogo langą Rodyti** kūrimo bloką, kuriame galite peržiūrėti kūrimo blokų grupės turinį.
4. Spustelėkite **Uždaryti** norėdami uždaryti dialogo langus.

### <a name="export-a-building-block-group"></a>Kūrimo blokų grupės eksportavimas

Galite eksportuoti kūrimo blokų grupę arba konkrečius ataskaitų kūrimo blokus, esančius kūrimo blokų grupėje. Eksportuotą kūrimo blokų grupę galite naudoti kaip atsarginę kopiją. Eksportuotus duomenis taip pat galite kopijuoti į kitas programas. Ataskaitų dizaino įrankyje nurodyti šriftų stiliai ir dimensijų rinkiniai pateikiami kartu su kūrimo blokų grupe.

1. Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo blokų grupės**.
2. Dialogo lange **Kūrimo bloko** grupės pasirinkite norimą eksportuoti kūrimo blokų grupę, tada spustelėkite **Eksportuoti**.
3. Dialogo lange **Eksportuoti** pasirinkite norimus eksportuoti ataskaitos aprašus.

    - Norėdami eksportuoti visus savo ataskaitų aprašus ir susijusius kūrimo blokus, spustelėkite **Žymėti viską**.
    - Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus. Norėdami skirtuke pasirinkti keletą elementų, paspauskite ir laikykite nuspaudę klavišą CTRL.

    > [!NOTE]
    > Kai pasirenkate eksportuotinas ataskaitas, pasirenkamos susijusios eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.

4. Baigę žymėti norimus eksportuoti elementus, spustelėkite **Eksportuoti**.
5. Dialogo lange **Įrašyti kaip** pažymėkite vietą, į kurią eksportuoti kūrimo bloko grupę.
6.  **Lauke Failo vardas** įveskite failo pavadinimą. Ataskaitų dizaino įrankis automatiškai įtraukia .tdbx failo vardo plėtinį.
7. Spustelėkite **Įrašyti**. Kūrimo bloko grupė įrašoma į nurodytą vietą.

### <a name="import-a-building-block-group"></a>Kūrimo bloko grupės importavimas

Į esamą kūrimo bloko grupę galite importuoti kitą kūrimo blokų grupę. Visos importuotos kūrimo blokų grupės išlaiko savo pradinius šrifto stilius ir įmonės nuorodas bei atitinkamus dimensijų rinkinius.

1. Ataskaitų konstruktoriuje, meniu **Įmonė**, spustelėkite Kūrimo **blokų grupės**.
2. Dialogo lange **Kūrimo blokų** grupės pasirinkite kūrimo bloką, į jį importuoti kūrimo blokų grupę, tada spustelėkite **Importuoti**.
3. Dialogo lange **Atidaryti** pasirinkite importuotiną kūrimo blokų grupę ir spustelėkite **Atidaryti**.
4. Dialogo lange **Importuoti** pasirinkite norimus importuoti ataskaitos aprašus.

    - Norėdami importuoti visus ataskaitų aprašus ir palaikymo kūrimo blokus, spustelėkite **Žymėti viską**.
    - Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

5. Baigę žymėti norimus importuoti elementus, spustelėkite **Importuoti**.

### <a name="undo-a-checkout-of-a-building-block"></a>Anuliuoti kūrimo bloko išregistravimą

Atidarę kūrimo bloką kiti vartotojai gali pasiekti tą kūrimo bloką tik skaitymo režimu. Kartais vartotojai pamiršta uždaryti kūrimo bloką arba išjungia sistemą neuždarę kūrimo bloko. Todėl kūrimo blokas išregistruojamas ir kiti vartotojai negali jo atidaryti. Šiais atvejais finansinių ataskaitų administratorius gali naudoti dialogo langą **Išregistruoti elementai** ir užregistruoti kūrimo blokus, kuriuos vartotojai paliko išregistruotus.

> [!NOTE]
> Turite turėti administratoriaus vaidmenį norėdami įregistruoti kūrimo blokus dialogo lange **Išregistruoti elementai**.

1. Ataskaitų dizaino įrankio meniu **Įrankiai** spustelėkite Išregistravimo **elementai**.
2. Dialogo lange **Išregistruoti** elementus pasirinkite **Rodyti prekes iš visų vartotojų**. Sąrašas atnaujinamas, kad būtų parodyti išregistruoti kūrimo blokai ir juos išregistravę vartotojai.
3. Pasirinkite kūrimo bloką, tada spustelėkite Anuliuoti **išregistravimas**.
4. Spustelėkite **Taip** norėdami įregistruoti kūrimo bloką.

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
