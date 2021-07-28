---
title: Funkcinių vietų pristatymas
description: Šioje temoje pateikiama modulio Turto valdymas funkcinių vietų apžvalga.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f31504d2e4ce61e64eb96c2b69326bcb4f1f2560
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6337104"
---
# <a name="introduction-to-functional-locations"></a>Funkcinių vietų pristatymas

[!include [banner](../../includes/banner.md)]

 

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

Sąrašo puslapyje **Visos funkcinės vietos** pasirinkite saitą stulpelyje **Funkcinė vieta**, kad peržiūrėtumėte išsamią pasirinkto įrašo informaciją. Norėdami redaguoti funkcinę vietą, spustelėkite mygtuką **Redaguoti**. Išsamios informacijos rodinyje pateikiama išsami informacija, susijusi su vieta. Dešinėje jame taip pat yra sritis **Susijusi informacija**. Šioje srityje rodoma funkcinės vietos hierarchija. Galite išplėsti ir sutraukti sritį **Susijusi informacija**.

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
| Išlaidų kontrolė                        | Atidaromas puslapis **Funkcinės vietos išlaidų kontrolė**, kuriame galima apskaičiuoti pasirinktos funkcinės vietos išlaidas.                |
| Valandų kontrolė                        | Atidaromas puslapis **Funkcinės vietos valandų kontrolė**, kuriame galima apskaičiuoti pasirinktos funkcinės vietos išlaidas.                |
| Turtas                              | Atidaromas puslapis **Visas turtas**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusio turto sąrašą.                      |
| Užklausos                            | Atidaromas puslapis **Aktyvios užklausos**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių užklausų sąrašą.               |
| Darbo užsakymai                         | Atidaromas puslapis **Aktyvūs darbo užsakymai**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių darbo užsakymų sąrašą.         |
| Gedimai                              | Atidaromas puslapis **Turto gedimai**, kuriame galima peržiūrėti su pasirinkta funkcine vieta susijusių užregistruotų turto gedimų sąrašą. |
| Naujinti funkcinės vietos būseną    | Atnaujinamas pasirinktos funkcinės vietos etapas.                                                                                        |
| Ciklo būsenų žurnalas                 | Peržiūrimas žurnalas, kuriame rodomi pasirinktos funkcinės vietos etapai.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]