---
title: "Maršrutai ir operacijos"
description: "Šioje temoje pateikiama informacija apie maršrutus ir operacijas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
ms.author: sorenand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6626540fcf8e39c3cc1c1471fa4bad0bc2fadc24
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="routes-and-operations"></a>Maršrutai ir operacijos

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie maršrutus ir operacijas. Maršrutas apibrėžia produkto arba produkto varianto gaminimo procesą. Jame aprašytas kiekvienas gamybos proceso veiksmas (operacija) ir užsakymas, kuriam šie veiksmai turi būti atlikti. Maršrute taip pat apibrėžti kiekvienam veiksmui reikalingi operacijų ištekliai, reikiamas nustatymo laikas ir vykdymo laikas ir būdas, kaip apskaičiuoti išlaidas.

<a name="overview"></a>Apžvalga
--------

Maršrute aprašyta operacijų tvarka, kuri reikalinga norint pagaminti produktą arba produkto variantą. Maršrute taip pat apibrėžti kiekvienai operacijai reikalingi operacijų ištekliai, operacijai nustatyti ir atlikti reikalingas laikas ir būdas, kaip apskaičiuoti išlaidas. Galite naudoti tą patį maršrutą norėdami pagaminti kelis produktus, arba galite apibrėžti unikalų maršrutą kiekvienam produktui ar produkto variantui. Net galite turėti kelis maršrutus tam pačiam produktui. Tokiu atveju naudojamas maršrutas kinta atsižvelgiant į tam tikrus veiksnius, pvz., kiekį, kurį reikia pagaminti. Maršruto apibrėžtį sprendime „Microsoft Dynamics 365 for Finance and Operations“ sudaro keturi atskiri elementai, kurie visi kartu apibūdina gamybos procesą:

-   **Maršrutas** – maršrutas apibrėžia gamybos proceso struktūrą. Kitaip tariant, jis apibūdina operacijų seką.
-   **Operacija** – operacija identifikuoja įvardintą veiksmą, pvz., **Surinkimas**. Ta pati operacija gali atsirasti keliuose maršrutuose ir gali turėti skirtingus operacijos numerius,
-   **Operacijos ryšys** – operacijos ryšis apibrėžia operacijos veiklos ypatybes, pvz., nustatymo laiką ir vykdymo laiką, savikainos kategorijas, suvartojimo parametrus ir išteklių reikalavimus. Operacijos ryšys įgalina operacijos veiklos ypatybių kitimą, atsižvelgiant į maršrutą, kuriame operacija naudojama, arba į gaminamus produktus.
-   **Maršruto versija** – maršruto versija apibrėžia maršrutą, kuris naudojamas produktui arba produkto variantui pagaminti. Maršrutų versijos leidžia maršrutus tarp produktų naudoti pakartotinai arba laikui bėgant keisti. Jie taip pat įgalina skirtingų maršrutų naudojimą tam pačiam produktui pagaminti. Tokiu atveju naudojamas maršrutas kinta atsižvelgiant tam tikrus veiksnius, pvz., vietą arba kiekį, kurį reikia pagaminti.

## <a name="routes"></a>Maršrutai
Maršrute aprašyta operacijų tvarka, kuri naudojama norint pagaminti produktą arba produkto variantą. Kiekvienai operacijai priskiriamas operacijos numeris ir vėlesnė operacija. Operacijų tvarka suformuoja maršruto tinklą, kurį galima parodyti kaip nurodytą diagramą, turinčią vieną ar daugiau pradžios taškų ir vienas pabaigos taškas. Programoje „Finance and Operations” maršrutai skiriami pagal struktūros tipą. Yra du maršrutų tipai – paprasti maršrutai ir maršrutų tinklai. Gamybos kontrolės parametruose galite nurodyti, ar galima naudoti tik paprastus maršrutus, ar galima naudoti ir sudėtingesnius maršrutų tinklus.

### <a name="simple-routes"></a>Paprasti maršrutai

Paprastas maršrutas yra nuoseklus ir turi tik vieną maršruto pradžios datą.  

[![Paprastas maršrutas](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Jei gamybos kontrolės parametruose įjungiate tik paprastus maršrutus, jums apibrėžiant maršrutą, „Finance and Operations“ automatiškai generuoja operacijų numerius (10, 20, 30 ir t. t.).

### <a name="route-networks"></a>Maršrutų tinklai

Jei gamybos kontrolės parametruose įgalinsite sudėtingesnius maršrutų tinklus, galėsite apibrėžti maršrutus, kurie turi kelias pradžios datas, ir operacijas, kurias galima vykdyti lygiagrečiai.  

[![Maršruto tinklas](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Pastabos**

-   Kiekviena operacija gali turėti tik vieną vėlesnę operaciją, o visas maršrutas turi baigtis viena operacija.
-   Nėra garantijos, kad kelios operacijos, kurios turi tą pačią vėlesnę operaciją (pvz., 30 ir 40 operacijos ankstesnėje iliustracijoje), iš tikro bus vykdomos lygiagrečiai. Pasiekiamumas ir išteklių pajėgumai gali apriboti būdą, kaip operacijos planuojamos.
-   Negalima naudoti 0 (nulio) kaip operacijos numerio. Šis numeris rezervuotas ir yra naudojamas nurodyti tai, kad paskutinė maršruto operacija neturi vėlesnės operacijos.

### <a name="parallel-operations"></a>Lygiagrečios operacijos

Kartais, norint atlikti operaciją, reikia kelių operacijų išteklių su skirtingomis charakteristikomis derinio. Pvz., operacijų rinkiniui gali reikėti įrenginio, įrankio ir vieno darbininko dviem įrenginiams – operacijai peržiūrėti. Šį pavyzdį galima sumodeliuoti naudojant lygiagrečias operacijas, kur viena operacija pažymėta kaip pirminė operacija, o kitos – kaip antrinės operacijos.  

[![Maršrutas, turintis pirminių ir antrinių operacijų](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Paprastai pirminė operacija nurodo ribotosios spartos išteklių ir nustato antrinių operacijų vykdymo laiką. Tačiau planavimo metu, kai apimamas ir ribotas pajėgumas, ir pirminei operacijai, ir antrinėms operacijoms planuojami ištekliai tuo pačiu metu turi būti pasiekiami ir turėti laisvų pajėgumų.  

Ir pirminė operacija, ir antrinės operacijos turi turėti tą patį operacijos numerį (ankstesnėje iliustracijoje – 30).  

Anksčiau pateikiamame pavyzdyje išteklių reikalavimas pirminei operacijai (30) yra įrenginys, tačiau antrinėms operacijoms (30' ir 30'') išteklių reikalavimai yra įrankis ir darbininkas. Penkiasdešimties procentų apkrova leidžia užtikrinti, kad suplanuotas darbininkas galės peržiūrėti du įrenginius vienu metu.

### <a name="approval-of-routes"></a>Maršrutų patvirtinimas

Maršrutas turi būti patvirtintas prieš jį naudojant planavimo ir gamybos procese. Patvirtinimas nurodo, kad maršruto kūrimas baigtas. Tas pats išleistas produktas arba produkto variantas gali turėti kelis patvirtintus maršrutus. Paprastai maršrutas patvirtinamas, patvirtinus pirmąją aktualią maršruto versiją. Tačiau kai kuriais verslo scenarijais maršruto ir maršruto versijos patvirtinimas yra atskiri veiksmai, ir, juos atliekant, gali dalyvauti skirtingi procesų savininkai.  

Galima atskirai patvirtinti arba nepatvirtinti kiekvieną maršrutą. Tačiau, atkreipkite dėmesį, kad, kai maršrutas nepatvirtintas, taip pat nepatvirtintos visos susijusios maršruto versijos. Gamybos kontrolės parametruose galite nurodyti, ar galima nepatvirtinti maršrutų, ar galima patvirtintus maršrutus keisti.  

Jei turite saugoti žurnalą, kuriame užrašyta, kas patvirtino kiekvieną maršrutą, galite reikalauti elektroninių parašų maršrutui patvirtinti. Vartotojai tada savo tapatybę turės patvirtinti naudodami [elektroninį parašą](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

## <a name="operations"></a>„Operations‟
Operacija yra gamybos proceso veiksmas. Sprendime „Finance and Operations“ kiekviena operacija turi savo ID ir paprastą aprašą. Toliau pateikiamose lentelėse nurodyti tipiški operacijų pavyzdžiai iš įrenginių parduotuvės.

| Operacija  | aprašymas        |
|------------|--------------------|
| PipeCut    | Vamzdžių pjaustymas       |
| TIGweld    | TIG suvirinimas        |
| JigAssy    | Veržiamosios pakabos sąranka       |
| Patikrinimas | Kokybės tikrinimas |

Operacijos veiklos ypatybės, pvz., operacijos nustatymo laikas ir vykdymo laikas, išteklių reikalavimas, įkainojimo informacija ir suvartojimo skaičiavimas nurodyti operacijos ryšyje. (Išsamesnės informacijos apie operacijos ryšius žr. kitą skyrių.)

## <a name="operation-relations"></a>Operacijų ryšiai
Toliau nurodytos operacijos veiklos ypatybės prižiūrimos operacijos ryšyje:

-   Išlaidų kategorijos
-   Suvartojimo parametrai
-   Apdorojimo laikas
-   Apdorojimo kiekiai
-   Išteklių reikalavimai
-   Pastabos ir instrukcijos

Tai pačiai operacijai galite nustatyti kelis operacijų ryšius. Tačiau kiekvienas operacijos ryšys yra būdingas vienai operacijai ir parduotuvės ypatybėms, būdingoms maršrutui, išleistam produktui ar išleistų produktų, susijusių su prekės grupe, rinkiniui. Todėl tą pačią operaciją galima naudoti keliuose maršrutuose, turinčiuose skirtingas operacijos veiklos ypatybes. Be to, galite lengviau prižiūrėti savo bendruosius duomenis, jei naudojate standartines operacijas, turinčias tas pačias operacijos veiklos ypatybes, nepaisant to, koks maršrutas naudojamas ir koks produktas gaminamas. Operacijų ryšio aprėptis apibrėžiama ypatybėmis **Prekės kodas**, **Prekės ryšys**, **Maršruto kodas** ir **Maršruto ryšys**, kaip parodyta toliau pateikiamoje lentelėje.

| Prekės kodas | Prekės ryšys         | Maršruto kodas | Maršruto ryšys   | Operacijų ryšio aprėptis                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lentelė     | &lt;Prekės ID&gt;       | Maršrutas      | &lt;Maršruto ID&gt; | Operacijos veiklos ypatybės, kai operacija naudojama maršrute, kur **Maršruto numeris**=&lt;maršruto ID&gt;, siekiant pagaminti išleistą produktą, kai **Prekės numeris**=&lt;prekės ID&gt;.                                                                                                                        |
| Lentelė     | &lt;Prekės ID&gt;       | Visos        |                  | Numatytosios operacijos veiklos ypatybės, kada operacija naudojama siekiant pagaminti išleistą produktą, kai **Prekės numeris**=&lt;prekės ID&gt;. Kitaip tariant, šios operacijų veiklos ypatybės taikomos tada, kai nėra išleisto produkto maršrutui būdingo operacijų ryšio.                                     |
| Grupuoti     | &lt;Prekių grupės ID&gt; | Maršrutas      | &lt;Maršruto ID&gt; | Operacijų veiklos ypatybės, kai operacija naudojama maršrute, kur **Maršruto numeris**=&lt;maršruto ID&gt;, siekiant pagaminti išleistus produktus, kurie susieti su prekių grupe &lt;prekių grupės ID&gt;, nebent yra išleisto produkto operacijų ryšys.                         |
| Grupuoti     | &lt;Prekių grupės ID&gt; | Visos        |                  | Numatytosios operacijų veiklos ypatybės, kai operacija naudojama gaminant išleistus produktus, kurie susieti su prekių grupe &lt;prekių grupės ID&gt;, nebent egzistuoja konkretesnis operacijų ryšys.                                                                                                  |
| Visos       |                       | Maršrutas      | &lt;Maršruto ID&gt; | Numatytosios operacijų veiklos ypatybės, kaip operacija naudojama maršrute, kur **Maršruto numeris**=&lt;maršruto ID&gt;. Kitaip tariant, šios operacijų veiklos ypatybės taikomos tada, kai nėra šio maršruto, kuris būdingas išleistam produktui arba susietai prekių grupei, operacijų ryšio. |
| Visos       |                       | Visos        |                  | Operacijos numatytosios operacijų veiklos ypatybės. Šios operacijų veiklos ypatybės taikomos tada, kai konkretesnis operacijų ryšys neegzistuoja.                                                                                                                                                                |

Be to, galite nurodyti, kad operacijų ryšys yra būdingas svetainei. Tokiu būdu operacijų veiklos ypatybės gali skirtis atsižvelgiant į vietą (t. y., svetainę), kur operacija atliekama. Be to, galite nurodyti sukonfigūruotų produktų kiekvieno produkto konfigūracijos skirtingas operacijų veiklos ypatybes.  

Operacijų ryšiai suteikia daug lankstumo, kai nustatote savo maršrutus. Be to, galimybė nustatyti numatytąsias ypatybes padeda sumažinti bendrųjų duomenų kiekį, kurį turite prižiūrėti. Tačiau, šis lankstumas reiškia ir tai, kad turite turėti omenyje kontekstą, kuriame modifikuojate operacijų ryšį.  

**Pastaba:** dėl to, kad operacijų veiklos ypatybės saugomos kiekvienos operacijos kiekvieno maršruto operacijų ryšiuose, visi tos pačios operacijos pasikartojimai (pvz., Surinkimas) turi tą patį nustatymo laiką, vykdymo laiką, išteklių reikalavimus ir t. t. Todėl jei du operacijos pasikartojimai turi būti tame pačiame maršrute, bet jų vykdymo laikas skirtingas, turite sukurti dvi atskiras operacijas, pvz., 1 surinkimas ir 2 surinkimas.

### <a name="modifying-product-specific-routes"></a>Su konkrečiu produktu susijusių maršrutų keitimas

Kai atidarote puslapį **Maršrutas** iš puslapio **Išleisto produkto informacija**, rodomos tos maršrutų versijos, kurios susietos su pasirinktu išleistu produktu. Šiame kontekste „Finance and Operations“ rodo kiekvienos operacijos veiklos ypatybes iš operacijų ryšio, kurios geriausiai atitinka maršruto versiją. Pastebėsite, kad operacijų sąrašas apima ypatybes **Prekės kodas** ir **Maršruto kodas** iš operacijų ryšių. Todėl galite nustatyti, kuris operacijos ryšys rodomas.  

Puslapyje **Maršrutas** galite keisti operacijų veiklos ypatybes, pvz., vykdymo laiką ar išlaidų kategorijas. Jūsų pakeitimai saugomi operacijų ryšyje, kuris būdingas maršrutui ir išleistam produktui, kurie nurodyti dabartinėje maršruto versijoje. Jei rodomas operacijų ryšys nėra būdingas maršrutui ir išleistam produktui, prieš išsaugant pakeitimus, sistema sukuria operacijų ryšio kopiją. Ši kopija *yra* būdinga maršrutui ir išleistam produktui. Todėl jūsų pakeitimai neturės poveikio kitiems maršrutams ar išleistiems produktams. Norėdami patikrinti, kuris operacijų ryšys yra keičiamas puslapyje **Maršrutas** pažiūrėkite į laukus **Prekės kodas** ir **Maršruto kodas**.  

Beto, galite rankiniu būdu sukurti operaciją, kuri būdinga maršrutui ir išleistam produktui, naudodami funkciją **Kopijuoti ir redaguoti ryšį**.  

**Pastaba:** jei įtrauksite naują operaciją į maršrutą puslapyje **Maršrutas**, operacijų ryšys sukuriamas tik dabartiniam išleistam produktui. Taigi, jei maršrutas naudojamas ir kitiems išleistiems produktams gaminti, nebus jokio taikomo operacijų ryšio šiems išleistiems produktams, o maršruto nebebus galima naudoti tiems išleistiems produktams.

### <a name="maintaining-operation-relations-per-route"></a>Maršruto operacijų ryšių priežiūra

Atidarius puslapį **Maršruto informacija** iš sąrašo puslapio **Maršrutai**, rodomas visų operacijų ryšių, kurie taikomi pasirinktam maršrutui, sąrašas. Todėl galite lengvai patikrinti, kurios operacijų veiklos ypatybės naudojamos kuriems produktams. Galite keisti ir numatytąsias ypatybių vertes, ir produktui būdingų ypatybių vertes.  

Jei įtrauksite naują operacijų ryšį puslapyje **Maršruto informacija**, laukas **Maršruto kodas** automatiškai nustatomas į **Maršrutas**, o laukas **Maršruto ryšys** nustatomas į dabartinio maršruto numerį.

### <a name="maintaining-operation-relations-per-operation"></a>Operacijos operacijų ryšių priežiūra

Iš puslapio **Operacijos** galite atidaryti puslapį **Operacijų ryšiai**. Šiame puslapyje galite keisti visus konkrečios operacijos operacijų ryšius. Galite keisti ir tuos operacijų ryšius, kuriuose yra numatytosios vertės.  

Jei jūsų verslas naudoja standartines operacijas ir jei operacijų veiklos ypatybės yra tos pačios visuose produktuose ir procesuose, puslapyje **Operacijų ryšiai** pateikiamas patogus būdas prižiūrėti šių operacijų numatytąsias operacijų veiklos ypatybes.

### <a name="applying-operation-relations"></a>Operacijų ryšių taikymas

Kai kuriais atvejais „Finance and Operations“ turi rasti operacijos operacijų veiklos ypatybes. Pvz., kai sukuriamas pirkimo užsakymas, kiekvienos operacijos operacijų veiklos ypatybės turi būti nukopijuotos iš operacijų ryšių į gamybos maršrutą. Tokiose situacijose „Finance and Operations“ ieško susijusių operacijų ryšių nuo pačių būdingiausių kombinacijų iki mažiausiai būdingų kombinacijų.  

Kai „Finance and Operations“ ieško išleisto produkto labiausiai susijusių operacijų ryšių, operacijų ryšiui, kuris atitinka išleisto produkto prekės ID, teikiama pirmenybė lyginant su operacijų ryšiu, kuris atitinka prekės grupės ID. Savo ruožtu operacijos ryšys, kuris atitinka prekės grupės ID turi pirmenybę lyginant su numatytuoju operacijų ryšiu. Ieška atliekama toliau nurodyta tvarka:

1.  **Prekės kodas**=**Lentelė** ir **Prekės ryšys**=&lt;prekės ID&gt;
2.  **Prekės kodas**=**Grupė** ir **Prekės ryšys**=&lt;prekių grupės ID&gt;
3.  **Prekės kodas**=**Visi**
4.  **Maršruto kodas**=**Maršrutas** ir **Maršruto ryšys**=&lt;maršruto ID&gt;
5.  **Maršruto kodas**=**Visi**
6.  **Konfigūracija**=&lt;konfigūracijos ID&gt;
7.  **Konfigūracija**=
8.  **Svetainė**=&lt;svetainės ID&gt;
9.  **Svetainė**=

Todėl operacija turėtų būti naudojama tik vieną kartą kiekviename maršrute. Jei tame pačiame maršrute operacija atsiras kelis kartus, visi tos pačios operacijos pasikartojimai turės tą patį operacijos ryšį ir nebus galimos skirtingos kiekvieno pasikartojimo ypatybės (pvz., apdorojimo laikai).

## <a name="route-versions"></a>Maršruto versijos
Maršruto versijos naudojamos, jei norima taikyti variacijas produktų gamybai arba suteikti galimybę labiau kontroliuoti gamybos procesą. Jos apibrėžia, kuris maršrutas turi būti naudojamas, kai gaminamas tam tikras produktas arba išleisto produkto variantas. Galite naudoti šiuos apribojimus norėdami nustatyti, kuris maršrutas naudojamas išleistam produktui:

-   Produkto dimensijos (dydis, spalva, stilius arba konfigūracija)
-   Gamybos kiekis
-   Gamybos svetainė
-   Gamybos data

Kai produktą gaminate tam tikroje svetainėje, tam tikrą jo kiekį arba tam tikru laikotarpiu, galite priskirti tam tikrą maršruto versiją kaip numatytąją maršruto versiją. Tačiau, atkreipkite dėmesį, kad nurodytam išleistam produktui leidžiamas tik vienas maršrutas ir nurodytas apribojimų rinkinys.  

Galite reikalauti, kad gamybos kontrolės parametruose visada būtų nurodytas maršruto versijos galiojimo laikotarpis.

### <a name="approval-of-route-versions"></a>Maršruto versijų patvirtinimas

Maršrutas turi būti patvirtintas prieš jį naudojant planavimo ir gamybos procese. Patvirtindami maršruto versiją, taip pat galite patvirtinti ir susijusį maršrutą. Tačiau atkreipkite dėmesį, kad maršruto versiją galima patvirtinti tik jei susijęs maršrutas irgi patvirtintas.

### <a name="activating-the-default-route-version"></a>Numatytosios maršruto versijos suaktyvinimas

Suaktyvindami maršruto versiją, ją nurodote kaip numatytąją maršruto versiją, kuri bus naudojama bendrojo planavimo metu, arba bus naudojama kuriant gamybos užsakymus. Tam tikram apribojimų rinkiniui (pvz., laikotarpis, svetainė arba kiekis) galima tik viena aktyvi maršruto versija. Jei versija, kurią mėginsite suaktyvinti, bus nesuderinama su jau aktyvia versija, gausite klaidos pranešimą. Siekiant išvengti nevienareikšmiško suaktyvinimo, reikia arba išaktyvinti nesuderinamą versiją, arba modifikuoti maršruto versijos apribojimus (paprastai laikotarpį).

### <a name="electronic-signatures"></a>Elektroniniai parašai

Jei turite saugoti žurnalą, kuriame užrašyta, kas patvirtino ir suaktyvino kiekvieną maršruto versiją, galite šioms užduotims atlikti reikalauti elektroninių parašų. Vartotojai, patvirtinantys ir suaktyvinantys maršruto versiją, savo tapatybę patvirtinti turės naudodami [elektroninį parašą](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

### <a name="product-change-that-uses-case-management"></a>Produkto keitimas naudojant atvejų valdymą

Produkto keitimo atvejis, skirtas tvirtinti ir aktyvinti naujiems ar pakeistiems maršrutams ir maršrutų versijoms, suteikia lengvą būdą apžvelgti maršruto versijos apribojimus. Be to, galite patvirtinti ir suaktyvinti visus maršrutus, susijusius su konkrečiu vienos operacijos pakeitimu, ir dokumentuoti rezultatus produkto keitimo atvejyje.

## <a name="maintaining-routes"></a>Maršrutų priežiūra
Atsižvelgiant į jūsų verslo reikalavimus, galbūt galėsite sumažinti pastangų, kurios reikalingos norint prižiūrėti proceso apibrėžimus.

### <a name="making-routes-independent-of-resources"></a>Maršrutų ir išteklių priklausomumo atsiejimas

Daugelyje sistemų operacijų išteklius arba išteklių grupė, kuri turėtų atlikti operaciją, turi būti nurodyta maršrute. Tačiau sprendime „Finance and Operations“ galite nustatyti reikalavimų rinkinį, kuriuos ištekliai turi atitikti tam, kad galėtų būti taikomi operacijai. Todėl konkretūs operacijos ištekliai ar išteklių grupė, kurie turi būti naudojami, neturi būti nustatyti tol, kol operacija nesuplanuojama faktiškai. Ši funkcija ypač naudinga, turint daug darbininkų arba įrenginių, kurie gali atlikti tą pačią operaciją.  

Pvz., nurodėte, kad operacijai atlikti reikia operacijos ištekliaus, kurio tipas **Įrenginys**, turinčio 20 t pajėgumo **Spaudavimas**. Planavimo mechanizmas tada nustatys šiuos reikalavimus konkrečiam operacijos ištekliui arba išteklių grupei, kada operacija suplanuota. Dėl to, kad galite tik nurodyti šiuos reikalavimus, o ne susieti operaciją su konkrečiu įrenginiu, turėsite daug daugiau lankstumo. Be to, kai resursai perkeliami arba įtraukiamas naujas išteklius – lengvesnė priežiūra.  

Išsamesnės informacijos apie įvairius išteklių reikalavimų tipus ir kaip juos naudoti žr. skyrių Operacijų išteklių reikalavimai [Išteklių pajėgumai](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Maršrutų bendrinimas svetainėse

Jei tą patį produktą gaminate daugiau nei vienoje gamybos vietoje ir jei produkto gamybos veiksmai yra tie patys visose vietose, dažnai galima sukurti bendrinamą maršrutą, naudojamą visose gamybos vietose. Norėdami sukurti bendrinamą maršrutą, vietos nenurodykite pačiame maršrute. Tačiau vis tiek turite sukurti maršruto versiją, kuri susieja bendrinamą maršrutą su gaminiu kiekvienoje vietoje.  

Taip pat turite įsitikinti, kad kiekvienos maršruto operacijos išteklių reikalavimai neprašo konkrečių operacijų išteklių ar išteklių grupių, bet yra išreiškiami pagal reikiamų išteklių charakteristikas. Planavimo mechanizmas tada galės priskirti atitinkamus operacijų išteklius iš tos vietos, kurioje gamyba yra suplanuota. Pvz., jei yra nedidelių vykdymo laiko skirtumų arba, jei tam tikros operacijos nustatymo laikas yra priklausomas nuo vietos, šią informaciją galite nurodyti tai vietai įtraukę papildomą operacijos ryšį.  

Norėdami pasinaudoti visais bendrinamų maršrutų pranašumais, turėtumėte naudoti ir išteklių suvartojimą atitinkamoje komplektavimo specifikacijoje (KS). Kai KS eilutėje nustatote išteklių suvartojimo vėliavėlę, sandėlis ir vieta, iš kurios turėtų būti vartojamos žaliavos, išgaunamos iš operacijos ištekliaus, su kuriuo operacija suplanuota. Todėl sandėlio ir vietos nereikia nustatyti tol, kol gamyba nėra faktiškai suplanuota. Tokiu būdu galite palikti ir KS, ir maršrutą nepriklausomus nuo fizinės vietos, kurioje produktas gaminamas.

### <a name="standard-operation-relations"></a>Standartiniai operacijų ryšiai

Jei jūsų verslo gamyboje naudojamos standartizuotos operacijos, ir jei mažai kinta ar visai nekinta nustatymo laikas, vykdymo laikas, suvartojimo apskaičiavimas, savikainos apskaičiavimas ir t.t., gali būti naudinga visoms operacijoms sukurti numatytuosius operacijų ryšius. Tokiu atveju stenkitės nekurti operacijų ryšių, kurie būdingi kuriam nors maršrutui ar išleistam produktui.  

Be to, jei išreikšite išteklių reikalavimus dėl įgūdžių ir pajėgumų ir padarysite maršrutus nepriklausomus nuo vietos, padėsite iki minimumo sumažinti nuolatinę verslo procesų priežiūrą.  

Naudojant šį būdą, puslapis **Operacijų ryšiai** tampa pirmine vykdymo laiko ir kitų ypatybių priežiūros paskirties vieta.

### <a name="resource-specific-process-times"></a>Ištekliui būdingi apdorojimo laikai

Jei nenurodysite operacijų ištekliaus arba išteklių grupės kaip operacijos išteklių reikalavimų dalies, taikomi ištekliai gali veikti skirtingu greičiu. Todėl laikas, reikalingas operacijai apdoroti, gali skirtis. Norėdami išspręsti šią problemą, naudokite operacijos ryšio lauką **Formulė** nurodyti, kaip apskaičiuojamas apdorojimo laikas. Galimos toliau nurodytos pasirinktys:

-   **Standartinė** – (numatytoji parinktis) skaičiuojant naudojami tik laukai iš operacijos ryšio, ir vykdymo laikas padauginamas iš užsakymo kiekio.
-   **Pajėgumas** – skaičiavimas apima lauką **Pajėgumas** iš operacijos ištekliaus. Taigi, laikas priklauso nuo išteklių. Vertė, kuri nurodyta operacijos ištekliuje, yra pajėgumas per valandą. Ši vertė padauginama iš užsakymo kiekio ir vertės **Koeficientas** iš operacijos ryšio.
-   **Paketas** – paketo pajėgumas apskaičiuojamas naudojant informaciją iš operacijos ryšio. Paketų skaičius, žinoma, ir apdorojimo laikas apskaičiuojami pagal užsakymo kiekį.
-   **Išteklių paketas** – ši parinktis iš esmės tokia pat kaip ir parinktis **Paketas**. Tačiau skaičiavimas apima lauką **Paketo pajėgumas** iš operacijų ištekliaus. Taigi, laikas priklauso nuo išteklių.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[KS ir formulės](bill-of-material-bom.md)

[Išlaidų kategorijos, naudojamos gamybos maršrutuose](../cost-management/cost-categories-used-production-routings.md)

[Išteklių galimybės](resource-capabilities.md)

[Elektroninio parašo apžvalga](../../fin-and-ops/organization-administration/electronic-signature-overview.md)




