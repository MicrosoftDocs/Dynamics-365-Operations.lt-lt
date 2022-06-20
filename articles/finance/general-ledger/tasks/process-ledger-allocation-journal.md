---
title: Didžiosios knygos paskirstymo žurnalo apdorojimas
description: Šiame straipsnyje paaiškinama, kaip apdoroti paskirstymo užklausą "Dynamics 365 Finance".
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
ms.openlocfilehash: b86f8f5d090d624e812d9e7e6c0bc0212e5e9716
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902435"
---
# <a name="process-ledger-allocation-journal"></a>Didžiosios knygos paskirstymo žurnalo apdorojimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip apdoroti paskirstymo užklausą. Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas. Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė. Šioje užduotyje naudojama demonstracinė įmonė USMF.

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
