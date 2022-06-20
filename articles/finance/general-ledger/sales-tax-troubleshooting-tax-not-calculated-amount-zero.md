---
title: Mokestis nesuskaičiuotas arba mokesčio suma lygi nuliui
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai mokesčio suma yra 0 (nulis) arba mokestis nėra apskaičiuojamas.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f2a5bb0d1cef93ec1fea2e21c1750fe94a454c18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849850"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Mokestis nesuskaičiuotas arba mokesčio suma lygi nuliui

[!include [banner](../includes/banner.md)]

Operacijoje gali būti eilutės suma, kuri nėra 0 (nulis), bet mokestis nėra apskaičiuotas arba apskaičiuota mokesčio suma yra 0. Norėdami išspręsti šią problemą, atlikite tolesniuose skyriuose nurodytus veiksmus.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Patikrinti, ar operacijos teisingai parinkti mokesčių kodai

Jei operacija nepasirinko teisingų mokesčių kodų arba nepasirinko jokių mokesčių kodų, pagal juos mokesčiai nebus skaičiuojami. Imkitės šių veiksmų, kad patikrintumėte, ar operacijos teisingai parinkti mokesčių kodai. 

1. Operacijos eilutės eilutės informacijos "FastTab" skirtuke Nustatymas, **PVM** **skyriuje** **patikrinkite**, **ar** **laukuose** Prekės PVM grupė ir PVM grupė pasirinktos tinkamos mokesčių grupės. Jei tinkamos mokesčių grupės nepasirinktos, pasirinkite jas.

    [![Prekės pardavimo mokesčio grupė ir pardavimo mokesčio grupės laukeliai.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM grupės**.
3. Pasirinkite atitinkamą PVM grupę, tada sąrankos **„FastTab" atlikite pastabą apie PVM** **kodą lauke PVM** kodas.

    [![PVM grupių puslapis.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **Prekės PVM grupės**.
5. Pasirinkite atitinkamą prekės PVM grupę, tada nustatymo **„FastTab" patikrinkite, ar PVM kodo lauke esantis mokesčio kodas atitinka PVM** **grupės mokesčio** kodą.

    [![Prekės pardavimo mokesčių grupių puslapis.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Jei mokesčių kodai nesutampa, atnaujinkite vienos iš grupių PVM kodą.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Patikrinti, ar pasirinkti mokesčių kodai nėra neapmokestinami ir ar jie turi teisingą mokesčio tarifo vertę

Jei mokesčio kodai yra neapmokestinami arba jei mokesčio tarifas yra 0 (nulis), mokesčio skaičiavimo rezultatas bus 0. Norėdami nustatyti, ar pasirinkti mokesčių kodai yra neapmokestinami, ir patikrinti, ar jiems taikomas teisingas mokesčio tarifas, atlikite šiuos veiksmus.

1. Eikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM grupės**.
2. Pasirinkite atitinkamą PVM grupę, tada **nustatymo** „FastTab" patikrinkite, ar **išvalytas** žymės langelis Atleista. Jei jis pažymėtas, išvalykite.

    [![PVM grupių puslapio žymės langelis Atleidžiamas nuo mokesčių.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.
4. Pasirinkite tinkamą PVM kodą, tada patikrinkite, ar mokesčio tarifo vertė **vertės lauke** nėra 0 (nulis). Jei tai 0, atnaujinkite lauką, kad jis būtų nustatytas pagal teisingą mokesčio tarifą.

    [![Vertės laukelis PVM kodų reikšmių puslapis.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Nustatyti, ar nulis yra teisinga mokesčio suma

Kai kuriuose scenarijuose 0 (nulis) esanti mokesčių suma yra teisinga. Norėdami nustatyti, ar 0 yra teisinga operacijos mokesčių suma, atlikite šiuos veiksmus.

1. Eikite į **Didžioji knyga** \> **Didžiosios knygos nustatymas** \> **DK parametrai**.
2. Skirtuko **PVM** lauke Skaičiavimo būdas **patikrinkite**, ar **pasirinkta Bendroji** suma.

    [![Skaičiavimo metodo laukelis Didžiosios knygos parametrų puslapyje.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.
4. Pasirinkite atitinkamą PVM kodą, rinkitės **Skaičiavimas** \> **Maržos bazė** ir patikrinkite, ar maržos bazė yra nustatyta į **Grynoji sąskaitos balanso suma** ar **Bendra sąskaitos suma įskaičiuoja kitas mokesčių sumas**. Daugiau informacijos rasite SF [sumą, įskaitant kitas PVM sumas](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Jei 2 ir 4 veiksmais nustatytos teisingos vertės, nustatykite, ar bendra operacijos suma yra 0 (nulis). Jei bendroji suma yra 0, numatomas rezultatas yra 0 mokesčių suma. Kadangi mokesčio skaičiavimas pagrįstas bendra SF balanso suma ir ši suma nėra eilutė pagal eilutę, mokesčio suma 0 bus priskirta kiekvienai eilutei po mokesčio skaičiavimo.

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas

Jei atlikote veiksmus ankstesniuose skyriuose, bet neradote problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
