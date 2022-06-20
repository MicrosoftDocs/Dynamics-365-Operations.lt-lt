---
title: Vietos nurodymo atsargų paėmimo skirstymas pagal terminus
description: Šiame straipsnyje paaiškinama, kaip išrinkimo metu naudoti "pirmasis į, pirmasis iš" (FIFO) ir "paskutinis į, pirmasis iš" (LIFO) vietos nustatymo strategijas.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 34ce119ca70596f0e40797c4b44a8fba4d5b7e0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885702"
---
# <a name="location-directive-inventory-picking-aging"></a>Vietos nurodymo atsargų paėmimo skirstymas pagal terminus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip išrinkimo metu naudoti "pirmasis į, pirmasis iš" (FIFO) ir "paskutinis į, pirmasis iš" (LIFO) vietos nustatymo strategijas. Šios strategijos dirba kartu su amžiaus duomenimis, kurie yra įrašyti į vietas sekimui, kai inventorius pirmąkart patenka į sandėlį. *Vietos direktyvos inventoriaus paėmimo amžiaus* savybė naudoja vietos duomenis tam, kad nustatytų amžių. *Sandėlio vietos būsenos* savybė atnaujina duomenis vietoje pagal duomenis iš licencijos numerio.

Galite naudoti FIFO ir LIFO strategijas tiek paketų sekamų elementų siuntimui, tiek ir nesupakuotų elementų sekimui pagal duomenis, kai inventorius patenka į sandėlį. Ši funkcija gali būti ypatingai naudinga nesupakuoto inventoriaus sekimui, kurio galiojimo data nėra prieinama rūšiavimo naudojimui.

Kai inventorius gaunamas pirmą kartą sandėlyje ar sukuriamas jame, sistema atnaujina atitinkamus licencijos numerius taip, kad esami duomenys būtų rodomi kaip amžiaus duomenys. Šie duomenys tuomet yra naudojami vietos direktyvos strategijoms, kurios nustato seniausią ir naujausią inventorių sandėlyje. Jei inventorius yra judinamas į vietą, kurios neseka licencijos numeris, vieta yra atnaujinama amžiaus informacija ir ši informacija vėliau naudojama strategijose.

## <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Šios savybės įjungimui, įjunkite tolesnes savybes [savybių valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)tokia tvarka:

1. Sandėlio vietos būsena
1. Vietos nurodymo atsargų paėmimo skirstymas pagal terminus

## <a name="feature-requirements"></a>Savybių reikalavimai

Šios savybės naudojimui, privalote nustatyti **Įjungti vietos būsenos** parinktį į *Taip* visiems [vietos profiliams](tasks/create-location-profile.md), kurie naudojami inventoriaus talpinimui. Šios parinkties vietos profilio nustatymui, eikite į **Sandėlio valdymas \> Sąranka \> Sandėlis \> Vietos profiliai** ir tuomet pasirinkite vietos profilį. Galite rasti parinktį **Bendri** „FastTab“.

## <a name="feature-scenarios"></a>Savybių scenarijai

Šiame skyriuje pateikti pavyzdžiai rodantys, kaip nustatyti ir naudoti FIFO ir LIFO strategijas.

> [!TIP]
> Šiame skyriuje pateikti du scenarijai, vienas FIFO ir vienas LIFO. Procedūros pateikiamos su sąlyga, kad jūs naudosite abu scenarijus tinkama tvarka. Rekomenduojame naudoti abu scenarijus, nes galėsite suprasti skirtumus tarp abiejų strategijų.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šiuos scenarijus, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį subjektą prieš pradedant.

Galite taip pat naudoti šiuos scenarijus kaip gaires savybės gamybos sistemoje naudojimui. Nepaisant to, tokiu atveju, turėsite pakeisti savo vertes kiekvienam šiame dokumente aprašytam nustatymui.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Scenarijų nustatymas

Demonstraciniai duomenys reikalauja nustatymo ir inventoriaus pakeitimų tam, kad palaikytų scenarijus. Atlikite šiuos žingsnius inventoriaus duomenų sukūrimui, kurie būtini dirbant su FIFO ir LIFO scenarijais.

1. Prisijunkite prie sistemos, kai demonstraciniai duomenys yra įdiegti ir pasirinkite **USMF** juridinį subjektą.
1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlis \> Vietos profiliai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Vietų profilių sąraše, pasirinkite **FLOOR-05**.
1. **Bendra** „FastTab“, nustatykite **Įjungti vietos būsenos** parinktį į *Taip*.
1. Pasirinkite **Įrašyti**.
1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Vietų profilių direktyvoje, pasirinkite **63 talpinimo į talpyklas pasirinkimas**.
1. Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.
1. **Vietos direktyvos veiksmų** „FastTab“, raskite eilutę, kurioje **Sekos numerio** laukelis yra nustatytas į *1* ir atlikite šiuos veiksmus:

    - Jei nustatote FIFO scenarijų, pakeiskite **Strategijos** laukelio vertę į *FIFO vietos amžius*.
    - Jei nustatote LIFO scenarijų, pakeiskite **Strategijos** laukelio vertę į *LIFO vietos amžius*.

1. **Vietos direktyvos veiksmų** „FastTab“, pasirinkite **Redaguoti užklausą**.
1. Užklausos teksto laukelyje, **Intervalas** skirtuke, pasirinkite **Įtraukti** eilutės įtraukimui ir tuomet nustatykite šias vertes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Zonos ID*
    - **Kriterijai:** *Grindys*

1. Pasirinkite **Gerai** tam, kad pritaikytumėte savo nustatymus uždarytumėte teksto laukelį.
1. Pasirinkite **Įrašyti** tam, kad išsaugotumėte pakeitimus vietos direktyvoje.
1. Mobiliame įrenginyje arba „*Dynamics 365 for Finance and Operations“ – Sandėliavimas* programoje savo kompiuteryje atlikite šiuos žingsnius ir pašalinkite esantį inventorių iš sandėlio vietos tam, kad palaikytumėte scenarijus:

    1. Prisijunkite prie sandėlio *63* naudodami būtiną vartotojo identifikavimo kodą ir slaptažodį.
    1. Pagrindiniame meniu pasirinkite **Kokybė**.
    1. **Kokybės valdymas** meniu pasirinkite **Išmesti**.
    1. **Išmesti** puslapyje pasirinkite **LOC/LP** laukelį ir tuomet įveskite *63\_1*.
    1. Pasirinkite **Įvesti** arba **Gerai**.
    1. Patvirtinkite **Išmesti** informaciją **Reguliavimui išorėje** pasirinkdami **Įvesti** arba **Gerai**.

    Kai licencijos numerio inventorius yra sureguliuotas išorėje, gausite pranešimą „Darbas baigtas“.

    Šie žingsniai palieka inventorių dvejose demonstracijos duomenų vietose. Visos vietos turi skirtingus amžiaus duomenis. Vieta *FL-001* turi amžiaus duomenis pradedant 2017 m. balandžio 15 d. ir vieta *FL-002* turi amžiaus duomenis pradedant 2017 m. sausio 29 d. Abi vietos turi elementą *A0001*.

    Šių duomenų peržiūrai eikite į **Inventoriaus valdymas \> Užklausos ir ataskaitos \> Esamas sąrašas** ir tuomet filtruokite sandėlį *63* ir elementą *A0001*. Eilutėse, kuriose **Vietos** laukas nustatytas į *FL-001* ar *FL-002*, pasirinkite eilutę su teigiama **Fizinio inventoriaus** verte ir tuomet veiksmų juostoje pasirinkite **Pervedimai**. **Fiziniai duomenys** laukelyje bus rodomi duomenis atitinkantys vieną iš prieš tai paminėtų amžiaus duomenų.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Scenarijus 1: Nustatykite ir naudokite FIFO vietos amžių

FIFO strategija suranda vietą, turinčią seniausius amžiaus duomenis ir priskiria paėmimą pagal tuos amžiaus duomenis.

1. Jei taip dar nepadarėte, [paruoškite pavyzdinius duomenis](#demo-set-up), kurių reikia šiame scenarijuje.
1. Eikite į **Prekyba ir komercija \> Prekybos užsakymas \> Visi prekybos užsakymai**.
1. Pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į *US–001*.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į *63*.

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jie apima naują, tuščią eilutę tinklelyje **Prekybos užsakymo eilutės** „FastTab“. Šiai užsakymo eilutei, nustatykite **Elemento numerio** laukelį į *A0001* ir **Kokybės** laukelį į *1*.
1. Virš tinklelio esančiame meniu **Atsargos** pasirinkite **Rezervavimas**.
1. **Rezervavimo** puslapyje, pasirinkite **Rezervuoti vietą** tam, kad rezervuotumėte užsakytą kiekį šiam elementui iš pasirinktame sandėlyje esančio inventoriaus.
1. Uždarykite **Rezervavimas** puslapį.
1. **Prekybos užsakymo** puslapyje, veiksmų juostoje **Sandėlio** skirtuke, **Veiksmai** grupėje, pasirinkite **Paleisti į sandėlį**. Gausite informacinį pranešimą. Sistema sukuria siuntą, įtraukia ją į naują krovinį ir sukuria reikiamą darbo užduotį.
1. **Prekybos užsakymo eilučių** „FastTab“,  **Sandėlio** meniu, pasirinkite **Darbo informacija** tam, kad atidarytumėte šiam prekybos užsakymui sukurtą darbą. Atkreipkite dėmesį, kad eilutė, kurioje **Darbo tipo** vertė yra *Paimti*, rodo **Vietos** vertę *FL-002*. Ši vieta apima licencijos numerį, kuris turi seniausius amžiaus duomenis (FIFO).
1. Pasirinkite **Sandėlis \> Siuntimo informacija**.
1. „FastTab“ **Bendra** užsirašykite bangos identifikavimo numerį, kad galėtumėte jį naudoji scenarijaus 2 metu.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Scenarijus 2: Nustatykite ir naudokite LIFO vietos amžių

LIFO strategija suranda vietą, turinčią naujausius amžiaus duomenis ir priskiria paėmimą pagal tuos amžiaus duomenis. Scenarijuje 2 redaguosite scenarijaus 1 (FIFO) nustatymus ir naudosite dar kartą prekybos užsakymą ir bangą, kurie buvo sukurti scenarijaus metu.

1. Prieš pradėdami šį scenarijų, nustatykite ir užbaikite visą FIFO scenarijų kaip aprašyta [ankstesniame skyriuje](#fifo-demo). Šiame scenarijuje dar kartą naudosite bangą ir didžiąją dalį nustatymų, kurie buvo sukurti šiam scenarijui.
1. Redaguokite **63 Paėmimo talpinimo į talpyklas** vietos direktyvą taip, kad ji naudotų *Vietos amžiaus LIFO* strategiją, kaip aprašyta pirmojoje [Scenarijų nustatymo](#demo-set-up) dalies procedūroje.

    Po to, keisite bangą, kuri buvo sukurta prekybos užsakymui scenarijuje 1 tam, kad ji naudotų *Vietos amžiaus LIFO* strategiją.

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite ir atidarykite bangą turinčia užsakymą, kurį sukūrėte FIFO scenarijui.
1. Veiksmų juostoje, **Darbas** skirtuke, pasirinkite **Atšaukti** tam, kad atšauktumėte jūsų FIFO scenarijuje sukurtą darbą.
1. Veiksmų srities skirtuke **Banga**, grupėje **Banga** pasirinkite **Vykdyti**.
1. Kai apdorojimas yra baigtas, veiksmų juostoje, **Bangos** skirtuke, **Susijusios informacijos** grupėje, pasirinkite **Darbas** tam, kad atidarytumėte šiai bangą sukurtą darbą.
1. **Darbo** puslapyje, **Peržiūros** skirtuke, turėtų būti dvi eilutės. Pasirinkite eilutę, kurioje **Darbo būsenos** laukelis nustatytas į *Atvirą*.
1. Atkreipkite dėmesį, kad eilutė, kurioje **Darbo tipo** vertė yra *Paimti*, rodo **Vietos** vertę *FL-001*. Ši vieta apima licencijos numerį, kuris turi naujausius amžiaus duomenis (LIFO).

Šiuose scenarijuose, jūs matėte, kaip vietos amžiaus strategija valdo darbą inventoriaus vietoje, kuri turi seniausią arba naujausią inventorių priklausomai nuo pasirinktos strategijos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]