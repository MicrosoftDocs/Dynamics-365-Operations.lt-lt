---
title: Pagrindinės statistinės prognozės generavimas
description: Šioje temoje pateikiama informacija apie parametrus ir filtrus, kurie naudojami skaičiuojant poreikio prognozę.
author: roxanadiaconu
manager: tfehr
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c56d80dca9bf7753585532dffd57552ce2ee7a3f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203830"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Pagrindinės statistinės prognozės generavimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie parametrus ir filtrus, kurie naudojami skaičiuojant poreikio prognozę. 

Kuriant pagrindinę prognozę, pirmiausia reikia nurodyti skaičiuojant naudojamus parametrus ir filtrus. Pavyzdžiui, galite sukurti pagrindinę prognozę, kurioje poreikis vertinamas remiantis praėjusių metų operacijų duomenimis konkrečioje įmonėje, ateinančiam mėnesiui ir pasirinktai prekių grupei. 

Norėdami generuoti poreikio prognozę, pasirinkite **Bendrasis planavimas &gt; Prognozė &gt; Poreikio prognozė &gt; Generuoti pagrindinę statistinę prognozę**. 

Prognozės rinkinį galima pasirinkti prognozės generavimo metu. Galima naudoti šias reikšmes: Diena, Savaitė ir Mėnesis. 

Lauke **Prognozės laikotarpis** nustatomas laikotarpių, kuriems reikia skaičiuoti prognozę, skaičių. 

Kai prognozės strategija nustatyta kaip **Kopijuoti praeities poreikį**, praeities laikotarpio pabaigos nepaisoma. Rinkinių skaičių, nurodytą lauke **Prognozės laikotarpis**, sistema nukopijuoja į poreikio prognozę, pradedant nuo dalyje **Praeities laikotarpis** esančiame lauke **Pradžios data** nurodytos dienos. Kopijuodami praeities poreikį nuo tam tikros datos į priekį, gamybos planuotojai gali kito ketvirčio planą sukurti dviem būdais:

-   kopijuodami poreikį iš to paties praėjusių metų ketvirčio;
-   kopijuodami poreikį iš praėjusio ketvirčio.

Siekiant išvengti painiavos gamybos planuose, tam tikrą prognozės rinkinių skaičių galima užblokuoti. Šis skaičius nustatomas lauke **Blokavimo laiko ribos**. Puslapyje **Pakoreguota poreikio prognozė** rodomi blokuojamų rinkinių langeliai vizualiai nurodo, kad tų reikšmių keisti negalima. 

Pagrindinės poreikio prognozės pradžios data neturi būti dabartinė data arba ateities data. Norėdami nustatyti kitą pradžios datą, naudokite lauką **Pagrindinės prognozės pradžios data – pradžios data**. Pavyzdžiui, birželį vartotojai gali generuoti kitų metų prognozę. Kadangi nenurodyti praeities poreikio pabaigos ir pagrindinės prognozės pradžios prognozės rinkiniai, prognozės gali būti netikslios. Jei naudojate poreikio prognozės tarnybą, trūkstamą informaciją galite įvesti keturiais būdais. Norimą metodą galite pasirinkti puslapyje **Poreikio prognozės parametrai** nustatydami parametrą MISSING\_VALUE\_SUBSTITUTION. 

> [!NOTE]
> Trūkstamos vertės pakaitalai veikia tik duomenų spragų, esančių tarp istorinių duomenų pradžios ir pabaigos datų, atveju. Jie neužpildys duomenų prieš arba po paskutinio faktinio duomenų taško; jie veikia tik kaip ekstrapoliacija tarp faktinių esamų duomenų taškų. 

Lauko **Pagrindinės prognozės pradžios data** -  **Pradžios data** reikšmė turi būti nustatyta prognozės rinkinio pradžioje, pvz., Jungtinėse Amerikos Valstijose tai būtų sekmadienis, jei prognozės rinkinys yra savaitė. Sistema automatiškai koreguoja lauko **Pagrindinės prognozės pradžios data**  -  **Pradžios data** reikšmę, kad ji atitiktų prognozės rinkinio pradžią. 

Lauko **Pagrindinės prognozės pradžios data** -  **Pradžios data** reikšmę galima nustatyti kaip praeities datą. Kitaip tariant, galima generuoti praeities poreikio prognozę. Tai naudinga, nes vartotojai gali koreguoti prognozės tarnybos parametrus, kad anksčiau sugeneruota statistinė prognozė atitiktų faktinį praeities poreikį. Tada vartotojai gali toliau naudoti šį parametrų nustatymą, norėdami generuoti ateities pagrindinę statistinę prognozę. 

Ankstesnių poreikio prognozavimo pakartojimų koregavimus, atliktus neautomatiniu būdu, galima automatiškai taikyti naujai pagrindinei prognozei, jei pažymėtas žymės langelis **Perkelti neautomatinius koregavimus į poreikio prognozę**. Jei žymės langelis išvalytas, neautomatiniai koregavimai neįtraukiami į pagrindinę prognozę, bet nėra panaikinami. Neautomatinius prognozės koregavimus galima panaikinti tik prognozės importavimo metu, išvalant žymės langelį **Įrašyti atliktus pagrindinės poreikio prognozės neautomatinius koregavimus**. Neautomatiniai koregavimai įrašomi autorizavimo metu. Todėl jei vartotojas neautomatiškai koreguoja prognozę, tačiau neįgalioja jos „Supply Chain Management“, pakeitimai bus prarasti. Daugiau informacijos apie rankinį koregavimą ir kaip jis veikia žr. [Koreguotos prognozės įgaliojimas](authorize-adjusted-forecast.md). 

Poreikio prognozės generavimo procesas gali turėti pavadinimą ir komentarų, kad vartotojai galėtų lengviau identifikuoti sugeneruotą prognozę. Šios reikšmės yra matomos prognozės generavimo retrospektyvoje puslapyje **Pagrindinės statistinės prognozės generavimo retrospektyva**. 

Vidinės įmonės planavimo grupės, prekių paskirstymo raktų ir kitus filtrus galima taikyti prognozės generavimo metu. Juos galima naudoti našumui pagerinti arba duomenims į įvykdomas dalis padalinti. Tačiau atkreipkite dėmesį, kad poreikio prognozė nėra generuojama su vidinės įmonės planavimo grupe nesusieto prekių paskirstymo rakto nariams, net jei užklausoje prekių paskirstymo raktas yra pasirinktas. 

> [!TIP]
> Kartais vartotojai gali gauti klaidų pranešimų, kai generuojama pagrindinė poreikio prognozė arba kai prognozės generavimas baigtas be seanso žurnalo. Tai gali įvykti dėl užklausoje likusių duomenų, kurie anksčiau buvo naudoti generuojant prognozę. Norėdami išspręsti šią problemą, spustelėkite **Pasirinkti** ir atidarykite puslapį **Užklausa**, pasirinkite **Iš naujo nustatyti** ir tada iš naujo generuokite pagrindinę prognozę. 

Jei prognozė generuojama ne dideliam prekių rinkiniui, bet, pavyzdžiui, vienai prekei arba vienam prekių paskirstymo raktui vienu metu, tada, norint gauti geresnių rezultatų, galima pasirinkti žymės langelį **Naudoti užklausos atsakymo režimą**, esantį skirtuke **Bendrasis planavimas – Sąranka – Poreikio prognozė** - **Poreikio prognozės parametrai – „Azure“ mašininis mokymas**.

> [!NOTE]
> Gana lygia atrodanti prognozė gali būti dėl istorinių duomenų, kurie yra iš ilgesnio istorinio laikotarpio (mažiausiai 3 laikotarpiai, kad būtų galima išrinkti pasikartojimus, pvz., 3 metai su mėnesine prognoze). Norėdami gauti geresnį rezultatą, galite pabandyti pakeisti laiko intervalo detalumą arba didinti laiko intervalą.

<a name="additional-resources"></a>Papildomi ištekliai
--------

- [Poreikio prognozavimo nustatymas](demand-forecasting-setup.md)

- [Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)

- [Pakoreguotos prognozės įgaliojimas](authorize-adjusted-forecast.md)
