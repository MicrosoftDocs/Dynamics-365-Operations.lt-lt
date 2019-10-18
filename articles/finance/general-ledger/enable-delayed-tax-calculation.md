---
title: Įjungti uždelstą mokesčių skaičiavimą žurnale
description: Šioje temoje paaiškinama, kaip naudoti funkciją **Įjungti uždelstą mokesčių skaičiavimą žurnale** siekiant pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178993"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Įjungti uždelstą mokesčių skaičiavimą žurnale
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip naudoti funkciją **Įjungti uždelstą mokesčių skaičiavimą žurnale** siekiant pagerinti mokesčių skaičiavimo efektyvumą, kai yra daug žurnalo eilučių.

PVM skaičiavimo funkcija žurnale realiuoju laiku suaktyvinama, kai vartotojas atnaujina su mokesčiais susijusius laukus, pvz., PVM grupę / prekės PVM grupę. Atnaujinus bet kurią žurnalo eilutę, iš naujo apskaičiuojama visų žurnalo eilučių mokesčių suma. Tai padeda vartotojui matyti apskaičiuotą mokesčių sumą realiu laiku, bet taip pat gali kelti našumo problemų, jei žurnalo eilučių yra daug.

Ši funkcija suteikia galimybę atidėti mokesčių skaičiavimą siekiant išspręsti našumo problemą. Jei ši funkcija įjungta, mokesčių suma bus apskaičiuota tik tada, kai vartotojas spustels komandą „PVM“ komandą arba užregistruos žurnalą.

Vartotojas gali įjungti / išjungti parametrą trimis lygiais:
- Pagal juridinį subjektą
- Pagal žurnalo pavadinimą
- Pagal žurnalo antraštę

Sistema kaip galutinę naudos žurnalo antraštėje esančią parametro reikšmę. Parametro reikšmė žurnalo antraštėje bus gauta iš žurnalo pavadinimo. Parametro reikšmė žurnalo pavadinime bus gauta iš didžiosios knygos parametro sukuriant žurnalo pavadinimą.

Jei šis parametras yra įjungtas, žurnalo laukai „Faktinė PVM suma“ ir „Apskaičiuota PVM suma“ bus paslėpti. Taip daroma siekiant nesupainioti vartotojo, nes, prieš vartotojui suaktyvinant mokesčių skaičiavimą, rodoma šių dviejų laukų reikšmė visada bus 0.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Įjungti uždelstą mokesčių skaičiavimą pagal juridinį subjektą

1. Eikite į **Didžioji knyga > DK nustatymas > DK parametrai**
2. Spustelėkite kortelę **PVM**
3. Sparčiajame skirtuke **Bendra** suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Įjungti uždelstą mokesčių skaičiavimą pagal žurnalo pavadinimą

1. Eikite į **Didžioji knyga > Žurnalo nustatymas > Žurnalo pavadinimai**
2. Sparčiajame skirtuke **Bendra** suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Įjungti uždelstą mokesčių skaičiavimą pagal žurnalą

1. Eikite į **Didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**
2. Spustelėkite **Naujas**
3. Pasirinkite žurnalo pavadinimą
4. Spustelėkite **Sąranka**
5. Suraskite parametrą **Uždelstas mokesčių skaičiavimas** ir jį įjunkite arba išjunkite

![](media/delayed-tax-calculation-journal-header.png)
