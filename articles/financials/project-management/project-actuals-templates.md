---
title: "„Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“"
description: "Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ faktines projekto reikšmes su „Dynamics 365 for Finance and Operations“."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: lt-lt
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>„Project Service Automation“ faktinių projekto reikšmių tiesioginis sinchronizavimas su projekto integravimo žurnalu, kad būtų galima registuroti „Finance and Operations“

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, naudojamos tiesiogiai sinchronizuojant „Microsoft Dynamics 365 for Project Service Automation“ faktines projekto reikšmes su „Dynamics 365 for Finance and Operations“.

Šablonas sinchronizuoja operacijas iš „Project Service Automation“ į „Finance and Operations“ išdėstymo lentelę. Atlikus sinchronizavimą būtina importuoti iš išdėstymo lentelės į integravimo žurnalą.

> [!NOTE]
> Faktinių projekto reikšmių integravimą galima atlikti naudojant „Dynamics 365 for Finance and Operations“ versiją 8.01.

> [!NOTE]
> Įvedant „Project Service Automation“ grafiko ir išlaidų operacijų PVM sumas būtina įdiegti „Project Service Automation“ 7 naujinimą. Jei šis naujinimas neįdiegtas, faktinės mokesčių reikšmės nebus susietos su atitinkamomis faktinėmis grafiko ir išlaidų reikšmėmis ir nebus sinchronizuojamos su „Finance and Operations“. Jei reikia daugiau informacijos, kreipkitės į pagalbos tarnybą.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>„Project Service Automation“ duomenų srautas į „Finance and Operations“

Naudojantis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu sinchronizuojant duomenis „Project Service Automation“ ir „Finance and Operations“ egzemplioriuose naudojama funkcija Duomenų integravimas. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas duomenų apie faktines projekto reikšmes srautas iš „Project Service Automation“ į „Finance and Operations“.

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys tarp „Project Service Automation“ ir „Finance and Operations“.

[![„Project Service Automation“ integravimo su „Finance and Operations“ duomenų srautas](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami atidaryti pasiekiamus šablonus, „Microsoft PowerApps“ administravimo centre paspauskite **Projektai**, po to viršutiniame dešiniajame kampe paspauskite **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys naudojamos sinchronizuojant „Project Service Automation“ faktines projekto reikšmes su „Finance and Operations“.

-  **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinės projekto reikšmės (iš PSA į „Fin and Ops“)

-  **Užduočių pavadinimas projekte** 
    - Faktinės reikšmės 
    - Operacijų ryšiai

## <a name="entity-set"></a>Objektų rinkinys

| „Project Service Automation“      | „Finance and Operations”                                      |
|---------------------------------|-------------------------------------------------------------|
| Faktinės reikšmės                         | Projekto faktinių duomenų integravimo objektas                      |
| Operacijų ryšiai         | Projekto operacijų ryšių integravimo objektas    |

## <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ projekto integravimo žurnalu. Apskaita taikoma pagal numatytąsias finansines dimensijas ir registravimo sąranką.

## <a name="preconditions"></a>Išankstinės sąlygos

Prieš atliekant sinchronizavimą būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus ir sinchronizuoti projektus, projektų užduotis ir projekto išlaidų operacijų kategorijas.

## <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytus veiksmus, faktinių projekto reikšmių šablone turite naudoti „Microsoft Power Query“.
- Pakeiskite „Project Service Automation“ reikšmę **operacijos tipas**, nurodydami tinkamą „Finance and Operations“ reikšmę **operacijos tipas**. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Project Service Automation“ reikšmę **atsiskaitymo tipas**, nurodydami tinkamą „Finance and Operations“ reikšmę **atsiskaitymo tipas**. Faktinių projekto reikšmių (iš PSA į „Fin Ops“) šablone šis pakeitimas jau buvo nurodytas. Tada atsiskaitymo tipas susiejamas su reikšme **eilutės ypatybė** pagal „Dynamics 365 for Project Service Automation“ integravimo parametrų formoje nurodytą konfigūraciją.
- Filtruoti konkrečias reikšmes **Išteklių organizacijos vienetai**, kurios turi būti sinchronizuojamos su šiuo šablonu.
- Jei **faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės** bus sinchronizuojamos su „Finance and Operations“, reikšmę **sutarties organizacijos vienetas** būtina pakeisti tinkama „Finance and Operations“ reikšme **juridinis subjektas**. Faktinių projekto reikšmių (iš PSA į „Fin and Ops“) šablone nurodytas demonstraciniais duomenimis grįstas sąlyginis stulpelis. Paskutinį įterptą sąlygos stulpelį būtina atnaujinti, nurodant tinkamus juridinius subjektus. To nepadarius gali būti rodoma integravimo klaida arba į „Finance and Operations“ gali būti importuotos netinkamos faktinės operacijos.
- Jei **faktinės vidinio įmonės grafiko arba vidinių įmonės išlaidų reikšmės** nebus sinchronizuojamos su „Finance and operations“, iš šablono būtina panaikinti paskutinį įterptą sąlygos stulpelį. To nepadarius gali būti rodoma integravimo klaida arba į „Finance and Operations“ gali būti importuotos netinkamos faktinės operacijos.

### <a name="contract-organizational-unit"></a>Sutarties organizacijos vienetas
Norėdami atnaujinti šablono stulpelyje įterptą sąlygą, spustelėję rodyklę **Susieti** atidarykite susiejimą. Paspauskite norėdami atidaryti funkcijų Išplėstinė užklausa ir Filtravimas langus.
- Jei naudojate numatytąjį faktinių „Microsoft Project“ reikšmių (iš PSA į „Fin and Ops“) šabloną, skyriuje **Pritaikyti veiksmai** paspauskite lasat **Įterpta sąlyga**. Įraše **Funkcija** reikšmę **USSI** pakeiskite reikšmės **Juridinis subjektas** pavadinimu, kuris turėtų būti naudojamas atliekant integravimą. Prireikus į įrašą **Funkcija** įtraukite papildomų sąlygų ir atnaujinkite sąlygą **kita** iš **USMF** į tinkamą reikšmę **Juridinis subjektas**.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį, kad būtų palaikomas vidinis įmonės grafikas ir išlaidos. Paspauskite **Įtraukti sąlyginį stulpelį** ir nurodykite stulpelio pavadinimą, pvz., LegalEntity. Įveskite stulpelio sąlygą: jei msdyn_contractorganizationalunitid.msdyn_name yra <organizational unit>, tada <enter the Legal entity>; kitu atveju reikšmė neapibrėžta.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktoje iliustracijoje vaizduojamas šablono užduoties susiejimo pavyzdys naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Project Service Automation“ sinchronizavimą su „Finance and Operations“.

[![Šablono susiejimas](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Importuoti iš išdėstymo lentelės

Importavimas iš išdėstymo lentelės periodinio proceso turi būti paleidžiamas atlikus faktinių reikšmių sinchronizavimą iš „Project Service Automation“ į „Finance and Operations“. Vykdant šį procesą projekto operacijos importuojamos iš išdėstymo lentelės į „Project Service Automation“ integravimo žurnalą, kuriame taikoma apskaita ir galima užregistruoti importuotas operacijas. Rekomenduojama paleisti šį procesą paketo režimu, taip pat galima nustatyti, kad jis būtų vykdomas kaip pasikartojantis paketas.

## <a name="update-actuals"></a>Faktinių reikšmių naujinimas

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojamos norint sinchronizuoti kvito numerį ir užregistruotų projekto operacijų PVM iš „Finance and Operations“ į „Project Service Automation“:

-  **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** faktinių projekto reikšmių naujinimas (iš „Fin Ops“ į PSA)
-  **Užduočių pavadinimas projekte** 
     - Faktinės reikšmės 
     - Operacijų ryšiai

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”                                         | „Project Service Automation“        |
|----------------------------------------------------------------|-----------------------------------|
| Projekto faktinių duomenų integravimo objektas                         | Faktinės reikšmės                           |
| Projekto operacijų ryšių integravimo objektas       | Operacijų ryšiai           |

## <a name="entity-flow"></a>Objekto srautas

Faktinės projekto reikšmės tvarkomos naudojantis „Project Service Automation“ ir yra sinchronizuojamos su „Finance and Operations“ projekto integravimo žurnalu. Užregistravus faktines reikšmes „Finance and Operations“ jos atnaujinamos „Project Service Automation“, naudojant kvito numerį iš „Finance and Operations“. Jei „Finance and Operations“ buvo įtraukti PVM mokesčiai, „PRoject Service Automation“ bus sukurtos naujos faktinės mokesčių reikšmės.

## <a name="power-query"></a>„Power Query“

Norėdami atlikti toliau nurodytus veiksmus, faktinių projekto reikšmių naujinimo šablone turite naudoti „Microsoft Power Query“.
- Pakeiskite „Finance and Operations“ reikšmę **operacijos tipas**, nurodydami tinkamą „Project Service Automation“ reikšmę **operacijos tipas**. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.
- Pakeiskite „Finance and Operations“ reikšmę **atsiskaitymo tipas**, nurodydami tinkamą „Project Service Automation“ reikšmę **atsiskaitymo tipas**. Faktinių projekto reikšmių naujinimo (iš „Fin Ops“ į PSA) šablone šis pakeitimas jau buvo nurodytas.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojami šablono užduoties susiejimų pavyzdžiai naudojant funkciją Duomenų integravimas. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama atliekant „Finance and Operations“ sinchronizavimą su „Project Service Automation“.

[![Šablono susiejimas](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Šablono susiejimas](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




