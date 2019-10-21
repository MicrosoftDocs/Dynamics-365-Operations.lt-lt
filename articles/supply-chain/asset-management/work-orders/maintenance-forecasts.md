---
title: Priežiūros prognozės
description: Šioje temoje aprašomos priežiūros prognozės modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024504"
---
# <a name="maintenance-forecasts"></a>Priežiūros prognozės

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Kai sukuriate darbo užsakymą, sukuriate darbo užsakymo užduotis su susijusiu turtu ir priežiūros užduočių tipais. Kai pasirenkate priežiūros užduoties tipą, kuriame yra priežiūros prognozių, prognozės automatiškai nukopijuojamos į darbo užsakymą.

Galbūt turėsite galimybę įtraukti arba pašalinti darbo užsakymo prognozės eilutes. Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti prognozės eilutes. 

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Sąraše pasirinkite darbo užsakymą ir spustelėkite **Prognozė**. Pasirinkus **Darbo užsakymo priežiūros prognozė**, rodomos priežiūros užduoties tipo, pasirinkto darbo užsakymo užduotyje, prognozės eilutės.


## <a name="add-hours-forecast-to-a-work-order"></a>Valandų prognozės įtraukimas į darbo užsakymą

1. Pažymėkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

2. Norėdami sukurti naują eilutę, FastTab **Valandos** spustelėkite **Įtraukti**.

3. Lauke **Kategorija** pasirinkite kategoriją.

4. Į lauką **Valandos** įterpkite prognozuojamų valandų skaičių.

5. Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.


## <a name="add-items-forecast-to-a-work-order"></a>Prekių prognozės įtraukimas į darbo užsakymą

Yra trys būdai įtraukti prekes į darbo užsakymo priežiūros prognozę: galite kurti į atsarginių dalių sąrašą arba turto KS neįtrauktų prekių (atsarginių dalių) eilutes, galite pasirinkti atsargines dalis iš patvirtinto atsarginių dalių sąrašo ir galite pasirinkti prekes iš turto KS.

1. Pažymėkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

2. Pasirinkite FastTab **Prekės**.

3. Spustelėję **Įtraukti**, įtraukite naują atsarginės dalies, neįtrauktos į atsarginių dalių sąrašą arba turto KS sąrašą, eilutę.

4. Lauke **Prekės numeris** pasirinkite prekę.

5. Lauke **Pardavimo kiekis** įterpkite kiekį, o lauke **Vienetas** pasirinkite kiekio vienetą.

6. Į atitinkamus laukus įterpkite savikainą ir valiutą ir pasirinkite **Eilutės ypatybė**.

7. Jei norite pakeisti prekės eilutėse rodomų dimensijų sąrašą, spustelėkite **Atsargos** > **Rodyti dimensijas**, pasirinkite dimensijas, paskui perjungimo mygtuke **Įrašyti sąranką** pasirinkite „Taip”.

8. Jei į priežiūros prognozę norite įtraukti patvirtintą atsarginę dalį, spustelėkite **Įtraukti atsarginių dalių**, pasirinkite atsarginę dalį, jei reikia, pakoreguokite susijusią informaciją ir spustelėkite **Gerai**.

9. Jei į prognozę norite įtraukti turto KS prekių, spustelėkite **Įtraukti KS prekių**, pasirinkite prekę, jei reikia, pakoreguokite susijusią informaciją ir spustelėkite **Gerai**.

10. Spustelėkite **Kur naudota prekė**, jei norite pamatyti, kur pasirinktoje eilutėje esanti prekė naudojama modulyje Turto valdymas turto, priežiūros užduoties tipo numatytųjų reikšmių, atsarginių dalių ir darbo užsakymų atžvilgiu. 



## <a name="add-expense-forecast-to-a-work-order"></a>Išlaidų prognozės įtraukimas į darbo užsakymą

1. Šioje temoje aiškinama, kaip įtraukti išlaidų prognozę į darbo užsakymą. Formos kairėje pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

2. Pasirinkite FastTab **Išlaidos**.

3. Sukurkite naują eilutę, spustelėję **Įtraukti**.

4. Lauke **Kategorija** pasirinkite kategoriją.

5. Lauke **Kiekis** įterpkite kiekį.

6. Į atitinkamus laukus įterpkite savikainą, pardavimo valiutą ir pardavimo kainą.

7. Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.

>[!NOTE]
>FastTab **Priežiūros prognozių sumos** matote pasirinktos darbo užsakymo užduoties ir darbo užsakymo kiekviename skirtuke sukurtų eilučių skaičiaus apžvalgą. Taip pat matote darbo užsakymo užduoties ir darbo užsakymo prognozuojamų darbo valandų sumą.

![1 pav.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Darbo užsakymo prognozių automatinis naujinimas

Modulyje Turto valdymas galima automatiškai naujinti darbo užsakymų prognozių informaciją apie valandos kainas, prekių kainas ir išlaidas, kuri buvo atnaujinta kituose moduliuose. Tai daroma siekiant užtikrinti, kad darbo užsakymų prognozėse naudojamos aktualiausios savikainos. Taip pat galima naujinti ir [priežiūros užduočių tipo prognozes](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Spustelėkite **Turto valdymas** > **Periodinis** > **Prognozė** > **Naujinti darbo užsakymo prognozę**.

2. Išplečiamajame dialogo lange **Naujinti darbo užsakymo prognozę**, jei reikia, galite pasirinkti parametrus, susijusius su konkrečiais darbo užsakymais arba darbo užsakymų užduotimis. Norėdami pasirinkti, spustelėkite **Filtras**.

3. Jei reikia, galite nustatyti automatinio naujinimo paketinę užduotį FastTab **Vykdyti fone**.

4. Spustelėjus **Gerai**, pradedamas prognozės naujinimas.


![2 paveikslėlis](media/07-work-orders.png)

