---
title: Kelių atkarpų veiklos ciklo nustatymas
description: Šioje temoje aprašoma, kaip nustatyti kelių atkarpų veiklos ciklus modulyje Iškrovimo kaina.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 045ded1fb881b0572f4490ab3a5d4ca1cb8c341a4d245e6d98991228a90aadb7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774083"
---
# <a name="multi-leg-journey-setup"></a>Kelių atkarpų veiklos ciklo nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti kelių atkarpų veiklos ciklus modulyje **Iškrovimo kaina**.

## <a name="legs"></a>Atkarpos

Atkarpos naudojamos atskiroms veiklos ciklo dalims identifikuoti. Kiekviena atkarpa kuriama pasirenkant kilmės ir paskirties uostus bei gabenimo būdą, naudojamą tos atkarpos metu. Su kiekviena atkarpa galima susieti gamybos laiką. Gamybos laikas gali padėti sekti siuntą ir taip pat gali būti naudojamas apskaičiuoti numatomą reiso prekių pristatymo datą. Be to, kai veiklos ciklo atkarpa baigta, reiso būseną, gabenimo konteinerį ir susijusias pirkimo užsakymo eilutes galima atnaujinti naudojant sekimo kontrolės sąranką. Atkarpas galima naudoti viename veiklos ciklo šablone arba pakartotinai naudoti keliuose veiklos ciklo šablonuose. Konteinerio pakrovimas, muitinės ir vietinis transportas paprastai nustatomi kaip atkarpos ir jiems naudojamas nekonkretus uostas.

Norėdami dirbti su atkarpomis, eikite į **Iškrovimo kaina \> Kelių atkarpų veiklos ciklo nustatymas \> Atkarpos**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti atkarpų įrašus. Šioje lentelėje apibūdinami galimi kiekvieno įrašo laukeliai.

| Laukas | aprašymas |
|---|---|
| Atkarpa | Įveskite unikalų veiklos ciklo atkarpos identifikavimo pavadinimą / numerį. |
| Aprašymas | Įveskite veiklos ciklo atkarpos aprašymą. Paprastai šis aprašymas nurodo kilmės ir paskirties uostus arba veiklos ciklo etapą. |
| Kilmės uostas | Įveskite atkarpos prekių kilmės vietą. |
| Paskirties uostas | Įveskite atkarpos prekių paskirties vietą. |
| Pristatymo metodas | Įvesti atkarpos gabenimo būdą. |

## <a name="journey-templates"></a>Kelionės šablonai

Veiklos ciklo šablonas apibrėžia kelių atkarpų veiklos ciklą tarp dviejų uostų, kurio metu gabenamos reiso prekės. Veiklos ciklo atkarpos sujungiamos, kad būtų galima nustatyti laiką, kurio prireiks prekėms nugabenti iš tiekėjo kilmės vietos į galutinį paskirties sandėlį. Kai atkarpos veiklos ciklo šablone pateikiamos tam tikra tvarka, gamybos laikas identifikuoja kiekvienos atkarpos datą ir reiso būseną, konteinerį bei reiso pirkimo eilutes. Naudokite [sekimo kontrolės centrą](delivery-information-setup.md), norėdami nustatyti gamybos laiką, susijusį su kiekviena atkarpa, kuri sudaro veiklos ciklo šabloną. Taip pat veiklos ciklo šablonas naudojamas, kai nustatomos automatinės reiso išlaidos. Apibrėžiant veiklos ciklą, išlaidas, susijusias su prekių gabenimu, galima nurodyti automatinių išlaidų puslapyje.

Norėdami dirbti su veiklos ciklų šablonais, eikite į **Iškrovimo kaina \> Kelių atkarpų kelionės nustatymas \> Veiklos ciklų šablonai**. Ten galite peržiūrėti, atidaryti, kurti ir naikinti veiklos ciklų šablonus.

Nustatykite kiekvieno veiklos ciklo šablono toliau pateiktus antraštės laukus.

| Laukas | aprašymas |
|---|---|
| Kelionės šablonas | Įveskite unikalų veiklos ciklo šablono identifikavimo pavadinimą / numerį. Paprastai veiklos ciklo šablonas apibūdina veiklos ciklo kilmės vietą ir paskirties vietą. |
| Aprašymas | Įveskite veiklos ciklo šablono aprašymą. Paprastai aprašyme nurodomi kilmės ir paskirties uostai bei kelionės tipas. |

Skyriuje **Eilutės** įtraukite kiekvienos veiklos ciklo atkarpos eilutę ir pateikite eilutes teisinga tvarka. Norėdami pakeisti eilučių tvarką, naudokite įrankių juostos rodykles **Aukštyn** ir **Žemyn**. Šioje lentelėje apibūdinami galimi kiekvienos eilutės laukai.

| Laukas | Aprašymas |
|---|---|
| Atkarpa | Pasirinkite atkarpą, kurią norite įtraukti į veiklos ciklą. |
| Aprašymas | Atkarpos aprašymas. |
| Kilmės uostas | Atkarpos prekių kilmės uostas. Šis uostas yra paskirties uostas, naudojamas reiso automatinėms išlaidoms nustatyti. |
| Paskirties uostas | Atkarpos prekių galutinis paskirties uostas. |
| Pristatymo būdas | Atkarpai naudojamas pristatymo būdas. |
| Veiklos ciklo kilmės uostas | Jei atkarpai nurodytas uostas naudojamas automatinėms išlaidoms nustatyti, pažymėkite šį žymės langelį, norėdami identifikuoti jį kaip veiklos ciklo kilmės uostą. Šis uostas bus rodomas reiso antraštėje. |
| Veiklos ciklo paskirties uostas | Jei atkarpai nurodytas uostas naudojamas automatinėms išlaidoms nustatyti, pažymėkite šį žymės langelį, norėdami identifikuoti jį kaip veiklos ciklo paskirties uostą. Šis uostas bus rodomas reiso antraštėje. |
| Gabenimo įmonė | Pasirinkite atkarpai naudojamą siuntimo įmonę. |

## <a name="activities"></a>Veiklos

Puslapio **Veiklos** parametrai nustato veiklų, kurios gali įvykti atkarpos paskirties uoste, tipus. Vartotojai, kurie dirba puslapyje **Visi gabenimo konteineriai**, įvertindami kiekvienos veiklos trukmę ir įrašydami faktinę palyginimui skirtą trukmę, gali rinktis iš šių verčių.

Norėdami nustatyti jūsų veiklas, eikite į **Iškrovimo kaina \> Kelių atkarpų veiklos ciklų nustatymas \> Veiklos**. Ten galite įtraukti, pašalinti ir redaguoti veiklas naudodami veiksmų srities mygtukus.

Šioje lentelėje apibūdinami galimi kiekvienos veiklos tinklelio laukai.

| Laukas | Aprašymas |
|---|---|
| Veikla | Veiklos pavadinimas. |
| Aprašymas | Veiklos aprašymas. |
| Gabenimo įmonė | Su veikla susietos siuntimo įmonės tiekėjo sąskaita. |
