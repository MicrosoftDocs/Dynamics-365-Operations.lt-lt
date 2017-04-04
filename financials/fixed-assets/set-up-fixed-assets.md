---
title: "Nustatyti ilgalaikį turtą"
description: "Šioje temoje pateikta Ilgalaikio turto modulio nustatymo peržiūra."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: dde8053df96d03c8c8e52fa6d2fdf7f74e95ec92
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fixed-assets"></a>Nustatyti ilgalaikį turtą

Šioje temoje pateikta Ilgalaikio turto modulio nustatymo peržiūra.

<a name="overview"></a>Apžvalga
--------
Parametrai valdo bendrą ilgalaikio turto modulio elgseną.

Naudojant ilgalaikio turto grupę galima sugrupuoti turtą ir nurodyti kiekvieno grupei priskirto turto numatytuosius atributus. Knygos priskiriamos ilgalaikio turto grupėmis. Knygose sekama ilgalaikio turto finansinė vertė per tam tikrą laiką naudojant nurodytą nusidėvėjimo šablono nusidėvėjimo konfigūraciją.

Ilgalaikis turtas priskiriamas grupei, kai jis sukuriamas. Tada pagal numatytuosius parametrus ilgalaikio turto grupei priskirtos knygos yra priskiriamos ilgalaikiam turtui. Knygos, kurios sukonfigūruotos būti registruojamos DK, yra susiejamos su registravimo šablonu. DK sąskaitos nurodomos kiekvienai knygai registravimo profilyje ir jos yra naudojamos registruojant ilgalaikio turto operacijas. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Nusidėvėjimo šablonai
Pirmiausia reikėtų nustatyti nusidėvėjimo šablonus. Nusidėvėjimo šablone galite konfigūruoti, kaip turto vertė nusidėvi per tam tikrą laiką. Jums reikės nurodyti nusidėvėjimo būdą, nusidėvėjimo metus (kalendoriniai metai arba finansiniai metai) ir nusidėvėjimo dažnį.

## <a name="books"></a>Knygos
Nustatę nusidėvėjimo šablonus, turite sukurti reikiamas turto knygas. Kiekvienoje knygoje sekamas atskiras turto finansinis ciklas. Knygas galima konfigūruoti, kad susietos operacijos būtų registruojamos DK. Ši konfigūracija yra pagal nutylėjimą, nes ji yra paprastai naudojamas įmonės finansinė atskaitomybė. Knygas, kurios nereikia registruoti į DK skelbti tik ilgalaikio turto subledger ir paprastai naudojami mokesčių ataskaitas.

Kiekvienai knygai priskiriamas pirminis nusidėvėjimo šablonas. Jei galima, knygoms taip pat gali būti priskiriamas alternatyvus arba perjungimo nusidėvėjimo šablonas. Norėdami automatiškai įtraukti ilgalaikio turto knygą į nusidėvėjimą, turite įjungti parinktį Skaičiuoti nusidėvėjimą. Jei ši pasirinktis nepasirinkta turto, nusidėvėjimo pasiūlymą praleidžia turto.

Taip pat galite nustatyti išvestinės knygas. Nurodytos išvestinės operacijos bus užregistruotos kaip pirminės operacijos pagal išvestines knygas. Todėl paprastai nustatomos ne nusidėvėjimo operacijų, o įsigijimų ir perleidimų išvestinės operacijos.

## <a name="fixed-asset-posting-profiles"></a>Ilgalaikio turto registravimo šablonai
Nustatę knygas, galite kurti registravimo šabloną. Registravimo šablonas turi būti nurodytas kiekvienai knygai, bet jį galima nurodyti ir išsamesniu lygiu. Pvz., galite nurodyti knygos ir ilgalaikio turto grupės derinio ar net atskiros ilgalaikio turto knygos registravimo šabloną. Pagal numatytuosius parametrus nurodytos DK sąskaitos taikomos ilgalaikio turto operacijoms.

Turite nurodyti DK sąskaitas, kurios naudojamos atliekant likvidavimo procesus, tiek likvidavimo pardavimus, tiek likvidavimo nurašymus. Likvidavimo metu anksčiau užregistruotos ilgalaikio turto operacijos bus atšauktos iš pradinių sąskaitų, o grynoji suma bus perkelta į atitinkamą turto likvidavimo pelno ir nuostolio sąskaitą. Reikia nustatyti kiekvieno versle naudojamo operacijos tipo sąskaitas, kad būtų galima tinkamai atšaukti operacijas. Pagrindinė sąskaita turėtų būti pradinė sąskaita, kurią nustatėte to operacijos tipo registravimo šablone, o korespondentinė sąskaita turi būti jūsų likvidavimo sąskaitos pelnas ir nuostolis. Išimtis yra balansinė vertė. Šiuo atveju pagrindinė ir korespondentinė sąskaitos turi būti nustatytos likvidavimo sąskaitos pelnui ir nuostoliui.

## <a name="fixed-asset-groups"></a>Ilgalaikio turto grupės
Ilgalaikio turto grupė yra vienintelis būtinas laukas, kai kuriate ilgalaikį turtą. Šio lauko reikšmė nurodo kelis informacinius turto laukų numatytąją reikšmę. Knygos nustatomos taip, kad numatytoji knyga būtų priskiriama kiekvienam grupės turtui. Tada galėsite nustatyti konkrečios turto grupės knygų atributus, pvz., atributus Dėvėjimo laikas ir Nusidėvėjimo konvencija.

Taip pat galite nurodyti konkretaus ilgalaikio turto grupės ir knygos derinio specialiąsias nusidėvėjimo nuolaidas (arba papildomą nusidėvėjimą). Specialiajai nusidėvėjimo nuolaidai turi būti taikomas prioritetas, kad būtų nurodoma tvarka, kuria būtų galima apskaičiuoti nuolaidas, kai prie nusidėvėjimo knygos priskirtos kelios nuolaidos.

## <a name="fixed-asset-parameters"></a>Ilgalaikio turto parametrai
Paskutinis veiksmas yra atnaujinti ilgalaikio turto parametrus.

Laukas Kapitalizacijos ribinė vertė nurodo, koks turtas nusidėvėjo. Jei pirkimo eilutėje yra pažymėtas kaip ilgalaikį turtą, bet jis neatitinka nurodyto kapitalizacijos ribinė vertė, ilgalaikis turtas vis dar kuriama arba atnaujinama, bet skaičiuoti nusidėvėjimo pasirinktis bus nustatyta į Nr. Todėl turtas nebus automatiškai nusidėvėti kaip nusidėvėjimo pasiūlymams.

Svarbi parinktis yra Automatiškai kurti nusidėvėjimo koregavimo sumas su likvidavimu. Kai nustatote šią parinktį į Taip, turto nusidėvėjimas automatiškai koreguojamas pagal turto likvidavimo metu galiojančius nusidėvėjimo nustatymus. Taip pat yra galimybė įsigyjant ilgalaikį turtą naudojant tiekėjo SF iš jūsų įsigijimo sumos atskaityti mokėjimo nuolaidas.

„FastTab“ Pirkimo užsakymai galite konfigūruoti, kaip norite, kad būtų sukurtas jūsų turtas kaip pirkimo proceso dalis. Pirmoji parinktis yra Leisti turto įsigijimą iš pirkimo. Jei šią parinktį nustatote į Taip, turto įsigijimas vykdomas, kai užregistruojama SF. Jei nustatote šią pasirinktį kaip ne, jūs vis dar galite įdėti ilgalaikio turto pirkimo užsakymo (PU) ir SF, bet nebus registruojamas įsigijimo. Registravimą reikės atlikti kaip atskirą ilgalaikio turto žurnalo veiksmą. Kurti turto važtaraštis arba SF registravimo parinktis leidžia sukurti naują turtą "ant skristi" registruojant, taip, kad ji nebūtinai turi būti nustatyta kaip ilgalaikio turto, iki sandorio. Paskutinė pasirinktis Tikrinti, ar įvedant eilutę kuriamas ilgalaikis turtas taikoma tik pirkimo paraiškoms.

Priežasčių kodus galima konfigūruoti taip, kad jų reikėtų keičiant ilgalaikį turtą arba atliekant konkrečias ilgalaikio turto operacijas.

Galiausiai skirtuke Numeracijos galite nurodyti ilgalaikio turto numeracijas. Ilgalaikio turto numeraciją galima perrašyti, jeigu nurodyta ilgalaikio turto grupės numeracija.


