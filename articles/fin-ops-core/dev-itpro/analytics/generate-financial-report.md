---
title: Generuoti finansines ataskaitas
description: Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą.
author: jinniew
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 00a860089265800ca1a0058f222d5e85c360501c
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119532"
---
# <a name="generate-financial-reports"></a>Generuoti finansines ataskaitas

[!include [banner](../includes/banner.md)]

Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą.

Norėdami sugeneruoti ataskaitą, atidarykite ataskaitos aprašą ir įrankių juostoje pasirinkite **Generuoti**. Atidaroma **ataskaitų darbo** grupės būsenos puslapis, kuris nurodo jūsų ataskaitos vietą eilėje.

Kai vyksta ataskaitos generavimas, šie ataskaitų eilės būsenos indikatoriai gali būti matomi ataskaitos **eilės būsenos** puslapyje.

| Būsena          | Apskritis | Aprašymas|
|-----------------|--------|--------------------|
| Perkeliama į eilę        | Laikinosios |Ataskaitos aprašas tikrinamas prieš ataskaitos įeidami į generavimo eilę.                    |
| Darbo grupėje          | Laikinosios | Ataskaita įveda ataskaitos generavimo eilę ir laukia, kol ji bus apdorota.                      |
| Vykdoma      | Laikinosios | Ši būsena paprastai yra po darbo eilėje **būsenos** ir paprastai pereina į **galutinę** būseną, kai baigiama apdoroti.       |
| PostProcessing | Laikinosios | Ši būsena seka po apdorojimo būsenos **ir nurodo, kad visi ataskaitos duomenys surinkti, bet šie veiksmai, pvz., skaičiavimas** ir sumavimas, yra atliekami.            |
| Atšaukiama      | Laikinosios | Vartotojo pageidavimu ataskaitos atšaukiamos. Ši būsena nustatyta pagal vartotojo reikalaujamo atšaukimo ataskaitą, kurios būsena Darbo **grupės arba** **Apdorojimas**. Sistema bando nustatyti ataskaitos būseną **Atšaukta**, nebent sistema yra per toli ir turi užbaigti ją kitoje būsenoje. |
| Atšauktas        | Galutinis | Ataskaita baigta apdoroti, bet ji nebaigta dėl vartotojo reikalaujamo stabdymo.            |
| Užbaigta       | Galutinis | Ataskaita paruošta naudoti.                      |
| Atlikta nesėkmingai          | Galutinis | Ataskaita baigta, bet jos atlikti nepavyko, todėl jos naudoti negalima. |

Pagal numatytuosius parametrus, sugeneruota ataskaita bus atidaroma žiniatinklio peržiūros programoje. Galima naudoti toliau nurodytas ataskaitų generavimo parinktis.

- Nustatykite grafiką, pagal kurį ataskaita arba ataskaitų grupė bus sugeneruota automatiškai
- Patikrinkite, ar ataskaitoje netrūksta sąskaitų arba duomenų, ir patikrinkite ataskaitos tikslumą

Generuojant ataskaitą naudojamos pasirinktys, kurias nurodėte ataskaitos aprašo skirtukuose.

## <a name="generate-a-financial-report"></a>Generuoti finansinę ataskaitą

Norėdami generuoti finansinę ataskaitą, eikite į **Didžioji knyga** \> **Užklausos ir ataskaitos** \> **Finansinės ataskaitos**.

- Pasirinkite norimą generuoti ataskaitą ir pasirinkite **Generuoti**.
- Užpildykite lauką **Ataskaitos data** ir pasirinkite **Gerai**.

Sugeneravus ataskaitą, ją bus galima peržiūrėti skyriuje **Ataskaitos**.

Galite pasirinkti **Peržiūrėti** arba **Panaikinti** ataskaitą.

Norėdami sugeneruoti ataskaitą naudodamiesi **Ataskaitos kūrimo įrankis**, atverkite ataskaitos aprašą ir pasirinkite mygtuką **Generuoti** įrankių juostoje. Atsidarys **Ataskaitos eilės būsena** puslapis ir nurodys jūsų ataskaitos vietą eilėje. Pagal numatytuosius parametrus, sugeneruota ataskaita bus atidaroma žiniatinklio peržiūros programoje.

## <a name="report-groups"></a>Ataskaitų grupės

Ataskaitų grupės yra efektyvus būdas vienu metu generuoti keletą ataskaitų. Pavyzdžiui, tarkime, kad kas mėnesį vartotojai kas mėnesį generuos aštuonias ataskaitas. Pasirinkite Ataskaitų grupė, o ne **Generuoti** kiekvienai iš aštuonių grupėje esančių ataskaitų, galite pasirinkti **Generuoti** ataskaitų grupei ir aštuonios ataskaitos bus sugeneruotos iš karto. Kai pasirinktos ataskaitų grupės ataskaitos yra sukurtos, galite eiti į **Finansinės ataskaitos** (**Didžioji knyga > Užklausos ir ataskaitos > Finansinės ataskaitos**), kad peržiūrėtumėte atskiras ataskaitas. Norėdami nustatyti ataskaitų grupę, atlikite šiuos veiksmus.

1. Ataskaitų kūrimo įrankyje, pasirinkite **Ataskaitų grupės**. 
2. Pasirinkite esamus ataskaitų apibrėžimus, kurie bus įtraukti į jūsų ataskaitų grupę. 
3. Pasirinkite perrašyti įmonės, informacijos ir datos parametrus kiekvienoje iš ataskaitų, kurios bus įtrauktos į grupę.
   Kiekvienai ataskaitai rekomenduojame nustatyti **Įmonė**, **Laikotarpis**,  **Metai** ir **Išsamumo lygis**. 
4. Įrašykite ataskaitų grupę.

## <a name="schedule-report-generation"></a>Ataskaitos generavimo planavimas
Siekdamos laikytis verslo procesų, daug įmonių turi pagrindinį ataskaitų, kurios rengiamos suplanuotais intervalais, rinkinį. Galite suplanuoti, kad ataskaita būtų generuojama reguliariai, pavyzdžiui, kasdien, kas savaitę, kas mėnesį arba kasmet. Tai gali būti viena ataskaita arba ataskaitų grupė, į kurią būtų įtrauktos kelios įmonės. Reikia įvesti jums suteiktus kredencialus (kiekvienos nurodytos įmonės), kurie pateikti ataskaitų medžio apraše. Jei kredencialai negalioja, ataskaitoje bus rodoma tik informacija, kurią turite prieigos teisė, pvz., įmonė, prie kurios tuo metu esate prisiregistravę. Išvesties informacija pirmiausia skaitoma iš ataskaitos grupės, o tada – iš atskirų ataskaitų.

Kadangi ataskaitos grafikai sukuriami ir įrašomi, jie rodomi ataskaitų grafikų naršymo srityje. Galite sukurti ataskaitoms tvarkyti skirtus aplankus. Jei viena į grafiką įtraukta ataskaita nepaleidžiama, visos kitos ataskaitos bus paleidžiamos.

> [!IMPORTANT]
> Norint kurti, modifikuoti ar panaikinti ataskaitų grafikus, jums turi būti suteiktas dizainerio arba administratoriaus vaidmuo. Vykdant ataskaitą, vartotojo, sukūrusio grafiką, kredencialai naudojami ataskaitai generuoti.

### <a name="create-a-report-schedule"></a>Ataskaitų grafiko kūrimas

1. Ataskaitų kūrimo įrankyje **Failas** meniu, pasirinkite **Naujas** ir tada pasirinkite **Ataskaitų grafikas**. Atidaromas dialogo langas **Naujas ataskaitų grafikas**.
2. Dalyje **Parametrai** pasirinkite atskirą ataskaitą arba ataskaitų grupę, kurią norite paskirti į grafiką. Pasiekiamos tik tos įmonės ar kūrimo bloko ataskaitos arba ataskaitų grupės, prie kurių esate prisijungę.
3. Pažymėkite žymės langelį **Aktyvus**, kad įjungtumėte ataskaitų grafiką. Tik ataskaitos kūrėjas arba administratorius gali suaktyvinti ataskaitos grafiką arba jį išjungti.
4. Pasirinkite mygtuką **Teisės** norėdami įvesti įmonės kredencialus. Pagal numatytąjį nustatymą jūsų prisijungimo informacija naudojama įmonei, prie kurios esate prisijungę. Jei įtrauktos kitos įmonės, kaip ataskaitų medžio aprašuose, pasirinkite **Naudoti atskirus kredencialus** ir tada įveskite bet kurios kitos į ataskaitų grafiką įtrauktos įmonės kredencialus. Galite pasirinkti **„Windows“ autentifikavimas** arba įvesti kiekvienos įmonės vartotojo vardą ir slaptažodį. Pažymėkite žymės langelį **Įrašyti kredencialus**, kad įrašytumėte šių įmonių kredencialus, ir tada pasirinkite **Gerai**, kad užvertumėte dialogo langą.
5. Dalies **Dažnumas** lauke **Pradėti pasikartojimą** pasirinkite datą, kada pradėti grafiką. Pagal numatytuosius nustatymus pasirenkama dabartinė kliento kompiuterio sistemos data.
6. Lauke **Vykdyti ataskaitą** pasirinkite laiką, kada reikia vykdyti ataskaitą. Jei įvesite laiką, buvusį iki esamo sistemos laiko, ataskaita bus paleista kitą suplanuotą datą.
7. Srityje **Kartojimas** nurodykite, kaip dažnai ataskaita bus vykdoma. Pagal numatytuosius parametrus **Kasdien**  yra pasirinktas su intervalo (dienos) verte 1. Kitos parinktys yra Kas savaitę, Kas mėnesį ir Kasmet.
8. Srityje Pasikartojimo diapazonas pasirinkite, kada baigti ataskaitos generavimą.

    - **Nėra pabaigos datos** – ataskaitos grafikas vykdomas neribotą laiką.
    - **Nustatytas pasikartojimų skaičius** – ataskaitos grafikas vykdomas nurodytą skaičių kartų, o paskui išjungiamas.
    - **Baigti iki** – ataskaitos grafikas baigiamas nurodytą datą.

9. Pasirinkite **Įrašyti**. Dialogo lange **Įrašyti kaip** įveskite ataskaitų grafiko unikalų pavadinimą ir aprašą.

Kad galėtumėte kopijuoti ataskaitų grafiką, turite turėti dizainerio arba administratoriaus vaidmenį. Net jei administratorius modifikuos ataskaitų grafiką, ataskaitoje išliks ją sukūrusio vartotojo kredencialai.

### <a name="copy-a-report-schedule"></a>Ataskaitų grafiko kopijavimas

1. Ataskaitų kūrimo įrankyje pasirinkite **Ataskaitų grafikai** ir atidarykite ataskaitų grafiką, kurį norite kopijuoti.
2. Meniu **Failas** pasirinkite **Įrašyti kaip** ir tada įveskite naują grafiko pavadinimą ir aprašą dialogo lange **Įrašyti kaip**. Pasirinkite **Gerai**, ir naujas grafikas bus rodomas naršymo srityje.
3. Jei reikia, naujame grafike modifikuokite laukus ir informaciją ir tada įrankių juostoje pasirinkite **Įrašyti** arba pasirinkite **Įrašyti** meniu **Failas**.

Kad galėtumėte panaikinti ataskaitos grafiką, turite būti ataskaitos grafiko savininkas arba turėti administratoriaus vaidmenį.

### <a name="delete-a-report-schedule"></a>Ataskaitų grafiko naikinimas

1. Ataskaitų kūrimo įrankyje, naršymo srityje pasirinkite **Ataskaitų grafikai**.
2. Pasirinkti ataskaitų grafiką, kurį norite panaikinti, ir tada pasirinkite **Naikinti** arba paspauskite klavišą **Naikinti**.
3. Naikinimo patvirtinimo dialogo lange pasirinkite **Taip** norėdami visam laikui panaikinti ataskaitos grafiką. Jei neturite teisės naikinti grafiko, bus rodomas pranešimas, o ataskaita nebus panaikinta.

### <a name="credentials-and-report-schedules"></a>kredencialai ir ataskaitų grafikai

Jei neįvesite kredencialų, kuriuos reikia įvesti prie visų įmonių, įtrauktų į ataskaitas, įrašydami ataskaitos grafiką gausite šį pranešimą: „Turite įvesti savo kredencialus prie įmonių, esančių šiame ataskaitų grafike. Norėdami įvesti kredencialus, pasirinkite mygtuką Teisės.“

Pavyzdžiui, naudotojas prisijungia prie A įmonės, įvesdamas savo prisijungimo vardą ir slaptažodį. Naudotojas sukuria ataskaitos, kuri renka duomenis iš kelių įmonių naudodama ataskaitų medžio aprašą, grafiką. Įrašęs šį ataskaitos grafiką, naudotojas paprašoma įvesti kitų į ataskaitų medžio aprašą įtrauktų įmonių kredencialus. Kai jūsų kredencialai baigia galioti, paveiktos ataskaitos grafiko ataskaitos nesugeneruojama, kol kredencialai nebus atnaujinti. Ataskaitų eilėje rodomas pranešimas, kuriame nurodoma, kad būtina atnaujinti teises. Ataskaitų grafikas sutrinka esant bet kuriam iš šių scenarijų (nes šiais atvejais būtini kredencialai):

- į atskiros ataskaitos ataskaitų medį įtraukta nauja įmonė;
- Buvo modifikuota ataskaitų grupėje esanti ataskaita.
- Į ataskaitų grupę buvo įtraukta nauja papildomos įmonės ataskaita.

Norėdami tęsti, dialogo lange pasirinkite **Ataskaitų grafikas** spustelėkite mygtuką **Teisės** ir tada įveskite reikiamus kredencialus.

## <a name="missing-account-analysis-feature"></a>Trūkstamų sąskaitų analizės funkcija
Galite ieškoti finansinių sąskaitų ir dimensijų, kurių gali trūkti visuose eilučių aprašuose, ataskaitų medžio aprašuose ir ataskaitų aprašuose kūrimo bloko grupėje. Tai naudinga kuriant arba naujinant keletą sąskaitų arba kūrimo blokų per trumpą laikotarpį, ir norint patikrinti, ar į ataskaitas įtraukta visa nauja informacija.

Trūkstamos sąskaitos nustatomos naudojant žemiausią ir didžiausią eilutės apibrėžimo arba ataskaitų medžio apibrėžimo vertę, tada rodomas sąskaitų, kurių nėra eilutės apibrėžime arba ataskaitų medžio apibrėžime, bet yra finansiniuuose duomenyse, sąrašas. Jei trūkstama sąskaita yra didesnė arba mažesnė nei eilutės apibrėžimo vertės, ši sąskaita neįtraukiama į trūkstamų sąskaitų sąrašą.

> [!TIP]
> Tikrinimo tikslais šį procesą reikia paleisti prieš generuojant mėnesio ataskaitas ir kuriant naujus kūrimo blokus.

Mažiau tikėtina, kad sąskaitų truks ataskaitose, turinčiose reikšmių diapazonus. Jei galima, kad kuriant naujas sąskaitas būtų galima naudoti kūrimo bloko diapazonus. Jei kurios nors ataskaitos apraše įmonės nuostata yra @ANY, galima įeiti į konkrečią įmonę ir įvykdyti tos įmonės duomenyse trūkstamų sąskaitų analizę.

> [!NOTE]
> Jei buvo įtraukta nauja įmonė, turite įtraukti naują įmonę į ataskaitų medžius visose esamose ataskaitose, arba įmonė nebus įtraukta į trūkstamų sąskaitų analizę.

### <a name="run-missing-account-analysis"></a>Trūkstamų sąskaitų analizės vykdymas

1. Ataskaitų kūrimo įrankyje pasirinkite **Įrankiai** ir tada pasirinkite **Trūkstamų sąskaitų analizė**.
2. Lauke **Įmonės filtras** pasirinkite įmonę, kurios rezultatai bus filtruojami, arba pasirinkite parinktį **Visos (filtro nėra)**, kad būtų rodomi rezultatai iš visų galimų įmonių.
3. Lauke **Dimensijų filtras** pasirinkite dimensiją kurios rezultatus norite filtruoti, arba pasirinkite **Visos (filtro nėra)** norėdami peržiūrėti visų galimų dimensijų informaciją.
4. Lauke **Grupuoti pagal** pasirinkite rezultatų rūšiavimo parinktį. Rezultatus galima rikiuoti pagal konkretų kūrimo bloką arba dimensiją ir verčių rinkinius.
5. Peržiūrėkite pateiktus rezultatus. Pažymėjus viršutinėje srityje esantį elementą, apatinėje srityje pateikiama papildomos informacijos apie išimtį. Nurodomos susijusios dimensijos, vertės ir ataskaitos.
6. Norėdami atidaryti paveiktą elementą, pasirinkite susietą piktogramą rodoma sąrašo srityje, arba spustelėkite elementą dešiniuoju pelės klavišu ir pasirinkite **Atidaryti**. Norėdami pasirinkti kelis elementus, palaikykite nuspaudę klavišą **Ctrl**, kol pažymėsite apatinėje srityje esančius elementus.
7. Jei grąžinamos kokios nors vertės, kūrimo blokai ar ataskaitos, kurių nereikia įtraukti į analizę, **dešiniuoju** pelės mygtuku spustelėkite prekę ir pasirinkite Pašalinti arba pasirinkite šalia prekės esantį žymės langelį Pašalinti, **kad** pašalintumėte prekę iš sąrašo. Neįtrauktos prekės nėra įtraukiamos atnaujinant sąrašą. Norėdami pasirinkti kelis elementus, palaikykite nuspaudę klavišą **Ctrl**, kol pažymėsite apatinėje srityje esančius elementus. Norėdami peržiūrėti visus elementus, įskaitant anksčiau analizėje pasirinktus rezultatus, pasirinkite **Rodyti neįtrauktus blokus ir vertes** žymės langelį, tada pasirinkite **Atnaujinti**.
8. Pasirinkite Atnaujinti **,** norėdami atnaujinti išimčių, kurias iškrendėte, sąrašą. Pasirinkite **Taip**, norėdami visiškai atnaujinti visus rezultatus, arba pasirinkite **Ne**, norėdami iš dalies atnaujinti sutvarkytus elementus.

    > [!NOTE]
    > Atidaroma forma automatiškai atkuriama, nebent ji buvo atidaryta per pastarąsias 15 minutes.

9. Išsprendę problemas spustelėkite, pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Klaviatūros spartieji klavišai trūkstamų sąskaitų analizei atlikti
Vykdant trūkstamų sąskaitų analizę, galima naudoti toliau nurodytus klaviatūros sparčiuosius klavišus.

| Norėdami tai padaryti                           | Paspauskite  |
|--------------------------------------|----------------------------|
| Filtruoti pagal įmonę                    | Alt + C                      |
| Filtruoti pagal dimensiją                  | ALT + D                      |
| Pažymėti lauką Grupuoti pagal            | ALT + G                      |
| Rodyti neįtrauktus kūrimo blokus ir vertes      | ALT + S                      |
| Atnaujinti rezultatus                      | ALT + R                      |
| Neįtraukti pažymėto kūrimo bloko  | ALT + X                      |
| Neįtraukti pažymėto eilutės aprašo  | CTRL + B                     |
| Neįtraukti pažymėtos dimensijos vertės | CTRL + D                     |
| Atidaryti pažymėtos ataskaitos aprašą  | CTRL + R                     |
| Atidaryti pažymėtos eilutės aprašą     | CTRL + O                     |


## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)

[Ataskaitų dizaino įrankio sąsaja](report-designer-interface.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
