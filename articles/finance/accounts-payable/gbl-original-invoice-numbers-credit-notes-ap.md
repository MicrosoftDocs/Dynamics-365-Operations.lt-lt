---
title: Nuorodos į pradines SF kredito pažymose (tiekėjo sąskaitos)
description: Šioje temoje aprašoma, kaip sukurti nuorodą į pradinę SF, kai kuriate kredito pažymą.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 698a23a98f027014c89073203e6d9dfa5539a2f6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689191"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Nuorodos į pradines SF kredito pažymose (tiekėjo sąskaitos)

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti nuorodą į pradinę SF, kai kuriate kredito pažymą.

## <a name="prerequisites"></a>Būtinieji komponentai

Funkcijų valdymo **darbo srityje** įgalinkite funkciją **Įgalinti tiekėjo SF kredito SF** išrašymą. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Šioje temoje aprašyta funkcija taikoma verslo dokumentams.

**Mokėtinos sumos:**

- Pirkimo užsakymas
- SF žurnalas
- SF registras

**DK:**

- Pagrindinis žurnalas

## <a name="define-a-reference-to-an-original-invoice"></a>Nustatyti nuorodą į originalią sąskaitą

Naudokite tolesnes procedūras, kad nustatytumėte nuorodą į originalią sąskaitą konkrečiuose verslo dokumento tipuose.

### <a name="vendor-credit-note-purchase-order"></a>Tiekėjo kredito pažyma (pirkimo užsakymas)

1. Eikite į **Mokėtinos sumos** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**.
2. Kurti naują pirkimo užsakymą arba naudoti esamą, norint sukurti kredito pažymą.
3. Veiksmų juostoje **Sąskaitos** skirtuke, **Įžanga** grupėje, rinkitės **Kredito sąskaitos išrašymas**.
4. Įveskite priežastį siekiant taisyti ir rinkitės priežastį taisymui.

### <a name="vendor-credit-note-ledger-journals"></a>Tiekėjo kredito pažyma (DK žurnalai)

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Mokėtinos sumos** \> **Sąskaitų žurnalas**.
    - Eikite į **Mokėtinos sumos** \> **Sąskaitų registras**.
    - Eikite į **Didžioji knyga** \> **Žurnalo įrašai** \> **Bendrieji žurnalai**.

2. Žurnalo ir naujo žurnalo naujų žurnalų eilutės.
3. Veiksmų srityje pasirinkite **Funkcijos** \> **Kredito sąskaita**.
4. Įveskite priežastį siekiant taisyti ir rinkitės priežastį taisymui.

> [!NOTE]
> Kredito **SF išrašymo** komanda matoma bendrojo žurnalo kvite, jei laukas **Sąskaitos tipas** nustatytas kaip **Tiekėjas**.
