---
title: Grynieji reikalavimai ir iškvietimo informacija
description: Šiame straipsnyje pateikiama informacija apie apskaičiuotus grynuosius poreikius ir iškvietimo informaciją.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748444"
---
# <a name="net-requirements-and-pegging-information"></a>Grynieji reikalavimai ir iškvietimo informacija

[!include [banner](../../includes/banner.md)]

Kai vykdote bendrąjį planavimą, svarbu suprasti jo išeigą, kaip esamas tiekimas padengia poreikį ir kodėl buvo sugeneruotas konkretus tiekimas. Galite naudoti **Grynųjų reikalavimų** puslapį, kad geriau suprastumėte apskaičiuotus bendrojo planavimo reikalavimus.

Grynųjų **poreikių** puslapis rodo grynuosius poreikius, kurie apskaičiuoti produktui bendrojo planavimo metu. Taip pat yra rodomi padengimo parametrai, kurie buvo taikyti bendrojo planavimo vykdymo metu, reikalavimų bendrųjų sumų paskirstymas pagal operacijos tipą ir iškvietimo informaciją.

## <a name="open-the-net-requirements-page"></a>Atidarykite Grynųjų reikalavimų puslapį

**Grynųjų reikalavimų** puslapį galite atidaryti bet kuriuo iš šių būdų:

- Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**. Pasirinkite arba atidarykite produktą. Tada veiksmų srities skirtuko **Planas** grupėje **Reikalavimai** pasirinkite **Grynieji reikalavimai**.
- Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**. Atidarykite pardavimo užsakymą. Tada **Pardavimo užsakymo eilutės** "FastTab", įrankių juostoje, pasirinkite **Produktas ir tiekimas \> Grynieji reikalavimai**.
- Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**. Pasirinkite ar atidarykite suplanuotą užsakymą. Tada veiksmų srities skirtuko **Žiūrėti** grupėje **Reikalavimai** pasirinkite **Reikalavimų profilis**.

## <a name="use-the-net-requirements-page"></a>Naudokite Grynųjų reikalavimų puslapį

**Grynųjų reikalavimų** puslapį sudaro viršutinė ir apatinė dalys. Šiame puslapyje esančioje veiksmų srityje yra **Naujinti** mygtukas. Pasirinkus šį mygtuką, rodomas komandų meniu.

### <a name="select-a-master-plan-to-view"></a>Pasirinkti norimą peržiūrėti pagrindinį planą

Prieš peržiūrėdami grynuosius produkto reikalavimus, puslapio viršuje laukelyje **Planas** būtinai pasirinkite reikiamą pagrindinį planą.

### <a name="upper-section"></a>Viršutinė dalis

Viršutinėje puslapio dalyje pateikiami šie skirtukai:

- **Peržiūra** – peržiūrėti produkto dimensijų prekių reikalavimus.
- **Prekės padengimas** – peržiūrėti padengimo parametrus, kurie buvo naudojami apskaičiuojant reikalavimus.
- **Suvestinė** – peržiūrėti reikalavimų sumų paskirstymą pagal operacijos tipą.
- **Laikotarpis** – peržiūrėti kiekvieno laikotarpio kvitus, problemas ir suprojektuotas turimas atsargas, kaip apibrėžta laikotarpio šablone. Taip pat galite gauti grafinį numatomų turimų atsargų vaizdą.

### <a name="lower-section"></a>Apatinė dalis

Apatinėje puslapio dalyje pateikiami šie skirtukai:

- **Peržiūra** - peržiūrėti produktų reikalavimų, apskaičiuotų vykdant bendrąjį planavimą, sąrašą kartu su išdavimo ir gavimo operacijomis, atitinkančiomis reikalavimus. Numatyta, kad sąrašas rūšiuojamas pagal reikalavimo datą. Kai pasirenkate reikalavimą, apatinėje dalyje "FastTab" esantis **Iškvietimas** rodo reikalavimo šaltinį arba operacijas, kurios atitinka reikalavimą.
- **Bendrieji** – peržiūrėkite išsamią informaciją apie pasirinktą reikalavimą.
- **Veiksmas** – peržiūrėti reikalavimų veiksmų pranešimus.

### <a name="the-action-pane"></a>Veiksmų sritis

Toliau nurodytos komandos galimos Veiksmų srityje:

- **Atnaujinti \> Pagrindinis planavimas** - paleiskite pagrindinį planavimą tiesiogiai iš **Grynųjų reikalavimų** puslapio.
- **Atnaujinti \> Numatyti planavimą** - paleiskite numatyti planavimą tiesiogiai iš **Grynųjų reikalavimų** puslapio. Planavimo optimizavimas nepalaiko šios operacijos.
- **Naujinti \> Tęstinumo planavimas** – paleiskite tęstinumo planavimą tiesiogiai iš **Grynieji reikalavimai** puslapio. Planavimo optimizavimas nepalaiko šios operacijos.

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šiame pavyzdyje parodyta, kaip iškvietimo informacija pateikiama **Grynųjų reikalavimų** puslapyje.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami dirbti su šiais naudojamais atvejais, parenkite šį scenarijų:

1. Turite dirbti su sistema, kurioje yra galimi standartiniai duomenų pavyzdžiai, ir juridinį subjektą turite nustatyti į *USMF*.
2. Šiame pavyzdyje naudojamas produktas *1000*, kuris yra USMF pavyzdinių duomenų dalis. Įsitikinkite, kad šis produktas yra pasiekiamas ir kad jis nustatytas šiuo būdu:

    - **Pagrindinis užsakymo tipas:** *Pirkimo užsakymas*
    - **Turimos atsargos:** *10.00*

3. Sukurkite pardavimo užsakymą, kai *25.00* yra produkto *1000* kiekis. Naudokite saugojimo dimensijas, kuriose yra turimos atsargos.
4. Paleiskite *DynPlan* pagrindinio planavimo pagrindinį planavimą.

### <a name="review-the-calculated-requirements"></a>Peržiūrėkite apskaičiuotą reikalavimų kiekį

Tada atidarysite **Grynieji reikalavimai** puslapį *1000* produktui, kad peržiūrėtumėte, kaip apskaičiuoti reikalavimai atitinka vienas kitą.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą, kuris turi **Prekės numerio** vertę *1000*.
1. Veiksmų srities skirtuko **Planas** grupėje **Reikalavimai** pasirinkite **Grynieji reikalavimai**.
1. Puslapyje **Grynieji reikalavimai** nustatykite **Planas** lauką į *DynPlan*.
1. Skirtuko **Apžvalga** puslapio apatinėje dalyje patikrinkite, ar šie reikalavimai išvardyti kaip tinklelio eilutės.

    | Nuoroda | Reikalaujamas kiekis | Sukaupta |
    |---|---|---|
    | Turimos atsargos | 10,00 | 10,00 |
    | Suplanuoti pirkimo užsakymai | 15.00 | 25.00 |
    | Pardavimo užsakymas | -25.00 | (tuščia) |

    > [!NOTE]
    > **Reikalavimo kiekio** laukas rodo bendrą kiekį, kuriam reikalavimas reikalaujamas (jei vertė yra neigiama) arba tiekiamas (jei vertė yra teigiama). Lauke **Sukaupta** rodomas bendras gavimo ir išdavimo kiekis, kuris buvo sukauptas per pasirinktą laikotarpį.

1. Pasirinkite *Turimo* reikalavimo eilutę, tada **Iškvietimo** "FastTab" peržiūrėkite reikalavimus, kuriuos apima šis tiekimas. Ten turėtų pasirodyti ši eilutė.

    | Nuoroda | Reikalaujamas kiekis | Padengtas kiekis |
    |---|---|---|
    | Pardavimo užsakymas | -25.00 | -10.00 |

    Esamos turimos atsargos iš dalies padengia poreikį, kuris kyla iš pardavimų užsakymo.

    ![Turimų atsargų iškvietimo informacija](media/pegging-on-hand.png "Turimų atsargų iškvietimo informacija")

1. Pasirinkite *Planuojamas pirkimo užsakymas* reikalavimo eilutę, tada **Iškvietimo** "FastTab" peržiūrėkite reikalavimus, kuriuos apima šis tiekimas. Ten turėtų pasirodyti ši eilutė.

    | Nuoroda | Reikalaujamas kiekis | Padengtas kiekis |
    |---|---|---|
    | Pardavimo užsakymas | -25.00 | -15.00 |

    Kadangi pardavimo užsakymas jau iš dalies padengtas, sistema likusiam nepadengtam kiekiui sukuria suplanuotą pirkimo užsakymą.

    ![Suplanuoto pirkimo užsakymo iškvietimo informacija](media/pegging-planned-purchase-order.png "Suplanuoto pirkimo užsakymo iškvietimo informacija")

1. Pasirinkite *Pardavimų užsakymas* reikalavimo eilutę, tada **Iškvietimo** "FastTab" peržiūrėkite reikalavimus, kuriuos padengia šis poreikis. Ten turėtų pasirodyti šios eilutės.

    | Nuoroda | Reikalaujamas kiekis | Padengtas kiekis |
    |---|---|---|
    | Turimos atsargos | 10,00 | 10,00 |
    | Suplanuoti pirkimo užsakymai | 15.00 | 15.00 |

    ![Pardavimo užsakymo iškvietimo informacija](media/pegging-planned-purchase-order.png "Pardavimo užsakymo iškvietimo informacija")

> [!NOTE]
> Nepakankaių *atsargų* poreikis neįtrauktas į grynųjų **poreikių** puslapį.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
