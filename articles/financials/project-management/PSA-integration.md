---
title: „Project Service Automation“
description: Šioje temoje pateikiama informacija apie „Project Service Automation“ integravimo į „Finance and Operations“ sprendimą. Šiame integravimo sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Project Service Automation“ egzemplioriuose.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "335697"
---
# <a name="project-service-automation"></a>„Project Service Automation“

[!include[banner](../includes/banner.md)]

Integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Project Service Automation“ egzemplioriuose. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas projektų, projekto sutarčių, projekto sutarčių eilučių, projekto sutarties eilutės etapų, projekto užduočių, išlaidų operacijų kategorijų, apytikslių grafiko reikšmių ir apytikslių išlaidų reikšmių srautas iš „Project Service Automation“ į „Finance and Operations“.

> [!NOTE]
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0“, įdiegę KB 4132657 ir KB 4132660 naudodami šablonus galėsite integruoti projekto užduotis, išlaidų operacijos kategorijas, apytiksles grafiko reikšmes, apytiksles išlaidų reikšmes ir faktines reikšmes, taip pat konfigūruoti funkcijų užrakinimą. Prireikus iš naujo nustatyti apskaitos paskirstymus, rekomenduojame įdiegti ir KB 4131710.
> - Jei naudojate „Finance and Operations“ versiją 7.3.0, turite įdiegti KB 4074835. Tada galėsite integruoti fiksuotos kainos projektus.
> - Jei naudojate „Finance and Operations 7.3.0“ ir atliekate mokesčio operacijas naudodami „Project Service Automation“, turite įdiegti KB 4345320, kad šie mokesčiai būtų įtraukti į projekto SF.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations“ versiją 8.0, galėsite naudotis projekto užduoties integravimu, išlaidų operacijos kategorijomis, apytikslėmis grafiko reikšmėmis, apytikslėmis išlaidų reikšmėmis ir funkcijų užrakinimu.
> - Jei naudojate „Microsoft Dynamics 365 for Finance and Operations“ 8.0.1 arba naujesnę versiją, galėsite sinchronizuoti faktines reikšmes.

Tam, kad būtų galima integruoti „Project Service Automation“ su „Finance and Operations“, būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus. Norėdami gauti daugiau informacijos, žr. [„Project Service Automation“ integravimo parametrus](PSA-parameters.md).

Naudojantis šiuo integravimo sprendimu galima tiesiogiai sinchronizuoti toliau nurodytais atvejais.

- Išsaugoti „Project Service Automation“ projekto sutartis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutartis su „Finance and Operations“ projekto sutartimis.
- Sukurti „Project Service Automation“ projektus ir tiesiogiai sinchronizuoti „Project Service Automation“ projektus su „Finance and Operations“ projektais.
- Išsaugoti „Project Service Automation“ projekto sutarties eilutes ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarties eilutes su „Finance and Operations“ projekto sutarties eilutėmis.
- Išsaugoti „Project Service Automation“ projekto sutarties eilutės etapus ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarties eilutės etapus su „Finance and Operations“ projekto sutarties eilutės etapais.
- Išsaugoti „Project Service Automation“ projekto užduotis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto užduotis su „Finance and Operations“ projekto užduotimis.
- Išsaugoti „Finance and Operations“ išlaidų operacijos kategorijas ir tiesiogiai sinchronizuoti „Project Service Automation“ išlaidų operacijos kategorijas su „Finance and Operations“ išlaidų operacijos kategorijomis.
- Sukurti „Project Service Automation“ apytiksles projekto grafiko reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto grafiko reikšmes su „Finance and Operations“ apytikslėmis projekto grafiko reikšmėmis.
- Sukurti „Project Service Automation“ apytiksles projekto išlaidų reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto išlaidų reikšmes su „Finance and Operations“ apytikslėmis projekto išlaidų reikšmėmis.
- Kurkite projekto laiko, išlaidų ir mokesčių faktines reikšmes naudodamiesi „Project Service Automation“, o projekto operacijas kurkite „Project Service Automation“ integravimo žurnale, kad jos būtų paskelbtos „Finance and Operations“.

## <a name="data-synchronization"></a>Duomenų sinchronizavimas

Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami duomenys atliekant „Project Service Automation“ ir „Finance and Operations“ integravimą.

> [!NOTE]
> Šiuo metu galima naudotis ne visais šablonais. Šablonai bus išleisti juos baigus.

[![„Project Service Automation“ integravimas su „Finance and Operations“](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>„Finance and Operations“ sistemos reikalavimai

Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu, turite įdiegti „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3“ su 12 ar naujesniu platformos naujinimu.

## <a name="system-requirements-for-project-service-automation"></a>„Project Service Automation“ sistemos reikalavimai

Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance and Operations“ sprendimu, turite įdiegti toliau nurodytus komponentus.

- „Microsoft Dynamics 365 for Project Service Automation“ 9.0.0.0 arba naujesnė versija
- Sprendimui „Microsoft Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.14.0.0 (v14) arba naujesnė
- „Project Service Automation to Finance and Operations“ sprendimas, skirtas „Microsoft Dynamics 365 for Project Service Automation“ 1.0.0.0 arba naujesnei versijai

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>„Project Service Automation“ integravimo į „Finance and Operations“ sprendimo diegimas „Project Service Automation“ egzemplioriuje

Atsisiųskite „Project Service Automation“ integravimo į „Finance and Operations“ sprendimą iš [„Microsoft“ atsisiuntimo centro](https://www.microsoft.com/en-us/download/details.aspx?id=57016) ir sekite prie sprendimo pridėtas instrukcijas.
