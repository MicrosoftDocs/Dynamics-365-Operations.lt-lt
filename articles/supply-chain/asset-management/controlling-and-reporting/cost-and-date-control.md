---
title: Kaštų ir datos valdymas
description: Šioje temoje aiškinamas kaštų ir datos valdymas turto valdyme.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918400"
---
# <a name="cost-and-date-control"></a>Kaštų ir datos valdymas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Turto valdyme galite apskaičiuoti kaštus, kad galėtumėte peržiūrėti faktinius kaštus, palygintus su turto, funkcinių vietų ir darbo užsakymų biudžeto kaštais. Faktiniai kaštai pagrįsti užregistruotomis operacijomis. Taip galite apskaičiuoti datą, jei norite palyginti darbo užsakymų suplanuotas pradžios ir pabaigos datas su faktinėmis pradžios ir pabaigos datomis.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Turto, funkcinių vietų ir dar užsakymų kaštų valdymas

Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški. Vienintelis skirtumas – skaičiuodami turto ir funkcinių vietų valandas, galite įtraukti antrinį turtą ir antrines vietas. Data yra operacijos, kai registracija buvo įrašyta, data.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto kaštų valdymas** arba **Funkcinės vietos kaštų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo kaštų valdymas**.

2. Dialoge lange **Turto kaštų valdymas** / **Funkcinės vietos kaštų valdymas** / **Darbo užsakymo kaštų valdymas** pasirinkite skaičiuotiną periodą.

3. Jei reikia, pažymėkite finansinių matmenų rinkinį, kad jis būtų įtrauktas į skaičiavimą.

4. Perjungimo mygtuke **Praleisti nulį** pažymėkite Taip, jei nenorite, kad būtų rodomi nulinių kaštų rezultatai.

5. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti kaštų valdymo eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra turi kelių lygių hierarchiją, visos kaštų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, kaštų valdymo eilutes.

6. Perjungimo mygtuke **Rodyti atvirus patvirtintus** pažymėkite Taip, jei norite į skaičiavimą įtraukti tą stulpelį.

7. Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.

8. Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.

9. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

Toliau pateiktame paveiksle rodomas dialogo langas **Turto kaštų valdymas**.

![1 pav.](media/01-controlling-and-reporting.png)

10. Puslapyje **Turto kaštų valdymas** veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti veiksmų srities mygtukai yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

Toliau pateiktame paveiksle rodomas rezultatų **Turto kaštų valdymas** pavyzdys.

![2 paveikslėlis](media/02-controlling-and-reporting.png)

Kitas būdas skaičiuoti kaštus – atlikti kelis pasirinkimus **Visas turtas** arba **Aktyvus turtas**. Tada skirtuke **Bendra** spustelėkite mygtuką **Kaštų valdymas**. Dialogo lange **Turto kaštų valdymas** pažymėtas turtas yra automatiškai įtraukiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**. Spustelėkite **Gerai** ir rodomas pasirinkto turto kaštų skaičiavimas. Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

>[!NOTE]
>Lauke **Originalus biudžetas** rodomi biudžeto kaštai iš darbo užsakymo prognozės. Lauke **Patvirtinti kaštai** rodoma bendra išlaidų suma, kurią juridinis asmuo įsipareigojo sau sumokėti. Laukuose **Atviri patvirtinti kaštai** rodomi įsipareigojimai sumokėti už elementus, valandas ir paslaugas, kurias užsakėte arba gavote, bet neapmokėjote. Kai visos naudojimo registracijos užregistruotos, susiję kaštai įtraukiami į lauką **Faktiniai kaštai**.

## <a name="work-order-date-control"></a>Darbo užsakymo datos kontrolė

Naudokite šį puslapį, kad galėtumėte peržiūrėti numatytas pradžios ir pabaigos datas, palygintas su darbo užsakymų pradžios ir pabaigos datomis.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo datos valdymas**.

2. Spustelėkite **Skaičiuoti**.

3. Lauke **Funkcinė sritis** pažymėkite funkcinę vietą.

4. Laukuose **Nuo datos** ir **Iki datos** įveskite laikotarpį, pagal kurį norite atlikti skaičiavimą. Bus įtraukti visi darbo užsakymai su laikotarpyje numatyta pradžia.

5. Spustelėkite **Gerai**.

6. Veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti veiksmų srities mygtukai yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

Toliau pateiktame paveiksle rodomas rezultatų **Darbo užsakymo datos valdymas** pavyzdys.

![3 paveikslėlis](media/03-controlling-and-reporting.png)

- Lauke **Vid. pradžios delsa** rodomas dienų tarp darbo užsakymo suplanuotos pradžios datos, palygintos su faktine pradžios data, skirtumas. Jei, pavyzdžiui, faktinė pradžios data buvo dvi dienos iki suplanuotos pradžios datos, lauke bus rodoma „-2“.  
- Lauke **Vid. pabaigos delsa** rodomas dienų tarp darbo užsakymo suplanuotos pabaigos datos, palygintos su faktine pabaigos data, skirtumas. Jei, pavyzdžiui, faktinė pabaigos data buvo trys dienos iki suplanuotos pabaigos datos, lauke bus rodoma „3“.  
- Laukuose **Įvykiai** rodomas laiko nuokrypių, susijusių su darbo užsakymo suplanuota ir faktine pradžios data ir suplanuota ir faktine pradžios data, skaičius.

