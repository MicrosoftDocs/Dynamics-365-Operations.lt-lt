---
title: Variantų grupės kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti produkto dydžio, stiliaus arba spalvų variantų grupę Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270106"
---
# <a name="create-a-variant-group"></a>Variantų grupės kūrimas


[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti produkto dydžio, stiliaus arba spalvų variantų grupę Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Peržiūra

„Dynamics 365 Commerce“ palaikomi keli produktų variantai. Ji puikiai tinka įvairių produktų kategorijų variantų grupėms nustatyti. Pavyzdžiui, galima sukurti marškinėlių dydžių grupę, įtraukus labai mažą, mažą, vidutinį, didelį ir labai didelį dydžius, ar spalvų grupę, įtraukus visas galimas produkto spalvas. Variantų grupes reikėtų įtraukti prieš įtraukiant produktus.

Šiame straipsnyje bus sukurta ir sukonfigūruota dydžių grupė. Panašiomis procedūromis galima vadovautis, norint įtraukti ir sukonfigūruoti stilių ir spalvų grupes.

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

![Dydžių grupės kūrimas.](media/Size-Groups.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų informacijos apžvalga](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Mažmeninės prekybos produktų nustatymas](set-up-retail-products.md)

[Produktų dimensijos](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
