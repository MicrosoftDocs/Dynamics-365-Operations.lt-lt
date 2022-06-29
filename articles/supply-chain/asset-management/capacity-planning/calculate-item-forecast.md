---
title: Elemento prognozės atskaičiavimas
description: Šiame straipsnyje paaiškinama, kaip apskaičiuoti prekės prognozę turto valdymo dalyje.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016107"
---
# <a name="calculate-item-forecast"></a>Apskaičiuoti elemento prognozę

[!include [banner](../../includes/banner.md)]

 

Taip, kaip galite atlikti pajėgumo skaičiavimus, aprašytus ankstesniame skyriuje, taip pat galite skaičiuoti toliau nurodytų elementų prognozes:

- priežiūros grafiko eilutės  
- darbo užsakymai, kurie dar nėra suplanuoti  
- suplanuoti darbo užsakymai

Tai naudinga, jei norite peržiūrėti numatytą elementų naudojimą (atsarginių dalių ir kitų elementų, kurių reikia norint įvykdyti darbo užsakymą) konkrečiu periodu. Galima apskaičiuoti viso turto arba pasirinkto turto elementų prognozę. Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklą (**Visos prižiūrimo turto prastovos veiklos** arba **Aktyvios prižiūrimo turto prastovos veiklos**) arba darbo užsakymų telkinį (**Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**).

1. **Spustelėkite Turto** > **·** > **·** **·** > **·** > **·** / **valdymo** užklausos Prekės prognozė arba Turto valdymo darbo užsakymų telkiniai Visi darbo užsakymų telkiniai Aktyvūs darbo užsakymų telkiniai > sąraše >**Prekės** prognozės mygtuke pasirinkite darbo užsakymų telkinį, **·** > **arba turto valdymo tvarkymo downtime** > **veikla Visos priežiūros downtime** / **veiklos Aktyvi** priežiūros downtime veikla > pasirinkite priežiūros downtime veiklą sąraše > Prekės **prognozės** mygtukas.

2. Dialoge **Skaičiuoti elemento prognozę** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.

3. Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti priežiūros grafiko eilutes.

4. Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti darbo užsakymo užduotis.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti elementų prognozės eilutėse. 

      Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. 
  
      Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.

6. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

7. Grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Toliau pateiktoje ekrano kopijoje pasirinkti mygtukai **Grupuoti pagal** yra pažymėti mėlynai. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

8. Spustelėkite mygtuką **Rodyti matmenis**, jei norite matyti elementus, susijusius su produktu, saugykla arba sekimo matmenimis. Pažymėkite atitinkamus žymės langelius ir spustelėkite **Gerai**.

![1 iliustracija.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]