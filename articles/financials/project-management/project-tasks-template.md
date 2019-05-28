---
title: Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“
description: Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557929"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduotume įdiegti ir KB 4131710.
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto užduotis srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablonai ir užduotys

Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Project Service Automation“ projekto užduotis su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto užduotys (iš PSA į „Fin and Ops“)
- **Užduoties pavadinimas projekte:** projekto užduotys

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | „Finance and Operations”              |
|----------------------------|-------------------------------------|
| Projekto užduotys              | Projekto užduoties integravimo objektas |

## <a name="entity-flow"></a>Objekto srautas

Projekto užduotys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto veiklos.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="power-query"></a>„Power Query“

Esant toliau nurodytai sąlygai filtruojant duomenis būtina naudoti „Microsoft Power Query“, skirtą „Excel“.

- Projekto užduotyje yra konkrečiam ištekliui būdingų įrašų.

Jei naudojate „Power Query“, vykdykite šį nurodymą:

- Projekto užduočių (PSA ir „Fin and Ops“) šablone naudojamas numatytasis filtras, kuris neįtraukia konkrečiam ištekliui būdingų projekto užduoties įrašų, nustatant **IsLineTask** filtro parinktį **Klaidinga**. Norint sukurti savo šabloną būtina įtraukti šį filtrą.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimų pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
