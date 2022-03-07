---
title: Iškrovimo kainos užklausos
description: Šioje temoje aprašoma, kaip rasti ir naudoti įvairių tipų iškrovimo kainos modulio užklausas.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b1d94621b68e443175102a1af5a5fdb4a25d0d1e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571766"
---
# <a name="landed-cost-inquiries"></a>Iškrovimo kainos užklausos

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Reiso eilutės užklausos

Užklausoje **Reiso eilutės** rodomos visos reisų eilutės pagal tai, kaip jos priklauso atsargoms. Šią užklausą galima naudoti kaip filtrą, kuris padės rasti prekę, pirkimo užsakymą ar kitą naudingą informaciją. Ją taip pat galima naudoti norint identifikuoti numatomą prekės, kuri gali būti viename ar keliuose reisuose, pristatymo datą. Tai gali padėti valdyti numatomų atsargų gavimą.

Kad atidarytumėte šią užklausą, eikite į **Iškrovimo kaina \> Užklausos \> Reiso eilutės**.

### <a name="overview-tab"></a>Apžvalgos skirtukas

Skirtuke **Apžvalga**, esančiame užklausos puslapyje **Reiso eilutės** yra tinklelis, kuriame rodoma pagrindinė informacija apie kiekvieną atitinkamą reiso eilutę. Toliau pateikiamoje lentelėje aprašomi tinklelyje esantys stulpeliai.

| Stulpelis | aprašymas |
|---|---|
| **Prekės Nr.** | Bendra eilutės prekės kaina. |
| **Nuoroda** | Užsakymo tipas (pirkimo užsakymas arba perkėlimo užsakymas). |
| **Numeris** | Pirkimo užsakymo numeris arba perkėlimo užsakymo numeris. |
| **Sąskaitos lapas** | Registravimo lapas, siejamas su reiso eilute. |
| **Gabenimo konteineris** | Gabenimo konteineris, siejamas su reiso eilute. |
| **Reisas** | Reisas, siejamas su reiso eilute. |
| **Kiekis** | Prekių kiekis reiso eilutei. |
| (Kitos dimensijos) | Jei reikia, galite rodyti papildomų dimensijų stulpelius. Šios dimensijos apima paketo numerį, atsargų būseną ir sandėlį. Veiksmų srityje pasirinkite **Atsargos \> Rodymo dimensijos**, norėdami atidaryti dialogo langą, kuriame galėsite pasirinkti, kurias dimensijas įtraukti. |

### <a name="general-tab"></a>Skirtukas Bendra

Pasirinkite skirtuką **Bendra informacija**, kad peržiūrėtumėte daugiau informacijos apie eilutę, kur šiuo metu pasirinkta skirtuke **Apžvalga**.

### <a name="dimensions-tab"></a>Dimensijų skirtukas

Pasirinkite skirtuką **Dimensijos**, kad peržiūrėtumėte visų turimų eilutės dimensijų vertes, kurios šiuo metu pasirinktos skirtuke **Apžvalga**, nepriklausomai nuo dimensijų, kurias pasirinkote rodyti tame skirtuke.

## <a name="cost-estimate-inquiries"></a>Savikainos vertinimo užklausos

Kiekvieną kartą, kai generuojate savikainos įvertinimą, vertinimas pridedamas prie užklausų puslapio **Savikainos vertinimas**. Išsamesnės informacijos apie tai, kaip generuoti, peržiūrėti ir dirbti su savikainos vertinimais (įskaitant užklausų puslapio vertinimus), žr. skyriuje [Iškrovimo kainos vertinimas ir valdymas](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Prekės sekimas

Puslapį **Prekių stebėjimas** naudokite norėdami peržiūrėti atviras pirkimo užsakymų eilutes ir dabartines jų būsenas. Eilučių nereikia susieti su reisu, kad jos būtų rodomos čia. Tačiau, jei prekė susieta su reisu, prekės sekimo įrašo eilutėje rodomas reiso ID.

Kad atidarytumėte šį puslapį, eikite į **Iškrovimo kaina \> Užklausos \> Sekimas \> Prekės sekimas**.

Kadangi jūsų sistemoje tikriausiai yra labai daug pirkimo užsakymo eilučių, iš pradžių puslapyje **Prekės sekimas** nerodomi jokie įrašai. Pradėkite naudodami puslapio viršuje esančius filtro laukelius, kad nustatytumėte ieškomo pirkimo užsakymo eilutes. Tada veiksmų srityje pasirinkite **Atnaujinti**, kad sugeneruotumėte sąrašą. Žvaigždutę (\*) galite naudoti kaip bet kurio filtro laukelio universalųjį simbolį. Pavyzdžiui, kad rastumėte visas pirkimo užsakymo eilutes prekėms, kurių pavadinime yra žodis „DVD“, laukelį **Tipas** nustatykite kaip **Produkto pavadinimas** ir įveskite *\*DVD\** laukelyje **Laukelio vertė**.

> [!NOTE]
> Šiuo metu neįvykdyti užsakymai apima tik pardavimo užsakymus. Pardavimo pasiūlymai nėra rodomi ar neįvykdytais laikomi užsakymai.

Šioje lentelėje aprašomi stulpeliai, esantys puslapio **Prekių stebėjimas** tinklelyje.

| Stulpelis | aprašymas |
|---|---|
| **Paskirties uostas** | Galutinė paskirties vieta. |
| **Pritarta** | Pirkimo užsakymo eilutės patvirtinimo data. |
| **Pristatymo data** | Pirkimo užsakymo eilutės pristatymo data. |
| **Reisas** | Jei eilutė siejama su reisu, reiso ID. |
| **Gabenimo konteineris** | Jei eilutė pridėta prie gabenimo konteinerio, konteinerio ID. |
| **Siuntimo uostas** | Dabartinis uostas, pagrįstas pirma sekimo formos atkarpa, kur nėra nustatytos faktinės gabenimo konteinerio, susijusio su pirkimo užsakymo eilute, datos. |
| **Veikla** | Dabartinė veikla, pagrįsta pirma sekimo formos atkarpa, kur nėra nustatytos faktinės gabenimo konteinerio, susijusio su pirkimo užsakymo eilute, datos. |
| **Numatyta pabaigos data** | Data, kada tikėtina priimti reisą paskirties sandėlyje. |
| **Pavadinimas / vardas ir (arba) pavardė** | Tiekėjo pavadinimas. |
| **Reiso būsena** | Siuntimo būsena, pridedama prie pirkimo užsakymo eilutės. |
| **Prekės Nr.** | Pirkimo užsakymo eilutės prekės numeris. |
| **Išorinės** | Tiekėjo prekės pavadinimas. |
| **Produkto pavadinimas** | Pirkimo užsakymo eilutės prekės pavadinimas. |
| **Kiekis** | Pirkimo užsakymo eilutės kiekis. |
| **Vienetas** | Pirkimo užsakymo eilutės matavimo vienetas. |
| **Nuoroda** | Užsakymo tipas (pirkimo užsakymas arba perkėlimo užsakymas) |
| **Nuorodos numeris** | Pirkimo užsakymo numeris arba perkėlimo užsakymo numeris. |
| **Neįvykdytas užsakymas** | Simbolis rodo, kad yra neįvykdytų prekės pardavimo užsakymų. |
| (Kitos dimensijos) | Jei reikia, galite rodyti papildomų dimensijų stulpelius. Šios dimensijos apima paketo numerį, atsargų būseną ir sandėlį. Veiksmų srityje pasirinkite **Rodyti matmenis**, kad atidarytumėte dialogo langą, kuriame galima pasirinkti įtraukiamas dimensijas. |

### <a name="related-information-about-backorders"></a>Susijusi informacija apie neįvykdytus užsakymus

Norėdami peržiūrėti daugiau informacijos apie neįvykdytus užsakymus, puslapio dešinėje pasirinkite skirtuką **Susijusi informacija**, o tada pasirinkite **Neįvykdyti užsakymai**. Kad peržiūrėtumėte dar daugiau informacijos apie konkretų neįvykdytą užsakymą, pasirinkite jo eilutę ir pasirinkite nuorodą **Daugiau**.

## <a name="individual-shipping-container-tracking"></a>Individualaus gabenimo konteinerio sekimas

Užklausa **Vieno gabenimo konteinerio sekimas** pateikia filtrą, kuris leidžia rasti gabenimo konteinerį, o tada identifikuoti reiso eilutes tame konteineryje.

Kad atidarytumėte šią užklausą, eikite į **Iškrovimo kaina \> Užklausos \> Sekimas \> Vieno gabenimo konteinerio sekimas**.

## <a name="multiple-shipping-container-tracking"></a>Kelių gabenimo konteinerių sekimas

Užklausa **Kelių gabenimo konteinerių sekimas** pateikia filtrą, kuris leidžia rasti gabenimo konteinerį, o tada identifikuoti reiso eilutes tuose konteineriuose.

Kad atidarytumėte šią užklausą, eikite į **Iškrovimo kaina \> Užklausos \> Sekimas \> Kelių gabenimo konteinerių sekimas**.
