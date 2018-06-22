---
title: "Tiesioginis „Project Service Automation“ projekto vertinimų sinchronizavimas su „Finance and Operations“ projekto prognozėmis"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“."
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
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Tiesioginis „Project Service Automation“ projekto vertinimų sinchronizavimas su „Finance and Operations“ projekto prognozėmis

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“.

> [!NOTE]
> Projekto užduočių integravimas, išlaidų operacijos kategorijos, apytikslės grafiko reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Dynamics 365 for Finance and Operations“ versija 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie apytiksles projekto grafiko ir projekto išlaidų reikšmes srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant apytiksles „Project Service Automation“ projekto grafiko reikšmes su „Finance and Operations“.

-  **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto grafiko reikšmės (iš PSA į „Fin and Ops“)

-  **Užduočių pavadinimas projekte** 
    - Operacijų ryšiai 
    - Numatomos išlaidos

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“      | „Finance and Operations”                          |
|---------------------------------|-------------------------------------------------|
| Projekto užduotys                   | Projekto valandų įvertinimo duomenų integravimo objektas   |

## <a name="entity-flow"></a>Objekto srautas

Apytikslės projekto grafiko reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip grafikų prognozės.

## <a name="preconditions"></a>Išankstinės sąlygos

Prieš sinchronizavimą projekto valandų įvertinimo gali atsirasti, galite sinchronizuoti projektus, projekto užduotims ir projekto išlaidų operacijų kategorijas.

## <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytus veiksmus, apytikslių projekto grafiko reikšmių šablone turite naudoti „Microsoft Power Query“.
- Nustatyti, **Prognozės modelio ID**, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.
- Filtruoti visus užduotyje esančius konkretaus išteklio įrašus, dėl kurių galėtų nepavykti integravimas į grafikų prognozes
- Filtruoti visas tuščias operacijos kategorijos eilutes. To nepadarius gali būti pateikiamos klaidingos grafikų prognozės.

### <a name="forecast-model-id"></a>Prognozės modelio ID
Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, spustelėję rodyklę **Susieti** atidarykite susiejimą. Paspauskite norėdami atidaryti funkcijų Išplėstinė užklausa ir Filtravimas langus.
- Jei naudojate numatytąjį apytikslių „Microsoft Project“ grafiko reikšmių (iš PSA į „Fin and Ops“) šabloną, skyriuje **Pritaikyti veiksmai** paspauskite **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **O_forecast** pakeiskite reikšmės **Prognozavimo modelio ID** pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. Paspauskite **Įtraukti sąlyginį stulpelį** ir nurodykite stulpelio pavadinimą, pvz., ModelID. Įveskite stulpelio sąlygą: jei projekto užduotis apibrėžta, tada<enter the forecast model ID>; kitu atveju reikšmė neapibrėžta.

### <a name="filter-out-resource-specific-records"></a>Filtruoti tam tikro išteklio įrašus
Apytikslių projekto grafiko reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo naudojantis pašalinami visi konkretaus išteklio įrašai. Norint sukurti savo šabloną būtina įtraukti šį filtrą. Formoje Išplėstinė užklausa ir filtravimas pasirinkite filtruoti stulpelį **msdyn_islinetask**, kad būtų įtraukiami tik užrašu **Klaidinga** pažymėti įrašai.

### <a name="filter-out-empty-transaction-category-rows"></a>Tuščių operacijos kategorijos eilučių filtravimas
Norėdami pašalinti visas eilutes su tuščiomis operacijos kategorijomis, turite įtraukti filtrą. Tai yra būtina, nepriklausomai nuo to, ar naudojate numatytąjį šabloną, ar sukuriate savo šabloną. Naudojantis šiuo filtru pašalinamos visos iš „Project Service Automation“ gautos eilutės, dėl kurių galėtų būti pateikiamos klaidingos „Finance and Operations“ grafikų prognozės. Formoje Išplėstinė užklausa ir filtravimas pasirinkite, kad būtų filtruojami neapibrėžti stulpelio **msdyn_transactioncategory_value** įrašai.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Toliau pateiktas šablonas ir pagrindinė užduotis naudojama sinchronizuojant apytiksles „Project Service Automation“ projekto išlaidų reikšmes su „Finance and Operations“.

-  **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto išlaidų reikšmės (iš PSA į „Fin and Ops“)
-  **Užduočių pavadinimas projekte** 
     - Operacijų ryšiai 
     - Numatomos išlaidos

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“      | „Finance and Operations”                                     |
|---------------------------------|------------------------------------------------------------|
| Operacijų ryšiai         | Projekto operacijų ryšių integravimo objektas.   |
| Įvertinimo eilutės                  | Projekto išlaidų įvertinimo duomenų integravimo objektas.           |

## <a name="entity-flow"></a>Objekto srautas

Apytikslės projekto išlaidų reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto išlaidų prognozės.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš atliekant apytikslių projekto išlaidų reikšmių sinchronizavimą būtina sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.

## <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytus veiksmus, apytikslių projekto išlaidų reikšmių šablone turite naudoti „Microsoft Power Query“.
- Filtruokite taip, kad būtų įtraukti tik apytikslių išlaidų reikšmių eilučių įrašai
- Nustatyti, **Prognozės modelio ID**, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.
- Pakeiskite atsiskaitymo tipus.
- Pakeiskite operacijų tipus.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtruokite taip, kad būtų įtrauktos tik apytikslių išlaidų reikšmių eilutės
Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kad išlaidų eilutės būtų įtraukiamos tik atliekant integravimą. Norint sukurti savo šabloną būtina įtraukti šį filtrą. Pasirinkite operacijos ryšių užduotį ir spustelėkite rodyklę **Susieti**. Paspauskite **Išplėstinė užklausa ir filtravimas**. Filtruokite taip, kad stulpelyje **msdyn_transactiontype1** būtų nurodyta tik **msdyn_estimateline**.

### <a name="forecast-model-id"></a>Prognozės modelio ID
Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, atlikdami apytikslės išlaidų reikšmės užduotį spustelėję rodyklę **Susieti** atidarykite susiejimą. Paspauskite norėdami atidaryti funkcijų Išplėstinė užklausa ir Filtravimas langus.
- Jei naudojate numatytąjį apytikslių „Microsoft Project“ išlaidų reikšmių (iš PSA į „Fin and Ops“) šabloną, skyriuje **Pritaikyti veiksmai** paspauskite pirmą **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **O_forecast** pakeiskite reikšmės **Prognozavimo modelio ID** pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. Paspauskite **Įtraukti sąlyginį stulpelį** ir nurodykite stulpelio pavadinimą, pvz., ModelID. Įveskite stulpelio sąlygą: jei apytikslės reikšmės eilutės ID reikšmė nėra neapibrėžta, tada < įveskite prognozės modelio ID >; kitais atvejais reikšmė neapibrėžta.

### <a name="transform-the-billing-types"></a>Atsiskaitymo tipų keitimas
Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, skirtas atliekant integravimą iš „Project Service Automation“ gautiems atsiskaitymo tipams keisti.
- Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį. Formoje Išplėstinė užklausa ir Filtravimas paspauskite **Įtraukti sąlyginį stulpelį**. Nurodykite stulpelio pavadinimą, pvz., „BillingType“. Įvedama toliau nurodyta sąlyga.

    Jei **msdyn_billingtype** = 192350000, tada **NonChargeable**, o jei **msdyn_billingtype** = 192350001, tada **Chargeable** o jei **msdyn_billingtype** = 192350002, tada **Complimentary**, kitais atvejais **NotAvailable**

### <a name="transform-the-transaction-types"></a>Operacijų tipų pakeitimas
Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, skirtas atliekant integravimą iš „Project Service Automation“ gautiems operacijų tipams keisti.
- Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį. Formoje Išplėstinė užklausa ir Filtravimas paspauskite **Įtraukti sąlyginį stulpelį**. Nurodykite stulpelio pavadinimą, pvz., „TransactionType“. Įvedama tokia sąlyga: jei **msdyn_transactiontypecode** = 192350000, tada **Cost**, o jei **msdyn_transactiontypecode** = 192350005, tada **Sales**, kitais atvejais **null**

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Šablono susiejimas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




