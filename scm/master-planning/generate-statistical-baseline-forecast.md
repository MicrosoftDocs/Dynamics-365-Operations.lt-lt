---
title: "Generuoti statistinę pradinis prognozė"
description: "Šiame straipsnyje pateikiama informacija apie parametrus ir filtrus, kurie naudojami skaičiuojant poreikio prognozę."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Generuoti statistinę pradinis prognozė

Šiame straipsnyje pateikiama informacija apie parametrus ir filtrus, kurie naudojami skaičiuojant poreikio prognozę. 

Kuriant pagrindinę prognozę, pirmiausia reikia nurodyti skaičiuojant naudojamus parametrus ir filtrus. Pavyzdžiui, galite sukurti pagrindinę prognozę, kurioje poreikis vertinamas remiantis praėjusių metų operacijų duomenimis konkrečioje įmonėje, ateinančiam mėnesiui ir pasirinktai prekių grupei. 

Norėdami generuoti paklausos prognozė, eikite į **kapitonas planavimo &gt;prognozės &gt;paklausos prognozavimo &gt;generuoti prognozė statistikos bazinės linijos**. 

Prognozės rinkinį galima pasirinkti prognozės generavimo metu. Galima naudoti šias reikšmes: Diena, Savaitė ir Mėnesis. 

Lauke **Prognozės laikotarpis** nustatomas laikotarpių, kuriems reikia skaičiuoti prognozę, skaičių. 

Kai prognozės strategija nustatyta kaip **Kopijuoti praeities poreikį**, praeities laikotarpio pabaigos nepaisoma. Programa kopijuoja kibirai, nurodytas skaičius į **oras horizonto** lauką Prognozuojama paklausa, pradedant nuo datos, nustatytos į **nuo dienos** lauko pagal **istorijos horizonto**. Kopijuodami praeities poreikį nuo tam tikros datos į priekį, gamybos planuotojai gali kito ketvirčio planą sukurti dviem būdais:

-   kopijuodami poreikį iš to paties praėjusių metų ketvirčio;
-   kopijuodami poreikį iš praėjusio ketvirčio.

Siekiant išvengti painiavos gamybos planuose, tam tikrą prognozės rinkinių skaičių galima užblokuoti. Šis skaičius nustatomas lauke **Blokavimo laiko ribos**. Puslapyje **Pakoreguota poreikio prognozė** rodomi blokuojamų rinkinių langeliai vizualiai nurodo, kad tų reikšmių keisti negalima. 

Pagrindinės poreikio prognozės pradžios data neturi būti dabartinė data arba ateities data. Norėdami nustatyti kitą pradžios datą, naudokite lauką **Pagrindinės prognozės pradžios data – pradžios data**. Pavyzdžiui, birželį vartotojai gali generuoti kitų metų prognozę. Kadangi nenurodyti praeities poreikio pabaigos ir pagrindinės prognozės pradžios prognozės rinkiniai, prognozės gali būti netikslios. Jei naudojate Microsoft Dynamics 365 operacijų paklausos prognozavimo tarnyba, yra keturi būdai, kuriais galite užpildyti trūkstamas spragas. Galite pasirinkti metodą, kurį norite nustatyti dėl trūkstamų\_vertė\_pakeitimo parametras su **paklausos prognozavimo parametrai** puslapis. 

Į **pradinis prognozė pradžios data** - **nuo dienos, kai** srityje turi būti nustatytas prognozės kibirą, pvz., pradžioje Jungtinėse Amerikos Valstijose, jei prognozės kibirą yra savaitės sekmadienį. Sistema automatiškai reguliuoja į **pradinis prognozė pradžios data** - **nuo dienos, kai** lauko atitikti prognozuojamas kibirą pradžios. 

Į **pradinis prognozė pradžios data** - **nuo** lauką galite nustatyti į datą – anksčiau. Kitaip tariant, galima generuoti praeities poreikio prognozę. Tai naudinga, nes vartotojai gali keisti prognozės tarnybos parametrus, kad anksčiau sugeneruota statistinė prognozė atitiktų faktinį praeities poreikį. Tada vartotojai gali toliau naudoti šį parametrų nustatymą, norėdami generuoti ateities pagrindinę statistinę prognozę. 

Ankstesnių poreikio prognozavimo pakartojimų koregavimus, atliktus neautomatiniu būdu, galima automatiškai taikyti naujai pagrindinei prognozei, jei pažymėtas žymės langelis **Perkelti neautomatinius koregavimus į poreikio prognozę**. Jei žymės langelis išvalytas, neautomatiniai koregavimai neįtraukiami į pagrindinę prognozę, bet nėra panaikinami. Neautomatinius prognozės koregavimus galima panaikinti tik prognozės importavimo metu, išvalant žymės langelį **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus**. Neautomatiniai koregavimai įrašomi autorizavimo metu. Todėl, jei vartotojas leidžia rankiniu būdu prognozei, bet ne leisti atgal į Dynamics 365 operacijų prognozę, pakeitimai bus prarasti. Daugiau informacijos apie rankiniu būdu ir kaip jie veikia rasite [leidžiantis koreguota prognozė](authorize-adjusted-forecast.md). 

Poreikio prognozės generavimo procesas gali turėti pavadinimą ir komentarų, kad vartotojai galėtų lengviau identifikuoti sugeneruotą prognozę. Šios reikšmės yra matomos prognozės generavimo retrospektyvoje puslapyje **Pagrindinės statistinės prognozės generavimo retrospektyva**. 

Vidinės įmonės planavimo grupės, prekių paskirstymo raktų ir kitus filtrus galima taikyti prognozės generavimo metu. Juos galima naudoti našumui pagerinti arba duomenims į įvykdomas dalis padalinti. Tačiau atkreipkite dėmesį, kad poreikio prognozė nėra generuojama su vidinės įmonės planavimo grupe nesusieto prekių paskirstymo rakto nariams, net jei užklausoje prekių paskirstymo raktas yra pasirinktas. 

**Patarimas**: kartais vartotojai gali gauti klaidų pranešimų, kai generuojama pagrindinė poreikio prognozė arba kai prognozės generavimas baigtas be seanso žurnalo. Tai gali įvykti dėl užklausoje likusių duomenų, kurie anksčiau buvo naudoti generuojant prognozę. Norėdami išspręsti šią problemą, spustelėkite **Pasirinkti** ir atidarykite puslapį **Užklausa**, spustelėkite **Iš naujo nustatyti** ir tada iš naujo generuokite pagrindinę prognozę. 

Jei prognozės nėra sukurtas didelis elementų rinkinys, bet, pvz., vienos prekės ar vienos prekių paskirstymo raktą vienu metu, tada norint gauti geresnių rezultatų, jūs galite pasirinkti ir **naudoti užklausą atsako režimą** žymės langelį į **kapitonas planavimo - Setup - paklausos prognozavimo** - **paklausos prognozavimo parametrai - Azure Machine Learning** tab.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)


