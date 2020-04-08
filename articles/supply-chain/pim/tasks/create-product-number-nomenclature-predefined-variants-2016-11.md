---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150060"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis. Paprastai šią užduotį atlieka produkto kūrėjas.


## <a name="create-a-product-number-nomenclature"></a>Produkto numerių nomenklatūros kūrimas
1. Pažymėkite **Produkto varianto modelio aprašas**.
2. Pažymėkite **Produkto nomenklatūra**.
3. Pasirinkite **Naujas**.
4. Lauke **Pavadinimas** įveskite nomenklatūros pavadinimą, kuris padės identifikuoti tikslinę produkto matmenų grupę, pavyzdžiui, `ColorSize`.
5. Lauke **Aprašo laukas**surinkite reikšmę.
6. Pasirinkite **Įtraukti**.
7. Pažymėkite **Produkto pagrindinį** numerį.
8. Pasirinkite **Įtraukti**.
9. Pažymėkite **Teksto konstanta**.
10. Lauke **Tekstas** įveskite reikšmę.
11. Pasirinkite **Įtraukti**.
12. Pažymėkite **Spalva**.
13. Pasirinkite **Įtraukti**.
14. Pažymėkite **Teksto konstanta**.
15. Lauke **Tekstas** įveskite reikšmę.
16. Pasirinkite **Įtraukti**.
17. Pažymėkite **Dydis**.
18. Uždarykite puslapį.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatūros priskyrimas bendrajam produktui
1. Pažymėkite **Produkto matmenų grupės**.
2. Pažymėkite grupę **SizeCol produkto matmuo**.
3. Pasirinkite **Redaguoti**.
4. Pažymėkite **Taip** lauke **Naudoti nomenklatūrą**.
5. Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.
6. Uždarykite puslapį.

