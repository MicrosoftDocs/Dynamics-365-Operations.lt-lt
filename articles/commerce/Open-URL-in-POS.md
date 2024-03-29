---
title: URL atidarymas EKA
description: Šiame straipsnyje pateikta patobulinimų, kurie buvo atlikti produktų ir klientų ieškos funkcijoms, apžvalga Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.custom: 141393
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: ad82cf1039515e58d1717453ee3fb4e3dafd84fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276433"
---
# <a name="open-url-in-pos"></a>URL atidarymas EKA

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukonfigūruoti mygtuką point Dynamics 365 Commerce of sale (EKA) ir atidaryti URL. Šiai funkcija įjungti nereikia tinkinti kodo, taip pat ją sukonfigūruoti gali bet kuris vartotojas, turintis ne kūrėjo vaidmenį. 

Ši funkcija leidžia sukonfigūruoti EKA mygtuką naudojant mygtukyno dizaino įrankį, kad būtų galima atidaryti URL. Šiuo metu atidaryti URL galima toliau nurodytomis konfigūracijomis.

- Atidaryti naujame lange.
- Atidaryti pačiame EKA.
- Atidaryti vietinėje programoje.

## <a name="open-in-new-window"></a>Atidaryti naujame lange

Šia konfigūracija apibrėžiama, ar URL atidaryti naujame lange, ar pačioje programoje. Sukonfigūravus atidaryti interneto URL pačioje programoje, matoma šoninė naršymo sritis ir EKA viršutinė juosta, su kuriomis vartotojas gali sąveikauti. Sukonfigūravus atidaryti naujame lange, URL bus atidarytas naujame „Modern POS“, skirto „Windows“, programos lange, o visų kitų EKA klientų atveju – naujame naršyklės skirtuke. Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.

## <a name="open-within-pos"></a>Atidaryti pačiame EKA

Šiuo metu galimybė atidaryti interneto URL pačiame EKA palaikoma tik „Modern POS“, skirtame „Windows“. Kitiems klientams ši funkcija dar kuriama ir ją planuojama išleisti kartu su būsimais naujinimais. Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti nepasirinkę parinkties **Atidaryti naujame lange**.

## <a name="open-a-native-app"></a>Atidaryti vietinėje programoje

Ši funkcija leidžia jums nurodyti ne interneto URL, kad būtų galima atidaryti vietinėje programoje. Pavyzdžiui, galite nurodyti URL protokolus, pvz., „MailTo“, SIP, IM arba MSTEAMS, kuriuos vėliau galima sutvarkyti naudojant atitinkamas prieglobos įrenginio vietines programas. Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.

- Jei naudojate kompiuterius, kuriuose įdiegti „Windows“, žr. [Numatytųjų programos susiejimų eksportavimas arba importavimas](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kad nustatytumėte numatytąsias protokolo asociacijas, kai kompiuterį nustatote naudodamiesi vaizdų aptarnavimo ir tvarkymo visuotinio diegimo (DISM) sprendimu.
- Jei „Windows“ kompiuteriams valdyti naudojate MDM, pvz., „Intune“, žr. [Strategijos CSP – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Jei esate kūrėjas, kuriant pasirinktinę žiniatinklio svetainę, žr. [Numatytosios programos URI paleidimas](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Sklandus atidarymas vietinėje programoje

„Windows“, „iOS“ ir „Android“ taip pat leidžiama sklandžiau atidaryti daugiau programų, priklausomai nuo programos protokolo susiejimo. Jei jūsų programa dar nesukonfigūruota taip, kad atidarymą galėtų tvarkyti interneto naršyklėje, šiai funkcijai sukonfigūruoti gali prireikti kūrėjo paslaugų.

- Jei naudojate „Windows“, žr. [Programų žiniatinklio svetainėms įgalinimas naudojant URI apdorojimo programas](/windows/uwp/launch-resume/web-to-app-linking).
- Jei naudojate „iOS“, žr. [Kūrėjams skirtos universalios nuorodos](https://developer.apple.com/ios/universal-links/).
- Jei naudojate „Android“, žr. [„Android“ programos nuorodų tvarkymas](https://developer.android.com/training/app-links/).

| Klientas                | Atidaryti naujame lange | Atidaryti vietinėje programoje | Atidaryti pačiame EKA | Informacija                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| „Windows“ skirtas „Modern POS“ | ✓\*                | ✓               | ✓              | \* Atidaroma naujame „Modern POS“ lange |
| „Cloud POS“             | ✓\*                | ✓               | X              | \* Atidaroma naujame naršyklės skirtuke        |
| „iOS“ skirtas „Modern POS“     | ✓\*                | ✓               | X              | \* Atidaroma naujame naršyklės skirtuke        |
| „Modern POS“, skirtas „Android“ | ✓\*                | ✓               | X              | \* Atidaroma naujame naršyklės skirtuke        |

## <a name="before-you-begin"></a>Prieš pradedant

Prieš pradėdami, peržiūrėkite, kaip konfigūruoti [elektroninio kasos aparato (EKA) ekrano maketus](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>URL atidarymas EKA

Norėdami sukonfigūruoti URL taip, kad jį būtų galima atidaryti EKA, atlikite toliau nurodytus veiksmus.

1. Pagrindiniame biure eikite į **„Retail and Commerce“ \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.
2. Pasirinkite **Mygtukynai \> Kūrimo įrankis**.
3. Sukurkite naują mygtuką.
4. Pasirinkite **mygtuko** ypatybes.
5. Kaip veiksmą pasirinkite **Atidaryti URL**.
6. Įveskite norimą naudoti URL.
7. Sukonfigūruokite, ar norite, kad URL būtų atidaromas naujame lange.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
