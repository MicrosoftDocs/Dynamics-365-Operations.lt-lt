---
title: Išlaidų tipų nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti išlaidų tipus turto nuomoje.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880989"
---
# <a name="set-up-expense-types"></a>Išlaidų tipų nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinta, kaip nustatyti išlaidų tipus turto nuomoje. Išlaidos, kurios neatstovaujamos pagal mokėjimus, yra žinomos kaip *išlaidų sąnaudos*. Šios išlaidos apima turto mokesčius, bendrąsias zonos priežiūros išlaidas ir draudimo išlaidas.

## <a name="add-an-administrative-expense-type"></a>Įtraukti administravimo išlaidų tipą

1. Eikite į **Turto nuoma \> Sąranka \> Išlaidų tipai**.
2. Pasirinkite **Naujas**.
3. Atitinkamuose laukuose įveskite naują išlaidų tipą ir aprašymą.

## <a name="assign-accounts-to-administrative-costs"></a>Sąskaitų priskyrimas administracinėms išlaidoms

Tada turėtumėte susieti abonementą su išlaidų tipais. Šios sąskaitos bus debetuojamos, užregistravus išlaidų grafiko įrašus. Korespondentinė sąskaita nurodyta kiekvienos nuomos **Eksploatavimo išlaidų mokėjimo grafiko** eilutėse.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuko **Sąskaitos** „FastTab“ **Eksploatavimo išlaidos** lauke **Išlaidų tipas** pasirinkite išlaidų tipą.
3. Pasirinkite **Įtraukti**.
4. Lauke **Knygos tipas** pasirinkite knygos tipą, kurį norite susieti su administravimo išlaidomis.

    > [!NOTE]
    > Keli knygos tipai gali būti siejami su ta pačia išlaidų sąskaita.

5. Lauke **Sąskaitos kodas** nurodykite, kuri nuomos knyga turi būti taikoma.

    - **Visos** – knyga taikoma visoms nuomoms.
    - **Grupė** – knyga taikoma konkrečiai nuomų grupei.
    - **Lentelė** – knyga taikoma konkrečioms nuomoms.

6. Jei parinktis **Grupė** arba **Lentelė** pasirinkote lauke **Sąskaitos kodas**, lauke **Sąskaitos / grupės numeris** pasirinkite sąskaitos numerį arba grupės numerį.
7. Atitinkamuose laukuose pasirinkite finansinės nuomos pagrindinės sąskaita ir pagrindinės veiklos nuomos abonementą.

Atlikę šiuos veiksmus, galite pridėti išlaidų per **Eksploatavimo išlaidų mokėjimo grafiko** eilutes pasirinktos nuomos puslapyje **Nuomos informacija**. Taip pat galite pridėti išlaidų kurdami naujas nuomos sutartis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
