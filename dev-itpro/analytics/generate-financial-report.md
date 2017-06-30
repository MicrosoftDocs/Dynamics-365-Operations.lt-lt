---
title: "Generuoti finansinę ataskaitą"
description: "Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 68843
ms.assetid: 271df6f4-12b7-4b3e-b2d7-36ea98ef1871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9b0d8fd9f5ae9d99f299cc71d7caef021ad3fb9d
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="generate-a-financial-report"></a>Generuoti finansinę ataskaitą

[!include[banner](../includes/banner.md)]


Šioje temoje parašoma informacija apie finansinės ataskaitos generavimą. 

Norėdami sugeneruoti ataskaitą, atidarykite ataskaitos aprašą ir tada spustelėkite įrankių juostos mygtuką Generuoti. Bus atidarytas langas Ataskaitų eilės būsena, kuriame bus nurodyta ataskaitos vieta eilėje. Pagal numatytuosius parametrus, sugeneruota ataskaita bus atidaroma žiniatinklio peržiūros programoje.
| ![Pastaba](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Pastaba")**Pastaba**        |
|------------------------------------------------------------------------------------------------|
| Sugeneruotos ataskaitos gali būti tik tuose aplankuose ir vietose, kurias turite teisę pasiekti. |

Toliau pateikiamoje lentelėje paaiškinamos parinktys, galimos generuojant ataskaitas.

| Parinktis                                                                                | Daugiau informacijos |
|---------------------------------------------------------------------------------------|----------------------|
| Nustatykite grafiką, pagal kurį ataskaita arba ataskaitų grupė bus sugeneruota automatiškai              |                      |
| Patikrinkite, ar ataskaitoje netrūksta sąskaitų arba duomenų, ir patikrinkite ataskaitos tikslumą |                      |

Generuojant ataskaitą, naudojamos parinktys, kurias nurodėte skirtukuose Ataskaitos aprašas. Skirtuke Išvestis ir paskirstymas galite nurodyti ataskaitos vietą bibliotekoje – tai lengvas būdas ataskaitai bendrinti.

## <a name="schedule-report-generation"></a> Ataskaitų generavimas pagal grafiką
Daugelis įmonių turi pagrindinių ataskaitų, kurios vykdomos suplanuotais intervalais, kad atitiktų verslo procesus. Galite suplanuoti, kad ataskaita būtų generuojama reguliariai, pavyzdžiui, kasdien, kas savaitę, kas mėnesį arba kasmet. Tai gali būti viena ataskaita arba ataskaitų grupė, kurioje yra kelių įmonių ataskaitų. Turite įvesti savo kredencialus prie kiekvienos nurodytos įmonės, kaip ataskaitų medžio apraše. Jei kredencialai netinkami, ataskaitoje bus rodoma tik ta informacija, kurią pasiekti turite teisę, pavyzdžiui, įmonė, prie kurios tuo metu esate prisiregistravę. Išvesties informacija pirmiausia skaitoma iš ataskaitos grupės, o tada – iš atskirų ataskaitų.

Sukūrus ir įrašius ataskaitų grafikus, jie bus rodomi naršymo srities dalyje Ataskaitų grafikai. Galite kurti aplankus ataskaitoms tvarkyti. Jei vieną tvarkaraščio ataskaita nevykdoma, visos kitos ataskaitos bus vykdomos toliau.
| ![Svarbu](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Svarbu")**Svarbu**                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kad galėtumėte kurti, modifikuoti ir naikinti ataskaitų grafikus, turite turėti dizainerio arba administratoriaus vaidmenį. Vykdant ataskaitą, vartotojo, sukūrusio grafiką, kredencialai naudojami ataskaitai generuoti. |

### <a name="create-a-report-schedule"></a>Ataskaitų grafiko kūrimas

1.  Ataskaitų konstruktoriaus meniu Failas spustelėkite Naujas ir tada pasirinkite Ataskaitų grafikas. Atidaromas dialogo langas Naujas ataskaitų grafikas.
2.  Dalyje Parametrai pasirinkite norimą suplanuoti atskirą ataskaitą arba ataskaitų grupę. Galimos tik pasirinktos įmonės arba kūrimo bloko, prie kurio šiuo metu esate prisiregistravę, ataskaitos arba ataskaitų grupės.
3.  Pažymėkite žymės langelį Aktyvus, kad įjungtumėte ataskaitų grafiką. Aktyvinti arba išjungti ataskaitos grafiką gali tik ataskaitos kūrėjas arba administratorius.
4.  Spustelėkite mygtuką Teisės norėdami įvesti įmonės kredencialus. Pagal numatytuosius parametrus jūsų registravimosi informacija naudojama įmonei, prie kurios esate prisiregistravę. Jei įtrauktos kitos įmonės, kaip ataskaitų medžio aprašuose, pasirinkite Naudoti atskirus kredencialus ir tada įveskite bet kurios kitos į ataskaitų grafiką įtrauktos įmonės kredencialus. Galite pasirinkti „Windows“ autentifikavimas arba įvesti kiekvienos įmonės vartotojo vardą ir slaptažodį. Pažymėkite žymės langelį Įrašyti kredencialus, kad įrašytumėte šių įmonių kredencialus, ir tada spustelėkite Gerai, kad užvertumėte dialogo langą.
5.  Dalies Dažnumas lauke Pradėti pasikartojimą pasirinkite datą, kada pradėti grafiką. Pagal numatytuosius parametrus pasirinkama dabartinė kliento kompiuterio sistemos data.
6.  Lauke Vykdyti ataskaitą pasirinkite laiką, kada reikia vykdyti ataskaitą. Jei įvesite laiką prieš dabartinį sistemos laiką, ataskaita bus vykdoma kitą suplanuotą datą.
7.  Srityje Kartojimas nurodykite, kaip dažnai ataskaita bus vykdoma. Pagal numatytuosius parametrus pasirinkta Kasdien su parinkties Intervalas (dienos) reikšme 1. Kitos parinktys yra Kas savaitę, Kas mėnesį ir Kasmet.
8.  Srityje Pasikartojimo diapazonas pasirinkite, kada ataskaitos generavimą reikia nutraukti.
    -   Nėra pabaigos datos – ataskaitos grafikas vykdomas neribotą laiką.
    -   Nustatytas pasikartojimų skaičius – ataskaitos grafikas vykdomas nurodytą skaičių kartų, o paskui išjungiamas.
    -   Baigti iki – ataskaitos grafikas baigiamas nurodytą datą.

9.  Įrankių juostoje spustelėkite Įrašyti. Dialogo lange Įrašyti kaip įveskite ataskaitų grafiko unikalų pavadinimą ir aprašą.

Kad galėtumėte kopijuoti ataskaitų grafiką, turite turėti dizainerio arba administratoriaus vaidmenį. Net jei administratorius modifikuos ataskaitų grafiką, ataskaitoje išliks ją sukūrusio vartotojo kredencialai.
### <a name="copy-a-report-schedule"></a>Ataskaitų grafiko kopijavimas

1.  Ataskaitos konstruktoriaus naršymo srityje spustelėkite Ataskaitų grafikai ir atidarykite ataskaitų grafiką, kurį norite kopijuoti.
2.  Meniu Failas spustelėkite Įrašyti kaip ir tada įveskite naują grafiko pavadinimą ir aprašą dialogo lange Įrašyti kaip. Spustelėkite Gerai, ir naujas grafikas bus rodomas naršymo srityje.
3.  Jei reikia, naujame grafike modifikuokite laukus ir informacija ir tada įrankių juostoje spustelėkite Įrašyti arba spustelėkite Įrašyti meniu Failas.

Kad galėtumėte panaikinti ataskaitos grafiką, turite būti ataskaitos grafiko savininkas arba turėti administratoriaus vaidmenį.
### <a name="delete-a-report-schedule"></a>Ataskaitų grafiko naikinimas

1.  Ataskaitų konstruktoriaus naršymo srityje spustelėkite Ataskaitų grafikai.
2.  Pasirinkti ataskaitų grafiką, kurį norite panaikinti, ir tada spustelėkite Naikinti arba paspauskite klavišą Delete.
3.  Naikinimo patvirtinimo dialogo lange spustelėkite Taip norėdami visam laikui panaikinti ataskaitos grafiką. Jei neturite teisės naikinti grafiko, rodomas pranešimas, ir ataskaita nepanaikinama.

### <a name="credentials-and-report-schedules"></a>Kredencialai ir ataskaitų grafikai

Jei neįvesite kredencialų, kuriuos reikia įvesti prie visų įmonių, įtrauktų į ataskaitas, įrašydami ataskaitos grafiką gausite šį pranešimą: „Turite įvesti savo kredencialus prie įmonių, esančių šiame ataskaitų grafike. Pasirinkite mygtuką Teisės norėdami įvesti savo kredencialus.“

Pavyzdžiui, Irena prisijungia prie įmonės A naudodama savo prisijungimo vardą ir slaptažodį. Ji sukuria ataskaitos, kuri renka duomenis iš kelių įmonių naudodama ataskaitų medžio aprašą, grafiką. Įrašius šį ataskaitos grafiką, Irena paraginama įvesti kredencialus prie kitų įmonių, kurios yra nurodytos ataskaitų medžio apraše. Kai kredencialų galiojimo laikas baigiasi, paveiktos ataskaitos ataskaitų grafike negeneruojamos, kol kredencialai atnaujinami. Ataskaitų eilėje rodomas pranešimas, kuriame nurodoma, kad būtina atnaujinti teises. Ataskaitų grafikas sutrinka esant bet kuriam iš šių scenarijų (nes šiais atvejais būtini kredencialai):
-   į atskiros ataskaitos ataskaitų medį įtraukta nauja įmonė;
-   ataskaitų grupės ataskaita buvo modifikuota;
-   į ataskaitų grupę įtraukta nauja papildomos įmonės ataskaita.

Norėdami tęsti, dialogo lange Ataskaitų planavimas spustelėkite mygtuką Teisės ir tada įveskite reikiamus kredencialus.

## <a name="missing-account-analysis-feature"></a> Trūkstamų sąskaitų analizės funkcija
Galite ieškoti finansinių sąskaitų ir dimensijų, kurių gali trūkti visuose eilučių aprašuose, ataskaitų medžio aprašuose ir ataskaitų aprašuose kūrimo bloko grupėje. Tai naudinga kuriant arba naujinant keletą sąskaitų arba kūrimo blokų per trumpą laikotarpį, ir norint patikrinti, ar į ataskaitas įtraukta visa nauja informacija.

Trūkstamos sąskaitos nustatomos naudojant mažiausią ir didžiausią reikšmes iš eilutės aprašo arba ataskaitų medžio aprašo, ir tada rodomas sąskaitų, kurių nėra eilutės apraše arba ataskaitų medžio apraše, bet kurios yra finansinių duomenų informacijoje, sąrašas. Jei trūkstama sąskaita yra didesnė arba mažesnė už eilutės apibrėžimo reikšmes, ta sąskaita į trūkstamų sąskaitų sąrašą neįtraukiama.
| ![Patarimas](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Patarimas")**Patarimas**                                             |
|----------------------------------------------------------------------------------------------------------------------------------|
| Siekiant patikrinti, šį procesą reikėtų vykdyti prieš generuojant mėnesio ataskaitas ir kuriant naujus kūrimo blokus. |

Mažiau tikėtina, kad sąskaitų truks ataskaitose, turinčiose reikšmių diapazonus. Jei įmanoma, naudokite diapazonus kūrimo bloke, kad būtų įtrauktos naujos sukurtos sąskaitos. Jei nustatyta, kad ataskaitos aprašas yra @ANY įmonės, galite prisijungti prie konkrečios įmonės ir vykdyti tos įmonės trūkstamų sąskaitų analizę.
| ![Pastaba](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Pastaba")**Pastaba**                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jei buvo įtraukta nauja įmonė, turite įtraukti naują įmonę į ataskaitų medžius visose esamose ataskaitose, arba įmonė nebus įtraukta į trūkstamų sąskaitų analizę. |

### <a name="run-missing-account-analysis"></a>Trūkstamų sąskaitų analizės vykdymas

1.  Ataskaitų konstruktoriuje spustelėkite Įrankiai ir tada spustelėkite Trūkstamų sąskaitų analizė.
2.  Lauke Įmonės filtras pasirinkite įmonę, kurios rezultatai bus filtruojami, arba pasirinkite parinktį Visos (filtro nėra), kad būtų rodomi rezultatai iš visų galimų įmonių.
3.  Lauke Dimensijų filtras pasirinkite dimensiją kurios rezultatus norite filtruoti, arba pasirinkite Visos (filtro nėra) norėdami peržiūrėti visų galimų dimensijų informaciją.
4.  Lauke Grupuoti pagal pasirinkite rezultatų rūšiavimo parinktį. Galite rūšiuoti rezultatus pagal paveiktą kūrimo bloką, arba galite rūšiuoti rezultatus pagal dimensiją ir reikšmių rinkinius.
5.  Peržiūrėkite rodomus rezultatus. Viršutinėje srityje pasirinkus elementą, apatinėje srityje rodoma papildoma informacija apie išimtį. Nurodomos susijusios dimensijos, reikšmės ir ataskaitos.
6.  Norėdami atidaryti paveiktą elementą, spustelėkite susietą piktogramą rodoma sąrašo srityje, arba spustelėkite elementą dešiniuoju pelės klavišu ir pasirinkite Atidaryti. Norėdami pasirinkti kelis elementus, apatinėje srityje pažymėkite juos laikydami nuspaudę klavišą Ctrl.
7.  Jei grąžinama reikšmių, kūrimo blokų arba ataskaitų, kurios neturi būti įtrauktos į analizę, spustelėkite elementą dešiniuoju pelės klavišu ir pasirinkite Neįtraukti arba pažymėkite žymės langelį Neįtraukti, esantį šalia elemento, kad pašalintumėte elementą iš sąrašo. Neįtraukti elementai neįtraukiami atnaujinus sąrašą. Norėdami pasirinkti kelis elementus, apatinėje srityje pažymėkite juos laikydami nuspaudę klavišą Ctrl. Norėdami peržiūrėti visus elementus, įskaitant visus rezultatus, kurių anksčiau pasirinkote neįtraukti į analizę, pažymėkite žymės langelį Rodyti neįtrauktus kūrimo blokus ir reikšmes ir tada spustelėkite Atnaujinti.
8.  Spustelėkite Atnaujinti norėdami atnaujinti išimtis, kurias sutvarkėte. Spustelėkite Taip, norėdami visiškai atnaujinti visus rezultatus, arba Ne, norėdami iš dalies atnaujinti sutvarkytus elementus.
    | ![Pastaba](https://i-technet.sec.s-msft.com/areas/global/content/clear.gif "Pastaba")**Pastaba**                    |
    |------------------------------------------------------------------------------------------------------------|
    | Forma automatiškai atnaujinama ją atidarant, išskyrus atvejus, kai forma buvo atidaryta per paskutines 15 minučių. |

9.  Išsprendę problemas spustelėkite Gerai, kad uždarytumėte dialogo langą.

## <a name="keyboard-shortcuts-for-missing-account-analysis"></a>Klaviatūros spartieji klavišai trūkstamų sąskaitų analizei atlikti
Vykdant trūkstamų sąskaitų analizę, galima naudoti toliau nurodytus klaviatūros sparčiuosius klavišus.

| Norint tai padaryti                           | Naudoti šį klaviatūros spartųjį klavišą |
|--------------------------------------|----------------------------|
| Filtruoti pagal įmonę                    | Alt + C                      |
| Filtruoti pagal dimensiją                  | Alt + D                      |
| Pasirinkti lauką Grupuoti pagal            | Alt + G                      |
| Rodyti neįtrauktus blokus ir vertes      | Alt + S                      |
| Atnaujinti rezultatus                      | Alt + R                      |
| Neįtraukti pasirinkto kūrimo bloko  | Alt + X                      |
| Neįtraukti pasirinkto eilutės aprašo  | Ctrl + B                     |
| Neįtraukti pasirinktos dimensijos reikšmės | Ctrl + D                     |
| Atidaryti pasirinktą ataskaitos aprašą  | Ctrl + R                     |
| Atidaryti pasirinktą eilutės aprašą     | Ctrl + O                     |

 
<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinės ataskaitos](financial-reporting-intro.md)

[Ataskaitų dizaino įrankio sąsaja](report-designer-interface.md)



