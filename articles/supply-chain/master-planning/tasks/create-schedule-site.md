---
title: Vietos grafiko kūrimas
description: Šia procedūra rodoma, kaip planuoti dar nepradėtus vietos gamybos užsakymus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bc2dc4a03f9d937339ec2470f6a065f77c7036a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209633"
---
# <a name="create-a-schedule-for-a-site"></a>Vietos grafiko kūrimas

[!include [banner](../../includes/banner.md)]

Šia procedūra rodoma, kaip planuoti dar nepradėtus vietos gamybos užsakymus.  Atlikti šiai procedūrai naudojama demonstracinių duomenų įmonė USMF.


## <a name="identify-production-orders-that-are-not-started"></a>Nepradėtų gamybos užsakymų identifikavimas
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Vieta reikšme „1“.
    * 1 – tai USMF vieta. Jei USMF nenaudojate, vietą pasirinkite iš savo įmonės.  
3. Atidarykite stulpelio filtrą Būsena.
4. Laukui Būsena taikykite filtrą – reikšmę Suplanuota, naudodami filtro operatorių „yra tiksliai‟.

## <a name="create-a-schedule"></a>Grafiko kūrimas
1. Pažymėkite arba atžymėkite visas sąrašo eilutes.
2. Veiksmų srityje spustelėkite Grafikas.
3. Spustelėkite Planuoti užduotis.
4. Lauke Planavimo kryptis pasirinkite „Atgal nuo pristatymo datos‟.
5. Lauke Ribotas pajėgumas pasirinkite Ne.
6. Lauke Ribotos medžiagos pasirinkite Ne.
7. Spustelėkite GERAI.
    * Tai gali užtrukti.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Suplanuotų gamybos užsakymų rezultato peržiūra
1. Sąraše pažymėkite pasirinktą eilutę.
    * Galite pažymėti bet kurią eilutę.  
2. Veiksmų srityje spustelėkite Gamybos užsakymas.
3. Spustelėkite Visos užduotys.
    * Šiame puslapyje galite matyti užduočių sąrašą. Skirtuke Planavimas galite matyti užduoties pradžios datą ir pabaigos datą.  
4. Spustelėkite Medžiagos.
    * Šiame puslapyje galite matyti įvertintą medžiagų suvartojimą gamybos užsakymo operacijoms atlikti ir dabartines turimas atsargas.  

