---
title: „Supply Chain Management” atsargų lygio informacijos sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.
author: Henrikan
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 31674b2be3deb52277cbf79e1e076da13bf94404
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566364"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>„Supply Chain Management” atsargų lygio informacijos sinchronizavimas su „Field Service“ 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų lygio informaciją su „Dynamics 365 Field Service“.

[![„Supply Chain Management“ ir „Field Service“ verslo procesų sinchronizavimas.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Supply Chain Management” turimų atsargų lygius su „Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Produktų atsargos (iš „Supply Chain Management” į „Field Service“)
  
**Užduotis projekte Duomenų integravimas**
- Produktų atsargos

Prieš sinchronizuojant atsargų lygius būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sandėliai (iš „Supply Chain Management” į „Field Service“) 
- „Field Service“ produktai su atsargų vienetu (iš „Supply Chain Management” į „Sales“) 

## <a name="entity-set"></a>Objektų rinkinys

| „Field Service“                      | „Supply Chain Management”                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Turimos „Dataverse” atsargos sandėlyje     |

## <a name="entity-flow"></a>Objekto srautas
Atsargų lygio informacija iš „Finance and Operations“ siunčiama į pasirinktų produktų „Field Service“. Atsargų lygio informacija apima 
- Turimas kiekis (dabartinis faktiškai užregistruotas sandėlyje esantis kiekis)
- Kiekis užsakyme (bendras užsakyme užregistruotas kiekis, pvz., pardavimo užsakymų kiekis)
- Užsakytas kiekis (bendras užregistruotas užsakytas kiekis, pvz., pirkimo užsakymų kiekis)

Ši informacija fiksuojama visiems kiekvieno sandėlio išleistiems produktams ir sinchronizuojama remiantis keitimų sekimu, kai pasikeičia atsargų lygis.

„Field Service“ integravimo sprendimas sukuria pokyčiui skirtus atsargų žurnalus „Field Service“ lygiams, atitinkantiems „Supply Chain Management” lygius, gauti.

„Supply Chain Management” veiks kaip atsargų lygių ruošinys. Todėl svarbu nustatyti darbo užsakymų, perkėlimo ir koregavimo integravimą iš „Field Service“ į „Supply Chain Management”, jei šis funkcionalumas naudojamas „Field Service“ kartu su „Supply Chain Management” atsargų lygių sinchronizavimu.

Produktus ir sandėlius, kuriuose atsargų lygiai tvarkomi pagal „Supply Chain Management”, galima valdyti naudojant išplėstinę užklausą ir filtravimą („Power Query“).

> [!NOTE]
> Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu „Supply Chain Management” sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą. Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tik siųstų naujinimus į „Supply Chain Management”. Šiuo atveju „Field Service“ negaus „Supply Chain Management” atsargų lygio naujinimų. Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su Tiekimo grandinės valdymu](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su pardavimo užsakymais, susietais su „Supply Chain Management” projektu](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Objektas **Išorinio produkto atsargos** naudojamas tik atliekant vidinį integravimą. Šis objektas gauna „Supply Chain Management” integravimo atsargų lygio reikšmes, kurios vėliau transformuojamos į atsargų žurnalus neautomatiniu būdu, o vėliau keičia atsargų produktus sandėlyje.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="data-integration"></a>Duomenų integravimas
Norėdami, kad projektas veiktų, turite užtikrinti, kad būtų atnaujintas msdynce_externalproductinventories integravimo raktas.
1.  Eikite į **Duomenų integravimas > Ryšio rinkiniai**.
2.  Pasirinkite naudotą ryšio rinkinį.
3.  Skirtuke **Integravimo raktas** patikrinkite, ar šie raktai įtraukti į msdynce_externalproductinventories:
      - msdynce_productnumber (produkto numeris)
      - msdynce_warehouseid (sandėlio ID)
      
### <a name="data-integration-project"></a>Duomenų integravimo projektas
Galite taikyti filtrus su išplėstine užklausa ir filtravimu, norėdami kontroliuoti, kad tik tam tikri produktai ir sandėliai siųstų atsargų lygio informaciją iš „Supply Chain Management” į „Field Service“.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Produktų atsargos (iš „Supply Chain Management” į „Field Service“): produktų atsargos

[![Šablono susiejimas naudojant funkcija Duomenų integravimas.](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]