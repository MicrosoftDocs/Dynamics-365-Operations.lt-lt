---
title: Sandėlio nustatymas
description: Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993658"
---
# <a name="warehouse-set-up"></a>Sandėlio nustatymas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.

## <a name="overview"></a>Peržiūrėti

Kiekvieną „Commerce“ kanalą reikia susieti su sukonfigūruotu sandėliu. Toliau pateiktos procedūros yra minimalios konfigūracijos, kurias reikia atlikti norint nustatyti „Commerce“ kanalo sandėlį. Daugiau informacijos apie sandėlio nustatymą žr. [Sandėlio valdymo peržiūra](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Sandėlis vietos konfigūravimas

Prieš nustatydami sandėlį, turite sukonfigūruoti sandėlio vietą.

Norėdami sukonfigūruoti sandėlio vietą, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Vieta** įveskite reikšmę.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Skyriuje **Bendra** nustatykite reikiamą **Laiko juosta**.
1. Skyriuje **Adresai** įveskite adresą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas sandėlio vietos pavyzdys.

![Sandėlio vietos pavyzdys](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Sandėlio nustatymas

Norėdami nustatyti sandėlį, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Sandėlis** įveskite reikšmę.  Jei tai yra 1:1 parduotuvės susiejimas, apsvarstykite parduotuvės pavadinimo arba regiono platintojo centro pavadinimo naudojimą.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Išplečiamajame sąraše **Vieta** pasirinkite anksčiau sukurtą sandėlio vietą.
1. Lauke **Tipas** pasirinkite **Numatytasis**.
    - Jei norite nustatyti **Sulaikymo sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Sulaikymas**.
    - Jei norite nustatyti **Tranzito sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Tranzitas**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="set-up-inventory-aisles"></a>Nustatyti atsargų perėjimus

Norėdami nustatyti atsargų perėjimus, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos sąranka \> Atsargų perėjimas**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Išplečiamajame sąraše **Sandėlis** pasirinkite anksčiau sukurtą sandėlį.
1. Lauke **Perėjimas** įveskite pavadinimą (pavyzdžiui, „Def“).
1. Lauke **Pavadinimas** įveskite pavadinimą (pavyzdžiui, „Numatytasis perėjimas“).
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="set-up-warehouse-inventory-locations"></a>Sandėlio atsargų vietų nustatymas

Norėdami nustatyti standartinių, pažeistų ar grąžintų sandėlio atsargų vietas, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.
1. Pasirinkite sandėlį, kurį sukūrėte anksčiau.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Veiksmų srityje pasirinkite **Sandėlis**, tada pasirinkite **Atsargų vieta**.
1. Veiksmų srityje pasirinkite **Nauja**. Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.
    1. Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą. 
    1. Nustatykite **Rankinis naujinimas** kaip **Taip**.
    1. Lauke **Vieta** įveskite sandėlio pavadinimą.
    1. Veiksmų srityje pasirinkite **Įrašyti**.
 1. Veiksmų srityje pasirinkite **Nauja**.  Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.
    1. Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.  
    1. Nustatykite **Rankinis naujinimas** kaip **Taip**.
    1. Lauke **Vieta** įveskite „Sugadintos“.
    1. Veiksmų srityje pasirinkite **Įrašyti**.
 1. Veiksmų srityje pasirinkite **Nauja**.  Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.
    1. Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą. 
    1. Nustatykite **Rankinis naujinimas** kaip **Taip**.
    1. Lauke **Vieta** įveskite „Grąžintos“.
    1. Veiksmų srityje pasirinkite **Įrašyti**.
    
Toliau pateiktame paveiksle parodytas San Francisko sandėlio atsargų vietos nustatymas.

![Atsargų vietos nustatymo pavyzdys](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Sandėlio sąrankos užbaigimas

Norėdami užbaigti sandėlio sąranką, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.
1. Pasirinkite sandėlį, kurį sukūrėte anksčiau.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Dalyje **Atsargų ir sandėlio valdymas**:
    1. Nustatykite **Numatytoji gavimo vieta** į anksčiau sukurtą numatytąją vietą.
    1. Pasirinkite **Numatytoji išdavimo vieta** į anksčiau sukurtą numatytąją vietą.
1. Skyriuje **Adresai** įveskite sandėlio adresą.
1. Skyriuje **Mažmeninė prekyba**: 
    1. Lauke **Numatytoji grąžinimo vieta** įveskite anksčiau sukurtą grąžinimo vietą.
    1. Nustatykite **Saugoti** kaip **Taip**.
    1. Nustatykite **Svoris** į **1,00**. 
    1. Lauke **Saugojimo matmenys** įveskite anksčiau sukurtą numatytąją vietą.
1. Skyriuje **Sandėlis** nustatykite **Faktinės neigiamos atsargos** kaip **Taip**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde rodoma išsami informacija apie sukonfigūruotą sandėlį.

![Sukonfigūruoto sandėlio pavyzdys](media/warehouse-sample.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sandėlio valdymo apžvalga](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)
    
[Interneto kanalo nustatymas](channel-setup-online.md)

[Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)





