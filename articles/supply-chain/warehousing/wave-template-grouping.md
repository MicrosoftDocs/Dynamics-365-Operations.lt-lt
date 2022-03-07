---
title: Bangos šablonų grupavimas
description: Bangos šablonų grupavimas leidžia sistemai naudoti bangos šablono nustatymus, kad remiantis Jūsų nustatytais kriterijais, būtų galima nuspręsti, kaip jis turi išskaidyti išleistas eilutes ir priskirti jas naujai ar esamai bangai. Ši funkcija gali būti naudinga tuose sandėliuose, kuriuose bangos kuriamos pagal tam tikrus kriterijus, bet valdytojai nori sukurti bangas automatiniu, o ne rankiniu būdu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: b265c0d5cb43e151386fe90e3a3dea414ec0aca6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579909"
---
# <a name="wave-template-grouping"></a>Bangos šablonų grupavimas

[!include [banner](../includes/banner.md)]

Bangos šablonų grupavimas leidžia sistemai naudoti [bangos šablono](tasks/configure-wave-processing.md) nustatymus, kad remiantis Jūsų nustatytais kriterijais, būtų galima nuspręsti, kaip jis turi išskaidyti išleistas eilutes ir priskirti jas naujai ar esamai bangai. Ši funkcija gali būti naudinga tuose sandėliuose, kuriuose bangos kuriamos pagal tam tikrus kriterijus, bet valdytojai nori sukurti bangas automatiniu, o ne rankiniu būdu. Tai leidžia sistemai pridėti kiekvieną naujai išleistą siuntą į pirmąją bangą, kuri suranda sutampančias grupavimo laukų vertes. Jei atitiktis nerandama, sistema naujai siuntai sukuria naują bangą.

> [!IMPORTANT]
> Bangos šablonų grupavimo nepalaikomo darbo tipai *Gamybos žaliavų paėmimas* ar " *„Kanban“ paėmimas*. Taip yra, nes bangos grupavimo pagrindas yra siuntos, o šie darbo tipai nenaudoja siuntų.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Bangos šablonų grupavimo funkcijos įjungimas

Norėdami naudoti *Bangos šablonų grupavimo* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Bangos šablonų grupavimas*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Nustatyti bangos šabloną, kad būtų galima naudoti bangos šablono grupavimą

Norėdami, kad būtų galima naudoti bangos šablono grupavimą, atlikite šiuos veiksmus nustatyti [bangos šablonui](tasks/configure-wave-processing.md).

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Bangos \> Bangų šablonai**.
1. Kairiojoje srityje pasirinkite nustatomą bangos šabloną. Jei ruošiatės dirbti pagal scenarijų, toliau pateiktą šioje temoje naudojant demonstracinius duomenis, pasirinkite **62 pristatymo numatytąjį** šabloną.
1. Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.
1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Automatizuoti bangos kūrimą:** *Taip*
    - **Priskirti atviroms bangoms:** *Taip*
    - **Apdoroti bangą išleidžiant ją į sandėlį** *Ne*

1. Veiksmų srityje pasirinkite **Redaguoti užklausą,** kad atidarytumėte užklausos dialogo langą.
1. Užklausos dialogo lango skirtuke **Rūšiavimas** peržiūrėkite rūšiavimo kriterijus ir įsitikinkite, kad yra taisyklė, apimanti lauką, kurį norite naudoti savo bangoms grupuoti.

    Jei ruošiatės dirbti pagal scenarijų naudojant demonstracinius duomenis, pridėkite eilutę, kurioje yra šios reikšmės:

    - **Lentelė:** *Siuntos*
    - **Išvestinė lentelė:** *Siuntos*
    - **Laukas:** *Vežėjo paslauga*

        > [!NOTE]
        > Pasirinkus šią reikšmę, gali būti parodytas šis pranešimas: „Vežėjo paslauga nėra indekso laukas. Ar norite įtraukti rūšiavimą?“ Pasirinkite **Taip** rūšiavimui įtraukti.

    - **Ieškos kryptis:** *Didėjanti*

1. Pasirinkite **Gerai**, kad išsaugotumėte pakeitimus ir uždarykite užklausos dialogo langą.
1. Veiksmų srityje pasirinkite **Bangos šablonų grupavimas**.
1. Puslapyje **Bangos šablonų grupavimas** pasirinkite **Grupuoti pagal** žymės langelį kiekvienai eilutei, kurią norite naudoti, kad būtų galima grupuoti užsakymų eilutes į bangą, kaip reikalinga. Jei ruošiatės dirbti per scenarijų naudojant demonstracinius duomenis, pasirinkite žymės langelį **Grupuoti pagal** *Vežėjo paslaugos* eilutėje.
1. Pasirinkite **Įrašyti**.
1. Uždarykite **Bangos šablono grupavimo** puslapį.
1. Pasirinkite **Įrašyti**, kad įrašytumėte šabloną.

## <a name="scenario"></a>Scenarijus

Šiame skyriuje pateikiamas planas, kuriuo vadovaujantis galite sužinoti, ką ši funkcija atlieka ir kaip ją naudoti.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Taip pat galite naudoti šią scenarijų kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje. Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.

### <a name="scenario-wave-template-grouping"></a>Scenarijus: Bangos šablonų grupavimas

Šis scenarijus parodo, kaip naudoti bangos šablonų grupavimą automatiniam kelių bangų sukūrimui, remiantis grupavimo kriterijais, apibrėžtais bangos šablone. Šiuo atveju bangos šablonas nustatomas sistemoje, kad būtų galima sukurti vieną bangą vienai vežėjo paslaugai.

Prieš pradėdami, paruoškite savo bangos šabloną, kaip aprašyta ankstesniame šios temos skyriuje [nustatyti bangos šabloną anksčiau šioje temoje naudoti bangos šablono grupavimo ](#set-up-template). Jei šiame scenarijuje dirbsite su demonstraciniais duomenimis, įsitikinkite, kad naudojate siūlomas šios procedūros demonstracines reikšmes. Šis nustatymas bangas sugrupuos pagal vežėjo paslaugą, nustatytą kiekvienam pardavimo užsakymui.

#### <a name="create-sales-order-1"></a>Pardavimo užsakymo 1 sukūrimas

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–004*.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.

1. Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.
1. Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje. Pasižymėkite pardavimo užsakymo numerį.
1. Perjunkite **Antraštės** rodinį.
1. „FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:

    - **Siuntos vežėjas:** *Oro transportas*
    - **Vežėjo paslauga:** *oro*

1. Grįžkite į **Eilučių** rodinį.
1. Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *2*

1. Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.
1. Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą. Pasižymėkite bangos ID ir siuntos ID numerius.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Peržiūrėkite bangą, kuri buvo sukurta iš pardavimo užsakymo 1

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangos ID, kuri buvo sukurta iš pardavimo užsakymo.
1. Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.
1. Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab“ skirtuką **Bangos eilutės**.

#### <a name="create-sales-order-2"></a>Pardavimo užsakymo 2 sukūrimas

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–005*.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.

1. Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.
1. Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje. Pasižymėkite pardavimo užsakymo numerį.
1. Perjunkite **Antraštės** rodinį.
1. „FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:

    - **Siuntimo vežėjas:** *„Flower moving“*
    - **Vežėjo paslauga:** *Std*

1. Grįžkite į **Eilučių** rodinį.
1. Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *1*

1. Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.
1. Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą. Pasižymėkite bangos ID ir siuntos ID numerius. Atkreipkite dėmesį, kad bangos ID skiriasi nuo pirmo pardavimo užsakymo bangos ID.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Peržiūrėkite bangą, kuri buvo sukurta iš pardavimo užsakymo 2

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangos ID, kuri buvo sukurta iš antrojo pardavimo užsakymo.
1. Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.
1. Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab“ skirtuką **Bangos eilutės**.

Buvo sukurta nauja šios siuntos banga, nes ji naudoja kitą vežėjo paslaugą nei pirmas pardavimo užsakymas.

#### <a name="create-sales-order-3"></a>Pardavimo užsakymo 3 sukūrimas

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–006*.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *62*.

1. Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir uždarykite **Kurti pardavimo užsakymą** dialogo langą.
1. Naujas pardavimo užsakymas atidaromas **Eilučių** rodinyje. Pasižymėkite pardavimo užsakymo numerį.
1. Perjunkite **Antraštės** rodinį.
1. „FastTab“ skirtuko **Pristatymas** dalyje **Transportavimas**, nustatykite šias vertes:

    - **Siuntos vežėjas:** *Oro transportas*
    - **Vežėjo paslauga:** *oro*

1. Grįžkite į **Eilučių** rodinį.
1. Dalyje **Pardavimo užsakymo eilutės** pasirinkite **Įtraukti eilutę,** kad įtrauktumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *1*

1. Pasirinkite naują užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.
1. Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** grupėje **Veiksmai** pasirinkite **Išleisti į sandėlį**.
1. Gausite informacinį pranešimą apie užsakymo siuntimą ir bangą. Pasižymėkite bangos ID ir siuntos ID numerius. Siunta buvo priskirta esamai bangai iš pirmojo pardavimo užsakymo.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Peržiūrėti 1 ir 3 pardavimų užsakymų bangas

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangos ID, kuri buvo sukurta iš trečiojo pardavimo užsakymo.
1. Pasirinkite bangos ID saitą, kad atidarytumėte puslapį Bangos išsami informacija.
1. Atkreipkite dėmesį, kad siunta buvo pridėta į „FastTab” skirtuką **Bangos eilutės** kartu su pirma pardavimo užsakymo siunta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]