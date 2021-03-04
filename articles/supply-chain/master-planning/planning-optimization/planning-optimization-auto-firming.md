---
title: Automatinis patvirtinimas su „Planning Optimization“
description: Šioje temoje paaiškinama, kaip naudoti automatinį patvirtinimą naudojant „Planning Optimization“.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 61e9e6aa660bc0828645c6bf1f2655539804831a
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594531"
---
# <a name="autofirming-with-planning-optimization"></a>Automatinis patvirtinimas su „Planning Optimization“

[!include [banner](../../includes/banner.md)]

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį. Kai patvirtinami suplanuoti užsakymai, jie paverčiami faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais. Naudojant „Planning Optimization“, suplanuoti užsakymai patvirtinami bendrojo planavimo metu, kai užsakymo data (t. y. pradžios data) yra patvirtinimo laiko riboje.

> [!NOTE]
> Automatinis suplanuoto pirkimo užsakymo patvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.

## <a name="turn-on-autofirming"></a>Įjunkite automatinį patvirtinimą

Norėdami įjungti automatinį patvirtinimą atlikite šiuos žingsnius.

1. Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **„Planning Optimization“ automatinis patvirtinimas**. Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.
1. Pasirinkite **Įjungti dabar**. Arba pasirinkite **Grafikas** ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.

## <a name="set-up-the-firming-time-fence"></a>Patvirtinimo laiko ribos nustatymas

Patvirtinimo laiko ribos skaičiuojamos į priekį nuo pagrindinio planavimo vykdymo datos. Ji nustatoma pagal įvestą dienų skaičių. Galite valdyti patvirtinimo laiko ribą toliau nurodytais būdais.

- Norėdami nustatyti numatytąją patvirtinimo laiko ribą padengimo grupei, eikite į **Pagrindinis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupės** ir pasirinkite padengimo grupę. Tada „FastTab“ **Kita** lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Norėdami perrašyti patvirtinimo laiko ribą, kuri nustatyta padengimo grupei dėl konkrečios prekės, eikite į **Produkto informacijos valdymas** \> **Išleisti produktai**, tada veiksmų skyde pasirinkite **Planas** ir pasirinkite **Prekės padengimas**. Tada skirtuke **Bendroji informacija** pasirinkite **Perrašyti laiko ribą** ir lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Jei norite perrašyti patvirtinimo laiko ribą, nustatytą padengimo grupei ir konkretaus bendrojo plano prekės padengimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Bendrieji planai** ir pasirinkite bendrąjį planą. Tada **Laiko tvoros dienomis** „FastTab“, nustatytas **Patvirtinimas** į **Taip** ir įveskite dienų skaičių.

Jei automatinis patvirtinimas yra įjungtas „Planning Optimization“ vykdymui, naudojančiam planavimo optimizavimą, automatinio patvirtinimo procesas atliekamas pagal jo nustatymus. Jei automatinis patvirtinimas yra įjungtas arba jei planavimas yra iš **Grynųjų reikalavimų** puslapio, automatinio patvirtinimo procesas praleidžiamas.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>„Planning Optimization“ ir įdiegtas „Supply Chain Management“ planavimo mechanizmas

„Planning Optimization“ ir planavimo variklis yra įdėti į „Microsoft Dynamics 365 Supply Chain Management“ ir gali būti naudojami automatiškai patvirtintiems suplanuotiems užsakymams. Tačiau yra keletas svarbių skirtumų. Pavyzdžiui, jei „Planning Optimization“ naudoja užsakymo datą (tai yra, pradžios datą), kad nustatytų, kuriuos suplanuotus užsakymus patvirtinti, įdiegtas „Supply Chain Management“ mechanizmas naudoja poreikio datą (tai yra, pabaigos datą). Toliau pateikiama skirtumų santrauka.

**Planavimo optimizavimas**

- Automatinis patvirtinimas yra pagrįstas užsakymo data (pradžios data).
- Kadangi užsakymo data (pradžios data) suaktyvina patvirtinimą, nebūtina atsižvelgti į gamybos laiką kaip patvirtinimo laiko ribos dalį.
- Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti viena savaitė.

**Įdiegtas „Supply Chain Management“ planavimo mechanizmas“**

- Automatinis patvirtinimas yra pagrįstas reikalavimo data (pabaigos data).
- Siekiant užtikrinti, kad užsakymai būtų patvirtinti laiku, patvirtinimo laiko riba turi būti ilgesnė už gamybos laiką.
- Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti gamybos laikas ir viena savaitė.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]