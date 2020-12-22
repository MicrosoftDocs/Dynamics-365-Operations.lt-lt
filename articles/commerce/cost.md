---
title: Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją
description: Šioje temoje aprašomas savikainos konfigūravimas naudojant „Dynamics 365 Commerce“ paskirstytų užsakymų tvarkymo (DOM) funkciją.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459525"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Savikainos konfigūravimas naudojant paskirstytų užsakymų tvarkymo (DOM) funkciją

[!include [banner](../includes/banner.md)]

Siekdamos nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymą, organizacijos apsvarsto keletą savikainos komponentų. Kai kurie iš šių savikainos komponentų yra siuntimo savikaina, tvarkymo savikaina ir pakavimo savikaina. Siekiant nustatyti įvykdymo vietą, apskaičiuojamas šių savikainų derinys.

Kai, naudojant pirmąją „Dynamics 365 Commerce“ paskirstytų užsakymų tvarkymo (DOM) funkciją, optimizuotas užsakymų priskyrimas įvykdymo vietoms, buvo atsižvelgiama tik į atstumą. Nors atstumas gali būti susijęs su savikaina, tai nėra tas pats. Pavyzdžiui, kai atstumas yra toks pats, siuntimo naktį būdas kainuoja daugiau, nei siuntimas per tris dienas ar siuntimas per septynias dienas.

Savikainos konfigūravimo funkcija mažmenininkams leidžia nustatyti ir konfigūruoti papildomus savikainos komponentus, kurie bus apskaičiuojami ir į kuriuos bus atsižvelgiama siekiant nustatyti optimalią vietą, iš kurios būtų galima įvykdyti užsakymų eilutes.

Kai sukonfigūruojami savikainos komponentai, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė naudoja tik tas savikainos apibrėžtis. Atstumo komponento ji nelaiko savikaina. Tačiau, jei savikainos komponentų nėra sukonfigūruota, siekdama nustatyti optimalią vietą užsakymams įvykdyti DOM sprendimų priemonė atstumo komponentą kaip savikainą naudoja.

## <a name="set-up-cost-components"></a>Savikainos komponentų nustatymas

Sistemoje galima nustatyti du pagrindinius savikainos komponentų tipus: **Siuntimo** ir **Kitas**.

Abu savikainos komponentų tipai palaiko keletą skaičiavimo pagrindų, kaip parodyta tolesnėje lentelėje.

<table>
<thead>
<tr>
<th>Savikainos komponento tipas</th>
<th>Skaičiavimo pagrindas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Siuntimo</td>
<td>
<ul>
<li>Paprastas</li>
<li>Pakopinis</li>
</ul>
</td>
</tr>
<tr>
<td>Kitas</td>
<td>
<ul>
<li>Pardavimo užsakymas</li>
<li>Pardavimo eilutė</li>
<li>Vieta</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Siuntimo savikainos komponento tipas

Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo **Siuntimo** derinį ir siuntimo savikainos skaičiavimo pagrindą. Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Paprastas

Jei yra naudojamas savikainos komponento tipo **Siuntimo** ir skaičiavimo pagrindo **Paprastas** derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą.

Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.

- **Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.
- **Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.
- **Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu. Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.
- **Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus. DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.
- **Įmonė** – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas. Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.
- **Pristatymo būdai** – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.
- **Skaičiavimo tipas** – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo savikaina. Palaikomi du tolesni skaičiavimo tipai.

    - **Fiksuotasis** – pristatymo būdui naudojama fiksuotoji savikaina. Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke **Savikaina**.
    - **Pagal atstumo vienetą** – pristatymo būdo savikaina apskaičiuojama kaip lauke **Savikaina** nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.

- **Savikaina** – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku **Skaičiavimo tipas** apskaičiuojama pristatymo būdo savikaina.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Savikainos komponento tipas = Siuntimo, o Skaičiavimo pagrindas = Pakopinis

Jei yra naudojamas savikainos komponento tipo **Siuntimo** ir skaičiavimo pagrindo **Pakopinis** derinys, tam tikro pristatymo būdo siuntimo savikaina apskaičiuojama pagal fiksuotąją savikainą arba atstumą. Tačiau šiame derinyje atstumas nustatomas pagal pakopinį atstumų intervalą.

Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.

- **Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.
- **Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.
- **Numatytoji savikaina** – nurodykite pristatymo būdo savikainą, kuri turi būti naudojama, jei atstumas tarp pristatymo adreso ir vietos nepatenka į jokį iš pristatymo būdo pakopinių atstumų.
- **Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu. Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.
- **Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus. DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.
- **Įmonė** – nurodykite juridinį subjektą, kuriam savikainos faktorius yra sukonfigūruotas. Visos skaičiavimo kriterijų eilutės turi būti to paties juridinio subjekto.
- **Pristatymo būdai** – nurodykite pristatymo būdus, kuriems savikaina yra sukonfigūruota.
- **Atstumo tipas** – nurodykite, ar pakopinis atstumas apibrėžiamas kaip atstumas oru, ar atstumas keliais.
- **Atstumo vienetai** – nurodyti vienetą, kuriuo matuojamas pakopinis atstumas.
- **Atstumas nuo** – nurodykite pakopinio atstumo intervalo pradžią.
- **Atstumas iki** – nurodykite pakopinio atstumo intervalo pabaigą.
- **Skaičiavimo tipas** – nurodykite, kaip turi būti skaičiuojama konkretaus pristatymo būdo ir pakopinio atstumo savikaina. Palaikomi du tolesni skaičiavimo tipai.

    - **Fiksuotasis** – pristatymo būdui naudojama fiksuotoji savikaina. Jei pasirenkate šį skaičiavimo tipą, fiksuotoji savikaina nustatoma lauke **Savikaina**.
    - **Pagal atstumo vienetą** – pristatymo būdo ir pakopinio atstumo savikaina apskaičiuojama kaip lauke **Savikaina** nurodyta savikainos reikšmė, padauginta iš atstumo tarp pristatymo adreso ir vietų.

- **Savikaina** – nurodykite savikainos reikšmę, kurią naudojant kartu su lauku **Skaičiavimo tipas** apskaičiuojama pristatymo būdo savikaina.

> [!NOTE]
> - Kai nustatote pakopinius atstumus, sistema patikrina, kad atstumų netrūktų ir kad jie nepersidengtų.
> - Naudojamas tam tikro pristatymo būdo atstumo tipas turi būti toks pats visuose pakopiniuose atstumuose.

### <a name="other-cost-component-type"></a>Savikainos komponento tipas Kitas

Šiame skyriuje paaiškinama, kaip nustatyti kiekvieną savikainos komponento tipo **Kitas** derinį ir kitą su siuntimu nesusijusių savikainų tipą. Jame taip pat paaiškinama, kaip DOM sprendimų priemonė naudoja kiekvieną derinį.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo užsakymas

Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Pardavimo užsakymas** derinį, pardavimo užsakymo lygiu apibrėžiamos su siuntimu nesusijusios savikainos.

Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.

- **Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.
- **Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.
- **Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu. Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.
- **Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus. DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.
- **Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo lygiu.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Pardavimo eilutė

Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Pardavimo eilutė** derinį, pardavimo užsakymo eilutės lygiu apibrėžiamos su siuntimu nesusijusios savikainos.

Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.

- **Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.
- **Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.
- **Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu. Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.
- **Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus. DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.
- **Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę pardavimo užsakymo eilutės lygiu.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Savikainos komponento tipas = Kitas, o Kitas savikainos tipas = Vieta

Naudojant savikainos komponento tipo **Kitas** ir kito savikainos tipo **Vieta** derinį, apibrėžiamos vietų grupės arba atskiros vietos su siuntimu nesusijusios savikainos.

Norėdami naudoti šį derinį, turite nustatyti tolesnius laukus.

- **Savikainos faktorius** – įveskite unikalų savikainos faktoriaus identifikatorių.
- **Aprašas** – įveskite savikainos faktoriaus pavadinimą ir aprašą.
- **Pradžios data** ir **Pabaigos data** – naudodami šiuos laukus galite apriboti savikainos faktorių konkrečiu datų intervalu. Jei šiuos laukus paliekate tuščius, savikainos faktorius galioja neribotą laikotarpį.
- **Aktyvus** – nurodykite, ar savikainos faktorius yra aktyvus. DOM svarsto tik aktyvius savikainos faktorius, susietus su įvykdymo profiliu.
- **Įvykdymo grupė** – nurodykite vietų grupę, kuriai apibrėžta su siuntimu nesusijusi savikaina.
- **Įvykdymo vieta** – nurodykite vietą, kuriai apibrėžta su siuntimu nesusijusi savikaina.

    > [!NOTE]
    > Toje pačioje vieta pagrįstų skaičiavimo kriterijų eilutėje negalite nurodyti ir įvykdymo grupės, ir įvykdymo vietos.

- **Savikaina** – nurodykite su siuntimu nesusijusios savikainos reikšmę įvykdymo grupės lygiu arba įvykdymo vietos lygiu.

> [!IMPORTANT]
> Norint, kad vykdoma DOM funkcija svarstytų šias savikainas, į atitinkamą įvykdymo profilį turite įtraukti savikainos faktorių.
