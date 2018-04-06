---
title: "Finansinio laikotarpio uždarymo darbo sritis"
description: "Šiame straipsnyje pateikta Finansinio laikotarpio uždarymo darbo sritis ir susijusi konfigūracija."
author: twheeloc
manager: AnnBe
ms.date: 11/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b999fd3c26304b81f24389a83faf73e1658c39b3
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="financial-period-close-workspace"></a>Finansinio laikotarpio uždarymo darbo sritis

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta Finansinio laikotarpio uždarymo darbo sritis ir susijusi konfigūracija.

Finansinio laikotarpio uždarymo darbo sritis

Naudodamiesi darbo sritimi **Finansinio laikotarpio uždarymas** galite sekti įmonių, sričių ir žmonių finansinius uždarymo procesus. Priklausomai nuo darbo srities **Finansinio laikotarpio uždarymas** rodinio, matote arba visas uždarymo grafiko užduotis ir būsenas, arba tik jums priskirtas užduotis. 

Pirmiausia darbo srities viršuje turite pasirinkti uždarymo grafiką. Tada visi darbo srityje rodomi duomenys filtruojami pagal pasirinktą uždarymo grafiką.

### <a name="summary-tiles"></a>Suvestinės išklotinės

Išklotinėse **Suvestinė** pateikiama proceso apžvalga, o indikatoriai padeda sekti uždarymo procesą. Galite matyti užduotis, kurių terminas praėjęs, likusias šiandienos užduotis, užduotis, kurios turi būti įvykdytos šiandien, bet yra blokuojamos dėl priklausomybių, ir visas kitas proceso užduotis. Ši informacija skirta visoms įmonėms, kurios įtrauktos į pasirinktą uždarymo grafiką.

### <a name="tasks-and-status-section"></a>Užduotys ir būsenos dalis

Skyriuje **Užduotys ir būsena** bendro uždarymo grafiko būsena yra suskaidoma įvairiais būdais: būsena pagal įmonę, būsena pagal sritį ir būseną pagal atsakingą asmenį. Galite peržiūrėti visų uždarymo grafiko užduočių būsenas, tik tų užduočių, kurias reikia atlikti šiandien, arba užduočių, kurios jau turėjo būti atliktos. Taip pat galite pasirinkti įmonės filtrą norėdami peržiūrėti konkrečios įmonės būseną. Kiekviename būsenos skirtuke pateikiamas suskaidymas pagal baigimo procentinę dalį ir likusių užduočių skaičių. Spustelėkite kortelę arba veiksmą **Peržiūrėti išsamią informaciją**, norėdami filtruoti išsamų užduočių sąrašą pagal pasirinktą kortelę. 

Paskutinis skirtukas skirtas išsamiam užduočių sąrašui. Šiame sąraše rodomas visas užduočių sąrašas ir jį galima filtruoti, kad jame būtų rodomos tik jus dominančios užduotys. Užduočių sąrašą galite filtruoti keliais būdais. Pavyzdžiui, galite filtruoti pagal užduoties atlikimo terminą, susijusią įmonę ir susijusią sritį. Taip pat galite pasirinkti, ar atliktos užduotys užduočių sąraše bus rodomos, ar slepiamos. 

Naudojami du užduočių indikatoriai:

-   Šauktuko piktograma nurodo, kad užduotis jau turėjo būti įvykdyta. Užduočių, kurios jau turėjo būti įvykdytos, terminas taip pat paryškintas raudonai.
-   Spynos piktograma nurodo, kad užduotis priklauso nuo kitų užduočių, kurios dar neatliktos. Priklausomybių blokuojamos užduoties negalima pažymėti kaip atliktos. Užduoties priklausomybes galite nustatyti naudodami veiksmą **Nustatyti priklausomybę**.

Užduoties pavadinimas yra nuorodą į „Microsoft Dynamics 365 for Operations“ puslapį arba kitą tinklalapį, kuriame turi apsilankyti vartotojas, norėdamas užbaigti darbą. Šią nuorodą galite nustatyti užduoties redagavimui arba kūrimui naudodami lauką **Užduoties saitas**. 

Naudodami veiksmą **Priedai** prie užduoties galite pridėti failus, pastabas, vaizdus ir URL. Pvz., galite nurodyti kaip užduoties dalis naudojamų žurnalų numerius, įtraukti komentarų apie konkrečią užduotį arba pridėti atspausdintą užduoties ataskaitos failą. Jei esama priedo, užduoties stulpelyje **Priedas** atsiranda piktograma. 

Atlikus užduotį būtina rankiniu būdu pasirinkti pasirinktį **Užduotis baigta**. Kai užduotis pažymėta kaip baigta, laukas **Baigimo data** atnaujinamas automatiškai, nurodant dabartinę datą ir laiką. Atitinkamai atnaujinami ir priklausomybės indikatoriai.

## <a name="all-financial-period-close-tasks-list-page"></a>Visų finansinio laikotarpio uždarymo užduočių sąrašo puslapis
Sąrašo puslapyje **Visos finansinio laikotarpio uždarymo užduotys** galite peržiūrėti visas dabartinio ir ankstesnio laikotarpio uždarymo užduotis. Šį puslapį geriausia naudoti jūsų uždarymo proceso istorinei analizei, nes jame pateikiama informacija apie numatytą atlikimo terminą, faktinę baigimo datą ir užduotį atlikusį asmenį. Teikdami ataskaitas ir atlikdami patikrinimus šiame sąrašo puslapyje pateikiamą informaciją galite lengvai eksportuoti į „Microsoft Excel“.

## <a name="financial-period-close-configuration-page"></a>Finansinio laikotarpio uždarymo konfigūracijos puslapis
Prieš naudodami darbo sritį **Finansinio laikotarpio uždarymas**, turite sukonfigūruoti „Microsoft Dynamics 365 for Finance and Operations“ procesą, naudodami puslapį **Finansinio laikotarpio uždarymo konfigūracija**. (Spustelėkite **Didžioji knyga** &gt; **Laikotarpio uždarymas** &gt; **Finansinio laikotarpio uždarymo konfigūracija.**)

### <a name="resources"></a>Ištekliai

Skirtuke **Ištekliai** nurodote asmenis, kurie dalyvauja uždarymo procese. Bet koks už uždarymo užduotį atsakingas darbuotojas pirmiausia turi būti priskirtas čia. Taip pat turite nurodyti darbuotojo darbo srities rodinį. Galimos toliau nurodytos pasirinktys:

-   **Tik priskirtos užduotys** – vartotojas matys tik jam arba jai priskirtas užduotis.
-   **Visos užduotys ir būsena** – vartotojas matys visas uždarymo užduotis ir viso proceso būseną.

Vartotojai, kurie turi teisę peržiūrėti tik jiems priskirtas užduotis, negalės įtraukti užduočių į užduočių sąrašą, redaguoti užduočių arba pašalinti užduočių iš užduočių sąrašo.

### <a name="task-areas"></a>Užduočių sritys

Naudokite užduočių sritis, norėdami grupuoti savo organizacijos uždarymo užduotis į logines nuosavybės sritis. Pavyzdžiui, kaip užduočių sritis galima naudoti Mokėtinos sumos, Gautinos sumos arba Didžioji knyga.

### <a name="calendars"></a>Kalendoriai

Kurkite ir redaguokite finansinius uždarymo kalendorius naudodami skirtuką Kalendoriai. Juose nurodysite uždarymo procesų darbo dienas ir jie bus naudojami planuojant uždarymo užduotis.  Sukurkite naują kalendorių ir nurodykite darbo dienas, kurios bus naudojamos planuojant užduotis.  Geriausia sukurti kalendorių ilgam laikotarpiui, pvz., metams ar keliems metams, nes sukūrus jį galima redaguoti.  Sukūrę kalendorių, spustelėkite mygtuką Redaguoti, kad galėtumėte jį atnaujinti, pažymėdami konkrečias dienas, pvz., šventes.  Uždarymo užduotis bus planuojama atlikti tomis dienomis, kai nustatyta dalies Valdymas reikšmė Atvira.  Jei uždarymo užduotys neturėtų būti planuojamos tam tikrai dienai, turėtų būti nustatyta tos dienos dalies Valdymas reikšmė Uždaryta.

### <a name="templates"></a>Šablonai

Norėdami apibrėžti visas užduotis, kurios yra uždarymo proceso dalis, naudojate finansinio uždarymo šabloną. Uždarymo užduotis yra pasikartojanti darbo pastanga, kuri priskiriama asmeniui ir atliekama kaip kiekvieno uždarymo proceso dalis. Šablone turi būti nurodytas kiekvienos uždarymo užduoties santykinis terminas. Uždarymo užduotis yra pasikartojanti darbo pastanga, kuri priskiriama asmeniui ir atliekama kaip kiekvieno uždarymo proceso dalis. Termino laikas priskiriamas ir kiekvienai užduočiai. Termino laikas nustatomas naudojant jūsų laiko juostos kontekstą ir jis bus konvertuotas į kiekvieno vartotojo laiko juostos laiką. 

Galite priskirti šablono užduotį vienai arba kelioms įmonėms, kuriose ta užduotis taikoma. Jei kiekvienos įmonės tai darbo pastangai atlikti priskiriamas kitas asmuo, gali būti naudinga sukurti kelias tos pačios darbo pastangos užduotis. Sukurkite po vieną užduotį kiekvienai įmonei. 

Meniu elementas **Užduoties saitas** susietas su užduoties darbo pastanga ir gali būti naudojamas norint pereiti iš darbo srities užduoties saito tiesiogiai į susietą puslapį. Pvz., uždarymo užduotis, skirta vykdyti mokėtinų sumų valiutos perkainojimo procesą, gali būti susijusi su susietu „Microsoft Dynamics 365 for Finance and Operations“ puslapiu **Užsienio valiutos kurso pasikeitimas**. Taip pat galite susieti su išoriniu URL. 

> [!TIP]
> Jei norite susieti konkrečią „Management Reporter“ ataskaitą su finansinio laikotarpio uždarymo užduotimi, galite naudoti ataskaitos URL. Norėdami pasiekti ataskaitų URL, atidarykite ataskaitą naudodami ataskaitų dizaino įrankį, tada spustelėkite **Failas** &gt; **Peržiūrėti ataskaitą** ir atidarykite ataskaitą žiniatinklio naršyklėje. Galite nukopijuoti naršyklės adreso juostoje esantį URL ir įklijuoti jį į lauką **Užduoties saitas** **URL**. 

Šablone galite nurodyti užduoties priklausomybes. Jei nustatyta, kad užduotis priklausoma nuo vienos ar kelių užduočių, tos užduoties negalima pažymėti kaip baigtos, kol neįvykdytos visos priklausomybės. 

Galite sukurti kelis finansinio uždarymo šablonus. Tada, naudodami įvairius šablonus, galite sekti skirtingų laikotarpių tipų, pvz., mėnesio pabaigos arba metų pabaigos, uždarymo procesus arba galite sekti įmones, kurios naudoja skirtingus uždarymo procesus. Sukūrę vieną šabloną galite jį kopijuoti ir sukurti naują šabloną ir atlikti reikiamus pakeitimus. Kiekvienam uždarymo grafikui galite priskirti tik po vieną šabloną.

### <a name="closing-schedules"></a>Uždarymo grafikai

Norėdami priskirti finansinio uždarymo šabloną konkrečiam ataskaitiniam laikotarpiui, kuris turėtų būti uždaromas, naudokite uždarymo grafiką. Tada automatiškai sugeneruojamos konkretaus laikotarpio šablono užduotys, o naujas uždarymo grafikas įtraukiamas į darbo sritį. Kai sukuriate naują uždarymo grafiką, laukas **Laikotarpio pabaigos data** naudojamas norint nustatyti faktinius uždarymo užduočių terminus pagal finansinio uždarymo šablone priskirtą santykinį terminą. 

Nustatykite, kad pagal uždarymo grafiką tinkamame kalendoriuje būtų nurodomos dienos, kurios bus naudojamos planuojant užduotis. Jeigu nenurodysite konkretaus kalendoriaus, užduočių terminai naudos visas savaitės dienas. 

Taip pat turite nurodyti įmones, kurios bus susietos su uždarymo grafiku. Jei šablono užduotys priskiriamos kelioms įmonėms, kiekvienai uždarymo grafike nurodytai įmonei bus sukurtos atskiros užduotys ir priskirtos šablono užduočiai. 

Įvykdę uždarymo grafiką pažymėkite parinktį **Uždaryta**. Užduoties retrospektyvą bus galima rasti sąrašo puslapyje **Visos ataskaitinio laikotarpio uždarymo užduotys**, bet uždarymo grafikas bus pašalintas iš darbo srities. Kai pažymima uždarymo grafiko parinktis **Uždaryta**, į jį negalima įtraukti užduočių, negalima redaguoti užduočių ir negalima užduočių iš jo pašalinti.




