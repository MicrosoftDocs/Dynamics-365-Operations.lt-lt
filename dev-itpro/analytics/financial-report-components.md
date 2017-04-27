---
title: "Finansinės ataskaitos komponentai"
description: "Šiame straipsnyje aprašoma, kaip ataskaitų aprašų komponentai (arba kūrimo blokai) naudojami finansinėse ataskaitose. Šie kūrimo blokai apima eilučių aprašus, stulpelių aprašus ir ataskaitų medžio aprašus. Straipsnis paaiškina, kaip blokus organizuoti ir užrakinti ir kaip naudoti kūrimo blokų grupes."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 54 - 02
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a423dff4d8796f454c9c4db03c8ceb2b8c3d6456
ms.lasthandoff: 03/30/2017


---

# <a name="financial-report-components"></a>Finansinės ataskaitos komponentai

Šiame straipsnyje aprašoma, kaip ataskaitų aprašų komponentai (arba kūrimo blokai) naudojami finansinėse ataskaitose. Šie kūrimo blokai apima eilučių aprašus, stulpelių aprašus ir ataskaitų medžio aprašus. Straipsnis paaiškina, kaip blokus organizuoti ir užrakinti ir kaip naudoti kūrimo blokų grupes. 

Finansinių ataskaitų dizaino įrankio suskaidyti informaciją į mažiausius komponentus ar kūrimo blokus ir tada komponentus pagal poreikį maišyti ir derinti. Todėl ataskaitos formatavimas skiriasi nuo finansinių duomenų formatavimo ir jūs galite pakeisti ataskaitos dizainą nekeisdami finansinių duomenų „Microsoft Dynamics ERP“ sistemoje. Naudodami šį kūrimo bloko metodą galite sujungti tekstą, sumas ir skaičiavimus ir sukurti reikiamas ataskaitas. Be to, šis lankstumas skatina kūrybiškumą, nes galite lengviau skirtingais būdais peržiūrėti operacijas. Atskiri ataskaitos aprašo kūrimo blokai panašūs į trimatę skaičiuoklę, bet turi daugiau galios. Ataskaitos apraše nurodomas eilutės aprašas, stulpelio aprašas ir ataskaitoje naudojamas pasirinktinis medžio aprašas. Jame taip pat pateikiama informacija apie tai, kur saugoti sugeneruotą ataskaitą ir kaip ją formatuoti. Norėdami geresnio pakartotinio naudojimo ir bendrinimo, galite sukurti kūrimo bloko grupę, kuri yra esamų su įmone susijusių ataskaitos aprašų, eilutės aprašų, stulpelio aprašų, ataskaitų medžio aprašų ir dimensijų rinkinių rinkinys.

## <a name="building-blocks-of-a-report"></a>Ataskaitos kūrimo blokai
| Kūrimo blokas            | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                              | Daugiau informacijos                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Eilutės apibrėžimas            | Ataskaitos eilutės apraše apibūdinamos aprašomosios eilutės (pavyzdžiui, atlyginimai arba pardavimai). Jame taip pat pateikiamos segmentų reikšmės arba dimensijos, kuriose yra kiekvienos eilutės elemento reikšmės ir jis apima eilutės formatavimą ir skaičiavimus.                                                    | [Eilutės apibrėžimai](row-definitions-financial-reporting.md)                       |
| Stulpelio aprašas         | Stulpelio apraše nurodomas laikotarpis, kuris turi būti naudojamas išskleidžiant duomenis iš finansinių dimensijų. Jis taip pat apima stulpelio formatavimą ir skaičiavimus.                                                                                                                                 | [Stulpelių apibrėžimai](column-definitions-financial-reports.md)         |
| Ataskaitų medžio apibrėžimas | Ataskaitų medžio apibrėžimas panašus į organizacijos struktūros diagramą. Jame yra atskiri ataskaitų vienetai, kurie atitinka kiekvieną diagramos langelį. Vienetai gali būti atskiri finansinių duomenų padaliniai arba aukštesnio lygio vienetai, kurie apibendrina duomenis iš kitų ataskaitų vienetų. | [Ataskaitų medžio apibrėžimai](financial-reporting-tree-definitions.md) |
| Ataskaitos aprašas         | Ataskaitos apraše naudojamas eilutės apibrėžimas, stulpelio apibrėžimas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio apibrėžimas. Jame taip pat pateikiamos papildomos parinktys ir parametrai, kuriuos galite naudoti ataskaitai tinkinti.                                                                    | [Ataskaitos aprašas](design-financial-report-definitions.md)                  |

Jei ataskaitas kuriate pirmą kartą, naudinga naudoti ataskaitų vedlį, kad galėtumėte greitai sukurti ataskaitos aprašą, kurį vėliau galėsite tinkinti. Jei turite ataskaitų kūrimo patirties ir kurdami ataskaitas norite daugiau lankstumo, galite sujungti naujus arba esamus kūrimo blokus ir sukurti naują ataskaitos aprašą. Norėdami sukurti kokybiškas ataskaitas, jūs neturite visiškai suprasti visų galimų ataskaitos aprašo parinkčių. Kai susipažinsite su ataskaitų kūrimu, galite išplėsti savo ataskaitų apibrėžimus, kad galėtumėte pasinaudoti sudėtingesnėmis funkcijomis. Sukūrę pagrindinę ataskaitą galite tinkinti ataskaitos aprašą ir bet kuriuos ataskaitos aprašo blokus.

## <a name="organize-the-building-blocks"></a>Kūrimo blokų tvarkymas
Norėdami sisteminti savo ataskaitų dizaino įrankio kūrimo blokus, naudokite aplankus. Visi aplankai surūšiuoti pagal juose nurodomą kūrimo bloko tipą. Pavyzdžiui, visi aplankai, kuriuose yra eilučių aprašai, yra ataskaitų dizaino įrankio srityje **Eilučių aprašai**.

### <a name="create-a-folder"></a>Kurti aplanką

1.  Ataskaitų dizaino įrankyje pasirinkite kūrimo bloko tipą, kurį ketinate sisteminti naršymo srityje. Pavyzdžiui, norėdami rūšiuoti eilutės apibrėžimą, spustelėkite **Eilučių apibrėžimai**.
2.  Naršymo srityje pasirinkite esamą aplanką, pagal kurį bus sukurtas naujas aplankas, o tada atlikite vieną iš tolesnių veiksmų.
    -   Dešiniuoju pelės klavišu spustelėkite pradinį aplanką ir tada spustelėkite **Naujas aplankas**.
    -   Pažymėkite pradinį aplanką, spustelėkite **Failas**, o tada spustelėkite **Naujas aplankas**.

3.  Kai bus rodomas naujas aplankas, įveskite naujo aplanko pavadinimą ir tada paspauskite Įvesti.

## <a name="lock-a-building-block"></a>Užrakinti kūrimo bloką
Norėdami apsaugoti ir užrakinti kūrimo bloką, galite sukurti slaptažodį. Tai padarius ataskaitos komponentui pridedamas saugumo lygis, tačiau visa sistema neapsaugoma. Slaptažodžiu galima geriau apsaugoti kūrimo bloko informaciją, kuri yra svarbi jūsų mėnesio pabaigos ataskaitų procesui. Kūrimo bloką gali užrakinti bet kurio vaidmens vartotojas. Tačiau kiti vartotojai visada turės tik skaitymo prieigą prie užrakinto komponento. Vartotojai gali atidaryti, keisti ir įrašyti užrakintą komponentą nauju pavadinimu. Administratoriaus vaidmenį turintis vartotojas visada gali pasiekti ir keisti užrakintą kūrimo bloką.
1.  Ataskaitų dizaino įrankyje atidarykite norimą užrakinti ataskaitos komponentą, pvz., eilutės aprašą, stulpelio aprašą, ataskaitos aprašą arba ataskaitų medžio aprašą.
2.  Meniu **Įrankiai** spustelėkite **Apsaugoti / panaikinti apsaugą**. Taip pat galite spustelėti įrankių juostos (spynos) piktogramą **Apsaugoti / panaikinti apsaugą**.
3.  Dialogo lange **Apsaugoti** įveskite ir patvirtinkite slaptažodį, o tada spustelėkite **Gerai**. Kai atviras kūrimo blokas užrakinamas, įrankių juostos užrakto piktograma paryškinama.

Norėdami atrakinti užrakintą kūrimo bloką, atidarykite kūrimo bloką ir įrankių juostoje spustelėkite piktogramą **Apsaugoti / panaikinti apsaugą**. Arba meniu **Įrankiai** spustelėkite **Panaikinti apsaugą**.

## <a name="building-block-groups"></a>Kūrimo blokų grupės

Kūrimo blokai yra jūsų sukurti ataskaitos eilučių apibrėžimai, stulpelių apibrėžimai, ataskaitų medžio apibrėžimai ir ataskaitų aprašai. Kūrimo bloko grupės yra su įmone susieti apibrėžimų ir dimensijų rinkiniai. Kūrimo blokų grupės gali būti susijusios su konkrečia įmone arba kelios įmonės gali bendrai naudoti tą patį kūrimo blokų rinkinį. Jei turite įmonių, turinčių skirtingus sąskaitų planus, galbūt norėsite kiekvienai įmonei naudoti skirtingą kūrimo blokų grupę. Arba galbūt norėsite pakeisti visų atskirų kūrimo blokų pavadinimus taip, kad būtų matoma, su kuria įmone jie suderinami.
### <a name="create-a-building-block-group"></a>Kūrimo bloko grupės kūrimas

1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo blokų grupės**.
2.  Dialogo lange **Kūrimo blokų grupės** spustelėkite **Nauja**.
3.  Įveskite unikalų kūrimo bloko grupės pavadinimą ir aprašymą. Kiekviename lauke gali būti iki 256 simbolių. (Šis skaičius apima tarpus.)
4.  Norėdami kurti naują kūrimo blokų grupę, spustelėkite **Gerai**.

### <a name="assign-a-building-block-group"></a>Kūrimo bloko grupės priskyrimas

Sukūrę blokų grupę turite ją priskirti bent vienai įmonei. Tada galite kurti ataskaitos, eilutės, stulpelio ir ataskaitų medžio aprašus ir įrašyti juos į kūrimo blokų grupę. Prieš pradėdami toliau nurodytą procedūrą, turite uždaryti visus kūrimo blokus.
1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Įmonės**.
2.  Dialogo lange **Įmonės** pasirinkite įmonę, kuriai norite priskirti kūrimo blokų grupę.
3.  Spustelėkite **Modifikuoti**.
4.  Dialogo lango **Modifikuoti įmonę** lauke **Kūrimo bloko grupė** pasirinkite kūrimo bloko grupę, kurią norite priskirti įmonei, arba spustelėkite **Nauja** ir sukurkite naują kūrimo bloko grupę.
5.  Norėdami proskirti kūrimo bloko grupę, spustelėkite **Gerai**.
6.  Norėdami uždaryti dialogo langą **Įmonės**, spustelėkite **Uždaryti**. Dabar jūsų pasirinkta kūrimo bloko grupė priskiriama įmonei. Dabar visi naujai sukurti eilučių aprašai, stulpelių aprašai ir pan. bus šiai įmonei priskirtos kūrimo blokų grupės dalis. Taip pat galite iš kitos sistemos importuoti .tdbx failą arba ataskaitą.

### <a name="view-a-building-block-group"></a>Kūrimo bloko grupės peržiūra

Kai kūrimo blokų grupė yra sukurta ir naudojama, galite peržiūrėti visus jai priskirtus kūrimo blokus. Taip pat galite eksportuoti arba importuoti kūrimo blokų grupę ir atlikti papildomą kūrimo blokų grupių priežiūrą.
1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo bloko grupės**.
2.  Dialogo lange **Kūrimo bloko grupės** pasirinkite norimą peržiūrėti kūrimo bloką.
3.  Norėdami atidaryti dialogo langą **Kūrimo bloko grupės peržiūra** ir peržiūrėti kūrimo blokų grupės turinį, spustelėkite **Peržiūrėti**.
4.  Norėdami uždaryti dialogo langus, spustelėkite **Uždaryti**.

### <a name="save-a-building-block-group-under-a-new-name"></a>Kūrimo blokų grupę įrašymas naudojant naują pavadinimą

Galite įrašyti esamą kūrimo blokų grupę, naudodami naują pavadinimą. Tada galite modifikuoti naują kūrimo blokų grupę, nekeisdami pradinės kūrimo blokų grupės.
1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo bloko grupės**.
2.  Dialogo lange **Kūrimo bloko grupės** pasirinkite kūrimo blokų grupę, kurią norite įrašyti naudodami naują pavadinimą.
3.  Spustelėkite **Įrašyti kaip**.
4.  Įveskite naują kūrimo bloko grupės pavadinimą ir aprašymą.
5.  Spustelėkite **GERAI**. Nauja kūrimo bloko grupė rodoma dialogo lange **Kūrimo bloko grupės**.

### <a name="export-a-building-block-group"></a>Kūrimo bloko grupės eksportavimas

Galite eksportuoti kūrimo blokų grupę arba konkrečius kūrimo blokų grupės ataskaitos kūrimo blokus. Eksportuotą kūrimo blokų grupę galite naudoti kaip atsarginę kopiją. Taip pat eksportuotus duomenis galite kopijuoti į kitas kūrimo blokų grupes arba „Dynamics 365 for Operations“ programas. Ataskaitų dizaino įrankyje nurodyti šriftų stiliai ir dimensijų rinkiniai pateikiami kartu su kūrimo blokų grupe.
1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo bloko grupės**.
2.  Dialogo lange **Kūrimo bloko grupės** pasirinkite kūrimo bloko grupę, kurią norite eksportuoti, tada spustelėkite **Eksportuoti**.
3.  Dialogo lange **Eksportuoti** pasirinkite norimus eksportuoti ataskaitos aprašus.
    -   Norėdami eksportuoti visus ataskaitos aprašus ir susietus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, spustelėkite atitinkamą skirtuką ir tada pasirinkite norimus eksportuoti elementus. Norėdami skirtuke pasirinkti keletą elementų, paspauskite ir laikykite nuspaudę klavišą CTRL. **Pastaba.** Pažymėjus norimas eksportuoti ataskaitas, pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.

4.  Baigę žymėti norimus eksportuoti elementus, spustelėkite **Eksportuoti**.
5.  Dialogo lange **Įrašyti kaip** pažymėkite vietą, į kurią eksportuoti kūrimo bloko grupę.
6.  Lauke **Failo pavadinimas** įveskite failo pavadinimą. Ataskaitų dizaino įrankis automatiškai įtraukia .tdbx failo vardo plėtinį.
7.  Spustelėkite **Įrašyti**. Kūrimo bloko grupė įrašoma į nurodytą vietą.

### <a name="import-a-building-block-group"></a>Kūrimo bloko grupės importavimas

Galite importuoti kūrimo blokų grupę į esamą kūrimo blokų grupę arba galite sukurti naują duomenų kūrimo blokų grupę. Visos importuotos kūrimo blokų grupės išlaiko savo pradinius šrifto stilius ir įmonės nuorodas bei atitinkamus dimensijų rinkinius.
1.  Ataskaitos dizaino įrankio meniu **Įmonė** spustelėkite **Kūrimo bloko grupės**.
2.  Dialogo lange **Kūrimo bloko grupės** pasirinkite kūrimo bloko grupę, į kurią norite eksportuoti kūrimo bloko grupę, tada spustelėkite **Importuoti**.
3.  Dialogo lange **Atidaryti** pasirinkite kūrimo bloko grupę, kurią norite importuoti, tada spustelėkite **Atidaryti**.
4.  Dialogo lange **Importuoti** pasirinkite norimus importuoti ataskaitos aprašus.
    -   Norėdami importuoti visus ataskaitos aprašus ir palaikomus kūrimo blokus, spustelėkite **Žymėti viską**.
    -   Norėdami importuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite norimas importuoti ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.

5.  Baigę žymėti norimus importuoti elementus, spustelėkite **Importuoti**.

### <a name="undo-a-checkout-of-a-building-block"></a>Anuliuoti kūrimo bloko išregistravimą

Atidarę kūrimo bloką kiti vartotojai gali pasiekti tą kūrimo bloką tik skaitymo režimu. Kartais vartotojai pamiršta uždaryti kūrimo bloką arba išjungia sistemą neuždarę kūrimo bloko. Todėl kūrimo blokas išregistruojamas ir kiti vartotojai negali jo atidaryti. Šiais atvejais finansinių ataskaitų administratorius gali naudoti dialogo langą **Išregistruoti elementai** ir užregistruoti kūrimo blokus, kuriuos vartotojai paliko išregistruotus. **Pastaba.** Norėdami dialogo lange **Išregistruoti elementai** užregistruoti nurodytus kūrimo blokus, turite turėti administratoriaus vaidmenį.
1.  Ataskaitų dizaino įrankio meniu **Įrankiai** spustelėkite **Išregistruoti elementai**.
2.  Dialogo lange **Išregistruoti elementai** pasirinkite **Rodyti visų vartotojų elementus**. Sąrašas atnaujinamas, kad būtų rodomi visi išregistruoti kūrimo blokai ir juos išregistravę vartotojai.
3.  Pasirinkite kūrimo bloką, tada spustelėkite **Anuliuoti išregistravimą**.
4.  Norėdami užregistruoti kūrimo bloką, spustelėkite **Taip**.

# <a name="see-also"></a>Taip pat žiūrėkite

[„Microsoft Dynamics ERP“ finansinės ataskaitos](financial-reporting-intro.md)


