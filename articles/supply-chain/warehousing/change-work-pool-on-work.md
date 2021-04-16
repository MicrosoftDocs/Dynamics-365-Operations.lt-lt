---
title: Darbo telkinio keitimas
description: Šiame skyriuje paaiškinama, kaip galite naudoti darbo telkinio keitimo mygtuką darbo elementams tam, kad pakeistumėte esančios užduoties darbo telkinį.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: cdd0a1b6d022c958e00a1ba8fa87a8715ff88ce5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808899"
---
# <a name="change-work-pool-on-work"></a>Darbo telkinio keitimas

[!include [banner](../includes/banner.md)]

Galite naudoti darbo telkinius užduočių suskirstymui į grupes. Pavyzdžiui, galite sukurti darbo telkinį tam, kad klasifikuotumėte darbus, kurie pasirodo konkrečioje sandėlio vietoje.

*Darbo telkinio keitimas darbui* funkcija įtraukiama į **Darbo telkinio keitimo** mygtuką darbo elementų veiksmų juostoje. Dėl to, sandėlio vadovai gali lengvai keisti esančios užduoties darbo telkinį. Ši savybė leidžia vadovams greitai reaguoti į pokyčius ant sandėlio parduotuvės grindų ir padeda jiems pagerinti jų galimybes prisitaikyti prie besikeičiančių situacijų ir poreikio perduoti darbą kitam darbo baseinui.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Įjunkite darbo baseino keitimus darbo savybėse

Prieš pradėdami nustatyti ar naudoti šią savybę, privalote įsitikinti, kad ji yra prieinama jūsų sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Savybės pavadinimas:** *Keisti darbo baseiną darbe*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Nustatykite darbo baseino keitimus darbo savybėse

Šios savybės naudojimui, privalote turėti nustatytus keletą darbo baseinų. Galite taip pat nustatyti savo darbo šablonus taip, kad jie automatiškai priskirtų baseiną. Jei norite dirbti su pavyzdiniu scenarijumi, pateiktu šioje temoje, nustatykite sistemą, kaip aprašyta šiame skyriuje.

### <a name="set-up-work-pools"></a>Darbo baseinų nustatymas

Darbo baseinai leidžia jums tvarkyti darbo elementus pagal tipą. Darbui su *Darbo baseino keitimu savo darbe* funkcija, privalote turėti mažiausiai du prieinamus darbo baseinus. Darbo baseinų peržiūrai ir įtraukimui, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbas \> Darbo baseinai**.
1. Jei dirbate su demo duomenimis iš **USMF** bendrovės ir dirbsite vėliau su pavyzdiniu scenarijumi šioje temoje, įtraukite du darbo baseinus, kurie turi šiuos nustatymus:

    - Darbo baseinas 1:

        - **Darbo baseino identifikavimo kodas:** *Tinklo parduotuvė*
        - **Aprašas:** *Tinklo parduotuvė*

    - Darbo baseinas 2:

        - **Darbo baseino identifikavimo kodas:** *Skambučių centras*
        - **Aprašas:** *Skambučių centras*

1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-work-templates"></a>Nustatyti darbo šablonus

Kiekvienam iš savo darbo šablonų galite nustatyti kokį norite nustatytąjį darbo baseiną. Kiekvienam atitinkamam šablonui, priskiriate darbo baseiną **Darbo baseino identifikavimo kodo** stulpelyje. Šiuo atveju, visi darbo elementai sukurti naudojant duotą šabloną automatiškai paveldės priskirtą darbo baseiną. Jei dirbate su demo duomenimis iš **USMF** bendrovės ir dirbsite vėliau su pavyzdiniu scenarijumi šioje temoje, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Veiksmų juostoje pasirinkite **Redaguoti** tam, kad lange įjungtumėte redagavimo režimą.
1. Redaguokite šabloną nustatydami šias vertes:

    - **Darbo šablonas:** *62 Paėmimas pakavimui*
    - **Darbo baseino identifikavimo kodas:** *Tinklo parduotuvė*

1. Pasirinkite **Įrašyti**.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šis scenarijus rodo, kaip keisti esančio darbo elemento apdorojimo srautą keičiant jo darbo baseiną. Jis naudoja demo duomenis **USMF** bendrovėje ir nustatymus, kurie buvo pasiūlyti anksčiau šioje temoje.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Sukuria prekybos užsakymą ir išleidžia jį į sandėlį

1. Patvirtinkite, kad yra pakankamai turimo inventoriaus elementams *A0001* ir *A0002* sandėlyje *62*. Eikite į **Inventoriaus valdymas \> Užklausos ir ataskaitos \> Turimas sąrašas** ir redaguokite čia rodomus filtrus:

    - **Sandėlis** vertė prasideda su *62*.
    - **Elemento numerio** vertė yra *A001* arba *A002*.

    Demo duomenys turi turėti 10 vienetų kiekvieniems duomenims.

    Vėliau, privalote sukurti prekybos užsakymą.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-007*
    - **Sandėlis:** *62*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *2*

1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
1. Uždarykite puslapį.
1. **Prekybos užsakymo linijos** „FastTab“, pasirinkite **Įtraukti liniją** kitos linijos į savo prekybos užsakymą įtraukimui. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *2*

1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
1. Uždarykite puslapį.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą, kuriame rodomas bangos identifikavimo kodas ir siuntimo identifikavimo kodas, kurie buvo sukurti po išleidimo. Užsirašykite bangos identifikavimo kodą.

### <a name="review-the-outbound-wave"></a>Peržiūrėkite siunčiamą bangą

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Tinklelyje ieškokite bangos identifikavimo kodo, kuris buvo sukurtas iš prekybos užsakymo išleidimo.
1. Pasirinkite bangos identifikavimo kodą informacijos peržiūrai.
1. **Bangos linijos** „FastTab“, įsitikinkite, kad siuntimo identifikavimo kodas yra rodomas prekybos užsakyme.

    > [!TIP]
    > Jei **Bangos apdorojimas išleidimui į sandėlį** parinktis yra nustatyta ties *Ne* siuntimo bangos šablono nustatymu, privalote ranka apdoroti bangą pasirinkdami **Apdoroti** **Bangos** skirtuke veiksmų juostoje tam, kad sukurtumėte darbą.

1. Įsitikinkite, kad banga buvo apdorota. Šis apdorojimas sukuria reikiamą darbą.

### <a name="view-work-details-and-change-the-work-pool"></a>Peržiūrėkite darbo informaciją ir pakeiskite darbo baseiną

Galite naudoti **Darbo informacijos** puslapį tam, kad peržiūrėtumėte sukurtą darbą ir valdytumėte darbo baseiną.

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo išsami informacija**.
1. Pasirinkite ką tik sukurto darbo eilutę. **Užsakymo numerio** stulpelis rodys prekybos užsakymo numerį.

    **Darbo baseino identifikavimo kodo** laukelis bus nustatytas į darbo baseino identifikavimo kodą, kuris buvo nustatytas darbo šablone.

    > [!TIP]
    > Jei nematote **darbo baseino identifikavimo kodo** laukelio, įtraukite stulpelį į tinklelį ir vėliau perkraukite puslapį.

1. Tam, kad pakeistumėte darbo baseiną susietą su darbo identifikavimo kodu, veiksmų juostoje **Darbo** skirtuke pasirinkite **Keisti darbo baseino identifikavimo kodą**.
1. **Keisti darbo baseiną** teksto laukelyje, **Parametrų** „FastTab“, **Darbo baseino identifikavimo kodo** laukelyje, pasirinkite *Skambučių centras*.
1. Pasirinkite **Gerai** keitimo pritaikymui.
1. Atkreipkite dėmesį, kad **Darbo baseino identifikavimo kodo** laukelis dabar buvo pakeistas į *Skambučio centrą*.

> [!IMPORTANT]
> Kai **Darbo baseino keitimo** laukelis pasirodo, **Darbo baseino identifikavimo kodo** laukelis gali būti paliktas tuščias iš anksto. Jei laukelis yra tuščias, kai pasirenkate **Gerai** keitimų pritaikymui, tuomet visai pašalinsite darbo baseiną iš darbo.
>
> Kartu su darbo baseinų keitimu, galite naudoti šią procedūrą darbo baseino įtraukimui į bet kurį darbo elementą, kuris jo neturi arba darbo baseino pašalinimui iš bet kurio darbo elemento, kuris jį turi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]