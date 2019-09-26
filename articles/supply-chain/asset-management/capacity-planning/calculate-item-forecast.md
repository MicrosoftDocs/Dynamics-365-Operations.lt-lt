---
title: Apskaičiuoti elemento prognozę
description: Šioje temoje aiškinama, kaip skaičiuoti elemento prognozę turto valdyme.
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886775"
---
# <a name="calculate-item-forecast"></a>Apskaičiuoti elemento prognozę

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kaip galite atlikti pajėgumo skaičiavimus, aprašytus ankstesniame skyriuje, taip pat galite skaičiuoti toliau nurodytų dalykų elementų prognozes:

- Priežiūros grafiko eilutės  
- Darbo užsakymai, kurie dar nėra suplanuoti  
- Suplanuoti darbo užsakymai

Tai naudinga, jei norite peržiūrėti numatytą elementų naudojimą (atsarginių dalių ir kitų elementų, kurių reikia norint įvykdyti darbo užsakymą) konkrečiu periodu. Galima apskaičiuoti viso turto arba pasirinkto turto elementų prognozę. Taip pat galite skaičiuoti prižiūrimo turto prastovos veiklą (**Visos prižiūrimo turto prastovos veiklos** arba **Aktyvios prižiūrimo turto prastovos veiklos**) arba darbo užsakymų telkinį (**Visi darbo užsakymų telkiniai** arba **Aktyvūs darbo užsakymų telkiniai**).

1. Spustelėkite mygtuką **Turto valdymas** > **Užklausos** > **Elemento prognozė** arba **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymų telkiniai** > **Visi darbo užsakymų telkiniai** / **Aktyvių darbo užsakymų telkiniai** >pasirinkti darbo užsakymų telkinį sąraše > **Elemento prognozė** arba mygtuką **Turto valdymas** > **Bendrieji dalykai** > **Prižiūrimo turto prastovos veiklos** > **Visos prižiūrimo turto prastovos veiklos** / **Aktyvios prižiūrimo turto prastovos veiklos** > pasirinkti prižiūrimo turto prastovos veiklą sąraše > **Elemento prognozė**.

2. Dialoge **Skaičiuoti elemento prognozę** laukuose **Pradžios data/laikas** ir **Pabaigos data/laikas** pažymėkite skaičiavimo laikotarpį.

3. Perjungimo mygtuke **Įtraukti priežiūros grafiką** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti priežiūros grafiko eilutes.

4. Perjungimo mygtuke **Įtraukti darbo užsakymą** pažymėkite Taip, jei norite į prognozės skaičiavimą įtraukti darbo užsakymo užduotis.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti elementų prognozės eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visos priežiūros grafikos eilutės ir darbo užsakymai, skirti funkcinei vietai, bus rodomi viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, visas priežiūros grafiko eilutes ir visus darbo užsakymus.

6. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

7. Veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pasirinktos veiksmų srities grupės mygtukai yra paryškinti mėlynai. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

8. Spustelėkite mygtuką **Rodyti matmenis**, jei norite matyti elementus, susijusius su produktu, saugykla arba sekimo matmenimis. Pažymėkite atitinkamus žymės langelius ir spustelėkite **Gerai**.

Paveiksle toliau pateikta šios sąsajos ekrano kopija.

![1 pav.](media/02-capacity-planning.png)