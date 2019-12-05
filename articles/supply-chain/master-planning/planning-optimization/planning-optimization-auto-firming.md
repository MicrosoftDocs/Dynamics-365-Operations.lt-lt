---
title: Automatinis patvirtinimas naudojant „Planning Optimization“
description: Šioje temoje paaiškinama, kaip naudoti automatinį patvirtinimą naudojant „Planning Optimization“.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783158"
---
# <a name="auto-firming-with-planning-optimization"></a>Automatinis patvirtinimas naudojant „Planning Optimization“

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį. Kai patvirtinami suplanuoti užsakymai, jie paverčiami faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais. Naudojant „Planning Optimization“, suplanuoti užsakymai patvirtinami bendrojo planavimo metu, kai užsakymo data (t. y. pradžios data) yra patvirtinimo laiko riboje.

> [!NOTE]
> Automatinis suplanuoto pirkimo užsakymo patvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.

## <a name="turn-on-auto-firming"></a>Automatinio patvirtinimo įjungimas

Norėdami įjungti automatinį patvirtinimą, atlikite toliau pateikiamus veiksmus.

1. Darbo srityje **Funkcijos valdymas** skirtuke **Naujas** iš sąrašo pasirinkite **„Planning Optimization“ automatinis patvirtinimas**. Jei funkcija neatsiranda skirtuke **Naujas**, žiūrėkite skirtukus **Neįjungta** ir **Visi**.
1. Pasirinkite **Įjungti dabar**. Arba pasirinkite **Grafikas**ir pasirinkite laiką, kada norite, kad funkcija būtų įjungta.

## <a name="set-up-the-firming-time-fence"></a>Patvirtinimo laiko ribos nustatymas

Patvirtinimo laiko ribos skaičiuojamos į priekį nuo pagrindinio planavimo vykdymo datos. Ji nustatoma pagal įvestą dienų skaičių. Galite valdyti patvirtinimo laiko ribą toliau nurodytais būdais.

- Norėdami nustatyti numatytąją patvirtinimo laiko ribą padengimo grupei, eikite į **Pagrindinis planavimas** \> **Sąranka** \> **Padengimas** \> **Padengimo grupės** ir pasirinkite padengimo grupę. Tada „FastTab“ **Kita** lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Norėdami perrašyti patvirtinimo laiko ribą, kuri nustatyta padengimo grupei dėl konkrečios prekės, eikite į **Produkto informacijos valdymas** \> **Išleisti produktai**, tada veiksmų skyde pasirinkite **Planas** ir pasirinkite **Prekės padengimas**. Tada skirtuke **Bendroji informacija** pasirinkite **Perrašyti laiko ribą** ir lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Jei norite perrašyti patvirtinimo laiko ribą, nustatytą padengimo grupei ir konkretaus bendrojo plano prekės padengimui, eikite į **Bendrasis planavimas** \> **Sąranka** \> **Bendrieji planai** ir pasirinkite bendrąjį planą. Tada „FastTab“ **Laiko riba dienomis** nustatykite **Fiksuoti** kaip **Taip** ir įveskite dienų skaičių.

Jei automatinis patvirtinimas yra įjungtas bendrojo planavimo vykdymui, kuris naudoja „Planning Optimizatio“, automatinio patvirtinimo procesas atliekamas pagal automatinio patvirtinimo sąranką. Jei automatinis patvirtinimas neįjungtas arba jei planavimas pradedamas puslapyje **Grynieji poreikiai**, automatinio patvirtinimo procesas yra praleidžiamas.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>„Planning Optimization“ ir įdiegtas „Supply Chain Management“ planavimo mechanizmas

Tiek „Planning Optimization“, tiek planavimo mechanizmą, kuris įdiegtas „Microsoft Dynamics 365 Supply Chain Management“, galima naudoti norint automatiškai patvirtinti planavimo užsakymus. Tačiau yra keletas svarbių skirtumų. Pavyzdžiui, jei „Planning Optimization“ naudoja užsakymo datą (tai yra, pradžios datą), kad nustatytų, kuriuos suplanuotus užsakymus patvirtinti, įdiegtas „Supply Chain Management“ mechanizmas naudoja poreikio datą (tai yra, pabaigos datą). Toliau pateikiama skirtumų santrauka.

**Planavimo optimizavimas**

- Automatinis patvirtinimas pagrįstas užsakymo data (pradžios data).
- Kadangi užsakymo data (pradžios data) suaktyvina patvirtinimą, nebūtina atsižvelgti į gamybos laiką kaip patvirtinimo laiko ribos dalį.
- Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti viena savaitė.

**Įdiegtas „Supply Chain Management“ planavimo mechanizmas“**

- Automatinis patvirtinimas pagrįstas poreikio data (pabaigos data).
- Siekiant užtikrinti, kad užsakymai būtų patvirtinti laiku, patvirtinimo laiko riba turi būti ilgesnė už gamybos laiką.
- Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti gamybos laikas ir viena savaitė.
