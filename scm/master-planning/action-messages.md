---
title: nedokumentuota
description: "Veiksmo pranešimas yra sistemos sugeneruotas pasiūlymas keisti esamą suplanuotą arba patvirtintą tvarką."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bfeca6506d2452bf7582bdd206f8c3ad3f2a4330
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="action-messages"></a>Veiksmų pranešimai

[!include[banner](../includes/banner.md)]


Veiksmo pranešimas yra sistemos sugeneruotas pasiūlymas keisti esamą suplanuotą arba patvirtintą tvarką.

## <a name="introduction"></a>Įžanga

Veiksmų pranešimai generuojami pakeitus reikalavimus, kai bendrojo planavimo metu atliekami skaičiavimai. Pvz., siuntimo data arba kiekis galėjo pakisti tame pardavimo užsakyme, kuriam jau sukūrėte pirkimo užsakymą, kad patenkintumėte poreikį. Šiuo atveju, atliekant bendrojo planavimo skaičiavimą, generuojamas vienas arba keli veiksmų pranešimai, kad būtų atnaujintas pirkimo užsakymas. Galite nuspręsti, ar atlikti siūlomus keitimus.

Galite nustatyti, kaip turi būti skaičiuojami padengimo grupės, kurią pridedate prie prekės, veiksmų pranešimai.

## <a name="select-action-messages"></a>Pasirinkite veiksmų pranešimus

**Padengimo grupių** puslapyje galite pasirinkti, kokius veiksmų pranešimus turi generuoti sistema ir kurioms padengimo grupėms ar prekėms pranešimai turi būti taikomi. Galite pasirinkti toliau nurodytus veiksmų pranešimus.

| Pranešimas             | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Išankstinis**         | Jei pasirinksite šį pranešimą, sistema prireikus generuos veiksmų pranešimus, kad užsakymus perkeltų į ankstesnę datą. **Paankstinimo maržos** lauke taip pat galite nurodyti maksimalų skaičių dienų tarp gavimo ir išdavimo be ankstinimo veiksmų. |
| **Atidėti**        | Jei pasirinksite šį pranešimą, sistema prireikus generuos veiksmų pranešimus, kad užsakymus perkeltų į vėlesnę datą. **Atidėjimo maržos** lauke galite nurodyti maksimalų skaičių dienų tarp gavimo ir išdavimo be atidėjimo veiksmų.       |
| **Mažinti**        | Jei pasirinksite šį pranešimą, gamybos užsakymai, pirkimo užsakymai ir kitos gavimo operacijos turėtų būti sumažintos, kad būtų išvengta perteklinių atsargų lygių.                                                                                                   |
| **Didinti**        | Jei pasirinksite šį pranešimą, gamybos užsakymai, pirkimo užsakymai ir kitos gavimo operacijos turėtų būti padidintos, kad būtų išvengta atsargų trūkumų.                                                                                                    |
| **Išvestiniai veiksmai** | Jei pasirenkate šį pranešimą, kuriami išvestinių reikalavimų veiksmų pranešimai, pvz., gamybos vykdymo komponentų užsakymų veiksmai.                                                                                                   |






