---
title: "Pastoviosios atlyginimo dalies planų kūrimas"
description: "Pastovioji atlyginimo dalis nurodo darbuotojo pastovų bruto atlyginimą ar darbo užmokestį. Šiame straipsnyje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e71e22cef2b65c4cf89b8fe0ea55e092e259c6dc
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="create-fixed-compensation-plans"></a>Pastoviosios atlyginimo dalies planų kūrimas

[!include[banner](includes/banner.md)]


Pastovioji atlyginimo dalis nurodo darbuotojo pastovų bruto atlyginimą ar darbo užmokestį. Šioje temoje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus.

Pastoviosios darbuotojų atlyginimo dalies sumas galima apskaičiuoti pagal tokius veiksnius kaip rezultatai, regionas ir biudžeto padidinimai. „Microsoft Dynamics 365 for Operations“ palaiko veiksmų, kategorijos ir intervalo kompensacijos tipus.

## <a name="fixed-compensation-components"></a>Pastoviosios atlyginimo dalies komponentai
### <a name="compensation-levels"></a>kompensacijos lygiai

Galite naudoti **kompensacijos lygius**, kad nustatytumėte kompensaciją už įvairias užduotis, užtikrindami, kad šias užduotys atliekantiems darbuotojams būtų sąžiningai mokama. Puslapyje **Kompensacijos lygiai** galite nustatyti kompensacijos lygius, kurių reikia kiekvienam veiksmų, kategorijos ir intervalo planui. Naudokite mygtukus **aukštyn** ir **žemyn**, kad išdėstytumėte lygius teisinga tvarka, pagal jų tipą. Nustatydami užduoties kompensacijos lygius, padedate užtikrinti, kad visiems darbuotojams, kurių pareigoms priskirta vienoda užduotis, bus mokama vienodai.

### <a name="reference-points"></a>Atskaitos taškai

**Atskaitos taškai** yra stulpeliai tinklelyje, apibrėžiantys kiekvieno lygio kompensacijos intervalus. kompensacijos lygis yra tinklelio eilutė. Įprasti kategorijos tipo plano atskaitos taškai yra mažiausias, vidurinis ir didžiausias. Atskaitos taškai kuriami puslapyje **Atskaitos taškų nustatymas**.

### <a name="compensation-grids"></a>Kompensavimo tinkleliai

Nustatę lygius ir atskaitos taškus, jie gali būti derinami sukuriant **kompensacijų tinklelį**. Puslapyje **Kompensacijų tinkleliai** nurodyti informaciją apie tinklelį. Pvz., nurodykite, kam sukurtas tinklelis turi būti naudojamas, su kokio tipo planu jis bus naudojamas ir kuriuos atskaitos taškus ar stulpelius rodyti tinklelyje. Baigę įvesti šią informaciją, spustelėkite **kompensacijos struktūra**, kad prie savo tinklelio pridėtumėte lygius ir sumas. 

**Patarimas:** nustatykite pradines sumas naudodami kompensacijos struktūros funkciją **Masiniai keitimai**, tada didinkite procentais arba sumomis savo lygiuose arba atskaitos taškuose.

### <a name="pay-frequencies"></a>Išmokų dažnumas

**Mokėjimo dažnumas** naudojamas norint apibrėžti, kaip nurodyti darbuotojo darbo užmokestį arba kompensaciją (pavyzdžiui, 10 $ per valandą ar 50 000 $ per metus) ir konvertuoti į valandinius, savaitinius, mėnesinis (12 mėnesių) ir metinius tarifus. Pavyzdžiui, įmonė, kur valandinį tarifą gaunančių darbuotojų darbo savaitė trunka 38 valandas, nustato mokėjimo dažnumą, kurio valandinis tarifas yra 1, savaitinis tarifas 38, mėnesinis tarifas 164,6666666667 ir metinis tarifas 1,976. Konvertavimas naudojamas norint apskaičiuoti įvairius darbuotojo pastoviosios atlyginimo dalies įrašuose nustatomus tarifus.

## <a name="fixed-compensation-plans"></a>Pastoviųjų atlyginimo dalių planai
Galite sukurti sujungti pastoviosios atlyginimo dalies planą, apimantį visus jūsų sukonfigūruotus komponentus. Norėdami sukurti pastoviosios atlyginimo dalies planą, atidarykite puslapį **Pastoviosios atlyginimo dalies planai**. Čia galite suteikti savo planui pavadinimą ir aprašymą, pasirinkti, kokio tipo planas tai yra (veiksmų, kategorijos ar intervalo), pasirinkti darbuotojo užmokesčio tarifo mokėjimo dažnumą (suma per valandą, suma per metus ir t.t.) ir nustatyti kompensacijos apdorojimo tvarkymo parinktis. 

Nustatymas **Nepatenka į leistiną nuokrypio diapazoną** leidžia nurodyti, kaip griežtai norite užtikrinti, kad kompensacijos sumos būtų tarp mažiausios ir didžiausios sumų. **Griežtas** nuokrypis reikalauja, kad kompensacija patektų į atitinkamo lygio diapazoną. **Nuosaikus** nuokrypis įspėja, kai kompensacijos suma nebepatenka į diapazoną, bet leidžia tęsti. Jei nustatysite nuokrypio reikšmę **Nėra**, galėsite įvesti darbuotojo kompensacijos sumą sumą ir negauti įspėjimo arba klaidos pranešim.. 

Parametras **Samdos taisyklė** leidžia nurodyti, ar visi darbuotojai turi gauti tokį patį padidėjimą, neatsižvelgiant į jų pasamdymo dieną(**Samdos taisyklė**  = **Nėra**), ar darbuotojai turi gauti procentą nuo premijos, atsižvelgiant į tai, kiek laiko jie dirbo per ciklą (**Samdos taisyklė**  = **Procentas**). 

**Diapazono realizavimo matrica** naudinga, jei norite sutrumpinti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono vidurio tašką, arba pailginti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono didžiausią atskaitos tašką. Pavyzdžiui, norite darbuotojams, kurie yra apatinių 25 procentų diapazone, suteikti 110 procentų jų tikslinės premijos, bet darbuotojams, kurie yra viršutinių 25 procentų diapazone, norite suteikti tik 80 procentų jų tikslinės premijos, kad neleistumėte taip greitai pasiekti didžiausios reikšmės. 

Apibrėžę pastoviosios atlyginimo dalies plano pagrindus, galite nustatyti plano kompensacijos struktūrą. Spustelėkite **Nustatyti kompensaciją**. Atidaromas dialogo slankiklis, kuris suteikia tris parinktis.

-   Sukurti naują kompensacijų tinklelį pasirenkant atskaitos taško nustatymą ir suteikiant tinkleliui pavadinimą.
-   Sukurti naują kompensacijų tinklelį nukopijuojant esamą tinklelį, kurį galite naudoti kaip pradžios tašką.
-   Naudoti esamą kompensacijų tinklelį, kuris jau apibrėžtas. Visi kompensacijų planai, kurie naudoja tą patį tinklelį, gauna atnaujinimus, jei tas tinklelis pakeičiamas.

Kai pasirenkate parinktį, atidaromas puslapis **kompensacijos struktūra** ir galite keisti naują ar esamą kompensacijų tinklelį.

## <a name="fixed-compensation-enrollment"></a>Pastoviosios atlyginimo dalies registracija
### <a name="determine-who-is-eligible-for-the-plan"></a>Nustatykite, kas turi teisę gauti planą

Pirmasis darbuotojų įtraukimo į pastoviosios atlyginimo dalies planą žingsnis yra nustatyti, kas turi teisę gauti gauti plane apibrėžtą kompensaciją. Kol nenustatysite tinkamumo, negalėsite priskirti plano nė vienam darbuotojui. Norėdami nustatyti tinkamumą, atidarykite puslapį **Tinkamumo taisyklės**. Čia galite sukurti naują tinkamumo jūsų kompensacijos planui taisyklę ir apibrėžti kriterijus, kuriuos darbuotojas turi atitikti, kad būtų tinkamas šiam planui. Galite riboti tinkamumą pagal padalinį, profesinę sąjungą, kompensacijų regioną (vietą), užduotį, užduoties tipą arba kompensacijos lygį. Darbuotojai gali būti įtraukti į kompensacijos planą tik tada, jei jie atitinka visus kriterijus, nustatytus tinkamumo taisyklėje. 

**Pastaba:** tinkamumo taisyklės naudojamos siekiant nustatyti teisę tiek į pastoviosios, tiek į kintamosios atlyginimo dalies planą. 

Tinkamumo taisyklė įvertina konkrečių užduoties, pareigų ir darbuotojo įrašų laukų reikšmę, kad nustatytų, ar darbuotojas turi teisę į kompensacijos planą.

-   Puslapyje **Užduotis** tinkamumo taisyklė atsižvelgia į šiuos laukus:
    -   Lauką **Užduotis**
    -   Skirtuke **Užduočių klasifikacija** – į laukus **Funkcija** ir **Užduoties tipas**
    -   Skirtuke **Kompensacija** – į lauką **Lygis**
-   Puslapyje **Pareigos** tinkamumo taisyklė įvertina laukus **Padalinys** ir **Kompensacijų regionas**.

Tinkamumo taisyklė taip pat įvertina su darbuotoju susijusias profesines sąjungas (puslapyje **Darbuotojai**, skirtuke **Darbuotojas**, spustelėkite **Asmeninė informacija** &gt; **Profesinės sąjungos**).

### <a name="define-fixed-compensation-actions"></a>Pastoviosios atlyginimo dalies veiksmų apibrėžimas

**Pastoviosios atlyginimo dalies veiksmai** naudojami, kai nustatote arba taikoti darbuotojo pastoviosios atlyginimo dalies pakeitimus. Pastoviosios atlyginimo dalies veiksmai leidžia pateikti aprašomuosius pavadinimus veiksmų tipams, kuriuos gali atlikti kompensacijų ir išmokų vadovas. Skirtingi veiksmų tipai paremti skirtinga logika, kad jie galėtų būti naudojami tik tam tikru metu. 

Pvz., nustačius pastoviąją atlyginimo dalį darbuotojui, galima naudoti tik tuos veiksmus, kurių tipas yra **Samda / Pakartotinė samda**. Tokiu atveju gali būti paranku sukurti tris skirtingus **Samda / Pakartotinė samda** tipo veiksmus ir juos pavadinti **Samdyti**, **Pakartotinai samdyti** ir **Perkelti**. Tokiu būdu turėsite detalesnį paaiškinimą, kodėl pastovioji atlyginimo dalis buvo skirta darbuotojui arba pakeista.

### <a name="enroll-the-employee"></a>Darbuotojo įtraukimas

Dabar galite pastoviosios atlyginimo dalies planui priskirti darbuotoją. Atidarykite puslapį **Darbuotojai** ir pasirinkite darbuotoją, kurį norite įtraukti į kompensacijos planą. Veiksmų srityje spustelėkite **Kompensacija** &gt; **Pastoviosios dalies planas**. Dabar tam darbuotojui galite sukurti naują pastoviosios atlyginimo dalies veiksmą. 

**Pastaba:** kompensacijos plano lauke rodomi tik tie planai, į kuriuos darbuotojas turi teisę pagal kiekvienam planui nustatytas tinkamumo taisykles. Jei planas neturi nustatytos tinkamumo taisyklės, į tokį planą negalės būti įtraukti jokie darbuotojai. 

Sistema patikrina, kad nurodyta kategorijos arba intervalo tipo kompensacijos plano suma yra tarp mažiausio ir didžiausio atskaitos taškų pagal darbuotojo užduočiai priskirtą kompensacijos lygį. Jei kompensacijos suma nepatenka į leidžiamą diapazoną, rodomas perspėjimas arba klaidos pranešimas, atsižvelgiant į pastoviosios atlyginimo dalies plano nuokrypio lygį.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kompensacijų planai](compensation-plans.md)




