---
title: Didžiosios knygos paskirstymo žurnalo apdorojimas
description: Šioje temoje paaiškinama, kaip vykdyti paskirstymo užklausą "Dynamics 365 Finance".
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec3653085aed278eb5d13d47f345c713cd39f1f
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722158"
---
# <a name="process-ledger-allocation-journal"></a>Didžiosios knygos paskirstymo žurnalo apdorojimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą. Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas. Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Naršymo srityje eikite į DK **informaciją> paskirstymai > paskirstymo užklausą**.
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
