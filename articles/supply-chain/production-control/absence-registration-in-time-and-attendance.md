---
title: Neatvykimų registravimas modulyje Laikas ir buvimas darbe
description: Šiame straipsnyje paaiškinama, kaip tvarkyti neatvykimo registracijas dalyje Laikas ir lankomumas.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a613edbe42d1bfb1d2ee43ee1cb2f1e0ab49a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890776"
---
# <a name="absence-registration-in-time-and-attendance"></a>Neatvykimų registravimas modulyje Laikas ir buvimas darbe

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos neatvykimo koncepcijos ir paaiškinama, kaip tvarkyti neatvykimą dalyje Laikas ir lankomumas.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Įprastomis darbo valandomis pagrįstas neatvykimas

Darbuotojai, nedirbantys įprastų darbo valandų metu, laikomi neatvykusiais į darbą. Įprastos darbo valandos apibrėžtos darbuotojo standartinio laiko profilyje.

Pavyzdžiui, darbuotojas dirba dienos profiliu, kai atėjimas į darbą registruojamas 7:00 val., o išėjimas iš darbo – 15:00 val. Jei darbuotojas atėjimą į darbą užregistruoja 9:00 val., yra laikoma, kad tą dieną jis nuo 7:00 iki 9:00 val. nebuvo darbe.

Tokiu atveju darbuotojai raginami įvesti neatvykimo į darbą priežastį. Jie nurodyti priežastį gali pasirinkdami neatvykimų kodą.

## <a name="absence-codes"></a>Neatvykimų kodai

Neatvykimų kodais apibrėžiami įvairių tipų neatvykimai. Neatvykimo kodus apibrėžia įmonė.

Neatvykimo kodams gali būti taikomos įvairios taisyklės. Pavyzdžiui, neatvykimo kodą galima sukonfigūruoti taip, kad jį pritaikius būtų atskaitomi arba paskiriami mokėjimai.

Pavyzdžiui, įmonė darbuotojai neatvykimo kodą **Vėluoja** naudotų tada, jei jie į darbą ateina vėlai be pateisinamos priežasties. Įmonė taip pat apibrėžia **Vidinių kursų** neatvykimo kodą, kurį darbuotojai vidiniuose kursuose praleistam laikui žymėti. Šiuos neatvykimo kodus galima nustatyti taip, kad nurodžius kodą **Vėluoja** iš darbo užmokesčio atskaitomi pinigai, bet nurodžius kodą **Vidiniai kursai** pinigai iš darbuotojo darbo užmokesčio neatskaitomi.

Galite nustatyti automatinius neatvykimo kodus. Šiuos neatvykimo kodus galima panaudoti darbuotojo laikui, kai neatvykimas neregistruojamas, apskaičiuoti. Darbuotojo darbo laiko profilyje nustatoma, ar neatvykimo laikas bus naudojamas standartiniam ar nukrypimo laikui.

### <a name="set-up-standard-time-and-flex-time"></a>Standartinio ir nukrypimo laiko nustatymas

- Sukonfigūruokite standartinio ir nukrypimo laiko parametrus naudodami parinktis **Automatinis neatvykimo įvedimas** ir **Automatinis nukrypimo įvedimas -**, pateikiamus puslapyje **Laiko ir buvimo darbe parametrai**.

## <a name="absence-groups"></a>Neatvykimų grupės

Neatvykimų kodai sugrupuojanti į neatvykimų grupes. Neatvykimų grupėse sugrupuojami vienodų charakteristikų neatvykimų kodai. Pavyzdžiai: leistino neatvykimo kodai arba neatvykimo į darbą dėl apsilankymo pas gydytoją, dalyvavimo komisijoje ar sergančio vaiko kodai.

## <a name="planned-absence"></a>Suplanuotas neatvykimas

Jei žinote, kad darbuotojo tam tikrą laikotarpį nebus darbe, pvz., dėl būsimų atostogų, galite naudoti suplanuotus neatvykimus. Suplanuotą neatvykimą galite nustatyti tam tikru būdu sukonfigūruodami neatvykimo kodą, kad į jį būtų įtraukta suplanuoto neatvykimo tikimybė. Nustatydami suplanuotą neatvykimą, neatvykimo laikotarpiu, kai skaičiuojamos vartotojo laiko registracijos, nesate raginami pateikti neatvykimo kodą. Galima apibrėžti vieno darbuotojo suplanuotą neatvykimą arba paketinę užduotį, kad informacija apie darbuotojų neatvykimus būtų atnaujinama masiškai.

### <a name="set-up-planned-absence"></a>Suplanuotų neatvykimų nustatymas

1. Pasirinkite **Personalas** &gt; **Darbininkai** &gt; **Darbuotojai** ir pasirinkite darbuotoją.
2. Pasirinkite **Laikas** &gt; **Laiko priskyrimas** &gt; **Neatvykimų laiko registracija** ir nustatykite suplanuotą neatvykimą.

## <a name="interrupted-planned-absence"></a>Nutraukiamas suplanuotas neatvykimas

Jei nustatydami suplanuotą neatvykimą taikysite parinktį **Nutraukti**, darbuotojui užsiregistravus suplanuoto laikotarpio metu, suplanuotas neatvykimas bus nutrauktas. Suplanuotas neatvykimas bus pažymėtas kaip **Nutraukta** ir neturės įtakos būsimiems skaičiavimams.

### <a name="set-up-a-planned-absence-for-interruption"></a>Suplanuoto neatvykimo nutraukimo nustatymas

1. Atidarykite puslapį **Neatvykimo laiko registracija**, kaip aprašyta suplanuoto neatvykimo nustatymo procedūroje.
2. Pasirinkite **Nutraukti**.

Parinktis **Nutraukti** taikoma, kai laikas registruojamas naudojant darbo laiko terminalą arba darbo laiko įrenginį. Parinktis netaikoma, jei registracijos įvedamos skaičiavimo ir patvirtinimo puslapiuose arba puslapyje **Elektroninė laiko kortelė**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Neatvykimų naudojimų pavyzdžiai nukrypimų profilyje

Toliau pateiktuose trijuose šablonuose rodoma, kaip apskaičiuojamas neatvykimas profilyje su nukrypimo laikotarpiais.

Šiuose pavyzdžiuose naudojamas toliau nurodytas profilis.

| Atėjimas į darbą | Standartinis laikas    | Pertrauka             | Standartinis laikas | Nukrypimas-        | Išėjimas iš darbo | Nukrypimas+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8:00 val.     | Nuo 9:00 iki 11:30 val. | Nuo 11:30 iki 12:00 val. | Nuo 12:00 iki 15:00 val. | Nuo 15:00 iki 16:00 val. | 16:00      | Nuo 16:00 iki 18:00 val. |

### <a name="example-1-signing-out-during-a-flex--period"></a>1 pavyzdys: išsiregistravimas iš darbo nukrypimo- laikotarpiu

Darbuotojas atėjimą į darbą užregistruoja 8:00 val., o išsiregistruoja 15:30 val. Tokiu atveju neatvykimas neskaičiuojamas, nes darbuotojas iš darbo išsiregistruoja nukrypimo- laikotarpiu ir iš darbuotojo nukrypimų balansų atskaičiuojamas pusvalandis.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>2 pavyzdys: išsiregistravimas iš darbo standartinio laiko laikotarpiu

Darbuotojas atėjimą į darbą užregistruoja 8:00 val., o išėjimą išregistruoja 14:30 val. Tokiu atveju neatvykimas skaičiuojamas nuo 14:30 iki 16:00 val., nes darbuotojas iš darbo išsiregistruoja standartinio laiko laikotarpiu ir registruojamas 1,5 valandos neatvykimo laikotarpis. Šiam laikotarpiui reikia priskirti neatvykimo kodą.

### <a name="example-3-signing-out-during-a-flex-period"></a>3 pavyzdys: išsiregistravimas iš darbo nukrypimo+ laikotarpiu

Darbuotojas atėjimą į darbą užregistruoja 8:00 val., o išsiregistruoja 16:30 val. Tokiu atveju neatvykimas neskaičiuojamas, nes darbuotojas iš darbo išsiregistruoja nukrypimo+ laikotarpiu ir prie darbuotojo nukrypimų balansų pridedamas pusvalandis.

## <a name="absence-in-the-calculation-and-approval-process"></a>Neatvykimas skaičiavimo ir patvirtinimo procese

Darbuotojo laiko registracijos turi būti apskaičiuojamas ir patvirtinamos prieš jas perkeliant į algalapio sistemą kaip mokėjimo elementus.

Tvirtintojas gali keisti darbuotojo darbo laiko registracijas. Tvirtintojas gali keisti netgi bet kokį darbuotojo užregistruotą neatvykimą. Jei tvirtintojas rankiniu būdu įveda laikotarpį, kuriam priskirtas neatvykimo kodas, tam laikotarpiui skirtas neatvykimas kodas nėra perrašomas Laiko ir buvimo darbe parametruose įvestu numatytuoju neatvykimo kodu.

Pavyzdžiui, darbuotojas atėjimą į darbą užregistruoja 10:00 val. ir pasirenka neatvykimo kodą, žymintis vėlavimą. Vėliau darbuotojas informuoja savo vadovą, kad jis nuo 8:00 iki 10:00 val. lankėsi pas gydytoją. Dėl apsilankymo pas gydytoją iš darbuotojo atlyginimo pinigai neturi būti atskaitomi. Todėl tokiu atveju prižiūrėtojas dviejų valandų neatvykimą nuo 8:00 iki 10:00 val. gali koreguoti rankiniu būdu įvesdamas neatvykimo kodą, kuriuo žymima, kad darbuotojas tas dvi valandas sirgo.

### <a name="calculate-and-approve-absence"></a>Neatvykimo apskaičiavimas ir patvirtinimas

- Pasirinkite **Laikas ir buvimas darbe** &gt; **Peržiūrėti ir patvirtinti** &gt; **Patvirtinti arba skaičiuoti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]