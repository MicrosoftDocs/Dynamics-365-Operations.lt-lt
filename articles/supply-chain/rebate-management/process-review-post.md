---
title: Grąžinimų apdorojimas, peržiūra ir registravimas
description: Šioje temoje aprašoma, kaip apdoroti jūsų grąžinimo valdymo sandorius, apskaičiuoti jų nuolaidas, peržiūrėti sugeneruotas operacijas, registruoti operacijas ir peržiūrėti registravimus.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 82b8a4e6ba7ebea7df9f5dad5abc3dfc3ce2687d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270766"
---
# <a name="process-review-and-post-rebates"></a>Grąžinimų apdorojimas, peržiūra ir registravimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip apdoroti jūsų grąžinimo valdymo sandorius, apskaičiuoti jų nuolaidas, peržiūrėti sugeneruotas operacijas, registruoti operacijas ir peržiūrėti registravimus.

## <a name="change-the-status-of-a-deal"></a>Sandorio būsenos pakeitimas

Kiekvienam sandoriui galite priskirti būseną, kad jį būtų galima sekti. Būsena skirta tik informaciniais tikslais.

1. Pasirinkite sandorį (pavyzdžiui, [puslapyje **Visi grąžinimų valdymo sandoriai**](rebate-management-deals.md)).
1. Veiksmų srities skirtuke **Grąžinimų valdymo sandoriai**, grupėje **Prižiūrėti** pasirinkite **Keisti būseną**.
1. Dialogo lange **Keisti būseną** laukui **Grąžinimų būsenos** nustatykite naują būseną.
1. Pasirinkite **Gerai**.

## <a name="calculate-fifo-purchase-prices"></a>FIFO pirkimo kainų skaičiavimas

Reikia vykdyti periodinę užduotį **Skaičiuoti FIFO pirkimo kainą** tam, kad suskaičiuoti grąžinimus tiems [sandoriams](rebate-management-deals.md), kurių laukas **Kainos pagrindimas** nustatytas į *FIFO*. Sistema naudos „pirmas ateina, pirmas išeina” (FIFO) taisyklę parduotų atsargų reikšmei suskaičiuoti. Tada ši vertė bus naudojama tiekėjo grąžinimams skaičiuoti.

Eikite į **Grąžinimo valdymas \> Periodinės užduotys \> Skaičiuoti FIFO pirkimo kainą**. Pasirodžiusiame dialogo lange pasirinkite **Gerai** skaičiavimui vykdyti.

## <a name="process-rebate-management-deals"></a>Grąžinimų valdymo sandorių apdorojimas

Kai apdorojate sandorį, sistema apskaičiuoja visus nustatytus atitinkamus grąžinimus ir autorinius honorarus. Bus apdorojami tik pasirinkti sandoriai, kurių skaičiavimo laikotarpiai yra parengti skaičiuoti, ir kurių būsena yra *Aktyvi*. Užbaigus apdorojimą, sistema sugeneruoja operacijų rinkinį, kurį galite peržiūrėti ir tada registruoti.

> [!NOTE]
> Visais atvejais, grąžinimai yra apdorojami lygyje, kurį nustato kiekvieno sandorio **Derinti pagal** parametras (*Sandoris* arba *Eilutė*). Vienos eilutės skaičiavimus galite atlikti tik tiems sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė*.

### <a name="process-all-lines-for-one-or-more-deals"></a>Vieno ar daugiau sandorių visų eilučių apdorojimas

1. Atidarykite atitinkamą [grąžinimo sandorių sąrašo puslapį](rebate-management-deals.md) tam sandorio tipui, su kuriuo norite dirbti.
1. Pasirinkite eilutę kiekvienam norimam apdoroti sandoriui (arba atidarykite norimą apdoroti sandorį).
1. Veiksmų srities skirtuko **Grąžinimų valdymo sandoriai** grupėje **Generuoti** pasirinkite vieną iš šių komandų:

    - **Apdoroti \> Nuostata** – nustatykite kiekvieno susijusio grąžinimo sandorio kaupimų rinkinį, tačiau neregistruokite jų. Šios meniu prekės negalima naudoti su sandoriais, kuriuose **Grąžinimo išeigos** laukas nustatytas kaip *Prekė*.
    - **Apdoroti \> Grąžinimo valdymas** – apdoroti operacijų seriją, pateikiančią kiekvieno sandorio grąžinimo vertę.
    - **Apdoroti \> Nurašyti** – apdorokite kiekvienos grąžinimo sandorio ir nurodyto laikotarpio šaltinio operacijos sumų, kurios buvo užregistruotos atidėjimui ir grąžinimo valdymui, nuokrypį. Šios meniu prekės negalima naudoti su sandoriais, kuriuose **Grąžinimo išeigos** laukas nustatytas kaip *Prekė*.

1. Pasirodžiusiame dialogo lange nustatykite laukus **Data nuo** ir **Data iki** skaičiavimo datos diapazonui apibrėžti.
1. Pasirinkite **Gerai** skaičiavimui vykdyti.

### <a name="process-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Vienos ar daugiau pasirinkto sandorio konkrečių eilučių apdorojimas

1. Atidarykite atitinkamą [grąžinimo sandorių sąrašo puslapį](rebate-management-deals.md) tam sandorio tipui, su kuriuo norite dirbti.
1. Atidarykite sandorį, iš kurio norite apdoroti eilutę.
1. Viršutiniame dešiniajame kampe pasirinkite skirtuką **Eilutės**.
1. „FastTab” **Grąžinimų valdymas** pasirinkite eilutę kiekvienai sandorio eilutei, kurią norite apdoroti.
1. „FastTab” **Grąžinimų valdymo** įrankių juostoje pasirinkite vieną iš šių komandų. (Šios komandos galimos tik tiems sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė*.)

    - **Apdoroti \> Nuostata** – nustatykite kiekvienos susijusios sandorio eilutės kaupimų rinkinį, tačiau neregistruokite jų. Šios meniu prekės negalima naudoti su sandoriais, kuriuose **Grąžinimo išeigos** laukas nustatytas kaip *Prekė*.
    - **Apdoroti \> Grąžinimo valdymas** – apdoroti operacijų seriją, pateikiančią kiekvieno sandorio eilutės grąžinimo vertę.
    - **Apdoroti \> Nurašyti** – apdorokite kiekvienos grąžinimo sandorio ir nurodyto laikotarpio šaltinio operacijos sumų, kurios buvo užregistruotos atidėjimui ir grąžinimo valdymui, nuokrypį. Šios meniu prekės negalima naudoti su sandoriais, kuriuose **Grąžinimo išeigos** laukas nustatytas kaip *Prekė*. 

1. Pasirodžiusiame dialogo lange nustatykite laukus **Data nuo** ir **Data iki** skaičiavimo datos diapazonui apibrėžti.
1. Pasirinkite **Gerai** skaičiavimui vykdyti.

### <a name="process-deals-using-a-batch-job"></a>Sandorių apdorojimas naudojant paketinę užduotį

Užuot apdoroję tam tikrus sandorius ar sandorio eilutes, galite vykdyti paketinę užduotį, skirtą kelių sandorių apdorojimui tuo pačiu metu. Galite pasirinktinai taikyti įrašų filtrus ir (arba) nustatyti pasikartojantį grafiką. Norėdami apdoroti sandorius naudojant paketinę užduotį, atlikite šiuos veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys \> Apdoroti \> Nuostata** tam kad nustatytumėte kiekvieno susijusio grąžinimo sandorio kaupimų rinkinį, tačiau neregistruokite jų.
    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys \> Apdoroti \> Grąžinimų valdymas** norėdami apdoroti operacijų seriją, pateikiančią kiekvieno sandorio eilutės grąžinimo vertę.
    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys \> Apdoroti \> Nurašyti** norėdami atšaukti anksčiau užregistruotas operacijas jų nurašymui tam, kad naujos grąžinimų sandorių operacijos galėtų būti suskaičiuotos.

1. Pasirodžiusio dialogo lango „FastTab” **Parametrai** skyriuje **Laikotarpis** nustatykite laukus **Data nuo** ir **Data iki** skaičiavimo operacijų datų diapazoną.
1. Skyriuje **Garantijos laikotarpis** nustatykite laukus **Data nuo** ir **Data iki** apskaičiuotinos garantijos datų diapazonui apibrėžti.
1. „FastTab” **Įtrauktini įrašai** galite nustatyti filtrus, kurie apribos paketinės užduoties apdorojamų sandorių rinkinį. Šie parametrai veikia taip pat, kaip ir kitiems paketinių užduočių tipams.
1. Jei reikia, „FastTab” **Vykdyti fone** galite nustatyti paketų apdorojimo ir planavimo parinktis. Šie parametrai veikia taip pat, kaip ir kitiems paketinių užduočių tipams.
1. Pasirinkite **Gerai** tam, kad būtų vykdomas ir (arba) planuojamas skaičiavimas.

## <a name="view-and-edit-rebate-management-transactions"></a>Grąžinimų valdymo operacijų peržiūra ir redagavimas

Kai apdorojate vieną ar daugiau sandorių, sistema sukuria operacijas, kurias galite peržiūrėti ir, galbūt, redaguoti prieš jas užregistruodami.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Pasirinkite sandorį, kuro operacijas norite peržiūrėti (pavyzdžiui, [**Visi grąžinimų valdymo sandoriai** puslapyje](rebate-management-deals.md)). Veiksmų srities skirtuko **Grąžinimų valdymo sandoriai** grupėje **Operacijos** pasirinkite **Operacijos** arba **Garantijos operacijos**, atsižvelgdami į norimos peržiūrėti operacijos tipą.
    - Atidarykite sandorį (pavyzdžiui, [**Visi grąžinimų valdymo sandoriai** puslapyje](rebate-management-deals.md)) jo išsamiai informacijai peržiūrėti. „FastTab” **Grąžinimų valdymas** pasirinkite sandorio eilutę, kurios operacijas norite peržiūrėti. Tada įrankių juostoje pasirinkite **Operacijos** arba **Garantijos operacijos**, atsižvelgdami į norimos peržiūrėti operacijos tipą. (Šie mygtukai galimi tik tiems sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė*.)

1. Rodomas **Grąžinimo valdymo datos operacijų** arba **Grąžinimo valdymo garantijos operacijų** puslapis. Jame yra tinklelis, kuriame kiekviena eilutė nurodo vieno grąžinimo arba vieno garantijos laikotarpio operacijų rinkinį. Pasirinkite eilutę tinklelyje ir tada veiksmų srityje pasirinkite **Paskirties operacijos** norėdami peržiūrėti tai eilutei priklausančias operacijas.
1. Pasirodžiusiame puslapyje pateikiamas pasirinkto tipo, priklausančio pasirinktai eilutei, operacijų sąrašas. Kiekviena operacija pateikia atitinkamą informaciją, priklausomai nuo operacijos tipo. Garantijos operacijoms galite peržiūrėti tik sąrašą. Kitų tipo operacijoms galite atlikti toliau pateiktus veiksmus šiame puslapyje:

    - Norėdami patvirtinti visų pareikalautų operacijų bendrą sumą puslapyje, peržiūrėkite lauką **Pareikalauta suma**.
    - Norėdami peržiūrėti daugiau informacijos apie bet kurią operaciją, pasirinkite ją, o tada pasirinkite **Bendra**, **Finansinė dimensija** arba **Dimensiją** skirtuką.
    - Norėdami peržiūrėti bet kuriuos taikomus sumažinimus veiksmų srityje pasirinkite **Mažinimo operacijos**. Daugiau informacijos rasite [Grąžinimų mažinimo principai](rebate-reduction-principle.md).
    - Norėdami pažymėti operacijas kaip pareikalautas arba nepareikalautas, jei naudojate pareikalavimų procesą, pasirinkite atitinkamas eilutes, o tada veiksmų srityje pasirinkite vieną iš šių komandų. (Pareikalavimų procesus įgalinate [**Grąžinimo valdymo parametrų** puslapyje](rebate-management-parameters.md) .)

        - **Nustatyti pareikalautas \> Visos** – pažymėti visas operacijas kaip pareikalautas.
        - **Nustatyti pareikalautas \> Pasirinktos** – pažymėti pasirinktas operacijas kaip pareikalautas.
        - **Nustatyti nepareikalautas \> Visos** – pažymėti visas operacijas kaip nepareikalautas.
        - **Nustatyti nepareikalautas \> Pasirinktos** – pažymėti pasirinktas operacijas kaip nepareikalautas.

    - Veiksmų srityje pasirinkite **Registruoti**, kad užregistruotumėte visų atitinkamų eilučių paraišką. Jei naudojate paraiškų procesą (kai parinktis **Naudoti paraiškų procesą** įjungta **Grąžinimų valdymo parametrų** puslapyje), registruojamos tik tos eilutės, kurios pažymėtos kaip **Pateikta**. Kitu atveju visos pasirinktos grąžinimo operacijos šaltinio operacijos yra užregistruojamos. **Registruoti** mygtukas galimas tik grąžinimo operacijoms. Jis negalimas parengimo ir nurašymo operacijoms. Dialogo lange **Registruoti** automatiškai nustatomi laukai **Data Nuo** ir **Data Iki**. Nustatykite lauką **Registravimo data** ir tada pasirinkite **Gerai**.
    - Norėdami koreguoti sumą, rodomą bet kuriai atvirai ar neužregistruotai operacijai, pasirinkite operaciją ir tada atlikite vieną iš šių veiksmų:

        - Redaguokite lauko **Pataisyta suma** vertę.
        - Veiksmų srityje pasirinkite **Nustatyti pataisymą**. Tada pasirodžiusiame išplečiamajame dialogo lango lauke **Pataisyta suma** įveskite vertę.

> [!NOTE]
> Jei naudojate paraiškų procesą, kai apdorosite kitą laikotarpį, operacijų sąraše bus visos nepareikalautos operacijos iš ankstesnio registravimo bei naujos pasirinkto laikotarpio operacijos.

## <a name="post-rebates-transactions"></a>Grąžinimų operacijų registravimas

Norėdami registruoti apdoroto parengimo, grąžinimo valdymo sumos ir nurašymo reikšmes, turite vykdyti registravimo procesą. Registravimo procesas pažymi parengimo, grąžinimo valdymo arba nurašymo operacijas kaip užregistruotas ir sukuria paskirties operaciją. Jeigu jums nereikia peržiūrėti paskirties operacijos, šias operacijas galima nustatyti taip, kad jos būtų registruojamos automatiškai.

### <a name="set-up-the-system-to-post-all-target-transactions-automatically"></a>Sistemos nustatymas registruoti visas paskirties operacijas automatiškai

Norėdami nustatyti savo sistemą užregistruoti visas paskirties operacijas iš kart jas sugeneravus užregistruojant parengimą, grąžinimo valdymo sumą ir nurašymą, įjunkite **Automatiškai registruoti žurnalus** ir (arba) **Automatiškai registruoti laisvos formos sąskaitos faktūras** parinktis puslapyje **Grąžinimų valdymo parametrai**. Daugiau informacijos rasite [Grąžinimų valdymo parametrai](rebate-management-parameters.md).

### <a name="post-transactions-for-all-lines-for-one-or-more-deals"></a>Vieno ar daugiau sandorių visų eilučių operacijų registravimas

Apdoroję aktualius sandorius, atlikite šiuos veiksmus, jei norite peržiūrėti ir užregistruoti sugeneruotas visų eilučių operacijas vienam ar daugiau sandorių.

1. Atidarykite atitinkamą [grąžinimo sandorių sąrašo puslapį](rebate-management-deals.md) tam sandorio tipui, su kuriuo norite dirbti.
1. Pasirinkite eilutę kiekvienam norimam registruoti sandoriui (arba atidarykite norimą registruoti sandorį).
1. Veiksmų srities skirtuko **Grąžinimų valdymo sandoriai** grupėje **Generuoti** pasirinkite vieną iš šių komandų:

    - **Registruoti \> Nuostata** – registruoti galimus sukurtų operacijų kaupimus.
    - **Registruoti \> Grąžinimų valdymas** – registruoti galimas sukurtas grąžinimų operacijas.
    - **Registruoti \> Nurašymas** – registruoti galimas sukurtas nurašymo operacijas.

1. Pasirodžiusiame dialogo lange nustatykite lauką **Registravimo data**. Tada nustatykite laukus **Data nuo** ir **Data iki** operacijų, kurios turi būti užregistruotos, datos diapazonui apibrėžti.
1. Pasirinkite **Gerai** operacijų registravimui.

### <a name="post-transactions-for-one-or-more-specific-deal-lines-for-a-selected-deal"></a>Vienos ar daugiau pasirinkto sandorio konkrečių eilučių operacijų registravimas

Apdoroję aktualius sandorius, atlikite šiuos veiksmus, jei norite peržiūrėti ir užregistruoti sugeneruotas vienos ar daugiau konkretaus sandorio eilučių operacijas pasirinktam sandoriui. Ši procedūra taikoma tik tiems sandoriams, kurių laukas **Derinti pagal** nustatytas į *Eilutė*.

1. Atidarykite atitinkamą [grąžinimo sandorių sąrašo puslapį](rebate-management-deals.md) tam sandorio tipui, su kuriuo norite dirbti.
1. Atidarykite sandorį, turintį eilutę, kurios operacijas norite registruoti.
1. Viršutiniame dešiniajame kampe pasirinkite skirtuką **Eilutės**.
1. „FastTab” **Grąžinimų valdymas** pasirinkite eilutę kiekvienai sandorio eilutei, kurią norite registruoti.
1. „FastTab” **Grąžinimų valdymo** įrankių juostoje pasirinkite vieną iš šių komandų. (Šios komandos galimos tik tiems sandoriams, kurių **Derinti pagal** nustatytas į *Eilutė*.)

    - **Registruoti \> Nuostata** – registruoti galimus sukurtų operacijų kaupimus.
    - **Registruoti \> Grąžinimų valdymas** – registruoti galimas sukurtas grąžinimų operacijas.
    - **Registruoti \> Nurašymas** – registruoti galimas sukurtas nurašymo operacijas.

1. Pasirodžiusiame dialogo lange nustatykite lauką **Registravimo data**. Tada nustatykite laukus **Data nuo** ir **Data iki** operacijų, kurios turi būti užregistruotos, datos diapazonui apibrėžti.
1. Pasirinkite **Gerai** operacijų registravimui.

### <a name="post-transactions-using-a-batch-job"></a>Operacijų registravimas naudojant paketinę užduotį

Užuot registravę tam tikrų sandorių ar sandorio eilučių operacijas, galite vykdyti paketinę užduotį, skirtą kelių sandorių operacijų registravimui tuo pačiu metu. Galite pasirinktinai taikyti įrašų filtrus ir (arba) nustatyti pasikartojantį grafiką. Norėdami registruoti operacijas naudojant paketinę užduotį, atlikite šiuos veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys\> Registruoti \> Nuostata**, jei norite registruoti pasiekiamas sukurtas kaupimų operacijas.
    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys\> Registruoti \> Grąžinimo valdymas**, jei norite registruoti pasiekiamas sukurtas grąžinimų operacijas.
    - Eikite į **Grąžinimų valdymas \> Periodinės užduotys\> Nurašyti \> Grąžinimo valdymas**, jei norite registruoti pasiekiamas sukurtas nurašymų operacijas.

1. Pasirodžiusio dialogo lango „FastTab” **Parametrai** skyriuje **Laikotarpis** nustatykite lauką **Registravimo data**. Tada nustatykite laukus **Data nuo** ir **Data iki** operacijų, kurios turi būti užregistruotos, datos diapazonui apibrėžti.
1. Skyriuje **Garantijos laikotarpis** nustatykite laukus **Data nuo** ir **Data iki** garantijų, kurios turi būti užregistruotos, datų diapazonui apibrėžti.
1. „FastTab” **Įtrauktini įrašai** galite nustatyti filtrus, kurie apribos paketinės užduoties apdorojamų sandorių rinkinį. Šie parametrai veikia taip pat, kaip ir kitiems paketinių užduočių tipams.
1. Jei reikia, „FastTab” **Vykdyti fone** galite nustatyti paketų apdorojimo ir planavimo parinktis. Šie parametrai veikia taip pat, kaip ir kitiems paketinių užduočių tipams.
1. Pasirinkite **Gerai** tam, kad būtų vykdomas ir (arba) planuojamas skaičiavimas.

## <a name="review-rebate-management-journals"></a>Grąžinimų valdymo žurnalų peržiūra

Užregistravę operacijas, galite peržiūrėti sukurtus žurnalus, dokumentus ar prekes. Grąžinimų ir autorinių honorarų paskirties operacijos yra pagrįstos mokėjimo registravimo šablone nustatytu mokėjimo tipu ir grąžinimo išeigos tipu. Pavyzdžiui, jei grąžinimo išvestis nustatyta kaip *Prekė*, kliento grąžinimo pardavimo užsakymas ir tiekėjo grąžinimo pirkimo užsakymas bus sukurti. Šiuos užsakymus galima peržiūrėti per paskirties operacijas. Kitu atveju, jei mokėjimas nustatytas naudoti mokėtinas sumas, bus sukurta kliento grąžinimų tiekėjo sąskaita faktūra nustatytam kliento tiekėjui.

Norėdami peržiūrėti žurnalo įrašus, susietus su grąžinimų valdymo sandoriu, atlikite šiuos veiksmus.

1. Atidarykite atitinkamą [grąžinimo sandorių sąrašo puslapį](rebate-management-deals.md) tam sandorio tipui, su kuriuo norite dirbti.
1. Pasirinkite sandorį, kuriam tikrinti žurnalo įrašus.
1. Veiksmų srities skirtuko **Grąžinimų valdymo sandoriai** grupėje **Operacijos** pasirinkite arba **Operacijos**, arba **Garantijos operacijos**, atsižvelgdami į norimos pažiūrėti operacijos tipą.
1. Įsitikinkite, kad laukas **Rodyti** nustatytas į *Visi* arba *Užregistruota*.
1. Raskite ir pasirinkite operacijų rinkinį, kurį norite patikrinti ir tada veiksmų srityje pasirinkite vieną iš toliau nurodytų mygtukų. (Šie mygtukai yra galimi tik tada, kai pasirinktame operacijų rinkinyje yra atitinkamų registravimų.)

    - **Paskirties operacijos** – peržiūrėti atitinkamus žurnalus ir kitų tipų dokumentus, sugeneruotus pasirinkto užsakymo.
    - **Prekės** – peržiūrėti atitinkamus pardavimo užsakymus arba pirkimo užsakymus, sugeneruotus pagal pasirinktą sandorį.

1. Pasirodo atitinkamų žurnalų, dokumentų ar prekių sąrašas. Norėdami peržiūrėti daugiau informacijos apie bet kurį žurnalą, dokumentą ar prekę, pasirinkite jo eilutę ir tada veiksmų srityje pasirinkite **Peržiūrėti informaciją**.
