---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio dimensiją ir kaip ją priskirti atitinkamai produkto dimensijų grupei.
author: t-benebo
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e77c8eabe1657f7fbfef71747627207dccff3b60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887318"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio dimensiją ir kaip ją priskirti atitinkamai produkto dimensijų grupei. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis. Paprastai šią užduotį atlieka produkto kūrėjas.


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