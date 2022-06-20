---
title: Automatinis vidinės įmonės mokėjimų SF kliento SF registravimas
description: Šiame straipsnyje paaiškinama, kaip automatiškai registruoti vidinės įmonės kliento SF mokėjimus
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878793"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Automatinis vidinės įmonės mokėjimų SF kliento SF registravimas

[!include [banner](../../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ sukuria kliento operaciją, kai užregistruojama vidinės įmonės kliento užsakymo SF. Ši kliento operacija lieka atvira iki sudengiama, tai reiškia, kad ji apmokėta. Atnaujinus atitinkamo vidinės įmonės pirkimo užsakymo SF, sukuriama tiekėjo operacija, atitinkanti kliento operaciją. Ši tiekėjo operacija taip pat lieka atvira iki sudengimo. Kad būtų išvengta skirtumų, galima automatiškai sukurti ir užregistruoti gautinų sumų mokėjimo žurnalą, kai bus užregistruotas mokėtinų sumų mokėjimo žurnalas.

1. Eikite į **Pardavimas ir rinkodara \> Klientai \> Visi klientai**.
1. Veiksmų srities skirtuke **Bendra** pasirinkite **Vidinė įmonė**.
1. Norėdami nustatyti vidinės įmonės gautinų sumų mokėjimus pardavimo užsakymų vidinės įmonės **puslapyje**, pasirinkite **pardavimo užsakymo strategijų** saitą.
1. Lauke **Mokėjimų žurnalas** pasirinkite gautinų sumų mokėjimo žurnalą, kuriame norite registruoti vidinės įmonės tiekėjo mokėjimus. Komandą galite nustatyti **Gautinų sumų parametrų** puslapyyje.
1. Jei norite automatiškai registruoti šiame žurnale, pažymėkite žymės langelį **Publikuoti žurnalą automatiškai**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
