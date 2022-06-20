---
title: Produkto parengtis
description: Šiame straipsnyje paaiškinama, kaip galima naudoti pasirengimo patikrinimus norint užtikrinti, kad prieš naudojant produktą operacijose reikiami pagrindiniai duomenys yra užbaigti.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8e76d5fc786b6f4cac7cd0430399ca3ad13a7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856228"
---
# <a name="product-readiness"></a>Produkto parengtis

[!include [banner](../includes/banner.md)]

Galite naudoti parengtumo patikras, kad jos padėtų užtikrinti, kad visi būtini pagrindiniai duomenys būtų nurodyti produktui prieš jo naudojimą perlaidose. Kai parengtumo patikros naudojamos, vartotojas ar komanda yra atsakinga už konkrečių iš anksto nustatytų produkto duomenų patvirtinimą.

Galite pažymėti **Aktyvus** žymės laukelį inžinerijos produktui, variantui ar versijai tik po to, kai visi būtini duomenys įvesti ir patvirtinti ir kai visos parengtumo patikros yra sutvarkytos. Jei viena ar daugiau produkto, versijos ar varianto patikrų nebuvo apdorotos, tada, kai bandysite pažymėti žymės langelį **Aktyvus**, gausite raginimo perspėjimą, kad ne visos patikros buvo užbaigtos.

Galite sukurti parengtumo patikras naujiems inžineriniams produktams, variantams ar versijoms. Taip pat galite taikyti parengtumo patikras standartiniams (ne inžinerijos) produktams (taip pat skaitykite [Standartinių produktų parengtumo patikros](#standard-products)). 

Operacijose galite naudoti standartinius produktus, nors ne visos parengtumo patikros buvo atliktos. Jei reikia užblokuoti produkto naudojimo operacijose, naudokite jo ciklo būseną. Galite priskirti ciklo būseną, kuri neleidžia naudoti produkto operacijose, o tada, baigę visas parengtumo patikras, priskirkite naują ciklo būseną, kuri leidžia atlikti reikalingas operacijas.

## <a name="types-of-readiness-checks"></a>Parengtumo patikrų tipai

Yra trys parengtumo patikrų tipai:

- **Sisteminės patikros** – Sistema patikrina, ar yra galiojantis įrašas. Pavyzdžiui, įrašas gali būti galiojantis medžiagų aprašas (BOM).
- **Rankinės patikros** – Vartotojas patikrina, ar yra galiojantis įrašas. Pavyzdžiui, parengtumo patikrą gali reikėti patvirtinti pagal nutylėto užsakymo nustatymus. Kai kuriais atvejais, tokiais kai produktas vis dar yra kuriamas ir dėl to negali būti padedamas į atsargas, nėra jokių būtinų nustatytojo užsakymo nustatymų. Nepaisant to, numatytieji užsakymo nustatymai gali būti reikalingi kitam to paties tipo produktui, nes produktą gali reikėti laikyti su atsargomis. Vartotojas atsakingas už tai, kaip tinkamai nuspręsti, ar parengtumo patikra būtina.
- **Patikrų sąrašas** – Vartotojas atsako už klausimų serijas iš patikrų sąrašo ir sistema nustato, ar atsakymai atitinka lūkesčius. Patikrų sąrašas gali turėti bet kokį subjektą. Pavyzdžiui, jis gali būti naudojamas siekiant nustatyti, ar ženklinimo medžiagos ar produkto dokumentai yra baigti.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Kaip pasirengimo patikrinimai sukuriama naujam inžineriniam produktui, variantui ar versijai

Pasirengimo patikrinimų strategijos gali būti taikomos išleisto produkto lygiu, išleisto varianto lygiu ir inžinerinės versijos lygiu.

Kai kuriate naują *inžinerinį produktą*, sistema nustato, ar jam taikoma [pasirengimo patikrinimo strategija](#assign-policy). Jei taikoma pasirengimo tikrinimo strategija, atsitinka šie įvykiai:

- Parengtumo patikros yra sukuriamos produktui pagal taikomą strategiją.
- Inžinerijos versija yra nustatyta kaip neįjungta siekiant užblokuoti produktą nuo naudojimo. Visos produkto inžinerinės versijos nustatytos kaip neaktyvios.

Jei naujas *variantas* sukuriamas produktui, sistema patikrina, ar jam taikoma pasirengimo patikrinimo strategija. (Pasirengimo patikrinimai gali būti taikomi išleisto varianto lygiu ir inžinerijos versijos lygiu.) Jei strategija yra taikoma, atsitinka šie įvykiai:

- Parengtumo patikros yra sukuriamos produktui pagal taikomą strategiją.
- Inžinerijos versija ir variantas nustatomi kaip neaktyvūs, siekiant užblokuoti produktą nuo naudojimo.

Jei nauja inžinerinė *versija* yra sukuriama produktui, sistema patikrina, ar jam taikoma pasirengimo patikrinimo strategija. (Pasirengimo patikrinimai gali būti taikomi inžinerijos versijos lygiu.) Jei strategija yra taikoma, atsitinka šie įvykiai:

- Parengtumo patikros yra sukuriamos produktui pagal taikomą strategiją.
- Inžinerijos versija yra nustatyta kaip neįjungta siekiant užblokuoti produktą nuo naudojimo.

> [!NOTE]
> Taip pat galite nustatyti pasirengimo patikrinimų strategijas standartiniams (neinžineriniams) produktams. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr. standartinių](#standard-products) produktų pasirengimo tikrinimus.

## <a name="view-readiness-checks"></a>Peržiūrėti parengtumo patikras

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Peržiūrėti atviras parengtumo patikras produktui ar jo versijai

Norėdami surasti atviras produkto parengtumo patikras, atidarykite **Išleistų produktų išsamios informacijos** puslapį. Tada, veiksmų juostoje skirtuke **Produkto** grupėje **Parengtumo patikros** pasirinkite **Parengtumo patikros**.

Norėdami surasti atvirą parengtumo patikrą produkto versijai, atverkite **Inžinerijos versijų** puslapį išleistam produktui ar pasirinktai versijai. Tada, veiksmų juostoje skirtuke **Produkto** grupėje **Patikros** pasirinkite **Parengtumo patikros**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Peržiūrėkite atviras parengtumo patikras, kurios jums priskirtos

Norėdami peržiūrėti atviras parengtumo patikras, kurios jums priskirtos, atlikite vieną iš veiksmų.

- Eikite į **Inžinerijos keitimo valdymą \> Bendri \> Produkto parengtumas \> Mano atviros parengtumo patikros**.
- Eikite į **Produkto informacijos valdymas \> Darbo erdvės \> Produkto parengtumas diskretiškai gamybai**.

Nustatymas, nurodantis, kam priskirtas pasirengimo patikrinimas, yra atliekamas pasirengimo strategijai. Parengtumo patikros gali būti priskirtos asmeniui ar komandai. Jei parengtumo patikra priskirta komandai, yra vienas asmuo komandoje, kuri turi sutvarkyti parengtumo patikrą.

## <a name="process-open-readiness-checks"></a>Tvarkyti atviras parengtumo patikras

### <a name="process-system-and-manual-readiness-checks"></a>Tvarkykite sistemą ir rankinio parengtumo patikras

Jums atvėrus **Parengtumo patikrų** puslapį galite peržiūrėti sistemos ir rankinių parengtumo patikrų subjektą pasirinkę **Peržiūrėti susijusią informaciją** . Tuomet galite užbaigti ir (arba) patvirtinti duomenis parengtumo patikrai. Atverkite parengtumo patikras, kurios turi **Būsenos** vertę *Laukianti*. Būsena rodo, kad parengtumo patikra vis dar turi būti sutvarkyta. Norėdami sutvarkyti parengtumo patikrą, atlikite vieną iš tolesnių veiksmų.

- Veiksmų juostoje rinkitės **Patikra/baigta** tam, kad peržiūrėtumėte ir užbaigtumėte parengtumo patikrą. Jums pabaigus **Būsenos** laukelis yra atnaujinamas į *Patvirtintas*.
- Veiksmų juostoje rinkitės **Praleisti** jei norite praleisti parengtumo patikrą, kuri nėra būtina. Pavyzdžiui, nustatėte parengtumo patikrą kainos apskaičiavimui. Nepaisant to, nusprendėte praleisti šią patikrą, kol produktas vis dar yra kūrimo etape. Tokiu atveju, **Būsenos** laukelis yra naujinamas į *Praleistas*.

Priklausomai nuo parengtumo strategijos konfigūravimo, kai **Būsenos** laukelis pasirengimo patikrai yra naujintas į *Patvirtintas*, papildomo žingsnio gali reikėti siekiant patvirtinti parengtumo patikrą. Tokiu atveju, rinkitės **Patvirtinimą** tam, kad užbaigtumėt parengtumo patikrą. Šis patvirtinimo žingsnis visuomet privalomas, kai parengtumo patikra praleista.

Kai visos atviros parengtumo patikros naujam produktui, variantui ar versijai buvo sutvarkytos ir patvirtintos kaip būtina, prekė automatiškai tampa įjungta ir dėl to parengta naudoti.

### <a name="process-checklist-readiness-checks"></a>Tvarkyti patikrinimo sąrašo parengtumo patikras

Norėdami atverti patikrų sąrašą, atverkite **Parengtumo patikrų** puslapį ir tada veiksmų juostoje pasirinkite **Pradėti patikrinimo sąrašą**. Jums užbaigus patikrų sąrašą, sistema patvirtina, ar parengtumo patikra yra patvirtinta pagal klausimyno nustatymus. Jei ši patikra praleidžiama, **Būsenos** laukelis yra atnaujinamas į *Patvirtintas*. Jei parengtumo patikra neprivaloma, galite ją praleisti. Tokiu atveju, **Būsenos** laukelis yra naujinamas į *Praleistas*.

Priklausomai nuo parengtumo strategijos konfigūravimo, kai **Būsenos** laukelis pasirengimo patikrai yra naujintas į *Patvirtintas*, papildomo žingsnio gali reikėti siekiant patvirtinti parengtumo patikrą. Tokiu atveju, rinkitės **Patvirtinimą** tam, kad užbaigtumėt parengtumo patikrą. Šis patvirtinimo žingsnis visuomet privalomas, kai parengtumo patikra praleista.

Kai visos atviros parengtumo patikros naujam produktui, variantui ar versijai buvo sutvarkytos ir patvirtintos kaip būtina, prekė automatiškai tampa įjungta ir dėl to parengta naudoti.

## <a name="create-and-manage-product-readiness-policies"></a>Sukurkite ir valdykite produkto parengtumo strategijas

Naudokite produkto parengtumo strategijas, kad valdytumėte parengtumo patikras taikomas produktui. Kiekviena parengtumo strategija turi parengtumo patikrų rinkinį. Kai pasirengimo strategija yra priskirta inžinerijos produkto kategorijai arba bendrinamam produktui, visi su ta kategorija susiję produktai arba bendrinami produktai turės pasirengimo patikrinimus, įtrauktus į pasirengimo strategiją.

Tam, kad dirbtumėte su produkto parengtumo strategijomis, eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto parengtumo strategijos**. Tuomet atlikite vieną iš šių žingsnių.

- Norėdami sukurti naują strategiją, rinkitės **Naujas** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami redaguoti esančią politiką, sąrašo juostoje ją pasirinkite ir rinkitės **Redaguoti** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami panaikinti politiką, sąrašo juostoje ją pasirinkite ir rinkitės  **Redaguoti** veiksmų juostoje ir tada **Bendri** „FastTab“, įsitikinkite, kad **Įjungta** parinktis nustatyta į *Ne*. Tada rinkitės **Naikinti** veiksmų juostoje.

### <a name="header"></a>Antraštė

Nustatykite tolesnius laukelius produkto parengtumo strategijai.

| Laukas | Aprašas |
|---|---|
| Pavadinimas | Įveskite strategijos pavadinimą. |
| aprašymas | Įveskite politikos aprašą. |

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

Nustatykite tolesnius laukelius **Bendri** produkto parengtumo strategijos „FastTab“.

| Laukas | Aprašas |
|---|---|
| Produkto tipas | Pasirinkite, ar strategija taikoma produktams *Prekės* ar *Paslaugų* tipo. Negalite keisti šio nustatymo po to, kai įrašote įrašą. |
| Aktyvios | Naudokite šią parinktį, kad padėtumėte išlaikyti savo pasirengimo strategijas. Nustatykite į *Taip* visom jūsų naudojamoms parengimo strategijoms. Nustatykite į *Ne* tam, kad pažymėtumėte parengimo strategiją kaip neaktyvią jos nenaudodami. Įsidėmėkite, kad negalite išjungti pasirengimo strategijos, kuri yra priskirta inžinerijos produkto kategorijai arba bendrinamam produktui, o panaikinti galite tik neaktyvias leidimo strategijas. |

### <a name="readiness-control-fasttab"></a>Parengimo valdymo „FastTab“

Kiekvienam parengimo patikros tipui, kuris jūsų nuomone turi įtraukti strategiją, įtraukite eilutę **Parengimo valdymo** „FastTab“. Naudokite tolesnius mygtukus Visi produktai „FastTab“ įrankių juostoje norėdami įtraukti ir pašalinti eilutes, kurių jums reikia:

- **Įtraukti patikrą** – Įtraukite standartinę parengimo patikrą į strategiją. Jums pasirinkus šį mygtuką, **Įtraukti patikrą** teksto laukelis pasirodo. Dėl to, galite pasirinkti esamas patikras iš sąrašo.
- **Įtraukite esantį klausimyną** – Įtraukti tuščią eilutę į tinklelį. Tuomet galite priskirti esantį klausimyną nustatydami laukelius tolesnėje lentelėje.
- **Kopijuoti** – Įtraukite pasirinktos eilutės kopiją į tinklelį.
- **Naikinti** – Panaikinkite pasirinktą eilutę iš tinklelio.

Kiekvienai įtrauktai eilutei, nustatykite tolesnius laukelius.

| Laukas | Aprašas |
| --- | --- |
| Proceso sritis | Pasirinkite sritį, su kuria susieta patikra. |
| Tipas | Pasirinkite, ar patikra yra sistemos patikra, rankinė ar iš patikrų sąrašo (klausimyno). |
| Pavadinimas | Jei patikra yra iš sąrašo, įveskite pavadinimą. Sistemos ir rankinėms patikroms, šis laukelis automatiškai nustatomas. |
| Aprašas | Jei patikra yra iš sąrašo, įveskite aprašą. Sistemos ir rankinėms patikroms, šis laukelis nustatomas automatiškai ir aprašas paaiškina patikros fokusą. |
| Taikyti patikras kam | Pasirinkite, ar eilutė turi būti sukurta parengtumo patikroms atsakant į naują išleistą produktą, išleistą variantą ar versiją. |
| Vykdyti | Pasirinkite, ar pasirengimo patikros, kurias eilutė sukuria taikomos visoms bendrovėms ar vienai. |
| Įmonė | Jei nustatote **Vykdyti** laukelį į *Vienoje bendrovėje*, pasirinkite bendrovę. |
| Savininko tipas | Pasirinkite, ar pasirengimo patikros, kurias eilutė sukuria turi būti priskirtos asmeniui ar komandai. |
| Savininkas | Pasirinkite asmenį ar komandą, kuriems bus priskirtos pasirengimo patikros, kurias eilutė sukuria. |
| Klausimynas | Rinkitės klausimyną, kuris turi būti naudojamas patikrų sąraše. Patikrų sąrašas yra vietinis patikrų sąrašas bendrovėje, kai pasirengimo patikra yra atlikta. Sistema privalo galėti įvertinti, ar patikrų sąrašas yra tinkamai sudarytas. Dėl to, patikrų sąrašą reikia nustatyti taip, kad vertinimas būtų atliktas pagal tinkamus atsakymus. Daugiau informacijos apie klausimynų kūrimo ieškokite klausimynų [naudojimas](/dynamicsax-2012/appuser-itpro/using-questionnaires) ir su jais susijusius straipsnius. |
| Automatinis patvirtinimas | Pasirengimo patikros įrašai apima **Patvirtinta** žymimą laukelį, kuris rodo patvirtinimo būseną. Pasirinkite **Automatinis patvirtinimas** žymimą laukelį patikroms, kurias reikia nustatyti kaip patvirtintas iš karto po jų priskyrimo vartotojams, kurie jas užbaigia. Atžymėkite šį laukelį, kad pareikalautumėte atskiro patvirtinimo kaip papildomo žingsnio. |
| Privalomas | Pasirinkite šį laukelį patikroms, kurias turi užbaigti paskirtas vartotojas. Privalomos patikros negali būti praleistos. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Pasirengimo strategijų priskyrimas standartiniams ir inžineriniams produktams

Kai kuriate naują produktą pagal inžinerijos kategoriją, sukuriate tiek *išleistą produktą*, tiek susijusį *bendrinamą* produktą. Būdas, kaip *yra* išspręstos išleisto produkto pasirengimo strategijos, priklauso nuo to, ar jūsų sistemai įjungta produkto pasirengimo tikrinimo funkcija ([informacijos](#standard-products) apie šią funkciją ir kaip įjungti ar išjungti standartinių produktų skyriuje žr. pasirengimo tikrinimus toliau šiame straipsnyje).

- Kai *Produkto pasirengimo patikrinimų* funkcija yra *išjungta* jūsų sistemoje, pasirengimo strategija yra nustatoma ir rodoma tik [inžinerijos kategorijos](engineering-versions-product-category.md) įrašuose. Tam, kad sužinotų, kuri strategija taikoma išleistam produktui, sistema tikrina **Produkto pasirengimo strategijos** lauką susijusiai inžinerijos kategorijai. Galite pakeisti esamo produkto pasirengimo strategiją redaguodami susijusią inžinerijos kategoriją (ne bendrinamą produktą).
- Kai *Produkto pasirengimo patikrinimų* funkcija yra *įjungta*, ji prideda **Produkto pasirengimo strategijos** lauką į **Produkto** puslapį (kuriame nustatomi bendrinami produktai) ir į **Išleisto produkto puslapį** (kuriame reikšmė yra tik skaitoma ir paimta iš susijusio bendrinamo produkto). Sistema randa išleisto produkto pasirengimo strategiją tikrindama susijusį bendrai naudojamą produktą. Jei kurdami naują inžinerijos produktą naudojate inžinerijos kategoriją, sistema sukuria tiek bendrai naudojamą, tiek išleistą produktą, ir nukopijuoja visus inžinerijos kategorijos **Produkto pasirengimo strategijos** nustatymus į naują bendrai naudojamą produktą. Tada galite pakeisti esamo produkto pasirengimo strategiją redaguodami susijusį bendrinamą produktą (ne išleistą inžinerijos kategoriją).

Norėdami priskirti parengties strategiją bendrinamam produktui, atlikite šiuos žingsnius.

1. Eikite į **Produkto informacija \> Produktai \> Produktai**.
1. Atidarykite arba sukurkite produktą, kuriam norite priskirti pasirengimo strategiją.
1. „FastTab” **Bendra** nustatykite **Produkto pasirengimo strategijos** lauką kaip strategijos, kuri turėtų būti taikoma produktui, pavadinimą.

Norėdami priskirti parengties strategiją inžinerijos kategorijai, atlikite šiuos žingsnius.

1. Eikite į **Inžinerinių keitimų valdymas \> Sąranka \> Inžinerijos produktų kategorijų išsami informacija**.
1. Atidarykite arba sukurkite inžinerijos kategoriją, kuriai norite priskirti pasirengimo strategiją.
1. „FastTab” **Produkto pasirengimo strategija** nustatykite **Produkto pasirengimo strategijos** lauką kaip strategijos, kuri turėtų būti taikoma inžinerijos kategorijai, pavadinimą.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Standartinių produktų pasirengimo patikrinimai

Galite įgalinti produkto pasirengimo patikrinimus standartiniams (ne inžinerijos) produktams įjungdami funkciją *Produkto pasirengimo patikrinimai* Funkcijų valdyme. Ši funkcija atlieka keletą smulkių pasirengimo patikrinimo sistemos pakeitimų tam, kad ji palaikytų standartinius produktus.

### <a name="enable-or-disable-readiness-checks-on-standard-products"></a>Įjungti arba išjungti standartinių produktų pasirengimo tikrinimą

Šiai funkcijai reikia, kad *jūsų sistemai* būtų įjungti *ir inžinerinių* pakeitimų valdymo ir produkto pasirengimo tikrinimų priemonės. Išsamesnės informacijos apie šių funkcijų įjungimą ir išjungimą žr. Inžinerinių [pakeitimų valdymo peržiūra](product-engineering-overview.md).

### <a name="create-readiness-policies-for-standard-products"></a>Standartinių produktų pasirengimo strategijų kūrimas

Kuriate pasirengimo strategijas standartiniams produktams taip pat, kaip ir inžineriniams produktams. Daugiau informacijos ieškokite šiame straipsnyje.

### <a name="assign-readiness-policies-to-standard-products"></a>Pasirengimo strategijų priskyrimas standartiniams produktams

Norėdami priskirti pasirengimo strategiją standartiniam produktui, atidarykite susijusį bendrai naudojamą produktą ir nustatykite **Produkto pasirengimo strategijos** lauką į strategijos, kuri turėtų būti taikoma, pavadinimą. Daugiau informacijos ieškokite anksčiau šiame [straipsnyje pateiktame standartinių ir inžinerijos produktų](#assign-policy) skyriuje Priskirti pasirengimo strategijas.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Peržiūrėti ir apdoroti standartinių produktų pasirengimo patikrinimus

Kai ši funkcija įjungta, peržiūrite ir apdorojate patikrinimus standartiniams produktams taip pat, kaip ir inžineriniams produktams. Daugiau informacijos ieškokite šiame straipsnyje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
