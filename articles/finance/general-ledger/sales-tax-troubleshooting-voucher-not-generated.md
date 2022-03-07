---
title: Kvitas nesugeneruojamas
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai kvitas turėtų būti generuojamas, bet jo nėra.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947682"
---
# <a name="voucher-isnt-generated"></a>Kvitas nesugeneruojamas

[!include [banner](../includes/banner.md)]

Jei kvitas turi būti sugeneruotas, bet kvito operacijų puslapyje nerodyti kvitų, norėdami pašalinti šią problemą, atlikite toliau nurodytus veiksmus, nurodytus **skyriuose**.

[![Kvito operacijų puslapis, kuriame nėra kvitų](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Patikrinti mokesčio taikomumą

1. Pereikite į **periodinių** \>**mokesčių užduočių** \> **papildomos knygos žurnalo įrašus, kurie dar nepervesti**.
2. Jei yra žurnalo įrašas, pasirinkite jį, tada pasirinkite **Perkelti** dabar.

    [![Perkelti dabar mygtuką papildomos knygos žurnalo įrašuose, kurie dar neperduoti puslapyje](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Dar kartą **atidarykite** kvito operacijų puslapį, kad pamatytumėte, ar kvitas buvo sugeneruotas.

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas

Jei atlikote veiksmus ankstesniame skyriuje, bet neradote problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
