---
title: "Elektroninė ataskaita (ER)"
description: "Šioje temoje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: a271887c4d2cfe4d0ee6518482dc4ebe407ebe56
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="electronic-reporting-er"></a>Elektroninė ataskaita (ER)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama elektroninių ataskaitų (ER) įrankio apžvalga. Jame yra informacijos apie pagrindines koncepcijas, ER palaikomus scenarijus ir išvardyti formatai, kurie sukurti ir išleisti kaip sprendimo dalis.

ER yra įrankis, kurį naudodami galite konfigūruoti tiek gaunamų, tiek siunčiamų elektroninių dokumentų formatus pagal įvairių šalių / regionų teisinius reikalavimus. ER suteikia galimybę valdyti šiuos formatus per jų naudojimo ciklą. Pavyzdžiui, galite pritaikyti naujus teisinius reikalavimus ir generuoti verslo dokumentus reikiamu formatu, skirtu keistis informacija su valdžios institucijomis, bankais ir kitomis šalimis elektroniniu būdu.

ER mechanizmas skirtas verslo vartotojui, o ne kūrėjui. Kadangi galite konfigūruoti formatus, o ne kodą, elektroninių dokumentų formatų kūrimo ir pritaikymo procesas greitesnis ir lengvesnis.

ER šiuo metu palaiko TEXT, XML, „Microsoft Word“ dokumento ir OPENXML darbalapio formatus. Tačiau naudojant plėtinio sąsają palaikomi papildomi formatai.

## <a name="capabilities"></a>Galimybės
ER mechanizmas turi toliau nurodytas galimybes.

- Tai vienas bendrai naudojamas įrankis, skirtas elektroninėms ataskaitoms skirtinguose domenuose kurti, kuris pakeičia daugiau nei 20 skirtingų mechanizmų, kuriančių tam tikras „Microsoft Dynamics 365 for Finance and Operations“ elektronines ataskaitas.
- Jis izoliuoja ataskaitos formatą nuo dabartinės įdiegtos „Finance and Operations“ versijos. Kitaip tariant, formatą galima taikyti skirtingoms „Finance and Operations“ versijoms.
- Jis palaiko pasirinktinio formato kūrimą pagal jo pradinę versiją. Jis taip pat apima galimybes automatiškai naujinti tinkintą formatą, kai pradinis formatas pakeičiamas dėl įvestų lokalizavimo / tinkinimo reikalavimų.
- Jis tampa pagrindiniu standartiniu „Microsoft“ ir „Microsoft“ partnerių elektroninių ataskaitų lokalizavimo reikalavimus palaikančiu įrankiu.
- Jis palaiko galimybę paskirstyti formatus partneriams ir klientams naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="key-concepts"></a>Pagrindinės koncepcijos
### <a name="components"></a>Komponentai

ER palaiko dviejų tipų komponentus: **Duomenų modelis** ir **Formatas**.

#### <a name="data-model-components"></a>Duomenų modelio komponentai

Duomenų modelio komponentas abstrakčiai vaizduoja duomenų struktūrą. Jis yra naudojamas tam tikrai verslo domeno sričiai aprašyti pakankamai išsamiai, kad būtų tenkinami tos srities ataskaitų reikalavimai. Duomenų modelio komponentą sudaro toliau nurodytos dalys.

- Duomenų modelis kaip domenui būdingų verslo objektų rinkinys ir hierarchiškai susistemintas jų ryšių aprašas.
- Modelio susiejimas, kuris susieja pasirinktus „Finance and Operations“ duomenų šaltinius su atskirais duomenų modelio elementais, vykdymo metu nurodančiais duomenų srautą ir taisykles, pagal kurias verslo duomenys automatiškai įvedami į duomenų modelio komponentą.

Duomenų modelio verslo objektas pateikiamas kaip konteineris (įrašas). Verslo subjekto ypatybės pateikiamos kaip duomenų elementai (laukai). Kiekvienas duomenų elementas turi unikalų pavadinimą, žymę, aprašą ir reikšmę. Kiekvieno duomenų elemento reikšmė gali būti sukurta taip, kad būtų atpažinta kaip eilutė, sveikasis skaičius, realusis skaičius, data, išvardijimas, Bulio logika ir t. t. Be to, tai gali būti kitas įrašas arba įrašų sąrašas.

Viename duomenų modelio komponente gali būti kelios domenui būdingų verslo objektų hierarchijos. Jame taip pat gali būti modelio susiejimai, kurie vykdymo metu palaiko konkretų ataskaitai būdingą duomenų srautą. Hierarchijos yra atskiriamos pagal vieną įrašą, kuris buvo pasirinktas kaip šakninis modelio susiejimo įrašas. Pavyzdžiui, mokėjimo domeno srities duomenų modelis gali palaikyti tolesnius susiejimus.

- Įmonė > Tiekėjas > AP domeno mokėjimo operacijos
- Klientas > Įmonė > AR domeno mokėjimo operacijos

Atkreipkite dėmesį, kad verslo objektai, pvz., įmonė ir mokėjimo operacijos, yra kuriami vieną kartą. Tada kiti susiejimai pakartotinai juos naudoja.

Modelio susiejimas, kuris palaiko siunčiamus elektroninius dokumentus, turi šias galimybes:

- Jis gali naudoti skirtingus „Finance and Operations“ duomenų tipus kaip duomenų modelio duomenų šaltinius. Pavyzdžiui, jis gali naudoti lenteles, duomenų objektus, metodus ar išvardijimus.
- Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo metu.
- Jis palaiko „Finance and Operations“ duomenų transformavimą į reikiamas grupes. Su juo galite filtruoti, rūšiuoti ir sumuoti duomenis, taip pat pridėti loginius apskaičiuotus laukus, sukurtus su formulėmis, panašiomis į „Microsoft Excel“ formules, kaip pavaizduota tolesnėje iliustracijoje. Daugiau informacijos rasite [Elektroninių ataskaitų formulių kūrimo įrankyje](general-electronic-reporting-formula-designer.md)).

[![Formulių kūrimo įrankis](./media/ER-overview-01.png)](./media/ER-overview-01.png) 

Modelio susiejimas, kuris palaiko gaunamus elektroninius dokumentus, turi šias galimybes:

- Jis gali naudoti skirtingus „Finance and Operations“ naujinamus duomenų elementus kaip tikslus. Šie duomenų elementai apima lenteles, duomenų objektus ir rodinius. Duomenis galima atnaujinti naudojant duomenis iš gaunamų elektroninių dokumentų. Vieno modelio susiejime galima naudoti kelis tikslus.
- Jis palaiko vartotojo įvesties parametrus, kuriuos galima apibrėžti kaip duomenų modelio šaltinius, kai kai kuriuos duomenis reikia nurodyti vykdymo metu.

Duomenų modelio komponentas skirtas kiekvienam verslo domenui, kuris turi būti naudojamas kaip suvienodintas ataskaitų duomenų šaltinis, atskiriantis ataskaitų teikimą nuo fizinio duomenų šaltinių diegimo. Tai konkrečios srities verslo koncepcijos ir funkcijos, pateiktos tokia forma, dėl kurios ataskaitų formato pirminis kūrimas ir tolesnė priežiūra tampa efektyvesnė.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Siunčiamų elektroninių dokumentų formato komponentai

Formato komponentas yra ataskaitų kūrimo planas, kuris bus generuojamas vykdymo metu. Schemą sudaro toliau nurodyti elementai.

- Formatas, kuris apibrėžia vykdymo metu sugeneruoto siunčiamo elektroninio dokumento struktūrą ir turinį.
- Duomenų šaltiniai kaip vartotojo įvesties parametrų rinkinys ir domenui būdingų duomenų modelis, kuris naudoja pasirinktą modelio susiejimą.
- Formato susiejimas kaip formato duomenų šaltinių susiejimų su atskirais formato elementais, vykdymo metu nurodančiais duomenų srautą ir formato išvesties generavimo taisykles, susiejimų rinkinys.
- Formato tikrinimas kaip konfigūruojamų taisyklių, kurios vykdymo metu valdo ataskaitos generavimą pagal vykdymo kontekstą, rinkinys. Pavyzdžiui, gali būti taisyklė, kuri sustabdo tiekėjo mokėjimų išeigos generavimą ir pritaiko išimtį, jei trūksta konkrečių pasirinkto tiekėjo atributų, pvz., banko sąskaitos numerio.

Formato komponentas palaiko tolesnes funkcijas.

- Ataskaitos išeigos kaip atskirų skirtingų formatų, pvz., teksto, XML, „Microsoft Word“ dokumento ar darbalapio, failų kūrimas.
- Kelių failų kūrimas atskirai ir tų failus glaudinimas į „zip“ failus.

Formato komponentas leidžia pridėti toliau nurodytus tam tikrus failus, kurie gali būti naudojami ataskaitų išeigoje.

- „Excel“ darbaknyges, kuriose yra darbalapis, galima naudoti kaip OPENXML darbalapio formato išeigos šabloną
- „Word“ failus, kuriuose yra dokumentas, kurį galima naudoti kaip „Microsoft Word“ dokumento formato išeigos šabloną
- Kiti failai, kurie gali būti įtraukti į formato išeigą kaip iš anksto apibrėžti failai

Šis pavyzdys rodo, kaip juda šių formatų duomenų srautai.

[![Siunčiamų formato komponentų duomenų srautas](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Norėdami paleisti vieną ER formato konfigūraciją ir generuoti siunčiamą elektroninį dokumentą, turite nustatyti formato konfigūracijos susiejimą.

#### <a name="format-components-for-incoming-electronic-documents"></a>Gaunamų elektroninių dokumentų formato komponentai
Formato komponentas yra gaunamo dokumento planas, kuris importuojamas vykdymo metu. Schemą sudaro toliau nurodyti elementai.

- Formatas, kuris apibrėžia vykdymo metu importuoto gaunamo elektroninio dokumento, kuriame yra duomenų, struktūrą ir turinį. Formato komponentas naudojamas išanalizuoti įvairiais formatais gaunamą dokumentą, pvz., teksto ir XML.
- Formato susiejimas, kuris sujungia atskirus formato elementus į konkrečios srities duomenų modelio elementus. Vykdymo metu duomenų modelio elementai nurodo duomenų srautą ir duomenų importavimo iš gaunamo dokumento taisykles, o tada išsaugo duomenų modelio duomenis.
- Formato tikrinimas kaip konfigūruojamų taisyklių, kurios vykdymo metu valdo duomenų importavimą pagal vykdymo kontekstą, rinkinys. Pavyzdžiui, gali būti taisyklė, kuri sustabdo banko išrašo, kuriame pateikiami tiekėjo mokėjimai, duomenų importavimą ir pritaiko išimtį, jei trūksta konkretaus tiekėjo atributų, pvz., tiekėjo identifikavimo kodo.

Šis pavyzdys rodo, kaip juda šių formatų duomenų srautai.

[![Gaunamų formato komponentų duomenų srautas](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Norėdami paleisti vieną ER formato konfigūraciją ir importuoti duomenis iš gaunamo elektroninio dokumento, turite nustatyti norimą formato konfigūracijos susiejimą, taip pat modelio susiejimo integravimo tašką. Galite naudoti tą patį modelio susiejimą ir paskirties vietas kartu su skirtingo tipo gaunamų dokumentų skirtingais formatais.

#### <a name="component-versioning"></a>Komponento versijos kūrimas

Palaikomas ER komponento versijos kūrimas. Toliau pateikta ER komponentų pakeitimų valdymo darbo eiga.

1. Pradinė sukurta versija pažymima kaip **Juodraštis**. Šią versiją galima redaguoti ir ją galima tikrinti.
2. Versiją **Juodraštis** galima konvertuoti į versiją **Baigta**. Šią versija galima naudoti vietiniuose ataskaitų teikimo procesuose.
3. Versiją **Baigta** galima konvertuoti į versiją **Bendrai naudojama**. Ši versija publikuojama LCS ir ją galima naudoti visuotiniuose ataskaitų teikimo procesuose.
4. Versiją **Bendrai naudojama** galima konvertuoti į versiją **Nebenaudojama**. Tada šią versiją bus galima naikinti.

Kai versijos būsena yra **Baigta** arba **Bendrai naudojama**, galima keistis duomenimis dar kitu būdu. Jei komponento būsena yra viena iš šių, galima atlikti toliau nurodytus veiksmus.

- Komponentą galima išdėstyti eilutėmis XML formatu ir eksportuoti kaip failą XML formatu.
- Komponentą galima sugrąžinti iš XML failo ir importuoti į „Finance and Operations“ kaip naują ER komponento versiją.

#### <a name="component-date-effectivity"></a>Komponento galiojimo data

ER komponento versijos turi galiojimo datą. Galite nustatyti ER komponento datą **Galioja nuo**, kad nurodytumėte datą, nuo kurios šis komponentas galioja ir jį galima naudoti ataskaitų teikimo procesuose. „Finance and Operations“ seanso data naudojama apibrėžti, ar komponentas yra tinkamas vykdyti. Jei konkrečią dieną galioja daugiau nei viena versija, ataskaitų teikimo procesuose naudojama naujausia versija.

#### <a name="component-access"></a>Prieiga prie komponento

Prieiga prie ER formato komponentų priklauso nuo ISO valstybės / regiono kodo parametro. Kai šis pasirinktos formato konfigūracijos versijos parametras nenurodytas, formato komponentą galima pasiekti iš bet kurios įmonės vykdymo metu. Kai šiame parametre yra ISO valstybės / regiono kodai, formatas komponentą galima pasiekti tik iš tų įmonių, kurių pagrindinis adresas nurodytas kaip vienas iš formato komponento ISO valstybės / regiono kodų.

Skirtingos duomenų formato komponento versijos gali turėti skirtingus ISO valstybės / regiono kodų parametrus.

#### <a name="configuration"></a>Konfigūravimas

ER konfigūracija yra tam tikro ER komponento ER viršelis. Šis komponentas gali būti duomenų modelio komponentas arba formato komponentas. Konfigūracija gali apimti skirtingas ER komponento versijas. Kiekviena konfigūracija pažymėta kaip priklausanti konkrečiam konfigūracijos teikėjui. Konfigūracijos komponento versiją **Juodraštis** galima redaguoti, jei „Finance and Operations“ ER parametruose konfigūracijos savininkas pasirinktas kaip aktyvus teikėjas.

Kiekvienoje modelio konfigūracijoje yra duomenų modelio komponentas. Naują formato konfigūraciją galima gauti iš konkrečios duomenų modelio konfigūracijos. Sukurta formato konfigūracija konfigūracijos medyje atrodo kaip antrinė pradinės duomenų modelio konfigūracijos konfigūracija.

Sukurtoje formato konfigūracijoje yra formato komponentas. Pirminės modelio konfigūracijos duomenų modelio komponentas yra automatiškai įterpiamas į antrinės formato konfigūracijos formato komponentą kaip numatytasis duomenų šaltinis.

„Finance and Operations“ įmonės bendrai naudoja ER konfigūraciją.

#### <a name="provider"></a>Teikėjas

ER teikėjas yra šalies identifikatorius, naudojamas kiekvienos ER konfigūracijos autoriui (savininkui) nurodyti. ER suteikia galimybę valdyti konfigūracijos teikėjų sąrašą. Formatų konfigūracijos, skirtos elektroniniams dokumentams kaip „Finance and Operations“ sprendimo dalis, yra pažymėtos kaip priklausančios konfigūracijos teikėjui **Microsoft**.

Norėdami sužinoti, kaip registruoti naują ER teikėją, paleiskite užduočių vedlį **ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677)** dalis).

#### <a name="repository"></a>Saugykla

ER saugykloje saugomos ER konfigūracijos. Šiuo metu palaikomos dviejų tipų ER saugyklos: **Operacijų ištekliai** ir **LCS projektas**.

**Operacijų išteklių** saugykla suteikia prieigą prie konfigūracijų sąrašo, kurį „Microsoft“, kaip ER konfigūracijų teikėjas, išleidžia kaip „Finance and Operations“ sprendimo dalį. Šias konfigūracijas galima importuoti į esamą „Finance and Operations“ egzempliorių ir naudoti elektroninių ataskaitų kūrimo tikslais. Taip pat jas galima naudoti tolesniam lokalizavimui ir tinkinimui atlikti.

**LCS projekto** saugykla suteikia prieigą prie tam tikro LCS projekto (LCS projekto turto bibliotekos), pasirinkto saugyklos registracijos etape, konfigūracijų sąrašo. ER suteikia galimybę nusiųsti bendrai naudojamas konfigūracijas iš dabartinio „Finance and Operations“ egzemplioriaus į konkrečią **LCS projekto** saugyklą. Taip pat galite konfigūracijas importuoti iš **LCS projekto** saugyklos į dabartinį „Finance and Operations“ egzempliorių.

Galima registruoti atskirai kiekvieno dabartinio „Finance and Operations“ egzemplioriaus konfigūracijos teikėjo būtinas **LCS projekto** saugyklas. Kiekvieną saugyklą galima priskirti konkrečiam konfigūracijos teikėjui.

## <a name="supported-scenarios"></a>Palaikomi scenarijai
### <a name="building-a-data-model"></a>Duomenų modelio kūrimas

ER teikia modelių kūrimo įrankį, kurį galite naudoti konkrečiam verslo domenui skirtam duomenų modeliui kurti. Visus domenui būdingus verslo objektus ir jų ryšius galima pateikti duomenų modelyje kaip hierarchinę struktūrą. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio pavyzdys (mokėjimo domeno duomenų modelis). 

[![Mokėjimo domeno duomenų modelis](./media/ER-overview-04.png)](./media/ER-overview-04.png)

Paleiskite užduočių vedlį **ER konkretaus domeno duomenų modelio kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="translating-data-model-content"></a>Duomenų modelio turinio vertimas

Duomenų modelio turinį (etiketes ir aprašus) galima išversti į kitas „Finance and Operations“ palaikomas kalbas. Duomenų modelio turinį galite norėti išversti dėl toliau nurodytų priežasčių.

-   Norint, kad kitomis kalbomis kalbantys formato kūrėjai, kurie naudos duomenų modelį formato komponentų duomenims susieti, kurdami lengviau suprastų turinį.
-   Norint turinį padaryti patogesnį naudoti vykdymo metu, teikiant vykdymo parametrų raginimus ir pagalbą bei sukonfigūruotus tikrinimo pranešimus (klaidų, įspėjimų) tuo metu prisijungusio vartotojo pageidaujama kalba.

Tolesnėje iliustracijoje pateikiamas pavyzdys, kuriame duomenų modelio turinys išverstas iš anglų k. į japonų k. 

[![Duomenų modelio turinys anglų k.](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Duomenų modelio turinys, išverstas į japonų k.](./media/ER-overview-06.png)](./media/ER-overview-06.png)


### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Siunčiamų dokumentų modelio susiejimų konfigūravimas

ER teikia modelio susiejimų kūrimo įrankį, kurį naudodami vartotojai gali susieti duomenų modelius, kuriuos sukūrė konkretiems „Finance and Operations“ duomenų šaltiniams. Remiantis susiejimu, vykdymo metu į duomenų modelį bus importuojami duomenys iš pasirinktų duomenų šaltinių. Tada duomenų modelis naudojamas kaip ER formatų, kurie generuoja siunčiamus elektroninius dokumentus, abstrakčių duomenų šaltinis. Tolesnėje iliustracijoje pateikiamas tokio tipo duomenų modelio susiejimo pavyzdys (mokėjimo domeno duomenų modelio **SEPA kredito pervedimo** modelio susiejimas). 

[![Duomenų modelio susiejimo pavyzdys](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Paleiskite užduočių vedlius **ER modelio susiejimo nustatymas ir duomenų šaltinių pasirinkimas** ir **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gaunamų dokumentų modelio susiejimų konfigūravimas
ER teikia modelio susiejimų kūrimo įrankį, kurį naudodami vartotojai gali susieti duomenų modelius, kuriuos sukūrė konkrečioms paskirties vietoms. Pavyzdžiui, duomenų modelius galima susieti su „Finance and Operations“ naujintinais duomenų komponentais (lentelėmis, duomenų objektais ir rodiniais). Remiantis susiejimu, vykdymo metu bus atnaujinti „Finance and Operations“ duomenys, naudojant duomenis iš duomenų modelio. Kaip ER formato abstrakti saugykla duomenų modelis užpildomas iš gaunamo elektroninio dokumento importuotais duomenimis. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio susiejimo pavyzdys. Šiame pavyzdyje naudojamas mokėjimo domeno duomenų modelio **Importavimo susiejimas, skirtas NETS** modelio susiejimas, skirtas palaikyti banko išrašų NETS banko formatu importavimą Norvegijoje.

[![Importavimo susiejimo, skirto NETS, duomenų modelio pavyzdys](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Sukurto modelio komponento saugojimas kaip modelio konfigūracijos

ER gali saugoti sukurtą duomenų modelį su susietais duomenų susiejimais kaip dabartinio „Finance and Operations“ egzemplioriaus modelio konfigūraciją. Tolesnėje iliustracijoje pateikiamas šio tipo duomenų modelio konfigūracijos pavyzdys (mokėjimo duomenų modelio konfigūracija). 

Paleiskite užduočių vedlį **ER duomenų modelio susiejimas su pasirinktais duomenų šaltiniais** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Formato kūrimas pasirenkant duomenų modelį kaip pagrindą

ER palaiko formato kūrimo įrankį, kurį galima naudoti norint kurti pasirinkto verslo domeno elektroninio dokumento formatą pasirenkant modelio komponentą kaip pagrindą. Tas pats ER formato kūrimo įrankis teikia galimybę sukurtą formatą susieti su pasirinkto domeno duomenų modelio susiejimu kaip duomenų šaltiniu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys (formato konfigūracija, kad būtų palaikomas Jungtinės Karalystės **BACS** mokėjimo formatas). 

[![Formato, kuriame duomenų modelis naudojamas kaip pagrindas, pavyzdys](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti OPENXML darbalapio formatu, kūrimas

ER formato kūrimo įrankį galima naudoti, norint kurti elektroninį dokumentą OPENXML darbalapio formatu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys (formato konfigūracija, skirta generuoti OPENXML darbalapį su pasirinkto mokėjimo žurnalo informacija).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Paleiskite užduočių vedlį **ER konfigūracijos, skirtos generuoti ataskaitas OPENXML formatu, kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi. Vykdydami užduočių vedlio veiksmą, skirtą importuoti šabloną, kaip šabloną naudokite „Excel“ failą [Mokėjimo ataskaitos šablonas (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfigūracijos, skirtos elektroninius dokumentus generuoti „Word“ dokumento formatu, kūrimas
ER formato kūrimo įrankį galima naudoti, norint kurti elektroninį dokumentą „Word“ dokumento formatu. Tolesnėje iliustracijoje pateikiamas šio tipo formato pavyzdys. Atkreipkite dėmesį, kad šis formatas pakartotinai naudoja esamą ER konfigūraciją, kuri iš pradžių buvo skirta ataskaitos išvesčiai OPENXML formatu generuoti.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Norėdami išsamiai susipažinti su šiuo scenarijumi, paleiskite užduočių vedlį ER konfigūracijos, skirtos generuoti ataskaitas „Microsoft WORD“ formatu, kūrimas (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677) dalis). Vykdant užduoties vadovas veiksmo importuoti šabloną, naudokite šiuos Word failus šablonų nustatymas ER formato:

- [Mokėjimo ataskaitos šablonas (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Susietas mokėjimo ataskaitos šablonas (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfigūracijos, skirtos importuoti duomenis iš gaunamų elektroninių dokumentų, kūrimas  
ER formato kūrimo įrankį galima naudoti norint aprašyti elektroninį dokumentą, kuriam suplanuotas duomenų importavimas XML arba teksto formatu. Sukurta formatas naudojamas išanalizuoti gaunamą dokumentą. ER formato susiejimo kūrimo įrankį galima naudoti norint apibrėžti sukurto formato elementų susiejimą su duomenų modeliu. Tolesnėse iliustracijose pateikiamas šio tipo formato ir formato susiejimo pavyzdys. Šiame pavyzdyje importuoti NETS banko išrašai, kuriuose pateikta tiekėjo mokėjimo informacija tekstiniu formatu.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Norėdami išsamiai susipažinti su šiuo scenarijumi, paleiskite užduočių vedlį ER konfigūracijos, skirtos importuoti duomenis iš išorinio failo, kūrimas (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų / sprendimų komponentų (10677) dalis). Norėdami paleisti šį vedlį, naudokite toliau nurodytus failus.

- [ER duomenų modelio konfigūracija (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER formato konfigūracija (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gaunamo dokumento XML formatu pavyzdys (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Darbaknygės, skirtos tvarkyti gaunamo dokumento duomenis, pavyzdys (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Sukurto formato komponento saugojimas formato konfigūracijoje

ER gali saugoti sukurtą formatą su sukonfigūruotais duomenų susiejimais kaip dabartinio „Finance and Operations“ egzemplioriaus modelio konfigūraciją. Ankstesnėje iliustracijoje pateiktas šio tipo formato konfigūracijos pavyzdys (**BACS (Jungtinė Karalystė)** – antrinis **mokėjimo modelio** konfigūracijos elementas). Paleiskite užduočių vedlį **ER konkretaus domeno formato kūrimas** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>„Finance and Operations“ konfigūravimas, norint pradėti naudoti sukurtą formatą viduje

„Finance and Operations“ galima konfigūruoti, kad ji sukurtą formatą pradėtų naudoti elektroninėms ataskaitoms generuoti. Nuoroda į sukurto formato konfigūraciją turi būti apibrėžta naudojant konkretaus domeno parametrus. Pvz., norint pradėti naudoti ER formato konfigūraciją elektroniniams tiekėjo mokėjimams BACS formatu apdoroti, formato konfigūraciją reikia nurodyti konkrečiuose mokėjimo būduose, kaip parodyta tolesnėse iliustracijose. 

[![BACS (JK) formato konfigūracija](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![BACS (JK) formato nurodymas mokėjimo būde](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Paleiskite užduočių vedlį **ER formato naudojimas elektroniniams mokėjimų dokumentams generuoti** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="handling-er-components"></a>ER komponentų tvarkymas
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER komponento publikavimas LCS, pateikiant jį naudoti išorėje (lokalizavimas)

Sukurto komponento (modelio arba formato) savininkas gali naudoti ER baigtai komponento versijai publikuoti LCS. Tam būtina dabartinio ER konfigūracijos teikėjo **LCS projekto** tipo saugykla. Kai baigtos komponento versijos būsena pakeičiama iš **BAIGTA** į **BENDRAI NAUDOJAMA**, ta versija publikuojama LCS. Publikavus komponentą LCS, to komponento savininkas tampa paslaugos teikėju, palaikančiu šį komponentą. Pavyzdžiui, jei formato komponentas yra skirtas pagal įstatymus būtinam elektroniniam dokumentui generuoti (pavyzdžiui, pagal lokalizavimo scenarijų), manoma, kad formatas turi atitikti teisės aktų pakeitimus ir kad tiekėjas turi išduoti naujas komponento versijas, kai to reikia naujiems įstatymų reikalavimams taikyti. Paleiskite užduočių vedlį **ER konfigūracijos nusiuntimas į „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER komponento importavimas iš LCS naudoti viduje

ER suteikia galimybę importuoti ER komponentus iš LCS į esamą „Finance and Operations“ egzempliorių. Būtina **LCS projekto** tipo saugykla. Importavus ER komponentą iš LCS į esamą „Finance and Operations“ egzempliorių, egzemplioriaus savininkas tampa paslaugos, kurią teikia importuoto komponento savininkas (autorius), vartotoju. Pavyzdžiui, jei šis formato komponentas skirtas konkrečiam elektroniniam dokumentui generuoti iš „Finance and Operations“ tam tikrai valstybei / regionui būdingu formatu (lokalizavimo scenarijus), preziumuojama, kad paslaugos vartotojas galės gauti visus šio formato naujinimus, kad formatas visada atitiktų įstatymų reikalavimus. Paleiskite užduočių vedlį **ER konfigūracijos importavimas iš „Lifecycle Services‟** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis), norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Formato kūrimas pasirinkus kitą formatą kaip pagrindą (tinkinimas)

ER palaiko galimybę kurti (išvesti) naują komponentą iš dabartinės komponento (pagrindo), importuoto iš LCS, versijos. Pavyzdžiui, vartotojas nori išvesti naują formatą, siekdamas patenkinti kai kuriuos specialius elektroninio dokumento reikalavimus (pvz., reikalavimą naudoti papildomą lauką arba išsamų aprašą), kad būtų palaikomas tinkinimo scenarijus. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują jo pagrindinę versiją** (verslo proceso **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Formato versijos naujinimas pasirenkant naują pagrindinio formato versiją (pagrindo keitimas)

ER suteikia galimybę automatiškai priimti naujausios pagrindinio komponento versijos pakeitimus dabartinėje išvestinio komponento juodraščio versijoje. Šis procesas vadinamas *pritaikymu kitoje vietoje*. Pavyzdžiui, naują reguliavimo pakeitimą, įtrauktą į naujausią komponento, importuoto iš LCS, versiją, galima automatiškai sulieti su pritaikyta šio elektroninio dokumento formato versija. Bet kokie pakeitimai, kurių negalima sulieti automatiškai, yra laikomi konfliktais. Šiuos konfliktus galima išspręsti neautomatiniu būdu naudojant atitinkamo komponento kūrimo įrankį. Paleiskite užduočių vedlį **ER formato versijos naujinimas priimant naują to formato pagrindinę versiją** (verslo proceso **7.5.5.3 Įsigyti / sukurti pakeistų IT paslaugų ir sprendimų komponentų (10683)** dalis) norėdami išsamiai susipažinti su šiuo scenarijumi.

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>ER konfigūracijų, kurios pateikiamos „Finance and Operations“ sprendime, sąrašas

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



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Lokalizacijos reikalavimai – elektroninių ataskaitų konfigūracijos kūrimas](electronic-reporting-configuration.md)

[Valdykite Elektroninių ataskaitų konfigūracijos ciklą](general-electronic-reporting-manage-configuration-lifecycle.md)




