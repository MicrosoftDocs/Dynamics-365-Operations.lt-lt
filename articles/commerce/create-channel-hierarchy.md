---
title: Kanalo naršymo hierarchijos kūrimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e43c4c00545dfecb2f9a2192f81cd25300e3d6e6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352475"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Kanalų naršymo hierarchijos kūrimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti kanalo naršymo hierarchiją.

## <a name="overview"></a>Peržiūra

Kanalo naršymo hierarchija naudojama, norint grupuoti ir skirstyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba elektroniniame kasos aparate (EKA).

## <a name="create-a-channel-navigation-hierarchy"></a>Kanalo naršymo hierarchijos kūrimas

Norėdami sukurti kanalo naršymo hierarchiją, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Kanalo naršymo kategorijos**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Langelyje **Pavadinimas** įveskite pavadinimą.
1. Langelyje **Aprašas** įveskite aprašą.
1. Pasirinkite **Kurti**.
1. Veiksmų srityje pasirinkę **Naujas kategorijos mazgas**, sukurkite šakninį mazgą.
1. Langelyje **Pavadinimas** įveskite pavadinimą.
1. Langelyje **Aprašas** įveskite aprašą.
1. Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas šakninio mazgo pavyzdys.

![Šakninio mazgo pavyzdys.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Naršymo kategorijos mazgų kūrimas

Norėdami sukurti papildomų naršymo kategorijos mazgų, nurodančių kanalo produktų kategorijas, atlikite tolesnius veiksmus.

1. Naršymo srityje pasirinkite pirminį mazgą, į kurį norite įtraukti kategoriją.
1. Veiksmų srityje pasirinkite **Naujas kategorijos mazgas**.
1. Langelyje **Pavadinimas** įveskite pavadinimą.
1. Langelyje **Aprašas** įveskite aprašą.
1. Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.
1. Langelyje **Rodymo tvarka** įveskite rodymo tvarką (nebūtina).
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas baigtos kanalo naršymo hierarchijos pavyzdys.

![Kanalo hierarchijos pavyzdys.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Produktų įtraukimas į kategorijų mazgus

Norėdami įtraukti produktus į kategorijų mazgus, atlikite tolesnius veiksmus.

1. Pasirinkite kategorijos mazgą.
1. Srityje **Produktai** pasirinkite **Įtraukti**.
1. Raskite naują (-ų) produktą (-ų), kurį (-iuos) norite įtraukti pagal produkto numerį arba produkto pavadinimą, ir pasirinkite **Gerai**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

> [!NOTE]
> Įtraukti produktus į mazgą kanalo naršymo hierarchijoje nepakanka, kad produktai būtų rodomi pasirinktame kanale, produktus taip pat reikia pateikti pagal produktą. Daugiau informacijos apie asortimentus ieškokite [asortimento](assortments.md) valdymas.

Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktais produktais.

![Produktai, įtraukti į kategorijos mazgą.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Produktų atributų grupių įtraukimas į kategorijų mazgus

> [!NOTE]
> Atributų grupes būtina sukurti prieš jas įtraukiant į mazgą kanalo naršymo hierarchijoje.

Norėdami įtraukti produkto atributo grupę į kategorijos mazgą, atlikite tolesnius veiksmus.

1. Pasirinkite kategorijos mazgą.
1. Dalyje **Produkto atributo grupė** pasirinkite **Įtraukti**.
1. Suraskite įtrauktiną (-as) atributo (-ų) grupę (-es) ir pasirinkite **Gerai**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas mazgo pavyzdys su įtrauktomis produktų atributų grupėmis.

![Produktų atributų grupės mazge.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Asortimentų nustatymas](set-up-assortments.md)

[Atributų ir atributų grupių tvarkymas](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
