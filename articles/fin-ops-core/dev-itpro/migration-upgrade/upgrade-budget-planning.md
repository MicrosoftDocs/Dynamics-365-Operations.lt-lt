---
title: Biudžeto planavimo naujinimas
description: Šiame straipsnyje paaiškinama, ką reikia konfigūruoti iš naujo ir aprašomos naujos priemonės, į kurias reikia atsižvelgti baigus naujinti.
author: panolte
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: panolte
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d098aa77b4eb87118692c18ecd1b09a5de2c53d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890412"
---
# <a name="upgrade-budget-planning"></a>Biudžeto planavimo naujinimas

[!include [banner](../includes/banner.md)]

2012 m. ir " Microsoft Dynamics AX Dynamics 365 Finance" biudžeto planuose esama didelių skirtumų. Kai kurios funkcijos nebuvo atnaujintos, todėl jas reikia perkonfigūruoti. Šiame straipsnyje paaiškinama, ką reikia konfigūruoti iš naujo ir aprašomos naujos priemonės, į kurias reikia atsižvelgti baigus naujinti.  

„Finance“ modulyje Biudžeto planavimas yra daug patobulinimų, kurių nebuvo „Dynamics AX 2012“. Šiame straipsnyje paaiškinami pakeitimai, kuriuos turi atlikti atnaujinę klientai. Joje taip pat nurodomos naujos funkcijos, į kurias reikėtų atsižvelgti atnaujinimo proceso metu. Dėl pakeitimų apimties visi esami biudžeto planai nebus atidaryti, kol nebus atlikti šiame straipsnyje nurodyti pakeitimai. Tačiau ataskaitos turėtų veikti neatlikus papildomų keitimų.

## <a name="overview-of-changes"></a>Keitimų apžvalga
Atlikta daug svarbių „Finance and Operations“ biudžeto sudarymo funkcijos keitimų. Atlikus šiuos keitimus, biudžeto planavimo funkciją turėtų būti lengviau konfigūruoti ir naudoti pakartotinai, todėl kasmetinė priežiūra ir sąranka turėtų atimti mažiau laiko. Toliau nurodytų „AX 2012“ sričių sprendime „Finance“ nebėra.

-   Biudžeto plano šablonai (biudžeto planavimo konfigūracija)
-   Biudžeto plano aplankai (biudžeto planavimo konfigūracija)
-   Scenarijaus apribojimai (biudžeto planavimo konfigūracija)
-   Biudžeto planavimo etapų taisyklių ir šablonų šablonai (biudžeto planavimo procesas)
-   Darbalapių šablonų matricos laukai
-   Biudžeto plano „Microsoft Excel“ šablono vedlys

Kai kurių naujų sampratų negalima tiesiogiai atnaujinti naudojant ankstesnes funkcijas. Todėl turite perkonfigūruoti kai kuriuos parametrus, kad šios naujos koncepcijos veiktų. Toliau pateikiamuose skyriuose aprašomos sampratos, kurios pakeitė ankstesnio sąrašo elementus.

### <a name="columns"></a>Stulpeliai

Stulpeliai yra nauja samprata, pakeičianti „Excel“" šablono ir matricos laukų dalis. Stulpeliuose galima nurodyti laikotarpį, mėnesį, ketvirtį, metus arba visą laiką. Laiko nuoroda yra dinaminė. Ji nurodo laikotarpį ar metus, susijusius su biudžeto procesu. Pavyzdžiui, stulpelis **Praėjusių metų sausio mėn.** nurodo –1 metų 1 ataskaitinį laikotarpį. Stulpelis yra susijęs su konkrečiu biudžeto plano scenarijumi, pvz., faktinės arba biudžeto sumos užklausa.

### <a name="layouts"></a>Maketai

Maketai yra nauja samprata, pakeičianti „Excel“ šabloną. Maketuose yra stulpeliai, nurodantys, kuri biudžeto arba faktinių sumų data ir kuris laikotarpis turi būti rodomi. Taip pat maketus bendrai naudoja klientas ir „Excel“ papildinys. Todėl duomenų įvedimo arba peržiūros vartotojo patirtis „Finance and Operations“ kliente yra geresnė nei vartotojo patirtis „AX 2012“. Norėdami įvesti duomenis į „Finance“ klientą, operacijos rodinyje galite peržiūrėti ir įvesti ne tik vieną scenarijų. Palyginimo rodinyje galite lengvai peržiūrėti ir įvesti kelių laikotarpių ir sąskaitų sumas tuo pačiu metu. Maketus taip pat galima nustatyti, todėl galite įvesti ir peržiūrėti valiutą, komentarus ir kitus papildomus duomenis. Maketai taip pat suteikia galimybę nurodyti, kurios DK dimensijos ir kurie dimensijų aprašymai turi būti rodomi. Maketai taip pat apima scenarijų apribojimus, kad būtų galima nustatyti, kuriuos stulpelius šablone galima redaguoti, o kuriuos stulpelius galima atidaryti programoje „Excel“. Nustačius maketą, sugeneruojamas jo šablonas. Tada šis šablonas sukuria atitinkamą „Excel“ šabloną. Tada galite redaguoti „Excel“ šabloną ir įtraukti daugiau formulių bei formatavimo elementų, o tada – įkelti jį dar kartą. Tada maketai priskiriami kiekvienai etapo taisyklei puslapyje **Biudžeto planavimo procesas**. Todėl maketai pakeičia šablonus, kurie buvo priskiriami ir naudojami panašiu būdu.

### <a name="budget-planning-processes"></a>Biudžeto planavimo procesai

Biudžeto planavimo procesai yra daugiau ar mažiau tokie patys kaip „AX 2012“. Didžiausias skirtumas yra šablonų pakeitimas maketais. Jei yra procesų, kurie anksčiau buvo baigti „AX 2012“, procesų būsena atnaujinama kaip vykdoma, kad būtų galima atlikti keitimus. Turite priskirti maketus, kurių reikės kiekvienai etapo taisyklei, kad būtų galima nustatyti, kurie scenarijai ir laikotarpiai rodomi, kai kliente atidaromas planas. Maketai taip pat nustato, kuris „Excel“ šablonas atidaromas ne sprendime „Dynamic 365 Finance“, kad galėtumėte peržiūrėti biudžetą. **Numatytoji sąskaitos struktūra** yra naujas būtinas biudžeto planavimo proceso laukas. Kiekvienam biudžeto planavimo procesui priskirkite pagrindinę sąskaitos struktūrą, kuri turi būti naudojama sudarant biudžetą.

### <a name="attachments"></a>Priedai

„AX 2012“ pagrindimo dokumentai buvo įrašomi priedų aplanke. Ankstesni pagrindimo dokumentai nėra naujinami. Dabar pagrindimo dokumentai saugomi duomenų bazėje. Jei ši informacija išsaugoma atnaujintoje versijoje, kiekvieno plano galutinio pagrindimo dokumentus galite įkelti naudodami veiksmų srities mygtuką **Pagrindimas**. „AX 2012“ kiekvieno biudžeto plano „Excel“ darbalapiai buvo kuriami pagal šabloną. Sprendime „Finance“ kuriant visus planus atidaroma maketo kopija. Tačiau neįrašomi jokie „Excel“ failo keitimai. Tam tikrame plane naudotas formules arba palaikymo informaciją reikia įtraukti per komentarus, pagrindimo dokumentą arba kitą papildomą procesą.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Atnaujintos aplinkos konfigūravimas naudojant „AX 2012“
Siekiant jums padėti suprasti, kaip konfigūruoti atnaujintą sistemą, tolesniame pavyzdyje naudojamas atnaujintas biudžeto procesas iš „AX 2012“ demonstracinių duomenų. Numatytieji stulpelių konfigūracijos duomenys sukurti tam, kad palengvintų atnaujinimo procesą. Galite atnaujinti arba naikinti šiuos numatytuosius duomenis, jei jie neatitinka jūsų konfigūracijos reikalavimų. **Pastaba:** yra naujų privalomų laukų, kurie sistemoje nustatyti nebus. Jei turite problemų puslapyje, pavyzdžiui, puslapyje **Biudžeto planavimo konfigūracija**, ir negalite puslapio uždaryti, galite uždaryti naršyklę ir tada naršyklėje atidaryti kitą puslapį, kad įvestumėte informaciją teisinga tvarka. Yra privalomų laukų, kurie dar nėra nustatyti. Dėl to gali kilti problemų, kol viskas nebus sukonfigūruota ir nebus nustatyti visi būtini laukai. Šiame straipsnyje paaiškinama, kaip, jei reikia, nustatyti šiuos laukus. Toliau pateikiami keletas šių privalomų laukų.

-   Puslapis **Biudžeto planavimo procesas**: laukas **Numatytoji sąskaitos struktūra**
-   Puslapis **Biudžeto planavimo procesas**: „FastTab“ **Biudžeto planavimo etapo taisyklės ir maketai** laukas **Maketas**

### <a name="define-columns-and-layouts"></a>Stulpelių ir maketų nustatymas

1. Puslapyje **Biudžeto planavimo konfigūracija** spustelėkite skirtuką **Stulpeliai**. Atlikus atnaujinimą nauji stulpeliai automatiškai kuriami pagal jūsų biudžeto plano eilutes. Dabar stulpeliuose naudojamos dinaminės datos, kurių laikas ir metai yra paslenkami nuo finansinių metų, nustatytų biudžeto planavimo procese. **Pastaba:** siekiant padidinti efektyvumą atnaujinimo metu laikoma, kad visi biudžeto ciklai sudaro kalendorinius metus, o ne finansinius metus. Jei naudojate finansinius metus, turite redaguoti ir tinkamai susieti stulpelius jų finansiniais metais. Pavyzdžiui, toliau nurodyti elementai buvo teikiami „AX 2012“.
   -   Biudžeto plano scenarijai: Faktinės sumos, Bazinė suma, Biudžeto užklausa, Patvirtintas biudžetas
   -   Biudžeto plano eilutes visiems scenarijams 2017 m., o faktinės sumos – 2017 m. ir 2016 m.

   Sprendime „Finance and Operations“ bus sukurti toliau nurodyti stulpeliai.

   | Stulpelio pavadinimas    | Biudžeto plano scenarijus | Stulpelio laikotarpis | Metų poslinkis |
   |----------------|----------------------|--------------------|-------------|
   | Sausio mėn. 1 scenarijus | Faktinės reikšmės              | 1                  | 0           |
   | Sausio mėn. 2 scenarijus | Bazinė linija             | 1                  | 0           |
   | Sausio mėn. 3 scenarijus | Biudžeto užklausa       | 1                  | 0           |
   | Sausio mėn. 4 scenarijus | Patvirtintas biudžetas      | 1                  | 0           |
   | Sausio mėn. 5 scenarijus | Faktinės reikšmės              | 1                  | -1          |
   | Vasario mėn. 1 scenarijus | Faktinės reikšmės              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   Šiame pavyzdyje sukuriamas stulpelis pavadinimu **Sausio mėn. 1 scenarijus** ir priskiriamas naujausiems rastiems biudžeto plano operacijų duomenims iš sausio mėn. operacijų. Panašus stulpelis sukuriamas kiekvienu scenarijumi, kai yra duomenų. Kai sukurti visų tų metų laikotarpių stulpeliai, kuriami ankstesnių metų stulpeliai.
2. Keiskite stulpelių pavadinimus ir aprašymus bei bet kokią kitą informaciją neautomatiniu būdu kliente arba atlikdami masinius naujinimus „Excel“papildinyje, kuris nurodo biudžeto plano stulpelių duomenų objektą. Dabar visi anksčiau nustatyti matricos laukų filtrai nustatomi stulpeliuose.
3. Sukurkite naują biudžeto plano maketą. Maketas nurodo kelis stulpelius, kad būtų galima nustatyti „Excel“ir kliente rodomą rodinį. Pirmiausia reikia nurodyti maketo DK dimensijų rinkinį, kad būtų galima nustatyti, kurias finansines dimensijas galima įvesti. Nurodę dimensijų rinkinį, spustelėkite **Aprašai** ir pasirinkite į maketą įtrauktinus dimensijų aprašus.
4. „FastTab“ **Maketo elementai** spustelėkite **Įtraukti**, kad įtrauktumėte kiekvienos eilutės duomenis, pvz., valiutą, komentarą arba biudžeto klasę, nurodančius įplaukų ir išlaidų eilutes. Tada įtraukite laikotarpio stulpelius ir scenarijus, kurie taikomi šiam biudžeto ciklui ir etapui. Šiuos keitimus galite atlikti neautomatiniu būdu kliente arba naudodami „Excel“papildinį, kuris nurodo biudžeto plano maketo elementų duomenų objektą.
5. Kiekviename maketo elemente pasirinkite, ar stulpelis turėtų būti redaguojamas ir ar jis turėtų būti rodomas šio maketo „Excel“ darbaknygėje. **Pastaba:** tvarkydami retrospektyvinius planus galbūt norėsite naudoti maketą, kuriame rodoma to proceso bet kurio biudžeto plano scenarijaus 12 mėnesių stulpelių.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Biudžeto planavimo procesų naujinimas norint naudoti tinkamą kiekvieno biudžeto etapo maketą

1.  Puslapyje **Biudžeto planavimo procesas** pasirinkite konfigūruotiną procesą.
2.  Veiksmų srityje spustelėkite **Redaguoti**.
3.  Nurodykite numatytąją šio biudžeto proceso sąskaitos struktūrą. **Numatytoji sąskaitos struktūra** yra naujas būtinas laukas, kurį reikia nustatyti.
4.  „FastTab“ **Biudžeto planavimo etapo taisyklės ir maketai** lauke **Maketas** pasirinkite maketą, kuris buvo sukonfigūruotas anksčiau ir tinka šiam etapui.
5.  Tada pasirinkite tuos pačius arba kitus įvairių biudžeto planavimo etapų maketus ir įrašykite keitimus.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Papildomos funkcijos, į kurias reikėtų atsižvelgti biudžeto sudarymo procese
### <a name="budget-planning-workspace"></a>Biudžeto planavimo darbo sritis

Ši darbo sritis yra skirta biudžeto savininkui ir atskiriems biudžeto bendrasavininkams. Joje pateikiami saitai į visus jums aktualius biudžeto dokumentus. Taip pat joje yra biudžeto proceso ataskaitos ir pagrindiniai efektyvumo indikatoriai (KPI). Biudžeto administratorius gali nustatyti visų vartotojų dabartinį biudžeto planavimo procesą puslapyje **Biudžeto sudarymo parametrai**. Skirtuko **Darbo srities parametrai** „FastTab“ **Biudžeto planavimas** yra laukas, kuriame galite pasirinkti biudžeto planavimo procesą.

### <a name="alternate-layouts"></a>Alternatyvūs maketai

Alternatyvūs maketai yra nauja funkcija, kuri suteikia galimybę peržiūrėti planus naudojant skirtingus maketus. Galima leisti pasirinkti vieną arba daugiau maketų. Tada galite peržiūrėti biudžeto planą naudodami mėnesio maketą arba ketvirčio maketą. Alternatyvūs maketai nustatomi puslapio **Biudžeto planavimo procesas** „FastTab“ **Biudžeto planavimo etapo taisyklės ir maketai laukas**.

### <a name="budget-milestones"></a>Biudžeto etapai

Vykdant biudžeto procesą labai svarbu suprasti pagrindines datas ir galutinius terminus. Dabar galite konfigūruoti datas, įtraukdami jų aprašus. Šiuos aprašus biudžeto sudarymo vartotojai matys atidarydami biudžetus ir norėdami redaguoti arba peržiūrėti jiems priskirtus elementus.

### <a name="copy-from-budget-plan-allocation"></a>Paskirstymas Kopijuoti iš biudžeto plano

Naujas paskirstymo metodas suteikia galimybę paskirstyti iš pirminio plano į antrinį planą, kai tarpinio hierarchijos lygio veiksmų atlikti nereikia. Šis metodas yra ypač naudingas klientams, kurie anksčiau sukūrė finansinę dimensiją tik tam, kad paskirstytų ir tvirtintų biudžetą.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Biudžeto planų generavimas pagal naujus biudžeto šaltinius

Toliau nurodytos parinktys įtrauktos kaip periodiniai procesai. Šios parinktys suteikia galimybę generuoti biudžeto planą, kaip pradinį tašką naudojant esamus duomenis iš kito modulio.

-   Biudžeto plano generavimas pagal poreikio prognozę
-   Biudžeto plano generavimas pagal tiekimo prognozę
-   Biudžeto plano generavimas pagal projektą
-   Biudžeto plano generavimas pagal biudžeto registrą

### <a name="more-complete-tracking-of-amounts"></a>Išsamesnis sumų sekimas

„AX 2012“ planuojant biudžetą buvo saugoma viena kiekvienos reikšmės biudžeto plano suma. Buvo išplėstas „Finance“ duomenų modelis. Dabar kiekviena vertė pateikiama apskaitos valiuta, operacijos valiuta ir ataskaitų valiuta. Atnaujinimo metu šie nauji stulpeliai užpildomi automatiškai pagal esamus duomenis.

### <a name="do-not-convert-currency-in-aggregation"></a>Nekonvertuoti valiutos, kai naudojama telkimo funkcija

Paprastai, kai antrinis planas sujungiamas su pagrindinio lygio planu, sumos automatiškai konvertuojamos iš operacijos valiutos į organizacijos apskaitos valiutą. Kai parinktį **Nekonvertuoti valiutos, kai naudojama telkimo funkcija** nustatote į **Ne**, sujungtos sumos pateikiamos pradine valiuta. Todėl ši parinktis suteikia galimybę pateikti tikslesnius koregavimus, kurie atspindi valiutos kurso svyravimus.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Žvelgimas atgal iš biudžeto plano į kitus modulius, kurie sudarė biudžetą

Biudžeto planus galima generuoti pagal poreikio arba tiekimo prognozes, projektą ir kitas sritis. Galima naudoti kelias užklausos Biudžeto planai pagal dimensijų rinkinį parinktis, norint pateikti užklausą biudžeto plano šaltinio duomenims nustatyti.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Perrašymas arba prijungimas prie paskirstymo grafikų plano

Jei yra keli sumų, kurias reikia paskirstyti, šaltiniai, galite nurodyti, kad sumos turi būti sudedamos. Tokiu atveju sumos neperrašo esamų sumų. Jos esamas sumas prijungia.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Biudžeto planavimo konfigūracijos numatytasis finansinių dimensijų rinkinys

Į puslapį **Biudžeto planavimo konfigūracija** dabar įtrauktas laukas, kuriame galite nurodyti numatytąjį finansinių dimensijų rinkinį. Nors šis laukas nėra privalomas, teikiant tam tikras užklausas jį gali reikėti užpildyti. Taip pat jį gali reikėti užpildyti, jei norite grupuoti arba filtruoti ataskaitų grupavimą pagal dimensijų rinkinį.

### <a name="data-entities"></a>Duomenų objektai

Įtraukti keli duomenų objektai, kad būtų pagreitintas biudžeto planavimo diegimas. Objektai taip pat suteikia galimybę atlikti daug pakeitimų naudojant „Excel“. Todėl kliente nereikia elementų kurti po vietą. Čia pateikiamas naujų duomenų objektų sąrašas.

-   Objekto pavadinimas
-   Biudžeto parametrai
-   Biudžeto plano parametras
-   Biudžeto plano scenarijai
-   Biudžeto plano etapai
-   Biudžeto plano darbo eigos etapas
-   Biudžeto plano paskirstymo grafikai
-   Biudžeto plano etapų paskirstymai
-   Biudžeto plano prioritetai
-   Biudžeto plano stulpeliai
-   Biudžeto plano maketo elementai






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]