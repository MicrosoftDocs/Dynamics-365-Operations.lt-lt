---
title: Didžiosios knygos paskirstymo žurnalo apdorojimas
description: Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą programoje „Dynamics 365 Finance“.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186077"
---
# <a name="process-ledger-allocation-journal"></a>Didžiosios knygos paskirstymo žurnalo apdorojimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą. Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas. Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymo užklausos procesas**.
2. Lauke **Taisyklė** pasirinkite norimą įrašą išplečiamajame meniu.
3. Lauke **Nuo datos** įveskite datą.

    - Laukas **Nuo datos** yra ypač svarbus, kai DK yra taisyklės duomenų šaltinis. Šia data reguliuojama, kuriuos didžiosios knygos balansus įtraukti į paskirstymą.  
    - Lauke **Nulinis šaltinis** pasirinkite **Stabdyti**. Šiuo veiksmu sustabdysite paskirstymo procesą ir pasirodys pranešimas, kuriama bus nurodoma, jog buvo pasirinktas nulinis šaltinių skaičius.  

4. Lauke **Pasiūlymo parinktys** pasirinkite **Tik pasiūlymas**. Pasirinkite **Tik pasiūlymas** peržiūrėti ir papildomai patvirtinti rezultatus paskirstymo žurnale prieš registruodami paskirstymą DK.  
5. Lauke DK registravimo data įveskite datą.
6. Pasirinkite **Gerai**.
7. Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymų žurnalai**.
8. Pasirinkite **Eilutės**.
9. Pasirinkite **Registruoti**.
10. Pasirinkite **Registruoti**.
