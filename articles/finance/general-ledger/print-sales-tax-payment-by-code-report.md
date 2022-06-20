---
title: PVM mokėjimo pagal kodą ataskaitos spausdinimas
description: Šiame straipsnyje pateikiama informacija apie parametrus ir veiksmus, reikalingus norint spausdinti PVM mokėjimą pagal kodo ataskaitą apskaitos arba mokesčių kodo valiuta.
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
ms.openlocfilehash: 9c6b51da41f2aaa3206f8ad97a364a9cd5ca6d49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856660"
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