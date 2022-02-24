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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a7e8c3ef6fa85daec2a191b433b1ec4ece441ee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968484"
---
# <a name="process-ledger-allocation-journal"></a>Didžiosios knygos paskirstymo žurnalo apdorojimas

[!include [banner](../../includes/banner.md)]

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

