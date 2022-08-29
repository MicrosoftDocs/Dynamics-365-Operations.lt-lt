---
title: Tinklelio charakteristikos
description: Šiame straipsnyje aprašomos kelios galinga tinklelio valdiklio funkcijos. Norėdami turėti prieigą prie šių galimybių, turite įjungti naują tinklelio funkcija.
author: jasongre
ms.date: 08/09/2022
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
ms.openlocfilehash: a8968a1263dfafd67b07b4beb78c51493e95756e
ms.sourcegitcommit: 47534a943f87a9931066e28f5d59323776e6ac65
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9258954"
---
# <a name="grid-capabilities"></a>Tinklelio charakteristikos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Naujas tinklelio valdiklis suteikia keletą naudingų ir galingų charakteristikų, kurias galite naudoti siekiant pagerinti vartotojo produktyvumą, kurti įdomesnius savo duomenų rodinius ir gauti prasmingų įžvalgų dėl duomenų. Šiame straipsnyje aptariamos šios charakteristikos: 

- Apskaičiuotų verčių rodymas 
- Rašymas anksčiau sistemos
- Matematinių išraiškų vertinimas 
- Grupavimo skirtukų duomenys (įgalinami atskirai, naudojant **funkciją Grupavimas tinkleliuose**)
- Įšaldyti stulpeliai (įgalinami atskirai, naudojant tinklelių **funkciją Įšaldyti** stulpelius)
- Automatiškai talpinti stulpelio plotį
- Ištempti stulpeliai

## <a name="showing-calculated-values"></a>Apskaičiuotų verčių rodymas
Finansų ir operacijų programėlių vartotojai gali peržiūrėti apskaičiuotą kiekvieno skaitinio stulpelio tinklelyje vertę. Poraštės dalis tinklelio apačioje rodo šias apskaičiuotas vertes.

[![Apskaičiuotų verčių rodymas tinkleliuose.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Versijose iki 10.0.29 visa suma yra vienintelė palaikoma apskaičiuota vertė. Tačiau, kaip ir versijoje 10.0.29, po to, **kai** jie įgalina išplėstinio tinklelio telkimo galimybių funkciją, vartotojai gali pasirinkti iš šių keturių apskaičiuotų verčių:

- Minimumas
- Maksimumas
- Bendroji suma
- Vidurkis

Viename stulpelyje gali būti rodomas tik vienas apskaičiuotos vertės tipas. Tačiau kiekvienas tinklelio stulpelis gali būti konfigūruojamas rodyti skirtingą apskaičiuotos vertės tipą.

### <a name="showing-the-grid-footer"></a>Tinklelio poraštės rodymas
Kiekvieno finansų ir operacijų programėlių skirtukų tinklelio apačioje yra poraštės sritis. Poraštėje gali būti vertingos informacijos, susijusios su duomenimis, kurie rodomi tinklelyje. Toliau pateikiami keletas šios informacijos pavyzdžių:

- Pažymėtų lentelės eilučių skaičius (kai pasirenkate daugiau nei vieną įrašą)
- Apskaičiuotos vertės sukonfigūruotų stulpelių apačioje, skaitiniai stulpeliai (pvz., bendrosios sumos)
- Duomenų rinkinį sudarančių eilučių skaičius 

Numatyta, kad ši poraštė paslėpta, bet ją galima įjungti. Norėdami rodyti tinklelio poraštę, rinkitės **Tinklelio parinktys** mygtuką antraštėje ir tada rinkitės **Rodyti poraštę** parinktį. Įjungus konkretaus tinklelio poraštę, šis parametras bus įsimintas tol, kol vartotojas rinksis slėpti poraštę. Norėdami paslėpti poraštę, tinklelio **Slėpti poraštę** meniu **Tinklo parinktys**.

### <a name="specifying-columns-with-calculated-values"></a>Stulpelių su apskaičiuotomis vertėmis nurodymas
Šiuo metu nėra stulpelių, pagal numatytuosius nustatymus skaičiuojamos vertės. Vietoj to nustatymas laikomas vienkarte veikla, pvz., stulpelių pločio koregavimas tinkleliuose. Kai nurodote, kad norite peržiūrėti apskaičiuotą stulpelio vertę, tas parametras bus atsimintas, kai kitą kartą aplankysite puslapį.

Yra du būdai sukonfigūruoti stulpelį, kad būtų rodoma apskaičiuota vertė:

- Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) stulpelyje, kurio apskaičiuotą vertę norite peržiūrėti. Jei įgalinta **išplėstinio tinklelio telkimo** galimybių funkcija, pasirinkite **Peržiūrėti stulpelio sumas**, tada pasirinkite norimą apskaičiuotą vertę. Jei ši funkcija neįgalinta, pasirinkite Šio stulpelio **Suma**. Dėl šio veiksmo atsiranda trys įvykiai:

    1. Tinklelio poraštė tampa matoma. 
    2. Jūsų nuostatos dėl apskaičiuotos stulpelio vertės peržiūros įrašomos. 
    3. Pradedamas pageidaujamas stulpelio ir visų kitų stulpelių, kuriuos anksčiau konfigūravote, kad rodytų apskaičiuotą vertę, skaičiavimas. Laikas, kurio reikia apskaičiuotoms vertėms rodyti, priklauso nuo duomenų rinkinio dydžio.

- Kai poraštė matoma, stulpelio, kurio apskaičiuotą vertę norite peržiūrėti, apačioje, poraštės srityje pasirinkite Rodyti bendrą sumą (**·** **arba** Pasirinkti apskaičiuotą vertę, **jei** įgalinta išplėstinio tinklelio telkimo galimybių funkcija). Jei nėra sukonfigūruotų stulpelių, tą mygtuką bus galima rasti visų skaitinių stulpelių poraštėje.

    Kai bent vienas stulpelis konfigūruojamas rodyti apskaičiuotą vertę, **mygtukas** Rodyti bendrą sumą (**arba** Pasirinkti apskaičiuotą vertę) bus galimas tik prie hover arba focus. Mygtuko pasirinkimo veiksmas tik įrašo jūsų nuostatas dėl apskaičiuotos vertės peržiūros stulpelyje, kad nuostatos būtų taikomos būsimų apsilankymų puslapyje metu. Poraštėje ši būsena nurodoma brūkšniu, kuris rodomas stulpelyje. (Atkreipkite dėmesį, kad apskaičiuota vertė iš karto atsiras, jei duomenų rinkinys yra pakankamai mažas.)

Jei darote klaidą ir nebenorite peržiūrėti apskaičiuotos vertės konkrečiame stulpelyje, stulpelyje pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku), **tada** pasirinkite Slėpti sumą (**arba Rodyti stulpelių sumas \>** **Nėra**, jei įgalinta išplėstinio tinklelio telkimo galimybių funkcija). Arba to stulpelio **poraštėje** pasirinkite **Slėpti sumą** (arba Slėpti apskaičiuotą vertę). Šis pasirinkimas taip pat bus įrašytas kitus kartus lankantis puslapyje. 

### <a name="calculating-aggregate-values"></a>Skaičiuojamos suvestinės vertės
Kai pereisite į puslapį, kuriame matoma poraštė, o stulpeliai jau sukonfigūruoti rodyti apskaičiuotas vertes, tos vertės gali būti nerodoma poraštę. Veikimo būdas priklauso nuo puslapio duomenų rinkinio dydžio. Jei duomenų rinkinys yra pakankamai mažas, apskaičiuotos vertės bus rodomos automatiškai kartu su duomenų rinkinio eilučių skaičiumi. Jei poraštės brūkšniais rodomi po stulpeliais, kuriuos sukonfigūravote, duomenų rinkinys per didelis, kad sistema apskaičiuotų vertes rodtų iš karto. Šiuo atveju norint apskaičiuoti vertes reikia pateikti aiškius veiksmus. Norėdami apskaičiuoti vertes, poraštėje **pasirinkite** mygtuką Skaičiuoti. Arba pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) stulpelyje, kurio sumą norite peržiūrėti, **ir** tada pasirinkite Bendroji šio stulpelio suma (**arba Peržiūrėti stulpelio sumas** **ir** norimą apskaičiuotą reikšmę, jei įgalinta išplėstinio tinklelio telkimo galimybių funkcija).

Jei skaičiavimui atlikti reikia daug laiko, galite bet kuriuo metu atšaukti operaciją pasirinkdami **Atšaukti**. Kartais duomenų rinkinys bus per didelis, kad apskaičiuotų sudėti vertes (ribą, kurią riboja jūsų organizacija). Šiuo atveju jums bus pranešta apie tai, kaip filtruoti duomenis daugiau.

> [!NOTE]
> Sistemos **administratoriai** **gali modifikuoti įrašų, kuriuos galima sudėti sumai skaičiuoti, limitą koreguodami maksimalų kiekvieno tinklelio parametro vietinių įrašų skaičių kliento našumo pasirinkčių** puslapyje. Numatytoji vertė – 25 000 įrašų. Administratoriai turi būti atsargūs koreguodami šią reikšmę, nes per didelė vertė gali užims vartotojo kompiuteryje prieinamą atminties kiekį. Rekomenduojame, kad vertė neviršytų 50 000 įrašų.

Apskaičiuotos vertės bus automatiškai atnaujintos atnaujinus, naikinat ar kuriant duomenų rinkinio eilutes.

## <a name="typing-ahead-of-the-system"></a>Rašymas anksčiau sistemos
Daugelyje verslo scenarijų itin svarbu greitai įvesti duomenis į sistemą. Prieš pradedant taikyti naują tinklelio valdiklį, vartotojai gali keisti tik dabartinės eilutės duomenis. Todėl, kai jie atliko eilutės pakeitimus, vartotojai negali perjungti į kitą eilutę ar sukurti naujos eilutės, kol sistema sėkmingai nepatvirtino dabartinės eilutės pakeitimų ir (eilutės kūrimo atveju) atliko visą logiką, susijusią su naujos eilutės sukūrimu. Siekiant sumažinti laiką, kurį vartotojai praleidžia laukia šių operacijų pabaigos, ir padėti padidinti vartotojų produktyvumą, naujas tinklelis koreguoja šiuos veiksmus taip, kad jie būtų asinchroniniai. Vartotojai gali kurti naujas eilutes arba perkelti į kitas eilutes, kad būtų atlikti pakeitimai, laukiant ankstesnių eilučių tikrinimo ir eilučių kūrimo logikos. 

[![Įvesti tekstą į priekį iki sistemos.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Siekiant palaikyti šį naują veikimą, kai tinklelis veikia redagavimo režimu, eilutės pasirinkimo stulpelio dešinėje įtraukiamas naujas eilutės būsenos stulpelis. Šiame stulpelyje rodoma viena iš tolesnių būsenų.

- **Tuščia** – jei nėra būsenos vaizdo, tai nurodo, kad sistema sėkmingai įrašė eilutę.
- **Apdorojimas laukia patvirtinimo** – ši būsena rodo, kad serveryje dar neįrašyti eilutės keitimai, tačiau jie yra keitimų, kuriuos reikia apdoroti, eilėje. Prieš imdamiesi veiksmų ne tinklelyje turite palaukti, kol bus apdoroti visi laukiantys keitimai. Be to, šių eilučių tekstas parašomas kursyvu, kad nurodytų neįrašytą eilučių būseną. 
- **Netinkama būsena** – ši būsena nurodo, kad apdorojant eilutę buvo suaktyvintas įspėjimas arba pranešimas, ir tai galėjo neleisti sistemai įrašyti šios eilutės keitimus. Senajame tinklelyje, jei įrašymo operacija buvo nesėkminga, buvote priversti grįžti atgal į eilutę, kad išspręstumėte problemą iš karto. Naujame tinklelyje jums pranešama, kad įvyko tikrinimo problema, tačiau jūs galite nuspręsti, kada norite taisyti bet kurias eilutės problemas. Kai esate pasiruošę ištaisyti problemą, galite rankiniu būdu pereiti atgal į eilutę. Taip pat galite pasirinkti veiksmą **Išspręsti šią problemą**. Pasirinkus šį veiksmą iš karto pereinama atgal į eilutę, kurioje yra problema, ir leidžiama redaguoti tinklelyje arba ne tinklelyje. Atkreipkite dėmesį, kad tolesnių laukiančių eilučių apdorojimas sustabdomas, kol išsprendžiamas šis tikrinimo įspėjimas. 
- **Pristabdyta** – ši būsena rodo, kad apdorojimas serveryje pristabdytas, nes tikrinant eilutę buvo suaktyvintas iššokantysis dialogo langas, reikalaujantis vartotojo įvesties. Kadangi vartotojas tuo metu gali vesti duomenis kitoje eilutėje, iššokantysis dialogo langas nėra iš karto pateikiamas vartotojui. Jis bus pateiktas, kai vartotojas nuspręs tęsti apdorojimą. Šią būseną lydi pranešimas, pranešantis vartotojui apie situaciją. Pranešime yra veiksmas **Tęsti apdorojimą**, kuris suaktyvina iššokantįjį dialogo langą.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Skirtumai įvedant duomenis į priekį nuo sistemos
Kai įvedate duomenis už vietos, kurioje sistema apdoros, galite tikisi iš kelių duomenų įvedimo patirties pakeitimų:

- Atkreipkite dėmesį, kad nėra peržvalgos išplečiamojo sąrašo, lauko vertės nėra patikrinamos jums perėjus į kitą tos pačios eilutės stulpelį, o stulpeliai iš pradžių nerodo numatytųjų verčių. Taip nutinka, kai kuriate arba atnaujinate anksčiau nei sistemoje. Tačiau sistemai persekiant iki vietos, kurioje šiuo metu redaguojate, standartinė patirtis bus tęsiama. Jei keičiate lauką, kuris paprastai gauna numatytąją vertę, jūsų pakeitimai panaikina numatytąją lauko vertę serveriui pradedant apdoroti eilutę.
- Jei sukuriate naują eilutę naudodami rodyklės **žemyn klavišą**, visi tinklelio stulpeliai bus rodomi kaip redaguojami. Pagal numatytuosius nustatymus židinio bus pirmojo stulpelio naujoje eilutėje. Šiame stulpelyje gali būti ne tas pats stulpelis, kuris gavo pradinį židinį į senesnį tinklelį, arba tas pats stulpelis **, kuris fokusuoja pažymėjus mygtuką** Naujas. Jūsų organizacija gali pritaikyti sistemą ir pakeisti stulpelį, kuris, pasirinkus rodyklės **žemyn raktą, gauna pradinį** židinį. Daugiau informacijos ieškokite stulpelyje [, kuris gauna pradinį židinį, kai naujos eilutės sukuriamos naudojant rodyklės į apačią klavišų skyrių,](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key) nurodymas. Nepaisant to, galite naudoti personalizavimą, norėdami optimizuoti kiekvieną tinklelį duomenų įrašui. Galite keisti laukų tvarką taip, kad pirmasis stulpelis būtų stulpelis, kuriame norite pradėti įvesti duomenis. Taip pat galite norėti pakeisti duomenų įvedimo laukus, sumažinti skirtukų sustoja ir slėpti laukus, kurių nereikia norint įvesti duomenis šiame konkrečiame rodinyje.

### <a name="pasting-from-excel"></a>Įklijavimas iš „Excel”
Vartotojai visada galėjo eksportuoti duomenis iš finansų ir operacijų programėlių tinklelių Microsoft Excel naudodami eksportavimo į **Excel mechanizmą**. Tačiau galimybė įvesti duomenis į priekį iki sistemos leidžia naujam tinkleliui palaikyti lentelių kopijavimą iš Excel ir įklijuoti jas tiesiai į finansų ir operacijų programėlių tinklelius. Tinklelio langelis, kuriame inicijuojama įklijavimo operacija, nustato, kur pradedamas nukopijuotos lentelės įklijavimas. Tinklelio turinys perrašomas nukopijuotos lentelės turiniu, išskyrus du tolesnius atvejus.

- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, vartotojas informuojamas, kad papildomų stulpelių, pradedant nuo įklijavimo vietos, nepaisoma. 
- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, pradedant nuo įklijavimo vietos, esami langeliai perrašomi įklijuotu turiniu, o visos papildomos nukopijuotos lentelės eilutės įterpiamos kaip naujos eilutės tinklelio apačioje. 

## <a name="evaluating-math-expressions"></a>Matematinių išraiškų vertinimas
Norėdami didinti produktyvumą vartotojai gali įvesti matematines formules tinklelyje esančiuose skaitiniuose langeliuose. Jiems nebereikia atlikti skaičiavimo programoje, esančioje ne sistemoje. Pavyzdžiui, jei įvesite **=15\*4**, o tada paspausite klavišą **TAB**, kad perkeltumėte lauką, sistema įvertins išraišką ir įrašys į lauką vertę **60**.

[![Matematinių išraiškų vertinimą.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Norėdami, kad sistema atpažintų vertę kaip išraišką, paleiskite reikšmę su lygybės ženklu (**=**). Daugiau informacijos apie palaikomus operatorius ir sintaksę žr. [Palaikomi matematiniai simboliai](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Kaip ir versija 10.0.29, gebėjimas įvertinti matematines išraiškas skaitiniais valdikliais buvo išplėstas ir dabar yra galimas ne tinklelyje.

## <a name="grouping-tabular-data"></a>Lentelės duomenų grupavimas
Verslo vartotojai dažnai turi atlikti ad hoc duomenų analizę. Microsoft Excel Nors šią analizę galima atlikti eksportuojant duomenis į ir naudojant suvestines lenteles **,** tinklelių grupavimo funkcija, kuri priklauso nuo naujos tinklelio valdymo funkcijos, suteikia vartotojams galimybę tvarkyti savo skirtukų duomenis delspinigių ir operacijų programėlių būdais. Kadangi ši funkcija išplečia apskaičiuotų **verčių** priemonę, **grupavimas** leidžia prasmingai geriau suprasti duomenis, pateikiant apskaičiuotas vertes (pvz., tarpines sumas) grupės lygiu.

[![Duomenų grupavimas tinklelyje.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Norėdami naudoti šią funkciją, dešiniuoju pelės klavišu spustelėkite stulpelį, pagal kurį norite grupuoti, ir pasirinkite **Grupuoti pagal šį stulpelį**. Šiuo veiksmu duomenys bus surūšiuoti pagal pasirinktą stulpelį, įtraukta nauja **grupė pagal stulpelį** į tinklelio pradžią ir įterptos „antraštės eilutės“ kiekvienos grupės pradžioje. Šios antraštės eilutės teikia šią informaciją apie kiekvieną grupę:

- Grupės duomenų reikšmė 
- Stulpelio pavadinimas (ši informacija bus itin naudinga, kai palaikomi keli grupavimo lygiai)
- Šios grupės duomenų eilučių skaičius
- Apskaičiuotos bet kurio sukonfigūruoto stulpelio vertės (pvz., tarpinės sumos, jei stulpelis sukonfigūruotas rodyti sumą)

Įgalinus [įrašytus](saved-views.md) rodinius, grupavimą galite įrašyti kaip dalį puslapių rodinio, leidžiančių įrašyti užklausas į rodinius. Pavyzdžiui, tie, kurie turi didelės peržiūros išrinkiklį. Išsamesnės informacijos [žr. peržiūrų](saved-views.md#switching-between-views) perjungimo skyriuje. 

### <a name="multiple-levels-of-grouping"></a>Keli grupavimo lygiai
Sugrupuotus duomenis pagal vieną stulpelį, galite grupuoti duomenis pagal stulpelį, pasirinkdami **Grupuoti pagal šį stulpelį**. Šis procesas gali būti kartojamas, kol bus 5 įdėtieji grupavimo lygiai, kurie yra maksimaliai palaikomi gylis. Šiuo metu nebegalėsite grupuoti pagal papildomus stulpelius.

Bet kuriuo metu galite pašalinti grupavimą bet kuriame stulpelyje dešiniuoju pelės klavišu spustelėję tą stulpelį ir pasirinkdami **Išgrupuoti**. Taip pat galite pašalinti grupavimą iš visų stulpelių, pasirinkdami **Tinklelio parinktys** ir **Išgrupuoti viską**.

### <a name="sorting-grouped-data"></a>Sugrupuotų duomenų rūšiavimas
Sugrupę duomenis viename arba daugiau stulpelių, galite pakeisti bet kurio grupavimo stulpelio rūšiavimo kryptį atitinkamoje stulpelio antraštėje. 

Jei rūšiuojate negrupuojate stulpelyje, grupavimo likutis lieka nesugadintas. Duomenys rūšiuojami kiekvienoje grupėje, remiantis pasirinktu stulpeliu.

### <a name="expanding-and-collapsing-groups"></a>Grupių išplėtimas ir sutraukimas
Pradiniame duomenų grupavime bus išplėstos visos grupės. Galite kurti apibendrintus duomenų rodinius sutraukdami atskiras grupes, taip pat galite naudoti grupių išplėtimą ir sutraukimą, kad būtų lengviau naršyti duomenis. Norėdami išplėsti arba sutraukti grupę, atitinkamoje grupės antraštės eilutėje pasirinkite ševrono (>) mygtuką. Atkreipkite dėmesį, kad atskirų grupių išskleidimo / sutraukimo būsena **neįrašoma** personalizavimo parametruose.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Eilučių pažymėjimas ir žymėjimo naikinimas grupės lygyje
Lygiai taip pat, kaip galite pažymėti visas tinklelio eilutes (arba panaikinti jų žymėjimą), pažymėdami žymimąjį langelį tinklelio pirmojo stulpelio viršuje, galite greitai pažymėti visas grupės eilutes (arba panaikinti jų žymėjimą) pasirinkdami žymės langelį atitinkamoje grupės antraštės eilutėje. Grupės antraštės eilutėje esantis žymės langelis visada atspindės dabartinę tos grupės eilučių žymėjimo būseną, nepriklausomai nuo to, ar pasirinktos visos eilutės, ar nepasirinkta nei viena eilutė, ar pasirinktos kelios eilutės.

### <a name="hiding-column-names"></a>Stulpelių pavadinimų slėpimas
Grupuojant duomenis numatytasis veikimas yra rodyti stulpelio pavadinimą grupės antraštės eilutėje. Galite pasirinkti nerodyti stulpelio pavadinimo grupės antraštės eilutėse pasirinkdami **Tinklelio parinktys** > **Slėpti grupės stulpelio pavadinimą**.

### <a name="grouping-on-date-and-time-columns"></a>Datos ir laiko stulpelių grupavimas
Kai grupuoti naudojate laukus Data arba DateTime, turite pasirinktį grupuoti pagal metus, mėnesį ar dieną. Atitinkamos antraštės eilutės grupė "vertė" atitiks to lauko formatą. Be to, laukuose DateTime ir Laikas galite grupuoti pagal valandą, minutę ar sekundę.

> [!IMPORTANT]
> Dabar vartotojai negali įtraukti grupavimo stulpelio po to, kai jie grupuoja į datos arba laiko stulpelio segmentą.

## <a name="freezing-columns"></a>Fiksuoti stulpeliai
Kai kurie tinklelio stulpeliai gali būti labai svarbūs kontekstui, tad nenorite, kad jie praslinktų per rodinį. Galbūt norėsite, kad tų stulpelių vertės būtų visada matomos. Įšaldę **stulpelius tinklelio** funkcija suteikia vartotojams galimybę lanksčiai. 

[![Į tinklelį įšaldyti stulpeliai.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Norėdami užfiksuoti stulpelį, dešiniuoju pelės klavišu spustelėkite stulpelio antraštę ir pasirinkite **Fiksuoti stulpelį**. Pirmą kartą užbaigus šį veiksmą, pasirinktas stulpelis tampa pirmu stulpeliu ir daugiau neišslinks iš rodinio. Bet kuris kitas vėliau užblokuotas stulpelis bus pridėtas paskutinio užfiksuoto stulpelio dešinėje pusėje. Galite naudoti standartinę funkciją Perkelti pertvarkyti užfiksuotiems stulpeliams taip, kaip jūs norite. Tačiau užfiksuotų stulpelių negalima perkelti taip, kad jie būtų rodomi tarp nefiksuotų stulpelių rinkinio. Taip pat, nefiksuotų stulpelių negalima perkelti taip, kad jie būtų rodomi tarp fiksuotų stulpelių rinkinio.

Norėdami panaikinti stulpelio fiksavimą, dešiniuoju pelės klavišu spustelėkite fiksuoto stulpelio antraštę ir pasirinkite **Nebefiksuoti stulpelio**. 

Atkreipkite dėmesį, kad eilučių pasirinkimo ir būsenos stulpeliai naujame tinklelyje yra visada užfiksuojami kaip du pirmieji stulpeliai. Todėl, kai šie stulpeliai yra įtraukti į tinklelį, jie visada bus matomi vartotojams, neatsižvelgiant į horizontaliosios slinkties padėtį tinklelyje. Šių dviejų stulpelių negalima pertvarkyti.

## <a name="autofit-column-width"></a>Automatiškai talpinti stulpelio plotį
Kaip ir Excel, vartotojai gali priversti automatiškai keisti stulpelio dydį, atsižvelgiant į jame rodomą turinį. Tiesiog du kartus (arba dukart spustelėkite) dydžio keitimo rankeną stulpelyje. Taip pat galite aktyvinti stulpelio antraštėje ir pasirinkti **raktą A** (automatinės konfigūracijos).

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kaip įjungti naują tinklelio valdiklį mano aplinkoje? 

Funkcija **Naujo tinklelio valdymas** yra prieinama tiesiogiai funkcijų valdyme bet kurioje aplinkoje. Įgalinus funkciją Funkcijų valdyme, visi vėlesni vartotojų seansai turės naudoti naują tinklelio valdiklį. 

Numatyta, kad ši priemonė pradėta įgalinti versijoje 10.0.21. Tikslinis jis yra privalomas 2022 m. spalio mėn.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Kūrėjas] Individualių puslapių pasirinkimas naudojant naują tinklelį 
Jei jūsų organizacija atranda puslapį, kuris turi tam tikrų problemų naudodama naują tinklelį, API yra prieinama tam, kad leistų individualiai formuoti naudojant ankstesnio tinklelio valdymą ir leidžiant jūsų sistemos likusiai daliai naudoti naujo tinklelio valdymą. Individualaus puslapio rodymui iš naujojo tinklelio, į formą įtraukite tolesnius skambinimo viešinimus `super()` naudodami `run()` metodą.

```this.forceLegacyGrid();```

Api galiausiai bus pasenusi ir bus leidžiama pašalinti senesnius tinklelio valdiklius. Tačiau jis bus galimas mažiausiai 12 mėnesių po to, kai bus pasisenęs. Jei sprendžiant tam tikras problemas reikia naudoti šią API, praneškite apie jas „Microsoft”.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Norint pasirinkti puslapį naudoti naują tinklelį, prieš tai pasirinkus tinklelį
Jei esate pasirinkę atskirą puslapį naudoti naują tinklelį, vėliau, išspręsę susijusias problemas, galite norėti iš naujo įgalinti naują tinklelį. Norėdami tai padaryti, tiesiog reikia pašalinti `forceLegacyGrid()` iškvietimą. Pakeitimas įsigalios tik tada, kai:

- **Aplinkos pakartotinis diegimas**: kai aplinka atnaujinama ir diegiama iš naujo, lentelė, kurioje saugomi puslapiai, kurie atsijungė nuo naujo tinklelio (FormControlReactGridState) automatiškai išvalomi.
- **Neautomatinis lentelės išvalymas**: programavimo scenarijuose turėsite naudoti SQL norėdami išvalyti lentelę FormControlReactGridState, tada iš naujo paleisti AOS. Šiuo veiksmų deriniu bus iš naujo nustatytas puslapių, kurie buvo pasirinkti iš naujo tinklelio, kaupimas talpykloje.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Programuotojas] Atskirų tinklelių pasirinkimas už sistemos galimybių neįvedimo
Kai kurie scenarijai iškilo taip, kad neuždirbtų *savęs* ir nedirbtų prie mygtukyno sistemos pajėgumo. (Pvz., kai kurie kodai, kurie paleidžiami, kai patikrinama eilutė, sukelia duomenų šaltinio tyrimų paleidimą, todėl tyrimas gali sugadinti neįvestus esamų eilučių redagavimus.) Jei jūsų organizacija apranda tokį scenarijų, GALIMA naudoti API, kuris leidžia programuotojui pasirinkti atskirą tinklelį be nesinchroninio eilutės tikrinimo ir grįžti prie senesnio veikimo būdo.

Kai asinchroninis eilučių tikrinimas išjungtas tinklelyje, vartotojai negali kurti naujos eilutės arba perkelti į kitą esamą eilutę tinklelyje, kol yra dabartinės eilutės tikrinimo problemų. Kadangi šis veiksmas turi įtakos, lentelės negali būti įklijuotos iš Excel į finansų ir operacijų tinklelius.

Norėdami pasirinkti atskirą tinklelį patikrinti asinchroniškai, `super()` po formos metodo pridėkite `run()` šį iškvietimą.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Šis iškvietimas turėtų būti iškviestas tik išskirtiniais atvejais ir neturėtų būti visų tinklelių norma.
> - Mes nerekomenduojame perjungiti šios API vykdymo metu po formos krovinio.

## <a name="developer-size-to-available-width-columns"></a>[Kūrėjas] Iki galimo pločio dydžio stulpeliai
Jei kūrėjas nustato **WidthMode** ypatybę į **SizeToAvailable** stulpeliams naujame tinklelyje, tie stulpeliai iš pradžių turi tokį plotį, kokį jie turėtų, jei ypatybė būtų nustatyta į **SizeToContent**. Tačiau jie ištempiami, norint tinklelyje naudoti bet kokį galimą papildomą plotį. Jei ypatybė nustatyta į **SizeToAvailable** keliems stulpeliams, visi šie stulpeliai bendrai naudoja bet kokį galimą papildomą plotį tinklelyje. Tačiau, jei vartotojas rankiniu būdu keičia vieno iš šių stulpelių dydį, stulpelis tampa statiniu. Jis išliks tokio pločio ir nebebus ištempiamas, kad būtų galima naudoti galimą papildomą tinklelio plotį.

## <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Programuotojas] Stulpelio, kuris gauna pradinį židinį, kai naujos eilutės kuriamos naudojant rodyklės žemyn klavišą, nurodymas
[Kaip](#differences-when-entering-data-ahead-of-the-system) buvo aptarta skirtumus įvedant duomenis už sistemos skyriaus, jei galimybė Įvesti **anksčiau** už sistemos, o vartotojas sukuria naują eilutę naudodamas rodyklės žemyn raktą, numatytoji veikimo būdas yra įtraukti židinį į pirmą naujos eilutės stulpelį. Ši patirtis gali skirtis nuo patirties senesnime tinklelyje arba **pasirinkus** mygtuką Naujas.

Vartotojai ir organizacijos gali kurti įrašytus rodinius, optimizuotus įvesti duomenis. (Pvz., galite užsakyti stulpelius taip, kad pirmasis stulpelis būtų tas, kuriame norite pradėti įvesti duomenis.) Be to, kaip ir 10.0.29 versiją, **organizacijos gali koreguoti šį elgseną, naudodamas pasirinktąControlOnCreate()** metodą. Šis būdas leidžia programuotojui nurodyti stulpelį, kuris turi gauti pradinį židinį, kai nauja eilutė sukuriama naudojant rodyklės **žemyn** raktą. Kaip įvestį, ši API paima valdiklio ID, atitinkantį stulpelį, į kurį turėtų būti skiriamas pradinis dėmesys.

## <a name="known-issues"></a>Žinomos problemos
Šiame skyriuje pateikiamas žinomų naujo tinklelio valdiklio problemų sąrašas.

### <a name="open-issues"></a>Atviros problemos
- Įjungus **Naujo tinklelio valdymo** funkciją, kai kurie puslapiai ir toliau naudos esamą tinklelio valdymą. Tai atsitiks esant tokiai situacijai:
 
    - Kortelės sąrašas egzistuoja puslapyje, kuris yra apdorojamas daugelyje stulpelių.
    - Grupuotų kortelių sąrašas egzistuoja puslapyje.
    - Tinklelio stulpelis su ne reaktyviu išplečiamu valdymu.

    Kai vartotojas pirmą kartą susiduria su viena iš šių situacijų, bus rodomas pranešimas dėl puslapio atnaujinimo. Šiai žinutei pasirodžius, puslapis ir toliau naudos esamą tinklelį visiems naudotojams iki kitos produkto naujinimo versijos. Geresnis šių scenarijų valdymas taip, kad naujas tinklelis gali būti naudojamas, bus svarstomas tolesniuose naujinimuose.

- [KB 4582758] Įrašai yra neryškūs, kai keičiate mastelį iš 100 į bet kurį kitą procentą

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

