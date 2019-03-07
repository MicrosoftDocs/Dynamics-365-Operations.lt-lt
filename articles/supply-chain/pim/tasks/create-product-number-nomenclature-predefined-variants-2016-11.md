---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šiame vadove parodoma, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerių nomenklatūrą ir kaip ją priskirti atitinkamai produkto dimensijų grupei.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "364884"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas

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

