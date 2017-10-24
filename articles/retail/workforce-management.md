---
title: "Paslaugos Darbo jėgos valdymas apžvalga"
description: "Šioje temoje aprašoma, kaip, naudodami paslaugą Darbo jėgos valdymas (WFM), galite pasinaudoti pažįstamais elektroninio kasos aparato (EKA) klientais, moderniuoju EKA ir debesies EKA, kad parduotuvių vadovai galėtų lengvai valdyti savo darbo jėgą."
author: shalabhjainmsft
manager: AnnBe
ms.date: 7/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-07-30
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: f747dce6b9595de50297cb5af7db523d5f26a844
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="workforce-management-overview"></a>Paslaugos Darbo jėgos valdymas apžvalga

[!include[banner](includes/banner.md)]
    
Paslauga Darbo jėgos valdymas (WFM) naudojasi pažįstamais elektroninio kasos aparato (EKA) klientais, moderniuoju EKA ir debesies EKA, kad parduotuvių vadovai galėtų lengvai valdyti savo darbo jėgą. WFM paslauga naudodama plėtinių sistemą į EKA atsiunčia reikiamus paketus. Šie paketai atsisiunčiami, kai EKA uždaromas ir vėl atidaromas. Todėl, kai „Microsoft“ išleidžia naujų WFM funkcijų, EKA programą reikia uždaryti ir vėl atidaryti.

Naudodami šią paslaugą, parduotuvių vadovai gali lengvai kurti ir publikuoti savaitinį parduotuvių darbo grafiką. Tada parduotuvių darbuotojai gali greitai peržiūrėti savo ir kolegų grafikus. Taip jie gali sužinoti, kas su jais dirbs priskirtose pamainose. Parduotuvės darbuotojai taip pat gali kurti leidimo neatvykti, pamainų sukeitimo ir pamainų siūlymo prašymus. Visi šie prašymai suaktyvina apibrėžtą darbo eigą.

Dirbdami pamainoje parduotuvės darbuotojai gali pasinaudoti registracijos atėjus į darbą ir jį baigus funkcija, kuri yra integruota į EKA klientus. Duomenys tada siunčiami į būstinę (HQ), kur pagal juos apdorojami atlyginimai. Registracijos atėjus į darbą ir darbą baigus funkcija yra esamas EKA pajėgumas. Norėdami gauti daugiau informacijos apie jos sąranką ir palaikomas situacijas, žr. [Registracija atėjus į darbą ir darbą baigus](retail-time-attendance.md).

## <a name="supported-scenarios"></a>Palaikomi scenarijai
Šiame skyriuje pateikiama daugiau informacijos apie palaikomas situacijas.

- **Kurti ir publikuoti grafikus** – WFM paslauga naudodama EKA teises, sukonfigūruotas būstinėje, nustato, ar darbuotojas turi parduotuvės vadovo teises. Kurti ir publikuoti grafikus naudojant operaciją Grafikų valdymas gali tik parduotuvių vadovai. Jie gali greitai sukurti grafiką, esamą darbo pamainą nukopijuodami ir iš vieno darbuotojo įklijuodami kitam darbuotojui. Grafiką jie taip pat gali kurti jį importuodami iš bet kurios ankstesnės savaitės į dabartinę savaitę.

    Jei grafikas nėra publikuotas, jis yra juodraščio būsenos ir atrodo kitaip nei publikuotas grafikas. Bet kurios savaitės grafiką parduotuvių vadovai gali publikuoti spustelėdami mygtuką **Publikuoti**. Publikavus savaitės grafiką, automatiškai publikuojami visi pakeitimai. Pakeitimų pavyzdžiai: darbo pamainų ar neatvykimų įtraukimas, naikinimas arba redagavimas. Parduotuvių darbuotojai gali peržiūrėti tik publikuotus įvairių savaičių grafikus.
    
- **Kurti ir tvirtinti prašymus** – parduotuvių darbuotojai gali kurti trijų tipų prašymus, nurodytus toliau.

    - Prašymas leisti neatvykti
    - Prašymas sukeisti pamainas
    - Prašymas pasiūlyti pamainą

    Šiuos prašymus galima kurti naudojant operaciją Grafikų prašymai. Kiekvienam prašymui taikoma apibrėžta darbo eiga ir darbuotojai gali lengvai matyti dabartinę savo prašymų būseną.
    
    Prašymai leisti neatvykti automatiškai siunčiami parduotuvės vadovui tvirtinti. Jei yra keli parduotuvės vadovai, konkretų prašymą gali peržiūrėti visi vadovai, tačiau jį patvirtinti ar atmesti gali tik vienas vadovas. Neatvykimo tipai konfigūruojami mažmeninės prekybos būstinėje, naudojant modulio **Mažmeninė prekyba** puslapį **Atostogų ir neatvykimų tipai**. Parduotuvės vadovui patvirtinus arba atmetus prašymą, jis perkeliamas į operacijos Grafikų prašymai skirtuką **Istorija**.
    
    Pamainų sukeitimo ar pamainos siūlymo prašymas pirmiausia įteikiamas darbuotojui, kuriam prašymas buvo išsiųstas. Parduotuvės vadovas peržiūrėti prašymą gali tik tada, kai jį patvirtina šis darbuotojas. Todėl, jei darbuotojas pamainų sukeitimo ar pamainos siūlymo prašymą atmeta, vadovas jo peržiūrėti negali. Prašymą sukūręs darbuotojas taip pat gali prašymą atšaukti prieš vadovui jį patvirtinant arba atmetant.

- **Rodyti aktyvius parduotuvės darbuotojus grafiko rodinyje** – kai darbuotojas įtraukiamas į parduotuvę, pavyzdžiui, jį susiejant su parduotuvės darbuotojų adresų knygele, darbuotojui galima planuoti grafikus naudojant WFM paslaugą. Būstinėje vykdoma pasikartojanti paketinė užduotis pavadinimu **Apdoroti darbuotojų duomenis, kad būtų galima valdyti darbo jėgą**. Ši užduotis paruošia parduotuvės darbuotojų susiejimus, kurie bus siunčiami į „Common Data Service“ (CD).

    Tas pats procesas naudojamas, kai darbuotojas pašalinamas iš parduotuvės. Tačiau, jei pašalintam darbuotojui priskirta aktyvi darbo pamaina ar neatvykimas, jis vis dar rodomas praėjusių, dabartinės ir būsimų savaičių grafikuose. Todėl, jei šios darbo pamainos ir šie neatvykimai nepanaikinami, pašalintas darbuotojas toliau bus rodomas šių savaičių grafikuose.

