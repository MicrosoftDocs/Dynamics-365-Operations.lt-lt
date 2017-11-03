---
title: Vieno kvito ir valiutos kurso pasikeitimo naujinimas
description: "Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Vieno kvito ir valiutos kurso pasikeitimo naujinimas

[!include[banner](../includes/banner.md)]


Kai kurios organizacijos įveda žurnalus, kuriuose yra vienas kvitas, turintis daugiau nei vieną klientą ar tiekėją, be to, vykdo Gautinų sumų ar Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Šioje temoje aprašyti veiksmai, kuriuos tos organizacijos turi atlikti, atnaujinant „Microsoft Dynamics 365 for Operations“ į 1611 versiją.

Atlikite šiuos veiksmus atnaujindami „Microsoft Dynamics 365 for Operations“ į 1611 versiją.

1.  Prieš atnaujindami į „Dynamics 365 for Operations“, įvykdykite Gautinų sumų ir Mokėtinų sumų užsienio valiutos kurso pasikeitimo procesą. Nustatykite lauką **Metodas** į **Sąskaitos faktūros data**. Sukuriama pasikeitimo operacija, kuri anuliuoja paskutinį užsienio valiutos pasikeitimą. Todėl atidarytos operacijos vertinamos pradine operacijos apskaitos valiuta.
2.  Atnaujinkite „Dynamics 365 for Operations“ į 1611 versiją.
3.  Įvykdykite Gautinų sumų ir mokėtinų sumų užsienio valiutos pasikeitimo procesą dar kartą. Šį kartą lauką **Metodas** nustatykite į **Standartinis**. Sukuriama nauja pasikeitimo operacija, kuri pagrįsta dabartiniu užsienio valiutos kursu. Ši operacija įrašo nerealizuotą pelną / nuostolį ir koreguoja suvestinę DK sąskaitą.





