---
title: Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“
description: Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Microsoft“ „Dynamics 365 Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 Finance“.
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
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770271"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Tiesioginis „Project Service Automation“ projekto užduočių sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas šablonas ir pagrindinė užduotis, kurie naudojami „Dynamics 365 Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 Finance“.

> [!NOTE]
> - Projektų užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiami 8.0 versijoje.
> - Jei naudojate „Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduotume įdiegti ir KB 4131710.
> - Faktinių duomenų integravimas pasiekiamas 8.0.1 arba naujesnėse versijose.

## <a name="data-flow-for-project-service-automation-to-finance"></a>„Project Service Automation“ duomenų srautas į „Finance“

Sprendime „Project Service Automation“ ir „Finance“ integravimas naudojama duomenų sinchronizavimo funkcija duomenims „Project Service Automation“ ir „Finance“ egzemplioriuose sinchronizuoti. Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto užduotis srautas iš „Project Service Automation“ į „Finance“.

Toliau esančiame paveikslėlyje pavaizduotas duomenų sinchronizavimas tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ integravimo su „Finance“ duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablonai ir užduotys

Norėdami atidaryti šabloną, „Microsoft Power Apps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant „Project Service Automation“ faktines projekto reikšmes su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto užduotys (iš PSA į „Fin and Ops“)
- **Užduoties pavadinimas projekte:** projekto užduotys

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | Finansai                             |
|----------------------------|-------------------------------------|
| Projekto užduotys              | Projekto užduoties integravimo objektas |

## <a name="entity-flow"></a>Objekto srautas

Projekto užduotys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance“ kaip projekto veiklos.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="power-query"></a>„Power Query“

Esant toliau nurodytai sąlygai filtruojant duomenis būtina naudoti „Microsoft Power Query“, skirtą „Excel“.

- Projekto užduotyje yra konkrečiam ištekliui būdingų įrašų.

Jei naudojate „Power Query“, vykdykite šį nurodymą:

- Projekto užduočių (PSA ir „Fin and Ops“) šablone naudojamas numatytasis filtras, kuris neįtraukia konkrečiam ištekliui būdingų projekto užduoties įrašų, nustatant **IsLineTask** filtro parinktį **Klaidinga**. Norint sukurti savo šabloną būtina įtraukti šį filtrą.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimų pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma „Project Service Automation“ laukų informacija, kuri bus sinchronizuojama su „Finance“.

[![Šablono susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
