---
title: Papildymo pagal zoną ribinės vertės
description: Pagal zoną paremtas papildymas naudoja minimalių / maksimalių (min. / maks.) verčių papildymo strategiją, įvertinančią visas sandėlio zonas, o ne tik atskiras vietas. Todėl sandėlio vadovai gali greičiau sužinoti, kada paėmimų zonose reikia papildomų atsargų.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: e3ec1f59e0b1d202d5591bfc1525c9034f4d8f45
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893126"
---
# <a name="zone-threshold-replenishment"></a>Papildymo pagal zoną ribinės vertės

[!include [banner](../includes/banner.md)]

Pagal zoną paremtas papildymas naudoja minimalių/maksimalių (min/max) verčių [papildymo](replenishment.md) strategiją, įvertinančią visas sandėlio zonas, o ne tik atskiras vietas. Todėl sandėlio vadovai gali greičiau sužinoti, kada paėmimų zonose reikia papildomų atsargų.

Šios funkcijos nustatymas yra panašus į vieta pagrįsto papildymo nustatymus. Tačiau, kai nustatote min. / maks. papildymo šabloną, taip pat galite nurodyti, ar ribinė vertė turi būti vertinama pagal vietą arba pagal zoną. Jei nustatote vertinimą, paremtą zonomis, turite pridėti konkrečias zonas prie srities parinkties užklausos.

Kaip ir vieta pagrįstas min. / maks. papildymo, zonomis pagrįsto min. / maks. papildymo pagrindas yra minimalios atsargų ribinės vertės nustatymas, kuris sukuria pažymėtų prekių papildymo darbo kūrimą. Šis papildymo darbas padidins atsargas iki nurodytos maksimalios ribos zonai.

> [!NOTE]
> Zonomis pagrįsto papildymo procesai nėra palaikomi produktų variantams dabartiniame leidime.


Skirtingai nei vieta pagrįstame min. / maks. papildyme, zona pagrįstame min. / maks. papildyme nereikia fiksuoti vietų, siekiant įvertinti, ar jos turi saugoti konkrečią prekę. Todėl, zona pagrįstame papildyme galima naudoti min. / maks. papildymą, net jei neužfiksavote vietos kiekvienai prekei ar prekės variantui sandėlyje. Kai zonoje esantis kiekis yra mažesnis už nurodytą minimalią ribinę vertę, sukuriamas papildymo darbas. Vietos nustatymo nurodymuose bus nustatoma, konkreti vieta, į kurią reikia padėti atsargas.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Papildymo pagal zoną ribinės vertės įjungimo funkcija

Norėdami naudoti *Papildymo pagal zoną ribinės vertės* funkciją, įjunkite ją savo sistemoje. Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *sandėlio valdymas*
- **Funkcijos pavadinimas** *Papildymo pagal zoną ribinės vertės*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Nustatyti papildymą pagal zoną

Norėdami zona pagrįstą papildymą, turite sukonfigūruoti kelias sistemos dalis. Šiame skyriuje pristatyti įvairūs parametrai ir pateikti demonstracinių duomenų vertės, kurias galite įvesti, jei norite dirbti su scenarijumi šio straipsnio pabaigoje.

### <a name="set-up-directive-codes"></a>Vietos nurodymų nustatymas

[Vietos nurodymai](control-warehouse-location-directives.md) leidžia tiksliau nustatyti vietos šabloną, naudojamą darbo šablone. Kiekvienas kodas nustato bendrąją vertę, kurią galite nurodyti konfigūruodami kiekvieną šablono tipą.

#### <a name="view-and-edit-directive-codes"></a>Peržiūrėti ir redaguoti nurodymo kodus

Norėdami peržiūrėti arba redaguoti savo nurodymų kodus, eikite į **Sandėlio valdymas \> Nustatymai \> Nurodymų kodai**.

#### <a name="prepare-demo-data-directive-codes"></a>Nurodymo kodų parodomųjų duomenų paruošimas

Šis pavyzdys parodo, kaip paruošti nurodymo kodą. Jei šio straipsnio pabaigoje planuojate naudoti scenarijų, naudokite čia pateiktas parodomąsias duomenų vertes. Kitu atveju naudokite savo vertes.

1. Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.
1. Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Nurodymo kodas:** _Zone replen_
    - **Nurodymo aprašas:** _Papildymas pagal zoną_

1. Pasirinkite **Įrašyti**, kad įrašytumėte naują kodą.

### <a name="set-up-replenishment-templates"></a>Nustatyti papildymo šablonus

[Min. / maks. papildymo šablonai](tasks/set-up-min-max-replenishment-process.md) yra pagrindinis mechanizmas, skirtas palaikyti optimalų prekių kiekį paėmimo vietose. Šiuose šablonuose turite nustatyti taisykles, kurios bus naudojamos atsargoms papildyti sandėlyje. Papildymas, kurį galima naudoti šablonuose, apima zona pagrįstą papildymą.

#### <a name="view-and-edit-replenishment-templates"></a>Peržiūrėti ir redaguoti papildymo šablonus

Papildymo šablonas yra taisyklės, kuriomis remiantis kontroliuojama, kada ir kaip vietos yra papildomos. Pasirinkite šabloną kontroliuoti, kada ir kaip bus vykdomas papildymas. Papildymo šablonų peržiūrai ir redagavimui eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Paruošti demonstracinius duomenis papildymo šablone

Šis pavyzdys parodo, kaip paruošti papildymo šabloną. Jei šio straipsnio pabaigoje planuojate naudoti scenarijų, naudokite čia pateiktas parodomąsias duomenų vertes. Kitu atveju naudokite savo vertes.

1. Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.
1. Eikite į **Sandėlio valdymas \> Nustatymas \> Papildymas \> Papildymo šablonai**.
1. Pasirinkite **Redaguoti,** kad pakeistumėte puslapio režimą į redagavimo.
1. Veiksmų srityje pasirinkite **Nauja,** kad pridėtumėte eilutę į **Peržiūros** tinklelį.
1. Naujoje eilutėje nustatykite šias vertes. Priimkite numatytąsias vertes visuose kituose laukuose.

    - **Papildyti šabloną:** _Zone min/maks replen_
    - **Aprašas:** _Zonos min. / maks. papildymas_
    - **Papildymo tipas:** _Minimalus arba maksimalus_

1. Pasirinkite **Įrašyti**.
1. Kol nauja eilutė vis dar pasirenkama **Peržiūros** tinklelyje, pasirinkite **Naujas** virš **Papildymo šablono informacija,** kad pridėtumėte eilutę, susijusią su jau sukurtu *Zone Min/Max replen* papildymo šablonu.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Sekos numeris:** Įveskite _1_.
    - **Aprašas:** Įveskite _Paėmimo zonos papildymas_.
    - **Papildymo vienetas:** Pasirinkite _EA_.
    - **Užklausos tipas** – palikite šį lauką tuščią.
    - **Nurodymo kodas:** Šis laukas susieja papildymo šabloną su vietos nurodymu. Pasirinkite demonstracinių duomenų nuorodos kodą, kurį sukūrėte anksčiau (_Zone replen_).
    - **Darbo šablonas** – Palikite šį lauką tuščią.
    - **Minimalus kiekis:** Šis laukas nustato kiekį, kuris suaktyvins papildymą. Įveskite _50_.
    - **Maksimalus kiekis:** Šis laukas nustato maksimalų prekės kiekį, kurį galima pristatyti zonoje. Sugeneruotas papildymo darbas padidins atsargų kiekį. Įveskite _150_.
    - **Vienetas:** Šis laukas nustato minimalių ir maksimalių verčių vienetą. Pasirinkite _EA_.
    - **Paklausos padidėjimas:** pasirinkite _Apvalinti_.
    - **Papildyti tuščias fiksuotas vietas:** pasirinkite šį žymės langelį.
    - **Papildyti tik fiksuotas vietas:** išvalykite šį žymės langelį.
    - **Produkto užklausos režimas:** Pasirinkite _Produkto užklausa_.
    - **Papildymo ribinės vertės aprėptis:** Šis laukas nurodo, ar šablonas turėtų būti įvertintas pagal zoną, ar pagal konkrečią vietą. Pasirinkite _Zone_.
    - **Sandėlis:** Pasirinkite _61_.

1. Pasirinkite **Pasirinkit produktus** virš **Papildymo šablono informacijos** tinklelio.
1. Dialogo lango **Produkto užklausa** skirtuke **Diapazonas** pasirinkite **Pridėti** eilutei pridėti į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** _Prekės_
    - **Išvestinė lentelė:** _Prekės_
    - **Laukas:** _Prekės numeris_
    - **Kriterijai:** _A0001_

1. Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.
1. Pasirinkite **Pasirinkit papildymo produktus** virš **Papildymo šablono informacijos** tinklelio.
1. Dialogo lango **Zonos užklausa** skirtuke **Diapazonas** pridėkite eilutei į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** _Sandėlio zona_
    - **Išvestinė lentelė:** _Sandėlio zona_
    - **Laukas:** _Zonos ID_
    - **Kriterijai:** _AUKŠTAS_

1. Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.

### <a name="set-up-location-directives"></a>Nustatyti vietos nurodymus

Skirtingai nei vieta pagrįstas min. / maks. papildymas, zona pagrįstas min. / maks. papildyme, reikia nustatyti tiek paėmimo, tiek padėjimo vietos direktyvas, nes sistema įvertina visą zoną, o ne tik vieną paėmimo vietą siuntimo darbui.

#### <a name="view-and-edit-location-directives"></a>Peržiūrėti ir redaguoti vietos nurodymus

Norėdami peržiūrėti arba redaguoti vietos nurodymus, eikite į **Sandėlio valdymas \> Nustatymai \> Vietos nurodymai**.

Pavyzdžiai, kuriais rodoma, kaip naudoti nustatymus siekiant sukurti reikiamos paėmimo vietos nurodymus ir nustatyti vietos nurodymus, pateikiami kitame skyriuje.

#### <a name="prepare-demo-data-location-directives"></a>Vietos nurodymo demonstracinių duomenų paruošimas

Norėdami paruošti demonstracinius duomenis, kad juos būtų galima naudoti šio straipsnio pabaigoje naudojamame scenarijuje, turite sukurti dvi vietos nurodymus: vieną paėmimui ir vieną – padėti.

##### <a name="create-a-replenishment-pick-directive"></a>Papildymo paėmimo vietos nurodymo kūrimas

1. Pasirinkite **USMF** juridinį subjektą dirbti su demonstraciniais duomenimis.
1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairinės srities lauką **Darbo užsakymo tipas** nustatykite į _Papildymas_.
1. Veiksmų srityje pasirinkite **Nauja** naujam nurodymui sukurti.
1. Nustatykite toliau nurodytas reikšmes.

    - **Sekos numeris:** Priimkite numatytąją vertę.
    - **Pavadinimas:** Įvesti _Zonos paėmimas_.
    - **Darbo tipas:** pasirinkite _Paėmimas_.
    - **Saitas** Pasirinkite _6_.
    - **Sandėlis:** Pasirinkite _61_.
    - **Nurodymo kodas:** Palikite šį lauką tuščią.
    - **Keli SKU:** Nustatykite šią pasirinktį į _Ne_.

1. Pasirinkite **įrašyti,** kad būtų kuriama nuoroda su parametrais, kuriuos sukonfigūravote iki šiol.
1. „FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Sekos numeris:** Įveskite _1_.
    - **Kiekis Nuo** įveskite _0_.
    - **Kiekis Iki:** įveskite _10000000_.
    - **Vienetas:** lauką palikite tuščią.
    - **Rasti kiekį:** Pasirinkite _Nėra_.
    - **Riboti pagal vienetą:** išvalykite šį žymės langelį.
    - **Apvalinti iki vieneto:** išvalykite šį žymės langelį.
    - **Rasti pakavimo kiekį:** Išvalykite šį žymės langelį.
    - **Leisti skaidyti:** pasirinkite šį žymės langelį.

1. Pasirinkite **Įrašyti** naujai eilutei įrašyti.
1. Kol jūsų nauja eilutė vis dar pasirenkama **Eilučių** tinklelyje, pasirinkite **Naujas** „FastTab“ **Vietos nurodymų veiksmai** eilutei įtraukti į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Sekos numeris:** Įveskite _1_.
    - **Pavadinimas:** Įveskite _Paėmimas iš krovinio_.
    - **Fiksuotos vietos naudojimas:** Pasirinkite _Fiksuotos ir nefiksuotos vietos_.
    - **Leisti neigiamas atsargas:** Išvalykite šį žymės langelį.
    - **Paketas įgalintas:** Išvalykite šį žymės langelį.
    - **Strategija:** Pasirinkite _Nėra_.

1. Pasirinkite **Įrašyti** naujam veiksmui įrašyti.
1. Kol vis dar pasirinktas naujas veiksmas, virš **Vietos nurodymų veiksmų tinklelio** pasirinkite **Redaguoti užklausą**.
1. Atsiranda užklausos dialogo langas, kuriame galite pasirinkti vietas, kurias norite papildyti. Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** _Vietos_
    - **Išvestinė lentelė:** _Vietos_
    - **Laukas:** _Zonos ID_
    - **Kriterijai:** _BULK_

1. Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.
1. Pasirinkite **Įrašyti**, kad įrašytumėte vietos nurodymą.

##### <a name="create-a-replenishment-put-directive"></a>Papildymo padėjimo vietos nurodymo kūrimas

1. Įsitikinkite, kas puslapio **Vietos nurodymai** kairiojoje srityje laukas **Darbo užsakymo tipas** vis dar nustatytas kaip _Papildymas_.
1. Veiksmų srityje pasirinkite **Nauja** kitam nurodymui sukurti.
1. Nustatykite toliau nurodytas reikšmes.

    - **Sekos numeris:** Priimkite numatytąją vertę.
    - **Pavadinimas:** Įvesti _Zonos padėjimas_.
    - **Darbo užsakymo tipas:** pasirinkite _Padėjimas_.
    - **Saitas:** Pasirinkite _6_.
    - **Sandėlis:** Pasirinkite _61_.
    - **Nurodymo kodas:** Pasirinkite _Zone replen_ norėdami susieti šį vietos nurodymo su papildymo šablonu, kuris buvo sukurtas anksčiau, naudojant anksčiau sukurtą kodą.
    - **Keli SKU:** Nustatykite šią pasirinktį į _Ne_.

1. Pasirinkite **įrašyti,** kad būtų kuriama nuoroda su parametrais, kuriuos sukonfigūravote iki šiol.
1. „FastTab“ skirtuke **Eilutės** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Sekos numeris:** Įveskite _1_.
    - **Kiekis Nuo** įveskite _0_.
    - **Kiekis Iki:** įveskite _10000000_.
    - **Vienetas:** lauką palikite tuščią.
    - **Rasti kiekį:** Pasirinkite _Nėra_.
    - **Riboti pagal vienetą:** išvalykite šį žymės langelį.
    - **Apvalinti iki vieneto:** išvalykite šį žymės langelį.
    - **Rasti pakavimo kiekį:** Išvalykite šį žymės langelį.
    - **Leisti skaidyti:** pasirinkite šį žymės langelį.

1. Pasirinkite **Įrašyti** naujai eilutei įrašyti.
1. Kol jūsų nauja eilutė vis dar pasirenkama **Eilučių** tinklelyje, pasirinkite **Naujas** „FastTab“ **Vietos nurodymų veiksmai** eilutei įtraukti į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Sekos numeris:** Įveskite _1_.
    - **Pavadinimas:** Įvesti _Zonos padėjimas_.
    - **Fiksuotos vietos naudojimas:** Pasirinkite _Fiksuotos ir nefiksuotos vietos_.
    - **Leisti neigiamas atsargas:** Išvalykite šį žymės langelį.
    - **Paketas įgalintas:** Išvalykite šį žymės langelį.
    - **Strategija:** Pasirinkti _Konsolidavimas_.

1. Pasirinkite **Įrašyti** naujam veiksmui įrašyti.
1. Kol vis dar pasirenkamas naujas veiksmas, pasirinkite **Redaguoti užklausą** virš **Vietos nurodymų veiksmų** tinklelio.
1. Atsiranda užklausos dialogo langas, kuriame galite pasirinkti zonas, kurias norite papildyti. Ši zona turi būti ta pati zona, kuri nurodyta papildymo šablone. Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias vertes:

    - **Lentelė:** _Vietos_
    - **Išvestinė lentelė:** _Vietos_
    - **Laukas:** _Zonos ID_
    - **Kriterijai:** _AUKŠTAS_

1. Pasirinkite **Gerai**, kad įrašytumėte jūsų užklausą ir uždarytumėte dialogo langą.
1. Pasirinkite **Įrašyti**, kad įrašytumėte vietos nurodymą.

## <a name="scenario"></a>Scenarijus

Šiame skyriuje pateikiamas pavyzdinis scenarijus, rodantis, kaip dirbti su funkcija.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Paruošti pavyzdinius duomenis, reikalingus pavyzdžio scenarijui

Prieš pradėdami dirbti su scenarijumi, turite suaktyvinti duomenų pavyzdžius ir nustatyti funkciją, kaip aprašyta šiame skyriuje ir ankstesniuose šio straipsnio skyriuose.

#### <a name="use-the-usmf-legal-entity"></a>Naudokite USMF juridinį subjektą

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

#### <a name="prepare-additional-sample-data"></a>Paruošti papildomus pavyzdžio duomenis

Pasirinkę USMF **juridinį** subjektą, įtraukite papildomą pavyzdžio duomenis, kurie yra būtini, [kaip](#setup) aprašyta anksčiau šiame straipsnyje skyriuje Nustatyti zoną pagrįstą papildymą.

#### <a name="check-your-on-hand-inventory"></a>Turimų atsargų patikrinimas

Atlikite šiuos veiksmus, norėdami įsitikinti, kad jūsų sistemoje yra pakankamai atsargų, kad būtų įvykdomas pavyzdinis scenarijus.

1. Įsitikinkite, kad yra prekės *A0001* turimos atsargos, esančios dvejose skirtingose paėmimo zonos (*AUKŠTAS*) vietose, yra nurodytos papildymo šablone. Tačiau bendroji atsargų suma turėtų būti mažesnė nei būtinas minimalus kiekis (*50*), nurodytas papildymo šablone. Tokiu būdu galite modeliuoti, kaip skaičiuoti visą zoną, o ne tik vieną vietą. **Naudokite bet kurį sandėlio procesą atsargų koregavimui koreguoti kaip reikia.**
1. Įsitikinkite, kad yra pakankamai prekės *A0001* atsargų masinėje vietoje, kuri yra nurodyta zonos paėmimo vietos nurodyme, kur papildymo darbas turėtų paimti prekes iš zonos ID *BULK*. Tačiau bendroji atsargų suma turėtų būti mažesnė nei būtinas maksimalus kiekis (*150*), nurodytas papildymo šablone.
1. Nebūtina, bet rekomenduojama: Vykdydami šiuos veiksmus sukursite atsargų koregavimo žurnalą:

    1. Eikite į **Atsargų valdymas \> Žurnalo įrašai \> Prekės \> Atsargų koregavimas**.
    1. Pasirinkite **Naujas**.
    1. Dialogo lango **Kurti atsargų žurnalą** lauke **Sandėlis** pasirinkite *61*.
    1. Pasirinkite **Gerai**.
    1. „FastTab skirtuke“ **Žurnalo eilutės** naudokite mygtuką **Nauja,** norėdami įtraukti tris eilutes į tinklelį ir nustatyti tolimesnes vertes. Kai baigsite nustatyti kiekvieną eilutę, pasirinkite **Įrašyti**.

        - **Eilutė 1:**

            - **Prekės numeris:** *A0001*
            - **Vieta:** *6*
            - **Sandėlis:** *61*
            - **Vieta:** *02A01R1S1B*
            - **Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.
            - **Kiekis:** *1000*

        - **Eilutė 2:**

            - **Prekės numeris:** *A0001*
            - **Vieta:** *6*
            - **Sandėlis:** *61*
            - **Vieta:** *07A01R2S1B*
            - **Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.
            - **Kiekis:** *15*

        - **Eilutė 3:**

            - **Prekės numeris:** *A0001*
            - **Vieta:** *6*
            - **Sandėlis:** *61*
            - **Vieta:** *07A01R1S1B*
            - **Numerio lentelė:** Iš sąrašo pasirinkite esamą numerio lentelę arba sukurkite naują numerio lentelę.
            - **Kiekis:** *10*

    1. Veiksmų srityje pasirinkite **Patvirtinti**. Prieš pereidami prie kito žingsnio, ištaisykite visas aptiktas klaidas.
    1. Veiksmų srityje pasirinkite **Registruoti,** kad atliktumėte atsargų registravimą.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Scenarijaus pavyzdys: paleisti zona pagrįstą min. / maks. papildymą

Kai visi būtinųjų sąlygų pavyzdžio duomenys yra vietoje, galite suaktyvinti papildymą atlikdami šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Papildymas \> Papildymai**.
1. Dialogo lango **Papildymas**„FastTab” skirtuke **Įtrauktini įrašai** Pasirinkite **Filtruoti**.
1. Dialogo lango **Užklausa** skirtuke **Diapazonas** redaguokite numatytąją lentelės eilutę taip:

    - **Lentelė:** Pasirinkti _Papildymo šablonai_.
    - **Išvestinė lentelė:** Pasirinkti _Papildymo šablonai_.
    - **Laukas:** Pasirinkti _Papildymo šablonai_.
    - **Kriterijai:** Pasirinkite _Zoną min/maks replen__. Šis papildymo šablonas yra sukuriamas, kai paruošiate demonstracinius duomenis šiam scenarijui.

1. Pasirinkite **Gerai,** kad įrašytumėte užklausą ir sugrįžtumėte į **Papildymo** dialogo langą.
1. Pasirinkite **Gerai,** norėdami paleisti papildymo šabloną.

Papildymo darbas yra sukuriamas, kad būtų galima paimti atsargas iš *BULK* zonos ir papildyti jomis *AUKŠTO* zoną.

## <a name="notes-and-tips"></a>Pastabos ir patarimai

Pateikiame kelias pastabas ir patarimus, kaip dirbti su funkcija:

- Norėdami nustatyti papildymo darbą, kuris eina į pageidaujamą zoną, papildymo šablono eilutes ir vietos nurodymus galite susieti vienu iš šių būdų:

    - Redaguoti vietos nurodymo antraštės užklausą ir filtruoti pasirinktas papildymo šablono eilutes.
    - Naudojant nurodymo kodą papildymo šablone galima jį susieti su paėmimo vietos nurodymu.

- Jei naudojate dinamines vietas, papildymo darbas bus pirmiausia sukurtas pirmoje galimoje vietoje arba toje vietoje, kurioje jau yra atsargų, jei vietos nustatymo veiksmas nustatomas taip, kad būtų galima naudoti **Konsolidavimo** strategiją.
- Jei naudojate fiksuotas vietas, o ne zonas, turite naudoti [standartinį min. / maks. papildymą](tasks/set-up-min-max-replenishment-process.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]