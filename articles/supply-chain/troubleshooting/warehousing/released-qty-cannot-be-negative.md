---
title: Negalima atnaujinti apkrovos linijos, nes išleistas kiekis būtų neigiamas
description: Ši problema kyla, kai apkrovos linijos atnaujinimas arba panaikinimas sukels neigiamą išleistą kiekį.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728464"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Negalima atnaujinti apkrovos linijos, nes išleistas kiekis būtų neigiamas

Klaidos kodas: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Požymiai

Ši problema kyla, kai apkrovos linijos atnaujinimas arba panaikinimas sukels neigiamą išleistą kiekį. Šiuo atveju, kai bandote atnaujinti ar panaikinti apkrovos liniją, sistema rodo šį klaidos pranešimą:

> Patvirtintas prekės %1, partijos %2 kiekis negali būti neigiamas.

Todėl negalima atnaujinti ar panaikinti apkrovos linijos.

## <a name="cause"></a>Priežastis

Atnaujinus arba panaikinus apkrovos liniją, sistema atnaujina susijusios pardavimo eilutės išleidimo kiekį (*whsSalesLine.ReleaseQty*). Sistema įvertina paleistus kiekius ir jeigu nustato, kad paleistų eilučių kiekis po atnaujinimo bus neigiamas, eilutė nebus atnaujinta ar panaikinta. Šis tikrinimas vyksta kaskart bandant atnaujinti krovinio eilutės kiekį arba matavimo vienetą, atliekant įvairius veiksmus, tokius kaip, naikinti krovinio eilutę, naikinti siuntą, keisti krovinio eilutės kiekį, sumažinti paimtą kiekį ir greitą paėmimą.

Dažniausia šios problemos šakninė priežastis yra vienetų konvertavimo, kuris naudojamas atidarytoms krovinio eilutėms, pakeitimas. Pavyzdžiui, vieneto konvertavimas, kai buvo išleistas pardavimo užsakymas, buvo *50 Ea = 1 PL*. Tačiau prieš tai, kai susijusi krovinio siunta buvo baigta, vieneto konvertavimas buvo pakeistas į *100 Ea = 1 PL*.

## <a name="resolution"></a>Sprendimas

Sprendimas yra grąžinti vienetų konvertavimo pakeitimus, atnaujinti arba panaikinti krovinio eilutę ir tada iš naujo įdiegti konvertavimą. Turite apsaugoti kitus krovinius, kuriuose yra prekė, kuri sukėlė problemą, iki tol, kol problema bus ištaisyta. Kitu atveju nauji konvertavimai gali būti naudojami kitiems jau atidarytiems kroviniams.

Norėdami ištaisyti problemą atlikite vieną arba kelias iš toliau nurodytų užduočių:

1. Peržiūrėkite vieneto konvertavimą, kuris buvo naudojamas krovinio eilutėje.
2. Peržiūrėkite dabartinį prekės vieneto konvertavimą ir atlikite koregavimus, kurie įgalins krovinio eilutės atnaujinimą arba naikinimą.
3. Atnaujinkite arba panaikinkite krovinio eilutę ir grąžinkite vieneto konvertavimo koregavimus.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Peržiūrėkite vieneto konvertavimą, kuris buvo naudojamas krovinio eilutėje

Atlikite šią procedūrą, norėdami peržiūrėti krovinio eilutes ir pateikti pastabą apie vienetų konvertavimą, kuris buvo naudojamas krovinio eilutėje.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Pasirinkite krovinį, kuriame yra krovinio eilutė, kurios negalima panaikinti arba atnaujinti.
1. Veiksmų srities skirtuko **Pakrovimas** grupėje **Susijusi informacija** pasirinkite **Darbas**.
1. Viršutiniame tinklelyje pasirinkite reikiamą darbo ID.
1. Skirtuke **Bendras** puslapio apačioje, apskaičiuokite konvertavimo kursą tarp **Atsargų darbo kiekio** vertės ir **darbo kiekio** vertės. Pasižymėkite kursą.
1. Pakartokite šią procedūrą visiems atitinkamiems darbo ID, kad įsitikintumėte, jog buvo naudojamas tas pats konvertavimas.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Peržiūrėkite dabartinį prekės vieneto konvertavimą ir atlikite koregavimus

Naudokite toliau pateiktą procedūrą, kad peržiūrėtumėte produkto vieneto konvertavimą ir atliktumėte koregavimus, siekiant užtikrinti, kad vieneto konvertavimas yra sulygiuotas su krovinio eilute.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite susijusį produktą, jei norite eiti į **Išleisto produkto informacija** puslapį.
1. Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Vienetų konvertavimas**.
1. Pasirinkite vienetų konvertavimą ir atlikite koregavimus naudodami ankstesniame skyriuje nurodyta konvertavimo eiga.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Atnaujinkite arba panaikinkite krovinio eilutę ir grąžinkite vieneto konvertavimo koregavimus

Naudokite šią procedūrą, reikalaujant apdoroti krovinio eilutę ir grąžinti vienetų konvertavimą.

1. Eikite į **Sandėlio valdymas \> Kroviniai \> Visi kroviniai**.
1. Atidarykite krovinį, kuriame yra krovinio eilutė, kurios negalima panaikinti arba atnaujinti.
1. „FastTab” **Krovinio eilutės** patikrinkite pakrovimo eilutę.
1. Tęskite reikiamus veiksmus, kaip nurodyta. (Pvz., panaikinkite krovinio eilutę arba pakeiskite jos kiekį.)
1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite susijusį produktą, jei norite eiti į **Išleisto produkto informacija** puslapį.
1. Veiksmų srities skirtuko **Produktas** grupėje **Nustatyti** pasirinkite **Vienetų konvertavimas**.
1. Pasirinkite vienetų konvertavimą ir atšaukite koregavimus, kuriuos atlikote kaip nurodyta ankstesniame skyriuje.
