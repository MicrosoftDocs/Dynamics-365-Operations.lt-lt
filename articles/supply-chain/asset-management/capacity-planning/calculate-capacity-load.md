---
title: Skaičiuoti pajėgumą
description: Šiame straipsnyje paaiškinama, kaip apskaičiuoti turto valdymo pajėgumo apkrovą.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95d1e38db8e4658a57f36139836264b87d525e61
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016136"
---
# <a name="calculate-capacity-load"></a>Pajėgumo skaičiavimas

[!include [banner](../../includes/banner.md)]


Turto valdyme galite apskaičiuoti pajėgumą šiems elementams:

- priežiūros grafiko eilutės  
- darbo užsakymai, kurie dar nėra suplanuoti  
- suplanuoti darbo užsakymai

Tai naudinga, jei norite peržiūrėti numatytą pajėgumą konkrečiu laikotarpiu. Galima apskaičiuoti viso turto arba pasirinkto turto pajėgumą. Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklas arba darbo užsakymų telkinius.

1. **·** > **·** > **·** **·** > **·** > **·** / **Spustelėkite** Turto valdymo užklausos Pajėgumas arba Turto valdymo darbo užsakymų telkiniai Visi darbo užsakymų telkiniai Aktyvūs darbo užsakymų telkiniai > sąraše >**Pajėgumo** įkelties mygtukas pasirinkite darbo užsakymų telkinį, **·** > **arba turto valdymo tvarkymo downtime** > **veikla Visa priežiūros downtime** / **veikla** Aktyvi priežiūros downtime veikla > pasirinkite priežiūros veiklą sąraše > Mygtukas **Pajėgumas**.

2. Dialoge **Skaičiuoti pajėgumą** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.

3. Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į skaičiavimą įtraukti priežiūros grafiko eilutes.

4. Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į skaičiavimą įtraukti darbo užsakymo užduotis.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti pajėgumo eilutėse. 

    Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. 
    
    Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.

6. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

7. Grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Toliau pateiktoje ekrano kopijoje pasirinkti mygtukai **Grupuoti pagal** yra pažymėti mėlynai. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

    ![1 iliustracija.](media/01-capacity-planning.png)

>[!NOTE]
>Jei norite planuoti tik suplanuotų darbo užsakymų pajėgumą, žr. [Suplanuotų darbo užsakymų pajėgumo skaičiavimas](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]