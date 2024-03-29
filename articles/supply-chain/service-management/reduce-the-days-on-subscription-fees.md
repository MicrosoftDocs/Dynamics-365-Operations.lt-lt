---
title: Abonementinio mokesčio dienų sumažinimas
description: Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014828"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Abonementinio mokesčio dienų sumažinimas 

[!include [banner](../includes/banner.md)]


Norėdami sumažinti esamo abonementinio mokesčio dienų skaičių, galite sukurti naują operaciją, į kurią perkelsite laikotarpį, kuris turi nebebūti abonementinio mokesčio intervalo dalimi.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Abonementinio mokesčio dienų sumažinimas

1.  Spustelėkite **Aptarnavimo valdymo** \> **abonementai** \> **Visi aptarnavimo abonementai**. Pasirinkite aptarnavimo abonementas ir veiksmų srityje spustelėkite **Abonementiniai mokesčiai**

2.  Lauke **Abonemento tipas** pasirinkite **Mažinimo dienos**.

3.  Laukuose **Pradžios data** ir **Pabaigos data** nustatykite abonementinio mokesčio dienų intervalą, kurį norite pašalinti iš abonementinio mokesčio laikotarpio, ir spustelėkite **Gerai**.

Norėdami peržiūrėti sukurtą operaciją, formoje **Abonementas** spustelėkite **Mokesčių operacijos**.

## <a name="example"></a>Pavyzdys

Jei abonementinės operacijos laikotarpis trunka nuo sausio 1 d iki sausio 31 d., o jūs norite sumažinti šį laikotarpį 10 dienų, sukurkite naują operaciją, kurioje sumažinimo laikotarpis bus nuo sausio 1 d. iki sausio 10 d. (Sumažinimo laikotarpis taip pat gali būti nuo sausio 5 d. iki sausio 15 d. arba bet kuris kitas dešimties dienų laikotarpis).

Be to, jei **Pradžios data** sumažinimo laikotarpyje yra sausio 21 d. (31 minus 10), kaip **Pabaigos datą** galite nustatyti bet kurią datą po sausio 31 d. ir vis tiek iš mokesčio operacijos laikotarpio bus pašalintos 10 dienų.

## <a name="see-also"></a>Taip pat žiūrėkite

[Mažinimo dienų pavyzdys](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]