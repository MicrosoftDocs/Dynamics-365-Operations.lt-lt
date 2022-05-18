---
title: Pastoviosios atlyginimo dalies planų kūrimas
description: Šioje temoje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable, HcmCompensationWorkspace
audience: Application User
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 05f4748f66f4027972aabf53e7a1c237b8dbb543
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693065"
---
# <a name="create-a-fixed-compensation-plans"></a>Pastoviosios atlyginimo dalies planų kūrimas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Pastovioji atlyginimo dalis nurodo darbuotojo pastovų bruto atlyginimą ar darbo užmokestį. Šioje temoje aprašomi komponentai, kurie turi būti nustatyti prieš kuriant pastoviosios atlyginimo dalies planą ir įtraukiant darbuotojus.

Pastoviosios darbuotojų atlyginimo dalies sumas galima apskaičiuoti pagal tokius veiksnius kaip rezultatai, regionas ir biudžeto padidinimai. „Dynamics 365 Human Resources” palaiko veiksmų, kategorijos ir intervalo kompensacijos tipus.

## <a name="fixed-compensation-components"></a>Pastoviosios atlyginimo dalies komponentai
### <a name="compensation-levels"></a>kompensacijos lygiai

Galite naudoti **Kompensacijos lygius**, kad nustatytumėte kompensaciją už įvairias užduotis, užtikrindami, kad šias užduotys atliekantiems darbuotojams būtų sąžiningai mokama. Puslapyje **Kompensacijos lygiai** galite nustatyti kompensacijos lygius, kurių reikia kiekvienam veiksmų, kategorijos ir intervalo planui. Naudokite mygtukus **aukštyn** ir **žemyn**, kad išdėstytumėte lygius teisinga tvarka, pagal jų tipą. Nustatydami užduoties kompensacijos lygius, padedate užtikrinti, kad visiems darbuotojams, kurių pareigoms priskirta vienoda užduotis, bus mokama vienodai.

### <a name="reference-points"></a>Atskaitos taškai

**Atskaitos taškai** yra stulpeliai tinklelyje, apibrėžiantys kiekvieno lygio kompensacijos intervalus. kompensacijos lygis yra tinklelio eilutė. Įprasti kategorijos tipo plano atskaitos taškai yra mažiausias, vidurinis ir didžiausias. Atskaitos taškai kuriami puslapyje **Atskaitos taškų nustatymas**.

### <a name="compensation-grids"></a>Kompensavimo tinkleliai

Nustatę lygius ir atskaitos taškus, jie gali būti derinami sukuriant **Kompensacijų tinklelį**. Puslapyje **Kompensacijų tinkleliai** nurodyti informaciją apie tinklelį. Pvz., nurodykite, kam sukurtas tinklelis turi būti naudojamas, su kokio tipo planu jis bus naudojamas ir kuriuos atskaitos taškus ar stulpelius rodyti tinklelyje. Baigę įvesti šią informaciją, spustelėkite **kompensacijos struktūra**, kad prie savo tinklelio pridėtumėte lygius ir sumas. 

**Patarimas:** nustatykite pradines sumas naudodami kompensacijos struktūros funkciją **Masiniai keitimai**, tada didinkite procentais arba sumomis savo lygiuose arba atskaitos taškuose.

### <a name="pay-frequencies"></a>Išmokų dažnumas

**Mokėjimo dažnumas** naudojamas norint apibrėžti, kaip nurodyti darbuotojo darbo užmokestį arba kompensaciją (pavyzdžiui, 10 $ per valandą ar 50 000 $ per metus) ir konvertuoti į valandinius, savaitinius, mėnesinis (12 mėnesių) ir metinius tarifus. Pavyzdžiui, įmonė, kur valandinį tarifą gaunančių darbuotojų darbo savaitė trunka 38 valandas, nustato mokėjimo dažnumą, kurio valandinis tarifas yra 1, savaitinis tarifas 38, mėnesinis tarifas 164,6666666667 ir metinis tarifas 1,976. Konvertavimas naudojamas norint apskaičiuoti įvairius darbuotojo pastoviosios atlyginimo dalies įrašuose nustatomus tarifus.

## <a name="fixed-compensation-plans"></a>Pastoviųjų atlyginimo dalių planai
Galite sukurti sujungti pastoviosios atlyginimo dalies planą, apimantį visus jūsų sukonfigūruotus komponentus. Norėdami sukurti pastoviosios atlyginimo dalies planą, atidarykite puslapį **Pastoviosios atlyginimo dalies planai**. Čia galite suteikti savo planui pavadinimą ir aprašymą, pasirinkti, kokio tipo planas tai yra (veiksmų, kategorijos ar intervalo), pasirinkti darbuotojo užmokesčio tarifo mokėjimo dažnumą (suma per valandą, suma per metus ir t.t.) ir nustatyti kompensacijos apdorojimo tvarkymo parinktis. 

Nustatymas **Nepatenka į leistiną nuokrypio diapazoną** leidžia nurodyti, kaip griežtai norite užtikrinti, kad kompensacijos sumos būtų tarp mažiausios ir didžiausios sumų. **Griežtas** nuokrypis reikalauja, kad kompensacija patektų į atitinkamo lygio diapazoną. **Nuosaikus** nuokrypis įspėja, kai kompensacijos suma nebepatenka į diapazoną, bet leidžia tęsti. Jei nustatysite nuokrypio reikšmę **Nėra**, galėsite įvesti darbuotojo kompensacijos sumą sumą ir negauti įspėjimo arba klaidos pranešim.. 

Parametras **Samdos taisyklė** leidžia nurodyti, ar visi darbuotojai turi gauti tokį patį padidėjimą, neatsižvelgiant į jų pasamdymo dieną(**Samdos taisyklė**  = **Nėra**), ar darbuotojai turi gauti procentą nuo premijos, atsižvelgiant į tai, kiek laiko jie dirbo per ciklą (**Samdos taisyklė**  = **Procentas**). 

**Diapazono realizavimo matrica** yra naudinga, jei norite sutrumpinti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono vidurio tašką, arba pailginti laiką, kurio reikia darbuotojams, kad pasiektų savo diapazono didžiausią atskaitos tašką. Pavyzdžiui, norite darbuotojams, kurie yra apatinių 25 procentų diapazone, suteikti 110 procentų jų tikslinės premijos, bet darbuotojams, kurie yra viršutinių 25 procentų diapazone, norite suteikti tik 80 procentų jų tikslinės premijos, kad neleistumėte taip greitai pasiekti didžiausios reikšmės. 

Apibrėžę pastoviosios atlyginimo dalies plano pagrindus, galite nustatyti plano kompensacijos struktūrą. Spustelėkite **Nustatyti kompensaciją**. Atidaromas dialogo slankiklis, kuris suteikia tris parinktis.

-   **Sukurti naują kompensacijos matricą** pasirenkant atskaitos taško nustatymą ir suteikiant tinkleliui pavadinimą.
-   **Sukurti naują kompensacijos matricą** nukopijuojant esamą tinklelį, kurį galite naudoti kaip pradžios tašką.
-   **Naudoti esamą kompensacijos matricą** kuri jau apibrėžta. Visi kompensacijų planai, kurie naudoja tą patį tinklelį, gauna atnaujinimus, jei tas tinklelis pakeičiamas.

Kai pasirenkate parinktį, atidaromas puslapis **kompensacijos struktūra** ir galite keisti naują ar esamą kompensacijų tinklelį.

## <a name="fixed-compensation-enrollment"></a>Pastoviosios atlyginimo dalies registracija
### <a name="determine-who-is-eligible-for-the-plan"></a>Nustatykite, kas turi teisę gauti planą

Pirmasis darbuotojų įtraukimo į pastoviosios atlyginimo dalies planą žingsnis yra nustatyti, kas turi teisę gauti gauti plane apibrėžtą kompensaciją. Kol nenustatysite tinkamumo, negalėsite priskirti plano nė vienam darbuotojui. Norėdami nustatyti tinkamumą, atidarykite puslapį **Tinkamumo taisyklės**. Čia galite sukurti naują tinkamumo jūsų kompensacijos planui taisyklę ir apibrėžti kriterijus, kuriuos darbuotojas turi atitikti, kad būtų tinkamas šiam planui. Galite riboti tinkamumą pagal padalinį, profesinę sąjungą, kompensacijų regioną (vietą), užduotį, užduoties tipą arba kompensacijos lygį. Darbuotojai gali būti įtraukti į kompensacijos planą tik tada, jei jie atitinka visus kriterijus, nustatytus tinkamumo taisyklėje. 

**Pastaba:** tinkamumo taisyklės naudojamos siekiant nustatyti teisę tiek į pastoviosios, tiek į kintamosios atlyginimo dalies planą. 

Tinkamumo taisyklė įvertina konkrečių **Užduoties**, **Pareigų** ir **Darbuotojo** įrašų laukų reikšmę, kad nustatytų, ar darbuotojas turi teisę į kompensacijos planą.

-   Puslapyje **Užduotis** tinkamumo taisyklė atsižvelgia į šiuos laukus:
    -   Lauką **Užduotis**
    -   Skirtuke **Užduočių klasifikacija** – į laukus **Funkcija** ir **Užduoties tipas**
    -   Skirtuke **Kompensacija** – į lauką **Lygis**
-   Puslapyje **Pareigos** tinkamumo taisyklė įvertina laukus **Padalinys** ir **Kompensacijų regionas**.

Tinkamumo taisyklė taip pat įvertina su darbuotoju susijusias profesines sąjungas (puslapyje **Darbuotojai**, skirtuke **Darbuotojas**, spustelėkite **Asmeninė informacija** &gt; **Profesinės sąjungos**).

### <a name="define-fixed-compensation-actions"></a>Pastoviosios atlyginimo dalies veiksmų apibrėžimas

**Pastoviosios atlyginimo dalies veiksmai** naudojami, kai nustatote arba taikoti darbuotojo pastoviosios atlyginimo dalies pakeitimus. Pastoviosios atlyginimo dalies veiksmai jums leidžia pateikti aprašomuosius pavadinimus veiksmų tipams, kuriuos gali atlikti kompensacijų ir išmokų vadovas. Skirtingi veiksmų tipai paremti skirtinga logika, kad jie galėtų būti naudojami tik tam tikru metu. 

Pvz., nustačius pastoviąją atlyginimo dalį darbuotojui, galima naudoti tik tuos veiksmus, kurių tipas yra **Samda / Pakartotinė samda**. Tokiu atveju gali būti paranku sukurti tris skirtingus **Samda / Pakartotinė samda** tipo veiksmus ir juos pavadinti **Samdyti**, **Pakartotinai samdyti** ir **Perkelti**. Tokiu būdu turėsite detalesnį paaiškinimą, kodėl pastovioji atlyginimo dalis buvo skirta darbuotojui arba pakeista.

### <a name="enroll-the-employee"></a>Darbuotojo įtraukimas

Dabar galite pastoviosios atlyginimo dalies planui priskirti darbuotoją. Atidarykite puslapį **Darbuotojai** ir pasirinkite darbuotoją, kurį norite įtraukti į kompensacijos planą. Veiksmų srityje spustelėkite **Kompensacija** &gt; **Pastoviosios dalies planas**. Dabar tam darbuotojui galite sukurti naują pastoviosios atlyginimo dalies veiksmą. 

**Pastaba:** Lauke **Kompensacijos planas** rodomi tik tie planai, į kuriuos darbuotojas turi teisę pagal kiekvienam planui nustatytas tinkamumo taisykles. Jei planas neturi nustatytos tinkamumo taisyklės, į tokį planą negalės būti įtraukti jokie darbuotojai. 

Patikrinama, ar nurodyta kategorijos arba intervalo tipo kompensacijos plano suma yra tarp mažiausio ir didžiausio atskaitos taškų pagal darbuotojo užduočiai priskirtą kompensacijos lygį. Jei kompensacijos suma nepatenka į leidžiamą diapazoną, rodomas perspėjimas arba klaidos pranešimas, atsižvelgiant į pastoviosios atlyginimo dalies plano nuokrypio lygį.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
