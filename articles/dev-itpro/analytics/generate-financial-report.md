---
title: Generuoti finansines ataskaitas
description: "Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą."
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b47c22576b3735fbc499c7ceed3f6a4637c2785c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="generate-financial-reports"></a>Generuoti finansines ataskaitas

[!include [banner](../includes/banner.md)]

Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą. 

Norėdami sugeneruoti ataskaitą, atidarykite ataskaitos aprašą ir tada spustelėkite įrankių juostos mygtuką Generuoti. Bus atidarytas langas Ataskaitų eilės būsena, kuriame bus nurodyta ataskaitos vieta eilėje. Pagal numatytuosius parametrus sugeneruota ataskaita bus atidaryta žiniatinklio peržiūros programoje.

> [!NOTE]
> Sugeneruotos ataskaitos gali būti tik tuose aplankuose ir vietose, kurias turite teisę pasiekti.

Toliau pateikiamoje lentelėje paaiškinamos parinktys, galimos generuojant ataskaitas.

| Parinktis                                                                                | 
|---------------------------------------------------------------------------------------|
| Nustatykite grafiką, pagal kurį ataskaita arba ataskaitų grupė bus sugeneruota automatiškai              |   
| Patikrinkite, ar ataskaitoje netrūksta sąskaitų arba duomenų, ir patikrinkite ataskaitos tikslumą |   

Generuojant ataskaitą, naudojamos parinktys, kurias nurodėte skirtukuose Ataskaitos aprašas. Skirtuke Išvestis ir paskirstymas galite nurodyti ataskaitos vietą bibliotekoje – tai lengvas būdas ataskaitai bendrinti.

## <a name="generate-a-financial-report"></a>Generuoti finansinę ataskaitą

Norėdami generuoti finansinę ataskaitą naudodami „Microsoft Dynamics 365 for Finance and Operations“, eikite į **Didžioji knyga** > **Užklausos ir ataskaitos** > **Finansinės ataskaitos**. 
- Pasirinkite norimą generuoti ataskaitą ir spustelėkite **Generuoti**. 
- Užpildykite lauką **Ataskaitos data** ir spustelėkite **Gerai**.

  Sugeneravus ataskaitą, ją bus galima peržiūrėti skyriuje **Ataskaitos**.
  Galite pasirinkti **Peržiūrėti** arba **Panaikinti** ataskaitą.


Norėdami sugeneruoti ataskaitą naudodami **Ataskaitų kūrimo įrankis**, atidarykite ataskaitos aprašą, tada įrankių juostoje spustelėkite mygtuką Generuoti. Bus atidarytas langas Ataskaitų eilės būsena, kuriame bus nurodyta ataskaitos vieta eilėje. Pagal numatytuosius parametrus sugeneruota ataskaita bus atidaryta žiniatinklio peržiūros programoje.

> [!NOTE]
> Sugeneruotos ataskaitos gali būti tik tuose aplankuose ir vietose, kurias turite teisę pasiekti.


## <a name="schedule-report-generation"></a>Ataskaitos generavimo planavimas
Siekdamos laikytis verslo procesų, daug įmonių turi pagrindinį ataskaitų, kurios rengiamos suplanuotais intervalais, rinkinį. Galite suplanuoti, kad ataskaita būtų generuojama reguliariai, pavyzdžiui, kasdien, kas savaitę, kas mėnesį arba kasmet. Tai gali būti viena ataskaita arba ataskaitų grupė, į kurią būtų įtrauktos kelios įmonės. Reikia įvesti jums suteiktus kredencialus (kiekvienos nurodytos įmonės), kurie pateikti ataskaitų medžio apraše. Jei kredencialai netinkami, ataskaitoje bus rodoma tik ta informacija, kurią pasiekti turite teisę, pavyzdžiui, įmonė, prie kurios tuo metu esate prisiregistravę. Išvesties informacija pirmiausia skaitoma iš ataskaitos grupės, o tada – iš atskirų ataskaitų.

Sukūrus ir įrašius ataskaitų grafikus, jie bus rodomi naršymo srities dalyje Ataskaitų grafikai. Galite sukurti ataskaitoms tvarkyti skirtus aplankus. Jei viena į grafiką įtraukta ataskaita nepaleidžiama, visos kitos ataskaitos bus paleidžiamos.

> [!IMPORTANT]
> Norint kurti, modifikuoti ar panaikinti ataskaitų grafikus, jums turi būti suteiktas dizainerio arba administratoriaus vaidmuo. Vykdant ataskaitą, vartotojo, sukūrusio grafiką, kredencialai naudojami ataskaitai generuoti.


### <a name="create-a-report-schedule"></a>Ataskaitų grafiko kūrimas

1.  Ataskaitų konstruktoriaus meniu Failas spustelėkite Naujas ir tada pasirinkite Ataskaitų grafikas. Atidaromas dialogo langas Naujas ataskaitų grafikas.
2.  Dalyje Parametrai pasirinkite norimą suplanuoti atskirą ataskaitą arba ataskaitų grupę. Pasiekiamos tik tos įmonės ar kūrimo bloko ataskaitos arba ataskaitų grupės, prie kurių esate prisijungę.
3.  Norėdami įjungti ataskaitos grafiką, pažymėkite žymės langelį Aktyvi. Tik ataskaitos kūrėjas arba administratorius gali suaktyvinti ataskaitos grafiką arba jį išjungti.
4.  Spustelėkite Teisės, kad galėtumėte įvesti įmonės kredencialus. Pagal numatytąjį nustatymą jūsų prisijungimo informacija naudojama įmonei, prie kurios esate prisijungę. Jei yra kitų, pavyzdžiui, į ataskaitų medžio aprašus, įtrauktų įmonių, pasirinkite Naudoti atskirus kredencialus ir įveskite bet kurios kitos į ataskaitos grafiką įtrauktos įmonės kredencialus. Galite pasirinkti „Windows“ autentifikavimas arba įvesti vartotojo vardą ir kiekvienos įmonės slaptažodį. Pažymėkite žymės langelį Įrašyti kredencialus, kad įrašytumėte šių įmonių kredencialus, ir tada spustelėkite Gerai, kad užvertumėte dialogo langą.
5.  Dalies Dažnumas lauke Pradėti pasikartojimą pasirinkite datą, kada pradėti grafiką. Pagal numatytuosius nustatymus pasirenkama dabartinė kliento kompiuterio sistemos data.
6.  Lauke Paleisti ataskaitą pasirinkite ataskaitos paleidimo laiką. Jei įvesite laiką, buvusį iki esamo sistemos laiko, ataskaita bus paleista kitą suplanuotą datą.
7.  Srityje Pasikartojimo šablonas nurodykite ataskaitos paleidimo dažnumą. Pagal numatytuosius parametrus pasirinkta Kasdien su parinkties Intervalas (dienos) reikšme 1. Kitos parinktys yra Kas savaitę, Kas mėnesį ir Kasmet.
8.  Srityje Pasikartojimo diapazonas pasirinkite, kada baigti ataskaitos generavimą.
    -   Nėra pabaigos datos – ataskaitos grafikas neribotas.
    -   Nustatyti pasikartojimų skaičių – ataskaitos grafikas paleidžiamas nustatytą skaičių kartų, po to aktyvinimas panaikinamas.
    -   Baigti – ataskaitos grafikas pabaigiamas nurodytą datą.

9.  Įrankių juostoje spustelėkite Įrašyti. Dialogo lange Įrašyti kaip įveskite ataskaitų grafiko unikalų pavadinimą ir aprašą.

Kad galėtumėte kopijuoti ataskaitų grafiką, turite turėti dizainerio arba administratoriaus vaidmenį. Net jei administratorius modifikuos ataskaitų grafiką, ataskaitoje išliks ją sukūrusio vartotojo kredencialai.
### <a name="copy-a-report-schedule"></a>Ataskaitų grafiko kopijavimas

1.  Ataskaitos konstruktoriaus naršymo srityje spustelėkite Ataskaitų grafikai ir atidarykite ataskaitų grafiką, kurį norite kopijuoti.
2.  Meniu Failas spustelėkite Įrašyti kaip ir dialogo lange Įrašyti kaip įveskite naują grafiko pavadinimą ir aprašą. Spustelėkite Gerai, naršymo srityje bus rodomas naujas grafikas.
3.  Jei reikia, naujame grafike modifikuokite laukus ir informacija ir tada įrankių juostoje spustelėkite Įrašyti arba spustelėkite Įrašyti meniu Failas.

Kad galėtumėte panaikinti ataskaitos grafiką, turite būti ataskaitos grafiko savininkas arba turėti administratoriaus vaidmenį.
### <a name="delete-a-report-schedule"></a>Ataskaitų grafiko naikinimas

1.  Ataskaitų konstruktoriaus naršymo srityje spustelėkite Ataskaitų grafikai.
2.  Pasirinkite naikintiną ataskaitos grafiką ir spustelėkite Naikinti arba paspauskite klavišą „Delete“.
3.  Naikinimą patvirtinančiame dialogo lange spustelėkite Taip, kad visam laikui panaikintumėte ataskaitos grafiką. Jei neturite teisės naikinti grafiko, rodomas pranešimas, ir ataskaita nepanaikinama.

### <a name="credentials-and-report-schedules"></a>kredencialai ir ataskaitų grafikai

Jei neįvesite kredencialų, kuriuos reikia įvesti prie visų įmonių, įtrauktų į ataskaitas, įrašydami ataskaitos grafiką gausite šį pranešimą: „Turite įvesti savo kredencialus prie įmonių, esančių šiame ataskaitų grafike. Norėdami įvesti kredencialus, pasirinkite mygtuką Teisės“.

Pavyzdžiui, Irena prisijungia prie įmonės A naudodama savo prisijungimo vardą ir slaptažodį. Ji sukuria ataskaitos, kuri renka duomenis iš kelių įmonių naudodama ataskaitų medžio aprašą, grafiką. Įrašius šį ataskaitos grafiką, Phyllis paprašoma įvesti kitų į ataskaitų medžio aprašą įtrauktų įmonių kredencialus. Kai kredencialų galiojimo laikas baigiasi, paveiktos ataskaitos ataskaitų grafike negeneruojamos, kol kredencialai atnaujinami. Ataskaitų eilėje rodomas pranešimas, kuriame nurodoma, kad būtina atnaujinti teises. Ataskaitų grafikas sutrinka esant bet kuriam iš šių scenarijų (nes šiais atvejais būtini kredencialai):
-   į atskiros ataskaitos ataskaitų medį įtraukta nauja įmonė;
-   Buvo modifikuota ataskaitų grupėje esanti ataskaita.
-   Į ataskaitų grupę buvo įtraukta nauja papildomos įmonės ataskaita.

Norėdami tęsti, dialogo lange Ataskaitų planavimas spustelėkite mygtuką Teisės ir tada įveskite reikiamus kredencialus.

## <a name="missing-account-analysis-feature"></a>Trūkstamų sąskaitų analizės funkcija
Galite ieškoti finansinių sąskaitų ir dimensijų, kurių gali trūkti visuose eilučių aprašuose, ataskaitų medžio aprašuose ir ataskaitų aprašuose kūrimo bloko grupėje. Tai naudinga kuriant arba naujinant keletą sąskaitų arba kūrimo blokų per trumpą laikotarpį, ir norint patikrinti, ar į ataskaitas įtraukta visa nauja informacija.

Trūkstamos sąskaitos nustatomos naudojant mažiausią ir didžiausią reikšmes iš eilutės aprašo arba ataskaitų medžio aprašo, ir tada rodomas sąskaitų, kurių nėra eilutės apraše arba ataskaitų medžio apraše, bet kurios yra finansinių duomenų informacijoje, sąrašas. Jei trūkstamos sąskaitos vertė yra didesnė arba mažesnė nei eilutės apraše nurodyta vertė, ta sąskaita į trūkstamų sąskaitų sąrašą neįtraukiama.

> [!TIP]
> Tikrinimo tikslais šį procesą reikia paleisti prieš generuojant mėnesio ataskaitas ir kuriant naujus kūrimo blokus.

Mažiau tikėtina, kad sąskaitų truks ataskaitose, turinčiose reikšmių diapazonus. Jei įmanoma, naudokite diapazonus kūrimo bloke, kad būtų įtrauktos naujos sukurtos sąskaitos. Jei nustatyta, kad ataskaitos aprašas yra @ANY įmonės, galite prisijungti prie konkrečios įmonės ir vykdyti tos įmonės trūkstamų sąskaitų analizę.

> [!NOTE]
> Jei buvo įtraukta nauja įmonė, turite įtraukti naują įmonę į ataskaitų medžius visose esamose ataskaitose, arba įmonė nebus įtraukta į trūkstamų sąskaitų analizę.


### <a name="run-missing-account-analysis"></a>Trūkstamų sąskaitų analizės vykdymas

1.  Ataskaitų konstruktoriuje spustelėkite Įrankiai ir tada spustelėkite Trūkstamų sąskaitų analizė.
2.  Lauke Įmonės filtras pažymėkite įmonę, kurios rezultatus norite filtruoti, arba pažymėkite Viskas (filtrų nėra), jei norite, kad būtų pateikti visų galimų įmonių rezultatai.
3.  Lauke Dimensijos filtras pažymėkite dimensiją, pagal kurią norite filtruoti rezultatus, arba pažymėkite Viskas (filtrų nėra), jei norite peržiūrėti visą dimensijų informaciją pagal visas galimas dimensijas.
4.  Lauke Grupuoti pagal pažymėkite rezultatų rikiavimo parinktį. Rezultatus galima rikiuoti pagal konkretų kūrimo bloką arba dimensiją ir verčių rinkinius.
5.  Peržiūrėkite pateiktus rezultatus. Pažymėjus viršutinėje srityje esantį elementą, apatinėje srityje pateikiama papildomos informacijos apie išimtį. Nurodomos susijusios dimensijos, vertės ir ataskaitos.
6.  Norėdami atidaryti paveiktą elementą, spustelėkite susietą piktogramą rodoma sąrašo srityje, arba spustelėkite elementą dešiniuoju pelės klavišu ir pasirinkite Atidaryti. Norėdami pasirinkti kelis elementus, apatinėje srityje pažymėkite juos laikydami nuspaudę klavišą Ctrl.
7.  Jei grąžinama reikšmių, kūrimo blokų arba ataskaitų, kurios neturi būti įtrauktos į analizę, spustelėkite elementą dešiniuoju pelės klavišu ir pasirinkite Neįtraukti arba pažymėkite žymės langelį Neįtraukti, esantį šalia elemento, kad pašalintumėte elementą iš sąrašo. Neįtraukti elementai neįtraukiami atnaujinus sąrašą. Norėdami pažymėti kelis elementus, laikykite nuspaudę klavišą „Ctrl“ ir žymėkite elementus apatinėje srityje. Norėdami peržiūrėti visus elementus, kuriuos anksčiau pažymėjote kaip neįtrauktinus į analizę, pažymėkite žymės langelį Rodyti neįtrauktus kūrimo blokus ir vertes, o tada spustelėkite Atnaujinti.
8.  Spustelėkite Atnaujinti, kad būtų atkurtos išimtys, su kuriomis atlikote veiksmus. Spustelėkite Taip, kad būtų atnaujinti visi rezultatai, arba Ne, kad būtų atnaujinti tik tie elementai, su kuriais atlikote veiksmus.

    > [!NOTE]
    > Atidaroma forma automatiškai atkuriama, nebent ji buvo atidaryta per pastarąsias 15 min.

9.  Išsprendę problemas spustelėkite Gerai, kad uždarytumėte dialogo langą.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Klaviatūros spartieji klavišai trūkstamų sąskaitų analizei atlikti
Vykdant trūkstamų sąskaitų analizę, galima naudoti toliau nurodytus klaviatūros sparčiuosius klavišus.

| Norint tai padaryti                           | Naudoti šį klaviatūros spartųjį klavišą |
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


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Finansinės ataskaitos](financial-reporting-intro.md)

[Ataskaitų dizaino įrankio sąsaja](report-designer-interface.md)



