---
title: Darbo eilutės informacija
description: Šioje temoje pateikiama informacija apie puslapį Darbo eilutės informacija, pateikiantį išsamų, rūšiuojamą ir filtruojamą atskirų sistemos darbo eilučių sąrašą.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4d7c6991c0171b0e09752b3305e0fa11a25b7833
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674116"
---
# <a name="work-line-details"></a>Darbo eilutės informacija

[!include [banner](../includes/banner.md)]

Puslapis **Darbo eilutės informacija** pateikia išsamų, rūšiuojamą ir filtruojamą atskirų sistemos darbo eilučių sąrašą. Jame pateikiama išsami planuojamų ir vykdomų sandėlio darbų peržiūra. Galite lengvai perjungti peržiūrą tarp visų ir tik atvirų darbo eilučių. Išsami informacija, pateikiama kiekvienai eilutei, apima darbo būseną, prekės numerį, vietą, darbo kiekį, krovinio ID ir siuntos ID.

## <a name="turn-on-the-work-line-details-feature"></a>Darbo eilutės informacijos funkcijos įjungimas

Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali naudotis funkcijų [valdymo puslapiu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), norėdami patikrinti priemonės būseną ir, jei reikia, ją įgalinti arba išjungti. Čia funkcija yra nurodyta kaip:

- **Modulis:** *Warehouse management*
- **Funkcijos pavadinimas:** *Darbo eilutės informacija*

## <a name="open-and-use-the-work-line-details-page"></a>Darbo eilutės informacijos puslapio atidarymas ir naudojimas

Norėdami peržiūrėti darbo eilutės informacijos sąrašą, eikite į **Sandėlio valdymas \> Darbas \> Eilutės informacija**. Dabar galite atlikti šiuos veiksmus:

- Naudoti lauką **Filtruoti** eilučių, turinčių konkrečią bet kurio galimo parametro vertę, paieškai. (Galimi parametrai apima daug parametrų, kurie tinklelyje nerodomi kaip stulpeliai.)
- Naudoti žymės langelį **Rodyti uždarytus** uždarytų eilučių rodymui arba paslėpimui.
- Pasirinkti **Rodyti dimensijas** dialogo langui **Dimensijų rodymas** atidaryti, kuriame galėsite pasirinkti rodyti arba slėpti skirtingus dimensijos stulpelius tinklelyje.
- Pasirinkite bet kurią stulpelio antraštę meniu atidaryti, kuriame galėsite pasirinkti sąrašą rūšiavimą arba filtravimą pagal to stulpelio vertes.
- Pasirinkite darbo eilutę ir tada **Keisti vietą** dialogo langui atidaryti, kuriame galėsite keisti tos darbo eilutės vietą. Jūsų nurodyta vieta nepaisys vietos nurodymo nustatymo.
- Pasirinkite darbo eilutę ir **Atšaukti darbo eilutę** dialogo langui atidaryti, kuriame galėsite iš dalies arba visiškai sumažinti tos darbo eilutės kiekį.
- Koreguoti kiekius.
- Peržiūrėti bet kurios darbo eilutės operacijas.

## <a name="try-out-the-feature"></a>Funkcijos išbandymas

Šiame skyriuje pateikiama trijų dalių parodomoji versija, kaip dirbti su darbo eilutės informacija.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti su parodomąja versija, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Taip pat galite naudoti šią parodomąją versiją kaip vedlį darbui gamybos sistemoje. Tačiau Jūs turėsite keisti vertes ir galite neturėti kai kurių tipų būtinų įrašų, kuriuos suteikia standartiniai demonstraciniai duomenys.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Patikrinkite ar scenarijaus nustatyme yra pakankamai pasiekiamų atsargų

Jei dirbate su **USMF** demonstraciniais duomenimis, pirmiausia turite įsitikinti, kad sistema nustatyta taip, kad kiekvienoje atitinkamoje vietoje yra pakankamai pasiekiamų atsargų. Šia parodomąja versija numanoma, kad toliau pateiktos atsargos yra pasiekiamos:

- **Prekė M9200:** 45 EA (ar daugiau)
- **Prekė M9202:** 10 EA (ar daugiau)

Atlikite šiuos veiksmus, norėdami patikrinti, ar yra pakankamai pasiekiamų atsargų ir visi reikalingi koregavimai yra atlikti.

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Vietos nurodymai**, sužinoti, kurios prekių paėmimų vietos yra naudojamos pardavimo užsakymo paėmimui 51 sandėlyje. (Daugiau informacijos rasite [Sandėlio darbo kontroliavimas naudojant darbo šablonus ir vietų nurodymus](control-warehouse-location-directives.md).)
1. Tikrinti atsargų lygius atitinkamose vietose.
1. Koreguoti atsargas kaip reikalinga. Jei reikia koreguoti atsargas, galite sukurti rankinius perkėlimus, naudoti papildymą arba pritaikyti bet kurį kitą srautą.

### <a name="part-1-create-picking-work"></a>1 dalis: Paėmimo darbo sukūrimas

Prieš pradėdami kurti darbo užduotį, įsitikinkite, kad sandėlis nustatytas taip, kad būtų galima atsakyti į darbo užklausas numatytu būdu.

Norėdami sukurti paėmimo darbo užduotį, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Nauja** dialogo langui **Sukurti pardavimų užsakymą** atidaryti.
1. Dialogo lange **Sukurti pardavimo užsakymą** nustatykite šias vertes:

    - „FastTab” skirtuke **Klientas**, nustatykite lauką **Kliento paskyra** į _US–001_.
    - „FastTab“ skirtuke **Bendra** nustatykite lauką **Sandėlis** į _51_.

1. Pasirinkite **Gerai** pirkimo užsakymui sukurti ir dialogo langui uždaryti.
1. Jūsų naujas pirkimo užsakymas yra atidarytas. Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** tinklelyje. Nustatykite tokias šios užsakymo eilutės reikšmes:

    - **Prekės numeris:** _M9200_
    - **Kiekis:** _20_
    - **Vienetas:** _ea_

1. Pasirinkite naują užsakymo eilutę ir meniu **Atsargos** pasirinkite **Rezervavimas** puslapiui **Rezervavimas** atidaryti.
1. Puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**. Sistema sukuria siuntą, įtraukia ją į naują krovinį ir sukuria reikiamą darbo užduotį.
1. Sukurkite antrą pardavimo užsakymą, skirtą tai pačiai kliento sąskaitai ir sandėliui, kurį naudojote pirmajam užsakymui. Įtraukite šias dvi užsakymo eilutes į šį užsakymą:

    - **1 eilutė:** Nustatykite lauką **Prekės numeris** į _M9200_, lauką **Kiekis** į _25_ ir lauką **Vienetas** į _EA_.
    - **2 eilutė:** Nustatykite lauką **Prekės numeris** į _M9202_, lauką **Kiekis** į _10_ ir **Vienetas** lauką į _EA_.

1. Pakartokite 6-8 veiksmus norėdami rezervuoti atsargas kiekvienai užsakymo eilutei (po vieną), tada pakartokite 9 veiksmą, užsakymui į sandėlį paleisti.

### <a name="part-2-change-the-location-for-a-work-line"></a>2 dalis: Darbo eilutės vietos pakeitimas

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo eilutės informacija**.
1. Suraskite ir pasirinkite vieną iš darbo eilučių, kurias sukūrėte šiai parodomajai versijai.
1. Pasirinkite **Keisti vietą** dialogo langui **Pasirinkti naują vietą** atidaryti.
1. Dialogo lango **Pasirinkti naują vietą** lauke **Vieta** pasirinkite naują darbo eilutės vietą.
1. Norėdami pritaikyti pakeitimus ir uždaryti dialogo langą, pasirinkite **Gerai**.

> [!IMPORTANT]
> Galite pateikti vietos keitimus tik tuo atveju, jei naujoje vietoje yra pakankamai prieinamų atsargų (paėmimui), arba jei ji praeina vietos tipo tikrinimą (dėl padėjimo).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>3 dalis: keisti darbo eilutės kiekį arba atšaukti darbo eilutę

1. Pasirinkite **Sandėlio valdymas \> Darbas \> Darbo eilutės informacija**.
1. Suraskite ir pasirinkite vieną iš darbo eilučių, kurias sukūrėte šiai parodomajai versijai. Atkreipkite dėmesį, kad galite atšaukti arba pakeisti tik tas darbo eilutes, kurių darbo tipas yra _paėmimas_.
1. Pasirinkite **Atšaukti darbo eilutę**, kad būtų atidarytas dialogo langas **Atšaukti kiekį**.
1. Dialogo lango **Atšaukiamas kiekis** lauke **Kiekis** nurodykite kiekį, kuris turi būti *atimamas iš* kiekio, šiuo metu nurodyto eilutėje. Pagal numatytuosius nustatymus lauke **Kiekis** rodomas visas kiekis.

    - Jei atšaukiate visą kiekį, **Darbo būsenos** vertė bus pakeista į _Atšaukta_, tačiau lauke **Darbo kiekis** vis tiek bus rodoma pradinė vertė.
    - Jei atšaukiate tik dalį kiekio, laukas **Darbo kiekis** bus rodoma atnaujinta reikšmė,, tačiau laukas **Darbo statusas** nepasikeis.

1. Norėdami pritaikyti pakeitimus ir uždaryti dialogo langą, pasirinkite **Gerai**.

> [!IMPORTANT]
> Jei atšaukiate tik dalį kiekio darbo eilutėje, taip pat turite pašalinti pasenusius kiekius iš krovinio eilutės. Kitu atveju, nebent tinkamai nustatytas pristatymo trūkumas, nebus galima patvirtinti krovinio išsiuntimo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]