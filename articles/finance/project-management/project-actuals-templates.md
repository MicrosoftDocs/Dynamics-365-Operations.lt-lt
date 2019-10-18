---
title: „Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos „Microsoft“ „Dynamics 365 Project Service Automation“ faktines projekto reikšmes tiesiogiai sinchronizuojant su „Finance and Operations“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0aeaa1ee4c35ca42a5382b3c7ff3519cba52996c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250535"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>„Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Dynamics 365 Project Service Automation“ faktines projekto reikšmes su „Dynamics 365 Finance“.

Šablonas sinchronizuoja operacijas iš „Project Service Automation“ į „Finance“ paruošimo lentelę. Atlikus sinchronizavimą **būtina** importuoti duomenis iš išdėstymo lentelės į integravimo žurnalą.

> [!NOTE]
> - Faktinių projekto reikšmių integravimą galima atlikti naudojant 8.0.1 ar naujesnę versiją.
> - Jei naudojate „Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.
> - Jei naudojate 7.3.0 versiją ir atliekate mokesčio operacijas naudodami „Project Service Automation“, turite įdiegti KB 4345320, kad šie mokesčiai būtų įtraukti į projekto SF.
> - Įvedant „Project Service Automation“ grafiko ir išlaidų operacijų PVM sumas būtina įdiegti „Project Service Automation“ 7 naujinimą. Kitu atveju faktinės mokesčių reikšmės nebus susietos su atitinkamomis faktinėmis grafiko arba išlaidų reikšmėmis ir nebus sinchronizuojamos su „Finance“. Jei reikia daugiau informacijos, kreipkitės į pagalbos tarnybą.

## <a name="data-flow-for-project-service-automation-to-finance"></a>„Project Service Automation“ duomenų srautas į „Finance“

Sprendime „Project Service Automation“ ir „Finance“ integravimas naudojama duomenų sinchronizavimo funkcija duomenims „Project Service Automation“ ir „Finance“ egzemplioriuose sinchronizuoti. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis duomenų integravimo funkcija, įgalinamas duomenų apie faktines projekto reikšmes srautas iš „Project Service Automation“ į „Finance“.

Toliau esančiame paveikslėlyje pavaizduotas duomenų sinchronizavimas tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>„Project Service Automation“ projekto faktiniai duomenys

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant „Project Service Automation“ faktines projekto reikšmes su „Finance“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinės projekto reikšmės (iš PSA į „Fin and Ops“)
- **Užduočių pavadinimas projekte**

    - Faktinės reikšmės
    - Operacijų ryšiai

### <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“ | Finansai                                   |
|----------------------------|----------------------------------------------------------|
| Faktiniai dydžiai                    | Projekto faktinių duomenų integravimo objektas                   |
| Operacijų ryšiai    | Projekto operacijų ryšių integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance“ projekto integravimo žurnalu. Apskaita taikoma pagal numatytąsias finansines dimensijas ir registravimo sąranką.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš atliekant sinchronizavimą būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus ir sinchronizuoti projektus, projektų užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, projekto faktinių duomenų šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.

- Pakeiskite „Project Service Automation“ operacijos tipą tinkamu „Finance“ operacijos tipu. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Project Service Automation“ atsiskaitymo tipą tinkamu „Finance“ atsiskaitymo tipu. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas. Tada atsiskaitymo tipas susiejamas su reikšme **eilutės ypatybė** pagal „Project Service Automation“ integravimo parametrų puslapyje nurodytą konfigūraciją.
- Filtruoti konkrečias reikšmes Išteklių organizacijos vienetai, kurios turi būti sinchronizuojamos su šiuo šablonu.
- Jei faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės bus sinchronizuojamos su „Finance“, reikšmę sutarties organizacijos vienetas būtina pakeisti tinkama „Finance“ reikšme juridinis subjektas. Faktinių projekto reikšmių (iš PSA į „Fin and Ops“) šablone nurodytas demonstraciniais duomenimis grįstas sąlyginis stulpelis. Paskutinį įterptą sąlygos stulpelį būtina atnaujinti, nurodant tinkamus juridinius subjektus. To nepadarius gali būti rodoma integravimo klaida arba į „Finance“ gali būti importuotos netinkamos faktinės operacijos.
- Jei faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės nebus sinchronizuojamos su „Finance“, iš šablono būtina panaikinti paskutinį įterptą sąlyginį stulpelį. To nepadarius gali būti rodoma integravimo klaida arba į „Finance“ gali būti importuotos netinkamos faktinės operacijos.

#### <a name="contract-organizational-unit"></a>Sutarties organizacijos vienetas
Norėdami atnaujinti šablono stulpelyje įterptą sąlygą, spustelėję rodyklę **Susieti** atidarykite susiejimą. Pasirinkite nuorodą **Išplėstinė užklausa ir Filtravimas**, kad atidarytumėte „Power Query“.

- Jei naudojate numatytąjį faktinių „Project“ reikšmių (iš PSA į „Fin and Ops“) šabloną, „Power Query“ skyriuje **Pritaikyti veiksmai** paspauskite paskutinę **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **USSI** pakeiskite reikšmės Juridinis subjektas pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Prireikus į įrašą **Funkcija** įtraukite papildomų sąlygų ir atnaujinkite sąlygą **kita** iš **USMF** į tinkamą reikšmę Juridinis subjektas.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį, kad būtų palaikomas vidinis įmonės grafikas ir išlaidos. Paspauskite **Įtraukti sąlyginį stulpelį** ir įveskite stulpelio pavadinimą, pvz., **Juridinis subjektas**. Įveskite stulpelio sąlygą, kur, jei **msdyn\_contractorganizationalunitid.msdyn\_pavadinimas** yra \<organizacijos vienetas\>, tada \<įvesti juridinį subjektą\>;

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma „Project Service Automation“ laukų informacija, kuri bus sinchronizuojama su „Finance“.

[![Šablono susiejimas](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Integravus iš „Project Service Automation“, importuoti iš išdėstymo lentelės

Importavimo iš paruošimo lentelės periodinis procesas turi būti paleidžiamas atlikus faktinių reikšmių sinchronizavimą iš „Project Service Automation“ į „Finance“. Vykdant šį procesą projekto operacijos importuojamos iš išdėstymo lentelės į „Project Service Automation“ integravimo žurnalą, kuriame taikoma apskaita ir galima užregistruoti importuotas operacijas. Rekomenduojame paleisti šį procesą paketo režimu; taip pat galima nustatyti, kad jis būtų vykdomas kaip pasikartojantis paketas.

## <a name="update-actuals-from-finance"></a>„Finance“ faktinių duomenų atnaujinimas

### <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojamos norint sinchronizuoti kvito numerį ir užregistruotų projekto operacijų PVM iš „Finance“ į „Project Service Automation“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinių projekto reikšmių naujinimas (iš „Fin Ops“ į PSA)
- **Užduočių pavadinimas projekte**

    - Faktiniai dydžiai 
    - Operacijų ryšiai

### <a name="entity-set"></a>Objektų rinkinys

| Finansai                                                  | „Project Service Automation“ |
|----------------------------------------------------------|----------------------------|
| Projekto faktinių duomenų integravimo objektas                   | Faktinės reikšmės                    |
| Projekto operacijų ryšių integravimo objektas | Operacijų ryšiai    |

### <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance“ projekto integravimo žurnalu. Užregistravus faktines reikšmes „Finance“ jos atnaujinamos „Project Service Automation“, naudojant kvito numerį iš „Finance“. Jei „Finance“ buvo įtrauktas PVM, „Project Service Automation“ bus sukurtos naujos faktinės mokesčių reikšmės.

### <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytas užduotis, projekto faktinių duomenų naujinimo šablone turite naudoti „Microsoft Power Query“, skirtą „Excel“.

- Pakeiskite „Finance“ operacijos tipą, nurodydami tinkamą „Project Service Automation“ operacijos tipą. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Finance“ atsiskaitymo tipą, nurodydami tinkamą „Project Service Automation“ atsiskaitymo tipą. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.

### <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma „Finance“ laukų informacija, kuri bus sinchronizuojama su „Project Service Automation“.

[![Šablono susiejimas](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
