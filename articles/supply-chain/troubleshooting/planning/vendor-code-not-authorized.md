---
title: Tiekėjo kodas nėra įgaliotas konkrečiam produktui ir datai
description: Kai bandote patvirtinti suplanuotą užsakymą arba prie pirkimo užsakymo pridėti eilutę, gaunate klaidos pranešimą, kuriame teigiama, kad tiekėjo kodas nėra įgaliotas produktui ir datai.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294140"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Tiekėjo kodas nėra įgaliotas konkrečiam produktui ir datai

Klaidos kodas: SYP4881415

## <a name="symptoms"></a>Požymiai

Kai bandote patvirtinti suplanuotą užsakymą arba pridėti eilutę prie pirkimo užsakymo, gaunate tokį klaidos pranešimą:

> Tiekėjo kodo %1 negalima naudoti %2 ir %3.

## <a name="cause"></a>Priežastis

Ši klaida įvyksta, nes laukas **Patvirtinto tiekėjo patikros metodas** yra nustatytas į *Tik įspėjimas* arba *Neleidžiama* konkrečiam produktui, o tiekėjas šiuo metu nėra įgaliotas tiekti tą produktą.

## <a name="resolution"></a>Sprendimas

Norėdami išspręsti šią problemą, išjunkite atitinkamo produkto tiekėjo patikrą arba patvirtinkite tiekėją.

Norėdami išjungti produkto tiekėjo patikrą, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite atitinkamą produktą.
1. „FastTab” **Pirkimas** nustatykite lauko **Patvirtinto tiekėjo patikros metodas** reikšmę į kitokią nei *Tik įspėjimas* ar *Neleidžiama*.

Norėdami patvirtinti produkto tiekėją, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite atitinkamą prekę.
1. Veiksmų srities skirtuko **Pirkimas** grupėje **Patvirtintas tiekėjas** pasirinkite **Nustatymas**.
1. **Patvirtintų tiekėjų** sąrašo puslapyje į tinklelį įtraukite eilutę ir nustatykite šias jo vertes:

    - **Tiekėjas** – Pasirinkite tiekėją, kuris patvirtins dabartinį produktą.
    - **Įsigaliojimo data** – Pasirinkite pirmą datą kuriai patvirtintas tiekėjas.
    - **Galiojimo data** – Pasirinkite paskutinę datą kuriai patvirtintas tiekėjas.

Daugiau informacijos rasite [Konkrečių produktų tiekėjų tvirtinimas](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
