---
title: Išlaidų tipų nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti išlaidų tipus turto nuomoje.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1538826f140393eec59be9ff4df5242d5ced9d8f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249754"
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