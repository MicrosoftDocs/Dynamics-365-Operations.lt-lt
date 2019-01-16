---
title: "„Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>„Finance and Operations“ atsargų lygio informacijos sinchronizavimas su „Field Service“ 

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų lygio informaciją su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ turimų atsargų lygius su „Microsoft Dynamics 365 for Field Service“.

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**
- Produktų atsargos („Finance and Operations“ su „Field Service“)
  
**Užduočių pavadinimai projekte Duomenų integravimas:**
- Produktų atsargos

Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sandėliai („Finance and Operations“ su „Field Service“) 
- „Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“) 

## <a name="entity-set"></a>Objektų rinkinys

| Field Service                      | „Finance and Operations”                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS turimos atsargos pagal sandėlį     |

## <a name="entity-flow"></a>Objekto srautas
Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“. Atsargų lygio informacija apima: 
- Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)
- Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, t. y. pardavimo užsakymų kiekis)
- Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, t. y. pirkimo užsakymų kiekis)

Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.

„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems „Finance and Operations“ lygius, gauti.

„Finance and Operations“ veiks kaip atsargų lygių ruošinys. Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į „Finance and Operations“, jei šis funkcionalumas naudojamas „Field Service“ kartu su „Finance and Operations“ atsargų lygių sinchronizavimu.

Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal „Finance and Operations“, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).

Pastaba. Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį „Tvarkomas išoriškai = Ne“), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą. Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tiesiog siųstų naujinimus į „Finance and Operations“. Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų. Papildomos informacijos žr. „Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“ ir „Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais“.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Išorinio produkto atsargų objektas yra naujas objektas, naudojamas tik vidiniam integravimui. Gaunamos „Finance and Operations“ integravimo atsargų lygio vertės, kurios paskui transformuojamos į atsargų žurnalus rankiniu būdu, o vėliau keičia atsargų produktus sandėlyje. 

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="in-the-data-integration-project"></a>Duomenų integravimo projekte
Taikykite filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik pageidaujami produktai ir sandėliai siųstų atsargų lygio informaciją iš „Finance and Operations“ į „Field Service“.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Produktų atsargos („Finance and Operations“ su „Field Service“): produktų atsargos

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

