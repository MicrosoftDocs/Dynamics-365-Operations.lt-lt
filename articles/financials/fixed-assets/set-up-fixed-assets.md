---
title: Ilgalaikio turto nustatymas
description: "Šioje temoje pateikta Ilgalaikio turto modulio nustatymo peržiūra."
author: twheeloc
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d16c9ca5740c27528d74800957f9b47984c135cd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fixed-assets"></a>Ilgalaikio turto nustatymas

[!include[banner](../includes/banner.md)]


Šioje temoje pateikta Ilgalaikio turto modulio nustatymo peržiūra.

<a name="overview"></a>Apžvalga
--------
Parametrai valdo bendrą ilgalaikio turto modulio elgseną.

Naudojant ilgalaikio turto grupę galima sugrupuoti turtą ir nurodyti kiekvieno grupei priskirto turto numatytuosius atributus. Knygos priskiriamos ilgalaikio turto grupėmis. Knygose sekama ilgalaikio turto finansinė vertė per tam tikrą laiką naudojant nurodytą nusidėvėjimo šablono nusidėvėjimo konfigūraciją.

Ilgalaikis turtas priskiriamas grupei, kai jis sukuriamas. Tada pagal numatytuosius parametrus ilgalaikio turto grupei priskirtos knygos yra priskiriamos ilgalaikiam turtui. Knygos, kurios sukonfigūruotos būti registruojamos DK, yra susiejamos su registravimo šablonu. DK sąskaitos nurodomos kiekvienai knygai registravimo profilyje ir jos yra naudojamos registruojant ilgalaikio turto operacijas. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Nusidėvėjimo šablonai
Pirmiausia reikėtų nustatyti nusidėvėjimo šablonus. Nusidėvėjimo šablone galite konfigūruoti, kaip turto vertė nusidėvi per tam tikrą laiką. Jums reikės nurodyti nusidėvėjimo būdą, nusidėvėjimo metus (kalendoriniai metai arba finansiniai metai) ir nusidėvėjimo dažnį. Daugiau informacijos žr. [Nustatyti ir kurti nusidėvėjimo profilius](tasks/set-up-depreciation-profiles.md)

## <a name="books"></a>Knygos
Nustatę nusidėvėjimo šablonus, turite sukurti reikiamas turto knygas. Kiekvienoje knygoje sekamas atskiras turto finansinis ciklas. Knygas galima konfigūruoti, kad susietos operacijos būtų registruojamos DK. Ši konfigūracija yra numatytasis parametras, nes ji paprastai naudojama įmonės finansinėse ataskaitose. Knygos, kurios neregistruojamos DK, gali būti registruojamos tik papildomoje ilgalaikio turto knygoje ir jos paprastai naudojamos mokesčių ataskaitų tikslais.

Kiekvienai knygai priskiriamas pirminis nusidėvėjimo šablonas. Jei galima, knygoms taip pat gali būti priskiriamas alternatyvus arba perjungimo nusidėvėjimo šablonas. Norėdami automatiškai įtraukti ilgalaikio turto knygą į nusidėvėjimą, turite įjungti parinktį Skaičiuoti nusidėvėjimą. Jei ši turto parinktis nepasirinkta, nusidėvėjimo pasiūlyme turtas praleidžiamas.

Taip pat galite nustatyti išvestinės knygas. Nurodytos išvestinės operacijos bus užregistruotos kaip pirminės operacijos pagal išvestines knygas. Todėl paprastai nustatomos ne nusidėvėjimo operacijų, o įsigijimų ir perleidimų išvestinės operacijos.
Daugiau informacijos žr. [NUstatyti knygas](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Ilgalaikio turto registravimo šablonai
Nustatę knygas, galite kurti registravimo šabloną. Registravimo šablonas turi būti nurodytas kiekvienai knygai, bet jį galima nurodyti ir išsamesniu lygiu. Pvz., galite nurodyti knygos ir ilgalaikio turto grupės derinio ar net atskiros ilgalaikio turto knygos registravimo šabloną. Pagal numatytuosius parametrus nurodytos DK sąskaitos taikomos ilgalaikio turto operacijoms.

Turite nurodyti DK sąskaitas, kurios naudojamos atliekant likvidavimo procesus, tiek likvidavimo pardavimus, tiek likvidavimo nurašymus. Likvidavimo metu anksčiau užregistruotos ilgalaikio turto operacijos bus atšauktos iš pradinių sąskaitų, o grynoji suma bus perkelta į atitinkamą turto likvidavimo pelno ir nuostolio sąskaitą. Reikia nustatyti kiekvieno versle naudojamo operacijos tipo sąskaitas, kad būtų galima tinkamai atšaukti operacijas. Pagrindinė sąskaita turėtų būti pradinė sąskaita, kurią nustatėte to operacijos tipo registravimo šablone, o korespondentinė sąskaita turi būti jūsų likvidavimo sąskaitos pelnas ir nuostolis. Išimtis yra balansinė vertė. Šiuo atveju pagrindinė ir korespondentinė sąskaitos turi būti nustatytos likvidavimo sąskaitos pelnui ir nuostoliui. Daugiau informacijos žr. [Nustatyti ilgalaikio turto registravimo profilius](tasks/set-up-fixed-asset-posting-profiles.md)

## <a name="fixed-asset-groups"></a>Ilgalaikio turto grupės
Ilgalaikio turto grupė yra vienintelis būtinas laukas, kai kuriate ilgalaikį turtą. Šio lauko reikšmė nurodo kelis informacinius turto laukų numatytąją reikšmę. Knygos nustatomos taip, kad numatytoji knyga būtų priskiriama kiekvienam grupės turtui. Tada galėsite nustatyti konkrečios turto grupės knygų atributus, pvz., atributus Dėvėjimo laikas ir Nusidėvėjimo konvencija.

Taip pat galite nurodyti konkretaus ilgalaikio turto grupės ir knygos derinio specialiąsias nusidėvėjimo nuolaidas (arba papildomą nusidėvėjimą). Specialiajai nusidėvėjimo nuolaidai turi būti taikomas prioritetas, kad būtų nurodoma tvarka, kuria būtų galima apskaičiuoti nuolaidas, kai prie nusidėvėjimo knygos priskirtos kelios nuolaidos. Daugiau informacijos žr. [Nustatyti ilgalaikio turto grupes](tasks/set-up-fixed-asset-groups.md)

## <a name="fixed-asset-parameters"></a>Ilgalaikio turto parametrai
Paskutinis veiksmas yra atnaujinti ilgalaikio turto parametrus.

Laukas **Kapitalizacijos ribinė vertė** nurodo, koks turtas nusidėvėjo. Jei pirkimo eilutė pasirenkama kaip ilgalaikis turtas, bet ji neatitinka nurodytos kapitalizacijos ribinės vertės, ilgalaikis turtas vis tiek sukuriamas arba atnaujinamas, bet parinktis Skaičiuoti nusidėvėjimą nustatoma į Ne. Todėl turtas nebus nusidėvėjęs automatiškai kaip nusidėvėjimo pasiūlymų dalis.

Svarbi parinktis yra **Automatiškai kurti nusidėvėjimo koregavimo sumas su likvidavimu**. Kai nustatote šią parinktį į **Taip**, turto nusidėvėjimas automatiškai koreguojamas pagal turto likvidavimo metu galiojančius nusidėvėjimo nustatymus. Taip pat yra galimybė įsigyjant ilgalaikį turtą naudojant tiekėjo SF iš jūsų įsigijimo sumos atskaityti mokėjimo nuolaidas.

„FastTab“ Pirkimo užsakymai galite konfigūruoti, kaip norite, kad būtų sukurtas jūsų turtas kaip pirkimo proceso dalis. Pirmoji parinktis yra Leisti turto įsigijimą iš pirkimo. Jei šią parinktį nustatote į Taip, turto įsigijimas vykdomas, kai užregistruojama SF. Jei šią parinktį nustatote į Ne, vis tiek galite ilgalaikį turtą taikyti pirkimo užsakyme (PU) ir SF, bet įsigijimas nebus registruojamas. Registravimą reikės atlikti kaip atskirą ilgalaikio turto žurnalo veiksmą. Parinktis Kurti turtą registruojant produkto gavimo kvitą ar sąskaitą faktūrą suteikia galimybę iš karto kurti naują turtą, todėl prieš operaciją jo kaip ilgalaikio turto nustatyti nereikės. Paskutinė pasirinktis Tikrinti, ar įvedant eilutę kuriamas ilgalaikis turtas taikoma tik pirkimo paraiškoms.

Priežasčių kodus galima konfigūruoti taip, kad jų reikėtų keičiant ilgalaikį turtą arba atliekant konkrečias ilgalaikio turto operacijas.

Galiausiai skirtuke Numeracijos galite nurodyti ilgalaikio turto numeracijas. Ilgalaikio turto numeraciją galima perrašyti, jeigu nurodyta ilgalaikio turto grupės numeracija.

Daugiau informacijos žr. [Kurti ilgalaikius turtus](tasks/create-fixed-asset.md).


