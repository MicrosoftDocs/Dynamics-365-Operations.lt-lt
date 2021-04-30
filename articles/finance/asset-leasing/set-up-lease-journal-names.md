---
title: Nuomos žurnalo pavadinimų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti nuomos žurnalų pavadinimus. Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose įrašai, kilę iš turto nuomos, registruojami.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880891"
---
# <a name="set-up-lease-journal-names"></a>Nuomos žurnalo pavadinimų nustatymas

[!include [banner](../includes/banner.md)]

Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose turto nuomos operacijos registruojamos. Puslapio **Turto nuomos parametrai** laukuose **Pirminis pripažinimas** ir **Mėnesio žurnalo pavadinimas** bus rodomi tik tie žurnalų pavadinimai, kurie priskirti žurnalo tipui **Turto nuoma**. Lauke **SF žurnalo pavadinimas** galima priskirti tik žurnalo tipą **Tiekėjo SF įrašymas**.

Norėdami sukonfigūruoti nuomos žurnalų pavadinimus, atlikite šiuos veiksmus.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuko **Bendra** lauke **Pirminio pripažinimo žurnalo pavadinimas** pasirinkite žurnalą. Visi pradiniai pripažinimo žurnalo įrašai bus registruojami į šį žurnalo pavadinimą.
3. Lauke **SF žurnalo pavadinimas** pasirinkite žurnalą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Taip**, nuomos ir išlaidų apmokėjimo SF bus užregistruotos šiame žurnalo pavadinime.
4. Lauke **Nuomos žurnalo pavadinimas** pasirinkite žurnalą. Visi nusidėvėjimo, palūkanų ir trumpojo laikotarpio perklasifikavimo įrašai bus registruojami į šį žurnalo pavadinimą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Ne**, nuomos mokėjimo ir išlaidų apmokėjimo įrašai bus taip pat užregistruoti šiame žurnalo pavadinime.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
