---
title: "KS skaičiavimas su standartinėmis išlaidomis"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f539e286b9f16aec3c73934403ba41f2641e6e0
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="bom-calculations-with-standard-costs"></a>KS skaičiavimas su standartinėmis išlaidomis

[!include[banner](../includes/banner.md)]




Nupirktos prekės informacija, kuri naudojama apskaičiuoti standartinės savikainos KS apima:
-   Išlaidos – nupirktos prekės išlaidos tvarkomos kaip savikainos įrašai tam tikrai teritorijai įkainojimo versijos ribose, skirtos standartinėms išlaidoms. Kiekvienas išlaidų įrašas turi efektyvumo datą, o KS apskaičiavimo data nurodo, kuris išlaidų įrašas bus naudojamas. Pavyzdžiui, KS apskaičiavimas su apskaičiavimo data ateityje gali naudoti išlaidų įrašą su laukiama būsena ir efektyvumo data ateityje.
-   Išlaidų grupė – išlaidų grupė, priskirta nupirktai prekei, suteikia pagrindą išlaidų segmentavimui apskaičiuotose pagamintos prekės išlaidose.
-   Perspėjimo sąlygos, įdėtos į prekės KS skaičiavimo grupę, suteikia KS skaičiavimui galimybę identifikuoti potencialias problemas. Taip gali būti, kai įsigytos prekės išlaidos yra lygios nuliui, prekės kiekis KS yra nulinis arba prekės išlaidų įrašas yra pasenęs. Taikomų perspėjimo sąlygų gali būti nepaisoma pradedant KS skaičiavimą.

Pagamintos prekės informacija, kuri naudojama apskaičiuoti standartinės savikainos KS apima:
-   Standartinis užsakymų kiekis atsargoms – prekės standartinis užsakymo kiekis (atsargoms) veikia kaip numatytasis apskaitos partijos dydis, skirtas amortizuoti pastovias išlaidas skaičiuojant KS. Apskaitos partijos dydis taip pat rodo kelių užsakymų kiekį, jei jis nurodytas.
-   Perspėjimo sąlygos, įdėtos į prekės KS skaičiavimo grupę, suteikia KS skaičiavimui galimybę identifikuoti potencialias problemas. Kaip pavyzdį galima nurodyti, kad pagaminta prekė neturi KS arba maršruto. Taikomų perspėjimo sąlygų gali būti nepaisoma pradedant KS skaičiavimą.

Komplektavimo specifikacijos informacija, kuri naudojama apskaičiuoti standartinės savikainos KS apima:
-   KS versija – KS versija, priskirta prie pagamintos prekės turi efektyvias pradžios ir pabaigos datas ir patvirtinimo bei aktyvumo būseną. Vekselio versija gali būti visai įmonei arba tam tikrai teritorijai ir pasirinktinai gali rodyti kiekio stabdos taškus.
-   KS eilutės prekių kiekis – sudedamasis kiekis paprastai yra kintamas, bet taip pat tai gali būti konstanta. Sudedamasis kiekis paprastai naudojamas pagaminti vieną pirminę prekę, bet jis gali būti naudojamas 100 arba 1000, kad išspręstų dešimtainio tikslumo problemas. Sudedamasis kiekis taip pat gali būti apskaičiuojamas remiantis matavimais.
-   KS eilutės prekės nurašymas – komponentas, skirtas nurašyti, gali būti kintamasis arba būti konstanta.
-   KS eilutės prekės teisingos datos – komponento pradžios ir pabaigos datos gali būti teisingos.
-   KS eilutės prekės gamybos tipas – partijos dydžio įkainojimas, skirtas amortizuoti pastovias išlaidas, parodys KS skaičiavimo kiekį ir paruoštą užsakyti išskleidimo režimą, nes KS skaičiavimas laiko, kad pagaminto komponento bus tikslus kiekis, o ne standartinis užsakymo kiekis.
-   Antrinis KS, skirtas pagamintam komponentui – pagamintas komponentas gali pasirinktinai turėti nurodytą KS versiją, kuri būtų naudojama vietoje šiuo metu aktyvios prekės KS versijos apskaičiuojant KS.
-   Antrinis maršrutas, skirtas pagamintam komponentui – pagamintas komponentas gali pasirinktinai turėti nurodytą maršruto versiją, kuri būtų naudojama vietoje šiuo metu aktyvios prekės maršruto versijos apskaičiuojant KS.
-   Operacijos numeris ir operacijos atliekų procento įtaka – operacijos numeris susieja komponentą su tam tikra operacija ir operacijos gali turėti nurašymų procentą. Sąsają leidžia KS skaičiavimams atsakyti už atliekų procentą ir kaupiamą nurašymų procentą (keliose operacijose) pagal reikiamą komponentų kiekį.
-   Nepaisyti KS eilutės prekės skaičiuojant išlaidas – komponentas gali būti ignoruojamas KS skaičiavimo tikslais.

Toliau nurodyta operacijų ištekliaus informacija, naudojama standartinių išlaidų KS apskaičiuoti.
-   Valandinės išlaidos – valandinės išlaidos, kurios siejamos su operacijų ištekliumi, išreiškiamos išlaidų kategorijomis, kurioms priskirtas nustatymo ir apdorojimo laikas. Šios išlaidų kategorijos turi būti identifikuotos išteklių grupėms ir operacijų ištekliams. Valandinės išlaidos, kurios susijusios su išlaidų kategorija gali būti konkrečios teritorijai arba taikomos visai įmonei.
-   Vieneto savikaina – kai kurios gamybos aplinkos operacijų ištekliui priskiria išeigos vieneto savikainą, kuri būtų išreiškiama kaip skirtinga išlaidų kategorija, skirta kiekiui. Pvz., su kiekiu susijusios išlaidos gali rodyti darbo dalių tarifus arba gamintojas gali priskirti operacijų ištekliaus išlaidas vienam išeigos galonui.
-   Operacijų ištekliaus informacijos nepaisymas nukreipimo operacijose – ištekliaus informacija apie išlaidų kategorijas perduodama operacijoms, kuriose jos galima nebepaisyti. KS skaičiavimai naudos išlaidų kategorijos informaciją, kuri nurodyta kelvados operacijose.
-   Išlaidų grupė, skirta išlaidų kategorijai – išlaidų grupė, priskirta išlaidų kategorijai, suteikia išlaidų segmentavimą apskaičiuotose pagamintos prekės išlaidose. Pvz., skirtingos išlaidų grupės gali būti naudojamos segmentuoti apskaičiuotas išlaidas, kurios susietos su įrenginiais ir darbu arba nustatymu ir apdorojimo laiku.

Maršruto informacija, kuri naudojama apskaičiuoti standartinės savikainos KS apima:
-   Maršruto versija – maršruto versija, priskirta prie pagamintos prekės turi efektyvias pradžios ir pabaigos datas ir patvirtinimo bei aktyvumo būseną. Maršruto versija turi būti skirta tam tikrai teritorijai ir pasirinktinai gali rodyti kiekio stabdos taškus.
-   Maršruto operacijos laikas – galima nurodyti paleidimo ir nustatymo laiką. Valandinis laikas paprastai naudojamas pagaminti vieną pirminę prekę, bet jis gali būti naudojamas 100 ar daugiau nei 1000, kad išspręstų dešimtainio tikslumo problemas.
-   Nukreipimo operacijos laikas, skirtas antriniams ištekliams – antrinių išteklių operacijos numeris tas pats, kaip ir pirminio ištekliaus, ir toks pats nukreipimo operacijos laikas. Pvz., operacijai gali reikėti įrenginio kaip pirminių išteklių, o darbo ir įrankių kaip antrinių išteklių.
-   Nukreipimo operacijos nurašymų procentas – KS skaičiavimai atsako už nurašymų procentą ir kaupiamą nurašymų procentą (keliose operacijose). Tai taikoma reikiamam nukreipimo operacijų laikui ir reikiamam su operacijų numeriais susietų komponentų kiekiui.
-   Išlaidų kategorijos nukreipimo operacija – operacijų ištekliaus informacija apie išlaidų kategorijas perduodama operacijoms, kuriose jos galima nepaisyti. KS skaičiavimai naudos išlaidų kategorijos informaciją, kuri nurodyta kelvados operacijose.

Gamybos papildomų duomenų informaciją, kuri naudojama skaičiuojant standartinės savikainos KS, sudaro:
-   Papildomas mokestis – papildomo mokesčio skaičiavimo formulė rodo vertės procentą, pvz., 100 procentų, kurie susiję su konkrečia išlaidų grupe, pvz., darbu.
-   Tarifas – tarifo skaičiavimo formulė sumą pagal vienetą, pvz., 10,00 USD per valandą, kurie susiję su konkrečia išlaidų grupe, pvz., darbu.
-   Laiku paremti papildomi duomenys palyginus su paremtais medžiagomis – gamybos papildomi duomenys gali būti susieti su kelvados operacijomis arba medžiagų komponentais.

Įkainojimo versijos informacija, kuri naudojama apskaičiuoti standartinės savikainos KS apima:
-   Kainos tipas – įkainojimo versija turi susidėti iš standartinės savikainos. KS skaičiavimams, naudojantiems standartines savikainas, taikomi keli apribojimai. Pvz., šie apribojimai nurodo, kad į vieneto savikainą turi būti įtrauktos papildomos išlaidos ir, kad KS skaičiavimo išskleidimo režimas turi būti vieno lygio.
-   Įgaliotas atsarginis principas – įkainojimo versija gali įgalioti atsarginio principo naudojimą, pvz., naudoti konkrečią įkainojimo versiją arba aktyvių išlaidų įrašus. Įgaliotas atsarginis principas paprastai taikomas įkainojimo versijai, kuri rodo atnaujinimus didėjančia tvarka dviejų versijų būdu, skirtu išlaidų atnaujinimui.
-   Blokavimo vėliavėlė, skirta laukiančioms išlaidoms – blokavimo vėliavėlė, gali apsaugoti nuo pagamintų prekių laukiančių išlaidų KS skaičiavimo.
-   Nurodyta pradžios data – nurodyta pradžios data veiks kaip numatytoji skaičiavimo data visiems KS skaičiavimams, su kuriais susijusi įkainojimo versija.
-   Nurodyta teritorija – nurodyta teritorija apribos KS skaičiavimus vienai teritorijai.
-   Įkainojimo versijos turinyje turi būti išlaidos − turinyje turi būti išlaidos. Čia pasirinktinai įtraukiamos pardavimo kainos, kad būtų apskaičiuotos pagamintoms prekėms siūlomos pardavimo kainos.

Pradedant KS skaičiavimą gali būti nurodomi keli informacijos šaltiniai. Tarp jų gali būti teritorija, skaičiavimo data ir įkainojimo versija.






