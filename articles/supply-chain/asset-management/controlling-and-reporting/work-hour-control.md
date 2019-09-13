---
title: Darbo valandų valdymas
description: Šioje temoje paaiškinamas modulio Turto valdymas darbo valandų valdymas.
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
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918377"
---
# <a name="work-hour-control"></a>Darbo valandų valdymas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Modulyje Turto valdymas galite apskaičiuoti valandas, kad galėtumėte apžvelgti faktines valandas, palygintas su turto, funkcinių vietų ar darbo užsakymų biudžeto valandomis. Faktinės valandos yra pagrįstos užregistruotomis operacijomis.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Turto, funkcinių vietų ir darbo užsakymų darbo valandų valdymas

Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški. Vienintelis skirtumas – skaičiuodami turto ir funkcinių vietų valandas, galite įtraukti antrinį turtą ir antrines vietas. Data yra operacijos, kai registracija buvo įrašyta, data.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto valandų valdymas** arba **Funkcinių vietų valandų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymų valandų valdymas**.

2. Dialogo lange **Turto valandų valdymas**.

3. Dialogo lango **Turto valandų valdymas** / **Funkcinių vietų valandų valdymas** / **Darbo užsakymų valandų valdymas** laukuose **Pradžios data** ir **Pabaigos data** pasirinkite skaičiuotiną laikotarpį.

4. Jei reikia, pasirinkite, kad skaičiuojant būtų įtrauktas **finansinių dimensijų rinkinys**.

5. Perjungimo mygtuke **Praleisti nulį** pasirinkite Taip, jei nenorite, kad būtų rodomi nulinių valandų rezultatai.

6. Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti valandų valdymo eilutėse. Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinių vietų hierarchija yra kelių lygių, visos valandų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršutiniame lygyje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje esančių funkcinių vietų. Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, valandų valdymo eilutes.

7. Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.

8. Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.

9. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

10. Puslapio **Turto valandų valdymas** veiksmų srities grupėse **Grupuoti pagal...** spustelėkite atitinkamus mygtukus, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis. Pažymėti veiksmų srities mygtukai yra paryškinti. Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.

Toliau pateiktame paveiksle rodomas **turto valandų valdymo** skaičiavimo pavyzdys.

![1 pav.](media/04-controlling-and-reporting.png)

Kitas būdas skaičiuoti valandas – atlikti kelis pasirinkimus srityse **Visas turtas** arba **Aktyvus turtas**. Tada reikia spustelėti „FastTab“ **Bendra** mygtuką **Valandų valdymas**. Pasirinktas turtas automatiškai įterpiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**. Dialogo lange **Turto valandų valdymas** spustelėkite **Gerai** – bus rodomas pasirinkto turto skaičiavimas. Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

>[!NOTE]
>Lauke **Pradinis biudžetas** rodomos biudžeto valandos iš darbo užsakymo prognozės. Lauke **Faktinės valandos** rodomos darbo užsakymuose užregistruotos valandos. Lauke **Skirtos valandos** rodomos visos valandos, kurias jūsų įmonė skyrė pagal darbo užsakymus.

