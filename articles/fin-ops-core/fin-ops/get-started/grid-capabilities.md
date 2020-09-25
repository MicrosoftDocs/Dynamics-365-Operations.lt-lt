---
title: Tinklelio charakteristikos
description: Šioje temoje aprašomos kelios galingos tinklelio valdiklio funkcijos. Norint turėti prieigą prie šių charakteristikų, turi būti įjungta nauja tinklelio funkcija.
author: jasongre
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b4efad8423ab42bf6f7f6e2d1054307c11d31d2c
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760404"
---
# <a name="grid-capabilities"></a>Tinklelio charakteristikos

[!include [banner](../includes/banner.md)]

Naujas tinklelio valdiklis suteikia daug naudingų ir galingų charakteristikų, kurias galima naudoti siekiant pagerinti vartotojo produktyvumą, kurti įdomesnius savo duomenų rodinius ir gauti prasmingų įžvalgų dėl duomenų. Šiame straipsnyje aptariamos šios charakteristikos: 

-  Skaičiuojamos sumos
-  Rašymas anksčiau sistemos
-  Matematinių išraiškų vertinimas 
-  Lentelės duomenų grupavimas (įjungta atskirai naudojant funkciją **(Peržiūra) Grupavimas tinkleliuose**)

## <a name="calculating-totals"></a>Skaičiuojamos sumos
„Finance and Operations“ programose vartotojai gali matyti bendrąsias sumas, esančias tinkleliuose, skaitinių stulpelių apačioje. Šios bendrosios sumos rodomos tinklelio apačioje esančiame poraštės skyriuje. 

### <a name="showing-the-grid-footer"></a>Tinklelio poraštės rodymas
Yra poraščių sritis, esanti kiekvieno „Finance and Operations” programų lentelės tinklelio apačioje. Poraštėje gali būti vertingos informacijos, susijusios su duomenimis, kurie rodomi tinklelyje. Toliau pateikiami keletas šios informacijos pavyzdžių:

- Pažymėtų lentelės eilučių skaičius (kai pasirenkamas daugiau nei vienas įrašas)
- Bendrosios sumos, kurios yra sukonfigūruotų skaitinių stulpelių apačioje
- Duomenų rinkinį sudarančių eilučių skaičius 

Pagal numatytuosius parametrus ši poraštė paslėpta, tačiau gali būti lengvai įjungiama. Norėdami rodyti tinklelio poraštę, dešiniu pelės klavišu spustelėkite ant stulpelio antraštės tinklelyje ir pažymėkite parinktį **Rodyti poraštę**. Kai poraštė įjungta konkrečiame tinklelyje, šis parametras bus įsimenamas, kol vartotojas nusprendžia paslėpti poraštę, o tai galima atlikti dešiniuoju pelės klavišu spustelėjus ant stulpelio antraštės ir pažymėjus **Paslėpti poraštę**.  Atkreipkite dėmesį, kad veiksmo **Rodyti poraštę / slėpti poraštę** išdėstymo vietą būsimame naujinime numatoma pakeisti. 

### <a name="specifying-columns-with-totals"></a>Stulpelių su bendrosiomis sumomis nurodymas
Šiuo metu jokie stulpeliai nebus sukonfigūruoti taip, kad pagal numatytuosius parametrus būtų rodomos bendrosios sumos. Užuot, tai laikoma vienkartine sąrankos veikla, panašiai kaip stulpelių pločių reguliavimas tinkleliuose. Kai nurodysite, kad norite matyti stulpelio bendrąsias sumas, šis parametras bus įsimenamas, kai kitą kartą lankysitės puslapyje.  

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

Jei skaičiavimas trunka per ilgai, galite atšaukti operaciją pasirinkdami mygtuką **Atšaukti**. Tačiau kartais duomenų rinkinys per didelis, kad būtų galima apskaičiuoti bendrąsias sumas (jūsų organizacijos nustatyta riba), ir jums bus pranešta, kad labiau perfiltruotumėte duomenis.

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
Vartotojai visada galėjo eksportuoti duomenis iš „Finance and Operations” tinklelių į „Excel”, naudodami mechanizmą **Eksportuoti į „Excel“**. Tačiau galimybė įvesti duomenis anksčiau sistemos įgalina naujo tinklelio lentelių kopijavimo iš „Excel” ir jų įklijavimo tiesiai į „Finance and Operations” programų tinklelius palaikymą. Tinklelio langelis, kuriame inicijuojama įklijavimo operacija, nustato, kur pradedamas nukopijuotos lentelės įklijavimas. Tinklelio turinys perrašomas nukopijuotos lentelės turiniu, išskyrus du tolesnius atvejus.

- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, vartotojas informuojamas, kad papildomų stulpelių, pradedant nuo įklijavimo vietos, nepaisoma. 
- Jei nukopijuotoje lentelėje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje, pradedant nuo įklijavimo vietos, esami langeliai perrašomi įklijuotu turiniu, o visos papildomos nukopijuotos lentelės eilutės įterpiamos kaip naujos eilutės tinklelio apačioje. 

## <a name="evaluating-math-expressions"></a>Matematinių išraiškų vertinimas
Norėdami didinti produktyvumą vartotojai gali įvesti matematines formules tinklelyje esančiuose skaitiniuose langeliuose. Jiems nebereikia atlikti skaičiavimo programoje, esančioje ne sistemoje. Pavyzdžiui, jei įvesite **=15\*4**, o tada paspausite klavišą **TAB**, kad perkeltumėte lauką, sistema įvertins išraišką ir įrašys į lauką vertę **60**.

Norėdami, kad sistema atpažintų vertę kaip išraišką, paleiskite reikšmę su lygybės ženklu (**=**). Daugiau informacijos apie palaikomus operatorius ir sintaksę žr. [Palaikomi matematiniai simboliai](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Lentelės duomenų grupavimas
[!include [preview banner](../includes/preview-banner.md)]

Verslo vartotojams dažnai reikia atlikti ad hoc duomenų analizę. Nors tai galima atlikti eksportuojant duomenis į „Microsoft Excel“ ir naudojant suvestines lenteles, funkcija **(Peržiūra) Grupavimas tinkleliuose**, priklausanti nuo naujos tinklelio valdiklio funkcijos, vartotojams leidžia išradingai tvarkyti savo lentelių duomenis „Finance and Operations“ programose. Kadangi ši funkcija praplečia funkcijos **Bendrosios sumos** galimybes, **grupuodami** taip pat galite gauti prasmingų įžvalgų į duomenis, pateikę tarpines sumas grupėms.

Norėdami naudoti šią funkciją, dešiniuoju pelės klavišu spustelėkite stulpelį, pagal kurį norite grupuoti, ir pasirinkite **Grupuoti pagal šį stulpelį**. Šiuo veiksmu duomenys bus surūšiuoti pagal pasirinktą stulpelį, įtraukta nauja **grupė pagal stulpelį** į tinklelio pradžią ir įterptos „antraštės eilutės“ kiekvienos grupės pradžioje. Šios antraštės eilutės teikia šią informaciją apie kiekvieną grupę: 
-  Grupės duomenų reikšmė 
-  Stulpelio pavadinimas (ši informacija bus itin naudinga, kai palaikomi keli grupavimo lygiai).  
-  Šios grupės duomenų eilučių skaičius
-  Visų stulpelių, sukonfigūruotų rodyti bendrąsias sumas, tarpinės sumos

Įjungus [Įrašyti rodiniai](saved-views.md), šį grupavimą galima išsaugoti personalizuojant kaip dalį rodinio sparčiajai prieigai kitą kartą lankantis puslapyje.  

Jei kitame stulpelyje pasirinksite **Grupuoti pagal šį stulpelį**, pradinis grupavimas bus pakeistas, nes tik vienas grupavimo lygis palaikomas versijoje 10.0.9 / 33 platformos naujinime.

Norėdami anuliuoti grupavimą tinklelyje, dešiniuoju pelės klavišu spustelėkite grupavimo stulpelį ir pasirinkite **Išgrupuoti**.  

### <a name="expanding-and-collapsing-groups"></a>Grupių išplėtimas ir sutraukimas
Pradiniame duomenų grupavime bus išplėstos visos grupės. Galite kurti apibendrintus duomenų rodinius sutraukdami atskiras grupes, taip pat galite naudoti grupių išplėtimą ir sutraukimą, kad būtų lengviau naršyti duomenis. Norėdami išplėsti arba sutraukti grupę, atitinkamoje grupės antraštės eilutėje pasirinkite ševrono (>) mygtuką. Atkreipkite dėmesį, kad atskirų grupių išskleidimo / sutraukimo būsena **neįrašoma** personalizavimo parametruose.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Eilučių pažymėjimas ir žymėjimo naikinimas grupės lygyje
Lygiai taip pat, kaip galite pažymėti visas tinklelio eilutes (arba panaikinti jų žymėjimą), pažymėdami žymimąjį langelį tinklelio pirmojo stulpelio viršuje, galite greitai pažymėti visas grupės eilutes (arba panaikinti jų žymėjimą) pasirinkdami žymės langelį atitinkamoje grupės antraštės eilutėje. Grupės antraštės eilutėje esantis žymės langelis visada atspindės dabartinę tos grupės eilučių žymėjimo būseną, neatsižvelgiant į tai, ar pasirinktos visos eilutės, nepasirinkta nei viena eilutė, ar pasirinktos kelios eilutės.

### <a name="hiding-column-names"></a>Stulpelių pavadinimų slėpimas
Grupuojant duomenis numatytasis veikimas yra rodyti stulpelio pavadinimą grupės antraštės eilutėje. Pradedant nuo versijos 10.0.14 / 38 platformos naujinimo, galite pasirinkti nerodyti stulpelio pavadinimo grupės antraštės eilutėse pasirinkdami **Tinklelio parinktys** > **Slėpti grupės stulpelio pavadinimą**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kaip įjungti naują tinklelio valdiklį mano aplinkoje? 

**10.0.9 / 33 ar naujesnis platformos atnaujinimas** Funkcija **Naujas tinklelio valdiklis** yra prieinama funkcijų valdyme bet kurioje aplinkoje. Įgalinant šią funkciją, kaip ir visas kitas funkcijas, gamyboje taikoma [Papildomų naudojimo sąlygų sutartis](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / 32 platformos atnaujinimas ir 10.0.7 / 31 platformos atnaujinimas** Funkciją **Naujas tinklelio valdiklis** galima įjungti 1 pakopos (kūrėjų / testavimo) ir 2 pakopos (smėlio dėžė) aplinkoje, kad, sekant toliau nurodytus veiksmus, būtų galima atlikti papildomus bandymus ir projektavimo pakeitimus.

1.  **Įgalinti testuojamą variantą**: vykdykite šį SQL teiginį: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Iš naujo nustatykite IIS**, kad išvalytumėte statinę testuojamo varianto talpyklą. 

3.  **Raskite funkciją**: eikite į darbo sritį **Funkcijų valdymas**. Jei funkcija **Naujas tinklelio valdiklis** nerodoma visų funkcijų sąraše, pasirinkite **Tikrinti, ar yra naujinimų**.   

4.  **Įjunkite funkciją**: funkcijų sąraše raskite funkciją **Naujas tinklelio valdiklis** ir išsamios informacijos srityje pasirinkite **Įjungti dabar**. Turėkite omenyje, kad reikia atnaujinti naršyklę. 

Visi vėlesni vartotojo seansai prasidės įjungus naują tinklelio valdiklį.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Kūrėjas] Individualių puslapių pasirinkimas naudojant naują tinklelį 
Jei jūsų organizacija atranda puslapį, kuris turi tam tikrų problemų naudodama naują tinklelį, API yra prieinama tam, kad leistų individualiai formuoti naudojant ankstesnio tinklelio valdymą ir leidžiant jūsų sistemos likusiai daliai naudoti naujo tinklelio valdymą. Individualaus puslapio rodymui iš naujojo tinklelio, įtraukite tolesnius skambinimo viešinimus `super()` formos `run()` metode.

 ```this.forceLegacyGrid();```

API bus palaikoma iki 2021 m. spalio mėn. išleidimo, kai naujo tinklelio valdymas taps privalomas. Prašome pranešti visas problemas „Microsoft“, kurios reikalauja naudoti šį API. 

## <a name="known-issues"></a>Žinomos problemos
Šiame skyriuje pateikimas žinomų problemų, susijusių su nauju tinklelio valdikliu, kai funkcija yra peržiūros būsenoje, sąrašas.  

### <a name="open-issues"></a>Atviros problemos
-  Įjungus **Naujo tinklelio valdymo** funkciją, kai kurie puslapiai ir toliau naudos esamą tinklelio valdymą. Tai atsitiks esant tokiai situacijai:  
    -  Kortelės sąrašas egzistuoja puslapyje, kuris yra apdorojamas daugelyje stulpelių.
    -  Grupuotų kortelių sąrašas egzistuoja puslapyje.
    -  Tinklelio stulpelis su ne reaktyviu išplečiamu valdymu.

    Kai vartotojas pirmą kartą susiduria su viena iš šių situacijų, bus rodomas pranešimas dėl puslapio atnaujinimo. Šiai žinutei pasirodžius, puslapis ir toliau naudos esamą tinklelį visiems naudotojams iki kitos produkto naujinimo versijos. Geresnis šių scenarijų valdymas taip, kad naujas tinklelis gali būti naudojamas, bus svarstomas tolesniuose naujinimuose.     

### <a name="fixed-as-part-of-10013"></a>10.0.13 pataisymai

-  [Bug 470173] Žymimi laukeliai neaktyviose eilutėse persijungia, kai balta erdvė laukelyje paspaudžiama.
-  [Bug 474848] Pagerinta išankstinė peržiūra su nerodomais tinkleliais
-  [Bug 474851] Hipersaitai ataskaitos grupės valdikliuose neveikia 
-  [Bug 471777] Negali pasirinkti laukelių tinklelėje redagavimui ar mobilios programos sukūrimui
-  [KB 4569441] Problemos su daugelio stulpelių kortelių sąrašų sukūrimu, patarimais ant paveikslėlių ir rodymo parinktimis kai kuriuose laukeliuose
-  [KB 4575279] Ne visos pažymėtos eilutės yra pašalintos pagrindiniame žurnale
-  [KB 4575233] Rodymo parinktys nėra atkuriamos perkėlus į kitą eilutę
-  [KB 4571095] Produkto gavimo skelbimas atsitinka, kai netyčia paspaudžiamas „Enter“ klavišas (tinkamo puslapio nustatytojo veiksmo tvarkymas)
-  [KB 4575437] Paieška su redaguojamais valdikliais netikėtai užsidaro
-  [KB 4569418] Dublikuotų eilučių sukūrimas pristatymo tvarkaraščio formoje
-  [KB 4575435] Pagerinta išankstinė peržiūra kartais išlieka, net jei pelės rodyklė nėra arti laukelio
-  [KB 4575434] Paieška nefiltruoja, kai laukelis yra pakeistas
-  [KB 4575430] Slaptažodžio vertės laukeliuose nėra maskuojamos tinklelyje
-  [KB 4569438] „Apdorojimas sustojo dėl patvirtinimo problemos“ rodomas po eilučių sukūrimu nustačius tiekėjo perlaidas
-  [KB 4569434] Teisinių subjektų atnaujinimas formuoja rezultatus keliuose įrašuose
-  [KB 4575297] Fokusas ir toliau juda į užduoties įrašymo jusotą, kai redagavimo ar skirtukų sukūrimas vyksta tinklelyje
-  [KB 4566773] Koregavimo perlaidos nerodomos kaip neigiamos kupono perlaidų užklausoje 
-  [KB 4575288] Fokusas panaikina aktyvią eilutę pasirinkus liniją tarp eilučių pavyzdiniame sąraše
-  [KB 4575287] Fokusas negrįžtą į pirmą eilutę naudojant apatinę rodyklę, kuria sukuriama nauja eilutę žurnaluose
-  [KB 4564819] Negali panaikinti eilučių laisvo teksto sąskaitoje (dėl duomenų šaltinio ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Patarimai ar pagerinta išankstinė peržiūra paveikslėliams nėra rodoma

### <a name="fixed-as-part-of-10012"></a>10.0.12 pataisymai

- [KB 4558545] Lentelės valdikliai neatnaujina rodomų elementų turinio.
- [KB 4558570] Elementai vis dar rodomi puslapyje po to, kai įrašas panaikinamas.
- [KB 4558572] Stiliaus keitimas, susietas su sąrašo skydu **ExtendedStyle**, nepritaikomas.
- [KB 4558573] Tikrinimo klaidų negalima ištaisyti, kai reikalingas pakeitimas yra ne tinklelyje.
- [KB 4558584] Neigiami skaičiai nėra tinkamai atvaizduojami.
- [KB 4560726] Po to, kai sąrašas perjungiamas naudojant sąrašo rodinio valdiklį, įvyksta „netikėta kliento klaida“.
- [KB 4562141] Tinklelio indeksai yra išjungiami po to, kai įtraukiamas naujas įrašas.
- [KB 4562151] Užduočių įrašymo priemonės parinktys **Tikrinti** ir **Kopijuoti** nepasiekiamos datos / numerio valdikliams. 
- [KB 4562153] Kelių pasirinkčių žymės langeliai nerodomi sąrašo / kortelės tinkleliuose.
- [KB 4562646] Kartais negalite spustelėti ne tinklelyje, kai pasirenkate kelias eilutes tinklelyje.
- [KB 4562647] Kai nauja eilutė įtraukiama į saugos vaidmenų tinklelį, dėmesio centras iš naujo perkeliamas į pirmąjį valdiklį dialogo lange **Publikavimas**.
- [KB 4563310] Pakeitus eilutę, patobulinta peržiūra neuždaroma.
- [KB 4563313] Kai peržvalgoje pasirenkama vertė, „Internet Explorer“ įvyksta „netikėta kliento klaida“.
- [KB 4564557] Paieška ir iškrentantys meniu neatsidaro „Internet Explorer“
- [KB 4563324] Naršymas neveikia po to, kai atidaroma darbo sritis **Personalo valdymas**.

### <a name="fixed-as-part-of-10011"></a>10.0.11 pataisymai

- [Problema 432458] Tuščios arba besidubliuojančios eilutės rodomos kai kurių antrinių surinkimų pradžioje.
- [KB 4549711] Po to, kai įjungiamas naujas tinklelio valdiklis, negalima tinkamai pašalinti mokėjimo pasiūlymo eilučių.
- [KB 4558374] Įrašo, kuriam reikalingas polimorfinis parinkiklio dialogo langas, sukurti negalima.
- [KB 4558375] Naujo tinklelio stulpeliuose nerodomas žinyno tekstas.
- [KB 4558376] Sąrašo skydo tinkleliai nėra atvaizduojami tinkamame aukštyje „Internet Explorer”.
- [KB 4558377] Pasirinktinio įvedimo lauko stulpeliai, kurių plotis yra **SizeToAvailable**, kai kuriuose puslapiuose neatvaizduojami.
- [KB 4558378] Naudojant detalizavimą kartais atidaromas neteisingas įrašas.
- [KB 4558379] Kai peržvalgos atidaromos ten, kur **ReplaceOnLookup**=**Ne**, įvyksta klaida.
- [KB 4558380] Laisva vieta tinklelyje neužpildoma iškart po to, kai puslapio dalis sutraukiama.
- [KB 4558381] Neigiami skaičiai nėra tinkamai atvaizduojami / vartotojai kartais užstringa po susidūrimo su tikrinimo problemomis.
- [KB 4558382] Įvyksta netikėtos kliento klaidos.
- [KB 4558383] Po to, kai panaikinamas paskutinis įrašas, valdikliai ne tinklelyje neatnaujinami.
- [KB 4558587] Kontrolinės grupės, kuriose yra pasirinktinio įvedimo laukai, skirti pakeitimo laukams, nerodo reikšmių.
- [KB 4562143] Laukai neatnaujinami po eilutės keitimo / tinklelio apdorojimas užstringa po eilučių naikinimo.
- [KB 4562645] Jei atidaryta peržvalga, kol vykdomi nuotolinio serverio administravimo įrankių (RSAT) bandymai, įvyksta išimtis.

### <a name="fixed-as-part-of-10010"></a>10.0.10 pataisymai

- [Problema 414301] Kai sukuriamos naujos eilutės, kai kurie ankstesnių eilučių duomenys dingsta.
- [Klaida 417044] Nėra tuščio tinklelio pranešimo, skirto sąrašo stiliaus tinkleliams.
- [KB 4539058] Kai kurie tinkleliai (paprastai „FastTab”) kartais nėra atvaizduojami (bet jie atvaizduojami, jei sumažinamas vaizdo mastelis).
- [KB 4549734] Aktyvios eilutės nėra laikomos pažymėtomis, jei žymėjimo stulpelis paslėptas.
- [KB 4549796] Kai tinklelis veikia rodinio režimu, negalima redaguoti reikšmių.
- [KB 4558367] Teksto pasirinkimas nesuderinamas, kai keičiamos eilutės.
- [KB 4558368] Vienos pasirinkties scenarijuose galima pasirinkti kelias eilutes klaviatūra.
- [KB 4558369] Būsenos vaizdai dingsta hierarchiniame tinklelyje.
- [KB 4558370] Nauja eilutė nėra nuslenkama į rodinį.
- [KB 4558372] Naujas tinklelis užstringa apdorojimo metu, jei įklijuotame turinyje esančių stulpelių skaičius yra didesnis nei stulpelių, esančių tinklelyje.
- [KB 4562631] Laiko vertės nėra tinkamai suformatuotos.

### <a name="quality-update-for-1009platform-update-33"></a>Kokybinis naujinimas, skirtas 10.0.9 / platformos 33 naujinimui

- [KB 4550367] Laiko vertės nėra tinkamai suformatuotos.
