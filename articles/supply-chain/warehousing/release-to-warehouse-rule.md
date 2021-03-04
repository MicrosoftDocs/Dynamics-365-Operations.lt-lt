---
title: Išleidimo į sandėlį taisyklė
description: Šioje temoje pateikiama informacija apie išleidimo į sandėlį taisyklę, suteikiančią lankstumo išleidimo į sandėlį metu. Jis prideda konfigūracijos parinktį, kontroliuojančią, ar sistema leidžia išleisti iš dalies rezervuotas užsakymo eilutes.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 27030e8dd58b290d80f6b00cbd250e09c1e50819
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433387"
---
# <a name="release-to-warehouse-rule"></a>Išleidimo į sandėlį taisyklė

[!include [banner](../includes/banner.md)]

Funkcija *Išleidimo į sandėlį taisyklė* suteikia lankstumo išleidimo į sandėlį metu. Ji prideda konfigūracijos parinktį kiekvienam sandėliui. Galite naudoti šią parinktį, norėdami nurodyti, ar iš dalies rezervuotas užsakymo eilutes galima išleisti į tą sandėlį. Priemonė veikia kartu su išplėstine prekių skirstymo funkcija tais atvejais, kai dalis užsakymo eilutės kiekio yra pažymėtas su tiekimo šaltiniu, tačiau likusiąją dalį galima apdoroti sandėlyje. Todėl eilutę galima išleisti taip, kad būtų galima tęsti pasiekiamo atsargų kiekio sandėlio apdorojimą.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Išleidimo į sandėlį taisyklės funkcijos įjungti ir inicijavimas

### <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Norėdami naudoti *Išleidimo į sandėlį taisyklės* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas:** *Išleidimo į sandėlį taisyklė*

### <a name="initialize-the-feature"></a>Funkcijos inicijavimas

Įjungę funkciją sistemoje, ją turite inicijuoti, kad taisyklė būtų nustatyta į tinkamą pradinę visų sandėlių būseną.

- Sandėlių, neįgalintų sandėlio valdymui, taisyklė iš pradžių nustatoma kaip **Netaikoma**.
- Sandėlių, įgalintų sandėlio valdymui, taisyklė iš pradžių nustatoma kaip **Leisti dalinę rezervaciją**

Norėdami inicijuoti funkciją ir nustatyti visų sandėlių išleidimo į sandėlį taisyklę, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**.
1. Puslapio **Sandėlio valdymo parametrai** skirtuke **Bendra** sekcijoje **Įmonės informacija** pasirinkite saitą į **Išleidimo į sandėlį inicijavimo** taisyklę. (Jei šis saitas nerodomas, funkcija yra neįjungta arba ji jau buvo inicijuota.)
1. Kai būsitė paraginti patvirtinti veiksmą, pasirinkite **Taip,** jei norite inicijuoti funkciją.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Nustatyti išleidimo į sandėlį taisyklę kiekvienam sandėliui

Po to, kai funkcija įjungta ir inicijuota, visi sandėliai turės pradinius nustatymus, kaip aprašyta ankstesniame skyriuje. Galite keisti šį nustatymą atskiriems sandėliams atlikdami šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Pasirinkti sandėlį konfigūravimui.
1. Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.
1. „FastTab“ skirtuko **Sandėlis** skyriuje **Rezervavimas** esantis laukas **Reikalavimai atsargų rezervavimui** kontroliuoja, ar leidžiama iš dalies išleisti užsakymus. Pasirinkite vieną iš šių reikšmių:

    - **Netaikoma** – kai funkcija pirmą kartą įjungiama ir inicijuota, ši reikšmė automatiškai priskiriama visiems sandėliams, neįgalintiems sandėlio valdymui. Jos negalima pakeisti. Ši vertė nėra taikoma sandėliams, įgalintiems sandėlių valdymui.
    - **Leisti dalinį rezervavimą** – užsakymai gali būti išleidžiami, kai rezervuotas bet koks kiekis. Sistema nustatys, ar nerezervuotas kiekis turėtų būti pažymėtas kaip išplėstiniame prekių skirstyme ir tą kiekį pažymės kaip reikiamą. Jei nebus žymėjimo, sistema sukurs darbą tik rezervuotam kiekiui. Kai funkcija pirmą kartą įjungiama ir inicijuota, ši reikšmė automatiškai priskiriama visiems sandėliams, įgalintiems sandėlio valdymui. Ši vertė nėra taikoma sandėliams, neįgalintiems sandėlio valdymui.
    - **Reikalauti visiško rezervavimo** – užsakymai gali būti išleidžiami tik jei visas kiekis yra rezervuotas. Jie negali būti išleisti, jei bendras kiekis nėra faktiškai rezervuotas arba numatytas prekių skirstyme. Ši vertė nėra taikoma sandėliams, neįgalintiems sandėlio valdymui.

1. Pasirinkite **Įrašyti**.

## <a name="scenarios"></a>Scenarijai

Šiame skyriuje pateikiami du scenarijai, kuriuos galite atlikti norėdami sužinoti, ką funkcija atlieka ir kaip ją naudoti.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šiuos scenarijus, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Taip pat galite naudoti šiuos scenarijus kaip vedlį, kaip naudotis funkcija dirbant gamybos sistemoje. Tačiau tokiu atveju, Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>1 scenarijus: reikalauti visiško paleidimo (nėra suplanuoto prekių skirstymo)

Šis scenarijus nurodo, kaip funkcija veikia sandėliams, kurie yra nustatyti **Reikalauti visiško rezervavimo**.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. Norėdami nustatyti _62_ sandėlį, nustatykite lauką **Atsargų rezervavimo reikalavimas** į **Reikalauti visiško rezervavimo**, kaip aprašyta ankstesniame šios temos skyriuje [Nustatyti išleidimo į sandėlį taisyklę kiekvienam sandėliui](#set-option-warehouse).
1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas** nustatykite lauką **Kliento paskyra** į _US–004_.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į _62_.

1. Pasirinkite **Gerai** naujam pardavimo užsakymui sukurti ir dialogo langui uždaryti.
1. Jūsų naujas pirkimo užsakymas yra atidarytas. Į jį įtraukta nauja tuščia eilutė, esanti skyriaus **Pardavimo užsakymo eilutės** tinklelyje. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *2*

1. Pasirinkite **Įtraukti eilutę** naujai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekės numeris:** *A0002*
    - **Kiekis:** *2*

1. Pasirinkite pirmą užsakymo eilutę ir tada meniu **Atsargos** virš tinklelio pasirinkite **Rezervavimas**.
1. Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Nerezervuokite antros užsakymo eilutės.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.
1. Atkreipkite dėmesį, kad gausite tokį klaidos pranešimą: „Visas kiekis turi būti faktiškai rezervuotas.“ Todėl sistema nesukuria jokio užsakymo darbo, siuntimo ar krovinio.

    > [!NOTE]
    > Jums bus parodytas tas pats klaidos pranešimas, jei iš dalies rezervuosite antrąją eilutę.

### <a name="scenario-2-allow-partial-release"></a>2 scenarijus: leisti dalinį išleidimą

Šis scenarijus parodo, kaip funkcija veikia sandėliams, kurie yra nustatyti **Leisti dalinį rezervavimą**.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Sandėliai**.
1. _62_ sandėlio lauką **Atsargų rezervavimo reikalavimas** nustatykite į **Leisti dalinį rezervavimą**, kaip aprašyta ankstesniame šios temos skyriuje [Nustatyti išleidimo į sandėlį taisyklę kiekvienam sandėliui](#set-option-warehouse).
1. Kaip ir [ankstesniame scenarijuje](#scenario1), eikite į **Pardavimai ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai** ir sukurkite pardavimo užsakymą kliento paskyrai _US-004_ iš sandėlio _62_. Įtraukite šias dvi užsakymo eilutes:

    - **1 eilutė:** Nustatykite lauką **Prekės numeris** į _A0001_, lauką **Kiekis** į _2_ ir **Vienetas** lauką į _vnt_.
    - **2 eilutė:** Nustatykite lauką **Prekės numeris** į _A0002_, lauką **Kiekis** į _2_ ir **Vienetas** lauką į _vnt_.

1. Kaip ir [ankstesniame scenarijuje](#scenario1), rezervuokite visą 1 užsakymo eilutės kiekį, bet nerezervuokite 2 užsakymo eilutės.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.
1. Atkreipkite dėmesį, kad šį kartą negausite klaidos pranešimo. Vietoj to sistema sukuria darbą, siuntas ir krovinius kaip reikalaujama ir pateikia rezultatus.
1. Norėdami peržiūrėti siuntos, krovinio ir darbo informaciją, naudokite parinktis virš tinklelio esančiame **Sandėlio** meniu:

    - **1 eilutė:** Galimos trys pasirinktys: **Išsami siuntos informacija**, **Išsami krovinio informacija** ir **Išsami darbo informacija**. Pasirinkite kiekvieną pasirinktį norėdami peržiūrėti išsamią informaciją apie siuntą, krovinį ir darbą, sukurtą, kai užsakymas buvo išleistas į sandėlį.
    - **2 eilutė:** galima tik **Darbo informacijos** parinktis. Pasirinkite ją ir atkreipkite dėmesį, kad nesukurtas joks darbas, nes atsargos nėra rezervuotos. Todėl siunta arba krovinys taip pat nebuvo sukurtas.

> [!NOTE]
> Toks pat rezultatas tikėtinas, kai antra eilutė yra rezervuota iš dalies. Šiuo atveju darbas bus sukurtas rezervuotam, o ne nerezervuotam eilutės kiekiui.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]