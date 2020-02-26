---
title: Tinklelio charakteristikos
description: Šioje temoje aprašomos kelios galingos tinklelio valdiklio funkcijos. Norint turėti prieigą prie šių charakteristikų, turi būti įjungta nauja tinklelio funkcija.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019911"
---
# <a name="grid-capabilites"></a>Tinklelio charakteristikos

[!include [banner](../includes/banner.md)]

Naujas tinklelio valdiklis suteikia daug naudingų ir galingų charakteristikų, kurias galima naudoti siekiant pagerinti vartotojo produktyvumą, kurti įdomesnius savo duomenų rodinius ir gauti prasmingų įžvalgų dėl duomenų. Šiame straipsnyje aptariamos šios charakteristikos: 

-  Skaičiuojamos sumos
-  Grupavimo duomenys
-  Rašymas anksčiau sistemos
-  Matematinių išraiškų vertinimas 

## <a name="calculating-totals"></a>Skaičiuojamos sumos
„Finance and Operations“ programose vartotojai gali matyti bendrąsias sumas, esančias tinkleliuose, skaitinių stulpelių apačioje. Šios bendrosios sumos rodomos tinklelio apačioje esančiame poraštės skyriuje. 

### <a name="showing-the-grid-footer"></a>Tinklelio poraštės rodymas
Kiekviename „Finance and Operations“ programų lentelės tinklelyje yra poraštės sritis tinklelio apačioje, kurioje gali būti rodoma vertinga informacija, susijusi su vaizduojamais duomenimis. Pateikiama tokia informacija: 
-  Pažymėtų lentelės eilučių skaičius (kai pasirenkamas daugiau nei vienas įrašas)
-  Bendrosios sumos, kurios yra sukonfigūruotų skaitinių stulpelių apačioje
-  Duomenų rinkinį sudarančių eilučių skaičius 

Pagal numatytuosius parametrus ši poraštė paslėpta, tačiau gali būti lengvai įjungiama. Norėdami rodyti tinklelio poraštę, dešiniu pelės klavišu spustelėkite ant stulpelio antraštės tinklelyje ir pažymėkite parinktį **Rodyti poraštę**. Kai poraštė įjungta konkrečiame tinklelyje, šis parametras bus įsimenamas, kol vartotojas nusprendžia paslėpti poraštę, o tai galima atlikti dešiniuoju pelės klavišu spustelėjus ant stulpelio antraštės ir pažymėjus **Paslėpti poraštę**.  Atkreipkite dėmesį, kad veiksmo **Rodyti poraštę / slėpti poraštę** išdėstymo vietą būsimame naujinime numatoma pakeisti. 

### <a name="specifying-columns-with-totals"></a>Stulpelių su bendrosiomis sumomis nurodymas
Šiuo metu jokie stulpeliai nebus sukonfigūruoti taip, kad pagal numatytuosius parametrus būtų rodomos bendrosios sumos. Užuot, tai laikoma vienkartine sąrankos veikla, panašiai kaip stulpelių pločių reguliavimas tinkleliuose. Kai nurodysite, kad norite matyti stulpelio bendrąsias sumas, šis parametras bus įsimenamas, kai kitą kartą lankysitės puslapyje.  

Yra du būdai konfigūruoti stulpelį, kad būtų rodoma bendroji suma: 
1.  Dešiniuoju pelės klavišu spustelėkite ant stulpelio, kurio bendrąją sumą norite matyti, ir pasirinkite **Skaičiuoti šio stulpelio bendrąją sumą**. Šiuo veiksmu bus atlikti trys dalykai. Pirmiausia, bus matoma poraštė. Antra, juo bus įrašyti jūsų pageidavimas matyti šiame stulpelyje bendrąją sumą. Trečia, šiuo veiksmu bus pradedamos skaičiuoti bendrosios sumos šio stulpelio ir visų kitų anksčiau sukonfigūruotų rodyti bendrąsias sumas. Laikas, kurio reikia, kad būtų galima rodyti bendrąją sumą, tiesiogiai susietas su duomenų rinkinio, kurio bendrąją sumą skaičiuojate, dydžiu.  

2.  Kai poraštė rodoma, taip pat galite spustelėti ties porašte mygtuką **Rodyti bendrąją sumą**, esantį stulpelio, kuriam norite matyti bendrąją sumą, apačioje. Jei nėra sukonfigūruotų stulpelių, tada mygtukas **Rodyti bendrąją sumą** bus matomas visiems skaitiniams stulpeliams. Kai yra bent vienas stulpelis, sukonfigūruotas bendrosioms sumoms, mygtukai **Rodyti bendrąją sumą** bus pasiekiami tik užvedus žymiklį ar suatyvinus. Šiuo veiksmu paprasčiausiai išsaugomi jūsų pageidavimai matyti bendrąją sumą šiame stulpelyje, kai vėl lankysitės šiame puslapyje, o ši būsena rodoma brūkšniu, kuris šiame stulpelyje rodomas poraštėje (arba bendroji suma bus rodoma iš karto, jei duomenų rinkinys yra pakankamai mažas).

Jei padarėte klaidą ir nebenorite daugiau matyti bendrosios sumos konkrečiame stulpelyje, dešiniuoju pelės klavišu spustelėkite ant stulpelio ir pasirinkite mygtuką **Slėpti bendrąją sumą** arba pasirinkite mygtuką **Slėpti bendrąją sumą** to stulpelio poraštėje. Šis pasirinkimas taip pat bus įrašytas kitus kartus lankantis puslapyje. 

### <a name="calculating-totals"></a>Skaičiuojamos sumos
Kai ateisite į puslapį, kuriame poraštė matoma, o stulpeliuose jau sukonfigūruotos bendrosios sumos, bendrosios sumos gali būti rodomos arba nerodomos poraštėje. Toks veikimas priklauso nuo duomenų rinkinio dydžio puslapyje. Jei duomenų rinkinys yra pakankamai mažas, bendrosios sumos bus rodomos automatiškai, kartu su duomenų rinkinio eilučių skaičiumi. Jei poraštėje yra brūkšnių po stulpeliais, kuriuos sukonfigūravote bendrosioms sumoms, tada duomenų rinkinys yra per didelis sistemai, kad būtų rodomos bendrosios sumos, ir reikia tiesioginio veiksmo bendrosioms sumoms skaičiuoti. Norėdami tai atlikti, poraštėje spustelėkite mygtuką **Skaičiuoti** arba dešiniuoju pelės klavišu spustelėkite stulpelį, kuriame norite gauti bendrąją sumą, ir pasirinkite **Skaičiuoti šio stulpelio bendrąją sumą**.  

Jei skaičiavimas trunka per ilgai, galite atšaukti operaciją pasirinkdami mygtuką **Atšaukti**. Tačiau kartais duomenų rinkinys per didelis, kad būtų galima apskaičiuoti bendrąsias sumas (jūsų organizacijos nustatyta riba), ir jums bus pranešta, kad labiau perfiltruotumėte duomenis.

Bendrosios sumos bus atnaujintos automatiškai, kai naujinate, naikinate ar kuriate duomenų rinkinyje esančias eilutes.  

## <a name="grouping-data"></a>Grupavimo duomenys
Verslo vartotojams dažnai reikia atlikti ad hoc duomenų analizę. Nors tai galima atlikti eksportuojant duomenis į „Microsoft Excel“ ir naudojant suvestines lenteles, galimybė **grupuoti** lentelės tinklelyje vartotojui naudinga išradingai tvarkant savo duomenis „Finance and Operations“ programose. Kadangi ši funkcija praplėčia funkcijos **Bendrosios sumos** galimybes, **grupuodami** taip pat galite gauti prasmingų įžvalgų į duomenis, pateikę tarpines sumas grupėms.

Norėdami naudoti šią funkciją, dešiniuoju pelės klavišu spustelėkite stulpelį, pagal kurį norite grupuoti, ir pasirinkite **Grupuoti pagal šį stulpelį**. Šiuo veiksmu duomenys bus surūšiuoti pagal pasirinktą stulpelį, pridėta nauja grupė pagal stulpelį prie tinklelio pradžios ir įterptos „antraštės eilutės“ kiekvienos grupės pradžioje. Šios antraštės eilutės teikia šią informaciją apie kiekvieną grupę: 
-  Grupės duomenų reikšmė 
-  Stulpelio žyma. Tai bus ypač naudinga, kai palaikomi keli grupavimo lygiai.  
-  Šios grupės duomenų eilučių skaičius
-  Visų stulpelių, sukonfigūruotų rodyti bendrąsias sumas, tarpinės sumos

Įjungus [Įrašyti rodiniai](saved-views.md), šį grupavimą galima išsaugoti personalizuojant kaip dalį rodinio sparčiajai prieigai kitą kartą lankantis puslapyje.  

Jei pasirinksite **Grupuoti pagal šį stulpelį** kitame stulpelyje, pradinis grupavimas bus pakeistas, nes tik dalis grupavimo palaikoma 10.0.9 / 33 platformos naujinime.

Norėdami anuliuoti grupavimą tinklelyje, dešiniuoju pelės klavišu spustelėkite grupavimo stulpelį ir pasirinkite **Išgrupuoti**.  


## <a name="evaluating-math-expressions"></a>Matematinių išraiškų vertinimas
Gerindamas savo produktyvumą vartotojas gali įvesti matematines formules į skaitinius langelius tinklelyje, užuot skaičiuodamas programoje, esančioje už sistemos ribų. Pavyzdžiui, galite įvesti **=15\*4** ir išeiti iš lauko. Sistema įvertins išraišką ir lauke įrašys vertę „60“.

Norėdami, kad sistema atpažintų vertę kaip išraišką, paleiskite reikšmę su lygybės ženklu (**=**). Norėdami gauti daugiau informacijos apie palaikomus operatorius ir sintaksę, žr. [Palaikomi matematiniai simboliai](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
