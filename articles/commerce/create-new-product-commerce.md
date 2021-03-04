---
title: Naujo produkto kūrimas „Commerce“ aplinkoje
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produktą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414305"
---
# <a name="create-a-new-product-in-commerce"></a>Naujo produkto kūrimas „Commerce“ aplinkoje


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produktą.

## <a name="overview"></a>Peržiūrėti

Produktą pirmiausia apibrėžia produkto numeris, pavadinimas ir aprašas. Tačiau, norint apibūdinti produktą ar paslaugą, taip pat būtini kiti duomenys:

## <a name="create-a-new-product"></a>Naujo produkto kūrimas

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Produktai pagal kategoriją**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Išplečiamajame sąraše **Produkto tipas** pasirinkite **Prekė** arba **Paslauga**.
1. Išplečiamajame sąraše **Produkto potipis** pasirinkite **Produktas** (jei nebus produkto variantų) arba **Bendrasis produktas** (jei bus produkto variantų).
1. Langelyje **Produkto numeris** įveskite produkto numerį, jei jis nėra iš anksto užpildytas.
1. Langelyje **Produkto pavadinimas** įveskite produkto pavadinimą.
1. Langelyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.
1. Išplečiamajame sąraše **Mažmeninės prekybos kategorija** pasirinkite reikiamą kategoriją.
1. Jei produktas yra rinkinys, pasirinkite **Taip** parinktyje **Produktų rinkinys**.
1. Jei produkto potipis yra bendrasis produktas, parinktyje **Produkto dimensijų grupė** nustatykite, kad būtų įtraukti palaikomi variantai. Tarp parinkčių yra **Spalva**, **Dydis**, **Stilius** ir **Konfigūracija**. Jei reikia, gali reikėti sukurti papildomų produktų dimensijų grupių.
1. Išplečiamajame sąraše **Konfigūracijos technologija** pasirinkite reikiamą parinktį.
1. Pasirinkite **Gerai**.

Toliau pateiktame vaizde parodytas įtraukiamas produkto pavyzdys.

![Produkto kūrimas](media/create-new-product.png)

Įtraukus produktą, galima nustatyti jo papildomus duomenis, pvz., **Produkto aprašas**, **Variantų grupės**, **Dimensijų grupės**, **Produkto atributai** ir **Susiję produktai**.

Toliau pateiktame vaizde parodyta papildoma produkto informacija.

![Produkto informacija](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Kurti produkto variantus

Jei produkto potipis yra **Bendrasis produktas**, reikės sukurti konkrečių variantų. 

Norėdami sukurti produkto variantų, atlikite tolesnius veiksmus.

1. Veiksmų srityje pasirinkite **Produkto variantai**.
1. Jei variantų grupės pasirinktos veiksmų srityje, pasirinkite **Variantų pasiūlymai*.
1. Pasirinkite palaikytinus produkto variantus.
1. Pasirinkite **Kurti**.

## <a name="release-a-product"></a>Produkto išleidimas

Norint parduoti produktą, jis pirmiausia turi būti pateiktas juridiniam subjektui.

1. Produkto puslapyje pasirinkite **Išleisti produktus**.

    ![Produkto išleidimas](media/create-new-product-3.png)

1. Pasirinkite išleistiną produktą, tada pasirinkite **Toliau**.

    ![Išleistino produkto pasirinkimas](media/create-new-product-4.png)

1. Pasirinkite išleistinų produkto variantų rinkinį, tada pasirinkite **Toliau**.

    ![Išleistinų variantų pasirinkimas](media/create-new-product-5.png)

1. Pasirinkite juridinį subjektą ir pasirinkite **Toliau**.

    ![Pasirinkite juridinį subjektą](media/create-new-product-6.png)

1. Pasirinkite **Baigti**.

    ![Produkto išleidimo užbaigimas](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Išleisto produkto konfigūravimas

Išleidus produktą, reikės jį papildomai konfigūruoti, įskaitant produkto kainos nustatymą.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Išleisti produktai pagal kategoriją**.
1. Pasirinkite išleisto produkto kategorijos mazgą ir produktų sąraše pasirinkite produktą.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Skyriuje **Pirkimas** sukonfigūruokite visas būtinas ypatybes, įskaitant **Vienetas**, **Kaina** ir **Kiekis**.
1. Norėdami užtikrinti, kad nėra klaidos pranešimų apie trūkstamus laukus, veiksmų srityje pasirinkite **Tikrinti**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas išleisto produkto konfigūracijos pavyzdys.

![Išleisto produkto konfigūravimas](media/create-new-product-8.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Juridinių subjektų kūrimas](channels-legal-entities.md)

[Variantų grupės kūrimas](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]