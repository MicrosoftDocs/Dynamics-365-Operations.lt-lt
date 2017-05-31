---
title: "Neautomatiniai pagrindinės prognozės koregavimai"
description: "Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 00e3d39d93a971dd6d4e88e322a1311eb58d7230
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Neautomatiniai pagrindinės prognozės koregavimai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją. 

Svarbu, kad prieš atlikdami neautomatinius koregavimus suprastumėte kelias įvairių puslapių sąvokas.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Tinklelis puslapyje Pakoreguota poreikio prognozė
Puslapyje **Pakoreguota poreikio prognozė** yra tinklelis, kurio struktūra nurodyta toliau.

-   Pirmajame stulpelyje rodoma, kam prognozė generuojama: prekių paskirstymo raktams, prekėms, įmonėms ir t.t.. Puslapio paantraštėje pateikiamas dabartinių prognozės dimensijų, rodomų tinklelyje, aprašymas. Pavyzdžiui, jei puslapio paantraštė yra **Įmonė / Teritorija / Prekių paskirstymo raktas**, o viena iš tinklelio eilučių antraščių yra **USMF / 1 / D\_Alloc**, toje eilutėje rodoma prognozė, skirta USMF įmonei, 1 teritorijai ir prekių paskirstymo raktui **D\_Alloc**.
-   Kiti stulpeliai atspindi prognozės rinkinius, kuriems prognozė generuojama. Kiekviena stulpelio antraštė yra pirmoji stulpelyje rodomo prognozės rinkinio data.
-   Langelių reikšmės nurodo to konkretaus prognozės rinkinio prognozę vienai prekei, prekių paskirstymo raktui ir t.t.

## <a name="forecast-aggregation-and-deaggregation"></a>Prognozės telkimas ir telkimo panaikinimas
Puslapio paantraštė nurodo prognozės telkimo lygį. 

Pavyzdžiui, jei puslapio paantraštė yra **Įmonė / Teritorija / Paskirstymo raktas / Prekės numeris / Spalva / Dydis / Konfigūracija / Stilius**, prognozės telkimo nėra ir prognozė rodoma prekės bei jos dimensijų lygyje. Norėdami keisti telkimą naudokite puslapį **Keisti prognozės dimensijas**, kurį galite atidaryti iš programų meniu. 

Norėdami modifikuoti prognozę, spustelėkite bet kurį galimą langelį ir įveskite pakoreguotą prognozės reikšmę. Pakeistas langelio reikšmė yra iš karto paryškinama siekiant nurodyti, kad rodoma prognozė nėra poreikio prognozės tarnybos sukurta prognozė, bet yra neautomatiškai pakoreguota. 

Pakeitus telkimą, kad puslapyje būtų rodoma daugiau apibendrintų duomenų, galima naudoti puslapį **Poreikio prognozės eilutės**, norint pamatyti atskiras prognozės eilutes, kurios sudaro agreguotą prognozę. 

Pvz., sugeneravote prognozę prekės lygiu, bet jūs žinote, kad dėl reklamos kampanijos arba kito panašaus įvykio šios prekės poreikis padidės visose teritorijose. Tokiu atveju puslapyje **Keisti prognozės dimensijas** galite telkimą nustatyti kaip **Įmonė / Prekių paskirstymo raktas / Prekė**. Tinklelyje **Pakoreguota poreikio prognozė** galite koreguoti visuotinę prekės prognozę visose teritorijose. Norėdami pamatyti keitimų visose teritorijose poveikį, atidarykite puslapį **Poreikio prognozės eilutės**. Šiame puslapyje matysite vieną prekės eilutę, skirtą kiekvienai teritorijai, pakoreguotam prognozės kiekiui ir pradiniam prognozės kiekiui. 

Atliekant prognozės kiekio koregavimą sudėtiniu lygiu, sistema naudoja svertinį paskirstymą koregavimams eilutėse, kurios kuria telkimą, proporcingai paskirstyti. 

Neautomatinius koregavimus taip pat galima atlikti puslapyje **Poreikio prognozės eilutės**, pakeičiant lauko **Bendras kiekis** reikšmę arba telkimo panaikinimo tinklelio dalies **Kiekis** langelius.

## <a name="viewing-details-of-the-forecast"></a>Prognozės informacijos peržiūra
Galite atidaryti puslapį **Poreikio prognozės informacija** ir peržiūrėti daugiau informacijos apie prognozę. 

Puslapyje **Poreikio prognozės informacija** toliau nurodyta informacija pateikiama lentelių ir grafiniu formatais.

-   Praeities poreikis, kuriuo prognozė pagrįsta.
-   Dabartinė prognozė, naudojama bendrajame planavime.
-   Naujos poreikio prognozės reikšmės ir jų neautomatiškai pakoreguotos sumos.
-   Prognozės reikšmių patikimumo intervalas.
-   Prognozės modelis, kuris buvo naudojamas generuojant prognozę. Jei peržiūrite apibendrintus duomenis, matysite visų metodų, naudotų per visas telkimo serijas, sąrašą.
-   Vidaus modelio tikslumas (MAPE). Daugiau informacijos apie prognozės tikslumą žr. [Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md).

**Pastabos**

-   Patikimumo intervalas, kuris rodomas puslapio dalyje **Prognozė**, nurodo skirtumą tarp viršutinės ir apatinės patikimumo intervalo ribų. Norėdami peržiūrėti apatinės ir viršutinės ribų reikšmes, nuveskite žymeklį virš diagramos dalyje **Praeities poreikis ir prognozė grafiškai**.
-   Jei naudojate „Dynamics 365 for Operations“ poreikio prognozės „Microsoft Azure“ mašininio mokymo tarnybą, galite nurodyti generuojamos prognozės patikimumo lygio procentinę dalį. Patikimumo intervalą sudaro reikšmės, kurios nurodo tinkamus poreikio prognozės įvertinimus. 95 procentų patikimumo lygio procentas nurodo 5 % tikimybę, kad prognozės rezultatas nepateks į patikimumo intervalo diapazoną.

Taip pat galite atlikti neautomatinius prognozės koregavimus puslapyje **Poreikio prognozės informacija**, pakeisdami reikšmes eilutėje **Prognozė**, kuri yra dalyje **Prognozė**.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)




