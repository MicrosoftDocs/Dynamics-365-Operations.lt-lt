---
title: „Project Service Automation“ integravimo parametrai
description: Šioje temoje paaiškinama, kaip konfigūruoti numatytųjų duomenų įvedimo būdą integruojant „Microsoft Dynamics 365 for Project Service Automation“ su „Microsoft Dynamics 365 for Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838996"
---
# <a name="project-service-automation-integration-parameters"></a>„Project Service Automation“ integravimo parametrai

[!include[banner](../includes/banner.md)]

Puslapyje **„Project Service Automation“ integravimo parametrai** galite konfigūruoti numatytųjų duomenų įvedimo būdą integruojant „Microsoft Dynamics 365 for Project Service Automation“ su „Microsoft Dynamics 365 for Finance and Operations“. Norėdami „Project Service Automation“ projektus sėkmingai sinchronizuoti su „Finance and Operations“, turite nustatyti toliau nurodytus laukus.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduotume įdiegti ir KB 4131710.

| Skirtukas                    | Laukas                | aprašymas |
|------------------------|----------------------|-------------|
| Bendri                | Numatytasis projekto tipas | Pasirinkite numatytąjį projekto tipą. Ši reikšmė naudojama sinchronizuojant projektus iš „Project Service Automation“, jei integravimo šablone nenurodėte numatytosios reikšmės. Atliekant sinchronizavimą, ši reikšmė nustatoma naujų projektų laukui **Projekto tipas**.  Visgi reikšmę galima atnaujinti projekto sutarties eilutes sinchronizavus iš „Project Service Automation“. |
|                        | Laiko kategorija        | Pasirinkti numatytąją laiko kategoriją. Ši reikšmė naudojama sinchronizuojant apytiksles grafiko reikšmes iš „Project Service Automation“. Kai apytikslės grafiko reikšmės ir faktinės grafiko reikšmės sinchronizuojamos iš „Project Service Automation“, naujo „Finance and Operations“ projekto grafiko prognozių reikšmė bus nustatyta laukui **Kategorija**,  |
|                        | Mokesčių kategorija         | Pasirinkti numatytąją mokesčio kategoriją. Ši reikšmė naudojama sinchronizuojant faktines mokesčių reikšmes iš „Project Service Automation“. Kai faktinės mokesčių reikšmės sinchronizuojamos iš „Project Service Automation, ši reikšmė nustatoma naujų „Finance and Operations“ mokesčių operacijų laukui **Kategorija**. |
| Numatytosios projekto grupių reikšmės | Projekto tipas         | Spustelėkite **Nauja**, kad įtrauktumėte eilutę, kurioje galėtumėte pasirinkti projekto tipą, kuriam bus nustatoma numatytoji projekto grupė. Atliekant konfigūraciją konkretų projekto tipą galima pasirinkti tik vieną kartą. |
|                        | Projektų grupė        | Pasirinkite numatytąją projekto grupę pasirinkto projekto tipui. Sinchronizuojant naujus projektus iš „Project Service Automation“, laukui **Projekto grupė** numatytoji reikšmė nustatoma pagal projekto tipą, jei integravimo šablone nenurodėte numatytosios reikšmės. |
| Numatytosios atsiskaitymo tipų reikšmės  | Atsiskaitymo tipas         | Spustelėkite **Nauja**, kad įtrauktumėte eilutę, kurioje galėtumėte pasirinkti atsiskaitymo tipą, kuriam bus nustatoma numatytoji eilutės ypatybė. Atliekant konfigūraciją konkretų atsiskaitymo tipą galima pasirinkti tik vieną kartą. |
|                        | Eilutės ypatybė        | Pasirinkite numatytąją eilutės ypatybę pasirinkto atsiskaitymo tipui. Sinchronizuojant naujas apytiksles grafiko reikšmes, naujas apytiksles išlaidų reikšmes arba naujas faktines reikšmes iš „Project Service Automation“, laukui **Eilutės ypatybė** numatytoji reikšmė nustatoma pagal atsiskaitymo tipą. |
| Funkcijų užrakinimas  | Netaikoma       | Pasirinkite norimą išjungti iš „Project Service Automation“ sukurtų projektų ir sutarčių funkciją naudojantis „Finance and Operations“. Pavyzdžiui, galite išjungti galimybę naudojantis „Finance and Operations“ redaguoti sutartis ir projektus, kurti darbo paskirstymo struktūras ir įvesti tabelius. Su apskaita susiję laukai išliks įgalinti, net jei pakeičiant parametro nuostatą bus padaroma, kad jie būtų nepasiekiami. Pagal numatytuosius parametrus įgalinamos visos funkcijos. |
