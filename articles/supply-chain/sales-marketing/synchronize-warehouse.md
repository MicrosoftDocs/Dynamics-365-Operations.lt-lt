---
title: „Supply Chain Management” sandėlių sinchronizavimas su „Field Service“
description: Šiame straipsnyje aptariamos šablonus ir su juos susijusias užduotis, kurios naudojamos sandėliams sinchronizuoti Dynamics 365 Supply Chain Management iš į Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
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
ms.openlocfilehash: 8b86b6a59344299a7a2d277543c3186ed2b8cee4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103240"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>„Supply Chain Management” sandėlių sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]



Šiame straipsnyje aptariamos šablonus ir su juos susijusias užduotis, kurios naudojamos sandėliams sinchronizuoti Dynamics 365 Supply Chain Management iš į Dynamics 365 Field Service.

[![„Supply Chain Management“ ir „Field Service“ verslo procesų sinchronizavimas.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Supply Chain Management” sandėlius su „Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Sandėliai (iš „Supply Chain Management” į „Field Service“)

**Užduotis projekte Duomenų integravimas**
- Sandėlis

## <a name="table-set"></a>Lentelės rinkinys
| „Field service“    | „Supply Chain Management”                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Sandėliai                             |

## <a name="table-flow"></a>Lentelių srautas
Sandėlius, kuriamus ir tvarkomus „Supply Chain Management”, galima sinchronizuoti su „Field Service“ per „Microsoft Dataverse“ „Data integration” projektą. Pageidaujamus sandėlius, kurie sinchronizuojami su „Field Service“, galima valdyti projekte naudojant išplėstinę užklausą ir filtravimą. Sandėliai, kurie sinchronizuojami iš „Supply Chain Management”, sukuriami „Field Service“, kurio stulpelis **Tvarkomas išoriškai** nustatomas **Taip**, o įrašas skirtas tik skaityti.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Reikalinga papildoma „Field Service“ CRM sprendimo funkcija, kad būtų palaikomas „Field Service“ ir „Supply Chain Management“ integravimas. Sprendimo laukas **Tvarkomas išoriškai** įtrauktas į objektą **Sandėlis (msdyn_warehouses)**. Šis stulpelis padeda nustatyti, ar sandėlis tvarkomas iš „Supply Chain Management”, ar jis yra tik „Field Service“. Į šio stulpelio nustatymus įeina:
- **Taip** – sandėlis paimtas iš „Supply Chain Management” ir jo nebus galima redaguoti sprendime „Sales“.
- **Ne** – sandėlis buvo įvestas tiesiogiai „Field Service“ ir tvarkomas čia.

Stulpelis **Tvarkomas išoriškai** padeda kontroliuoti atsargų lygių sinchronizavimą, koregavimą, perkėlimą ir naudojimą darbo užsakymuose. Tik sandėlius, kurių parinktis **Tvarkomas išoriškai** nustatyta į **Taip**, galima naudoti norint tiesiogiai sinchronizuoti su tuo pačiu sandėliu kitoje sistemoje. 

> [!NOTE]
> Galima sukurti keletą „Field Service“ sandėlių (esant **Tvarkomas išoriškai** = Ne), o tada juos susieti su vienu sandėliu, naudojant išplėstinės užklausos ir filtravimo funkcionalumą. Tai naudojama tais atvejais, kai norite, kad „Field Service“ tvarkytų išsamų atsargų lygį ir į „Supply Chain Management“ siųstų tik naujinimus. Šiuo atveju „Field Service“ negaus „Supply Chain Management” atsargų lygio naujinimų. Papildomos informacijos žr. [„Field Service“ atsargų koregavimo sinchronizavimas su Tiekimo grandinės valdymu](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ir [„Field Service“ darbo užsakymų sinchronizavimas su pardavimo užsakymais, susietais su „Supply Chain Management” projektu](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka
### <a name="data-integration-project"></a>Duomenų integravimo projektas
Prieš sinchronizuojant sandėlius būtina atnaujinti projekto išplėstinę užklausą ir filtravimą, įtraukiant tik tuos sandėlius, kuriuos norima perkelti iš „Supply Chain Management” į „Field Service“. Atkreipkite dėmesį, kad jums reikės „Field Service“ sandėlio, kurį būtų galima taikyti darbo užsakymams, koregavimui ir perkėlimui.  

Įsitikinkite, kad yra **Integravimo kodas**, skirtas **msdyn_warehouses**.
1. Pasirinkite Duomenų integravimas.
2. Pasirinkite skirtuką **Ryšio rinkinys**.
3. Pasirinkite ryšio rinkinį, naudojamą darbo užsakymui sinchronizuoti.
4. Pasirinkite skirtuką **Integravimo raktas**.
5. Raskite msdyn_warehouses ir patikrinkite, ar pridėtas raktas **msdyn_name (pavadinimas)**. Jei jis nerodomas, pridėkite jį puslapio viršuje spustelėję **Pridėti raktą** ir spustelėję **Įrašyti**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Sandėliai (iš „Supply Chain Management” į „Field Service“): sandėliai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
