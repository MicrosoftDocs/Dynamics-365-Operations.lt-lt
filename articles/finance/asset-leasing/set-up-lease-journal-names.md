---
title: Nuomos žurnalo pavadinimų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti nuomos žurnalų pavadinimus. Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose įrašai, kilę iš turto nuomos, registruojami.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990922"
---
# <a name="set-up-lease-journal-names"></a>Nuomos žurnalo pavadinimų nustatymas

[!include [banner](../includes/banner.md)]

Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose turto nuomos operacijos registruojamos. Puslapio **Turto nuomos parametrai** laukuose **Pirminis pripažinimas** ir **Mėnesio žurnalo pavadinimas** bus rodomi tik tie žurnalų pavadinimai, kurie priskirti žurnalo tipui **Turto nuoma**. Lauke **SF žurnalo pavadinimas** galima priskirti tik žurnalo tipą **Tiekėjo SF įrašymas**.

Norėdami sukonfigūruoti nuomos žurnalų pavadinimus, atlikite šiuos veiksmus.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuko **Bendra** lauke **Pirminio pripažinimo žurnalo pavadinimas** pasirinkite žurnalą. Visi pradiniai pripažinimo žurnalo įrašai bus registruojami į šį žurnalo pavadinimą.
3. Lauke **SF žurnalo pavadinimas** pasirinkite žurnalą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Taip**, nuomos ir išlaidų apmokėjimo SF bus užregistruotos šiame žurnalo pavadinime.
4. Lauke **Nuomos žurnalo pavadinimas** pasirinkite žurnalą. Visi nusidėvėjimo, palūkanų ir trumpojo laikotarpio perklasifikavimo įrašai bus registruojami į šį žurnalo pavadinimą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Ne**, nuomos mokėjimo ir išlaidų apmokėjimo įrašai bus taip pat užregistruoti šiame žurnalo pavadinime.
