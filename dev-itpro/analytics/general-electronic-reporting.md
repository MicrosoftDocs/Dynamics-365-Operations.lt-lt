---
title: "Elektroninių ataskaitų apžvalga"
description: "Šiame straipsnyje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Elektroninių ataskaitų apžvalga

Šiame straipsnyje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis.

Elektroninės ataskaitos (ER) – tai įrankis, kurį naudodami galite konfigūruoti elektroninių dokumentų formatus pagal įvairių šalių ir regionų teisinius reikalavimus. ER suteikia galimybę valdyti šiuos formatus per jų naudojimo ciklą. Pavyzdžiui, galite pritaikyti naujus teisinius reikalavimus ir generuoti verslo dokumentus reikiamu formatu, skirtu keistis informacija su valdžios institucijomis, bankais ir kitomis šalimis elektroniniu būdu. ER mechanizmas skirtas verslo vartotojui, o ne kūrėjui. Kadangi galite konfigūruoti formatus, o ne kodus, elektroninių dokumentų formatų kūrimo ir pritaikymo procesas greitesnis ir lengvesnis. ER šiuo metu palaiko TEXT, XML ir OPENXML darbalapio formatus. Tačiau naudojant plėtinio sąsają palaikoma daugiau formatų.

## <a name="capabilities"></a>Galimybės
ER mechanizmas turi toliau nurodytas galimybes.

-   Ji atstovauja viena bendra priemonė elektroninių ataskaitų skirtinguose domenuose, ir pakeičia daugiau nei 20 skirtingų variklių, ar kokios nors rūšies elektroninių ataskaitų Microsoft Dynamics "365" operacijoms.
-   Tai leidžia izoliuoti nuo dabartinių Dynamics 365 operacijų įgyvendinimo ataskaitų formato. (Kitaip tariant, formatas yra taikomas skirtingas versijas Dynamics 365 operacijų.)
-   Jis palaiko pasirinktinio formato kūrimą pagal jo pradinę versiją. Jis apima galimybes automatiškai naujinti tinkintą formatą, kai pradinis formatas pasikeičia dėl įvestų lokalizavimo / tinkinimo reikalavimų.
-   Jis tampa pagrindiniu standartiniu „Microsoft“ ir „Microsoft“ partnerių elektroninių ataskaitų lokalizavimo reikalavimus palaikančiu įrankiu.
-   Jis palaiko galimybę paskirstyti formatus partneriams ir klientams naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="concepts"></a>Koncepcijos
### <a name="components"></a>Komponentai

ER palaiko dviejų tipų komponentus: **Duomenų modelis** ir **Formatas**.

#### <a name="data-model-components"></a>Duomenų modelio komponentai

Duomenų modelio komponentas abstrakčiai vaizduoja duomenų struktūrą ir yra naudojamas tam tikrai verslo domeno sričiai aprašyti pakankamai išsamiai, kad būtų tenkinami tos srities ataskaitų reikalavimai. Duomenų modelio komponentą sudaro toliau nurodytos dalys.

-   Duomenų modelis kaip domenui būdingų verslo objektų rinkinys ir hierarchiškai susistemintas jų ryšių aprašas
-   Modelio atvaizdavimo, kad nuorodos pasirinkta Dynamics 365 operacijų duomenų šaltiniu, prie atskirų elementų duomenų modelis, nurodantis, vykdymo metu, duomenų srauto ir taisyklių verslo duomenis gyventojų į duomenų modelio komponentas.

Duomenų modelio verslo objektas pateikiamas kaip konteineris (įrašas). Verslo subjekto ypatybės pateikiamos kaip duomenų elementai (laukai). Kiekvienas duomenų elementas turi unikalų pavadinimą, žymę, aprašą ir reikšmę. Kiekvieno duomenų elemento reikšmė gali būti sukurta taip, kad būtų atpažinta kaip eilutė, sveikasis skaičius, realusis skaičius, data, išvardijimo tipas, bulio logika ir t. t. Be to, tai gali būti kitas įrašas arba įrašų sąrašas. Viename duomenų modelio komponente gali būti kelios domenui būdingų verslo objektų hierarchijos, taip pat modelio susiejimai, kad vykdymo metu būtų palaikomas konkretus ataskaitai būdingas duomenų srautas. Hierarchijos yra atskiriamos pagal vieną įrašą, kuris buvo pasirinktas kaip šakninis modelio susiejimo įrašas. Pavyzdžiui, mokėjimo domeno srities duomenų modelis gali palaikyti tolesnius susiejimus.

-   Įmonės -&gt; tiekėjas -&gt; mokėjimo operacijų AP domeno
-   Klientas -&gt; bendrovė -&gt; mokėjimo operacijas AR domeno

Atkreipkite dėmesį, kad verslo subjektai (pvz., Įmonė ir Mokėjimo operacijos) yra sukurtos vieną kartą. Tada kiti susiejimai pakartotinai juos naudoja. Toliau pateikiamos modelio susiejimo galimybės.

-   Jį galite naudoti įvairių Dynamics 365 operacijų duomenų tipų duomenų šaltinių duomenų modelis. Pavyzdžiui, jis gali naudoti lenteles, duomenų objektus, metodus ar išvardijimus.
-   Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo metu.
-   Jis palaiko Dynamics 365 transformacijos operacijos duomenų į reikalinga organizacijoms, filtravimas, rūšiavimas ir sumuojant duomenis, ir taip pat pridėtos su logiškai apskaičiuoti laukai, kurie skirti per Microsoft Excel, kaip formulės (daugiau informacijos rasite [formulių kūrimo priemonę, elektroniniai pranešimai](general-electronic-reporting-formula-designer.md)).

[!["Excel" pavidalo formulių redaktorius](./media/pic-formula-1024x615.png)](./media/pic-formula.png) duomenų modelio komponentas yra skirtas kiekvienam verslo domeno, kuris turėtų būti naudojamas kaip vieninga duomenų šaltinis apie, kuris izoliuoja reportažus iš fizinio įgyvendinimo Dynamics 365 operacijų duomenų šaltinių, ir yra konkreti verslo koncepcija ir tokia forma, kuri leidžia duomenų pateikimo formatas eskizo ir tolesnei priežiūrai, efektyviau funkcijų.

#### <a name="format-components"></a>Formato komponentai

Formato komponentas yra ataskaitų kūrimo planas, kuris bus generuojamas vykdymo metu. Schemą sudaro toliau nurodyti elementai.

-   Formatas, kuris apibrėžia vykdymo metu sugeneruoto elektroninio ataskaitos dokumento struktūrą ir turinį
-   Duomenų šaltiniai kaip vartotojo įvesties parametrų rinkinys ir domenui būdingų duomenų modelis, kuris naudoja pasirinktą modelio susiejimą.
-   Formato susiejimas kaip formato duomenų šaltinių susiejimų su atskirais formato elementais, vykdymo metu nurodančiais duomenų srautą ir formato išvesties generavimo taisykles, susiejimų rinkinys.
-   Formato tikrinimas kaip konfigūruojamų taisyklių, kurios vykdymo metu valdo ataskaitos generavimą pagal vykdymo kontekstą, rinkinys (pvz., taisyklė, kuri sustabdo tiekėjo mokėjimų išeigos generavimą ir pritaiko išimtį, jei trūksta konkrečių pasirinkto tiekėjo atributų, pvz., banko sąskaitos numerio).

Formato komponentas palaiko tolesnes funkcijas.

-   Ataskaitos išeigos kaip atskirų skirtingų formatų (teksto, XML ar darbalapio) failų kūrimas
-   Kelių failų kūrimas atskirai, taip pat tų failus glaudinimas į „zip“ failus

Formato komponentas suteikia galimybę pridėti tam tikrus failus, kurie gali būti naudojami ataskaitų išeigoje toliau nurodytais būdais.

-   „Excel“ darbaknyges, kuriose yra darbalapis, galima naudoti kaip OPENXML darbalapio formato išeigos šabloną
-   Kiti failai, kurie gali būti įtraukti į formato išeigą kaip iš anksto apibrėžti failai

#### <a name="component-versioning"></a>Komponento versijos kūrimas

Palaikomas ER komponento versijos kūrimas. Toliau pateikta ER komponentų pakeitimų valdymo darbo eiga.

-   Pradinė sukurta versija pažymima kaip **JUODRAŠTIS**. Šią versiją galima redaguoti ir ją galima tikrinti.
-   Versiją **JUODRAŠTIS** galima konvertuoti į versiją **BAIGTA**. Šią versija galima naudoti vietiniuose ataskaitų teikimo procesuose.
-   Į **atlikta** versija gali būti konvertuojamos į a **bendro naudojimo** versija. Ši versija skelbiama ant LCS ir gali būti naudojamas pasauliniu atskaitomybės procesuose.
-   Versiją **BENDRAI NAUDOJAMA** galima konvertuoti į versiją **NEBENAUDOJAMA**. Tada šią versiją bus galima naikinti.

Versijų, kurios turi turėti ** atlikta ** ar **bendro naudojimo** statusas nėra kitų duomenų mainams. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

-   Jie gali būti serializowany į XML formato ir eksportuoti iš Dynamics 365 operacijoms kaip failą XML formatu.
-   Jie gali būti reserialized iš XML failo ir importuojamas į Dynamics 365 operacijoms kaip sudedamoji ER nauja versija.

#### <a name="component-date-effectivity"></a>Komponento galiojimo data

ER komponento versijos turi galiojimo datą. Galima apibrėžti ER komponento datą** Galioja nuo**, norint nurodyti datą, nuo kurios šis komponentas galioja, ir jį galima naudoti ataskaitų teikimo procesuose. Dynamics 365 operacijų seanso datą yra naudojamas nustatyti, ar komponentas galioja vykdymo. Jei konkrečią dieną galioja daugiau nei viena versija, ataskaitų teikimo procesuose naudojama naujausia versija.

#### <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato komponentų priklauso nuo ISO valstybės / regiono kodo parametro. Kai šis parametras yra tuščias, jei pasirinkta versija formatas konfigūracijos, formatas komponentas galima pasiekti bet Dynamics 365 operacijų bendrovės vykdymo metu. Kai šis parametras yra ISO šalies/regiono kodus, formatas komponentas yra prieinamas tik iš Dynamics 365 veiklą įmonėms, kurios yra pagrindinis adresas, kuris yra apibrėžta naudoti formatą komponento ISO šalies/regiono kodus. Skirtingos duomenų formato komponento versijos gali turėti skirtingus ISO valstybės / regiono kodų parametrus.

#### <a name="configuration"></a>Konfigūravimas

ER konfigūracija yra tam tikro ER komponento (**Duomenų modelis** arba **Formatas**) aplankas. Konfigūracija gali apimti skirtingas tam tikro ER komponento versijas. Kiekviena konfigūracija pažymėta kaip priklausanti konkrečiam konfigūracijos teikėjui. Į **projektu** konfigūracijos komponento versija gali būti redaguojami, kai konfigūracijos savininkas buvo pasirinktas kaip active teikėjas ER parametruose Dynamics 365 operacijoms. Kiekvienoje modelio konfigūracijoje yra komponentas **Duomenų modelis**. Naują formato konfigūraciją galima išvesti (gauti) iš konkrečios duomenų modelio konfigūracijos. Sukurta formato konfigūracija konfigūracijos medyje bus pateikta kaip antrinė pradinės duomenų modelio konfigūracijos konfigūracija. Sukurtoje formato konfigūracijoje yra komponentas **Formatas **. Pirminės modelio konfigūracijos komponentas **Duomenų modelis** yra automatiškai įterpiamas į antrinės formato konfigūracijos komponentą **Formatas **kaip numatytasis duomenų šaltinis. ER konfigūracija yra bendrinamas Dynamics "365" veiklos įmonėms.

#### <a name="provider"></a>Teikėjas

ER teikėjas yra šalies identifikatorius, naudojamas kiekvienos ER konfigūracijos autoriui (savininkui) nurodyti. ER suteikia galimybę valdyti konfigūracijos teikėjų sąrašą. Formatuoti konfigūracijų, kuris yra išleistas į elektroninių dokumentų kaip Dynamics 365 operacijų tirpalo dalis pažymėtos kaip priklauso, **"Microsoft"** teikėjo konfigūracijos.

#### <a name="repository"></a>Saugykla

ER saugykloje saugomos ER konfigūracijos. Šiuo metu palaikomi šių tipų ER saugyklas: **operacijų išteklius** ir **LKD projektas**. Yra ** operacijos išteklių ** saugyklos suteikia prieigą prie sudėčių, išleisti ER konfigūracijos teikėjas Microsoft Dynamics 365 operacijų tirpalo dalis sąrašą. Šias konfigūracijas gali būti importuojami į dabartinę Dynamics 365 operacijų atveju ir naudojami elektroniniai pranešimai. Taip pat jas galima naudoti tolesniam lokalizavimui / tinkinimui atlikti. **LCS projekto** saugykla suteikia prieigą prie tam tikro LCS projekto (LCS projekto turto bibliotekos), pasirinkto saugyklos registracijos etape, konfigūracijų sąrašo. ER leidžia jums įkelti bendrai naudojamą konfigūracijos iš dabartinės Dynamics 365 operacijų atveju konkrečiam **LKD projektas** saugykloje. Taip pat galite importuoti konfigūracijos iš konkretaus **LKD projektas** saugyklos į dabartinę Dynamics 365 operacijų atveju. Reikalingas **LKD projektas** saugyklas galima registruoti atskirai kiekvienos konfigūracijos teikėjas dabartinė dinamika 365 operacijų atveju. Kiekvieną saugyklą galima priskirti konkrečiam konfigūracijos teikėjui.

## <a name="supported-scenarios"></a>Palaikomi scenarijai
### <a name="building-a-data-model"></a>Duomenų modelio kūrimas

ER teikia modelių kūrimo įrankį, kurį galite naudoti konkrečiam verslo domenui skirtam duomenų modeliui kurti. Visus domenui būdingus verslo objektus ir jų ryšius galima pateikti duomenų modelyje kaip hierarchinę struktūrą. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio pavyzdys (mokėjimo domeno duomenų modelis). [![Duomenų modelio pavyzdys](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) turi būti susipažinę su informacija apie šį scenarijų, žaisti su **ER dizainas domeno konkrečių duomenų modelis** užduoties vadovas (dalis su **7.5.4.3 Acquire/plėtoti IT paslaugų/sprendimų komponentai (10677)** verslo procesų).

### <a name="translating-data-model-content"></a>Duomenų modelio turinio vertimas

Duomenų modelio turiniu (etiketes ir aprašymai) gali išversta į kitas kalbas, palaikančią Dynamics 365 operacijoms. Duomenų modelio turinį galite norėti išversti dėl toliau nurodytų priežasčių.

-   Norint, kad kita kalba kalbantys formato kūrėjai, kurie naudos duomenų modelį formato komponentų duomenims susieti, kurdami lengviau suprastų turinį
-   Ne darbo laiko, kad turinys vartotojui draugiškas pateikiant raginimus ir padėti vykdymo laiko parametrų, ir taip pat sukonfigūruotas patikrinimo pranešimų (klaidos ir įspėjimai), kalba šiuo metu įėjęs Dynamics 365 operacijų vartotojas pageidauja

Tolesnėje iliustracijoje pateikiamas pavyzdys, kaip duomenų modelio turinį galima išversti iš anglų k. į japonų k.. [![Duomenų modelio turinys anglų kalba](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![duomenų modelio turinio išversta į japonų](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Duomenų modelio susiejimų konfigūravimas

ER numato modelio atvaizdavimo dizaineris, kuris leidžia vartotojams priskirti konkrečių Dynamics 365 operacijų duomenų šaltinių duomenų modelius, kad jie sukūrė. Tolesnėje iliustracijoje pateikiamas tokio tipo duomenų modelio susiejimo pavyzdys (mokėjimo domeno duomenų modelio **SEPA kredito pervedimo** modelio susiejimas). [![Duomenų modelio atvaizdavimo pavyzdys ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png)susipažinti su informacija apie šį scenarijų, žaisti su **ER apibrėžti modelio atvaizdavimo ir pasirinkite duomenų šaltinius** ir **ER žemėlapyje duomenų modelio prie pasirinktų duomenų šaltinių** užduočių vadovai (dalis su **7.5.4.3 Acquire/plėtoti IT paslaugų/sprendimų komponentai (10677)** verslo procesų).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Sukurto modelio komponento saugojimas kaip modelio konfigūracijos

ER gali saugoti sukurta duomenų modelis kartu su susijusių duomenų susiejimų kaip dabartinis Dynamics 365 operacijų atveju, modelio konfigūracija. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio konfigūracijos pavyzdys (mokėjimo duomenų modelio konfigūracija). [![Duomenų modelio konfigūracijos pavyzdys ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png)susipažinti su informacija apie šį scenarijų, žaisti su **ER žemėlapyje duomenų modelio prie pasirinktų duomenų šaltinių** užduoties vadovas (dalis su **7.5.4.3 Acquire/plėtoti IT paslaugų/sprendimų komponentai (10677)** verslo procesų).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Formato kūrimas pasirenkant duomenų modelį kaip pagrindą

ER palaiko formato kūrimo įrankį, kurį galima naudoti norint kurti pasirinkto verslo domeno konkretaus elektroninio dokumento formatą pasirenkant modelio komponentą kaip pagrindą. Tas pats ER formato kūrimo įrankis teikia galimybę sukurtą formatą susieti su pasirinkto domeno duomenų modelio susiejimu kaip duomenų šaltiniu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys (formato konfigūracija, kad būtų palaikomas Jungtinės Karalystės **BACS** mokėjimo formatas). [![Pavyzdys, tokia forma, kad duomenų bazės modelis](./media/pic-format-1024x690.png)](./media/pic-format.png) turi būti susipažinę su informacija apie šį scenarijų, žaisti su **ER dizainas domeno konkretaus formato** užduoties vadovas (dalis su **7.5.4.3 Acquire/plėtoti IT paslaugų/sprendimų komponentai (10677)** verslo procesų).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti OPENXML darbalapio formatu, kūrimas

ER formato kūrimo įrankį galima naudoti, norint kurti konkretų elektroninį dokumentą OPENXML darbalapio formatu. Iliustracijoje parodyta šio tipo formatas (format konfigūracijos generuoti OPENXML darbalapį su išsamia informacija apie pasirinktas mokėjimo žurnalą) pavyzdys:[![Pic-ER-formatą-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) susipažinti su informacija apie šį scenarijų, žaisti su **ER kurti ataskaitas OPENXML formatu konfigūraciją** užduoties vadovas (dalis su **7.5.4.3 Acquire/plėtoti IT paslaugų/sprendimų komponentai (10677)** verslo procesų). Naudoti nenurodyta toliau Excel failą kaip šabloną projektavimas ER formato užbaigti formos šablono importo šio darbo vadovo žingsnis: [mokėjimo ataskaitos šabloną (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Sukurto formato komponento saugojimas formato konfigūracijoje

ER gali saugoti suprojektuoti formatą kartu su sukonfigūruotas duomenų rodymo formatas sąrankos Dabartinis Dynamics "365" operacijų atveju. Ankstesnėje iliustracijoje pateiktas šio tipo formato konfigūracijos pavyzdys (**BACS (Jungtinė Karalystė)** – antrinis **mokėjimo modelio** konfigūracijos elementas). Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Konfigūravimas Dynamics 365 veiklai pradėti naudoti susikurtą formatą viduje

Dinamika 365 operacijoms gali būti sukonfigūruota pradėti naudoti susikurtą formatą elektroninėms ataskaitoms generuoti. Nuoroda į sukurto formato konfigūraciją turi būti apibrėžta naudojant konkretaus domeno parametrus. Pvz., pradėti naudoti ER formatas konfigūracijos elektroninių tiekėjo mokėjimams atlikti BACS formatu, formatu konfigūraciją turėtų būti nuorodos į konkrečius mokėjimo būdus be mokėjimo, kaip parodyta paveikslėliuose: 

[![BACS (Didžioji Britanija) format konfigūracijos](media/ger-bacs-uk-format-configuration.png) 

[![Nuorodų BACS (Jungtinė Karalystė) formatą, mokėjimo būdą](media/ger-bacs-uk-format-method.png) 

Paleiskite užduočių vedlį **ER formato naudojimas elektroniniams mokėjimų dokumentams generuoti** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="handling-er-components"></a>ER komponentų tvarkymas
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponento publikavimas LCS, pateikiant jį naudoti išorėje (lokalizavimas)

Sukurto komponento (modelio arba formato) savininkas gali naudoti ER baigtai komponento versijai publikuoti LCS. Tam būtina dabartinio ER konfigūracijos teikėjo **LCS projekto **tipo saugykla. Kai baigtos komponento versijos būsena pakeičiama iš **BAIGTA** į **BENDRAI NAUDOJAMA**, ta versija publikuojama LCS. Publikavus komponentą LCS, to komponento savininkas tampa paslaugos teikėju, palaikančiu šį komponentą. Pavyzdžiui, jei formato komponentas yra skirtas pagal įstatymus būtinam elektroniniam dokumentui generuoti (pavyzdžiui, pagal lokalizavimo scenarijų), manoma, kad formatas turi atitikti teisės aktų pakeitimus ir kad tiekėjas turi išduoti naujas komponento versijas, kai to reikia naujiems įstatymų reikalavimams taikyti. Paleiskite užduočių vedlį **ER konfigūracijos nusiuntimas į „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponento importavimas iš LCS naudoti viduje

ER leidžia importuoti ER komponentai iš LKD dabartinė dinamika 365 operacijų atveju. Būtina **LCS projekto **tipo saugykla. Kai ER komponentas yra importuoti iš LKD dabartinė dinamika 365 operacijų atveju, egzemplioriaus savininkas tampa paslauga, kuri teikia savininkas (autorius) importuotų komponento vartotojas. Pavyzdžiui, jei formatas komponentas yra siekiama sukurti konkretų elektroninį dokumentą iš Dynamics 365 operacijoms šaliai/regionui būdingų formatu (lokalizacijos scenarijus), daroma prielaida, kad paslaugos vartotojui bus suteikta galimybė gauti visus atnaujinimus, atliktus ta forma, kad ji atitiktų teisės aktų reikalavimus. Paleiskite užduočių vedlį **ER konfigūracijos importavimas iš „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formato kūrimas pasirinkus kitą formatą kaip pagrindą (tinkinimas)

ER palaiko galimybę kurti (išvesti) naują komponentą iš dabartinės komponento (pagrindo), importuoto iš LCS, versijos. Pavyzdžiui, vartotojas nori išvesti naują formatą, siekdamas patenkinti kai kuriuos specialius elektroninio dokumento reikalavimus (pvz., reikalavimą naudoti papildomą lauką arba išsamų aprašą), kad būtų palaikomas tinkinimo scenarijus. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formato versijos naujinimas pasirenkant naują pagrindinio formato versiją (pagrindo keitimas)

ER suteikia galimybę automatiškai priimti naujausios pagrindinio komponento versijos pakeitimus dabartinėje išvestinio komponento juodraščio versijoje. Šis procesas vadinamas *pritaikymu kitoje vietoje*. Pavyzdžiui, naują reguliavimo pakeitimą, įtrauktą į naujausią komponento, importuoto iš LCS, versiją, galima automatiškai sulieti su pritaikyta šio elektroninio dokumento formato versija. Bet kokie pakeitimai, kurių negalima sulieti automatiškai, yra laikomi konfliktais. Šiuos konfliktus galima išspręsti neautomatiniu būdu naudojant atitinkamo komponento kūrimo įrankį. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>ER sudėčių, pristatyti Dynamics 365 operacijų tirpalo sąrašą
| Konkretaus domeno duomenų modelio konfigūracijos: pavadinimas | Domenas                | Nuo duomenų modelio priklausančio formato konfigūracijos: pavadinimas | Prekės/Paslaugos pavadinimas                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Audito failo modelis                                 | Finansinis auditas       |                                                   |                                                                    |
|                                                  |                       | Audito failas (NL)                                   | Nyderlandų audito failas                                  |
| BAS modelis                                        | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | Australijos BAS formatas                                           |
| Statybos pramonės schemos modelis               | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | CIS grąžinimas kas mėnesį (UK)                           | CIS grąžinimo kas mėnesį formatas, skirtas Jungtinei Karalystei                   |
| Priminimo laiško modelis                          | Elektroninių SF išrašymas  |                                                   |                                                                    |
|                                                  |                       | OIOUBL priminimo laiškas (DK)                     | OIOUBL priminimo laiško formatas, skirtas Danijai                        |
| Elektroninės DK apskaitos modelis (MX)          | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | Pagalbinė DK XML formatu (MX)                         | Pagalbinės DK operacijos pagal sąskaitą ataskaitos formatas, skirtas Meksikai |
|                                                  |                       | Sąskaitų planas XML formatu (MX)                         | Sąskaitų plano ataskaitos formatas, skirtas Meksikai                          |
|                                                  |                       | Žurnalai XML formatu (MX)                                 | Žurnalo operacijų ataskaitos formatas, skirtas Meksikai                      |
|                                                  |                       | Bandomasis balansas XML formatu (MX)                            | Bandomojo balanso ataskaitos formatas, skirtas Meksikai                             |
| „Elster“ modelis                                     | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | „Elster“ formatas, skirtas Vokietijai                                          |
| ES pardavimo sąrašo modelis                              | Prekybos ataskaitos       |                                                   |                                                                    |
|                                                  |                       | ES pardavimo sąrašas (DE)                                | ES pardavimo sąrašas TXT formatu, skirtas Vokietijai                               |
|                                                  |                       | ES pardavimo sąrašas (DK)                                | ES pardavimo sąrašas TXT formatu, skirtas Danijai                               |
|                                                  |                       | ES pardavimo sąrašas (FR)                                | ES pardavimo sąrašas XML formatu, skirtas Prancūzijai                                |
|                                                  |                       | ES pardavimo sąrašas (NL)                                | ES pardavimo sąrašas XML formatu, skirtas Nyderlandams                           |
|                                                  |                       | ES pardavimo sąrašas (UK)                            | ES pardavimo sąrašas TXT formatu, skirtas Jungtinei Karalystei                    |
|                                                  |                       | ES pardavimo sąrašas XML formatu (UK)                            | ES pardavimo sąrašas XML formatu, skirtas Jungtinei Karalystei                    |
|                                                  |                       | ES pardavimo sąrašo pagal stulpelius ataskaita                   | ES pardavimo sąrašo pagal stulpelius ataskaita                                    |
|                                                  |                       | ES pardavimo sąrašo pagal eilutes ataskaita                      | ES pardavimo sąrašo pagal eilutes ataskaita                                       |
| FEC apskaitos modelis (FR)                        | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | FEC apskaitos duomenys XML formatu (FR)                      | Prancūzijos FEC apskaitos duomenys, eksportuoti XML formatu                   |
| Vokietijos audito failas                                | Finansinis auditas       |                                                   |                                                                    |
|                                                  |                       | Vokietijos audito failo išvestis                          | Audito failo išvestis, skirta Vokietijai ir Austrijai                          |
| Intrastat modelis                                  | Prekybos ataskaitos       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat formatas, skirtas Vokietijai                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat formatas, skirtas Danijai                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM formatas, skirtas Prancūzijai                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC formatas, skirtas Prancūzijai                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat formatas, skirtas Nyderlandams                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastat formatas, skirtas Jungtinei Karalystei                            |
|                                                  |                       | Intrastat ataskaita                                  | Intrastat „Excel“ kontrolės ataskaita                                     |
| Kliento SF modelis                           | Elektroninių SF išrašymas  |                                                   |                                                                    |
|                                                  |                       | OIOUBL projekto kredito pažyma (DK)                   | OIOUBL projekto kredito pažymos formatas, skirtas Danijai                      |
|                                                  |                       | OIOUBL projekto SF (DK)                       | OIOUBL projekto SF formatas, skirtas Danijai                          |
|                                                  |                       | OIOUBL pardavimo kredito pažyma (DK)                     | OIOUBL pardavimo kredito pažymos formatas, skirtas Danijai                        |
|                                                  |                       | OIOUBL pardavimo SF (DK)                         | OIOUBL pardavimo SF formatas, skirtas Danijai                            |
| OB deklaracijos modelis                             | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | OB deklaracija (NL)                               | OB deklaracijos formatas, skirtas Nyderlandams                          |
| Mokėjimo modelis                                    | Mokėjimai              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | „Betalingsservice“ mokėjimo formatas, skitas Danijai                        |
|                                                  |                       | Įsakomojo vekselio pavedimas (FR)                  | Įsakomojo vekselio pavedimo formatas, skirtas Prancūzijai                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91 tiekėjo mokėjimo formatas, skirtas Nyderlandams                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB tiesioginio debeto mokėjimo formatas, skirtas Prancūzijai                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB vietinio tiekėjo mokėjimo formatas, skirtas Prancūzijai                    |
|                                                  |                       | „Nordea“ tiekėjas (DK)                                | „Nordea corporate netbank“ tiekėjo mokėjimo formatas, skirtas Danijai         |
|                                                  |                       | ANZ tiesioginio kredito paslauga (AU)                    | ANZ tiesioginio kredito paslaugos formatas, skirtas Australijai                 |
|                                                  |                       | CBA tiesioginio kredito paslauga (AU)                    | CBA tiesioginio kredito paslaugos formatas, skirtas Australijai                 |
|                                                  |                       | NAB tiesioginio kredito paslauga (AU)                    | NAB tiesioginio kredito paslaugos formatas, skirtas Australijai                 |
|                                                  |                       | STG tiesioginio kredito paslauga (AU)                    | STG tiesioginio kredito paslaugos formatas, skirtas Australijai                 |
|                                                  |                       | WBC tiesioginio įrašymo sistema (AU)                      | WBC tiesioginio įrašymo sistemos formatas, skirtas Australijai                   |
|                                                  |                       | DirectLink (NZ)                                   | „DirectLink“ formatas, skirtas Naujajai Zelandijai                              |
|                                                  |                       | JBA mokėjimo failas (JP)                             | JBA mokėjimo formatas, skirtas Japonijai                                       |
|                                                  |                       | ISO20022 kredito pervedimas                          | SEPA kredito pervedimo formatas, skirtas Europai                             |
|                                                  |                       | ISO20022 kredito pervedimas (FR)                     | SEPA kredito pervedimo formatas, skirtas Prancūzijai                             |
|                                                  |                       | ISO20022 kredito pervedimas (DE)                     | SEPA kredito pervedimo formatas, skirtas Vokietijai                            |
|                                                  |                       | ISO20022 kredito pervedimas (NL)                     | SEPA kredito pervedimo formatas, skirtas Nyderlandams                    |
|                                                  |                       | ISO20022 tiesioginis debetas                             | SEPA tiesioginio debeto formatas, skirtas Europai                                |
|                                                  |                       | ISO20022 tiesioginis debetas (FR)                        | SEPA tiesioginio debeto formatas, skirtas Prancūzijai                                |
|                                                  |                       | ISO20022 tiesioginis debetas (DE)                        | SEPA tiesioginio debeto formatas, skirtas Vokietijai                               |
|                                                  |                       | ISO20022 tiesioginis debetas (NL)                        | SEPA tiesioginio debeto formatas, skirtas Nyderlandams                       |
|                                                  |                       | BACS (UK)                                         | BACS tiekėjo mokėjimo formatas, skirtas Jungtinei Karalystei                  |
| Atvirkštinis apmokestinimas                                   | Mokesčių ataskaitos         |                                                   |                                                                    |
|                                                  |                       | Atvirkštinio apmokestinimo sąrašo atšaukimas                         | Atvirkštinio apmokestinimo pardavimo sąrašo formatas                                   |
| Olandijos XBRL integravimo modelis                     | XBRL ataskaitos        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | „Semansys XBRL“ eksportavimo formatas, skirtas Nyderlandams                    |
| GAF modelis (MY)                                   | Finansinis auditas       |                                                   |                                                                    |
|                                                  |                       | GAF failas (MY)                                     | GAF formatas, skirtas Malaizijai                                         |
| Tiekėjų skirstymo pagal terminus ataskaita (CN)                         | Tiekėjų duomenų analizė |                                                   |                                                                    |
|                                                  |                       | Tiekėjų skirstymo pagal terminus ataskaitos formatas (CN)                   | Tiekėjų skirstymo pagal terminus ataskaitos formatas, skirtas Kinijai                               |
| Tiekėjo SF deklaracijos modelis                 | Tiekėjų duomenų analizė |                                                   |                                                                    |
|                                                  |                       | Tiekėjo SF deklaracija (IS)                   | Tiekėjo SF deklaracijos formatas, skirtas Islandijai                      |
|                                                  |                       | Tiekėjo SF deklaracijos ataskaita (IS)            | Tiekėjo SF deklaracijos ataskaita, skirta Islandijai                      |



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Lokalizacijos reikalavimai – elektroninių ataskaitų konfigūracijos kūrimas](electronic-reporting-configuration.md)

[Valdykite Elektroninių ataskaitų konfigūracijos ciklą](general-electronic-reporting-manage-configuration-lifecycle.md)


