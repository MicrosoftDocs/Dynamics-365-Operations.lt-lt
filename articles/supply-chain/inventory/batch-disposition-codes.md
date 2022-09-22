---
title: Naudoti paketo perdavimo kodus norint pažymėti paketus kaip turimus arba negalima
description: Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti paketo perdavimo kodus norint pažymėti paketus kaip turimus arba jų negalima naudoti bendrojo planavimo, rezervavimo, paėmimo ir (arba) siuntimo metu.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542909"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Naudoti paketo perdavimo kodus norint pažymėti paketus kaip turimus arba negalima

Šiame straipsnyje aprašoma, kaip nustatyti ir naudoti *paketo perdavimo kodus*. Kiekvieno paketo perdavimo kodo būsena yra Turima *arba* *Nepasiekiama*. Atsargų paketams priskiriate paketo perdavimo kodus, kad nurodydami, ar kiekvieną paketą galima naudoti bendrojo planavimo, rezervavimo, paėmimo ir (arba) siuntimo metu.

Norėdami naudoti paketo perdavimo kodus, turite nustatyti kodus ir priskirti juos paketams, kuriuos norite valdyti.

## <a name="set-up-batch-disposition-codes"></a>Nustatyti paketo perdavimo kodus

Turite nustatyti kiekvieną paketo perdavimo kodą, kurį norite naudoti savo sistemoje. Galite sukurti tiek kodų, kiek norite. (Pvz., galite kurti kodus, kad identifikuokite skirtingas priežastis, dėl kurių paketas gali būti pasiekiamas arba negalimas). Tačiau dažniausiai būna tik du kodai: vienas galimas *,* o kitas – *negalimas*. Taip pat galite kurti pasirinktinius kodus, kurie įgalina kai kurių operacijų, bet ne kitų operacijų paketą, naudoti.

Norėdami nustatyti paketo perdavimo kodus, atlikite šiuos veiksmus.

1. Eikite **į atsargų valdymo \> nustatymo \> pagrindinį \> paketo perdavimą**.
1. Paketo **perdavimo puslapio pagrindinis puslapis** išvardija jūsų dabartinius paketo perdavimo kodus ir leidžia juos kurti, naikinti ir redaguoti. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami redaguoti esamą kodą, pasirinkite jį sąrašo srityje.
    - Norėdami sukurti naują kodą, veiksmų **srityje** pasirinkite Naujas.

1. Naujo ar pasirinkto kodo antraštėje nustatykite šiuos laukus:

    - **Paketo perdavimo kodas** – įveskite rodomą kodo pavadinimą.
    - **Aprašas** – aprašyti, kaip turi būti naudojamas kodas.
    - **Paketo perdavimo būsena** – pasirinkite būseną, kuri taikoma paketams, kurių kodas priskirtas:

        - *Negalima* – paketų negalima naudoti bendrojo planavimo, rezervavimo, paėmimo arba siuntimo metu. Kai pasirenkate šią reikšmę, visos **·** **Pasirinktys** Blokavimo pasirinktys nustatymo "FastTab *" yra nustatytos kaip Taip*, **o visos Nettable** pasirinktys yra nustatytos kaip *Ne.* Tačiau kai kuriuos parametrus galima pakeisti norint pridėti išimtis.
        - *Turima* – paketus galima naudoti bendrojo planavimo, rezervavimo, paėmimo ir (arba) siuntimo metu. Kai pasirenkate šią vertę, visos **·** **FastTab** Nustatymo FastTab *blokavimo pasirinktys yra nustatytos kaip Ne*, **o visos Nettable** pasirinktys yra nustatytos kaip *Taip.* Šiuos parametrus bus galima tik skaityti, kai **nustatyta lauko Paketo perdavimo būsena** *reikšmė Turima*.

1. Jei nustatote **paketo perdavimo būsenos lauką kaip Neprieinamas, galite pritaikyti kiekvienos operacijos (rezervuoti, paimti ir siųsti) blokavimo būseną kiekvienam užsakymo tipui (pardavimas** *·*, perkėlimas ir gamyba). Gamybos užsakymuose galite pasirinkti blokuoti arba atblokuoti gamybos paėmimo žurnalą. Taip pat galite pasirinkti blokuoti arba atblokuoti bendrąjį planavimą. Norėdami užblokuoti arba atblokuoti **kiekvieną** operaciją, naudokite "FastTab" nustatymo pasirinktis, jei reikia. Norėdami įgalinti **bendrąjį planavimą, nustatykite** Pasirinktį Nettable *kaip Taip* arba nustatykite ją kaip *Ne*, jei norite blokuoti bendrąjį planavimą.

## <a name="assign-batch-disposition-codes-to-batches"></a>Priskirti paketo perdavimo kodus paketams

Apibrėžę paketo perdavimo kodus, kurių jums reikia, atlikite šiuos veiksmus, norėdami priskirti juos paketams.

1. Eiti į **sandėlio \> valdymo \> nustatymo atsargų \> paketus**.
1. Pasirinkite vieną ar daugiau paketų, jei norite priskirti paketo perdavimo kodą.
1. Veiksmų srities skirtuke Nustatyti iš **naujo** pasirinkite Iš naujo **nustatyti paketo perdavimo kodą**.
1. Dialogo lange **Keisti atsargų paketo apribojimus** nustatykite lauką Naujas paketo perdavimo kodas **kaip kodo pavadinimą,** kurį norite priskirti.
1. Pasirinkite **Gerai,** jei norite pritaikyti naują parametrą ir įrašyti keitimą.

    Paketų puslapyje **paketo** perdavimo **·** **kodo** ir paketo perdavimo būsenos stulpeliuose vertės atnaujinamos, kad atspindėtų naujus pasirinktų paketų parametrus.

## <a name="master-planning-example"></a>Bendrojo planavimo pavyzdys

Šis pavyzdys rodo, kaip paketo perdavimo kodai gali paveikti bendrąjį planavimą.

Pavyzdžiui, paketo perdavimo kodai nustatomi taip:

- *Turimas P:*

    - **Paketo perdavimo būsena:** *yra*
    - **Grynoji vertė:** *Taip*

- *P-nepasiekiamas:*

    - **Paketo perdavimo būsena:** *nėra*
    - **Nettable:** *Ne*

Yra produktas (*Produktas –1),* kuriame yra du paketai: *paketas A* ir *B paketas*. Šie paketai nustatomi taip:

- *Paketas – A:*

    - **Paketo perdavimo kodas:** *P – turimas*
    - **Turimo kiekio:** 1

- *Paketas B:*

    - **Paketo perdavimo kodas:** *P nepasiekiamas*
    - **Turimo kiekio:** 1

Pardavimo užsakymas (*SO1*) 2 produkto – *1 kiekiui*. Pristatymo data yra trys dienos nuo šiandienos.

Jūs vykdote bendrąjį planavimą ir nustatote su šiuo pavyzdžiu susijusias vertes:

- **Suplanuotas užsakymas:** *pirkimo užsakymas*
- **Papildymo strategija:** *reikalavimas*
- **Gamybos laikas:** *0*

Po planavimo vykdymo sistema naudoja prieinamą paketą (*paketas-A*) pardavimo užsakymo SO1 kiekiui *1* *produkto –1 padengti*. Tačiau paketo B naudoti *negalima*, nes šis paketas pažymėtas kaip negalimas planavimui. Todėl, siekdama padengti likusį kiekį, sistema sukuria naujo produkto -1 paketo suplanuotą pirkimo užsakymą (*²1* *·*).

Toliau pateikta iliustracija rodo planavimo rezultato laiko juostą.

![Pavyzdys, kuriame parodyta, kaip paketo perdavimo kodai gali paveikti bendrąjį planavimą.](media/batch-codes-planning-example.png "Pavyzdys, kuriame parodyta, kaip paketo perdavimo kodai gali paveikti bendrąjį planavimą")
