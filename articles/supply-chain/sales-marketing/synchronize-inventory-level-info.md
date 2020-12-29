---
title: Tiekimo grandinės valdymo atsargų lygio informacijos sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 1228339c12d26f7b91875d15f0daa8da2869cba0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433476"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Tiekimo grandinės valdymo atsargų lygio informacijos sinchronizavimas su „Field Service“ 

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdyme turimų atsargų lygius su „Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Produktų atsargos (iš Tiekimo grandinės valdymo į „Field Service“)
  
**Užduotis projekte Duomenų integravimas**
- Produktų atsargos

Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“) 
- „Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“) 

## <a name="entity-set"></a>Objektų rinkinys

| „Field Service“                      | Tiekimo grandinės valdymas                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS turimos atsargos pagal sandėlį     |

## <a name="entity-flow"></a>Objekto srautas
Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“. Atsargų lygio informacija apima 
- Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)
- Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, pvz., pardavimo užsakymų kiekis)
- Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, pvz., pirkimo užsakymų kiekis)

Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.

„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems Tiekimo grandinės valdymo lygius, gauti.

Tiekimo grandinės valdymas veiks kaip atsargų lygių ruošinys. Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į Tiekimo grandinės valdymą, jei šis funkcionalumas naudojamas „Field Service“ kartu su Tiekimo grandinės valdymo atsargų lygių sinchronizavimu.

Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal Tiekimo grandinės valdymą, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).

> [!NOTE]
> Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu Tiekimo grandinės valdymo sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą. Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tik siųstų naujinimus į Tiekimo grandinės valdymą. Šiuo atveju „Field Service“ negaus Tiekimo grandinės valdymo atsargų lygio naujinimų. Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su Tiekimo grandinės valdymu](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su pardavimo užsakymais, susietais su Tiekimo grandinės valdymo projektu](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Objektas **Išorinio produkto atsargos** naudojamas tik atliekant vidinį integravimą. Šis objektas gauna tiekimo grandinės valdymo integravimo atsargų lygio reikšmes, kurios vėliau transformuojamos į atsargų žurnalus neautomatiniu būdu, o vėliau keičia atsargų produktus sandėlyje.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="data-integration"></a>Duomenų integravimas
Norėdami, kad projektas veiktų, turite užtikrinti, kad būtų atnaujintas msdynce_externalproductinventories integravimo raktas.
1.  Eikite į **Duomenų integravimas > Ryšio rinkiniai**.
2.  Pasirinkite naudotą ryšio rinkinį.
3.  Skirtuke **Integravimo raktas** patikrinkite, ar šie raktai įtraukti į msdynce_externalproductinventories:
      - msdynce_productnumber (produkto numeris)
      - msdynce_warehouseid (sandėlio ID)
      
### <a name="data-integration-project"></a>Duomenų integravimo projektas
Galite taikyti filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik tam tikri produktai ir sandėliai siųstų atsargų lygio informaciją iš Tiekimo grandinės valdymo į „Field Service“.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Produktų atsargos (iš Tiekimo grandinės valdymo į „Field Service“): produktų atsargos

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
