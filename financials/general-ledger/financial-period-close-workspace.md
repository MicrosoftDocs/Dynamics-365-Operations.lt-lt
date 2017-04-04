---
title: "Finansinio laikotarpio uždarymo darbo sritis"
description: "Šiame straipsnyje pateikta Finansinio laikotarpio uždarymo darbo sritis ir susijusi konfigūracija."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Finansinio laikotarpio uždarymo darbo sritis

Šiame straipsnyje pateikta Finansinio laikotarpio uždarymo darbo sritis ir susijusi konfigūracija.

Finansinio laikotarpio uždarymo darbo sritis

Į **finansiniam laikotarpiui uždaryti** darbo sritis leidžia stebėti jūsų finansų uždarymo procesus kompanijų, srityse, ir žmonės. Priklauso nuo jūsų nuomone, kad **finansiniam laikotarpiui uždaryti** darbo srities, matysite arba užduočių ir uždarymo grafiką arba tik užduotys, kurie yra jums priskirti būsenos. 

Pirmiausia turite pasirinkti uždarymo grafiką darbo srities viršuje. Tada visi duomenys, kurie yra rodomas darbo srities nufiltruota pagal pasirinktą uždarymo grafiką.

### <a name="summary-tiles"></a>Suvestinės išklotinės

Išklotinėse **Suvestinė** pateikiama proceso apžvalga, o indikatoriai padeda sekti uždarymo procesą. Galite peržiūrėti užduotis, kurios yra praeities apmokamos, likusius užduotis šiandien, užduočių, kurios turi būti užsakytas, bet yra užblokuotas, nes priklausomybes ir visus likusius užduotis procesui. Ši informacija skirta visoms bendrovėms, kurios yra įtrauktos į pasirinktą uždarymo grafiką.

### <a name="tasks-and-status-section"></a>Užduotys ir būsenos dalis

– Į **užduotis ir statuso** skyriuje, bendras statusas uždarymo planas yra suskirstytas įvairiais būdais: statusą iš įmonės, statuso pagal vietą ir būseną iš atsakingo asmens. Būseną galite peržiūrėti už visas užduotis uždaryti planuoti, tiesiog užduočių, kurias reikia šiandien, ar užduotis yra pradelstas keisdami filtro kortelės sąrašo viršuje. Taip pat galite pasirinkti įmonės filtrą norėdami Rodyti programos būseną konkrečią įmonę. Kiekviename skirtuke statusas suteikia suskirstymą pagal procentas, kuris bus baigta ir užduočių, kurios lieka skaičius. Spustelėkite kortelę, arba **peržiūrėti informaciją apie** veiksmų ir išsamios užduočių sąrašo pasirinktą kortele. 

Paskutinis skirtukas yra išsamios užduočių sąrašą. Šis sąrašas rodo visą užduočių sąrašą ir gali būti filtruojamas, taip, kad tik užduotis, kurios jus domina. Galite filtruoti užduočių sąraše keliais būdais. Pvz., galite filtruoti pagal užduoties terminas, asocijuotos bendrovės, ir susijusias sritis. Taip pat galite pasirinkti Rodyti arba slėpti užduočių sąraše atliktas užduotis. 

Naudojami du užduočių indikatoriai:

-   Šauktuko piktograma nurodo, kad užduotis yra pradelstas. Užduotis, kurios yra pradelstos, terminas taip pat yra paryškinta raudona spalva.
-   Spynos piktograma rodo, kad užduotis priklauso nuo kitų užduočių, kurios dar nėra baigtas. Užduotis, kurios yra blokuojami iš priklausomybių negalima pažymėti kaip atliktą. Priklausomybių užduotį galite nustatyti naudodami prie **nustatyti priklausomybės** veiksmų.

Užduoties pavadinimas yra nuorodą į "Microsoft Dynamics 365" operacijų puslapį arba kitą tinklalapį tais atvejais, kai vartotojas turi eiti į užbaigti darbus. Šią nuorodą galite nustatyti naudodami, **užduotis nuoroda** lauko redaguoti ar sukurti užduotį. 

Failai, pastabos, vaizdus ir URL galite pridėti užduotį naudojant į **priedai** veiksmų. Pvz., galite nurodyti žurnalo numerius, kurie yra naudojami kaip dalis užduoties, pridėti komentarus apie tam tikrą užduotį arba pridėti ataskaitų failas, kuris buvo atspausdintas užduotis. Pasirodo piktograma su **priedą** stulpelio užduotis, jei priedas yra. 

Į **užduočiai užbaigti** variantas turi būti rankiniu būdu pasirinktas po užduoties atlikimo. Kai užduotis yra pažymėti kaip atliktą, kad **baigė data** laukas atnaujinamas automatiškai dabartinę datą ir laiką. Atitinkamai atnaujinami priklausomumo rodiklius.

## <a name="all-financial-period-close-tasks-list-page"></a>Visų finansinio laikotarpio uždarymo užduočių sąrašo puslapis
Jūs galite peržiūrėti visus dabartinius ir ankstesnius laikotarpio glaudžiai užduotis iš į **visus finansiniam laikotarpiui uždaryti užduočių** sąrašo puslapį. Šis sąrašas puslapis yra geriausia naudoti istorinė analizė jūsų uždarymo proceso, nes jame yra informacija apie reguliaraus terminas, faktinės įvykdymo datos, ir asmuo, kuris baigė užduotį. Lengvai informaciją šiame sąraše puslapyje galite eksportuoti į programą Microsoft Excel ataskaitų ir audito tikslais.

## <a name="financial-period-close-configuration-page"></a>Finansinio laikotarpio uždarymo konfigūracijos puslapis
Prieš naudodami, **finansiniam laikotarpiui uždaryti** darbo sritį, turite sukonfigūruoti šį procesą Microsoft Dynamics 365 operacijoms naudojant į **finansinio laikotarpio uždaryti konfigūracijos** puslapis. (Spustelėkite **bendrosios knygos**&gt;**laikotarpiui uždaryti**&gt;**finansinio laikotarpio uždaryti konfigūracijos**.)

### <a name="resources"></a>Ištekliai

Dėl to **išteklių** pažymėtame lape galite nustatyti žmonės, kurie yra įtraukti į uždarymo procesus. Bet kuris darbuotojas, kuris bus atsakingas už uždarymo užduotis pirmiausia turi būti priskirtas čia. Taip pat turite nurodyti darbuotojo darbo srities vaizdas. Galimos toliau nurodytos pasirinktys:

-   **Tik priskirtos užduotys** – vartotojas matys tik jam arba jai priskirtas užduotis.
-   **Visos užduotys ir būsena** – vartotojas matys visas uždarymo užduotis ir viso proceso būseną.

Vartotojai, kurie turi teisę peržiūrėti tik jiems priskirtas užduotis, negalės įtraukti užduočių į užduočių sąrašą, redaguoti užduočių arba pašalinti užduočių iš užduočių sąrašo.

### <a name="task-areas"></a>Užduočių sritys

Naudokite užduočių sritis, norėdami grupuoti savo organizacijos uždarymo užduotis į logines nuosavybės sritis. Pavyzdžiui, kaip užduočių sritis galima naudoti Mokėtinos sumos, Gautinos sumos arba Didžioji knyga.

### <a name="calendars"></a>Kalendoriai

Kurkite ir redaguokite finansų uždarymo kalendorių naudodami skirtuką kalendorius.  Tai kur jums bus apibrėžti darbo dienų uždarymo procesus, ir bus naudojamas paskutinės užduočių planavimo.  Sukurti naują kalendorių ir rodo dienas naudoti užduočių planavimo.  Tai geriausia sukurti kalendorių ilgą laiką, pvz., metus ar keletą metų, nes ji gali būti redaguojama po sukūrimo.  Sukūrus kalendorių, spustelėkite mygtuką Redaguoti, atnaujinti kalendoriaus konkrečias dienas, pvz., šventes.  Tomis dienomis, kai kontrolinė vertė yra nustatyta atviros uždarymo užduotys bus planuojamos.  Jei uždarymo užduotis neturėtų būti tvarkaraštį konkrečią dieną, tą dieną turėtų turėti kontrolės reikšmė nustatyta kaip uždaryta.

### <a name="templates"></a>Šablonai

Galite naudoti finansų glaudžiai šabloną apibrėžti visas užduotis, kurios yra uždarymo proceso dalis. Uždarymo užduotis yra pasikartojančių darbo pastangų, kuris priskiriamas individualus užbaigti kiekvieną uždarymo proceso dalis. Šablone, santykinis išsamaus patikrinimo data turi būti nustatyta užduoties uždarymo. Tą santykinę termino data yra dienų prieš skaičių ar po apibrėžta laikotarpio pabaigos datos, užduotis nebus skaičiuojami kiekvienam laikotarpiui. Laiku taip pat priskiriama kiekvienai užduočiai. Laiku yra nustatyti atsižvelgiant į laiko juostą ir bus konvertuoti į laiko juostą kiekvienam vartotojui. 

Užduotį šablone galite priskirti vieną ar daugiau bendrovių, kai taikoma šiai užduočiai atlikti. Jei tas pats asmuo priskiriamas užbaigti šio darbo pastangų kiekvienoje įmonėje, jūs galbūt bus naudinga sukurti kelias užduotis dėl paties darbo pastangų. Sukurkite po vieną užduotį kiekvienai įmonei. 

Į **užduotis nuoroda** meniu elementas yra susietas su užduočių darbo pastangų ir galima eiti tiesiai į susijęs puslapis iš užduočių link darbo srityje. Pvz., uždarymo užduotis būtų vykdoma valiutos perkainojimo procesas mokėtinos sąskaitos gali būti susietos su atitinkamais **valiutos kurso** puslapio dalyje Microsoft Dynamics 365 operacijoms. Taip pat galite susieti su išoriniu URL. 

> [! Patarimas] Jei norite susieti konkrečią valdymo reporteris ataskaitą finansinio laikotarpio uždaryti užduotį, galite naudoti ataskaitą URL. Norėdami atidaryti ataskaitos URL, atidarykite ataskaitą į ataskaitų konstruktorius, o tada spustelėkite **failo**&gt;**peržiūrėti ataskaitą** atidaryti pranešimą naudodami žiniatinklio naršyklę. Galite nukopijuoti naršyklės adreso juostoje esantį URL ir įklijuoti jį į lauką **Užduoties saitas** **URL**. 

Galite apibrėžti užduočių priklausomybes šabloną. Jei užduotis buvo nustatyta priklauso nuo vieno ar daugiau užduočių, tą užduotį negali būti pažymėtas kaip tol, kol nebus įvykdyti visas priklausomybes. 

Galite sukurti kelis finansinių glaudžiai šablonai. Tada galite naudoti įvairius šablonus, sekti uždarymo procesus laikotarpio įvairių, pvz., mėnesio pabaigoje arba metų pabaigoje, arba sekti įmonės, kurios naudojasi skirtingais uždarymo procesus. Sukūrus vieną šabloną, galite kopijuoti į naują šabloną ir atlikite reikiamus keitimus. Galite priskirti vieną šabloną kiekvienam uždarymo grafiką.

### <a name="closing-schedules"></a>Uždarymo grafikai

Galite naudoti uždarymo grafiką finansų glaudžiai šabloną priskirti konkretų finansinį laikotarpį, turi būti uždarytas. Užduotis iš šablono, tada automatiškai sugeneruotas per nustatyt ą, o naujas uždarymo tvarkaraštis pridedamas prie darbų srities. Kai kuriate naują uždarymo grafiką, su **laikotarpio pabaigos data** laukas naudojamas nustatyti faktinį tinkamai uždarymo užduotis, remiantis santykine termino datos dieną, kurią priskiriamas finansinės glaudžiai šablone. 

Priskirti tinka uždarymo grafiką, nurodyti darbo dienas naudoti užduočių planavimo kalendorius. Jei negalima nustatyti konkrečių kalendorinių, užduotis dėl datos bus naudoti visų savaitės dienų. 

Taip pat turite nustatyti bendrovėms, kurios bus susietas su uždarymo grafiką. Jei šablono užduotys priskiriamos kelios įmonės, atskiras užduotis bus sukurti kiekvienos įmonės, kuri yra uždarymo grafiką ir šablono užduoties. 

Po uždarymo planas bus baigtas, pasirinkite, **uždaryta** variantą už jį. Užduočių retrospektyva bus pasiekiamas iš į **visus finansiniam laikotarpiui uždaryti užduočių** sąrašo puslapį, tačiau uždarymo planas bus pašalintas iš darbo srities. Po uždarymo grafiką buvo pažymėtas kaip **uždaryta**, jūs negalėsite pridėti užduotis jai, redaguoti užduotis arba užduotis pašalinti iš jo.


