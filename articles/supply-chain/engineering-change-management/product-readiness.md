---
title: Produkto parengtis
description: Šioje temoje paaiškinta, kaip galite naudoti parengtumo patikras siekiant užtikrinti, kad būtini pagrindiniai duomenys yra baigti produktui prieš jo naudojimą perlaidose.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 58b5a35800ab464f25868c6756b16f25d14d8d78
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434049"
---
# <a name="product-readiness"></a>Produkto parengtis

[!include [banner](../includes/banner.md)]

Galite naudoti parengtumo patikras siekiant užtikrinti, kad visi būtini pagrindiniai duomenys būtų nurodyti produktui prieš jo naudojimą perlaidose. Kai parengtumo patikros naudojamos, vartotojas ar komanda yra atsakinga už konkrečių iš anksto nustatytų produkto duomenų patvirtinimą. Jei yra atvira parengtumo patikra produktui, jis negali būti išleistas ar naudojamas perlaidose.

Žymimas laukelis **Įjungtas** inžinerijos produktui, variantui ar versijai prieinamas tik po to, kai visi būtini duomenys įvesti ir patvirtinti ir kai visos parengtumo patikros yra sutvarkytos. Tuo metu, produktas, versija ar variantas gali būti išleistas į kitas bendroves ir naudojamas perlaidose. Galite sukurti parengtumo patikras naujam produktui, variantui ar inžinerijos versijai.

## <a name="types-of-readiness-checks"></a>Parengtumo patikrų tipai

Yra trys parengtumo patikrų tipai:

- **Sisteminės patikros** – Sistema patikrina, ar yra galiojantis įrašas. Pavyzdžiui, įrašas gali būti galiojantis medžiagų aprašas (BOM).
- **Rankinės patikros** – Vartotojas patikrina, ar yra galiojantis įrašas. Pavyzdžiui, parengtumo patikrą gali reikėti patvirtinti pagal nutylėto užsakymo nustatymus. Kai kuriais atvejais, tokiais kai produktas vis dar yra kuriamas ir dėl to negali būti padedamas į atsargas, nėra jokių būtinų nustatytojo užsakymo nustatymų. Nepaisant to, numatytieji užsakymo nustatymai gali būti reikalingi kitam to paties tipo produktui, nes produktą gali reikėti laikyti su atsargomis. Vartotojas atsakingas už tai, kaip tinkamai nuspręsti, ar parengtumo patikra būtina.
- **Patikrų sąrašas** – Vartotojas atsako už klausimų serijas iš patikrų sąrašo ir sistema nustato, ar atsakymai atitinka lūkesčius. Patikrų sąrašas gali turėti bet kokį subjektą. Pavyzdžiui, jis gali būti naudojamas siekiant nustatyti, ar ženklinimo medžiagos ar produkto dokumentai yra baigti.

## <a name="how-readiness-checks-are-created-for-a-new-product-variant-or-version"></a>Kaip parengtumo patikros sukuriamos naujam produktui, variantui ar versijai

Jums sukūrus naują inžinerijos **produktą**, sistema nustato, ar parengtumo patikros politika buvo nustatyta inžinerijos produkto kategorijai. (Parengtumo patikros politikos gali būti taikomos išleistam produkto lygiui, išleistas varianto lygis ir inžinerijos versijos lygiui.) Jei politika buvo nustatyta, atsitinka tolesni įvykiai:

- Parengumo patikros yra sukuriamos produktui pagal taikomą politiką.
- Inžinerijso versija yra nustatyta kaip neįjungta siekiant užblokuoti produktą nuo naudojimo. Visos versijos konkrečiam produktui, yra neįjungtos.

Jei naujas **variantas** sukuriamas produktui, sistema tikrina, ar parengtumo patikros buvo nustaytos inžinerijos produkto kategorijoje. (Parengtumo patikros politikos gali būti taikomos išleistam produkto lygiui, išleistas varianto lygis ir inžinerijos versijos lygiui.) Jei parengtumo patikra buvo nustatyta, atsitinka tolesni įvykiai:

- Parengtumo patikros sukuriamos produktui.
- Inžinerijso versija yra nustatyta kaip neįjungta siekiant užblokuoti produktą nuo naudojimo.

Jei nauja inžinerijos **versija** sukuriama produktui, sistema tikrina, ar parengtumo patikros buvo nustaytos inžinerijos produkto kategorijoje. (Parengtumo patikros gali būti taikomos inžinerijos versijos lygiui.) Jei parengtumo patikra buvo nustatyta, atsitinka tolesni įvykiai:

- Parengtumo patikros sukuriamos produktui.
- Inžinerijso versija yra nustatyta kaip neįjungta siekiant užblokuoti produktą nuo naudojimo.

## <a name="view-readiness-checks"></a>Peržiūrėti parengtumo patikras

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Peržiūrėti atviras parengtumo patikras produktui ar jo versijai

Norėdami surasti atviras produkto parengtumo patikras, atidarykite **Išleistų produktų išsamios informacijos** puslapį. Tada, veiksmų juostoje skirtuke **Produkto** grupėje **Parengtumo patikros** pasirinkite **Parengtumo patikros**.

Norėdami surasti atvirą parengtumo patikrą produkto versijai, atverkite **Inžinerijos versijų** puslapį išleistam produktui ar pasirinktai versijai. Tada, veiksmų juostoje skirtuke **Produkto** grupėje **Patikros** pasirinkite **Parengtumo patikros**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Peržiūrėkite atviras parengtumo patikras, kurios jums priskirtos

Norėdami peržiūrėti atviras parengtumo patikras, kurios jums priskirtos, atlikite vieną iš veiksmų.

- Eikite į **Inžinerijos keitimo valdymą \> Bendri \> Produkto parengtumas \> Mano atviros parengtumo patikros**.
- Eikite į **Produkto informacijos valdymas \> Darbo erdvės \> Produkto parengtumas diskretiškai gamybai**.

Nustatymas, kuris rodo, kam parengtumo patikra priskirta pagal inžinerinio produkto kategoriją. Parengtumo patikros gali būti priskirtos asmeniui ar komandai. Jei parengtumo patikra priskirta komandai, yra vienas asmuo komandoje, kuri turi sutvarkyti parengtumo patikrą. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

## <a name="process-open-readiness-checks"></a>Tvarkyti atviras parengtumo patikras

### <a name="process-system-and-manual-readiness-checks"></a>Tvarkyit sistemą ir rankinio parengtumo patikras

Jums atvėrus **Parengtumo patikrų** puslapį galite peržiūrėti sistemos ir rankinių parengtumo patikrų subjektą pasirinkę **Peržiūrėti susijusią informaciją** . Tuomet galite užbaigti ir (arba) patvirtinti duomenis parengtumo patikrai. Atverkite parengtumo patikras, kuriso turi **Būsenos** vertę *Laukianti*. Būsena rodo, kad parengtumo patikra vis dar turi būti sutvarkyta. Norėdami sutvarkyti parengtumo patikrą, atlikite vieną iš tolesnių veiksmų.

- Veiksmų juostoje rinkitės **Patikra/baigta** tam, kad peržiūrėtumėte ir užbaigtumėte parengtumo patikrą. Jums pabaigus **Būsenos** laukelis yra atnaujinamas į *Patvirtintas*.
- Veiksmų juostoje rinkitės **Praleisti** jei norite praleisti parengtumo patikrą, kuri nėra būtina. Pavyzdžiui, nustatėte parengtumo patikrą kainos apskaičiavimui. Nepaisant to, nusprendėte praleisti šią patikrą, kol produktas vis dar yra kūrimo etape. Tokiu atveju, **Būsenos** laukelis yra naujinamas į *Praleistas*.

Priklausomai nuo parengtumo poltikos konfigūravimo, kai **Būsenos** laukelis pasirengimo patikrai yra naujintas į *Patvirtintas*, papildomo žingsnio gali reikėti siekiant patvirtinti parengtumo patikrą. Tokiu atveju, rinkitės **Patvirtinimą** tam, kad užbaigtumėt parengtumo patikrą. Šis patvirtinimo žingsnis visuomet privalomas, kai parengtumo patikra praleista.

Kai visos atviros parengtumo patikros naujam produktui, variantui ar versijai buvo sutvarkytos ir patvirtintos kaip būtina, prekė automatiškai tampa įjungta ir dėl to parengta naudoti.

### <a name="process-checklist-readiness-checks"></a>Tvarkyti patikrinimo sąrašo parengtumo patikras

Norėdami atverti patikrų sąrašą, atverkite **Parengtumo patikrų** puslapį ir tada veiksmų juostoje pasirinkite **Pradėti patikrumo sąrašą**. Jums užbaigus patikrų sąrašą, sistema patvirtina, ar parengtumo patikra yra patvirtinta pagal klausimyno nustatymus. Jei ši patikra praleidžiama, **Būsenos** laukelis yra atnaujinamas į *Patvirtintas*. Jei parengtumo patikra neprivaloma, galite ją praleisti. Tokiu atveju, **Būsenos** laukelis yra naujinamas į *Praleistas*.

Priklausomai nuo parengtumo poltikos konfigūravimo, kai **Būsenos** laukelis pasirengimo patikrai yra naujintas į *Patvirtintas*, papildomo žingsnio gali reikėti siekiant patvirtinti parengtumo patikrą. Tokiu atveju, rinkitės **Patvirtinimą** tam, kad užbaigtumėt parengtumo patikrą. Šis patvirtinimo žingsnis visuomet privalomas, kai parengtumo patikra praleista.

Kai visos atviros parengtumo patikros naujam produktui, variantui ar versijai buvo sutvarkytos ir patvirtintos kaip būtina, prekė automatiškai tampa įjungta ir dėl to parengta naudoti.

## <a name="create-and-manage-product-readiness-policies"></a>Sukurkite ir valdykite produkto parengtumo politikas

Naudokite produkto parengtumo politikas, kad valdytumėte parengtumo patikras taikomas produktui. Kadangi parengtumo politika priskirta inžinerijos kategorijai, visos patikros parengtumo politikai taikomos inžinerijos produktams, kruie remiasi inžinerijos kategorija. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

Kiekviena parengtumo politika turi parengtumo patikrų rinkinį. Kai parengtumo politika priskirta inžinerijos produkto kategorijai, visi produktai sukurti iš to inžinerijos produkto kategorijas turės parengtumo patikras, nurodytas parengtumo politikoje.

Tam, kad dirbtumėte su produkto parengtumo politikomis, eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto parengtumo politikos**. Tuomet atlikite vieną iš šių žingsnių.

- Norėdami sukurti naują politiką, rinkitės **Naujas** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami redaguoti esančią politiką, sąrašo juostoje ją pasirinkite ir rinkitės **Redaguoti** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami panaikinti politiką, sąrašo juostoje ją pasirinkite ir rinkitės  **Redaguoti** veiksmų juostoje ir tada **Bendri** „FastTab“, įsitikinkite, kad **Įjungta** parinktis nustatyta į *Ne*. Tada rinkitės **Naikinti** veiksmų juostoje.

### <a name="header"></a>Antraštė

Nustatykite tolesnius laukelius produkto parengtumo politikai.

| Laukas | aprašymas |
|---|---|
| Pavadinimas / vardas ir (arba) pavardė | Įveskite politikos pavadinimą. |
| aprašymas | Įveskite politikos aprašą. |

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

Nustatykite tolesnius laukelius **Bendri** produkto parengtumo politikos „FastTab“.

| Laukas | aprašymas |
|---|---|
| Produkto tipas | Pasirinkite, ar politika taikoma produktams *Prekės* ar *Paslaugų* tipo. Negalite keisti šio nustatymo po to, kai įrašote įrašą. |
| Aktyvios | Naudokite šią parinktį, kad padėtumėte išlaikyti savo pasirengimo politikas. Nustatykite į *Taip* visom jūsų naudojamoms parengimo politikoms. Nustatykite į *Ne* tam, kad pažymėtumėte parengimo politiką kaip neaktyvią jos nenaudodami. Įsidėmėkite, kad negali išjungti parengimo politikos, kuri yra priskirta inžinerijos produkto kategorijai ir galite panaikinti tik neaktyvias leidimo politikas. |

### <a name="readiness-control-fasttab"></a>Parengimo valdymo „FastTab“

Kiekvienam parengimo patikros tipui, kuris jūsų nuomone turi įtraukti politiką, įtraukite eilutę **Parengimo valdymo** „FastTab“. Naudokite tolesnius mygtukus Visi produktai „FastTab“ įrankių juostoje norėdami įtraukti ir pašalinti eilutes, kurių jums reikia:

- **Įtraukti patikrą** – Įtraukite standartinę parengimo patikrą į poltiką. Jums pasirinkus šį mygtuką, **Įtraukti patikrą** teksto laukelis pasirodo. Dėl to, galite pasirinkti esamas patikras iš sąrašo.
- **Įtraukite esantį klausimyną** – Įtraukti tuščią eilutę į tinklelį. Tuomet galite priskirti esantį klausimyną nustatydami laukelius tolesnėje lentelėje.
- **Kopijuoti** – Įtraukite pasirinktos eilutės kopiją į tinklelį.
- **Naikinti** – Panaikinkite pasirinktą eilutę iš tinklelio.

Kiekvienai įtrauktai eilutei, nustatykite tolesnius laukelius.

| Laukas | aprašymas |
| --- | --- |
| Proceso sritis | Pasirinkite sritį, su kuria susieta patikra. |
| Tipas | Pasirinkite, ar patikra yra sistemos patikra, rankinė ar iš patikrų sąrašo (klausimyno). |
| Pavadinimas / vardas ir (arba) pavardė | Jei patikra yra iš sąrašo, įveskite pavadinimą. Sistemos ir rankinėms patikroms, šis laukelis automatiškai nustatomas. |
| aprašymas | Jei patikra yra iš sąrašo, įveskite aprašą. Sistemos ir rankinėms patikroms, šis laukelis nustatomas automatiškai ir aprašas paaiškina patikros fokusą. |
| Taikyti patikras kam | Pasirinkite, ar eilutė turi būti sukurta parengtumo patikroms atsakant į naują išleistą produktą, išleistą variantą ar versiją. |
| Vykdyti | Pasirinkite, ar pasirengimo patikros, kurias eilutė sukuria taikomos visoms bendrovėms ar vienai. |
| Įmonė | Jei nustatote **Vykdyti** laukelį į *Vienoje bendrovėje*, pasirinkite bendrovę. |
| Savininko tipas | Pasirinkite, ar pasirengimo patikros, kurias eilutė sukuria turi būti priskirtos asmeniui ar komandai. |
| Savininkas | Pasirinkite asmenį ar komandą, kuriems bus priskirtos pasirengimo patikros, kurias eilutė sukuria. |
| Klausimynas | Rinkitės klausimyną, kuris turi būti naudojamas patikrų sąraše. Patikrų sąrašas yra vietinis patikrų sąrašas bendrovėje, kai pasirengimo patikra yra atlikta. Sistema privalo galėti įvertinti, ar patikrų sąrašas yra tinkamai sudarytas. Dėl to, patikrų sąrašą reikia nustatyti taip, kad vertinimas būtų atliktas pagal tinkamus atsakymus. Dėl išsamesnės informacijos apie tai, kaip sukurti klausimynus, žr. [Naudoti klausimynus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/using-questionnaires) ir su jais susijusias temas. |
| Automatinis patvirtinimas | Pasirengimo patikros įrašai apima **Patvirtinta** žymimą laukelį, kuris rodo patvirtinimo būseną. Pasirinkite **Automatinis patvirtinimas** žymimą laukelį patikroms, kurias reikia nustatyti kaip patvirtintas iš karto po jų priskyrimo vartotojams, kurie jas užbaigia. Atžymėkite šį laukelį, kad pareikalautumėte atskiro patvirtinimo kaip papildomo žingsnio. |
| Privalomas | Pasirinkite šį laukelį patikroms, kurias turi užbaigti paskirtas vartotojas. Privalomos patikros negali būti praleistos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]