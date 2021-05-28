---
title: Klientų įrašai nerodomi „Commerce“ valdymo srityje
description: Šioje temoje pateikiamos trikčių šalinimo gairės, kurios gali padėti, kai klientų įrašai iš karto nerodomi „Commerce“ valdymo srityje.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018487"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Klientų įrašai nerodomi „Commerce“ valdymo srityje

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių šalinimo gairės, kurios gali padėti, kai klientų įrašai iš karto nerodomi „Commerce“ valdymo srityje.

## <a name="description"></a>aprašymas

Kai sukuriate naują kliento įrašą naudodami registracijos srautą el. komercijos vitrinoje, atitinkamas kliento įrašas iš karto nerodomas „Commerce“ valdymo srityje.

## <a name="resolution"></a>Skiriamoji geba

### <a name="disable-customer-creation-in-async-mode"></a>Išjungti kliento kūrimą „Async“ režimu

> [!IMPORTANT]
> Jei išjungsite asinchroninį klientų kūrimą, gali būti paveiktas sistemos našumas, nes sukūrus kiekvieną įrašą „Commerce“ valdymo srityje bus sukuriama užklausa realiuoju laiku. Be to, jei „Commerce“ valdymo sritis neveikia (pvz., aptarnavimo srautų metu), dėl visų naujų klientų kūrimo srautų bus gaunamos klaidos.

Kad išjungtumėte kliento kūrimą asinchroniniu režimu „Commerce“ valdymo srityje, atlikite nurodytus veiksmus.

1. Eikite į **Mažmeninė prekyba ir komercija \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcijų profiliai**.
1. Jei savo interneto kanalui dar nenaudojate funkcijų profilio, sukurkite jį.
1. Įsitikinkite, kad parinktis **Kurti klientą asinchroniniu režimu** nustatyta kaip **Ne**.
1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Internetinės parduotuvės**.
1. Pasirinkite interneto parduotuvę, kad išjungtumėte asinchroninį kliento kūrimą.
1. Skirtuke **Bendra** patikrinkite, ar laukelis **Funkcijų profilis** nustatytas kaip funkcijų profilis, kurį naudojate savo interneto kanalui.

## <a name="additional-resources"></a>Papildomi ištekliai

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](../set-up-b2c-tenant.md)
