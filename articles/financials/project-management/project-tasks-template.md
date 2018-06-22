---
title: "„Project Service Automation“ projekto užduočių sinchronizavimas"
description: "Šioje temoje aprašomas šablonas ir pagrindinė užduotis, naudojama „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>„Project Service Automation“ tiesioginis sinchronizavimas su „Finance and Operations“ projekto veiklomis

Šioje temoje aprašomas šablonas ir pagrindinė užduotis, naudojama „Microsoft Dynamics 365 for Project Service Automation“ projekto užduotis tiesiogiai sinchronizuojant su „Dynamics 365 for Finance and Operations“.

> [!NOTE]
> Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonu, kuris pasiekiamas naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto užduotis srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablonai ir užduotys

Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Project Service Automation“ projekto užduotis su „Finance and Operations“.

-**Duomenų integravimo šablono pavadinimas:** Projekto užduotys (PSA ir „Fin and Ops“) -**Projekto užduoties pavadinimas:** Projekto užduotys

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="entity-set"></a>Objektų rinkinys

|„Project Service Automation“               | „Finance and Operations”                |
|-----------------------------------------|---------------------------------------|
| Projekto užduotys                           | Projekto užduoties integravimo objektas.   |

## <a name="entity-flow"></a>Objekto srautas

Projekto užduotys tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto veiklos.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Norint sinchronizuoti projekto užduotis būtina sinchronizuoti projekto sutartis ir projektus.

## <a name="power-query"></a>„Power Query“

Esant toliau nurodytoms sąlygoms filtruojant duomenis būtina naudoti „Microsoft Power Query“.

- Esama konkrečiam ištekliui būdingų projekto užduoties įrašų.

Jei naudojate „Power Query“, vykdykite toliau išvardytus nurodymus.

- Projekto užduočių (PSA ir „Fin and Ops“) šablone naudojamas numatytasis filtras, skirtas neįtraukti konkrečiam ištekliui būdingų projekto užduoties įrašų, nustatant **IsLineTask** filtro parinktį **Klaidinga**. Norint sukurti savo šabloną būtina įtraukti šį filtrą.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimų pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


