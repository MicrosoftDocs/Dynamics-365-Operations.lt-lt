---
title: Tiekimo grandinės valdymo sandėlių sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ sandėlius sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 94fb6720152cbf6aec58d2b8d9d02fc5343c05e2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251183"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Tiekimo grandinės valdymo sandėlių sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ sandėlius sinchronizuojant su „Dynamics 365 Field Service“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdymo sandėlius su „Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“)

**Užduotis projekte Duomenų integravimas**
- Sandėlis

## <a name="entity-set"></a>Objektų rinkinys
| „Field Service“    | Tiekimo grandinės valdymas                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Sandėliai                             |

## <a name="entity-flow"></a>Objekto srautas
Sandėlius, kurie kuriami ir tvarkomi Tiekimo grandinės valdyme, galima sinchronizuoti su „Field Service“ per „Common Data Service“ (CDS) duomenų integravimo projektą. Pageidaujamus sandėlius, kurie sinchronizuojami su „Field Service“, galima valdyti projekte naudojant išplėstinę užklausą ir filtravimą. Sandėliai, kurie sinchronizuojami iš Tiekimo grandinės valdymo, sukuriami „Field Service“, kurios lauke **Tvarkomas išoriškai** nustatoma **Taip**, o įrašas skirtas tik skaityti.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Reikalinga papildoma funkcija iš „Field Service“ CRM sprendimo, kad būtų palaikomas „Field Service ir „Finance and Operations“ integravimas. Sprendimo laukas **Tvarkomas išoriškai** įtrauktas į objektą **Sandėlis (msdyn_warehouses)**. Šis laukas padeda nustatyti, ar sandėlis tvarkomas iš Tiekimo grandinės valdymo, ar jis yra tik „Field Service“. Šio lauko parametrai apima toliau nurodytas parinktis.
- **Taip** – sandėlis paimtas iš Tiekimo grandinės valdymo ir jo nebus galima redaguoti sprendime „Sales“.
- **Ne** – sandėlis buvo įvestas tiesiogiai „Field Service“ ir tvarkomas čia.

Laukas **Tvarkomas išoriškai** padeda kontroliuoti atsargų lygių sinchronizavimą, koregavimą, perkėlimą ir naudojimą darbo užsakymuose. Tik sandėlius, kurių parinktis **Tvarkomas išoriškai** nustatyta į **Taip**, galima naudoti norint tiesiogiai sinchronizuoti su tuo pačiu sandėliu kitoje sistemoje. 

> [!NOTE]
> Galima sukurti keletą „Field Service“ sandėlių (pagal parinktį **Tvarkomas išoriškai = Ne**), o tada juos susieti su vienu „Finance and Operations“ sandėliu, naudojančiu išplėstinės užklausos ir filtravimo funkcionalumą. Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir tiesiog siųstų naujinimus į „Finance and Operations“. Šiuo atveju „Field Service“ negaus „Finance and Operations“ atsargų lygio naujinimų. Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ projektu susietais pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka
### <a name="data-integration-project"></a>Duomenų integravimo projektas
Prieš sinchronizuojant sandėlius būtina atnaujinti projekto išplėstinę užklausą ir filtravimą, įtraukiant tik tuos sandėlius, kuriuos norima perkelti iš Tiekimo grandinės valdymo į „Field Service“. Atkreipkite dėmesį, kad jums reikės „Field Service“ sandėlio, kurį būtų galima taikyti darbo užsakymams, koregavimui ir perkėlimui.  

Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_warehouses**.
1. Pasirinkite Duomenų integravimas.
2. Pasirinkite skirtuką **Ryšio rinkinys**.
3. Pasirinkite ryšio rinkinį, naudojamą darbo užsakymui sinchronizuoti.
4. Pasirinkite skirtuką **Integravimo raktas**.
5. Raskite msdyn_warehouses ir patikrinkite, ar pridėtas raktas **msdyn_name (pavadinimas)**. Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Sandėliai (iš Tiekimo grandinės valdymo į „Field Service“): sandėliai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/Warehouse1.png)](./media/Warehouse1.png)
