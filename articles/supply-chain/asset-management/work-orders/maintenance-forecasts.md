---
title: Priežiūros prognozės
description: Šioje temoje aprašomos priežiūros prognozės modulyje Turto valdymas.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6503d5110a4cb5e4041afa7b4e80395b2974a64e5a150eb6bfce1f32a6703e06
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761859"
---
# <a name="maintenance-forecasts"></a>Priežiūros prognozės

[!include [banner](../../includes/banner.md)]



Kai sukuriate darbo užsakymą, sukuriate darbo užsakymo užduotis su susijusiu turtu ir priežiūros užduočių tipais. Kai pasirenkate priežiūros užduoties tipą, kuriame yra priežiūros prognozių, prognozės automatiškai nukopijuojamos į darbo užsakymą.

Galbūt galėsite įtraukti prognozės eilutes į darbo užsakymą arba panaikinti jas iš darbo užsakymo. Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti prognozės eilutes. Daugiau informacijos apie darbo užsakymo ciklo būsenas ir susijusius projekto etapus žr. [Prognozės, darbo užsakymai ir projektai](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Pasirinkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Sąraše pasirinkite darbo užsakymą, tada veiksmų srityje > skirtuke **Darbo užsakymas** > grupėje **Projektas**, pasirinkite **Prognozė**. Puslapyje **Darbo užsakymo priežiūros prognozė** rodomos priežiūros užduoties tipo, pasirinkto darbo užsakymo užduotyje, prognozės eilutės.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Valandų prognozės įtraukimas į darbo užsakymą

1. Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

2. Norėdami sukurti naują eilutę, „FastTab” **Valandos** pasirinkite **Įtraukti**.

3. Lauke **Kategorija** pasirinkite kategoriją.

4. Į lauką **Valandos** įterpkite prognozuojamų valandų skaičių.

5. Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.


## <a name="add-an-items-forecast-to-a-work-order"></a>Prekių prognozės įtraukimas į darbo užsakymą

Yra trys būdai, kaip įtraukti prekes į darbo užsakymo priežiūros prognozę. Galite kurti į atsarginių dalių sąrašą arba turto KS neįtrauktų prekių (atsarginių dalių) eilutes, galite pasirinkti atsargines dalis iš patvirtinto atsarginių dalių sąrašo ir galite pasirinkti prekes iš turto KS.

- Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

- „FastTab” **Prekės**, naudodami tinkamą metodą, įtraukite prekes į priežiūros prognozę.

Norėdami įtraukti atsarginės dalies, neįtrauktos į atsarginių dalių sąrašą arba turto KS sąrašą, eilutę atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Įtraukti**.
2. Lauke **Elemento numeris** pasirinkite elementą.
3. Lauke **Pardavimo kiekis** įveskite kiekį.
4. Lauke **Vienetas** pasirinkite kiekio matavimo vienetą.
5. Laukuose **Savikaina** ir **Valiuta** įveskite tinkamas vertes.
6. Lauke **Eilutės ypatybė** pasirinkite eilutės ypatybę.
7. Jei norite pakeisti prekės eilutėse rodomų dimensijų sąrašą, pasirinkite **Atsargos** > **Rodyti dimensijas**, pasirinkite dimensijas, paskui nustatykite parinktį **Įrašyti sąranką** į **Taip**.

Norėdami įtraukti atsarginę dalį iš patvirtintų atsarginių dalių sąrašo, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Įtraukti atsarginių dalių**.
2. Pasirinkite atsarginę dalį ir pagal poreikį redaguokite susijusią informaciją.
3. Pasirinkite **Gerai**.

Norėdami įtraukti prekę iš turto KS, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Įtraukti KS prekių**.
2. Pasirinkite prekę ir pagal poreikį redaguokite susijusią informaciją.
3. Pasirinkite **Gerai**.

Jei norite apžvelgti, kur naudojama prekė pasirinktoje eilutėje atsižvelgiant į turtą, priežiūros užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus turto valdyme, pasirinkite **Kur naudota prekė**. Daugiau informacijos apie šią apžvalgą žr. [Kur naudota prekė](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Išlaidų prognozės įtraukimas į darbo užsakymą

1. Puslapyje **Darbo užsakymo priežiūros prognozė** pasirinkite darbo užsakymo užduotį, į kurią norite įtraukti prognozę.

2. Norėdami sukurti eilutę, „FastTab” **Išlaidos** pasirinkite **Įtraukti**.

3. Lauke **Kategorija** pasirinkite kategoriją.

4. Lauke **Kiekis** įveskite kiekį.

5. Laukuose **Savikaina**, **Pardavimo valiuta** ir **Pardavimo kaina** įveskite tinkamas vertes.

6. Lauke **Eilutės ypatybė** pasirinkite eilutėje naudotiną išlaidų tipą.

>[!NOTE]
>„FastTab” **Priežiūros prognozių sumos** rodoma pasirinktos darbo užsakymo užduoties ir darbo užsakymo kiekviename „FastTab” sukurtų eilučių skaičiaus apžvalga. Taip pat rodoma darbo užsakymo užduoties ir darbo užsakymo prognozuojamų darbo valandų suma.

Toliau pateiktame paveikslėlyje parodytas puslapio **Darbo užsakymo priežiūros prognozė** pavyzdys.

![1 iliustracija.](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Darbo užsakymo prognozių automatinis naujinimas

Turto valdyme galima automatiškai naujinti darbo užsakymų prognozių informaciją apie valandines išlaidas, prekių kainas ir išlaidas, jei ji buvo atnaujinta kituose „Microsoft Dynamics 365 for Finance and Operations“ moduliuose. Ši galimybė padeda užtikrinti, kad darbo užsakymų prognozėse naudojamos aktualiausios savikainos. Taip pat galima naujinti ir [priežiūros užduočių tipo prognozes](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Pasirinkite **Turto valdymas** > **Periodinis** > **Prognozė** > **Naujinti darbo užsakymo prognozę**.

2. Dialogo lange **Naujinti darbo užsakymo prognozę**, „FastTab” **Įtrauktini įrašai**, pagal poreikį galite pasirinkti parametrus, susijusius su konkrečiais darbo užsakymais arba darbo užsakymų užduotimis. Norėdami atlikti reikiamus pasirinkimus, spustelėkite **Filtras**.

3. FastTab **Vykdyti fone** pagal poreikį galite nustatyti automatinio naujinimo paketinę užduotį.

4. Pasirinkus **Gerai**, pradedamas prognozės naujinimas.


Toliau pateiktame paveikslėlyje parodytas dialogo lango **Naujinti darbo užsakymo prognozę** pavyzdys.

![2 iliustracija.](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]