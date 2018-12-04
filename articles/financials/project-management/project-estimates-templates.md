---
title: "Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Tiesioginis „Project Service Automation“ apytikslių projekto reikšmių sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant apytiksles „Microsoft Dynamics 365 for Project Service Automation“ projekto grafiko ir projekto išlaidų reikšmes su „Microsoft Dynamics 365 for Finance and Operations“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, apytikslės grafiko reikšmės, apytikslės išlaidų reikšmės ir funkcijų užrakinimas pasiekiamas naudojantis „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0.
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie apytiksles projekto grafiko ir projekto išlaidų reikšmes srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Apytikslės projekto grafiko reikšmės

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant apytiksles „Project Service Automation“ projekto grafiko reikšmes su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto grafiko reikšmės (iš PSA į „Fin and Ops“)
- **Užduočių pavadinimas projekte**

    - Operacijų ryšiai
    - Numatomos išlaidos

### <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | „Finance and Operations”                        |
|----------------------------|-----------------------------------------------|
| Projekto užduotys              | Projekto valandų įvertinimo duomenų integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Apytikslės projekto grafiko reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip grafikų prognozės.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš sinchronizavimą projekto valandų įvertinimo gali atsirasti, galite sinchronizuoti projektus, projekto užduotims ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto grafiko reikšmių šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.

- Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.
- Filtruoti visus užduotyje esančius konkretaus ištekliaus įrašus, dėl kurių galėtų nepavykti integravimas į grafikų prognozes.
- Filtruoti visas tuščias operacijos kategorijos eilutes. Nepavykus atlikti užduoties, gali būti pateikiamos klaidingos grafikų prognozės.

#### <a name="set-the-default-forecast-model-id"></a>Nustatyti numatytąjį prognozės modelio ID

Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, spustelėję rodyklę **Susieti** atidarykite susiejimą. Tada pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.

- Jei naudojate numatytąjį apytikslių „Microsoft Project“ grafiko reikšmių (iš PSA į „Fin and Ops“) šabloną, sąraše **Pritaikyti veiksmai** paspauskite **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**. Įveskite stulpelio sąlygą: jei projekto užduotis apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.

#### <a name="filter-out-resource-specific-records"></a>Filtruoti tam tikro ištekliaus įrašus

Apytikslių projekto grafiko reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo naudojantis pašalinami visi konkretaus ištekliaus įrašai. Norint sukurti savo šabloną būtina įtraukti šį filtrą. Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad filtruotumėte stulpelį **msdyn\_islinetask**, kad būtų įtraukiami tik užrašu **Klaidinga** pažymėti įrašai.

#### <a name="filter-out-empty-transaction-category-rows"></a>Tuščių operacijos kategorijos eilučių filtravimas

Norėdami pašalinti visas eilutes, kurių operacijos kategorijos yra tuščios, turite įtraukti filtrą. Šią užduotį atlikti būtina, nepriklausomai nuo to, ar naudojate numatytąjį šabloną, ar sukuriate savo šabloną. Naudojantis šiuo filtru pašalinamos visos iš „Project Service Automation“ gautos eilutės, dėl kurių galėtų būti pateikiamos klaidingos „Finance and Operations“ grafikų prognozės. Pasirinkite nuorodą **Išplėstinė užklausa ir filtravimas**, kad būtų filtruojami neapibrėžti stulpelio **msdyn\_transactioncategory\_value** įrašai.

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Apytikslės projekto išlaidų reikšmės

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateiktas šablonas ir pagrindinės užduotys naudojami sinchronizuojant apytiksles „Project Service Automation“ projekto išlaidų reikšmes su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** apytikslės projekto išlaidų reikšmės (iš PSA į „Fin and Ops“)
- **Užduočių pavadinimas projekte**

    - Operacijų ryšiai 
    - Numatomos išlaidos

### <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | „Finance and Operations”                                   |
|----------------------------|----------------------------------------------------------|
| Operacijų ryšiai    | Projekto operacijų ryšių integravimo objektas |
| Įvertinimo eilutės             | Projekto išlaidų įvertinimo duomenų integravimo objektas         |

### <a name="entity-flow"></a>Objekto srautas

Apytikslės projekto išlaidų reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ kaip projekto išlaidų prognozės.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atliekant apytikslių projekto išlaidų reikšmių sinchronizavimą būtina sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, apytikslių projekto išlaidų reikšmių šablone turite naudoti „Power Query“.

- Filtruokite taip, kad būtų įtraukti tik apytikslių išlaidų reikšmių eilučių įrašai.
- Nustatyti numatytojo prognozės modelio ID, kuris bus naudojamas integracijai kuriant naujas grafikų prognozes.
- Pakeiskite atsiskaitymo tipus.
- Pakeiskite operacijų tipus.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtruokite taip, kad būtų įtrauktos tik apytikslių išlaidų reikšmių eilutės

Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuris atliekant integravimą apima tik išlaidų eilutes. Norint sukurti savo šabloną būtina įtraukti šį filtrą. Pasirinkite užduotį **Operacijos ryšiai**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**. Filtruokite taip, kad stulpelyje **msdyn\_transactiontype1** būtų nurodyta tik **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Nustatyti numatytąjį prognozės modelio ID

Norėdami atnaujinti numatytąją šablono prognozės modelio ID vertę, pasirinkite užduotį **Apytikslės išlaidų reikšmės**, tada spustelėję rodyklę **Susieti** atidarykite susiejimą. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**.

- Jei naudojate numatytąjį apytikslių „Microsoft Project“ išlaidų reikšmių (iš PSA į „Fin and Ops“) šabloną, naudodami „Power Query“, skyriuje **Pritaikyti veiksmai** paspauskite pirmą parinktį **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **O\_forecast** pakeiskite prognozės modelio ID pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Numatytajame šablone nurodytas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. Naudodami „Power Query“, pasirinkite **Įtraukti sąlyginį stulpelį** ir įveskite naujo stulpelio pavadinimą, pavyzdžiui, **ModelID**. Įveskite stulpelio sąlygą: jei apytikslės reikšmės eilutės ID reikšmė apibrėžta, tada \<įveskite prognozės modelio ID\>; kitais atvejais reikšmė neapibrėžta.

#### <a name="transform-the-billing-types"></a>Atsiskaitymo tipų keitimas

Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems atsiskaitymo tipams keisti. Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**. Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **BillingType**. Tada įveskite toliau nurodytą sąlygą.

Jei **msdyn\_billingtype** = 192350000, tada **NonChargeable**,  
o jei **msdyn\_billingtype** = 192350001, tada **Chargeable**,  
o jei **msdyn\_billingtype** = 192350002, tada **Complimentary**,  
kitais atvejais **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Operacijų tipų pakeitimas

Apytikslių projekto išlaidų reikšmių (iš PSA į „Fin and Ops“) šablone įtrauktas sąlyginis stulpelis, naudojamas atliekant integravimą iš „Project Service Automation“ gautiems operacijų tipams keisti. Norint sukurti savo šabloną būtina įtraukti šį sąlyginį stulpelį. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, tada pasirinkite **Įtraukti sąlyginį stulpelį**. Įveskite naujo stulpelio pavadinimą, pavyzdžiui, **TransactionType**. Tada įveskite toliau nurodytą sąlygą.

Jei **msdyn\_transactiontypecode** = 192350000, tada **Cost**,  
o jei **msdyn\_transactiontypecode** = 192350005, tada **Sales**,  
kitu atveju **null**

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Šablono susiejimas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)

