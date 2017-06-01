---
title: "Registravimo aprašai"
description: "Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti. Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e1865a695a89ed0501f97189b542b3915a96bf08
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="posting-definitions"></a>Registravimo aprašai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti. Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose.

Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose. Galite peržiūrėti palaikomus dokumentus ir registravimo tipus puslapyje **Operacijų registravimo aprašai**. 

Norėdami pradėti naudoti registravimo aprašus, pasirinkite parinktį**Naudoti registravimo aprašus** puslapyje **DK parametrai**. Net kai naudojate registravimo aprašus, turite dar nustatyti pradinių įrašų ir nepalaikomų registravimo tipų bei dokumentų registravimo šablonus. 

Naudokite registravimo aprašus norėdami įjungti pirkimo užsakymų biudžeto rezervavimo apskaitą ir pirkimo paraiškų preliminaraus biudžeto rezervavimo apskaitą.

## <a name="defining-posting-definitions"></a>Registravimo aprašų apibrėžimas
Naudokite puslapį**Registravimo aprašai**, kad nurodytumėte gretinimo kriterijus ir apibrėžtumėte įrašus, kurie turėtų būti sugeneruoti įvykus sugretinimui. Pradinių įrašų gretinimo kriterijai įvertinami kaip apskaitos paskirstymai. 

Puslapyje **Registravimo aprašai** taip pat galite priskirti prioriteto numerius įrašų eilutėms, taip kontroliuodami eilučių įvertinimo tvarką. Pirma įvertinamos eilutės, kurių prioriteto numeris mažiausias. Pvz., įvertinamos visos eilutės, kurių prioritetas yra 1, tada eilutės, kurių prioritetas yra 2 ir t. t. Radus atitikmenį kiti gretinimo kriterijai ignoruojami. Be to, sugeneruotus įrašus kuria tik pradinę operaciją atitinkančioje grupėje esantys kriterijai. 

Savo registravimo aprašus galite patikrinti naudodami vedlį **Tikrinti registravimo aprašą**. Nurodę registravimo aprašo pradinio įrašo pavyzdį, pamatysite sugeneruotus įrašus. 

Galite naudoti registravimo aprašų versijas kartu su įsigaliojimo datomis. Pvz., galite sukurti būsimą registravimo aprašo versiją, kad užregistruotumėte kitą DK sąskaitą į naujus finansinius metus. 

Naudokite puslapį **Operacijų registravimo aprašai**, kad priskirtumėte registravimo aprašus operacijų tipams.

## <a name="linking-posting-definitions"></a>Registravimo aprašų susiejimas
Kai kuriate registravimo aprašus, galite susieti vieną registravimo aprašą su kitu. Tada, be dabartinio registravimo aprašo kriterijų, atsižvelgiama ir į jūsų susieto aprašo kriterijus. Ši funkcija padeda sutaupyti laiko, nes nereikės iš naujo įvesti dabartinio registravimo aprašo kriterijų „FastTab“ **Įrašai** puslapyje **Registravimo aprašai**, jei šias eilutes jau įvedėte kitam aprašui. 

Į diagramas arba lenteles įtraukite visus saitus, kuriuos galite naudoti. Norėdami išvengti konfliktų su dabartiniu registravimo aprašu, įsitikinkite, kad visuose registravimo aprašuose esančios eilutės yra unikalios. 

Kuriant saitus registravimo aprašuose taikomi šie apribojimai:

-   Registravimo aprašas gali būti susietas su kitu registravimo aprašu arba kitas registravimo aprašas gali būti susietas su pirmuoju, bet ne abu vienu metu. Tačiau vieną registravimo aprašą galima susieti su keliais registravimo aprašais.
-   Galite nustatyti saitus tik tarp tarp tame pačiame modulyje esančių registravimo aprašų.
-   Galite priskirti registravimo aprašą bet kokiam operacijos tipui, bet operacijos tipas turi būti tame pačiame modulyje kaip ir registravimo aprašas. Naudokite puslapį **Operacijų registravimo aprašai** norėdami pamatyti, kuriame modulyje yra operacijos tipas.


Daugiau informacijos ieškokite [Registravimo aprašų pavyzdžiai](example-posting-definitions.md). 



