---
title: Skaičiuoti pajėgumą
description: Šioje temoje aiškinama, kaip išsiųsti apskaičiuoti pajėgumą turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886798"
---
# <a name="calculate-capacity-load"></a>Skaičiuoti pajėgumą

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Turto valdyme galite apskaičiuoti pajėgumą šiems elementams:

- priežiūros grafiko eilutės  
- darbo užsakymai, kurie dar nėra suplanuoti  
- suplanuoti darbo užsakymai

Tai naudinga, jei norite peržiūrėti numatytą pajėgumą konkrečiu laikotarpiu. Galima apskaičiuoti viso turto arba pasirinkto turto pajėgumą. Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklas arba darbo užsakymų telkinius.

1. Spustelėkite mygtuką **Turto valdymas** > **Užklausos** > **Pajėgumas** arba **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** / **Aktyvių darbo užsakymų telkiniai** >pasirinkti darbo užsakymų telkinį sąraše > **Pajėgumas** arba mygtuką **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos** / **Aktyvios prižiūrimo turto prastovos veiklos** > pasirinkti priežiūros veiklą sąraše > **Pajėgumas**.

2. Dialoge **Skaičiuoti pajėgumą** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.

3. Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į skaičiavimą įtraukti priežiūros grafiko eilutes.

4. Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į skaičiavimą įtraukti darbo užsakymo užduotis.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti pajėgumo eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.

6. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

7. Veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pasirinktos veiksmų srities grupės mygtukai yra paryškinti mėlynai. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

Toliau pateiktame paveiksle rodomas šios sąsajos pavyzdys.

![1 pav.](media/01-capacity-planning.png)

>[!NOTE]
>Jei norite planuoti tik suplanuotų darbo užsakymų pajėgumą, žr. [Suplanuotų darbo užsakymų pajėgumo planavimas](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).

