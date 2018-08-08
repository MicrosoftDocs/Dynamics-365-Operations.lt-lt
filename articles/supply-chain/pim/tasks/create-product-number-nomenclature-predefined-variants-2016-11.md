--- 
title: "Iš anksto nustatytų produkto variantų produkto numerių kūrimas"
description: "Šiame vadove parodoma, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerių nomenklatūrą ir kaip ją priskirti atitinkamai produkto dimensijų grupei."
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: c423aab341ddad9383c4c95b9dbb63c9875c99ef
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>Iš anksto nustatytų produkto variantų produkto numerių kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame vadove parodoma, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerių nomenklatūrą ir kaip ją priskirti atitinkamai produkto dimensijų grupei. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis. Paprastai šią užduotį atlieka produkto kūrėjas.


## <a name="create-a-product-number-nomenclature"></a>Produkto numerių nomenklatūros kūrimas
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto nomenklatūra.
3. Spustelėkite Naujas.
4. Lauke Pavadinimas įveskite nomenklatūros pavadinimą, kuris padeda nustatyti tikslinę produkto dimensijų grupę, pavyzdžiui, ColorSize.
5. Lauke Aprašas įveskite reikšmę.
6. Spustelėkite Pridėti.
7. Spustelėkite Bendrojo produkto numeris.
8. Spustelėkite Pridėti.
9. Spustelėkite Teksto konstanta.
10. Lauke „Tekstas“ įveskite reikšmę.
11. Spustelėkite Pridėti.
12. Spustelėkite Spalva.
13. Spustelėkite Pridėti.
14. Spustelėkite Teksto konstanta.
15. Lauke „Tekstas“ įveskite reikšmę.
16. Spustelėkite Pridėti.
17. Spustelėkite Dydis.
18. Uždarykite puslapį.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatūros priskyrimas bendrajam produktui
1. Spustelėkite Produkto dimensijų grupės.
2. Pasirinkite produkto dimensijų grupę SizeCol.
3. Spustelėkite Redaguoti.
4. Lauke Naudoti nomenklatūrą pasirinkite Taip.
5. Lauke Produkto varianto numerių nomenklatūra įveskite arba pasirinkite reikšmę.
6. Uždarykite puslapį.


