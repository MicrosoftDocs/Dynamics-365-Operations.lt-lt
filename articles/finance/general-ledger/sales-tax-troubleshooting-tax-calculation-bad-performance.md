---
title: Mokesčių skaičiavimo efektyvumas veikia operacijas
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, susijusi su mokesčių skaičiavimo našumui ir jo poveikis operacijoms.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3ee0e3a0f8d9c06760776719fbe49e684cb882cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894912"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Mokesčių skaičiavimo efektyvumas veikia operacijas

[!include [banner](../includes/banner.md)]

Kartais operacijai daro įtakos našumo problemos, kurias turi mokesčių skaičiavimas. Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.

## <a name="review-the-transaction-line-count"></a>Peržiūrėti perlaidos eilutės skaičiavimą

Nustatykite, ar operacijoje yra daug eilučių (pvz., daugiau nei keli šimtai). Jei nėra, pereisite į kitą skyrių. Jei operacijoje yra keli šimtai eilučių, atidėti mokesčių skaičiavimą. Daugiau informacijos rasite Įgalinti [atidėtų mokesčių skaičiavimą](enable-delayed-tax-calculation.md) žurnaluose. 

Po to galite nustatyti, ar įvykdyta kuri nors iš šių sąlygų:

- Yra importavimo operacijų iš didelių failų.
- Keli seansai vienu metu apdoros tą patį operacijos mokesčio skaičiavimą.
- Operacijoje yra kelios eilutės, o rodiniai atnaujinami tikru laiku. Pvz., laukas Apskaičiuota PVM suma, pateiktas bendrojo žurnalo puslapyje, yra atnaujinamas realiuoju laiku, **kai** pakeičiami eilutės **laukai**.

   [![Apskaičiuotas PVM sumos laukas Jounal kvito puslapyje.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Jei įvykdyta kuri nors iš šių sąlygų, atidėti mokesčių skaičiavimą.

## <a name="review-the-call-stack"></a>Peržiūrėti iškvietimų dėklą

Peržiūrėti iškvietimų dėklą ir nustatyti, ar mokesčių skaičiavimas iškviestas kelis kartus. Jei jo nėra, pereisite į kitą skyrių. Jei iškvietimų dėklas iškviestas kelis kartus, atlikite šiuos veiksmus ir taip sumažinsite mokesčių skaičiavimo laiką.

1. Jei į žurnalą atsižvelgta į operaciją, atidėti mokesčio skaičiavimą. Daugiau informacijos rasite Įgalinti [atidėtų mokesčių skaičiavimą](enable-delayed-tax-calculation.md) žurnaluose.
2. Jei operacija yra pirkimo užsakymas, o programos versija vėlesnė nei 10.0.15, galite atidėti mokesčių skaičiavimą iki galutinio skaičiavimo, įjungdami atėjimo **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.

## <a name="review-the-call-stack-timeline"></a>Peržiūrėti iškvietimų dėklo laiko juosta

Peržiūrėkite iškvietimų dėklo laiko juostą, kad nustatytumėte, ar yra tokių problemų. Jei taip ir yra, įjunkite **TaxUncommittedDoIsolateFreFlighting skrydžio funkciją,** kad išspręstumėte problemą.

- Dėl operacijos sistema nustoja reaguoti, kol seansas baigiasi. Todėl operacija negali apskaičiuoti mokesčio rezultato. Šioje iliustracijoje rodomas jūsų gauti pranešimų langas „Seansas baigtas".

    [![Pranešimas apie seansą.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- **TaxUncommitted metodai** užtruko daugiau laiko nei kiti metodai. Pavyzdžiui, pagal šį pavyzdį **TaxUncommitted ::updateTaxUncommitted() metodas trunka 43 347,42 sekundėmis, tačiau kiti metodai** užtrunka 0,09 sekundės.

    [![Metodo trukmė.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Mokesčių skaičiavimo tinkinimas ir iškviečiamas

Kai pritaikote, nekviesti mokesčių skaičiavimo **įterpimo()** ar **update()** metodo kiekvienai eilutei. Mokesčių skaičiavimas turi būti iškviestas operacijos lygiu.

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas

Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
