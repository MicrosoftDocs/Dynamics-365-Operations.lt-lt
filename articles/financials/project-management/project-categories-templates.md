---
title: "„Project Service Automation“ projekto išlaidų kategorijų sinchronizavimas"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Dynamics 365 for Project Service Automation“."
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Dynamics 365 for Project Service Automation“.

> [!NOTE]
> Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>„Project Service Automation“ ir „Finance and Operations“ duomenų srautas

Naudojantis „Project Service Automation“ ir „Finance and Operations“ integravimo sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto išlaidų operacijos kategorijas srautas iš „Finance and Operations“ ir „Project Service Automation“.

Jei projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“, integravimo srautas pirmiausia yra iš „Finance and Operations“ į „Project Service Automation“, o po to, sinchronizuojant iš „Project Service Automation“ į „Finance and Operations“, atnaujinamos projekto išlaidų kategorijų integravimo ID reikšmės.

Jei projekto išlaidų kategorijos tvarkomos naudojantis „Project Service Automation“, integravimo srautas pirmiausia yra iš „Project Service Automation“ į „Finance and Operations“. Prieš atliekant sinchronizavimą iš „Project Service Automation“, projekto kategorijos jau turi būti sukonfigūruotos naudojantis „Finance and Operations“. Po to sinchronizuokite iš „Finance and Operations“ į „Project Service Automation“, o po to vėl iš „Project Service Automation“ į „Finance and Operations“. Taip užtikrinama, kad tikrai susiejamos kategorijos ir nesukuriamos pasikartojančios kategorijos.

> [!NOTE]
> Paprastai projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“. Jei jūsų atveju taip nėra arba jau turite sukūrę „Project Service Automation“ išlaidų kategorijas, pirmiausia turite sinchronizuoti naudodami projekto išlaidų operacijos kategorijas (iš PSA į „Fin and Ops“), o po to – naudodami projekto išlaidų operacijos kategorijas (iš „Fin and Ops“ į PSA). Tada turėtumėte dar kartą paleisti sinchronizavimą iš PSA į „Fin and Ops“.

> Jei pirmiausia sinchronizuojama iš „Project Service Automation“, jau turi būti nustatytos „Finance and Operations“ projekto kategorijos, taip pat turi būti nustatyta visų kitų projekto kategorijų, kurias reikia sinchronizuoti su „Project Service Automation“ operacijos kategorijomis, reikšmė **Aktyvios žurnaluose**.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Project Service Automation“ projekto išlaidų kategorijas su „Project Service Automation“.

-  **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA)
-  **Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su PSA

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”               | „Project Service Automation“    |
|--------------------------------------|-------------------------------|
| Kategorijų integravimo objektas    | Operacijų kategorijos        |

## <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.

## <a name="power-query"></a>„Power Query“

Sinchronizuojant su „Project Service Automation“, jei norima nustatyti operacijos kategorijos atsiskaitymo tipą, būtina naudoti „Microsoft Power Query“. Projekto išlaidų operacijos kategorijų (iš „Fin and Ops“ į PSA) šablone jau pateikiamas numatytasis stulpelis ir susiejimas. Norint sukurti savo šabloną į „Power Query“ būtina įtraukti sąlyginį stulpelį.
- Atlikdami projekto išlaidų kategorijų susiejimo užduotį atidarykite formą Išplėstinė užklausa ir filtravimas.
- Paspauskite **Įtraukti sąlyginį stulpelį**.
- Nurodykite naujo stulpelio pavadinimą, pvz., „BillingType“.
- Įveskite šią sąlygą: jei reikšmė **CATEGORYID nėra lygi neapibrėžtai reikšmei, tada 19235001, kitais atvejais reikšmė neapibrėžta**.
- Stulpelyje spustelėkite **Gerai**.
- Įsitikinkite, kad šis stulpelis susietas susiejimo puslapyje.

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.

[![Šablono susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Project Service Automation“ projekto išlaidų kategorijas su „Finance and Operations“.

-**Duomenų integravimo šablono pavadinimas:** Projekto išlaidų operacijos kategorijos (iš PSA į „Fin and Ops“) -**Projekto užduoties pavadinimas:** Kategorijų sinchronizavimas su „Fin Ops“

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“      | „Finance and Operations”             |
|---------------------------------|------------------------------------|
| Operacijų kategorijos          | Kategorijų integravimo objektas  | 

## <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos. Vėl sinchronizuojant su „Finance and Operations“ atnaujinama „Finance and Operations“ projekto kategorijos „Project Service Automation“ integravimo ID reikšmė.

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.

> [!NOTE]
> Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

