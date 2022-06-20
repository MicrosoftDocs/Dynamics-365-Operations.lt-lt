---
title: Neautomatiniai pagrindinės prognozės koregavimai
description: Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e602e6d46f928fd5376a6a6d4f94bb4a726d92b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844973"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Neautomatiniai pagrindinės prognozės koregavimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip galima neautomatiškai koreguoti pagrindinę prognozę ir peržiūrėti prognozės informaciją. 

Svarbu, kad prieš atlikdami neautomatinius koregavimus suprastumėte kelias įvairių puslapių sąvokas.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Tinklelis puslapyje Pakoreguota poreikio prognozė
Puslapyje **Pakoreguota poreikio prognozė** yra tinklelis, kurio struktūra nurodyta toliau.

-   Pirmajame stulpelyje rodoma, kam prognozė generuojama: prekių paskirstymo raktams, prekėms, įmonėms ir t.t.. Puslapio paantraštėje pateikiamas dabartinių prognozės dimensijų, rodomų tinklelyje, aprašymas. Pavyzdžiui, jei puslapio paantraštė yra **Įmonė / Teritorija / Prekių paskirstymo raktas**, o viena iš tinklelio eilučių antraščių yra **USMF / 1 / D\_Alloc**, toje eilutėje rodoma prognozė, skirta USMF įmonei, 1 teritorijai ir prekių paskirstymo raktui **D\_Alloc**.
-   Kiti stulpeliai atspindi prognozės rinkinius, kuriems prognozė generuojama. Kiekviena stulpelio antraštė yra pirmoji stulpelyje rodomo prognozės rinkinio data.
-   Langelių reikšmės nurodo to konkretaus prognozės rinkinio prognozę vienai prekei, prekių paskirstymo raktui ir t.t.

## <a name="forecast-aggregation-and-de-aggregation"></a>Prognozės telkimas ir telkimo panaikinimas
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

- Poreikio *prognozės informacijos funkcijos* prognozės modelio pasirinkimas įtraukia parametrus į informacijos apie poreikio prognozę puslapį, kuris leidžia pasirinkti įtraukti norimus prognozės **modelius**. Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, tada administratoriai gali įjungti arba išjungti šią funkciją ieškodami *prognozės*[modelio](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pasirinkimo duomenų funkcijos, kuri yra funkcijų valdymo darbo srityje.
- Patikimumo intervalas, kuris rodomas puslapio dalyje **Prognozė**, nurodo skirtumą tarp viršutinės ir apatinės patikimumo intervalo ribų. Norėdami peržiūrėti apatinės ir viršutinės ribų reikšmes, nuveskite žymeklį virš diagramos dalyje **Praeities poreikis ir prognozė grafiškai**.
- Jei naudojate poreikio prognozių „Microsoft Azure“ mašininį mokymą, galite nurodyti generuojamos prognozės patikimumo lygio procentinę dalį. Patikimumo intervalą sudaro reikšmės, kurios nurodo tinkamus poreikio prognozės įvertinimus. 95 procentų patikimumo lygio procentas nurodo 5 % tikimybę, kad prognozės rezultatas nepateks į patikimumo intervalo diapazoną.

Taip pat galite atlikti neautomatinius prognozės koregavimus puslapyje **Poreikio prognozės informacija**, pakeisdami reikšmes eilutėje **Prognozė**, kuri yra dalyje **Prognozė**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]