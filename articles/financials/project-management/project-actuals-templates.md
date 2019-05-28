---
title: „Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ faktines projekto reikšmes su „Microsoft Dynamics 365 for Finance and Operations“.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571105"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>„Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ faktines projekto reikšmes su „Microsoft Dynamics 365 for Finance and Operations“.

Šablonas sinchronizuoja operacijas iš „Project Service Automation“ į „Finance and Operations“ išdėstymo lentelę. Atlikus sinchronizavimą **būtina** importuoti duomenis iš išdėstymo lentelės į integravimo žurnalą.

> [!NOTE]
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 ar naujasnę versiją.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.
> - Jei naudojate „Finance and Operations 7.3.0“ ir atliekate mokesčio operacijas naudodami „Project Service Automation“, turite įdiegti KB 4345320, kad šie mokesčiai būtų įtraukti į projekto SF.
> - Įvedant „Project Service Automation“ grafiko ir išlaidų operacijų PVM sumas būtina įdiegti „Project Service Automation“ 7 naujinimą. Kitu atveju faktinės mokesčių reikšmės nebus susietos su atitinkamomis faktinėmis grafiko ir išlaidų reikšmėmis ir nebus sinchronizuojamos su „Finance and Operations“. Jei reikia daugiau informacijos, kreipkitės į pagalbos tarnybą.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie faktines projekto reikšmes srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>„Project Service Automation“ projekto faktiniai duomenys

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant „Project Service Automation“ faktines projekto reikšmes su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinės projekto reikšmės (iš PSA į „Fin and Ops“)
- **Užduočių pavadinimas projekte**

    - Faktinės reikšmės
    - Operacijų ryšiai

### <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | „Finance and Operations”                                   |
|----------------------------|----------------------------------------------------------|
| Faktinės reikšmės                    | Projekto faktinių duomenų integravimo objektas                   |
| Operacijų ryšiai    | Projekto operacijų ryšių integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ projekto integravimo žurnalu. Apskaita taikoma pagal numatytąsias finansines dimensijas ir registravimo sąranką.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atliekant sinchronizavimą būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus ir sinchronizuoti projektus, projektų užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, projekto faktinių duomenų šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.

- Pakeiskite „Project Service Automation“ reikšmę operacijos tipas, nurodydami tinkamą „Finance and Operations“ reikšmę operacijos tipas. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Finance and Operations“ reikšmę atsiskaitymo tipas, nurodydami tinkamą „Project Service Automation“ reikšmę atsiskaitymo tipas. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas. Tada atsiskaitymo tipas susiejamas su reikšme **eilutės ypatybė** pagal „Project Service Automation“ integravimo parametrų puslapyje nurodytą konfigūraciją.
- Filtruoti konkrečias reikšmes Išteklių organizacijos vienetai, kurios turi būti sinchronizuojamos su šiuo šablonu.
- Jei faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės bus sinchronizuojamos su „Finance and Operations“, reikšmę sutarties organizacijos vienetas būtina pakeisti tinkama „Finance and Operations“ reikšme juridinis subjektas. Faktinių projekto reikšmių (iš PSA į „Fin and Ops“) šablone nurodytas demonstraciniais duomenimis grįstas sąlyginis stulpelis. Paskutinį įterptą sąlygos stulpelį būtina atnaujinti, nurodant tinkamus juridinius subjektus. To nepadarius gali būti rodoma integravimo klaida arba į „Finance and Operations“ gali būti importuotos netinkamos faktinės operacijos.
- Jei faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės nebus sinchronizuojamos su „Finance and operations“, iš šablono būtina panaikinti paskutinį įterptą sąlygos stulpelį. To nepadarius gali būti rodoma integravimo klaida arba į „Finance and Operations“ gali būti importuotos netinkamos faktinės operacijos.

#### <a name="contract-organizational-unit"></a>Sutarties organizacijos vienetas
Norėdami atnaujinti šablono stulpelyje įterptą sąlygą, spustelėję rodyklę **Susieti** atidarykite susiejimą. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, kad atidarytumėte „Power Query“.

- Jei naudojate numatytąjį faktinių „Project“ reikšmių (iš PSA į „Fin and Ops“) šabloną, „Power Query“ skyriuje **Pritaikyti veiksmai** paspauskite paskutinę **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **USSI** pakeiskite reikšmės Juridinis subjektas pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Prireikus į įrašą **Funkcija** įtraukite papildomų sąlygų ir atnaujinkite sąlygą **kita** iš **USMF** į tinkamą reikšmę Juridinis subjektas.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį, kad būtų palaikomas vidinis įmonės grafikas ir išlaidos. Paspauskite **Įtraukti sąlyginį stulpelį** ir įveskite stulpelio pavadinimą, pvz., **Juridinis subjektas**. Įveskite stulpelio sąlygą, kur, jei **msdyn\_contractorganizationalunitid.msdyn\_pavadinimas** yra \<organizacijos vienetas\>, tada \<įvesti juridinį subjektą\>;

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Integravus iš „Project Service Automation“, importuoti iš išdėstymo lentelės

Importavimas iš išdėstymo lentelės periodinio proceso turi būti paleidžiamas atlikus faktinių reikšmių sinchronizavimą iš „Project Service Automation“ į „Finance and Operations“. Vykdant šį procesą projekto operacijos importuojamos iš išdėstymo lentelės į „Project Service Automation“ integravimo žurnalą, kuriame taikoma apskaita ir galima užregistruoti importuotas operacijas. Rekomenduojame paleisti šį procesą paketo režimu, taip pat galima nustatyti, kad jis būtų vykdomas kaip pasikartojantis paketas.

## <a name="update-actuals-from-finance-and-operations"></a>„Finance and Operations“ faktinių reikšmių naujinimas

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojamos norint sinchronizuoti kvito numerį ir užregistruotų projekto operacijų PVM iš „Finance and Operations“ į „Project Service Automation“:

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinių projekto reikšmių naujinimas (iš „Fin Ops“ į PSA)
- **Užduočių pavadinimas projekte**

    - Faktinės reikšmės 
    - Operacijų ryšiai

### <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”                                   | „Project Service Automation“ |
|----------------------------------------------------------|----------------------------|
| Projekto faktinių duomenų integravimo objektas                   | Faktinės reikšmės                    |
| Projekto operacijų ryšių integravimo objektas | Operacijų ryšiai    |

### <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ projekto integravimo žurnalu. Užregistravus faktines reikšmes „Finance and Operations“ jos atnaujinamos „Project Service Automation“, naudojant kvito numerį iš „Finance and Operations“. Jei „Finance and Operations“ buvo įtraukti PVM mokesčiai, „Project Service Automation“ bus sukurtos naujos faktinės mokesčių reikšmės.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, projekto faktinių duomenų naujinimo šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.

- Pakeiskite „Finance and Operations“ reikšmę operacijos tipas, nurodydami tinkamą „Project Service Automation“ reikšmę operacijos tipas. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Project Service Automation“ reikšmę atsiskaitymo tipas, nurodydami tinkamą „Finance and Operations“ reikšmę atsiskaitymo tipas. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.

[![Šablono susiejimas](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
