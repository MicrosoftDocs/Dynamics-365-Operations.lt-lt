---
title: Abonementinio mokesčio dienų sumažinimas
description: Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd76e30b14d0fd21617e0ab7d892ba5ea3e89f2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217315"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Abonementinio mokesčio dienų sumažinimas 

[!include [banner](../includes/banner.md)]


Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Abonementinio mokesčio dienų sumažinimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo abonementai** \> **Visi aptarnavimo abonementai**. Pasirinkite aptarnavimo abonementas ir veiksmų srityje spustelėkite **Abonementiniai mokesčiai**

2.  Lauke **Abonemento tipas** pasirinkite **Mažinimo dienos**.

3.  Laukuose **Pradžios data** ir **Pabaigos data** nustatykite abonementinio mokesčio dienų intervalą, kurį norite pašalinti iš abonementinio mokesčio laikotarpio, ir spustelėkite **Gerai**.

Norėdami peržiūrėti sukurtą operaciją, formoje **Abonementas** spustelėkite **Mokesčių operacijos**.

## <a name="example"></a>Pavyzdys

Jei abonementinės operacijos laikotarpis trunka nuo sausio 1 d iki sausio 31 d., o jūs norite sumažinti šį laikotarpį 10 dienų, sukurkite naują operaciją, kurioje sumažinimo laikotarpis bus nuo sausio 1 d. iki sausio 10 d. (Sumažinimo laikotarpis taip pat gali būti nuo sausio 5 d. iki sausio 15 d. arba bet kuris kitas dešimties dienų laikotarpis).

Be to, jei **Pradžios data** sumažinimo laikotarpyje yra sausio 21 d. (31 minus 10), kaip **Pabaigos datą** galite nustatyti bet kurią datą po sausio 31 d. ir vis tiek iš mokesčio operacijos laikotarpio bus pašalintos 10 dienų.

## <a name="see-also"></a>Taip pat žiūrėkite

[Mažinimo dienų pavyzdys](reduction-days-example.md)

  


