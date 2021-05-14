---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920662"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis. Paprastai šią užduotį atlieka produkto kūrėjas.


## <a name="create-a-product-number-nomenclature"></a>Produkto numerių nomenklatūros kūrimas

1. Eikite į **Produkto informacijos valdymas \> Nustatymas \> Bendroji nomenklatūra**.
1. Pasirinkite **Naujas**.
1. Lauke **Pavadinimas** įveskite nomenklatūros pavadinimą, kuris padės identifikuoti tikslinę produkto matmenų grupę, pavyzdžiui, `ColorSize`.
1. Lauke **Aprašo laukas** surinkite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Produkto pagrindinį** numerį.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Spalva**.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Teksto konstanta**.
1. Lauke **Tekstas** įveskite reikšmę.
1. Pasirinkite **Įtraukti**.
1. Pažymėkite **Dydis**.
1. Uždarykite puslapį.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatūros priskyrimas bendrajam produktui

1. Pažymėkite **Produkto matmenų grupės**.
2. Pažymėkite grupę **SizeCol produkto matmuo**.
3. Pasirinkite **Redaguoti**.
4. Pažymėkite **Taip** lauke **Naudoti nomenklatūrą**.
5. Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.
6. Uždarykite puslapį.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]