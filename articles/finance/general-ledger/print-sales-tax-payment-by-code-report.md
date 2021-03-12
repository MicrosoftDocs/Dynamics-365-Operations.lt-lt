---
title: Spausdinti PVM mokėjimo pagal kodą ataskaitą
description: Šioje temoje pateikiama informacija apie parametrus ir veiksmus, kurių reikia norint išspausdinti PVM mokėjimo pagal kodą ataskaitą, pateikiamą apskaitos arba PVM kodo valiuta.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dd490663e66d1eda0eb0ea052e5b54fb867f81df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990305"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Spausdinti PVM mokėjimo pagal kodą ataskaitą 

[!include [banner](../includes/banner.md)]

Norėdami spausdinti **PVM mokėjimo pagal kodą** ataskaitą, eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **PVM ataskaitos** \> **PVM mokėjimas pagal kodą**. Pagal numatytuosius nustatymus ataskaitos sumos generuojamos juridinio subjekto apskaitos valiuta visiems ataskaitų kodams, kurie nustatyti puslapyje **PVM ataskaitų kodai**.

Taip pat galite generuoti šią ataskaitą taip, kad joje nurodyta PVM kodų valiuta būtų rodomos visų ataskaitų kodų, priskirtų PVM kodams puslapyje **PVM kodai**, PVM mokėjimų sumos.

## <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Darbo srityje **Funkcijų valdymas** įjunkite šią funkciją: **Generuoti PVM mokėjimo pagal kodą ataskaitą, pateikiamą PVM kodo valiuta**.

## <a name="run-the-report"></a>Paleiskite ataskaitą

1. Eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **PVM ataskaitos** \> **PVM mokėjimas pagal kodą**.
2. Lauke **Ataskaitos valiuta** pasirinkite vieną iš toliau pateiktų reikšmių.

    - **Apskaitos valiuta** – spausdinti ataskaitos sumas apskaitos valiuta.
    - **PVM kodo valiuta** – spausdinti ataskaitos sumas PVM kodų valiuta.

    ![Dialogo langas PVM mokėjimas pagal kodą](media/Sales-tax-payment-by-code.png)

Toliau pateikiamoje iliustracijoje rodomas pavyzdys, kaip generuojama ataskaita. Ataskaita nurodo, kad ataskaitos kodas **101** pateiktas **EUR** valiuta, jei laukas **PVM valiuta** nustatytas į **EUR** PVM kodui, kuriam priskirtas ataskaitos kodas.

![PVM mokėjimo pagal kodą ataskaitos pavyzdys](media/Sales-tax-payment-by-code-2.png)
