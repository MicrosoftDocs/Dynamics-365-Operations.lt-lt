---
title: Finansinių dimensijų apibrėžimas
description: Naudojant šią procedūrą rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10a991938f68c0ade19999e48a02f032c92a6779
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716949"
---
# <a name="define-financial-dimensions"></a>Finansinių dimensijų apibrėžimas

[!include [banner](../../includes/banner.md)]

Naudojant šią procedūrą rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją. Šiame vadove naudojama demonstracinė įmonė USMF.

## <a name="create-an-entity-backed-financial-dimension"></a>Objekto remiamos finansinės dimensijos kūrimas
1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinės dimensijos**.
2. Spustelėkite **Naujas**.
3. Lauke **Vartotojo verčių forma** pasirinkite sistemos nurodytą objektą, kurio pagrindu bus sukurta finansinė dimensija. 
4. Lauke **Dimensijos pavadinimas** įveskite finansinę dimensiją aprašančią vertę. Pavadinimas gali skirtis nuo sistemos nurodyto objekto, tačiau jame negali būti tarpų arba specialiųjų simbolių.
5. Spustelėkite **Aktyvinti**. Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.  
6. Aktyvinimo pranešime spustelėkite **Uždaryti**.
7. Spustelėkite **Aktyvinti**. Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.  
8. **Veiksmų srityje** spustelėkite **Dimensijos reikšmės**. Kai kurios dimensijų reikšmės siejamos su konkrečia įmone. Tai, ar jos siejamos su konkrečia įmone, sužinosite patikrinę, ar dimensijos reikšmių sąraše nurodomas įmonės pavadinimas.  

## <a name="create-a-custom-financial-dimension"></a>Pasirinktinės finansinės dimensijos kūrimas
1. Spustelėkite **Naujas**.
2. Lauke **Naudoti vertes iš** pasirinkite **Pasirinktinė dimensija**.
3. Lauke **Dimensijos pavadinimas** įveskite finansinę dimensiją aprašančią vertę.
    - Pavadinime negali būti tarpų arba specialiųjų simbolių.  
    - Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą.   
    - Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį. Taip pat galite įvesti skaičiaus ženklus (#) ir ampersandus (&) kaip vietos rezervavimo ženklus vietoj raidžių ir skaitmenų, kurie bus skirtingi kaskart sukūrus dimensijos reikšmę. Naudokite skaičiaus ženklą (#) kaip skaitmens vietos rezervavimo ženklą, o ampersandą (&) kaip raidės vietos rezervavimo ženklą.  Pavyzdys: Norėdami apriboti dimensijos reikšmę iki raidžių CC ir trijų skaitmenų, kaip formato šabloną įveskite CC-###.  
4. Spustelėkite **Aktyvinti**. Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.     
5. Spustelėkite **Aktyvinti**. Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.      
6. **Veiksmų srityje** spustelėkite **Dimensijos reikšmės**.
7. Spustelėkite **Naujas**.
8. Lauke **Dimensijos reikšmė** įveskite jūsų finansinės dimensijos reikšmę aprašantį pavadinimą.
9. Lauke **Aprašas** įveskite aprašymą, kuris apibūdina jūsų finansinės dimensijos reikšmę.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
