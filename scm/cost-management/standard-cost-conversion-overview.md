---
title: "Standartinių išlaidų konvertavimo peržiūra"
description: "Šiame straipsnyje apžvelgiami procesai, padėsiantys nustatyti ir vykdyti standartinių išlaidų konvertavimą. Išvardytus veiksmus reikia atlikti įvykdžius būtinąsias standartinių išlaidų konvertavimo sąlygas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8b13d734c22203618183b8855f99da8e51114f76
ms.lasthandoff: 03/31/2017


---

# <a name="standard-cost-conversion-overview"></a>Standartinių išlaidų konvertavimo peržiūra

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiami procesai, padėsiantys nustatyti ir vykdyti standartinių išlaidų konvertavimą. Išvardytus veiksmus reikia atlikti įvykdžius būtinąsias standartinių išlaidų konvertavimo sąlygas. 

Norėdami konvertuoti pasirinktų prekių paketo atsargų modelį iš faktinių išlaidų būdo į standartinį įkainojimo būdą, naudokite puslapį **Standartinių išlaidų konvertavimas**. Konvertavimo procesas apima būtiną atsargų uždarymą, kelis veiksmus perėjimo laikotarpiu (kurį nusako perėjimo pradžios data ir planuojama konvertavimo data) ir konvertavimą bei susijusių atsargų uždarymą.

-   Atsargų uždarymas prieš perėjimo laikotarpį – Atsargų uždarymas atitinka būtinuosius žingsnius, nes jis sudengia naudojant seną vertinimo metodą pradėtas prekės operacijas. Perėjimo laikotarpiu galite įvesti ir įregistruoti operacijas atgaline data, pvz., SF, kad galėtumėte uždaryti ankstesnį laikotarpį. Atsargų uždarymo data turi būti viena diena prieš perėjimo pradžios datą, kad būtų užtikrinamas sklandus atskyrimas nuo senojo vertinimo metodo.
-   Konvertavimo veiksmai perėjimo laikotarpiu − naudokite puslapį **Standartinių išlaidų konvertavimai** norėdami sukurti konvertavimo įrašą, kuriame taip pat būtų vartotojo nustatytas identifikatorius naujai įkainojimo versijai. Nurodykite prekes, kurias reikia konvertuoti, ir įveskite tos prekės laukiančias standartines išlaidas į naująją įkainojimo versiją. Atlikite pasirinktų prekių patikrinimą, siekdami nustatyti problemas, kurios gali trukdyti konvertuoti, išspręskite problema ir atlikite kitą tikrinimą. Po to, kai prekės buvo sėkmingai patikrintos, konvertavimo įrašo būseną pakeičiate į **Paruošta**. Suplanuotą konvertavimo dieną atlikite konvertavimą ir, jei norite, įtraukite atsargų uždarymą. Perėjimo laikotarpiu prekės atsargų perkėlimas registruojamas ir įvertinamas pagal senąjį atsargų modelį. Tada, sėkmingai konvertavus, atsargų perkėlimas perkainojamas į standartines išlaidas.
-   Atsargų uždarymas prieš konvertavimą – atsargų uždarymas gali būti įtrauktas kaip konvertavimo suplanuotą konvertavimo dieną dalis arba jis gali būti atliekamas kaip atskiras išankstinis veiksmas.

Sėkmingai atlikus konvertavimo procesą kiekvienos prekės atsargų modelis bus paremtas standartinėmis išlaidomis ir bus įgalintos prekės standartinės išlaidos. Tolesnės atsargų operacijos bus įkainojamos pagal standartines prekės išlaidas. Be to, sistema konvertuoja faktinių prekės atsargų gavimo ir išdavimo operacijas į standartines išlaidas pagal konvertavimo datą. Sistema taip pat konvertuoja turimas prekės finansines atsargas pagal standartines išlaidas ir registruoja vertės skirtumus kaip atsargų perkainojimą. Visos po konvertavimo atliekamos operacijos vertinamos pagal prekės standartines išlaidas. Negalėsite įvesti operacijų atgaline data prieš konvertavimo dieną, nes atsargų uždarymas turi būti atliktas dieną prieš konvertavimo datą. Tai yra, konvertavimas gali būti atliktas, jei atsargų uždarymas buvo įvykdytas vieną dieną anksčiau. Šis atsargų uždarymas negali būti atšauktas.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Apibrėžkite standartinių išlaidų konvertavimo įrašą ir susijusią įkainojimo versiją.
Norėdami sukurti konvertavimo įrašą naudokite puslapį **Standartinių išlaidų konvertavimas**. Naują konvertavimo įrašą galite sukurti tik kai esantys konvertavimo įrašai yra užbaigti. Suplanuoto perėjimo laikotarpio trukmė yra apibrėžta pagal perėjimo pradžios datą ir suplanuotą konvertavimo datą. Suplanuotas perėjimo laikotarpis gali trukti tik vieną dieną. Suplanuotas perėjimo laikotarpis padeda užtikrinti, kad užteks laiko atlikti visiems konvertavimo proceso veiksmams. Atsargų uždarymas turi būti atliktas vieną dieną prieš perėjimo pradžią, kad sudengimai būtų tikrai baigti prieš jums pradedant konvertavimo procesą. Norėdami užtikrinti, kad teisingai sulygiuotos perėjimo pradžios data ir atsargų uždarymo data, galite arba pakeisti perėjimo pradžios datą į vieną dieną po esamo atsargų uždarymo, arba atlikti atsargų uždarymą. Įvesdami konvertavimo įrašą, taip pat įvesite vartotojų apibrėžiamą identifikatorių naujai įkainojimo versijai, kurioje bus konvertuotų prekių standartinės išlaidos. Įkainojimo versija sugeneruojama automatiškai, jums įrašius konvertavimo įrašą.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Naujosios konvertavimo įrašo įkainojimo versijos peržiūra ir keitimas
Naujoji įkainojimo versija yra skirta konvertavimo įrašui, kaip nurodo įkainojimo tipas **Konvertavimas**. Skirtoji įkainojimo versija panaši į standartinių išlaidų įkainojimo versiją ir joje yra prekių, kurios susietos su konvertavimo įrašu, išlaidų įrašai. Skirtoji konvertavimo įrašo įkainojimo versija turi tolesnius parametrus, kuriuos pagal poreikį reikėtų peržiūrėti ir modifikuoti įvairiuose skirtukuose.

-   **Įkainojimo tipas.** Šis laukas turėtų būti nustatytas į **Standartinės išlaidos**.
-   **Versija.** Identifikatorius rodo informaciją, kuri yra įvesta įkainojimo versijos ID konvertavimo įraše.
-   **Vardas (pavadinimas).** Pagal numatytuosius parametrus vardas (pavadinimas) yra tuščias. Jei reikia, galite vardą (pavadinimą) įvesti.
-   **Blokuoti.** Šis laukas turėtų būti nustatytas į **Ne**. Galite įvesti išlaidų įrašus į įkainojimo versiją tol, kol konvertavimo būseną pakeičiate į **Paruošta**. Būsena **Paruošta** nurodo, kad pasirinktos prekės buvo patikrintos ir kad išlaidų įrašų pakeitimai neturėtų būti leidžiami.
-   **Blokuoti aktyvinimą.** Šis laukas turėtų būti nustatytas į **Taip**. Negalite rankiniu būdu suaktyvinti būsimo skirtosios įkainojimo versijos išlaidų įrašo. Aktyvinimas vyksta, kai atliekate konvertavimą.
-   **Pradžios data.** Pradžios data rodo suplanuotą konvertavimo datą, kuri yra įvesta konvertavimo įraše.
-   **Vieta.** Šį lauką palikite tuščią, kad būtų galima įvesti bet kokios vietos išlaidų įrašus.
-   **Leisti kainų tipų laukų grupę.** Šį lauką nustatykite į **Taip**, kad būtų galima įvesti tik savikainos įrašus.
-   **Atsarginis principas.** Šis laukas nustatytas į **Nėra**. Atsarginį principą pakeiskite į **Aktyvus**, jei reikia išlaidų informacijos, kuri buvo suaktyvinta kitose įkainojimo versijose. Pavyzdžiui, išlaidų informacijos apie komponentus, išlaidų kategorijas ir netiesiogines išlaidas gali reikėti norint apskaičiuoti pagamintų prekių išlaidas.
-   **Atsarginė įkainojimo versija.** Šį lauką palikite tuščią.

Prekės išlaidų informacija, esanti skirtojoje įkainojimo versijoje, gali būti tvarkoma tik iš puslapio **Standartinių išlaidų konvertavimas**. Konvertavimo metu norėdami apskaičiuoti įkainojimo versijos išlaidas, puslapių **Įkainojimo versijos nustatymas** ir **Įkainojimo versijos tvarkymas** naudoti negalite. Tačiau tvarkyti skirtąją įkainojimo versiją naudodami šiuos puslapius galite atlikę konvertavimo procesą.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Prekių, konvertuotinų į standartines išlaidas, identifikavimas
Norėdami identifikuoti atskiras prekes, kurias reikėtų konvertuoti į standartines išlaidas, naudokite puslapį **Standartinių išlaidų konvertavimas**. Naudodami puslapį **Prekių įtraukimas į standartinių išlaidų konvertavimą**, galite įtraukti kelias prekes. Apskritai visas pagamintas prekes reikėtų įtraukti į vieną konvertavimo įrašą, kad išlaidos būtų tikrai apskaičiuojamos teisingai.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Kiekvienos konvertuojamos prekės būsimų standartinių išlaidų įvedimas ar apskaičiavimas
Naudokite puslapį **Prekės kaina**, norėdami įvesti būsimas standartines išlaidas nupirktų ir perkeltų prekių skirtojoje įkainojimo versijoje. Išlaidų įrašai yra būdingi tam tikrai teritorijai ir būsimos prekės išlaidos turi būti įvestos kiekvienai teritorijai. Naudokite puslapį **Prekės kaina**, norėdami apskaičiuoti pagamintų prekių būsimas standartines išlaidas. Pagamintos prekės būsimos išlaidos turi būti apskaičiuojamos kiekvienai gaminimo vietai, nebent vieta yra perkėlimo vieta. Tokiu atveju būsimas išlaidas reikėtų įvesti rankiniu būdu. Kai kurios prekės gali turėti produkto spalvos, dydžio ar konfigūracijos dimensijų. Puslapyje **Standartinių išlaidų konvertavimas** žymės langelis **Naudoti savikainą pagal variantus** rodo kiekvienos produktų dimensijų kombinacijos standartines išlaidas. Kai šis žymės langelis išvalytas, jums reikia įvesti tik būsimas prekės išlaidas.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Bet kokių su konvertuojamomis prekėmis susijusių problemų patikra ir sprendimas
Norėdami identifikuoti su konvertuojamomis prekėmis susijusias problemas, naudokite ataskaitą **Standartinių išlaidų konvertavimo tikrinimai**. Jei su preke susijusių problemų nėra, jos būsena konvertavimo įraše pakeičiama į **Patikrinta**. Jei su preke susijusių problemų yra, turite jas išspręsti ir tada vėl paleisti ataskaitą, kol prekės būsena pasikeis į **Patikrinta**. Jei negalite išspręsti problemos laiku, galite prekę ištrinti iš konvertavimo įrašo ir ją konvertuoti vėliau.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Konvertavimo įrašo būsenos pakeitimas į Paruošta
Kai konvertavimo įrašo būsena pakeičiama į **Paruošta**, prieš paleisdama standartinių išlaidų konvertavimą sistema atlieka galutinį tikrinimą. Būsena pakeičiama į **Paruošta** tik jei įvykdytos tolesnės sąlygos.

-   Visų konvertavimo įrašo prekių būsena yra **Patikrinta**.
-   Atsargų uždarymas buvo atliktas dieną prieš perėjimo pradžią. Norėdami užtikrinti, kad teisingai sulygiuotos perėjimo pradžios data ir atsargų uždarymo data, galite arba pakeisti perėjimo pradžios datą į vieną dieną po esamo atsargų uždarymo, arba atlikti atsargų uždarymą.

## <a name="7-back-up-the-database-before-conversion"></a>7. Duomenų bazės atsarginės kopijos sukūrimas prieš konvertavimą
Atsarginė kopija leidžia atkurti duomenų bazę, jei konvertavimo metu įvyktų klaidų.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Konvertavimas, kai konvertavimo įrašo būsena yra Paruošta
Norint atlikti konvertavimo procesą, reikia, kad atsargų uždarymas būtų atliktas vieną dieną prieš suplanuotą konvertavimą. Šiuo reikalavimu padedama užtikrinti, kad perėjimo laikotarpiu nebūtų galima įvesti atgaline data registruotų operacijų. Jei atsargų uždarymas dar neatliktas, jūsų paklaus, ar norite jį atlikti kaip konvertavimo proceso dalį. Konvertavimo procesas vienu metu tvarko vieną prekę. Pradedama nuo žemiausių produktų struktūros prekių, atsižvelgiant į prekės žemo lygio kodą. Kai prekė sėkmingai konvertuota, jos būsena konvertavimo įraše pakeičiama į **Konvertuota**. Jei konvertavimo procesas nutraukiamas, visų prekių, kurios nebuvo sėkmingai konvertuotos, būsena vis tiek bus **Patikrinta**. Sėkmingai baigus konvertavimo procesą atliekami tolesni veiksmai.

-   Konvertavimo įrašo būsena iš **Paruošta** pakeičiama į **Baigta**, o kiekvienos pasirinktos prekės būsena iš **Patikrinta** pakeičiama į **Konvertuota**.
-   Pakeičiama konvertuotų prekių modelių grupė, kad atspindėtų naują grupę su standartinių išlaidų atsargų modeliu.
-   Standartinės konvertuotų prekių išlaidos įgalintos skirtojoje įkainojimo versijoje.
-   Įkainojimo versijos įkainojimo tipas iš **Konvertavimas** pakeičiamas į **Standartinės išlaidos** ir įkainojimo versija dabar yra tokia pat kaip kitos standartinių išlaidų įkainojimo versijos.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Konvertuotų prekių atsargų verčių tikrinimas ir derinimas
Ataskaita **Nuokrypių analizės išrašas** leidžia analizuoti perkainojimo nuokrypį, o ataskaita **Atsargų vertė** leidžia peržiūrėti konkrečios datos atsargų vertę.

-   Analizuokite perkainojimo nukrypimus. Naudodami ataskaitą **Nuokrypių analizės išrašas** galite peržiūrėti konvertuotų prekių atsargų perkainojimo nuokrypius. Taip pat galite naudoti puslapį **Standartinių išlaidų operacijos** ir peržiūrėti konvertuotų prekių su atsargomis perkainojimo operacijas.
-   Analizuokite atsargų vertę prieš perėjimo pradžią. Naudodami ataskaitą **Atsargų vertė** galite peržiūrėti konvertuotų prekių atsargų vertes. Nustatydami ataskaitos pabaigos datą, naudokite vieną dieną prieš perėjimo pradžią.
-   Analizuokite atsargų vertę prieš konvertavimo datą. Naudodami ataskaitą **Atsargų vertė** galite peržiūrėti konvertuotų prekių atsargų vertes. Kaip ir su ataskaitos pabaigos data, naudokite vieną dieną prieš kovertavimo datą.
-   Analizuokite atsargų vertę konvertavimo dieną. Naudodami ataskaitą **Atsargų vertė** galite peržiūrėti atsargų vertes konvertavimo dieną. Tiek ataskaitos Pradžios data, tiek Pabaigos data turėtų atitikti konvertavimo datą. Ataskaitos pasirinkimo kriterijai turi rodyti konvertuotas prekes.
-   Analizuokite atgaline data registruotus atsargų perkėlimus. Naudodami ataskaitą **Atsargų vertė** galite peržiūrėti atgaline data registruotus atsargų perkėlimus, kurie buvo įvesti po konvertavimo. Ataskaitos Pradžios data ir Pabaigos data turėtų atitikti perėjimo pradžios datą ir konvertavimo datą, minus viena diena. Ataskaitos pasirinkimo kriterijai turi rodyti konvertuotas prekes. Ataskaitoje rodomi atsargų perkėlimai, atlikti su standartinėmis išlaidomis perėjimo laikotarpiu.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Būtinosios standartinių išlaidų konvertavimo sąlygos](prerequisites-standard-cost-conversion.md)




