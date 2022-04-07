---
title: Tinklelio charakteristikos
description: Šioje temoje aprašomos kelios galingos tinklelio valdiklio funkcijos. Norėdami turėti prieigą prie šių galimybių, turite įjungti naują tinklelio funkcija.
author: jasongre
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 81577f54bd7fdc7d683c760dd4410f27da8ee1f0
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462798"
---
# <a name="grid-capabilities"></a>Tinklelio charakteristikos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Naujas tinklelio valdiklis suteikia keletą naudingų ir galingų charakteristikų, kurias galite naudoti siekiant pagerinti vartotojo produktyvumą, kurti įdomesnius savo duomenų rodinius ir gauti prasmingų įžvalgų dėl duomenų. Šiame straipsnyje aptariamos šios charakteristikos: 

- Skaičiuojamos sumos
- Rašymas anksčiau sistemos
- Matematinių išraiškų vertinimas 
- Grupavimo skirtukų duomenys (įgalinami atskirai, naudojant **funkciją Grupavimas tinkleliuose**)
- Įšaldyti stulpeliai (įgalinami atskirai, naudojant tinklelių **funkciją Įšaldyti** stulpelius)
- Automatiškai talpinti stulpelio plotį
- Ištempti stulpeliai

## <a name="calculating-totals"></a>Skaičiuojamos sumos
Finansų ir operacijų programėlių vartotojai gali matyti sumas tinklelių skaitinių stulpelių apačioje. Tinklelio apačioje esančiame poraštės skyriuje rodomos šios bendrosios sumos. 

### <a name="showing-the-grid-footer"></a>Tinklelio poraštės rodymas
Kiekvieno finansų ir operacijų programėlių skirtukų tinklelio apačioje yra poraštės sritis. Poraštėje gali būti vertingos informacijos, susijusios su duomenimis, kurie rodomi tinklelyje. Toliau pateikiami keletas šios informacijos pavyzdžių:

- Pažymėtų lentelės eilučių skaičius (kai pasirenkate daugiau nei vieną įrašą)
- Bendrosios sumos, kurios yra sukonfigūruotų skaitinių stulpelių apačioje
- Duomenų rinkinį sudarančių eilučių skaičius 

Numatyta, kad ši poraštė paslėpta, bet ją galima įjungti. Norėdami rodyti tinklelio poraštę, rinkitės **Tinklelio parinktys** mygtuką antraštėje ir tada rinkitės **Rodyti poraštę** parinktį. Įjungus konkretaus tinklelio poraštę, šis parametras bus įsimintas tol, kol vartotojas rinksis slėpti poraštę. Norėdami paslėpti poraštę, tinklelio **Slėpti poraštę** meniu **Tinklo parinktys**.

### <a name="specifying-columns-with-totals"></a>Stulpelių su bendrosiomis sumomis nurodymas
Šiuo metu nėra stulpelių, kurie rodytų bendrąsias sumas pagal numatytuosius nustatymus. Užuot, tai laikoma vienkartine sąrankos veikla, panašiai kaip stulpelių pločių reguliavimas tinkleliuose. Kai nurodysite, kad norite matyti stulpelio bendrąsias sumas, šis parametras bus įsimenamas, kai kitą kartą lankysitės puslapyje.

Yra du būdai konfigūruoti stulpelį, kad būtų rodoma bendroji suma: 

- Dešiniuoju pelės klavišu spustelėkite ant stulpelio, kurio bendrąją sumą norite matyti, tada pasirinkite **Skaičiuoti šio stulpelio bendrąją sumą**. Dėl šio veiksmo atsiranda trys įvykiai:

    1. Poraštė tampa matoma. 
    2. Įrašomas jūsų pasirinkimas matyti šiame stulpelyje bendrąją sumą. 
    3. Pradedamos skaičiuoti bendrosios sumos šio stulpelio ir visų kitų stulpelių, anksčiau sukonfigūruotų rodyti bendrąsias sumas. Laikas, kurio reikia norint parodyti bendrąją sumą, priklauso nuo duomenų rinkinio, kurį norite sumuoti, dydžio.

- Kai poraštė matoma, pasirinkite **Rodyti bendrąją sumą** poraštės srityje stulpelio, kuriame norite matyti bendrąją sumą, apačioje. Jei nėra sukonfigūruotų stulpelių, mygtukas **Rodyti bendrąją sumą** bus pasiekiamas visiems skaitiniams stulpeliams. 

    Sukonfigūravus bent vieną stulpelį bendrosioms sumoms, mygtukai **Rodyti bendrąją sumą** bus pasiekiami tik užvedus žymiklį ar suatyvinus. Pasirinkus veiksmą **Rodyti bendrąją sumą** tik įrašomi jūsų pasirinkimai, kad būtų galima matyti bendrąją sumą šiame stulpelyje, todėl pasirinkimas bus taikomas kitą kartą lankantis puslapyje. Poraštėje ši būsena nurodoma brūkšniu, kuris rodomas stulpelyje. (Arba, jei duomenų rinkinys yra pakankamai mažas, iš karto rodoma bendroji suma.)

Jei padarėte klaidą ir nebenorite daugiau matyti bendrosios sumos konkrečiame stulpelyje, dešiniuoju pelės klavišu spustelėkite ant stulpelio ir pasirinkite mygtuką **Slėpti bendrąją sumą** arba pasirinkite mygtuką **Slėpti bendrąją sumą** to stulpelio poraštėje. Šis pasirinkimas taip pat bus įrašytas kitus kartus lankantis puslapyje. 

### <a name="calculating-totals"></a>Skaičiuojamos sumos
Kai ateisite į puslapį, kuriame poraštė matoma, o stulpeliuose jau sukonfigūruotos bendrosios sumos, bendrosios sumos gali būti rodomos arba nerodomos poraštėje. Toks veikimas priklauso nuo duomenų rinkinio dydžio puslapyje. Jei duomenų rinkinys yra pakankamai mažas, bendrosios sumos bus rodomos automatiškai, kartu su duomenų rinkinio eilučių skaičiumi. Jei poraštėje yra brūkšnių po stulpeliais, kuriuos sukonfigūravote bendrosioms sumoms, tada duomenų rinkinys yra per didelis sistemai, kad būtų rodomos bendrosios sumos, ir reikia tiesioginio veiksmo bendrosioms sumoms skaičiuoti. Norėdami tai atlikti, poraštėje spustelėkite mygtuką **Skaičiuoti** arba dešiniuoju pelės klavišu spustelėkite stulpelį, kuriame norite gauti bendrąją sumą, ir pasirinkite **Skaičiuoti šio stulpelio bendrąją sumą**.

Jei skaičiavimui atlikti reikia daug laiko, galite atšaukti operaciją, pasirinkdami **mygtuką** Atšaukti. Kartais duomenų rinkinys bus per didelis, kad būtų galima apskaičiuoti sumas (ribą, kurią riboja jūsų organizacija), ir jums bus pranešta apie duomenų filtravimą daugiau. 

> [!NOTE]
> Sistemos administravimo institucijos gali modifikuoti įrašų, kurių galima skaičiuoti **sumas** **, limitą, pakoreguojant maksimalų kiekvieno kliento našumo parinkčių puslapio tinklelio parametro vietinių įrašų** skaičių. Numatytoji vertė – 25 000 įrašų. Koreguojant šią reikšmę administratoriai turėtų būti atsargūs, nes per didelė vertė gali užeiti prie laisvos vartotojo įrenginio atminties. Rekomenduojama ne daugiau kaip 50 000 įrašų.   

Bendrosios sumos bus atnaujintos automatiškai, kai naujinate, naikinate ar kuriate duomenų rinkinyje esančias eilutes.

## <a name="typing-ahead-of-the-system"></a>Rašymas anksčiau sistemos
Daugelyje verslo scenarijų itin svarbu greitai įvesti duomenis į sistemą. Prieš naujo tinklelio valdiklio įvedimą vartotojai galėjo keisti duomenis tik šioje eilutėje. Prieš sukurdami naują eilutę arba perjungdami į kitą eilutę, jie buvo priversti palaukti, kol sistema sėkmingai patikrins visus keitimus. Bandydamas sutrumpinti laiką, kurį vartotojai laukia, kol šie tikrinimai baigiami, ir pagerinti vartotojo produktyvumą, naujas tinklelis koreguoja šiuos tikrinimus, kad jie būtų asinchroniniai. Todėl vartotojas gali pereiti prie kitų eilučių, kad atliktų keitimus, kol ankstesnių eilučių tikrinimai laukia patvirtinimo. 

Siekiant palaikyti šį naują veikimą, kai tinklelis veikia redagavimo režimu, eilutės pasirinkimo stulpelio dešinėje įtraukiamas naujas eilutės būsenos stulpelis. Šiame stulpelyje rodoma viena iš tolesnių būsenų.

- **Tuščia** – jei nėra būsenos vaizdo, tai nurodo, kad sistema sėkmingai įrašė eilutę.
- **Apdorojimas laukia patvirtinimo** – ši būsena rodo, kad serveryje dar neįrašyti eilutės keitimai, tačiau jie yra keitimų, kuriuos reikia apdoroti, eilėje. Prieš imdamiesi veiksmų ne tinklelyje turite palaukti, kol bus apdoroti visi laukiantys keitimai. Be to, šių eilučių tekstas parašomas kursyvu, kad nurodytų neįrašytą eilučių būseną. 
- **Netinkama būsena** – ši būsena nurodo, kad apdorojant eilutę buvo suaktyvintas įspėjimas arba pranešimas, ir tai galėjo neleisti sistemai įrašyti šios eilutės keitimus. Senajame tinklelyje, jei įrašymo operacija buvo nesėkminga, buvote priversti grįžti atgal į eilutę, kad išspręstumėte problemą iš karto. Naujame tinklelyje jums pranešama, kad įvyko tikrinimo problema, tačiau jūs galite nuspręsti, kada norite taisyti bet kurias eilutės problemas. Kai esate pasiruošę ištaisyti problemą, galite rankiniu būdu pereiti atgal į eilutę. Taip pat galite pasirinkti veiksmą **Išspręsti šią problemą**. Pasirinkus šį veiksmą iš karto pereinama atgal į eilutę, kurioje yra problema, ir leidžiama redaguoti tinklelyje arba ne tinklelyje. Atkreipkite dėmesį, kad tolesnių laukiančių eilučių apdorojimas sustabdomas, kol išsprendžiamas šis tikrinimo įspėjimas. 
- **Pristabdyta** – ši būsena rodo, kad apdorojimas serveryje pristabdytas, nes tikrinant eilutę buvo suaktyvintas iššokantysis dialogo langas, reikalaujantis vartotojo įvesties. Kadangi vartotojas tuo metu gali vesti duomenis kitoje eilutėje, iššokantysis dialogo langas nėra iš karto pateikiamas vartotojui. Jis bus pateiktas, kai vartotojas nuspręs tęsti apdorojimą. Šią būseną lydi pranešimas, pranešantis vartotojui apie situaciją. Pranešime yra veiksmas **Tęsti apdorojimą**, kuris suaktyvina iššokantįjį dialogo langą.

Kai vartotojai įveda duomenis anksčiau vietos, kur serveris vykdo apdorojimą, duomenų įvedimo metu gali įvykti sutrikimų, pvz., peržvalgų, tikrinimo kontrolės lygiu ir numatytųjų reikšmių įvedimo trūkumo. Vartotojams, kuriems reikia išplečiamojo sąrašo rasti reikšmę, patariama palaukti, kol serveris pasivys dabartinę eilutę. Tikrinimas kontrolės lygiu ir numatytųjų reikšmių įvedimas taip pat įvyks tada, kai serveris tą eilutę apdoros.

### <a name="pasting-from-excel"></a>Įklijavimas iš „Excel”
Vartotojai visada galėjo eksportuoti duomenis iš finansų ir operacijų programėlių tinklelių Microsoft Excel naudodami eksportavimo į **Excel mechanizmą**. Tačiau galimybė įvesti duomenis į priekį iki sistemos leidžia naujam tinkleliui palaikyti lentelių kopijavimą iš Excel ir įklijuoti jas tiesiai į finansų ir operacijų programėlių tinklelius. Tinklelio langelis, kuriame inicijuojama įklijavimo operacija, nustato, kur pradedamas nukopijuotos lentelės įklijavimas. Tinklelio turinys perrašomas nukopijuotos lentelės turiniu, išskyrus du tolesnius atvejus.

- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, vartotojas informuojamas, kad papildomų stulpelių, pradedant nuo įklijavimo vietos, nepaisoma. 
- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, pradedant nuo įklijavimo vietos, esami langeliai perrašomi įklijuotu turiniu, o visos papildomos nukopijuotos lentelės eilutės įterpiamos kaip naujos eilutės tinklelio apačioje. 

## <a name="evaluating-math-expressions"></a>Matematinių išraiškų vertinimas
Norėdami didinti produktyvumą vartotojai gali įvesti matematines formules tinklelyje esančiuose skaitiniuose langeliuose. Jiems nebereikia atlikti skaičiavimo programoje, esančioje ne sistemoje. Pavyzdžiui, jei įvesite **=15\*4**, o tada paspausite klavišą **TAB**, kad perkeltumėte lauką, sistema įvertins išraišką ir įrašys į lauką vertę **60**.

Norėdami, kad sistema atpažintų vertę kaip išraišką, paleiskite reikšmę su lygybės ženklu (**=**). Daugiau informacijos apie palaikomus operatorius ir sintaksę žr. [Palaikomi matematiniai simboliai](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Lentelės duomenų grupavimas
Verslo vartotojams dažnai reikia atlikti ad hoc duomenų analizę. Microsoft Excel Kol tai galima atlikti eksportuojant duomenis į ir naudojant suvestinės lenteles **,** tinklelių grupavimo funkcija, kuri priklauso nuo naujos tinklelio valdymo funkcijos, suteikia vartotojams galimybę tvarkyti savo skirtukų duomenis pagal grafiką finansų ir operacijų programėlių būdais. Kadangi ši funkcija praplečia funkcijos **Bendrosios sumos** galimybes, **grupuodami** taip pat galite gauti prasmingų įžvalgų į duomenis, pateikę tarpines sumas grupėms.

Norėdami naudoti šią funkciją, dešiniuoju pelės klavišu spustelėkite stulpelį, pagal kurį norite grupuoti, ir pasirinkite **Grupuoti pagal šį stulpelį**. Šiuo veiksmu duomenys bus surūšiuoti pagal pasirinktą stulpelį, įtraukta nauja **grupė pagal stulpelį** į tinklelio pradžią ir įterptos „antraštės eilutės“ kiekvienos grupės pradžioje. Šios antraštės eilutės teikia šią informaciją apie kiekvieną grupę:

- Grupės duomenų reikšmė 
- Stulpelio pavadinimas (ši informacija bus itin naudinga, kai palaikomi keli grupavimo lygiai)
- Šios grupės duomenų eilučių skaičius
- Visų stulpelių, sukonfigūruotų rodyti bendrąsias sumas, tarpinės sumos

Įjungus [Įrašyti rodiniai](saved-views.md), šį grupavimą galima išsaugoti personalizuojant kaip dalį rodinio sparčiajai prieigai kitą kartą lankantis puslapyje.

### <a name="multiple-levels-of-grouping"></a>Keli grupavimo lygiai
Sugrupuotus duomenis pagal vieną stulpelį, galite grupuoti duomenis pagal stulpelį, pasirinkdami **Grupuoti pagal šį stulpelį**. Šis procesas gali būti kartojamas, kol bus 5 įdėtieji grupavimo lygiai, kurie yra maksimaliai palaikomi gylis. Šiuo metu nebegalėsite grupuoti pagal papildomus stulpelius.

Bet kuriuo metu galite pašalinti grupavimą bet kuriame stulpelyje dešiniuoju pelės klavišu spustelėję tą stulpelį ir pasirinkdami **Išgrupuoti**. Taip pat galite pašalinti grupavimą iš visų stulpelių, pasirinkdami **Tinklelio parinktys** ir **Išgrupuoti viską**.

### <a name="sorting-grouped-data"></a>Sugrupuotų duomenų rūšiavimas
Sugrupę duomenis viename arba daugiau stulpelių, galite pakeisti bet kurio grupavimo stulpelio rūšiavimo kryptį atitinkamoje stulpelio antraštėje. 

Veikimo būdas, kai rūšiuojate nesugrupuotiuose stulpeliuose, priklauso nuo produkto versijos:

- Jei rūšiuojate negrupuotą stulpelį, 10.0.24 ir ankstesnės versijos grupavimas pašalinamas iš visų stulpelių, o duomenys rūšiuojami pasirinktame stulpelyje. 
- Jei rūšiuojate negrupuotą stulpelį, 10.0.25 ir vėlesnėje versijoje grupavimas lieka nesugadintas, o duomenys rūšiuojami kiekvienoje grupėje pagal pasirinktą stulpelį.

### <a name="expanding-and-collapsing-groups"></a>Grupių išplėtimas ir sutraukimas
Pradiniame duomenų grupavime bus išplėstos visos grupės. Galite kurti apibendrintus duomenų rodinius sutraukdami atskiras grupes, taip pat galite naudoti grupių išplėtimą ir sutraukimą, kad būtų lengviau naršyti duomenis. Norėdami išplėsti arba sutraukti grupę, atitinkamoje grupės antraštės eilutėje pasirinkite ševrono (>) mygtuką. Atkreipkite dėmesį, kad atskirų grupių išskleidimo / sutraukimo būsena **neįrašoma** personalizavimo parametruose.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Eilučių pažymėjimas ir žymėjimo naikinimas grupės lygyje
Lygiai taip pat, kaip galite pažymėti visas tinklelio eilutes (arba panaikinti jų žymėjimą), pažymėdami žymimąjį langelį tinklelio pirmojo stulpelio viršuje, galite greitai pažymėti visas grupės eilutes (arba panaikinti jų žymėjimą) pasirinkdami žymės langelį atitinkamoje grupės antraštės eilutėje. Grupės antraštės eilutėje esantis žymės langelis visada atspindės dabartinę tos grupės eilučių žymėjimo būseną, nepriklausomai nuo to, ar pasirinktos visos eilutės, ar nepasirinkta nei viena eilutė, ar pasirinktos kelios eilutės.

### <a name="hiding-column-names"></a>Stulpelių pavadinimų slėpimas
Grupuojant duomenis numatytasis veikimas yra rodyti stulpelio pavadinimą grupės antraštės eilutėje. Galite pasirinkti nerodyti stulpelio pavadinimo grupės antraštės eilutėse pasirinkdami **Tinklelio parinktys** > **Slėpti grupės stulpelio pavadinimą**.

### <a name="grouping-on-date-and-time-columns"></a>Datos ir laiko stulpelių grupavimas
Naudojant versiją 10.0.24 laukuose Data arba DateTime, pasirinktis buvo pridėta prie grupės pagal metus, mėnesį ar dieną. Atitinkamos antraštės eilutės grupė "vertė" atitiks to lauko formatą. Be to, laukuose DateTime ir Laikas galite grupuoti pagal valandą, minutę ar sekundę. 

## <a name="freezing-columns"></a>Fiksuoti stulpeliai
Kai kurie tinklelio stulpeliai gali būti labai svarbūs kontekstui, tad nenorite, kad jie praslinktų per rodinį. Galbūt norėsite, kad tų stulpelių vertės būtų visada matomos. Įšaldę **stulpelius tinklelio** funkcija suteikia vartotojams galimybę lanksčiai. 

Norėdami užfiksuoti stulpelį, dešiniuoju pelės klavišu spustelėkite stulpelio antraštę ir pasirinkite **Fiksuoti stulpelį**. Pirmą kartą užbaigus šį veiksmą, pasirinktas stulpelis tampa pirmu stulpeliu ir daugiau neišslinks iš rodinio. Bet kuris kitas vėliau užblokuotas stulpelis bus pridėtas paskutinio užfiksuoto stulpelio dešinėje pusėje. Galite naudoti standartinę funkciją Perkelti pertvarkyti užfiksuotiems stulpeliams taip, kaip jūs norite. Tačiau užfiksuotų stulpelių negalima perkelti taip, kad jie būtų rodomi tarp nefiksuotų stulpelių rinkinio. Taip pat, nefiksuotų stulpelių negalima perkelti taip, kad jie būtų rodomi tarp fiksuotų stulpelių rinkinio.

Norėdami panaikinti stulpelio fiksavimą, dešiniuoju pelės klavišu spustelėkite fiksuoto stulpelio antraštę ir pasirinkite **Nebefiksuoti stulpelio**. 

Atkreipkite dėmesį, kad eilučių pasirinkimo ir būsenos stulpeliai naujame tinklelyje yra visada užfiksuojami kaip du pirmieji stulpeliai. Todėl, kai šie stulpeliai yra įtraukti į tinklelį, jie visada bus matomi vartotojams, neatsižvelgiant į horizontaliosios slinkties padėtį tinklelyje. Šių dviejų stulpelių negalima pertvarkyti.

## <a name="autofit-column-width"></a>Automatiškai talpinti stulpelio plotį
Panašus į „Excel“ vartotojai gali automatiškai pakeisti stulpelio dydį, atsižvelgiant į tuo metu rodomą to stulpelio turinį. Norėdami tai padaryti, du kartus spustelėkite stulpelio dydžio keitimo ranketes arba pereidami į stulpelio antraštę ir spausdami **A** (automatinės talpinimo). Ši savybė yra prieinama nuo 10.0.23 prekybos versijos.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kaip įjungti naują tinklelio valdiklį mano aplinkoje? 

Funkcija **Naujo tinklelio valdymas** yra prieinama tiesiogiai funkcijų valdyme bet kurioje aplinkoje. Įgalinus funkciją Funkcijų valdyme, visi vėlesni vartotojų seansai turės naudoti naują tinklelio valdiklį. 

Numatyta, kad ši funkcija įgalinta versijoje 10.0.21, ji yra privaloma 2022 m. spalio mėn.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Kūrėjas] Individualių puslapių pasirinkimas naudojant naują tinklelį 
Jei jūsų organizacija atranda puslapį, kuris turi tam tikrų problemų naudodama naują tinklelį, API yra prieinama tam, kad leistų individualiai formuoti naudojant ankstesnio tinklelio valdymą ir leidžiant jūsų sistemos likusiai daliai naudoti naujo tinklelio valdymą. Individualaus puslapio rodymui iš naujojo tinklelio, į formą įtraukite tolesnius skambinimo viešinimus `super()` naudodami `run()` metodą.

```this.forceLegacyGrid();```

Api bus pagerbta, kol naujasis tinklelio valdiklis taps privalomas. Šiuo metu šis pakeitimas skirtas 2022 m. spalio mėn. Jei sprendžiant tam tikras problemas reikia naudoti šią API, praneškite apie jas „Microsoft”.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Norint pasirinkti puslapį naudoti naują tinklelį, prieš tai pasirinkus tinklelį
Jei esate pasirinkę atskirą puslapį naudoti naują tinklelį, vėliau, išspręsę susijusias problemas, galite norėti iš naujo įgalinti naują tinklelį. Norėdami tai padaryti, tiesiog reikia pašalinti `forceLegacyGrid()` iškvietimą. Pakeitimas įsigalios tik tada, kai:

- **Aplinkos pakartotinis diegimas**: kai aplinka atnaujinama ir diegiama iš naujo, lentelė, kurioje saugomi puslapiai, kurie atsijungė nuo naujo tinklelio (FormControlReactGridState) automatiškai išvalomi.
- **Neautomatinis lentelės išvalymas**: programavimo scenarijuose turėsite naudoti SQL norėdami išvalyti lentelę FormControlReactGridState, tada iš naujo paleisti AOS. Šiuo veiksmų deriniu bus iš naujo nustatytas puslapių, kurie buvo pasirinkti iš naujo tinklelio, kaupimas talpykloje.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Programuotojas] Atskirų tinklelių pasirinkimas už sistemos galimybių neįvedimo
Kai kurie scenarijai iškilo taip, kad neuždirbtų *savęs* ir nedirbtų prie mygtukyno sistemos pajėgumo. (Pvz., kai kurie kodai, kurie paleidžiami, kai patikrinama eilutė, sukelia duomenų šaltinio tyrimų paleidimą, todėl tyrimas gali sugadinti neįvestus esamų eilučių redagavimus.) Jei jūsų organizacija apranda tokį scenarijų, GALIMA naudoti API, kuris leidžia programuotojui pasirinkti atskirą tinklelį be nesinchroninio eilutės tikrinimo ir grįžti prie senesnio veikimo būdo.

Kai asinchroninis eilučių tikrinimas išjungtas tinklelyje, vartotojai negali kurti naujos eilutės arba perkelti į kitą esamą eilutę tinklelyje, kol yra dabartinės eilutės tikrinimo problemų. Kadangi šis veiksmas turi įtakos, lentelių negalima įklijuoti iš Excel į finansų ir operacijų tinklelius.

Norėdami pasirinkti atskirą tinklelį patikrinti asinchroniškai, `super()` po formos metodo pridėkite `run()` šį iškvietimą.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Šis iškvietimas turėtų būti iškviestas tik išskirtiniais atvejais ir neturėtų būti visų tinklelių norma.
> - Mes nerekomenduojame perjungiti šios API vykdymo metu po formos krovinio.

## <a name="developer-size-to-available-width-columns"></a>[Kūrėjas] Iki galimo pločio dydžio stulpeliai
Jei kūrėjas nustato **WidthMode** ypatybę į **SizeToAvailable** stulpeliams naujame tinklelyje, tie stulpeliai iš pradžių turi tokį plotį, kokį jie turėtų, jei ypatybė būtų nustatyta į **SizeToContent**. Tačiau jie ištempiami, norint tinklelyje naudoti bet kokį galimą papildomą plotį. Jei ypatybė nustatyta į **SizeToAvailable** keliems stulpeliams, visi šie stulpeliai bendrai naudoja bet kokį galimą papildomą plotį tinklelyje. Tačiau, jei vartotojas rankiniu būdu keičia vieno iš šių stulpelių dydį, stulpelis tampa statiniu. Jis išliks tokio pločio ir nebebus ištempiamas, kad būtų galima naudoti galimą papildomą tinklelio plotį.

## <a name="known-issues"></a>Žinomos problemos
Šiame skyriuje pateikiamas žinomų naujo tinklelio valdiklio problemų sąrašas.

### <a name="open-issues"></a>Atviros problemos
- Įjungus **Naujo tinklelio valdymo** funkciją, kai kurie puslapiai ir toliau naudos esamą tinklelio valdymą. Tai atsitiks esant tokiai situacijai:
 
    - Kortelės sąrašas egzistuoja puslapyje, kuris yra apdorojamas daugelyje stulpelių.
    - Grupuotų kortelių sąrašas egzistuoja puslapyje.
    - Tinklelio stulpelis su ne reaktyviu išplečiamu valdymu.

    Kai vartotojas pirmą kartą susiduria su viena iš šių situacijų, bus rodomas pranešimas dėl puslapio atnaujinimo. Šiai žinutei pasirodžius, puslapis ir toliau naudos esamą tinklelį visiems naudotojams iki kitos produkto naujinimo versijos. Geresnis šių scenarijų valdymas taip, kad naujas tinklelis gali būti naudojamas, bus svarstomas tolesniuose naujinimuose.

- [KB 4582758] Įrašai yra neryškūs, kai keičiate mastelį iš 100 į bet kurį kitą procentą
- [KB 4592012] Netikėta kliento klaida IE11, įklijuojant kelias eilutes iš „Excel”

    „Microsoft” nesiekia šios problemos sprendimo


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
