---
title: Skirtingų pakavimo ir saugojimo dimensijų nustatymas
description: Šioje temoje aprašoma, kaip nurodyti, kuriam procesui (pakavimui, saugojimui ar įdėtajam pakavimui) naudojama kiekviena nurodyta dimensija.
author: Mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 090a6f653b50d8f22a2f34354172f129624813f1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687651"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Skirtingų pakavimo ir saugojimo dimensijų nustatymas

[!include [banner](../../includes/banner.md)]

Kai kurios prekės yra supakuotos arba saugomos taip, kad jums gali reikėti sekti kiekvieno iš kelių skirtingų procesų faktines dimensijas atskirai. Funkcija *Produkto pakavimo dimensijos* leidžia jums nustatyti vieną ar kelis kiekvieno produkto dimensijų tipus. Kiekvienas dimensijos tipas pateikia faktinių matavimų (svorio, pločio, gylio ir aukščio) rinkinį ir nustato procesą, kuriame taikomos šių faktinių matavimų vertės. Kai ši funkcija yra įgalinta, jūsų sistema palaiko šiuos dimensijų tipus:

- *Saugojimas* – saugojimo dimensijos naudojamos kartu su vietos tūrio metrikomis, siekiant nustatyti, kiek kiekvienos prekės vienetų galima saugoti įvairiose sandėlio vietose.
- *Pakavimas* – pakavimo dimensijos naudojamos krovimo į konteineriu ir rankinio pakavimo proceso metu, siekiant nustatyti, kiek kiekvienos prekės vienetų tilptų į įvairiems konteinerių tipus.
- *Įdėtasis pakavimas* – įdėtojo pakavimo dimensijos naudojamos, kai pakavimo procese yra keli lygiai.

*Saugojimo* dimensijos palaikomos net tada, kai funkcija *Produkto pakavimo dimensijos* nėra įgalinta. Jas nustatote naudodami **Faktinės dimensijos** „Supply Chain Management” puslapį. Šios dimensijos naudojamos visuose procesuose, kuriuose nenurodytos pakavimo ir įdėtojo pakavimo dimensijos.

*Pakavimo* ir *Įdėtojo pakavimo* dimensijos yra nustatomos naudojant **Faktinės produkto dimensijos** puslapį, kuris įtraukiamas įgalinus *Produkto pakavimo dimensijų* funkciją.
Šioje temoje pateikiamas scenarijus, iliustruojantis šios funkcijos naudojimą.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Produkto pakavimo dimensijų funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [Funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) darbo sritį, norėdami sužinoti funkcijos būseną ir įjungti ją, jei reikia. Ten ši funkcija pateikiama taip:

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Produkto pakavimo dimensijos*

## <a name="example-scenario"></a>Pavyzdinis scenarijus

### <a name="set-up-the-scenario"></a>Scenarijaus nustatymas

Prieš vykdydami pavyzdinį scenarijų, turite paruošti savo sistemą, kaip aprašyta šiame skyriuje.

#### <a name="enable-demo-data"></a>Demonstracinių duomenų įgalinimas

Norėdami dirbti pagal šį scenarijų, naudodami čia nurodytus demonstracinius įrašus ir vertes, turite būti sistemoje su įdiegtais standartiniais [demonstraciniais duomenimis](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Be to, prieš pradedant turite pasirinkti *„USMF”* juridinį subjektą.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Produkto faktinės dimensijos įtraukimas

Įtraukite naują produkto faktinę dimensiją, atlikdami šiuos veiksmus:

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą su **Prekės numeriu** *„A0001”*.
1. Veiksmų srityje atidarykite **Inventoriaus valdymo** skirtuką ir iš **Sandėlio** grupės, pasirinkite **Faktinės produkto dimensijos**.
1. Atidaromas **Faktinės produkto dimensijos** puslapis. Veiksmų srityje pasirinkite **Naujas** norėdami įtraukti naują dimensiją į tinklelį su šiais parametrais:
    - **Faktinės dimensijos tipas** - *Pakavimas*
    - **Faktinis vienetas** - *vnt*
    - **Svoris** - *4'*
    - **Svorio vienetas** - *kg'*
    - **Gylis** - *3'*
    - **Aukštis** - *4'*
    - **Plotis** - *3'*
    - **Ilgis** - *cm'*
    - **Tūrio vienetas** - *cm3'*

Laukas **Tūris** apskaičiuojamas automatiškai pagal jūsų **Gylio**, **Aukščio** ir **Pločio** parametrus.

#### <a name="create-a-new-container-type"></a>Naujo konteinerio tipo kūrimas

Eikite į **Sandėlio valdymas \> Sąranka \> Konteineris \> Konteinerių tipai** ir sukurkite naują įrašą su šiais parametrais:

- **Konteinerio tipo kodas** - *Trumpa dėžė*
- **Aprašymas** - *Trumpa dėžė*
- **Didžiausias grynasis svoris** - *50'*
- **Tūris** - *144'*
- **Ilgis** - *6'*
- **Plotis** - *6'*
- **Aukštis** - *4'*

#### <a name="create-a-container-group"></a>Konteinerių grupės kūrimas

Eikite į **Sandėlio valdymas \> Sąranka \> Konteineris \> Konteinerių grupės** ir sukurkite naują įrašą su šiais parametrais:

- **Konteinerių grupės ID** - *Trumpa dėžė*
- **Aprašymas** - *Trumpa dėžė*

Įtraukite naują eilutę į **Išsamios informacijos** skyrių. Nustatykite **Konteinerio tipą** į *Trumpa dėžė*.

#### <a name="set-up-a-container-build-template"></a>Konteinerio kūrimo šablono nustatymas

Eikite į **Sandėlio valdymas \> Sąranka \> Konteineriai \> Konteinerių kūrimo šablonai** ir pasirinkite **Dėžės**. Pakeiskite **Konteinerių grupės ID** į *Trumpa dėžė*.

### <a name="run-the-scenario"></a>Scenarijaus vykdymas

Parengę sistemą, kaip aprašyta ankstesniame skyriuje, esate pasiruošę vykdyti scenarijų, kaip aprašyta kitame skyriuje.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Pardavimo užsakymo ir siuntos kūrimas

Šio proceso metu jūs sukursite siuntą pagal prekės *Pakavimo* dimensijas su aukščiu mažesniu nei 3.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - **Kliento sąskaita:** *US-001*
    - **Sandėlis:** *63*

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Naujas pardavimo užsakymas yra atidarytas. Jame turi būti nauja tuščia eilutė, esanti **Pardavimo užsakymo eilutės** „FastTab” skirtuko tinklelyje. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *5*

1. **Prekybos užsakymo eilučių** „FastTab“, pasirinkite **Atsargos \> Rezervavimas**.
1. **Rezervavimo** puslapyje, veiksmų juostoje pasirinkite **Rezervuoti vietą** inventoriaus rezervavimui.
1. Uždarykite puslapį.
1. Veiksmų srityje atidarykite skirtuką **Sandėlis** ir pasirinkite **Išleisti į sandėlį** sandėlio darbo užduočiai sukurti.
1. „FastTab” **Pardavimų užsakymų eilutės** pasirinkite **Sandėlis \> Siuntimo informacija**.
1. Veiksmų srityje atidarykite skirtuką **Transportavimas** ir pasirinkite **Rodyti konteinerius**. Patvirtinkite, kad prekė buvo sudėta į du *Trumpos dėžės* konteinerius.

#### <a name="place-an-item-into-storage"></a>Prekės patalpinimas į saugyklą

1. Atidarykite mobilųjį įrenginį, prisijunkite prie 63 sandėlio ir eikite į **Atsargos \> Koregavimas**.
1. Įveskite **Vieta** = *TRUMPA-01*. Sukurkite naują numerio lentelę su **Preke** = *„A0001”* ir **Kiekiu** = *1 vnt*.
1. Pasirinkite **Gerai**. Gausite klaidą „Vieta TRUMPA-01 nepavyko, nes prekė „A0001” neatitinka nurodytų vietos dimensijų.” Taip nutinka dėl to, kad produkto *Saugojimo* tipo dimensijos yra didesnės nei vietos profilyje nurodytos dimensijos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]