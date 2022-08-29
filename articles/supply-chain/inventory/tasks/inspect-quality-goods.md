---
title: Prekių kokybės tikrinimas
description: Šiame straipsnyje aprašoma, kaip apdoroti kokybės užsakymus.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219041"
---
# <a name="inspect-the-quality-of-goods"></a>Prekių kokybės tikrinimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip apdoroti kokybės užsakymus. Kokybės patikrinimus paprastai atlieka kokybės klerkas.

Jei įdiegti standartiniai [demonstraciniai](../../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys, galite naudoti juos šiame straipsnyje procedūroms atlikti. Norėdami naudoti demonstracinius duoemnis, pasirinkite *„USMF”* juridinį subjektą. Tada turite patvirtinti pirkimo užsakymą *000016* ir užregistruoti produkto gavimo kvitą. Kokybės užsakymas generuojamas automatiškai.

## <a name="step-1-select-a-quality-order"></a>1 veiksmas: Pasirinkti kokybės užsakymą

Norėdami pasirinkti kokybės užsakymą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Periodinės užduotys \> Kokybės valdymas \> Kokybės užsakymai**.
1. Pasirinkite kokybės užsakymą, sukurtą prieš jums pradedant šią procedūrą.

## <a name="step-2-record-test-results"></a>2 veiksmas: Įrašyti tikrinimo rezultatus

Norėdami įrašyti tikrinimo rezultatus, atlikite šiuos veiksmus.

1. Pasirinkite **Rezultatai**.
1. Pasirinkite **Redaguoti**.
1. Lauke **Rezultatų kiekis** įveskite skaičių.
1. Lauke **Išvados** pasirinkite norimą įrašą. Šiame pavyzdyje rezultatas priklauso nuo iš anksto nustatytos baigties. Paprastai įrašomas konkretesnis bandymo rezultatas, pavyzdžiui, dydis ar kitas matmuo.
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

## <a name="step-3-validate-the-quality-order"></a>3 veiksmas: Tikrinti kokybės užsakymą

Norėdami patvirtinti kokybės užsakymą, atlikite šiuos veiksmus.

1. Pasirinkite **Tikrinti**.
1. Lauke **Patvirtinta pagal** pasirinkite vartotoją, kuris atlieka patikrinimą.
1. Pasirinkite **Pasirinkti**.
1. Pasirinkite **Gerai**.
1. Uždarykite puslapį.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
