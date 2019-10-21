---
title: „Project Service Automation“ apžvalga
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Service Automation“ ir „Dynamics 365 Finance“ integravimo sprendimą.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250558"
---
# <a name="project-service-automation-overview"></a>„Project Service Automation“ apžvalga

[!include[banner](../includes/banner.md)]

Integravimo iš „Project Service Automation“ į „Finance“ sprendime naudojant funkciją Duomenų integravimas ir „Common Data Service“ sinchronizuojami duomenys „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“ egzemplioriuose. Naudojantis integravimo šablonais, kurie pasiekiami naudojantis funkcija Duomenų integravimas, įgalinamas projektų, projekto sutarčių, projekto sutarčių eilučių, projekto sutarties eilutės etapų, projekto užduočių, išlaidų operacijų kategorijų, apytikslių grafiko reikšmių ir apytikslių išlaidų reikšmių srautas iš „Project Service Automation“ į „Finance“.

> [!NOTE]
> - Jei naudojate 7.3.0 versiją, turite įdiegti KB 4074835. Tada galėsite integruoti fiksuotos kainos projektus.
> - Jei naudojate 7.3.0 versiją ir atliekate mokesčio operacijas naudodami „Project Service Automation“, turite įdiegti KB 4345320, kad šie mokesčiai būtų įtraukti į projekto SF.
> - Jei naudojate 8.0 versiją, galėsite naudotis projekto užduoties integravimu, išlaidų operacijos kategorijomis, apytikslėmis grafiko reikšmėmis, apytikslėmis išlaidų reikšmėmis ir funkcijų užrakinimu.
> - Jei naudojate 8.0.1 arba naujesnę versiją, galėsite sinchronizuoti faktines reikšmes.

Tam, kad būtų galima integruoti „Project Service Automation“ su „Finance“, būtina sukonfigūruoti „Project Service Automation“ integravimo parametrus. Norėdami gauti daugiau informacijos, žr. [„Project Service Automation“ integravimo parametrus](PSA-parameters.md).

Naudojantis šiuo integravimo sprendimu galima tiesiogiai sinchronizuoti toliau nurodytais atvejais.

- Išsaugoti „Project Service Automation“ projekto sutartis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutartis su „Finance“ projekto sutartimis.
- Sukurti „Project Service Automation“ projektus ir tiesiogiai sinchronizuoti „Project Service Automation“ projektus su „Finance“ projektais.
- Išsaugoti „Project Service Automation“ projekto sutarčių eilutes ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarčių eilutes su „Finance“ projekto sutarčių eilutėmis.
- Išsaugoti „Project Service Automation“ projekto sutarčių eilučių etapus ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto sutarčių eilučių etapus su „Finance“ projekto sutarčių eilučių etapais.
- Išsaugoti „Project Service Automation“ projekto užduotis ir tiesiogiai sinchronizuoti „Project Service Automation“ projekto užduotis su „Finance“ projekto užduotimis.
- Išsaugoti „Finance“ išlaidų operacijos kategorijas ir tiesiogiai sinchronizuoti „Finance“ išlaidų operacijos kategorijas su „Project Service Automation“ išlaidų operacijos kategorijomis.
- Sukurti „Project Service Automation“ apytiksles projekto grafiko reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto grafiko reikšmes su „Finance“ apytikslėmis projekto grafiko reikšmėmis.
- Sukurti „Project Service Automation“ apytiksles projekto išlaidų reikšmes ir tiesiogiai sinchronizuoti „Project Service Automation“ apytiksles projekto išlaidų reikšmes su „Finance“ apytikslėmis projekto išlaidų reikšmėmis.
- Kurti projekto grafiko, išlaidų ir mokesčių faktines reikšmes naudodamiesi „Project Service Automation“, o projekto operacijas kurti „Project Service Automation“ integravimo žurnale, kad jos būtų paskelbtos „Finance“.

## <a name="data-synchronization"></a>Duomenų sinchronizavimas

Toliau esančiame paveikslėlyje rodoma, kaip sinchronizuojami duomenys atliekant „Project Service Automation“ ir „Finance“ integravimą.

> [!NOTE]
> Šiuo metu galima naudotis ne visais šablonais. Šablonai bus išleisti juos baigus.

[![„Project Service Automation“ ir „Finance“ integravimas](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>„Finance“ sistemos reikalavimai

Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance“ sprendimu, turite įdiegti „Enterprise Edition 7.3“ su 12 ar naujesniu „Platform“ naujinimu.

## <a name="system-requirements-for-project-service-automation"></a>„Project Service Automation“ sistemos reikalavimai

Norėdami naudotis integravimo iš „Project Service Automation“ į „Finance“ sprendimu, turite įdiegti toliau nurodytus komponentus.

- „Dynamics 365 Project Service Automation“ 9.0.0.0 arba naujesnė versija
- Sprendimui „Dynamics 365 Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai 1.14.0.0 (v14) arba naujesnė versija
- „Project Service Automation“ į „Finance“ sprendimas, skirtas „Dynamics 365 Project Service Automation“ 1.0.0.0 arba naujesnei versijai

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>„Project Service Automation“ integravimo į „Finance“ sprendimo diegimas „Project Service Automation“ egzemplioriuje

Atsisiųskite „Project Service Automation“ integravimo į „Finance“ sprendimą iš [„Microsoft“ atsisiuntimo centro](https://www.microsoft.com/download/details.aspx?id=57016) ir sekite prie sprendimo pridėtas instrukcijas.
