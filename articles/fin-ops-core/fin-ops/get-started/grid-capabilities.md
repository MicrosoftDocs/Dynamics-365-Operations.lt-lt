---
title: Tinklelio charakteristikos
description: Šioje temoje aprašomos kelios galingos tinklelio valdiklio funkcijos. Norint turėti prieigą prie šių charakteristikų, turi būti įjungta nauja tinklelio funkcija.
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
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
ms.openlocfilehash: 0fd0e15ea88e9f5f34d8dff82606a8d26616a16d
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260465"
---
# <a name="grid-capabilities"></a>Tinklelio charakteristikos

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Naujas tinklelio valdiklis suteikia daug naudingų ir galingų charakteristikų, kurias galima naudoti siekiant pagerinti vartotojo produktyvumą, kurti įdomesnius savo duomenų rodinius ir gauti prasmingų įžvalgų dėl duomenų. Šiame straipsnyje aptariamos šios charakteristikos: 

-  Skaičiuojamos sumos
-  Grupavimo duomenys
-  Rašymas anksčiau sistemos
-  Matematinių išraiškų vertinimas 

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

## <a name="grouping-data"></a>Grupavimo duomenys
Verslo vartotojams dažnai reikia atlikti ad hoc duomenų analizę. Nors tai galima atlikti eksportuojant duomenis į „Microsoft Excel“ ir naudojant suvestines lenteles, galimybė **grupuoti** lentelės tinklelyje vartotojui naudinga išradingai tvarkant savo duomenis „Finance and Operations“ programose. Kadangi ši funkcija praplėčia funkcijos **Bendrosios sumos** galimybes, **grupuodami** taip pat galite gauti prasmingų įžvalgų į duomenis, pateikę tarpines sumas grupėms.

Norėdami naudoti šią funkciją, dešiniuoju pelės klavišu spustelėkite stulpelį, pagal kurį norite grupuoti, ir pasirinkite **Grupuoti pagal šį stulpelį**. Šiuo veiksmu duomenys bus surūšiuoti pagal pasirinktą stulpelį, pridėta nauja grupė pagal stulpelį prie tinklelio pradžios ir įterptos „antraštės eilutės“ kiekvienos grupės pradžioje. Šios antraštės eilutės teikia šią informaciją apie kiekvieną grupę: 
-  Grupės duomenų reikšmė 
-  Stulpelio žyma (ši informacija bus itin naudinga, kai palaikomi keli grupavimo lygiai).
-  Šios grupės duomenų eilučių skaičius
-  Visų stulpelių, sukonfigūruotų rodyti bendrąsias sumas, tarpinės sumos

Įjungus [Įrašyti rodiniai](saved-views.md), šį grupavimą galima išsaugoti personalizuojant kaip dalį rodinio sparčiajai prieigai kitą kartą lankantis puslapyje.  

Jei kitame stulpelyje pasirinksite **Grupuoti pagal šį stulpelį**, pradinis grupavimas bus pakeistas, nes tik vienas grupavimo lygis palaikomas versijoje 10.0.9 su 33 platformos naujinimu.

Norėdami anuliuoti grupavimą tinklelyje, dešiniuoju pelės klavišu spustelėkite grupavimo stulpelį ir pasirinkite **Išgrupuoti**.  


## <a name="evaluating-math-expressions"></a>Matematinių išraiškų vertinimas
Norėdami didinti produktyvumą vartotojai gali įvesti matematines formules tinklelyje esančiuose skaitiniuose langeliuose. Jiems nebereikia atlikti skaičiavimo programoje, esančioje ne sistemoje. Pavyzdžiui, jei įvesite **=15\*4**, o tada paspausite klavišą **TAB**, kad perkeltumėte lauką, sistema įvertins išraišką ir įrašys į lauką vertę **60**.

Norėdami, kad sistema atpažintų vertę kaip išraišką, paleiskite reikšmę su lygybės ženklu (**=**). Daugiau informacijos apie palaikomus operatorius ir sintaksę žr. [Palaikomi matematiniai simboliai](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

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
