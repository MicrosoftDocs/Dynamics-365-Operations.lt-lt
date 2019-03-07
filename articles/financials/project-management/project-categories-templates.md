---
title: „Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Microsoft Dynamics 365 for Project Service Automation“.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "347841"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projekto išlaidų kategorijas su „Microsoft Dynamics 365 for Project Service Automation“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>„Project Service Automation“ ir „Finance and Operations“ duomenų srautas

Naudojantis „Project Service Automation“ ir „Finance and Operations“ integravimo sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie projekto išlaidų operacijos kategorijas srautas iš „Finance and Operations“ ir „Project Service Automation“.

Jei projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“, integravimo srautas pirmiausia yra iš „Finance and Operations“ į „Project Service Automation“. Tada projekto išlaidų kategorijų integravimo ID atnaujinami atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

Jei projekto išlaidų kategorijos tvarkomos naudojantis „Project Service Automation“, integravimo srautas pirmiausia yra iš „Project Service Automation“ į „Finance and Operations“. Prieš atliekant sinchronizavimą iš „Project Service Automation“, projekto kategorijos jau turi būti sukonfigūruotos naudojantis „Finance and Operations“. Po to sinchronizuokite iš „Finance and Operations“ į „Project Service Automation“, o po to vėl iš „Project Service Automation“ į „Finance and Operations“. Tokiu būdu padedate užtikrinti, kad kategorijos yra susietos ir nesukurta dublikatų.

> [!NOTE]
> Paprastai projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“. Tačiau, jei išlaidų kategorijos nebus tvarkomos naudojantis „Finance and Operations“ arba jos jau buvo sukurtos „Project Service Automation“, pirma turite jas sinchronizuoti, naudodami projekto išlaidų kategorijos (iš PSA į „Fin and Ops“) šabloną. Tada sinchronizuokite naudodami projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA) šabloną. Tada turėtumėte dar kartą atlikti „Project Service Automation“ sinchronizavimą su „Finance and Operations“.
>
> Jei pirmiausia sinchronizuojate iš „Project Service Automation“, prieš atlikdami sinchronizavimą turite įvykdyti tokius „Finance and Operations“ reikalavimus:
>
> - Turi būti bendro naudojimo kategorija, kuri sutampa su projekto kategorija, nustatyta „Project Service Automation“, be to, ji turi būti įgalinta ir **Projektui** ir **Išlaidoms**.
> - Kiekvienam „Finance and Operations“ juridiniam subjektui, kuris turi būti integruotas, turi būti tokios projekto kategorijos:
>
>     - **Projektas/kategorija** yra. 
>     - **Naudoti tvarkant išlaidas** įgalintas.
>     - **Aktyvus žurnale** įgalintas.
>     - Nustatyta **Operacijos tipas** **Išlaidos**

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>„Finance and Operations“ projekto išlaidų kategorijų sinchronizavimas su „Project Service Automation“

### <a name="template-and-task"></a>Šablonai ir užduotys

Norėdami atidaryti šabloną, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Finance and Operations“ projekto išlaidų kategorijas su „Project Service Automation“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš „Fin and Ops“ į PSA)
- **Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su PSA

### <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”            | „Project Service Automation“ |
|-----------------------------------|----------------------------|
| Kategorijų integravimo objektas | Operacijų kategorijos     |

### <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos.

### <a name="power-query"></a>„Power Query“

Sinchronizuojant su „Project Service Automation“, jei norima nustatyti operacijos kategorijos atsiskaitymo tipą, būtina naudoti „Microsoft Power Query for Excel“. Projekto išlaidų operacijos kategorijų (iš „Fin and Ops“ į PSA) šablone pateikiamas numatytasis stulpelis ir susiejimas. Norint sukurti savo šabloną į „Power Query“ būtina įtraukti sąlyginį stulpelį. Atlikite šiuos veiksmus.

1. Spustelėkite rodyklę, kad atidarytumėte projekto išlaidų kategorijų užduoties susiejimą projekto išlaidų kategorijų (iš „Fin and Ops“ į PSA) šablone.
2. Spustelėkite nuorodą **Išplėstinė užklausa ir Filtravimas**, kad atidarytumėte „Power Query“.
2. Paspauskite **Įtraukti sąlyginį stulpelį**.
3. Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**.
4. Įveskite šią sąlygą: jei reikšmė **CATEGORYID nėra lygi neapibrėžtai reikšmei, tada 19235001, kitais atvejais reikšmė neapibrėžta**.
5. Stulpelyje spustelėkite **Gerai**.
6. Įsitikinkite, kad šis stulpelis susietas susiejimo puslapyje.

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.

[![Šablono susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ projekto išlaidų kategorijų sinchronizavimas su „Finance and Operations“

### <a name="template-and-task"></a>Šablonai ir užduotys

Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant „Finance and Operations“ projekto išlaidų kategorijas su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** projekto išlaidų kategorijos (iš PSA į „Fin and Ops“)
- **Projekto užduoties pavadinimas:** kategorijų sinchronizavimas su „Fin Ops“

### <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | „Finance and Operations”            |
|----------------------------|-----------------------------------|
| Operacijų kategorijos     | Kategorijų integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos tvarkomos naudojantis „Finance and Operations“ ir yra sinchronizuojamos su „Project Service Automation“ kaip operacijos kategorijos. Vėl sinchronizuojant su „Finance and Operations“ atnaujinama „Finance and Operations“ projekto kategorijos „Project Service Automation“ integravimo ID reikšmė.

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas.

> [!NOTE]
> Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
