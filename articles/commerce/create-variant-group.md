---
title: Variantų grupės kūrimas
description: Šioje temoje aprašoma, kaip naudojant „Microsoft Dynamics 365 Commerce“ sukurti produkto variantų, besiskiriančių dydžiu, stiliumi ar spalva, grupę.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d9279e1076796bb455429e5ff004c89ec5829e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414345"
---
# <a name="create-a-variant-group"></a>Variantų grupės kūrimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip naudojant „Microsoft Dynamics 365 Commerce“ sukurti produkto variantų, besiskiriančių dydžiu, stiliumi ar spalva, grupę.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ palaikomi keli produktų variantai. Ji puikiai tinka įvairių produktų kategorijų variantų grupėms nustatyti. Pavyzdžiui, galima sukurti marškinėlių dydžių grupę, įtraukus labai mažą, mažą, vidutinį, didelį ir labai didelį dydžius, ar spalvų grupę, įtraukus visas galimas produkto spalvas. Variantų grupes reikėtų įtraukti prieš įtraukiant produktus.

Šioje temoje bus sukurta ir sukonfigūruota dydžių grupė. Panašiomis procedūromis galima vadovautis, norint įtraukti ir sukonfigūruoti stilių ir spalvų grupes.

## <a name="create-a-size-group"></a>Dydžių grupės kūrimas

Norėdami sukurti dydžių grupę, atlikite tolesnius veiksmus.
 
1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Variantų grupės \> Dydžių grupės**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Langelyje **Dydžių grupė** įveskite dydžių grupės pavadinimą.
1. Langelyje **Aprašas** įveskite tinkamą aprašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="add-attributes-to-the-size-group"></a>Atributų įtraukimas į dydžių grupę

Norėdami į dydžių grupę įtraukti atributų, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Variantų grupės \> Dydžių grupės**
1. Naršymo srityje pasirinkite dydžių grupę.
1. Dalyje **Dydžių grupės eilutės** pasirinkite **Įtraukti**.
1. Langelyje **Dydis** įveskite dydį (pavyzdžiui, „XL“) nurodančią eilutę.
1. Langelyje **Dydžio pavadinimas** įveskite dydžio pavadinimą (pavyzdžiui, „Labai didelis“).
1. Langelyje **Papildymo svoris** įveskite skaičių, reiškiantį papildymo svorį.
1. Langelyje **Brūkšninio kodo skaičius** įveskite skaičių, reiškiantį brūkšninį kodą.
1. Langelyje **Rodymo tvarka** įveskite rodymo tvarką reiškiantį skaičių.
1. Įtraukę visus norimus dydžius, veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas dydžių grupės pavyzdys „kasdienių marškinių dydžiai“.

![Dydžių grupės kūrimas](media/create-variant-group.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų informacijos apžvalga](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Mažmeninės prekybos produktų nustatymas](set-up-retail-products.md)

[Produktų dimensijos](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]