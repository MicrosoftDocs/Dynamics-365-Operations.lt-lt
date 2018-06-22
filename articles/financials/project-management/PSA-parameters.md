---
title: "„Project Service Automation“ integravimo parametrai"
description: "Galite konfigūruoti, kaip turėtų būti numatomi duomenys integruojant „Project Service Automation“ su „Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>„Project Service Automation“ integravimo parametrai

Puslapyje **„Project Service Automation“ integravimo parametrai** galite konfigūruoti, kaip turėtų būti numatomi duomenys integruojant „Project Service Automation“ su „Finance and Operations“. Norint „Project Service Automation“ projektus sėkmingai sinchronizuoti su „Finance and Operations“, būtina nustatyti toliau nurodytus parametrus.

> [!NOTE]
> Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.




| **Skirtukas**                      | **Laukas**                          | **Aprašas**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Bendra**                  | **Numatytasis projekto tipas**               | Pasirinkite numatytąją reikšmę **Projekto tipas**, t. y. projektus sinchronizuojant iš „Project Service Automation“, jei integravimo šablone nenurodėte numatytosios reikšmės. Atliekant sinchronizavimą ši reikšmė bus nustatyta naujų projektų parinkčiai **Projekto tipas** ir ją galima atnaujinti sinchronizuojant projekto sutarties eilutes iš „Project Service Automation“.               |
| **Bendra**                  | **Laiko kategorija**                      | Pasirinkite numatytąją parinkties **Laiko kategorija** reikšmę, t. y. kai apytikslės grafiko reikšmės sinchronizuojamos iš „Project Service Automation“. Sinchronizuojant naujo „Finance and Operations“ projekto grafiko prognozes ši reikšmė bus nustatyta parinkčiai **Kategorija**, kai apytikslės grafiko reikšmės ir faktinės grafiko reikšmės sinchronizuojamos iš „Project Service Automation“.   |
| **Bendra**                  | **Mokesčių kategorija**                       | Pasirinkite numatytąją parinkties **Mokesčų kategorija** reikšmę, t. y. kai faktinės mokesčių reikšmės sinchronizuojamos iš „Project Service Automation“. Sinchronizuojant naujų „Finance and Operations“ mokesčių operacijas ši reikšmė bus nustatyta parinkčiai **Kategorija**, kai faktinės mokesčių reikšmės sinchronizuojamos iš „Project Service Automation“.          |
| **Numatytosios projekto grupių reikšmės**   | **Projekto tipas** | Norėdami įtraukti eilutę, kurioje galėtumėte pasirinkti projekto tipą, kuriam bus nustatoma numatytoji projekto grupė, spustelėkite **Nauja**. Atliekant konfigūraciją konkretų projekto tipą galima pasirinkti tik vieną kartą.              
|                              | **Projektų grupė**          | Pasirinkite konkretaus projekto tipo numatytąją projekto grupę. Sinchronizuojant naujus projektus iš „Project Service Automation“ parinktis **Projekto grupė** bus numatytoji pagal projekto tipą, jei integravimo šablone nenurodėte numatytosios reikšmės.  |
| **Numatytosios atsiskaitymo tipų reikšmės**    | **Atsiskaitymo tipas** | Norėdami įtraukti eilutę, kurioje galėtumėte pasirinkti atsiskaitymo tipą, kuriam bus nustatoma numatytoji eilutės ypatybė, spustelėkite **Nauja**. Atliekant konfigūraciją konkretų atsiskaitymo tipą galima pasirinkti tik vieną kartą.          |
|                              | **Eilutės ypatybė**| Pasirinkite konkretaus atsiskaitymo tipo numatytąją eilutės ypatybę. Sinchronizuojant naujas apytiksles grafiko reikšmes, naujas apytiksles išlaidų reikšmes arba naujas faktines reikšmes iš „Project Service Automation“ parinktis **Eilutės ypatybė** bus numatytoji pagal atsiskaitymo tipą.          |
| **Funkcijų užrakinimas**    |                   | Pasirinkite norimą išjungti iš „Project Service Automation“ sukurtų projektų ir sutarčių funkciją naudojantis „Finance and Operations“. Pavyzdžiui, galite išjungti galimybę naudojantis „Finance and Operations“ redaguoti sutartis ir projektus, kurti darbo paskirstymo struktūras ir įvesti tabelius. Su apskaita susiję laukai išliks įgalinti, net jei pakeičiant parametro nuostatą bus padaroma, kad jie būtų nepasiekiami. Pagal numatytuosius parametrus įgalinamos visos funkcijos.           |

