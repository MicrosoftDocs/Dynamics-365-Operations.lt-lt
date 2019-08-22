---
title: Turto gamintojai ir modeliai
description: Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
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
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783467"
---
# <a name="asset-manufacturers-and-models"></a>Turto gamintojai ir modeliai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“. Modeliai gali būti susieti su turto tipais.

## <a name="set-up-product-model-relations"></a>Nustatyti produktų ryšius

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Gamintojas ir modelis**.
2. Pasirinkite **New**, kad sukurtumėte naują produktą.
3. Lauke **Gamintojas** įveskite turto gamintojo pavadinimą.
4. Lauke **Description** įveskite aprašą.
5. „FastTab“ skirtuke **Modeliai** pasirinkite **Įtraukti**, kad sukurtumėte turto modelį, kurį reikia susieti su turto gamintoju.
6. Lauke **Modelis** įveskite turto modelio pavadinimą.
7. Lauke **Description** įveskite aprašą.
8. Lauke **Turto tipas** pasirinkite turto tipą, su kuriuo turėtų būti susietas gamintojo modelis.

    > [!NOTE]
    > Taip pat galite nustatyti turto tipų, gamintojų ir modelių ryšius peržvalgoje **Asset types**. Daugiau informacijos žr. [Kurti ilgalaikį turtą](../setup-for-objects/object-types.md).

    „FastTab“ skirtuke **Išsami informacija** lauke **Modeliai** rodomas turto modelių, kurie yra nustatyti pasirinktam turto gamintojui, skaičius. Lauke **Turtas** rodomas turtų, naudojančių pasirinktą gamintoją, skaičius.
    
    Lauke **Turtas** rodomas objektų, naudojančių šio gamintojo modelį, skaičius.

> [!NOTE]
> Turto tipas negali turėti jokio turto gamintojo modelio ryšių, jis gali būti susietas su vieno turto gamintojo modeliu arba su keliais turto gamintojų modeliais. Jei turto tipas yra susijęs bent su vienu gamintojo modeliu, tik deriniai, nustatyti peržvalgoje **Manufacturer model**, gali būti pasirinkti tuose turto valdymo puslapiuose, kuriuose gali būti nustatytas turto tipo, gamintojo ir modelio derinys. Šiuos puslapius sudaro **Visas turtas**, **Turto aptarnavimo lygis**, **Numatytieji užduočių tipai** ir **Priežiūros biudžeto eilutės**. Jei tam tikri išteklių tipai nėra susieti su jokiu gamintojo modeliu, šiuose puslapiuose rodomi tik tie turto tipai ir gamintojo modeliai, kurie taip pat nėra susieti su turto tipais.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Objekto gamintojo ir modelio pasirinkimas

1. Pasirinkite **Asset management** \> **Common** \> **Assets** \> **All assets**.
2. Stulpelyje **Turtas** pasirinkite turto saitą. Pasirodo puslapis **Details**.
3. Pasirinkite **Redaguoti**.
4. „FastTab“ skirtuko **Bendra** laukuose **Gamintojas** ir **Modelis** pasirinkite reikšmes.
