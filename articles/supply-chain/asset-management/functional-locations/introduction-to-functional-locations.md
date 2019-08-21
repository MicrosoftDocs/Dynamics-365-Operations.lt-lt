---
title: Funkcinių vietų pristatymas
description: Šioje temoje pateikiama modulio Turto valdymas funkcinių vietų apžvalga.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d7d98ec5434d9cdc93276952035b559625be2bd
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783463"
---
# <a name="introduction-to-functional-locations"></a>Funkcinių vietų pristatymas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje pateikiama modulio Turto valdymas funkcinių vietų apžvalga. Funkcinės vietos yra techninės struktūros elementai, pvz., sistemos funkciniai vienetai. Funkcinės vietos kuriamos hierarchiškai, o jūs vietose diegiate turtą. Jūsų įmonės funkcinių vietų konfigūracija priklauso nuo įmonės reikalavimų.

Štai keletas funkcinių vietų naudojimo pavyzdžių:

- **Funkcinės** – funkcinės vietos gali būti orientuotos į vartotoją ir gali būti naudojamos panašiai veikiančiam turtui valdyti.
- **Susijusios su procesu** – funkcinės vietos gali būti orientuotos į darbo eigą.
- **Erdvinės** – funkcinės vietos gali reikšti geografines vietoves ar vietas.

Kiekviena funkcinė vieta modulyje Turto valdymas valdoma atskirai. Toliau pateikiama keletas naudingų funkcinių vietų funkcijų:

- Funkcinių vietų specifikacijų konfigūracija.
- Turto specifikacijų reikalavimų konfigūracija.
- Prevencinės ir einamosios priežiūros sekų konfigūracija.
- Įdiegtų išteklių valdymas.
- Aktyviųjų užklausų ir darbo užsakymų, susijusių su įdiegtu turtu, sekimas.
- Aptiktų turto gedimų sekimas.
- Su funkcine vieta susijusio turto priežiūros išlaidų sekimas bet kuriuo metu.

Funkcinės vietos užtikrina turto atsekamumą, susijusį su užklausomis, darbo užsakymais, gedimų registravimu, būklės vertinimu, gamybos sustabdymo registravimu ir turto skaitiklio registravimu.

> [!NOTE]
> Net jei turtas per naudojimo laikotarpį įdiegiamas skirtingose funkcinėse vietose, išlaidos gali būti susijusios su kiekviena vieta. Kitaip tariant, turto išlaidos visada yra susijusios su funkcine vieta, kurioje tam tikru metu buvo įdiegtas turtas.

Funkcinės vietos **nėra** kintamos. Todėl, nustačius funkcinės vietos hierarchiją, joje negalima keisti vietų padėties. 

Sukūrus funkcinės vietos hierarchiją, toliau joje diegiamas turtas. Daugiau informacijos žr. skyriuje [Išteklių diegimas funkcinėse vietose](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Visos funkcinės vietos

Pasirinkite **Turto valdymas** \> **Dažnas** \> **Funkcinės vietos** \> **Visos funkcinės vietos,** kad būtų atidarytas **visų funkcijų vietų** sąrašas. Šiame puslapyje pateikiamos visos funkcinės vietos ir dalis informacijos apie jas. Norėdami peržiūrėti tik aktyviąsias funkcines vietas, pasirinkite **Aktyviosios funkcinės vietos**. Norėdami peržiūrėti tik funkcines vietas, su kuriomis esate susiję kaip darbuotojas, pasirinkite **Mano aktyviosios funkcinės vietos**. (Šis ryšys nustatomas puslapyje **Darbuotojai**. Daugiau informacijos žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)

Sąrašo puslapyje **Visos funkcinės vietos** pasirinkite saitą stulpelyje **Funkcinė vieta**, kad peržiūrėtumėte išsamią pasirinkto įrašo informaciją. Norėdami redaguoti funkcinę vietą, spustelėkite mygtuką **Edit**. Išsamios informacijos rodinyje pateikiama išsami informacija, susijusi su vieta. Dešinėje jame taip pat yra sritis **Related information**. Šioje srityje rodoma funkcinės vietos hierarchija. Galite išplėsti ir sutraukti sritį **Related information**.

Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose. Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.

| Mygtuko pavadinimas                         | Aprašymas                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Redagavimas                                | Įjungiamas puslapio redagavimo režimas arba rodinio režimas.                                                                                         |
| Naujos                                 | Sukuriama nauja funkcinė vieta.                                                                                                            |
| Naikinti                              | Panaikinama pasirinkta funkcinė vieta.                                                                                                     |
| Keisti pavadinimą                              | Pervardijama pasirinkta funkcinė vieta.                                                                                                     |
| Kopijuoti funkcinės vietos struktūrą  | Kopijuojama funkcinės vietos hierarchija.                                                                                                      |
| Diegti turtą                       | Funkcinėje vietoje įdiegiamas turtas, įskaitant antrinį turtą.                                                                        |
| Pakeisti turtą                       | Funkcinėje vietoje turto hierarchija pakeičiama kita turto hierarchija.                                                         |
| Išlaidų kontrolė                        | Atidaromas puslapis **Functional location cost control**, kuriame galima apskaičiuoti pasirinktos funkcinės vietos išlaidas.                |
| Valandų kontrolė                        | Atidaromas puslapis **Functional location hour control**, kuriame galima apskaičiuoti pasirinktos funkcinės vietos išlaidas.                |
| Turtas                              | Atidaromas puslapis **All assets**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusio turto sąrašą.                      |
| Užklausos                            | Atidaromas puslapis **Active requests**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių užklausų sąrašą.               |
| Darbo užsakymai                         | Atidaromas puslapis **Active work orders**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių darbo užsakymų sąrašą.         |
| Gedimai                              | Atidaromas puslapis **Asset faults**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių užregistruotų turto gedimų sąrašą. |
| Naujinti funkcinės vietos būseną    | Atnaujinamas pasirinktos funkcinės vietos etapas.                                                                                        |
| Ciklo būsenų žurnalas                 | Peržiūrimas žurnalas, kuriame rodomi pasirinktos funkcinės vietos etapai.                                                                        |
