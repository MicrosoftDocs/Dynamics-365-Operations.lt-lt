---
title: Suvartojimo registravimas
description: Šiame straipsnyje paaiškinama, kaip registruoti suvartojimą turto valdymo dalyje.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 729ef6aae228ad1e528945031567b92c44cdf256
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111761"
---
# <a name="register-consumption"></a>Suvartojimo registravimas

[!include [banner](../../includes/banner.md)]

 

Kai pagal darbo užsakymą atliekama priežiūros užduotis, kitas veiksmas – registruoti suvartojimą ir skelbti žurnalus. Galite registruoti šiuos suvartojimo tipus: valandas, prekes ir išlaidas. Skirtingi suvartojimo tipai registruojami ir skelbiami puslapyje **Darbo užsakymo žurnalai**. Modulio **Turto valdymas** žurnalo sąranka naudojama atskiriems valandų, prekių ir išlaidų žurnalams kurti ir skelbti modulyje **Projekto valdymas ir apskaita**.

Kai kuriais atvejais turėsite galimybę įtraukti arba pašalinti darbo užsakymo prognozės eilutes. Darbo užsakymo ciklo būsenos sąranka, susijęs projekto tipas ir su projekto tipu susijusios etapo taisyklės nulemia tai, ar galite įtraukti arba redaguoti žurnalo eilutes. Daugiau apie darbo užsakymo ciklo būsenas ir susijusius projekto etapus skaitykite [Prognozės, darbo užsakymai ir projektai](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Galima nustatyti, kad žurnalai būtų automatiškai skelbiami darbo užsakymo ciklo būsenoje. Daugiau informacijos rasite [Darbo užsakymų ciklo būsenos](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Spustelėkite **Turto valdymo darbo** > **užsakymai Visi** > **darbo užsakymai arba** Aktyvūs **darbo užsakymai**.

2. Pasirinkite darbo užsakymą ir spustelėkite **Žurnalai**.

3. Spustelėkite **Kopijuoti iš prognozės**, kad būtų perkeltos bet kokios prognozės eilutės, kurios gali būti sujungtos su darbo užsakymu. Galite pasirinkti, kuriuos suvartojimo tipus norite perkelti.

4. Jei reikia, atitinkamame „FastTab“ galite įtraukti daugiau suvartojimo eilučių spustelėję **Įtraukti eilutę** ir eilutėje įvedę duomenis.

5. Norėdami patikrinti žurnalo eilutes prieš paskelbiant, spustelėkite **Tikrinti žurnalus**.

6. Spustelėkite **Skelbti žurnalus**, kad skelbtumėte žurnalo eilutes.

7. Paskelbę suvartojimo žurnalus galite atnaujinti darbo užsakymo ciklo būseną. Pavyzdžiui, norėdami nurodyti, kad darbo užsakymas buvo baigtas, galite atnaujinti ciklo būseną į „Baigta“.

    - Lauke **Rodyti**, esančiame puslapio **Darbo užsakymo žurnalai** viršuje, pasirinkite, kurias žurnalo eilutes norite matyti: **Visas**, **Nepaskelbtas** arba **Paskelbtas**. Jei žurnalas paskelbtas, žymės langelyje **Paskelbta** yra varnelė.  
    - Kai darbo užsakymo žurnale sukuriamos prekės eilutės, su preke susijusios produkto dimensijos ir sekimo dimensijos automatiškai perkeliamos į žurnalo eilutę.  

Toliau pateiktoje ekrano kopijoje matomas darbo užsakymo valandų ir prekių registracijų **darbo užsakymo žurnaluose** pavyzdys.

![1 iliustracija.](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Darbo užsakymų su keliomis darbo užsakymo užduotimis valandų padalijimas

Jei darbo užsakyme yra kelios darbo užsakymo užduotys, darbo valandas galite registruoti naudodami funkciją **Padalyti valandas**, t. y., viena valandos registracijos eilutė gali būti vienodai padalyta kiekvienai darbo užsakymo užduočiai.

1. Spustelėkite **Turto valdymo darbo** > **užsakymai Visi** > **darbo užsakymai arba** Aktyvūs **darbo užsakymai**.

2. Pasirinkite darbo užsakymą ir spustelėkite **Žurnalai**.

3. Pasirinkite valandų registracijos eilutę, kurią norite padalyti, ir spustelėkite **Padalyti valandas**.

4. Dialogo lango **Padalyti valandas darbo užsakymo priežiūros užduotims** lauke **Darbuotojas** automatiškai rodomas prisijungusio darbuotojo vardas. Jei reikia, galite pasirinkti kitą darbuotoją.

5. Lauke **Kategorija** pasirinkite valandų registravimo kategoriją.

6. Lauke **Valandos** įrašykite darbo valandų, kurias norite padalyti, skaičių.

    ![2 iliustracija.](media/02-consumption.png)

7. Spustelėkite **Gerai**.

*Pavyzdys:* Toliau pateiktoje ekrano kopijoje matomos darbo užsakymo, kuriame yra trys darbo užsakymo užduotys, žurnalo eilutės. Pirmoji eilutė, kurioje yra trys valandos, buvo padalyta, ir kiekvienoje darbo užsakymo užduotyje užregistruojama viena darbo valanda. Sukūrus tris valandų registracijos eilutes galite nuspręsti, ką daryti su pradine valandų registracijos eilute (pirmoji eilutė pavyzdyje). Galite ją palikti arba ištrinti. 

![3 iliustracija.](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Suvartojimo registracijų finansinės dimensijos

Registruojant suvartojimą į registracijas konkrečia seka įtraukiamos finansinės dimensijos, susijusios su skirtingais registravimo tipais. 

- *Valandų ir išlaidų registracijos:* jei yra, pirmiausia įtraukiamos žurnalo antraštės finansinės dimensijos. Tada įtraukiamos susijusio darbo užsakymo projekto finansinės dimensijos. Galiausiai įtraukiamos išteklių (darbuotojo) finansinės dimensijos.

- *Prekių registracijos:* jei yra, pirmiausia įtraukiamos žurnalo antraštės finansinės dimensijos. Tada įtraukiamos susijusio darbo užsakymo projekto finansinės dimensijos. Tada įtraukiamos vietos finansinės dimensijos. Galiausiai įtraukiamos prekės finansinės dimensijos.

>[!NOTE]
>Visuose trijuose registracijų tipuose patikrinamas finansinių dimensijų derinys, o netinkami deriniai uždengiami. Tai standartinis nustatymas su kitomis finansų ir operacijų programėle.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
