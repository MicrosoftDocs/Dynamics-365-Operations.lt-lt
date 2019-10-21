---
title: „Project Service Automation“ integravimo parametrai
description: Šioje temoje paaiškinama, kaip konfigūruoti numatytųjų duomenų įvedimo būdą integruojant „Microsoft Dynamics 365 for Project Service Automation“ su „Microsoft“ „Dynamics 365 Finance“.
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
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174963"
---
# <a name="project-service-automation-integration-parameters"></a>„Project Service Automation“ integravimo parametrai

[!include[banner](../includes/banner.md)]

Puslapyje **„Project Service Automation“ integravimo parametrai** galite konfigūruoti numatytųjų duomenų įvedimo būdą integruojant „Dynamics 365 Project Service Automation“ su „Dynamics 365 Finance“. Norėdami „Project Service Automation“ projektus sėkmingai sinchronizuoti su „Finance“, turite nustatyti toliau nurodytus laukus.

> [!NOTE]
> - Projektų užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiami 8.0 versijoje.
> - Faktinių duomenų integravimas pasiekiamas 8.0.1 arba naujesnėse versijose.


| Tab                    | Laukas                | Aprašymas |
|------------------------|----------------------|-------------|
| Bendri                | Numatytasis projekto tipas | Pasirinkite numatytąjį projekto tipą. Ši reikšmė naudojama sinchronizuojant projektus iš „Project Service Automation“, jei integravimo šablone nenurodėte numatytosios reikšmės. Atliekant sinchronizavimą, ši reikšmė nustatoma naujų projektų laukui **Projekto tipas**.  Visgi reikšmę galima atnaujinti projekto sutarties eilutes sinchronizavus iš „Project Service Automation“. |
|                        | Laiko kategorija        | Pasirinkti numatytąją laiko kategoriją. Ši reikšmė naudojama sinchronizuojant apytiksles grafiko reikšmes iš „Project Service Automation“. Kai apytikslės grafiko reikšmės ir faktinės grafiko reikšmės sinchronizuojamos iš „Project Service Automation“, ši reikšmė nustatoma naujo „Finance“ projekto grafiko prognozių laukui **Kategorija**. |
|                        | Mokesčių kategorija         | Pasirinkti numatytąją mokesčio kategoriją. Ši reikšmė naudojama sinchronizuojant faktines mokesčių reikšmes iš „Project Service Automation“. Kai faktinės mokesčių reikšmės sinchronizuojamos iš „Project Service Automation, ši reikšmė nustatoma naujų „Finance“ mokesčių operacijų laukui **Kategorija**. |
| Numatytosios projekto grupių reikšmės | Projekto tipas         | Spustelėkite **Nauja**, kad įtrauktumėte eilutę, kurioje galėtumėte pasirinkti projekto tipą, kuriam bus nustatoma numatytoji projekto grupė. Atliekant konfigūraciją konkretų projekto tipą galima pasirinkti tik vieną kartą. |
|                        | Projektų grupė        | Pasirinkite numatytąją projekto grupę pasirinkto projekto tipui. Sinchronizuojant naujus projektus iš „Project Service Automation“, laukui **Projekto grupė** numatytoji reikšmė nustatoma pagal projekto tipą, jei integravimo šablone nenurodėte numatytosios reikšmės. |
| Numatytosios atsiskaitymo tipų reikšmės  | Atsiskaitymo tipas         | Spustelėkite **Nauja**, kad įtrauktumėte eilutę, kurioje galėtumėte pasirinkti atsiskaitymo tipą, kuriam bus nustatoma numatytoji eilutės ypatybė. Atliekant konfigūraciją konkretų atsiskaitymo tipą galima pasirinkti tik vieną kartą. |
|                        | Eilutės ypatybė        | Pasirinkite numatytąją eilutės ypatybę pasirinkto atsiskaitymo tipui. Sinchronizuojant naujas apytiksles grafiko reikšmes, naujas apytiksles išlaidų reikšmes arba naujas faktines reikšmes iš „Project Service Automation“, laukui **Eilutės ypatybė** numatytoji reikšmė nustatoma pagal atsiskaitymo tipą. |
| Funkcijų užrakinimas  | Netaikoma       | Pasirinkite norimą išjungti iš „Project Service Automation“ sukurtų projektų ir sutarčių funkciją naudojantis „Finance“. Pavyzdžiui, galite išjungti galimybę naudojantis „Finance“ redaguoti sutartis ir projektus, kurti darbo paskirstymo struktūras ir įvesti tabelius. Su apskaita susiję laukai išliks įgalinti, net jei pakeičiant parametro nuostatą bus padaroma, kad jie būtų nepasiekiami. Pagal numatytuosius parametrus įgalinamos visos funkcijos. |
