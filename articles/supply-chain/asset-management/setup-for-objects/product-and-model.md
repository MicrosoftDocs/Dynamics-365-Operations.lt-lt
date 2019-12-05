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
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812173"
---
# <a name="asset-manufacturers-and-models"></a>Turto gamintojai ir modeliai

[!include [banner](../../includes/banner.md)]

 

Šioje temoje aprašoma, kaip nustatyti turto gamintojus ir susietus modelius modulyje „Turto valdymas“. Modeliai gali būti susieti su turto tipais.

## <a name="set-up-product-model-relations"></a>Nustatyti produktų ryšius

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turtas** \> **Gamintojas ir modelis**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują produktą.
3. Lauke **Gamintojas** įveskite turto gamintojo pavadinimą.
4. Lauke **Aprašymas** įveskite aprašą.
5. „FastTab“ skirtuke **Modeliai** pasirinkite **Įtraukti**, kad sukurtumėte turto modelį, kurį reikia susieti su turto gamintoju.
6. Lauke **Modelis** įveskite turto modelio pavadinimą.
7. Lauke **Aprašymas** įveskite aprašą.
8. Lauke **Turto tipas** pasirinkite turto tipą, su kuriuo turėtų būti susietas gamintojo modelis.

    > [!NOTE]
    > Taip pat galite nustatyti turto tipų, gamintojų ir modelių ryšius peržvalgoje **Turto tipai**. Daugiau informacijos žr. [Turto tipai](../setup-for-objects/object-types.md).

    „FastTab“ skirtuke **Išsami informacija** lauke **Modeliai** rodomas turto modelių, kurie yra nustatyti pasirinktam turto gamintojui, skaičius. Lauke **Turtas** rodomas turtų, naudojančių pasirinktą gamintoją, skaičius.
    
    Lauke **Turtas** rodomas objektų, naudojančių šio gamintojo modelį, skaičius.

> [!NOTE]
> Turto tipas negali turėti jokio turto gamintojo modelio ryšių, jis gali būti susietas su vieno turto gamintojo modeliu arba su keliais turto gamintojų modeliais. Jei turto tipas yra susijęs bent su vienu gamintojo modeliu, tik deriniai, nustatyti peržvalgoje **Gamintojo modelis**, gali būti pasirinkti tuose turto valdymo puslapiuose, kuriuose gali būti nustatytas turto tipo, gamintojo ir modelio derinys. Šiuos puslapius sudaro **Visas turtas**, **Turto aptarnavimo lygis**, **Numatytieji užduočių tipai** ir **Priežiūros biudžeto eilutės**. Jei tam tikri išteklių tipai nėra susieti su jokiu gamintojo modeliu, šiuose puslapiuose rodomi tik tie turto tipai ir gamintojo modeliai, kurie taip pat nėra susieti su turto tipais.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Objekto gamintojo ir modelio pasirinkimas

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**.
2. Stulpelyje **Turtas** pasirinkite turto saitą. Pasirodo puslapis **Detalės**.
3. Pasirinkite **Redaguoti**.
4. „FastTab“ skirtuko **Bendra** laukuose **Gamintojas** ir **Modelis** pasirinkite reikšmes.
