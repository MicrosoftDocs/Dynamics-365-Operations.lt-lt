---
title: Prižiūrėti atributų tipus
description: Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783454"
---
# <a name="maintenance-attribute-types"></a>Prižiūrėti atributų tipus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą. Atributai naudojami įvairių elementų ypatybėms apibūdinti. Kiekviename skirtuke galite nustatyti šiuos parametrus:

- [Funkcinių vietovių tipai](../setup-for-functional-locations/functional-location-types.md)
- [Funkcinės vietovės](../functional-locations/create-functional-locations.md)
- [Turto tipas](../setup-for-objects/object-types.md)
- Turtas

Atributai, kuriuos galite nustatyti, kinta priklausomai nuo elemento. Pavyzdžiui, funkcinei vietovei galite nustatyti vietovės konfigūracijos ir fizinio dydžio atributus. Turto tipui arba turtui galite nustatyti variklio tūrio, energijos suvartojimo ir didžiausios apkrovos pajėgumo skirtingomis sąlygomis atributus.

## <a name="create-attribute-types"></a>Atributų tipų kūrimas

Galite sukurti savo atributų tipus. Be to, galite perkelti produkto dimensijas iš Microsoft Dynamics 365 for Finance and Operations į puslapį **Attribute types**.

1. Pasirinkite **Asset management** \> **Setup** \> **Attribute types**.
2. Kai atributus nustatote pirmą kartą, pasirinkite **Create product dimensions**, kad automatiškai perkeltumėte standartines „Finance and Operations“ produkto dimensijas.
3. Pasirinkite **New**, kad sukurtumėte naują atributo tipą.
4. Lauke **Attribute type** įveskite atributo tipo pavadinimą.
5. Lauke **Description** įveskite aprašą.
6. Lauke **Vienetas** pasirinkite atitinkamą atributo vienetą, kaip reikalaujama.
7. Lauke **Data type**pasirinkite paketo tipą
8. Jei duomenų tipu pasirinkote **String**, atlikite šiuos veiksmus, kad šiam atributo tipui sukurtumėte reikšmes:

    1. Pasirinkite atributo tipą ir pasirinkite **reikšmės**.
    2. Lauke **Atributo kodas** pasirinkite **Visi**.
    3. Lauke **Atributo tipas** pasirinkite atributo tipą.
    4. Lauke **Value** įveskite arba pasirinkite reikšmę.
    5. Lauke **Description** įveskite aprašą.
    6. Įrašykite įrašą.
    7. Grįžkite į puslapį **Attribute types**.

9. Įrašykite įrašą.

    Lauke **Funkcinių vietovių tipai** rodomas funkcinių vietovių, kurios naudoja šį atributo tipą, skaičius. Lauke **Turto tipai** rodomas jį naudojančių turto tipų skaičius.
