---
title: Neatitikimų sulaikymo zonos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti sulaikymo zonas neatitiktims.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ca74ec4586fffa3b9156aadab887629283b98a
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956763"
---
# <a name="quarantine-zones-for-nonconformances"></a>Neatitikimų sulaikymo zonos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti ir naudoti sulaikymo zonas neatitiktims.

Naudokite puslapį **Sulaikymo zonos**, kad apibrėžtumėte zonas, kurios gali būti priskirtos prie neatitikčių. Kai sukuriate neatitikčių formą, galite nustatyti sulaikymo zonos ir sulaikymo tipo laukus skirtuke Bendra, **kuris** **yra** **neatitikties** **puslapyje**. Sulaikymo **zonos laukas paprastai nurodo sritį ar** vietą, kurioje yra prekė. Lauke **Sulaikymo tipas prekė apibrėžiama kaip** Apribotas *naudojimas* arba *Nenaudojama*.

Kai spausdinate neatitikties arba neatitikties pataisų ataskaitą, galite peržiūrėti sulaikymo zoną, kurioje yra prekė.

Taip pat galite spausdinti neatitikties žymę. Ši ataskaita rodo priskirtą sulaikymo zoną ir informaciją apie naudojimą, kuri nurodo, kaip tvarkyti medžiagas su defektais. Karantino zonos gali atitikti atsargų vietas arba operacijų išteklius.

## <a name="examples-of-quarantine-zones"></a>Sulaikymo zonų pavyzdžiai

### <a name="example-1"></a>1 pavyzdys

Jūs dirbate elektroninėje gamybos įmonėje, kuri gamina ir paskirsto ttsirbatorius, anglų ir laikmenų gamybas. Tokiu atveju galite konfigūruoti sulaikymo zoną, kad ji atspindėtų kiekvieną produktų tipą.

### <a name="example-2"></a>2 pavyzdys

3 talpyklos ir du stelažai naudojami neatitikimo prekėms saugoti. Tokiu atveju galite konfigūruoti penkias sulaikymo zonas, po vieną kiekvienam talpyklos ir kiekvienam stelažai.

## <a name="create-a-quarantine-zone"></a>Sukurkite karantino zoną

1. Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Sulaikymo zonos**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Sulaikymo zona** – įveskite unikalų sulaikymo zonos ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų karantino zonos aprašą.

1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Darbuotojai, atsakingi už neatitikties tvirtinimą](quality-responsible-workers.md)
- [Neatitikimų diagnostikos problemos](quality-quarantine-zones.md)
- [Neatitikimų diagnostikos tipai](quality-diagnostic-types.md)
- [Neatitikimų kokybės mokesčiai](quality-charges.md)
- [Neatitikties operacijos](quality-operations.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
