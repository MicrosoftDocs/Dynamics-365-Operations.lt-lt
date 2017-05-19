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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: abe9212372fb7429d68c1fb6b32ec1d15c20a6d7
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-reporting-overview"></a>Elektroninių ataskaitų apžvalga

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis.

Elektroninės ataskaitos (ER) – tai įrankis, kurį naudodami galite konfigūruoti elektroninių dokumentų formatus pagal įvairių šalių ir regionų teisinius reikalavimus. ER suteikia galimybę valdyti šiuos formatus per jų naudojimo ciklą. Pavyzdžiui, galite pritaikyti naujus teisinius reikalavimus ir generuoti verslo dokumentus reikiamu formatu, skirtu keistis informacija su valdžios institucijomis, bankais ir kitomis šalimis elektroniniu būdu. ER mechanizmas skirtas verslo vartotojui, o ne kūrėjui. Kadangi galite konfigūruoti formatus, o ne kodus, elektroninių dokumentų formatų kūrimo ir pritaikymo procesas greitesnis ir lengvesnis. ER šiuo metu palaiko TEXT, XML ir OPENXML darbalapio formatus. Tačiau naudojant plėtinio sąsają palaikoma daugiau formatų.

## <a name="capabilities"></a>Galimybės
ER mechanizmas turi toliau nurodytas galimybes.

-   Jis yra vienas bendras įrankis, skirtas elektroninėms ataskaitoms kurti skirtinguose domenuose, ir pakeičia daugiau nei 20 skirtingų mechanizmų, kuriančių tam tikras „Microsoft Dynamics 365 for Operations“ elektronines ataskaitas.
-   Jis izoliuoja ataskaitos formatą nuo dabartinės įdiegtos „Dynamics 365 for Operations“ versijos. (Kitaip tariant, , formatą galima taikyti skirtingoms „Dynamics 365 for Operations“ versijoms.)
-   Jis palaiko pasirinktinio formato kūrimą pagal jo pradinę versiją. Jis apima galimybes automatiškai naujinti tinkintą formatą, kai pradinis formatas pasikeičia dėl įvestų lokalizavimo / tinkinimo reikalavimų.
-   Jis tampa pagrindiniu standartiniu „Microsoft“ ir „Microsoft“ partnerių elektroninių ataskaitų lokalizavimo reikalavimus palaikančiu įrankiu.
-   Jis palaiko galimybę paskirstyti formatus partneriams ir klientams naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="concepts"></a>Koncepcijos
### <a name="components"></a>Komponentai

ER palaiko dviejų tipų komponentus: **Duomenų modelis** ir **Formatas**.

#### <a name="data-model-components"></a>Duomenų modelio komponentai

Duomenų modelio komponentas abstrakčiai vaizduoja duomenų struktūrą ir yra naudojamas tam tikrai verslo domeno sričiai aprašyti pakankamai išsamiai, kad būtų tenkinami tos srities ataskaitų reikalavimai. Duomenų modelio komponentą sudaro toliau nurodytos dalys.

-   Duomenų modelis kaip domenui būdingų verslo objektų rinkinys ir hierarchiškai susistemintas jų ryšių aprašas
-   Modelio susiejimas, kuris susieja pasirinktus „Microsoft Dynamics 365 for Operations“ duomenų šaltinius su atskirais duomenų modelio elementais, vykdymo metu nurodančiais duomenų srautą ir taisykles, pagal kurias verslo duomenys automatiškai įvedami į duomenų modelio komponentą.

Duomenų modelio verslo objektas pateikiamas kaip konteineris (įrašas). Verslo subjekto ypatybės pateikiamos kaip duomenų elementai (laukai). Kiekvienas duomenų elementas turi unikalų pavadinimą, žymę, aprašą ir reikšmę. Kiekvieno duomenų elemento reikšmė gali būti sukurta taip, kad būtų atpažinta kaip eilutė, sveikasis skaičius, realusis skaičius, data, išvardijimo tipas, bulio logika ir t. t. Be to, tai gali būti kitas įrašas arba įrašų sąrašas. Viename duomenų modelio komponente gali būti kelios domenui būdingų verslo objektų hierarchijos, taip pat modelio susiejimai, kad vykdymo metu būtų palaikomas konkretus ataskaitai būdingas duomenų srautas. Hierarchijos yra atskiriamos pagal vieną įrašą, kuris buvo pasirinktas kaip šakninis modelio susiejimo įrašas. Pavyzdžiui, mokėjimo domeno srities duomenų modelis gali palaikyti tolesnius susiejimus.

-   Įmonė -&gt; Tiekėjas -&gt; AP domeno mokėjimo operacijos
-   Klientas -&gt; Įmonė -&gt; AR domeno mokėjimo operacijos

Atkreipkite dėmesį, kad verslo subjektai (pvz., Įmonė ir Mokėjimo operacijos) yra sukurtos vieną kartą. Tada kiti susiejimai pakartotinai juos naudoja. Toliau pateikiamos modelio susiejimo galimybės.

-   Jis gali naudoti skirtingus „Dynamics 365 for Operations“ duomenų tipus kaip duomenų modelio duomenų šaltinius. Pavyzdžiui, jis gali naudoti lenteles, duomenų objektus, metodus ar išvardijimus.
-   Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo metu.
-   Jis palaiko „Dynamics 365 for Operations“ duomenų transformavimą į reikiamas grupes, duomenų filtravimą, rūšiavimą ir sumavimą, taip pat duomenų pridėjimą naudojant loginius apskaičiuotus laukus, sukurtus su formulėmis, panašiomis į „Microsoft Excel“ formules (daugiau informacijos rasite dalyje [Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)).

[![Formulių, panašių į „Excel“ formules, rengyklė](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Duomenų modelio komponentas skirtas kiekvienam verslo domenui, kuris turi būti naudojamas kaip bendrasis ataskaitų duomenų šaltinis, atskiriantis ataskaitas nuo fizinių įdiegtų „Dynamics 365 for Operations“ duomenų šaltinių; jis pateikia domenui būdingas verslo koncepcijas ir funkcijas tokia forma, kuri padaro ataskaitų formato pradinį kūrimą ir tolesnę priežiūrą efektyvesnius.

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
-   Versiją **BAIGTA** galima konvertuoti į versiją **BENDRAI NAUDOJAMA**. Ši versija publikuojama LCS ir ją galima naudoti visuotiniuose ataskaitų teikimo procesuose.
-   Versiją **BENDRAI NAUDOJAMA** galima konvertuoti į versiją **NEBENAUDOJAMA**. Tada šią versiją bus galima naikinti.

Kai versijos būsena yra **BAIGTA** arba **BENDRAI NAUDOJAMA**, galima keistis duomenimis dar kitu būdu. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

-   Juos galima išdėstyti eilutėmis XML formatu ir eksportuoti iš „Dynamics 365 for Operations“ kaip failą XML formatu.
-   Juos galima sugrąžinti iš XML failo ir importuoti į „Dynamics 365 for Operations“ kaip naują ER komponento versiją.

#### <a name="component-date-effectivity"></a>Komponento galiojimo data

ER komponento versijos turi galiojimo datą. Galima apibrėžti ER komponento datą**Galioja nuo**, norint nurodyti datą, nuo kurios šis komponentas galioja, ir jį galima naudoti ataskaitų teikimo procesuose. „Dynamics 365 for Operations“ seanso data naudojama apibrėžti, ar komponentas yra tinkamas vykdyti. Jei konkrečią dieną galioja daugiau nei viena versija, ataskaitų teikimo procesuose naudojama naujausia versija.

#### <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato komponentų priklauso nuo ISO valstybės / regiono kodo parametro. Kai šis pasirinktos formato konfigūracijos versijos parametras nenurodytas, formato komponentą galima pasiekti iš bet kurios „Dynamics 365 for Operations“ įmonės vykdymo metu. Kai šiame parametre yra ISO valstybės / regiono kodai, formatas komponentą galima pasiekti tik iš tų „Dynamics 365 for Operations“ įmonių, kurių pagrindinis adresas nurodytas kaip vienas iš formato komponento ISO valstybės / regiono kodų. Skirtingos duomenų formato komponento versijos gali turėti skirtingus ISO valstybės / regiono kodų parametrus.

#### <a name="configuration"></a>Konfigūravimas

ER konfigūracija yra tam tikro ER komponento (**Duomenų modelis** arba **Formatas**) aplankas. Konfigūracija gali apimti skirtingas tam tikro ER komponento versijas. Kiekviena konfigūracija pažymėta kaip priklausanti konkrečiam konfigūracijos teikėjui. Konfigūracijos komponento versiją **JUODRAŠTIS** galima redaguoti, jei konfigūracijos savininkas pasirinktas kaip aktyvus teikėjas „Dynamics 365 for Operations“ ER parametruose. Kiekvienoje modelio konfigūracijoje yra komponentas **Duomenų modelis**. Naują formato konfigūraciją galima išvesti (gauti) iš konkrečios duomenų modelio konfigūracijos. Sukurta formato konfigūracija konfigūracijos medyje bus pateikta kaip antrinė pradinės duomenų modelio konfigūracijos konfigūracija. Sukurtoje formato konfigūracijoje yra komponentas **Formatas**. Pirminės modelio konfigūracijos komponentas **Duomenų modelis** yra automatiškai įterpiamas į antrinės formato konfigūracijos komponentą **Formatas**kaip numatytasis duomenų šaltinis. „Dynamics 365 for Operations“ įmonės bendrai naudoja ER konfigūraciją.

#### <a name="provider"></a>Teikėjas

ER teikėjas yra šalies identifikatorius, naudojamas kiekvienos ER konfigūracijos autoriui (savininkui) nurodyti. ER suteikia galimybę valdyti konfigūracijos teikėjų sąrašą. Formatų konfigūracijos, skirtos elektroniniams dokumentams kaip „Dynamics 365 for Operations“ sprendimo dalis, yra pažymėtos kaip priklausančios konfigūracijos teikėjui **Microsoft**.

#### <a name="repository"></a>Saugykla

ER saugykloje saugomos ER konfigūracijos. Šiuo metu palaikomos šių tipų ER saugyklos: **Operacijų ištekliai** ir **LCS projektas**. **Operacijų išteklių** saugykla suteikia prieigą prie konfigūracijų sąrašo, kuris pristatomas kaip „Dynamics 365 for Operations‟ sprendimo, teikiamo „Microsoft‟ kaip ER konfigūracijų teikėjo, dalis. Šias konfigūracijas galima importuoti į esamą „Dynamics 365 for Operations‟ egzempliorių ir naudoti elektroninių ataskaitų kūrimo tikslais. Taip pat jas galima naudoti tolesniam lokalizavimui / tinkinimui atlikti. **LCS projekto** saugykla suteikia prieigą prie tam tikro LCS projekto (LCS projekto turto bibliotekos), pasirinkto saugyklos registracijos etape, konfigūracijų sąrašo. ER suteikia galimybę nusiųsti bendrai naudojamas konfigūracijas iš dabartinio „Dynamics 365 for Operations“ egzemplioriaus į konkrečią **LCS projekto** saugyklą. Taip pat galite konfigūracijas importuoti iš konkrečios **LCS projekto** saugyklos į dabartinį „Dynamics 365 for Operations“ egzempliorių. Galima registruoti atskirai kiekvieno dabartinio „Dynamics 365 for Operations“ egzemplioriaus konfigūracijos teikėjo būtinas **LCS projekto** saugyklas. Kiekvieną saugyklą galima priskirti konkrečiam konfigūracijos teikėjui.

## <a name="supported-scenarios"></a>Palaikomi scenarijai
### <a name="building-a-data-model"></a>Duomenų modelio kūrimas

ER teikia modelių kūrimo įrankį, kurį galite naudoti konkrečiam verslo domenui skirtam duomenų modeliui kurti. Visus domenui būdingus verslo objektus ir jų ryšius galima pateikti duomenų modelyje kaip hierarchinę struktūrą. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio pavyzdys (mokėjimo domeno duomenų modelis). [![Duomenų modelio pavyzdys](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Paleiskite užduočių vedlį **ER konkretaus domeno duomenų modelio kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="translating-data-model-content"></a>Duomenų modelio turinio vertimas

Duomenų modelio turinį (etiketes ir aprašus) galima išversti į kitas „Dynamics 365 for Operations“ palaikomas kalbas. Duomenų modelio turinį galite norėti išversti dėl toliau nurodytų priežasčių.

-   Norint, kad kita kalba kalbantys formato kūrėjai, kurie naudos duomenų modelį formato komponentų duomenims susieti, kurdami lengviau suprastų turinį
-   Norint turinį padaryti patogesnį naudoti vykdymo metu, teikiant vykdymo parametrų raginimus ir pagalbą bei sukonfigūruotus tikrinimo pranešimus (klaidų, įspėjimų) tuo metu prisijungusio „Dynamics 365 for Operations“ vartotojo pageidaujama kalba

Tolesnėje iliustracijoje pateikiamas pavyzdys, kaip duomenų modelio turinį galima išversti iš anglų k. į japonų k.. [![Duomenų modelio turinys anglų k.](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Duomenų modelio turinys, išverstas į japonų k.](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Duomenų modelio susiejimų konfigūravimas

ER teikia modelio susiejimų kūrimo įrankį, kurį naudodami vartotojai susieti duomenų modelius, kuriuos jie sukūrė konkretiems „Dynamics 365 for Operations“ duomenų šaltiniams. Tolesnėje iliustracijoje pateikiamas tokio tipo duomenų modelio susiejimo pavyzdys (mokėjimo domeno duomenų modelio **SEPA kredito pervedimo** modelio susiejimas). [![Duomenų modelio susiejimo pavyzdys](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Paleiskite užduočių vedlius **ER modelio susiejimo nustatymas ir duomenų šaltinių pasirinkimas** ir **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Sukurto modelio komponento saugojimas kaip modelio konfigūracijos

ER gali saugoti sukurtą duomenų modelį su susietais duomenų susiejimais kaip dabartinio „Dynamics 365 for Operations“ egzemplioriaus modelio konfigūraciją. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio konfigūracijos pavyzdys (mokėjimo duomenų modelio konfigūracija). [![Duomenų modelio konfigūracijos pavyzdys](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Paleiskite užduočių vedlį **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Formato kūrimas pasirenkant duomenų modelį kaip pagrindą

ER palaiko formato kūrimo įrankį, kurį galima naudoti norint kurti pasirinkto verslo domeno konkretaus elektroninio dokumento formatą pasirenkant modelio komponentą kaip pagrindą. Tas pats ER formato kūrimo įrankis teikia galimybę sukurtą formatą susieti su pasirinkto domeno duomenų modelio susiejimu kaip duomenų šaltiniu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys (formato konfigūracija, kad būtų palaikomas Jungtinės Karalystės **BACS** mokėjimo formatas). [![Formato, kuriame duomenų modelis naudojamas kaip pagrindas, pavyzdys](./media/pic-format-1024x690.png)](./media/pic-format.png) Paleiskite užduočių vedlį **ER konkretaus formato modelio kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti OPENXML darbalapio formatu, kūrimas

ER formato kūrimo įrankį galima naudoti, norint kurti konkretų elektroninį dokumentą OPENXML darbalapio formatu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys (formato konfigūracija, skirta generuoti OPENXML darbalapį su pasirinkto mokėjimo žurnalo informacija):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Paleiskite užduočių vedlį **ER konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi. Naudokite toliau nurodytą „Excel“ failą kaip ER formato kūrimo šabloną, kad atliktumėte šio užduočių vedlio formato šablono importavimo veiksmą: [Mokėjimo ataskaitos šablonas (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Sukurto formato komponento saugojimas formato konfigūracijoje

ER gali saugoti sukurtą formatą su sukonfigūruotais duomenų susiejimais kaip dabartinio „Dynamics 365 for Operations“ egzemplioriaus modelio konfigūraciją. Ankstesnėje iliustracijoje pateiktas šio tipo formato konfigūracijos pavyzdys (**BACS (Jungtinė Karalystė)** – antrinis **mokėjimo modelio** konfigūracijos elementas). Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>„Dynamics 365 for Operations“ konfigūravimas, norint pradėti naudoti sukurtą formatą viduje

„Dynamics 365 for Operations“ galima konfigūruoti, kad ji sukurtą formatą pradėtų naudoti elektroninėms ataskaitoms generuoti. Nuoroda į sukurto formato konfigūraciją turi būti apibrėžta naudojant konkretaus domeno parametrus. Pvz., norint pradėti naudoti ER formato konfigūraciją elektroniniams tiekėjo mokėjimams BACS formatu apdoroti, formato konfigūraciją reikia nurodyti konkrečiuose mokėjimo būduose, kaip parodyta tolesnėse iliustracijose. 

[![BACS (JK) formato konfigūracija](media/ger-bacs-uk-format-configuration.png) 

[![BACS (JK) formato nurodymas mokėjimo būde](media/ger-bacs-uk-format-method.png) 

Paleiskite užduočių vedlį **ER formato naudojimas elektroniniams mokėjimų dokumentams generuoti** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="handling-er-components"></a>ER komponentų tvarkymas
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponento publikavimas LCS, pateikiant jį naudoti išorėje (lokalizavimas)

Sukurto komponento (modelio arba formato) savininkas gali naudoti ER baigtai komponento versijai publikuoti LCS. Tam būtina dabartinio ER konfigūracijos teikėjo **LCS projekto**tipo saugykla. Kai baigtos komponento versijos būsena pakeičiama iš **BAIGTA** į **BENDRAI NAUDOJAMA**, ta versija publikuojama LCS. Publikavus komponentą LCS, to komponento savininkas tampa paslaugos teikėju, palaikančiu šį komponentą. Pavyzdžiui, jei formato komponentas yra skirtas pagal įstatymus būtinam elektroniniam dokumentui generuoti (pavyzdžiui, pagal lokalizavimo scenarijų), manoma, kad formatas turi atitikti teisės aktų pakeitimus ir kad tiekėjas turi išduoti naujas komponento versijas, kai to reikia naujiems įstatymų reikalavimams taikyti. Paleiskite užduočių vedlį **ER konfigūracijos nusiuntimas į „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponento importavimas iš LCS naudoti viduje

ER suteikia galimybę importuoti ER komponentus iš LCS į esamą „Dynamics 365 for Operations“ egzempliorių. Būtina **LCS projekto**tipo saugykla. Importavus ER komponentą iš LCS į esamą „Dynamics 365 for Operations“ egzempliorių, egzemplioriaus savininkas tampa paslaugos, kurią teikia importuoto komponento savininkas (autorius), vartotoju. Pavyzdžiui, jei šis formato komponentas skirtas konkrečiam elektroniniam dokumentui generuoti iš „Dynamics 365 for Operations“ tam tikros valstybės / regiono būdingu formatu (lokalizavimo scenarijus), manoma, kad paslaugos vartotojas galės gauti visus šio formato naujinimus, kad formatas visada atitiktų įstatymų reikalavimus. Paleiskite užduočių vedlį **ER konfigūracijos importavimas iš „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formato kūrimas pasirinkus kitą formatą kaip pagrindą (tinkinimas)

ER palaiko galimybę kurti (išvesti) naują komponentą iš dabartinės komponento (pagrindo), importuoto iš LCS, versijos. Pavyzdžiui, vartotojas nori išvesti naują formatą, siekdamas patenkinti kai kuriuos specialius elektroninio dokumento reikalavimus (pvz., reikalavimą naudoti papildomą lauką arba išsamų aprašą), kad būtų palaikomas tinkinimo scenarijus. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formato versijos naujinimas pasirenkant naują pagrindinio formato versiją (pagrindo keitimas)

ER suteikia galimybę automatiškai priimti naujausios pagrindinio komponento versijos pakeitimus dabartinėje išvestinio komponento juodraščio versijoje. Šis procesas vadinamas *pritaikymu kitoje vietoje*. Pavyzdžiui, naują reguliavimo pakeitimą, įtrauktą į naujausią komponento, importuoto iš LCS, versiją, galima automatiškai sulieti su pritaikyta šio elektroninio dokumento formato versija. Bet kokie pakeitimai, kurių negalima sulieti automatiškai, yra laikomi konfliktais. Šiuos konfliktus galima išspręsti neautomatiniu būdu naudojant atitinkamo komponento kūrimo įrankį. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>ER konfigūracijų, kurios pateikiamos „Dynamics 365 for Operations“ sprendime, sąrašas
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




