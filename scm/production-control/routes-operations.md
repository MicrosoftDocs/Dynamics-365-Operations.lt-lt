---
title: "Maršrutai ir operacijų"
description: "Šioje temoje pateikta informacija apie maršrutus ir operacijas. Maršrutą nurodo gamybos produkto ar gaminio variantas procesas. Ji apibūdina kiekvieno veiksmo (veikimo) gamybos procesas ir kad reikia atlikti šiuos veiksmus. Kiekviename žingsnyje, maršrutas taip pat apibrėžiami operacijų priemones, reikalingas laiko ir darbo laiką, ir kaip reikėtų apskaičiuoti išlaidas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Maršrutai ir operacijų

Šioje temoje pateikta informacija apie maršrutus ir operacijas. Maršrutą nurodo gamybos produkto ar gaminio variantas procesas. Ji apibūdina kiekvieno veiksmo (veikimo) gamybos procesas ir kad reikia atlikti šiuos veiksmus. Kiekviename žingsnyje, maršrutas taip pat apibrėžiami operacijų priemones, reikalingas laiko ir darbo laiką, ir kaip reikėtų apskaičiuoti išlaidas.

<a name="overview"></a>Apžvalga
--------

Maršruto aprašoma operacijos tvarka, ko reikia norint pagaminti gaminį ar gaminio variantas. Kiekvienai operacijai, maršrutas taip pat apibrėžia veiklos išteklius, kurių reikia, laiką, kurio reikia norint nustatyti ir atlikti operaciją, o kaip reikėtų apskaičiuoti išlaidas. Galite naudoti to paties maršruto kelių produktams gaminti, arba galite nurodyti kiekvieno produkto ar gaminio variantas unikalių maršrutą. Galite net turėti kelių maršrutų už tą patį produktą. Šiuo atveju, maršrutas, kurį naudoja skiriasi, priklausomai nuo veiksnių pvz., kiekis, kuris turi būti gaminamas. Maršruto Microsoft Dynamics 365 operacijų apibrėžimas susideda iš keturių atskirų elementų, kurie kartu, apibūdinti gamybos procesą:

-   **Maršrutas** – maršrutą apibrėžia struktūrą ir gamybos proceso. Kitaip tariant, ji apibrėžia veiklos tvarką.
-   **Operacija** – operacija identifikuoja pavadintas žingsnis maršrutą, pvz., **Asamblėjos**. Tos pačios operacijos gali atsirasti kelių maršrutų ir gali turėti skirtingas operacijos numerius.
-   **Operacijos** – operacijos ryšio apibrėžia veiklos ypatybes operaciją, pvz., nustatymo laiko ir vykdymo laiko išlaidų kategorijas, ir vartojimo parametrai ir išteklių poreikius. Operacijos ryšys leidžia veiklos ypatybes gali skirtis, priklausomai nuo maršruto, kad operacija yra naudojama, arba produktų, kurie gaminami operacijos.
-   **Maršruto versiją** – maršruto versiją nustato maršrutą, kuris yra naudojamas gaminti gaminį ar gaminio variantas. Maršruto versijos sudaryti maršrutai turi būti pakartotinai naudojamos produktuose arba pasikeitė per tam tikrą laiką. Jie taip pat leidžia skirtingų maršrutų į gaminti tą patį produktą. Tokiu atveju maršrutą, kuris yra naudojamas priklauso nuo veiksnių, tokių kaip vieta arba kiekis, kuris turi būti gaminamas.

## <a name="routes"></a>Maršrutai
Maršruto aprašoma operacijų tvarką, naudojamas gaminti gaminį ar gaminio variantas. Kiekvienai operacijai suteikiamas operacijos numerį ir įpėdinis operacija. Operacijų tvarka sudaro maršruto tinklo, kuris gali atstovauti nukreiptą diagramoje, kuriame yra vienas ar daugiau įdirbis ir vieną pabaigos tašką. Dynamics 365 operacijoms, keliai skirstomi pagal konstrukcijos tipą. Dviejų tipų maršrutai yra paprasta maršrutus ir maršruto tinklus. Gamybos kontrolės parametrų, galite nurodyti ar tik paprastas maršrutai gali būti naudojamas arba ar daugiau sudėtingų maršrutų tinklo gali būti naudojamas.

### <a name="simple-routes"></a>Paprasta maršrutus

Paprastas būdas yra nuoseklus, ir tai tik vienas atskaitos taškas maršrute.  

[![Paprastas būdas](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Jei įjungsite tik paprasta maršrutus gamybos kontrolės parametrų, Dynamics 365 operacijoms automatiškai generuoja operacijos numerius (10, 20, 30 ir t.t.) nurodžius maršrutą.

### <a name="route-networks"></a>Maršrutų tinklo

Jei įjungsite daugiau sudėtingų maršrutų tinklo gamybos kontrolės parametrų, galite nustatyti maršrutų, keli atspirties taškų ir operacijų, kurios gali būti vykdomos lygiagrečiai.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Pastabos**

-   Kiekvienos operacijos gali būti tik vienas įpėdinis operacija, o visą maršrutą turi baigtis per vieną operaciją.
-   Nėra jokių garantijų, kad iš tikrųjų daug operacijų, kurios neturi tos pačios įpėdinis operacijos (pvz., 30 – 40 ankstesnėje iliustracijoje operacijos) vyks tuo pačiu metu. Pakankamumu ir pajėgumu išteklių kokybiniais apribojimais, kaip kad planuojamos veiklos.
-   0 (nulis) negalima naudoti kaip operacijos numerį. Šis skaičius yra rezervuotas ir yra naudojamas nurodyti, kad paskutinės operacijos maršruto neturi jokių teisių perėmėjas operacija.

### <a name="parallel-operations"></a>Lygiagrečias operacijas

Kartais, sujungiant keletą operacijų išteklius, kurie turi skirtingas savybes būtina atlikti operaciją. Pvz., surinkimo operacijos gali prireikti mašina, priemonė ir vienas darbuotojas per dvi mašinos prižiūrėti operacija. Šiame pavyzdyje galima modeliuoti naudojant lygiagrečias operacijas, kur viena operacija yra paskirta pirminė operacija ir kiti yra antraeiliai.  

[![Maršrutas, kuriame yra pirminės ir antrinės operacijos](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Paprastai, pirminės operacijos yra Ribotosios spartos ištekliai ir diktuoja laikas, antrinės operacijos. Tačiau planavimo metu, kuris apima Ribotosios spartos pajėgumas, išteklių, kurie yra numatyta ir pirminė operacija ir antrinės operacijos turi būti prieinama ir turi neišnaudotų pajėgumų, tuo pačiu metu.  

Pirminė operacija ir antrinės operacijos turi turėti tą patį operacijos numerį (30 ankstesnėje iliustracijoje).  

Ankstesniame pavyzdyje, pirminė operacija (30) išteklių reikalavimas yra mašina, kadangi išteklių poreikių antrinės operacijos (30' ir 30'') įrankį ir darbuotojo. Penkiasdešimt procentų apkrovos padeda užtikrinti, kad suplanuotas darbuotojas galėtų prižiūrėti dvi mašinos ir tuo pačiu metu.

### <a name="approval-of-routes"></a>Maršrutų patvirtinimas

Maršrutas turi būti patvirtintas prieš ji gali būti naudojama planavimas arba gamybos procesas. Patvirtinimas rodo, kad maršruto dizainas bus baigta. Tas pats išleido produktą arba jau išleistą produktą variantas gali turėti kelių patvirtintų maršrutų. Paprastai patvirtinimas maršruto kyla patvirtinus pirmoji atitinkama maršruto versija. Tačiau kai kurių verslo scenarijai, patvirtinti maršrutą ir maršruto versiją yra atskiras veiklas, kad būtų įtraukti įvairių proceso savininkai.  

Kiekvienam maršrutui gali būti patvirtintas arba nepatvirtintas atskirai. Tačiau Atkreipkite dėmesį, kad, kai maršrutas yra nepatvirtintų, visas susijusias maršruto versijos taip pat yra nepatvirtintas. Gamybos kontrolės parametrų, galite nurodyti ar maršrutai gali būti nepatvirtinti, ir ar galima pakeisti patvirtintų maršrutų.  

Jei jūs privalote prisijungti kad įrašų, kurie patvirtina kiekvieno maršruto, jums reikia elektroninio parašo maršruto patvirtinimo. Tada vartotojai turės patvirtinti savo tapatybę naudodami, [elektroninio parašo](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>„Operations“
Operacija yra gamybos proceso žingsnis. Dynamics 365 operacijoms, kiekviena operacija turi ID ir paprastą aprašymą. Šios lentelės rodo tipiškų pavyzdžių operacijas iš mašinos parduotuvė.

| Operacija  | aprašymas        |
|------------|--------------------|
| PipeCut    | Vamzdžių pjovimas       |
| TIGweld    | TIG suvirinimas        |
| JigAssy    | S montavimas       |
| Patikrinimas | Kokybės kontrolės |

Veiklos ypatybes operaciją, pvz., nustatymo laiko ir vykdymo laiko išteklių poreikius, ir savikainos informaciją ir sąnaudų skaičiavimui, yra nurodyta operacijos ryšiui. (Daugiau informacijos apie operaciją santykių, žr. kitą skyrių.)

## <a name="operation-relations"></a>Operacijų ryšiai
Šios veiklos ypatybės operacijos tvarkomos operacijos ryšiui:

-   Išlaidų kategorijos
-   Vartojimo parametrai
-   Nagrinėjimo laiką
-   Apdoroti kiekiai
-   Išteklių reikalavimai
-   Pastabos ir nurodymai

Galite nurodyti kelis operacijos santykių už tą pačią operaciją. Tačiau, kiekvienos operacijos ryšys yra susijusios su viena operacija ir saugo ypatybes, būdingas maršrutą, išleistą produktą arba išleistų produktų, kurie yra susiję su prekių grupę. Todėl kelis maršrutus, kad skirtingas veiklos savybes galima tos pačios operacijos. Be to, jūs lengviau išlaikyti savo pagrindinius duomenis, jei jūs naudojate standartinį operacijų, kurios neturi tos pačios veiklos ypatybės, nepriklausomai nuo maršruto, kuris naudojamas ir produkto, kuris yra gaminamas. Į operacijos ryšio apimtis yra apibrėžiama per į **prekės kodas**, **prekės atžvilgiu**, **maršruto kodas** ir **nukreipti ryšio** savybės, kaip parodyta toliau pateiktoje lentelėje.

| Prekės kodas | Prekės ryšys         | Maršruto kodas | Maršruto ryšys   | Taikymo į operacijos ryšio                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lentelė     | &lt;Prekės ID&gt;       | Maršrutas      | &lt;Maršruto ID&gt; | Veiklos ypatybes operaciją naudojant maršruto kur **maršruto numeris**=&lt;maršruto ID&gt; išleistas produktui gaminti kur **prekės numeris**=&lt;prekės ID&gt;.                                                                                                                        |
| Lentelė     | &lt;Prekės ID&gt;       | Visos        |                  | Numatytasis veiklos ypatybes operaciją, kai jis naudojamas gaminti išleido produktą kur **prekės numeris**=&lt;prekės ID&gt;. Kitaip tariant, šios veiklos ypatybės taikomos, kai yra ne konkretų operacijos ryšio pateikto produkto.                                     |
| Grupuoti     | &lt;Prekių grupės ID&gt; | Maršrutas      | &lt;Maršruto ID&gt; | Veiklos ypatybes operaciją naudojant maršruto kur **maršruto numeris**=&lt;maršruto ID&gt; gaminti išleistų produktus, kurie yra susiję su prekių grupės &lt;prekių grupės ID&gt;, nebent yra konkretų operacijos ryšio išleido produktą.                         |
| Grupuoti     | &lt;Prekių grupės ID&gt; | Visos        |                  | Numatytasis veiklos ypatybes operaciją, kai jis naudojamas gaminti išleistų produktus, kurie yra susiję su prekių grupės &lt;prekių grupės ID&gt;, nebent konkretesnės veiklos ryšys.                                                                                                  |
| Visos       |                       | Maršrutas      | &lt;Maršruto ID&gt; | Numatytasis veiklos ypatybes operaciją, kai jis yra naudojamas maršruto kur **maršruto numeris**=&lt;maršruto ID&gt;. Kitaip tariant, šios veiklos ypatybės taikomos, kai nėra jokios operacijos ryšio tokį problemos sprendimo būdą, būdingą arba išleistą produktą arba yra su jais susijusios prekės grupė. |
| Visos       |                       | Visos        |                  | Numatytasis veiklos ypatybes operaciją. Šios veiklos ypatybės taikomos, kai daugiau konkrečios operacijos ryšio nėra.                                                                                                                                                                |

Jūs taip pat galite nurodyti, kad operacijos ryšys yra konkrečios vietos. Tokiu būdu operacijos veiklos ypatybes gali skirtis, priklausomai nuo vietos (t. y. svetainę), kur operacija atliekama. Konfigūruotų produktų, taip pat galite nurodyti skirtingas veiklos savybes kiekvienas gaminio konfigūracijai.  

Operacijos santykių jums lankstumo, kai nustatote savo maršrutus. Be to, galimybė nustatyti numatytųjų ypatybių padeda sumažinti pagrindinių duomenų, kad jūs turite palaikyti. Tačiau šis lankstumas taip pat reiškia, kad jums reikia žinoti kontekstą, kad jums pakeisti operacijos ryšio.  

**Pastaba:** nes veiklos Ypatybės saugomos už kiekvieno maršruto operacijos santykiuose, visų atvejų, kai tos pačios operacijos (pvz., surinkimo) turi patį nustatymo laikas, vykdymo laikas, išteklių poreikius, ir t.t.. Taigi, jeigu dviejų atvejų, kai operacija turi atsirasti tuo pačiu maršrutu, bet turi skirtingus veikimo laiką, turite sukurti dvi atskiras operacijas, pvz., Assembly1 ir Assembly2.

### <a name="modifying-product-specific-routes"></a>Modifikuoti specifines maršrutai

Kai atidarote į **maršruto** puslapis iš į **išleistas informacija apie** puslapyje, maršruto versijų, kurios yra susijusios su pasirinkto išleistas produktas yra rodomas. Tokiu atveju už kiekvieną operaciją, Dynamics 365 operacijoms rodo veiklos ypatybes iš operacijos ryšiui, geriausiai tenkinančias maršruto versiją. Jūs pastebėsite, kad veiksmų sąrašas apima ir **prekės kodas** ir **maršruto kodas** ypatybes iš operacijos ryšiui. Todėl galite nurodyti, kurios operacijos ryšys yra.  

Dėl į **maršruto** puslapyje, galite keisti veiklos ypatybes operaciją, pvz., laikas ar išlaidų kategorijų. Jūsų pakeitimai išsaugomi operacijos ryšiui, skirtas maršrutas, išleistą produktą, kurie yra nuorodos į dabartinio maršruto versiją. Jei į operacijos ryšio, kuris yra rodomas maršrutas ir išleisti produktą, prieš jūsų keitimai yra saugomi, sistema sukuria kopiją į operacijos ryšio. Ši kopija *yra* maršrutas ir išleisti produktą. Todėl, jūsų keitimai neturės įtakos kitų maršrutų arba išleisti produktai. Patikrinti, kurios operacijos ryšys yra yra keistas, **maršruto** psl., pažvelgti į **prekės kodas** ir **maršruto kodas** laukus.  

Galite rankiniu būdu sukurti operacijoje, kurios yra susijusios su maršrutu ir jau išleistą produktą naudojant į **kopijuoti ir redaguoti ryšį** funkcija.  

**Pastaba:** jei galite pridėti naują operaciją į maršrutą į **maršruto** puslapyje, operacijos ryšys sukuriamas tik už dabartinę išleido produktą. Todėl, jei maršrutas taip pat naudojamas kitų išleistų produktams gaminti, nėra taikomos operacijos ryšio būsiančių išleistų produktų ir maršruto nebegali būti naudojamas tų išleistų produktų.

### <a name="maintaining-operation-relations-per-route"></a>Operacijos ryšių maršruto dalyje.

Kai atidarote į **maršruto duomenys** puslapis iš į **maršrutų** sąrašo puslapį, rodomas sąrašas visų operation relations, taikomas pasirinkto maršruto. Todėl galite lengvai patikrinti, kurioje veiklos apgyvendinimo įstaigos yra naudojami produktai. Galite keisti numatytąjį ypatybių reikšmes ir konkretaus produkto ypatybių reikšmes.  

Jei galite pridėti naują operacijos ryšio su **maršruto duomenys** puslapis, į **maršruto kodas** laukas automatiškai nustatomas kaip **maršruto**, ir **nukreipti ryšio** laukas yra nustatytas dabartinio maršruto numeris.

### <a name="maintaining-operation-relations-per-operation"></a>Operacijos ryšių operacijos sąnaudos

Iš į **veiklos** puslapį, galite atidaryti su **operacijos santykių** puslapis. Šiame puslapyje galite keisti visos operacijos santykių dėl konkrečios operacijos. Galite net keisti operacijos santykių, kuriuose yra numatytųjų reikšmių.  

Jei jūsų įmonė naudoja standartinį operacijų ir veiksmų parametrai yra tokie patys visose produktų ir procesų, į **operacijos santykių** puslapis suteikia galimybę patogiai išlaikyti numatytasis veiklos ypatybes tų operacijų.

### <a name="applying-operation-relations"></a>Taikant operacijos santykių

Kai kuriais atvejais, Dynamics 365 operacijoms turi rasti veiklos ypatybes operacijai. Pvz., kai sukuriamas pirkimo užsakymas, kiekvienos operacijos veiklos ypatybės turi būti kopijuojami iš operation relations gamybos maršrute. Tokiais atvejais Dynamics 365 operacijoms daugiau atitinkamų operation relations konkrečiausia derinimu su mažiau kaip tikras derinys.  

Dynamics 365 operacijų ieško tinkamiausios operacijos ryšio išleistas produktas, operacijos ryšio, kuris atitinka elemento ID pateikto produkto, kai yra geriau negu operacijos ryšio kad rungtynes prekių grupės ID. Savo ruožtu, operacijos ryšio, kuris atitinka prekių grupės ID yra teikiama pirmenybė per numatytąjį operacijos ryšiui. Paieška atliekama tokia tvarka:

1.  **Prekės kodas**=**lentelė** ir **prekės atžvilgiu**=&lt;prekės ID&gt;
2.  **Prekės kodas**=**grupės** ir **prekės atžvilgiu**=&lt;prekių grupės ID&gt;
3.  **Prekės kodas**=**visi**
4.  **Maršruto kodas**=**maršruto** ir **nukreipti ryšio**=&lt;maršruto ID&gt;
5.  **Maršruto kodas**=**visi**
6.  **Konfigūracija**=&lt;konfigūracijos ID&gt;
7.  **Configuration**=
8.  **Svetainės**=&lt;svetainės ID&gt;
9.  **Site**=

Todėl, operacijos turėtų būti naudojamas tik vieną kartą kiekvienam maršrutui. Jei operacija vyksta kelis kartus tuo pačiu maršrutu, visų atvejų, kai ši operacija vykdoma turės pačios operacijos ryšio, ir jūs negalėsite turėti skirtingas savybes (pavyzdžiui, paleisti kartus) aptikusi.

## <a name="route-versions"></a>Maršruto versijos
Maršruto versijos naudojamos variacijas produktų gamybai arba labiau kontroliuoti gamybos procesą. Jie nustatyti, kurioje maršrutas turi būti naudojamas, kai konkreti išleido produktą arba jau išleistą produktą variantas yra gaminamas. Nustatyti, kurioje yra vartojamas išleido produktą, galite naudoti šiuos suvaržymus:

-   Gaminio matmenys (dydį, spalvą, stilių ar konfigūracijos)
-   Gamybos kiekis
-   Gamybos vietos
-   Pagaminimo data

Kada jums gaminti produkto konkrečioje vietoje, tam tikrame kiekyje, arba tam tikrą laikotarpį, galite nustatyti konkrečių maršruto versiją kaip numatytojo maršruto versiją. Tačiau Atkreipkite dėmesį, kad tik vienas aktyvus maršrutas leidžiama tam tikras išleistas produktas ir reikiamam apribojimus.  

Gamybos kontrolės parametrų, galite reikalauti, kad galiojimo laiką maršruto versiją visada galima nurodyti.

### <a name="approval-of-route-versions"></a>Maršruto versijos patvirtinimo

Prieš maršruto versiją galima planavimas arba gamybos procesas, jis turi būti patvirtintas. Kai patvirtinsite maršruto versiją, taip pat gali patvirtinti būdo. Tačiau Atkreipkite dėmesį, kad maršruto versiją galima patvirtinti tik tada, jei būdo, taip pat patvirtinama.

### <a name="activating-the-default-route-version"></a>Aktyvinti numatytojo maršruto versiją

Kai aktyvinate maršruto versiją, galite paskirti jį kaip numatytojo maršruto versiją, kurios kapitonas planavimo bus naudojamas arba kad bus naudojamos gamybos užsakymuose. Jūs galite turėti tik vieną aktyvią nukreipimo versiją reikiamam apribojimus (pvz., laiką, svetainę ar kiekis). Jei versiją, kad jūs bandote aktyvinti konfliktų su versija tai jau aktyvus, galite gauti klaidos pranešimą. Norėdami išvengti dviprasmiškų aktyvinimo, turite tada nesuderinamą versiją išaktyvinti arba keisti maršruto versiją suvaržymai (paprastai laikotarpis).

### <a name="electronic-signatures"></a>Elektroniniai parašai

Jei jūs privalote prisijungti kad įrašų, kurie pritaria ir aktyvina kiekvieno maršruto versiją, jums reikia elektroninių parašų už šias užduotis. Vartotojai, kurie patvirtinti ir įjunkite maršruto versijos turės patvirtinti savo tapatybę naudodami, [elektroninio parašo](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Prekės keitimą, kuris naudoja bylų valdymo

Produkto keisti patvirtinimo ir aktyvuoti naują ar pakitusią maršrutai ir maršrutų versijos leidžia lengvai peržiūrėti maršruto versiją apribojimai. Taip pat galite patvirtinti ir suaktyvinti visų maršrutų, kurie yra susiję su konkrečių keisti vienos operacijos ir dokumento rezultatus produkto pokyčių atveju.

## <a name="maintaining-routes"></a>Išsaugoti maršrutai
Priklausomai nuo jūsų verslo poreikius, galėsite sumažinti pastangų, kurio reikia siekiant išlaikyti savo proceso apibrėžimai.

### <a name="making-routes-independent-of-resources"></a>Todėl maršrutų nepriklausomai nuo išteklių

Daugelis sistemų, veiklos išteklių arba išteklių grupę, kuri turėtų atlikti operaciją turi būti nurodytas maršrutas. Vis dėlto Dynamics 365 operacijoms, galite nustatyti tam tikrų reikalavimų, veiklos išteklių turi atitikti taikytiną operacija. Todėl tam tikroms operacijoms išteklių arba išteklių grupę, kuri turėtų būti naudojama neturi būti nustatyta tik operacija iš tikrųjų planuojama. Ši funkcija yra ypač naudinga, kai turite daug darbuotojai arba mašinos, kurios gali atlikti tą pačią operaciją.  

Pvz., galite nurodyti, kad operacija reikalauja operacijos išteklių, kad **mašina** tipą, kuris yra per **štampavimo** 20 tonų pajėgumų. Planavimo modulis bus tada išspręsti šiuos reikalavimus į konkrečias operacijas išteklių arba išteklių grupę, kai planuojama operacija. Nes jūs tiesiog nurodyti šie reikalavimai vietoj privalomos operaciją su konkrečia mašina, jūs turite daug daugiau lankstumo. Be to, išlaikymą bus lengviau, jeigu ištekliai perkeliami arba naujų išteklių pridėta.  

Daugiau informacijos apie įvairių rūšių išteklių poreikius ir kaip juos naudoti, peržiūrėkite operacijos išteklių poreikius ir [išteklių pajėgumus](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Dalintis maršrutai svetainėse

Jei galite gaminti tą patį produktą daugiau nei viename gamybos vietoje, o gamybos produktas yra tas pats visose teritorijose, dažnai galite sukurti bendro naudojimo maršruto, kuris naudojamas visose gamybos svetainėse. Sukurti bendro naudojimo kelias, nėra nurodyti svetainėje maršrutą. Tačiau vis tiek turi sukurti maršruto versiją, kuri sieja bendras maršruto su produkto kiekvienoje vietoje.  

Taip pat įsitikinkite, kad išteklių poreikių kiekvieno maršruto operacija nereikalauja konkrečias operacijas išteklius arba išteklių grupes, bet vietoj to išreiškiami būtini ištekliai charakteristikos. Tada planavimo modulis galės priskirti atitinkamų operacijų išteklius iš svetainės, kurioje planuojama gamybos. Pavyzdžiui, jei yra mažų skirtumų, skaičiuoti laiką, arba sąrankos metu tam tikros operacijos yra konkrečios vietos, šią informaciją galite nurodyti pridedant papildomą operacijos ryšio toje svetainėje.  

Išnaudoti visas bendras maršrutų naudą, taip pat turėtų naudoti išteklių vartojimas atitinkamą komplektavimo specifikacijos (KS). Kai nustatote vėliavos darbo centro suvartojimui KS eilutėje, sandėlio ir vietą, kurioje žaliavų, kurios turi būti vartojamos nuo numanyti operacijų išteklių, kuri veikla planuojama. Todėl sandėlio ir vietoje neturi nustatyti tol, kol iš tikrųjų planuojama gaminti. Tokiu būdu, jūs galite KS ir maršruto nepriklausomai nuo fizinę vietovę, kur auginamas produktas.

### <a name="standard-operation-relations"></a>Standartinei veiklai santykių

Jei jūsų įmonė naudoja standartizuotą veiklą visoje gamybos ir jei yra mažai arba jokio pokyčio nustatymo laikas, vykdymo laikas, sąnaudų skaičiavimui, išlaidų skaičiavimas, ir taip toliau, jums gali būti naudinga sukurti numatytąjį operacijos santykių už visas operacijas. Tokiu atveju nekurti operacijos santykiai, kurie yra būdingi bet kokį maršrutą arba išleido produktą.  

Jei taip pat išreikšti išteklių poreikius, gebėjimus ir pajėgumus, ir padaryti savo maršrutus svetainėje nepriklausomas, gali padėti išlaikyti savo verslo procesus, vykdomos priežiūros iki minimumo.  

Naudojant šį metodą, į **operacijos santykių** puslapis tampa savo pirminės paskirties, išlaikyti veikimo laiką ir kitas ypatybes.

### <a name="resource-specific-process-times"></a>Išteklių konkrečių apdorojimo trukmė

Jei nenurodysite dalis išteklių poreikių operacijos operacijų ištekliu ar išteklių grupe, taikomas išteklių gali veikti skirtingais greičiais. Todėl laikas, kurio reikia, kad galėtume apdoroti operaciją gali skirtis. Norėdami išspręsti šią problemą, galite naudoti su **formulės** lauko operacijos ryšiui nustatyti kaip proceso laikas skaičiuojamas. Galimos toliau nurodytos pasirinktys:

-   **Standartinis** – (Numatytoji parinktis) apskaičiuoti naudoja tik laukai, į operacijos ryšio ir daugina iš užsakymo kiekis nurodytas laikas.
-   **Talpa** – į skaičiavimus įtrauktos į **talpos** lauko iš operacijų išteklių. Todėl laikas yra išteklių požiūriu priklausomomis. Nenurodytas operacijas išteklių reikšmė pajėgumo per valandą. Ši reikšmė yra padauginama iš užsakymo kiekį ir **veiksnys** į operacijos ryšio vertę.
-   **Partijos** – partijos talpa apskaičiuojama naudojant informaciją iš operacijos ryšiui. Partijų ir vykdymo laikas gali tada būti apskaičiuojamos pagal užsakymo kiekį.
-   **Išteklių partijos** – Ši parinktis yra iš esmės tas pats kaip su **partijos** variantą. Tačiau į skaičiavimus įtrauktos į **partijos talpa** lauko iš operacijų išteklių. Todėl laikas yra išteklių požiūriu priklausomomis.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


