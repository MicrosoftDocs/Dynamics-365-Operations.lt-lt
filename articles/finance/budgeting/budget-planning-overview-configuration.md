---
title: Biudžeto planavimo peržiūra
description: Šiame straipsnyje pristatytas biudžeto planavimas ir pateikta informacija, kuri padės konfigūruoti biudžeto planavimą ir nustatyti biudžeto planavimo procesus.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce94f3bbb988640bc53ca2170c7ed54c6c01c18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179069"
---
# <a name="budget-planning-overview"></a>Biudžeto planavimo peržiūra

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pristatytas biudžeto planavimas ir pateikta informacija, kuri padės konfigūruoti biudžeto planavimą ir nustatyti biudžeto planavimo procesus.

<a name="overview-of-budget-planning"></a>Biudžeto planavimo apžvalga
---------------------------

Biudžeto planavimas atliekamas tada, kai sudarinėjate jūsų organizacijoje ketinamus taikyti biudžetus. Organizacija gali konfigūruoti biudžeto planavimą, tada nustatyti biudžeto planavimo procesus, kurie atitiktų jos biudžeto sudarymo strategijas, procedūras ir reikalavimus. 

Kai žinote „Microsoft Dynamics 365 Finance“ naudojamas koncepcijas ir terminus, bus lengviau įgyvendinti biudžeto planavimą savo organizacijoje.

### <a name="key-terms"></a>Pagrindiniai terminai

-   **Biudžeto planavimo procesai** – biudžeto planavimo procesai lemia, kaip biudžeto planus galima naujinti, nukreipti, peržiūrėti ir patvirtinti biudžeto sudarymo organizacijos hierarchijoje. Biudžeto planavimo procesas yra susijęs su biudžeto ciklu ir organizacija per juridinį subjektą.
-   **Biudžeto planai** – biudžeto planuose pateikiami biudžeto ciklo biudžeto duomenys. Jūs galite turėti keletą biudžeto planų, kurie naudojami įvairiems tikslams. Pavyzdžiui, biudžeto planus galima naudoti kuriant skirtingų organizacinių vienetų biudžeto sumas arba jie gali padėti jums atlikti palyginimus ir priimti sprendimus.
-   **Biudžeto plano scenarijai** – biudžeto plano scenarijuose nustatomos biudžeto planų duomenų kategorijos. Galite nurodyti biudžeto plano scenarijus pinigų ir kitų matavimo vienetų klasėms palaikyti, pvz., kiekį. Piniginės išraiškos biudžeto plano scenarijų pavyzdžiams priskirtini Padalinio ankstesnių metų scenarijai ir Padalinio užklausos. Kiekius naudojančių biudžeto planavimo scenarijų pavyzdžiams priskirtini ankstesnių metų techninio aptarnavimo skambučiai ir visos darbo dienos ekvivalento (FTE) įdarbinimo koeficiento skaičiavimas.
-   **Biudžeto planavimo etapai** – biudžeto planavimo etapuose nustatomi veiksmai, kuriuos biudžetas atlieka nuo pat pradžių iki galutinio patvirtinimo. Biudžeto planavimo etapai yra nurodyti biudžeto planavimo darbo eigose.
-   **Biudžeto planavimo darbo eigos** – biudžeto planavimo darbo eigas sudaro ir jose nustatomi biudžeto planavimo etapai. Biudžeto planavimo darbo eigos yra susijusios su biudžeto sudarymo darbo eigomis. Biudžeto sudarymo darbo eigos yra automatizuoti ir neautomatizuoti procesai, perkeliantys biudžeto planus per biudžeto planavimo etapus.

[![Biudžeto planavimo terminologija](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Bendros užduotys

Biudžeto planavimą galima naudoti toliau pateiktoms užduotims atlikti:

-   Kurti biudžeto planus, kad būtų galima nustatyti numatomas biudžeto ciklo įplaukas ir išlaidas.
-   Analizuoti ir atnaujinti kelių scenarijų biudžeto planus.
-   Automatiškai nukreipti biudžeto planus kartu su darbalapiais, pagrindimo dokumentais ir kitais priedais peržiūrai ir patvirtinimui.
-   Konsoliduoti kelis žemesnio organizacijos lygio biudžeto planus į vieną pirminį aukštesnio organizacijos lygio biudžeto planą. Be to, galima sukurti vieną biudžeto planą aukštesniame organizacijos lygyje ir paskirstyti biudžetą žemesniems organizacijos lygiams.

Biudžeto planavimas yra integruotas kituose moduliuose. Todėl galite perkelti ankstesnių biudžetų, faktinių išlaidų, ilgalaikio turto ir personalo informaciją. Kadangi biudžeto planavimas taip pat integruotas programose „Microsoft Excel“ ir „Microsoft Word“, galite naudoti jas dirbdami su biudžeto planavimo duomenimis. Pavyzdžiui, biudžeto vadybininkas gali eksportuoti padalinio biudžeto užklausą iš biudžeto plano scenarijaus į „Excel“ darbalapį. Duomenis galima analizuoti, atnaujinti ir pateikti darbalapyje, o tada publikuoti biudžeto plano eilutėse.

## <a name="configuring-budget-planning"></a>Biudžeto planavimo konfigūravimas
Puslapyje **Biudžeto planavimo konfigūracija** pateikiama dauguma parametrų, kurių jums gali prireikti norint nustatyti biudžeto planavimą. Toliau pateikiamuose skyriuose aprašomi kai kurie pagrindiniai veiksniai, į kuriuos turėtumėte atsižvelgti konfigūruodami biudžeto planavimą. Užbaigę konfigūraciją galite nustatyti biudžeto planavimo procesus.

### <a name="create-a-budget-planning-schema"></a>Biudžeto planavimo schemos kūrimas

Neprivalomas, tačiau rekomenduojamas pirmas veiksmas yra sukurti schemą, kurioje parodoma jūsų organizacijos biudžeto rengimo procedūra. Kurdami šią schemą galite naudoti bet kurį metodą. Toliau pateikiamoje iliustracijoje rodomas bendrasis pavyzdys, kuriame skirtingiems organizacijos lygiams sukuriamos atskiros biudžeto planavimo darbo eigos. Etapai nurodomi kiekvienai darbo eigai ir kiekvienam etapui, kuriame laikomi biudžeto duomenys, priskiriami konkretūs scenarijai. Atliekami veiksmai, skirti perkelti duomenis iš vieno etapo į kitą. Pavyzdžiui, sumas galima paskirstyti arba sujungti į skirtingas sąskaitas, patvirtinimus arba kitas peržiūras. Šiame pavyzdyje pasvirasis tekstas nurodo neredaguotiną etapo scenarijų arba praeities ar ankstesniame etape patvirtintus duomenis, kurie neturėtų būti keičiami. 

[![Biudžeto planavimo bendroji schema](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Šiame pavyzdyje įmonių būstinės įvertina pradinio biudžeto pagrindines sumas ir paskirsto jas pardavimų skyriams. Tada pardavimų skyriai įvertina ir pateikia savo prognozę atgal į būstinę, o biudžeto vadybininkas sujungia ir pakoreguoja prognozę. Galiausiai biudžeto vadybininkas siunčia pakoreguotas biudžeto sumas CFO peržiūrai, galutiniams koregavimams ir patvirtinimui. 

[![Biudžeto planavimo schemos pavyzdys](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Biudžeto planavimo organizacijos hierarchija

Puslapyje **Organizacijos hierarchija** galite nustatyti organizacijos hierarchiją, kuri bus naudojama kaip kiekvieno biudžeto planavimo proceso biudžeto planavimo hierarchija. Biudžeto planavimo hierarchija nebūtinai turi atitikti standartinę organizacijos hierarchiją, kuri naudojama kitiems tikslams. Kadangi ši hierarchija naudojama duomenų sujungimui ir platinimui, galbūt norėsite, kad ji būtų kitokios struktūros. Schemos pavyzdyje pardavimų skyriai priklauso būstinės lygiui, kuriam priklauso biudžeto ir finansų skyriai. Ši struktūra galbūt skiriasi nuo struktūros, kuri naudojama tvarkant pardavimų skyrių operacijas. Kiekvienam biudžeto planavimo procesui gali būti priskirta tik viena organizacijos hierarchija. 

Norėdami gauti daugiau informacijos, žr. [Organizacijos ir organizacijų hierarchijos](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Vartotojo sauga

Apibrėždamas vartotojų teises biudžeto planavimas gali naudoti vieną iš dviejų saugos modelių. Norėdami nurodyti saugos modelį, puslapyje **Biudžeto planavimo konfigūracija** nustatykite biudžeto planavimo parametrą.

### <a name="budget-planning-workflows-stages"></a>Biudžeto planavimo darbo eigų etapai

Biudžeto planavimo darbo eigos naudojamos kartu su biudžeto sudarymo darbo eigomis, kad būtų galima valdyti biudžeto planų kūrimą ir raidą.

Biudžeto planavimo darbo eigą sudaro etapų rinkinys, kuriuos pereina biudžeto planas. Kiekviena biudžeto planavimo darbo eiga yra susijusi su biudžeto sudarymo darbo eiga. Biudžeto sudarymo darbo eigos yra vienas iš „Finance and Operations“ naudojamų darbo eigos tipų. Biudžeto sudarymo darbo eiga siunčia biudžeto planus kartu su darbalapiais, pagrindimais ir priedais per organizaciją peržiūrai ir patvirtinimui. 

Puslapio **Biudžeto planavimo konfigūracija** dalyje **Darbo eigos etapai** sukuriate biudžeto planavimo darbo eigą. Ten galite pasirinkti etapus ir biudžeto sudarymo darbo eigą, kuri bus naudojama, taip pat sukonfigūruoti papildomus parametrus. 

Naudinga sukurti kiekvieno biudžeto sudarymo hierarchijos lygio biudžeto planavimo darbo eigą. Tada priskiriate biudžeto sudarymo darbo eigą, kurioje yra elementų, atitinkančių biudžeto planavimo darbo eigos etapus. Pirmiau šiame straipsnyje pateiktame schemos pavyzdyje viena biudžeto planavimo darbo eiga būtų sukurta pardavimų skyriams, o kita – būstinei. Biudžeto sudarymo darbo eiga perkelia biudžeto planus per etapus. 

Puslapyje **Biudžeto sudarymo darbo eigos** sukuriate biudžeto planavimo biudžeto sudarymo darbo eigą. Procesas panašus į kitų darbo eigų kūrimą. Toliau pateikiamoje iliustracijoje rodomas būstinės darbo eigos pavyzdys. 

[![Biudžeto planavimo biudžeto sudarymo darbo eiga](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Darbo eiga apima paskirstymo pardavimų skyriams elementus ir jų pateikimų sujungimą, biudžeto vadybininko peržiūrą, CFO patvirtinimą ir etapų perėjimus tarp kiekvieno etapo. 

Puslapio **Biudžeto planavimo konfigūracija** dalyje **Darbo eigos etapai** priskiriate biudžeto sudarymo darbo eigą kiekvienai biudžeto planavimo darbo eigai.

### <a name="parameters-scenarios-and-stages"></a>Parametrai, scenarijai ir etapai

Naudodami pradinius puslapio **Biudžeto planavimo konfigūracija** parametrus galite sukurti kelis kūrimo blokus vėlesniems konfigūravimo veiksmams:

-   **Parametrai** – naudojant parametrus nustatomos biudžeto planams norimos taikyti saugos taisyklės ir numatytosios finansinės dimensijos, kurios turėtų būti naudojamos vartotojams detalizuojant biudžeto plano scenarijaus sumas.
-   **Scenarijai** – scenarijai apima norimų biudžeto planų duomenų kategorijas. Galite nurodyti biudžeto plano scenarijus pinigų ir kitų matavimo vienetų klasėms palaikyti, pvz., kiekį. Biudžeto plano scenarijai atitinka vieną biudžeto planavimo duomenų versiją. Piniginės išraiškos biudžeto plano scenarijų pavyzdžiams priskirtini Praėjusių metų pardavimai ir Pasirašytos sutartys. Kiekius naudojančių scenarijų pavyzdžiams priskirtinas pardavimų skambučių skaičius ir visos darbo dienos ekvivalento (FTE) skaičiavimas.
-   **Etapai** – etapais nurodomi biudžeto plano veiksmai nuo pat pradžių iki galutinio patvirtinimo. Biudžeto planavimo etapų pavyzdžiams priskirtinas HQ sumavimas, vyriausiojo finansininko peržiūra ir galutinė suma.

### <a name="allocation-schedules"></a>Paskirstymo grafikai

Planuodami biudžetą galite paskirstyti biudžeto plano eilučių sumas arba kiekius iš vieno scenarijaus į kitą scenarijų arba net į tą patį scenarijų. Pavyzdžiui, galite priskirti tam pačiam scenarijui, jei norite taikyti pakeitimus finansinėms dimensijoms arba to scenarijaus sumų datoms. Paskirstymą galima atlikti biudžeto plane arba iš vieno biudžeto plano į kitą. 

Paskirstymo grafikai automatiškai paskirsto biudžeto plano eilutes, kai apdorojama darbo eiga. Galite atlikti paskirstymus naudodamiesi bet kuriuo iš šių sąrašo **Paskirstymo metodas** metodų:

- <strong>Paskirstyti laikotarpiams</strong> – naudokite laikotarpio paskirstymo raktą, jei norite biudžeto plano eilutes iš šaltinio biudžeto plano scenarijaus paskirstyti po paskirties scenarijaus laikotarpius. <strong>Pastaba.</strong> Prieš paskirstydami laikotarpiams, puslapyje *<strong><em>Laikotarpio paskirstymo kategorijos</em></strong>* turite nustatyti laikotarpių paskirstymo raktus.
- <strong>Paskirstyti dimensijoms</strong> – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus finansinėms dimensijoms paskirties scenarijuje. <strong>Pastaba.</strong> Prieš paskirstydami dimensijoms, puslapyje *<strong><em>Biudžeto paskirstymo sąlygos</em></strong>* turite nustatyti biudžeto paskirstymo sąlygas.
- **Sujungti** – biudžeto plano eilutės sujungiamos iš susietųjų biudžeto planų šaltinio biudžeto plano scenarijaus į pirminio biudžeto plano paskirties scenarijų.
- **Paskirstyti** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus pirminiame biudžeto plane į paskirties scenarijų susijusiuose biudžeto planuose.
- **Naudoti DK paskirstymo taisykles** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus į paskirties scenarijų pagal pasirinktą DK paskirstymo taisyklę.
- **Kopijuoti iš biudžeto plano** – galite pasirinkti kitą biudžeto planą, kuris bus naudojamas kaip paskirstymo šaltinis.

### <a name="stage-allocations"></a>Etapo paskirstymai

Etapo paskirstymai naudojami norint automatiškai paskirstyti biudžeto plano eilutes apdorojant darbo eigą. Naudojant etapo paskirstymus, biudžeto plano eilutės paskirties scenarijuje gali būti sukuriamos ir modifikuojamos nedalyvaujant biudžeto plano rengėjui arba redaktoriui.

Kai nustatote etapo paskirstymą, susiekite biudžeto planavimo darbo eigą ir etapą su paskirstymo grafiku. Biudžeto planavimo darbo eiga turi būti susieta su biudžeto sudarymo darbo eiga, kuri naudoja automatizuotą darbo eigos užduotį *<strong><em>Biudžeto planavimo etapo paskirstymas</em></strong>*. Darbo eigai pasiekus nurodytą etapą, paskirstymas vyksta automatiškai. Šią automatizuotą užduotį galima naudoti kuriant naujo scenarijaus biudžeto plano eilutes. 

Pirmiau šiame straipsnyje pateiktame schemos pavyzdyje paskirstymas atliekamas tam, kad būtų galima perkelti sumas iš biudžeto plano ir scenarijų būstinės pagrindiniame etape į kitą biudžeto planą ir scenarijus pardavimų skyriaus įvertinimo etape. Toliau pateikiamoje iliustracijoje rodomas atitinkamas schemos pavyzdžio skyrius.

[![Etapo paskirstymas](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Be to, schemos pavyzdyje telkimas atliekamas iš etapo Pardavimo skyriaus pateiktas biudžeto planų ir scenarijų į HQ sumavimo etapo pirminį planą. Toliau pateikiamoje iliustracijoje rodomas atitinkamas schemos pavyzdžio skyrius.

[![Telkimas](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioritetai

Pasirinktinai galite naudoti biudžeto plano prioritetus ir galite nurodyti savo nustatytų biudžeto planų kategorijas ir tikslus. Taip pat galite naudoti prioritetus norėdami sisteminti, klasifikuoti ir įvertinti kelis biudžeto planus. Pavyzdžiui, galite sukurti sveikatos ir saugos biudžeto planavimo prioritetą, tada įvertinti tam prioritetui priskirtus biudžeto planus. Taip pat galite priskirti numerį, kad išrikiuotumėte visus biudžeto planus pagal reitingą.

### <a name="columns-and-layouts"></a>Stulpeliai ir maketai

Biudžeto skaičiai rodomi biudžeto plano eilutėse ir stulpeliuose. Pirmiausia turite nurodyti stulpelius, tada galite kurti maketą ir nurodyti stulpelių pateikimą. 

Norėdami nurodyti stulpelį, pasirinkite biudžeto plano scenarijų. To scenarijaus eilutės sumos rodomos biudžeto plane. Pasirinkę laikotarpį galite filtruoti sumą, taip pat galite taikyti DK sąskaita grįstus filtrus. 

Nurodydami maketą pasirinkite DK dimensijų rinkinį, kad galėtumėte sukurti norimas rodyti biudžeto plano eilutes, ir pasirinkite stulpelius kaip maketo elementus. Galite sukurti kelis maketus, kad biudžeto plane būtų rodomi duomenys, kurių norite skirtinguose biudžeto planavimo proceso etapuose. 

Kartu su biudžeto sumų stulpeliais galite nurodyti stulpelius, skirtus biudžeto plano projekto, siūlomo projekto, turto ir siūlomo turto laukams. Taip pat galite nurodyti pareigų biudžeto stulpelį. Ši pasirinktis yra labai naudinga, kai turite analizuoti personalo biudžetus. 

Schemos pavyzdyje galbūt norėsite sukurti scenarijų PY pardavimai, Sutartys ir Prognozė stulpelius (toliau pateikiamoje iliustracijoje rodomas atitinkamas schemos skyrius). Tada galite išskaidyti visus šiuo scenarijus ar vieną iš jų į atskirus stulpelius, skirtus kiekvienam finansinių metų ketvirčiui, kad pardavimų skyriaus vadybininkas galėtų tiksliai įvesti kiekvieno laikotarpio prognozės sumas.

[![Stulpeliai](./media/columns.png)](./media/columns.png) 

Taip pat nurodote, ar galima redaguoti kiekvieną maketo elementą (stulpelį) ir ar tai galima padaryti bet kuriame tam maketui sukurto darbalapio šablone. Schemos pavyzdyje, etapui Vertinimas naudojamame makete, stulpelius Prognozė galima redaguoti, o stulpelius PY pardavimai ir Sutartys galima tik skaityti.

[!Note] Pagal numatytuosius parametrus bus apribota iki 36 stulpelių, nebent pratęsite biudžeto planavimo procesą atlikdami veiksmus, nurodytus [Išplėsti biudžeto planavimo maketą](./extending-budget-planning-layout.md).

### <a name="templates"></a>Šablonai

Puslapio **Biudžeto planavimo konfigūracija** dalyje **Maketai** taip pat galite generuoti, peržiūrėti arba įkelti „Excel“ šablonus. Šie šablonai yra darbaknygės, kurios susietos su kiekvienu biudžeto planu, kad būtų galima pasinaudoti papildomomis analizės, grafiko ir duomenų įvedimo galimybėmis. 

Galite generuoti, peržiūrėti arba įkelti kiekvieno maketo šabloną. Sugeneravus šabloną, maketas užrakinamas ir negali būti redaguojamas. Šis užraktas padeda užtikrinti, kad šablono formatas atitinka biudžeto plano maketą ir kad jame yra tokie patys duomenys. Sugeneravus šabloną, jį galima peržiūrėti ir redaguoti. Pavyzdžiui, į šabloną galite įtraukti diagramų arba toliau tinkinti jo išvaizdą.

> [!NOTE] 
> Šablonas turėtų būti įrašytas į tokią vietą, prie kurios vartotojas turi prieigą, kad baigus redaguoti jį būtų galima įkelti į maketą. Tokiu būdu šablonas bus naudojamas su maketą naudojančiais biudžeto planais.

### <a name="descriptions"></a>Aprašai

Aprašymai, kuriuos galite priskirti skyriuje **Maketai**, naudojami norint rodyti į maketą įtrauktos finansinės dimensijos pavadinimą. Pavyzdžiui, organizacija biudžeto plane pagrindinės sąskaitos pavadinimą gali norėti rodyti prie pagrindinės sąskaitos numerio, bet gali norėti neįtraukti kitų finansinių dimensijų pavadinimų, kad neperpildytų ekrano.

## <a name="setting-up-budget-planning-processes"></a>Biudžeto planavimo procesų nustatymas

Baigę konfigūruoti biudžeto planavimą, puslapyje **Biudžeto planavimo procesas** galite nustatyti biudžeto planavimo procesus. Biudžeto planavimo procesai yra taisyklių rinkiniai, kurie lemia, kaip biudžeto planus galima naujinti, nukreipti, peržiūrėti ir patvirtinti biudžeto sudarymo organizacijos hierarchijoje. 

Kiekvienam biudžeto planavimo procesui pirmiausia pasirinkite biudžeto ciklą ir didžiąją knygą. Kiekvienas biudžeto planavimo procesas yra susijęs tik su vienu biudžeto ciklu ir viena didžiąja knyga. Tada „FastTab“ skirtuke **Biudžeto planavimo proceso administravimas** pasirinkite biudžeto organizacijos hierarchiją ir visiems tinklelyje rodomiems organizacijos atsakingiesiems centrams priskirkite biudžeto planavimo darbo eigą. 

Norėdami priskirti arba pakeisti panašių atsakingųjų centrų biudžeto planavimo darbo eigą, spustelėkite **Priskirti darbo eigą** ir pasirinkite reikiamą organizacijos tipą bei naudotiną biudžeto planavimo darbo eigą. Biudžeto sudarymo darbo eigos ID, susietas su kiekviena biudžeto planavimo darbo eiga, yra automatiškai įtraukiamas į tinklelį. 

Kai „FastTab“ skirtuke **Biudžeto planavimo etapo taisyklės ir maketai** nustatote etapo taisykles ir šablonus, kiekvienam biudžeto planavimo etapui galite nurodyti skirtingus taisyklių ir numatytųjų maketų rinkinius. Pavyzdžiui, naudodami etapą Pardavimų skyriaus įvertinimas vartotojai gali modifikuoti biudžeto plano eilutes, bet negali įtraukti eilučių. Naudodami etapą Pateikta vartotojai gali peržiūrėti eilutes, bet negali jų įtraukti arba modifikuoti, nes tame etape darbas baigtas ir negalima keisti biudžeto planų. Norėdami pasirinkti galimus biudžeto planų maketus, spustelėkite **Alternatyvieji maketai**. 

„FastTab“ skirtuke **Biudžeto plano prioritetų apribojimai** galite pasirinkti biudžeto planavimo prioritetus. Tada galima pasirinkti prioritetus biudžeto planuose. 

Paskutinis veiksmas yra suaktyvinti biudžeto planavimo procesą, naudojant meniu **Veiksmai**. Biudžeto planavimo proceso negalima naudoti, kol jis nesuaktyvintas. 

Meniu **Veiksmai** taip pat galite nukopijuoti esamą procesą ir sukurti naują procesą. Ši funkcija naudinga organizacijoms, kurios kiekvieną biudžeto ciklą naudoja tą patį proceso srautą ir atlieka nedaug pakeitimų arba visai nieko nekeičia. 

Kita naudinga meniu **Veiksmai** komanda yra **Peržiūrėti biudžeto proceso būseną**. Ši komanda grafiškai pavaizduoja biudžeto planus vykstant procesui kartu su atitinkamais duomenimis, pvz., planų darbo eigos būsena, suvestinės pagal sumą ir vienetą ir nukėlimas į pačius biudžeto planus vienu paspaudimu.

[![Biudžeto planavimo proceso būsena](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)



