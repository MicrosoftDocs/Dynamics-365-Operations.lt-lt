---
title: Tiesioginis „Project Service Automation“ projekto sutarčių ir projektų sinchronizavimas su „Finance and Operations“
description: Šioje temoje aprašomas šablonas ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ projekto sutartis ir projektus su „Microsoft Dynamics 365 for Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561467"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Tiesioginis „Project Service Automation“ projekto sutarčių ir projektų sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas šablonas ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ projekto sutartis ir projektus su „Microsoft Dynamics 365 for Finance and Operations“.

> [!NOTE] 
> Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition“ 7.3.0 versiją, turite įdiegti KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

> [!NOTE]
> Prieš naudodamiesi integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu turite susipažinti su „Microsoft Dynamics 365“ funkcija Duomenų integravimas.

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto sutartis, projektus, projekto sutarčių eilutes ir projekto sutarties eilutės etapus srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant „Project Service Automation“ projekto sutartis ir projektus su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projektai ir sutartys (iš PSA į „Fin and Ops“)
- **Užduočių pavadinimas projekte**

    - Projekto sutartys iš PSA į „Fin and Ops“
    - Projektai iš PSA į „Fin and Ops“
    - Projekto sutarties eilutės iš PSA į „Fin and Ops“
    - Projekto sutarties eilutės etapai iš PSA į „Fin and Ops“

Norint sinchronizuoti projekto sutartis ir projektus, būtina sinchronizuoti sąskaitas.

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“       | „Finance and Operations”                                 |
|----------------------------------|--------------------------------------------------------|
| Užsakymai                           | Projekto sutarties integravimo objektas                |
| Projektai                         | Projekto integravimo objektas                         |
| Užsakymo eilutės                      | Projekto sutarties eilutės integravimo objektas           |
| Projekto sutarties eilučių etapai | Projekto sutarties eilutės etapo integravimo objektas |

## <a name="entity-flow"></a>Objekto srautas

Projekto sutartys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto sutartys. Integravimo šablone galite nustatyti projekto sutarties integavimo į „Finance and Operations“ šaltinį.

Laiko ir medžiagų projektas ir fiksuotos kainos projektai tvarkomi naudojantis „Project Service Automation“ ir yra sinchronizuojami su „Finance and Operations“ kaip projektai. Atlikdami šablono integravimą galite nustatyti projekto integavimo į „Finance and Operations“ šaltinį.

Projekto sutarties eilutės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto sutarties atsiskaitymo taisyklės. Jei atsiskaitymo būdas skiriasi nuo numatytojo projekto tipo, atliekant sinchronizavimą bus atnaujintas sutarties eilutės projekto ir projekto grupės projekto tipas.

Projekto sutarties eilutės etapai tvarkomi naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto sutarties atsiskaitymo taisyklės etapai.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimas

Laukas **Projekto sutarties ID** galimas puslapyje **Projekto sutartys**. Šis laukas sukurtas kaip srities ir unikalus raktas integracijai palaikyti.

Sukūrus naują projekto sutartį, bet nesant vertės **Projekto sutarties ID**, ji automatiškai sugeneruojama naudojant numeraciją. Vertę sudaro raidės **ORD**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **ORD-01022-Z4M9Q0**.

Laukas **Projekto numeris** galimas puslapyje **Projektai**. Šis laukas sukurtas kaip srities ir unikalus raktas integracijai palaikyti.

Sukūrus naują projektą, bet nesant vertės **Projekto numeris**, ji automatiškai sugeneruojama naudojant numeraciją. Vertę sudaro raidės **PRJ**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **PRJ-01049-CCNID0**.

Taikant integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimą<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, naujinimo scenarijus nustato esamų projekto sutarčių lauką **Projekto sutarties ID** ir esamų „Project Service Automation“ projektų lauką **Projekto numeris**.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

- Norint sinchronizuoti projekto sutartis ir projektus, būtina sinchronizuoti sąskaitas.
- Savo ryšio rinkinyje įtraukite integravimo rakto lauko **msdyn\_organizationalunits** susiejimą su lauku **msdyn\_name \[Name\]**. Pirmiausia į ryšių rinkinį gali prireikti įtraukti projektą. Daugiau informacijos rasite [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Savo ryšio rinkinyje įtraukite integravimo rakto lauko **msdyn\_projects** susiejimą su lauku **msdynce\_projectnumber \[Project Number\]**. Pirmiausia į ryšių rinkinį gali prireikti įtraukti projektą. Daugiau informacijos rasite [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Galima atnaujinti projekto sutarčių ir projektų **SourceDataID** vertę arba pašalinti iš susiejimo. Numatytoji šablono vertė yra **„Project Service Automation“**.
- Būtina atnaujinti susiejimą **PaymentTerms**, kad jis atitiktų galimas „Finance and Operations“ mokėjimo sąlygas. Taip pat galite pašalinti susiejimą iš projekto užduoties. Numatytosios vertės susiejimui priskirtos numatytosios demonstracinių duomenų vertės. Toliau pateikiamoje lentelėje nurodomos „Project Service Automation“ vertės.

    | Vertė | aprašymas   |
    |-------|---------------|
    | 1     | Grynoji 30        |
    | 2     | 2 % 10, grynoji 30 |
    | 3     | Grynoji 45        |
    | 4     | Grynoji 60        |

## <a name="power-query"></a>„Power Query“

Esant toliau nurodytoms sąlygoms filtruojant duomenis būtina naudoti „Microsoft Power Query“, skirtą „Excel“.

- Turite „Microsoft Dynamics 365 for Sales“ pardavimo užsakymų.
- Turite kelis „Project Service Automation“ organizacijos vienetus ir šie organizacijos vienetai bus susieti su keliais „Finance and Operations“ juridiniais subjektais.

Jei naudojate „Power Query“, vykdykite toliau išvardytus nurodymus.

- Projektų ir sutarčių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuris apima tik tuos pardavimo užsakymus, kurių tipas **Darbo elementas (msdyn\_ordertype = 192350001)**. Šis filtras padeda užtikrinti, kad naudojant „Finance and Operations“ pardavimo užsakymų projekto sutartys nekuriamos. Norint sukurti savo šabloną būtina įtraukti šį filtrą.
- Turite sukurti „Power Query“ filtrą, apimantį tik tas sutarties organizacijas, kurios turi būti sinchronizuojamos su integracijos ryšių rinkinio juridiniu subjektu. Pavyzdžiui, su „Contoso US“ sutarties organizacijos vienetu sudarytos jūsų projekto sutartys turėtų būti sinchronizuojamos su USSI juridiniu subjektu, tačiau su „Contoso Global“ sutarties organizacijos vienetu sudarytos sutartys turėtų būti sinchronizuojamos su USMF juridiniu subjektu. Neįtraukus šio filtro į užduoties susiejimą visos projekto sutartys bus sinchronizuojamos su nurodytu ryšio rinkinio juridiniu subjektu, nepriklausomai nuo sutarties organizacijos vieneto.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE] 
> Laukai **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ir **AddressZipCode** į numatytąjį projekto sutarčių susiejimą neįtraukti. Prireikus šiuos duomenis sinchronizuoti su projekto sutartimis galite įtraukti susiejimų.
>
> Laukai **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ir **ProjectType** į numatytąjį projektų siejimą neįtraukti. Prireikus šiuos duomenis sinchronizuoti su projektais galite įtraukti susiejimų.

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Šablono susiejimas](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Šablono susiejimas](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Šablono susiejimas](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
