---
title: Kur naudota prekė
description: Šioje temoje aiškinama, kaip sužinoti, kur prekė naudojama modulyje Turto valdymas.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2308fc4fabe541b8affeba5860a3154f81e8903e4853fd36d777f15a503d9dd8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752831"
---
# <a name="item-where-used"></a>Kur naudota prekė

[!include [banner](../../includes/banner.md)]

 

Galite atlikti tam tikros prekės apskaičiavimą, kad sužinotumėte, kur prekė panaudota modulyje Turto valdymas. Gavus rezultatus, pateikiamas kontekstas, kuriame prekė buvo naudota per egzistavimo laikotarpį. Puslapį **Kur naudota prekė** galima atsiversti naudojant pagrindinį modulio Turto valdymas meniu; minėtą puslapį taip pat galima pasiekti atsivertus toliau pateikiamus puslapius.

- [Turto KS](../objects/object-BOM.md)

- [Turto tipo numatytųjų reikšmių atsarginės dalys](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [Priežiūros užduoties tipo kategorijos ir priežiūros užduočių tipai, priežiūros užduočių tipo variantai, priežiūros užduočių prekyba ir prižiūrimo turto kontroliniai sąrašai](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [Priežiūros prognozė](../work-orders/maintenance-forecasts.md)

- [Įsigijimas](../work-orders/procurement.md)

- [Darbo užsakymo pirkimas](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a>Apskaičiavimo Kur naudota prekė atlikimas

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Kur naudota prekė** arba pasirinkite mygtuką **Kur naudota prekė** viename iš pirmiau minėtų puslapių.

2. Dialogo lange **Kur naudota prekė** lauke **Prekės numeris** pasirinkite prekę, kurios apskaičiavimą norite atlikti.

3. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti prekės eilutėse. 

    Pavyzdžiui, jei lauke įrašysite skaičių „1“ ir funkcinių vietų struktūroje yra keletas lygių, visos funkcinės vietos prekės eilutės bus rodomos aukščiausiame lygyje. Todėl eilutės ryšys / kiekis gali būti žemesniame lygyje esančių funkcinių vietų suma. 
    
    Jei lauke **Lygis** įrašysite skaičių „0“, matysite išsamų rezultatą, rodantį visas prekių eilutes visuose funkcinių vietų lygiuose, su kuriais jos yra susijusios.

4. Skyriuje **Įtraukti** perjungimo mygtukuose, kuriuos norite įtraukti į apskaičiavimą, pasirinkite Taip.

5. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

6. Skirtuke **Kur naudota prekė** pasirinkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas apskaičiavimo išsamumo lygis. Pažymėti mygtukai **Grupuoti pagal** yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

7. Spustelėkite **Rodyti dimensijas**, jei norite matyti dimensijas, susijusias su preke, ir pasirinkite rodytinas dimensijas.

## <a name="example"></a>Pavyzdys

Toliau pateiktoje ekrano kopijoje rodomas apskaičiavimo Kur naudota prekė, kai prekių skaičius yra „1000“, pavyzdys.

![Apskaičiavimo Kur naudota prekė pavyzdys.](media/12-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]