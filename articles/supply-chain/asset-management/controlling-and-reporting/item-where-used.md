---
title: Kur naudota prekė
description: Šioje temoje aiškinama, kaip sužinoti, kur prekė naudojama modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918331"
---
# <a name="item-where-used"></a>Kur naudota prekė

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Galite atlikti tam tikros prekės apskaičiavimą, kad sužinotumėte, kur prekė panaudota modulyje Turto valdymas. Gavus rezultatus, pateikiamas kontekstas, kuriame prekė buvo naudota per egzistavimo laikotarpį. Puslapį **Kur naudota prekė** galima atsiversti naudojant pagrindinį modulio Turto valdymas meniu; minėtą puslapį taip pat galima pasiekti atsivertus toliau pateikiamus puslapius.

[Turto KS](../objects/object-BOM.md)

[Turto tipo numatytųjų reikšmių atsarginės dalys](../setup-for-objects/object-types.md)

[Priežiūros užduočių tipų numatytųjų reikšmių prognozės prekės prognozė](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[Darbo užsakymo priežiūros prognozė](../work-orders/maintenance-forecasts.md)

[Darbo užsakymo pirkimo paraiška](../work-orders/procurement.md)

[Darbo užsakymo pirkimas](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Apskaičiavimo Kur naudota prekė atlikimas

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Kur naudota prekė** arba pasirinkite mygtuką **Kur naudota prekė** viename iš pirmiau minėtų puslapių.

2. Dialogo lange **Kur naudota prekė** lauke **Prekės numeris** pasirinkite prekę, kurios apskaičiavimą norite atlikti.

3. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti prekės eilutėse. Pavyzdžiui, jei lauke įrašysite skaičių „1“ ir funkcinių vietų struktūroje yra keletas lygių, visos funkcinės vietos prekės eilutės bus rodomos aukščiausiame lygyje. Todėl eilutės ryšys / kiekis gali būti žemesniame lygyje esančių funkcinių vietų suma. Jei lauke **Lygis** įrašysite skaičių „0“, matysite išsamų rezultatą, rodantį visas prekių eilutes visuose funkcinių vietų lygiuose, su kuriais jos yra susijusios.

4. Skyriuje **Įtraukti** perjungimo mygtukuose, kuriuos norite įtraukti į apskaičiavimą, pasirinkite Taip.

5. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

6. Skirtuke **Kur naudota prekė** veiksmų srities grupėse **Grupuoti pagal...** pasirinkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas apskaičiavimo išsamumo lygis. Pažymėti veiksmų srities mygtukai yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

7. Spustelėkite **Rodyti dimensijas**, jei norite matyti dimensijas, susijusias su preke, ir pasirinkite rodytinas dimensijas.

Toliau pateiktame paveikslėlyje rodomas apskaičiavimo Kur naudota prekė, kai prekių skaičius yra „1000“, pavyzdys.

![1 pav.](media/12-controlling-and-reporting.png)

