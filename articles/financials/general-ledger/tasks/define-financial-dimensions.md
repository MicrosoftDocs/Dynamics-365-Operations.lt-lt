--- 
title: "Apibrėžti finansines dimensijas"
description: "Šiame užduoties vadove rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją."
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="define-financial-dimensions"></a>Apibrėžti finansines dimensijas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame užduoties vadove rodoma, kaip įtraukti objekto remiamą finansinę dimensiją ir pasirinktinę finansinę dimensiją.  Šiame vadove naudojama demonstracinė įmonė USMF.


## <a name="create-an-entity-backed-financial-dimension"></a>Objekto remiamos finansinės dimensijos kūrimas
1. Eikite į Didžioji knyga > Sąskaitų planas > Dimensijos > Finansinės dimensijos.
2. Spustelėkite Naujas.
3. Lauke Vartotojo vertės nuo pasirinkite sistemos nurodytą objektą, kurio pagrindu bus sukurta finansinė dimensija. 
4. Lauke Dimensijos pavadinimas įveskite finansinę dimensiją aprašančią vertę.
    * Pavadinimas gali skirtis nuo sistemos nurodyto objekto, tačiau jame negali būti tarpų arba specialiųjų simbolių.  
5. Spustelėkite Aktyvinti.
    * Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.  
6. Aktyvinimo pranešime spustelėkite Uždaryti.
7. Spustelėkite Aktyvinti.
    * Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.  
8. Spustelėkite Dimensijos reikšmės.
    * Kai kurios dimensijų reikšmės siejamos su konkrečia įmone. Tai, ar jos siejamos su konkrečia įmone, sužinosite patikrinę, ar dimensijos reikšmių sąraše nurodomas įmonės pavadinimas.  

## <a name="create-a-custom-financial-dimension"></a>Pasirinktinės finansinės dimensijos kūrimas
1. Uždarykite puslapį.
2. Spustelėkite Naujas.
3. Lauke Naudoti vertes iš pasirinkite <Custom dimension>.
4. Lauke Dimensijos pavadinimas įveskite finansinę dimensiją aprašančią vertę.
    * Pavadinime negali būti tarpų arba specialiųjų simbolių.  
    * Taip pat galite nurodyti sąskaitos šabloną, ribojantį informacijos, kurią galite įvesti kaip dimensijos reikšmes, kiekį ir tipą.   
    * Galite įvesti simbolius, kurie išlieka vienodi visose dimensijos reikšmėse, pvz., raides arba brūkšnelį. Taip pat galite įvesti skaičiaus ženklus (#) ir ampersandus (&) kaip vietos rezervavimo ženklus vietoj raidžių ir skaitmenų, kurie bus skirtingi kaskart sukūrus dimensijos reikšmę. Naudokite skaičiaus ženklą (#) kaip skaitmens vietos rezervavimo ženklą, o ampersandą (&) kaip raidės vietos rezervavimo ženklą.  Pavyzdys: Norėdami apriboti dimensijos reikšmę iki raidžių CC ir trijų skaitmenų, kaip formato šabloną įveskite CC-###.  
5. Spustelėkite Aktyvinti.
    * Suaktyvinus finansinę dimensiją lentelė atnaujinama ir joje pateikiamas finansinės dimensijos pavadinimas, o panaikintos dimensijos pašalinamos. Dimensijų reikšmes galima įvesti prieš suaktyvinant finansinę dimensiją, bet finansinės dimensijos negalima naudoti, kol ji yra suaktyvinta.  
6. Spustelėkite Aktyvinti.
    * Dimensijos aktyvinimą galima suplanuoti atlikti pakete, nurodant konkrečią dieną ir laiką.  
7. Spustelėkite Dimensijos reikšmės.
8. Spustelėkite Naujas.
9. Lauke Dimensijos reikšmė įveskite jūsų finansinės dimensijos reikšmę aprašantį pavadinimą.
10. Lauke Aprašas įveskite aprašymą, kuris apibūdina jūsų finansinės dimensijos reikšmę.


