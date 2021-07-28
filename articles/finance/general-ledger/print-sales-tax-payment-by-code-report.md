---
title: Spausdinti PVM mokėjimo pagal kodą ataskaitą
description: Šioje temoje pateikiama informacija apie parametrus ir veiksmus, kurių reikia norint išspausdinti PVM mokėjimo pagal kodą ataskaitą, pateikiamą apskaitos arba PVM kodo valiuta.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dad1cad6dcda1c7768f9be8bd7bd4426be7fbcbb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358862"
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

    ![Dialogo langas PVM mokėjimas pagal kodą.](media/Sales-tax-payment-by-code.png)

Toliau pateikiamoje iliustracijoje rodomas pavyzdys, kaip generuojama ataskaita. Ataskaita nurodo, kad ataskaitos kodas **101** pateiktas **EUR** valiuta, jei laukas **PVM valiuta** nustatytas į **EUR** PVM kodui, kuriam priskirtas ataskaitos kodas.

![PVM mokėjimo pagal kodą ataskaitos pavyzdys.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]