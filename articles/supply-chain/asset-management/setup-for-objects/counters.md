---
title: Turto matai
description: Šiame straipsnyje paaiškinama, kaip kurti turto valdymo turto matų tipus.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1bcef89265697c1898b7d61a0b0ae6331ce1c851
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909678"
---
# <a name="counters"></a>Skaitikliai

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip kurti skaitiklio tipus turto valdymo dalyje. Skaitiklio tipai naudojami norint atlikti turto skaitiklių registracijas, pvz., gamybos valandų skaičių arba pagaminto turto kiekį. Turto tipai yra susiję su skaitiklio tipais. Tai reiškia, kad skaitiklis gali būti naudojamas turtui tik tuo atveju, jei skaitiklis yra nustatytas naudojamam turto tipui.

Prieš atliekant turto skaitiklio registracijas, būtina sukurti skaitiklio tipus, kuriuos norite naudoti **Skaitikliai**. Tada **Skaitikliai** galima kurti skaitiklio registracijas. 

Skaitikliai gali būti naudojami priežiūros planuose. Priežiūros plano eilutė gali būti tipo „Skaitiklis“, pavyzdžiui, susijusi su gamybos valandų skaičiumi arba pagamintu kiekiu. 

Skaitiklio registraciją galima atnaujinti rankiniu būdu arba automatiškai, atsižvelgiant į gamybos valandas arba pagamintą kiekį. Skaitiklis gali būti nustatytas naudoti vieną iš trijų naujinimo metodų (pasirinktų lauke **Naujinti**, dalyje **Skaitikliai**):
  
- Rankinis – skaitiklio reikšmes būtina užregistruoti rankiniu būdu.  
- Gamybos valandos – skaitiklis automatiškai atnaujinamas pagal gamybos valandų skaičių.  
- Gamybos kiekis – skaitiklis automatiškai atnaujinamas pagal pagamintą kiekį.  

>[!NOTE]
>Jei naudojamas pagamintas kiekis, *visi* užregistruoti elementai įtraukiami į skaitiklio registraciją, t. y. tiek tinkamas kiekis, tiek kiekis su klaidomis. Jei reikia, skaitiklio registraciją visada galima atlikti rankiniu būdu.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Turto skaitiklio registravimų skaitiklio tipų kūrimas

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują skaitiklio tipą.
3. Lauke **Skaitiklis** įterpkite ID, o lauke **Pavadinimas** – skaitiklio pavadinimą.
4. „FastTab“ **Bendra** pasirinkite skaitiklio vienetą lauke **Vienetas**.
5. Lauke **Naujinti** pasirinkite skaitikliui naudojamą naujinimo metodą.
6. Perjungimo mygtuke **Paveldėti skaitiklio reikšmes** pasirinkite „Taip“, jei antrinis turtas turto struktūroje turi automatiškai paveldėti skaitiklio registracijas, atliktas pagrindiniame turte.
7. Lauke **Bendroji agreguota reikšmė** pasirinkite skaitikliui naudojamą sumavimo metodą naudojant šį skaitiklio tipą. „Sum“ yra standartinis pasirinkimas, naudojamas norint nuolat įtraukti užregistruotas reikšmes į bendrąją reikšmę. „Average“ gali būti naudojamas, jei skaitiklis nustatytas stebėti ribines reikšmes, pvz., temperatūrą, vibraciją ar turto nusidėvėjimą. 
8. Lauke **Nuokrypis virš** įveskite viršutinę procentinę reikšmę tikrinant, ar rankiniu būdu atliktos skaitiklio registracijos patenka į numatytą intervalą. Tikrinimas pagrįstas esamų skaitiklio registracijų tiesiniu padidėjimu.
9. Lauke **Nuokrypis iki** įveskite apatinę procentinę reikšmę tikrinant, ar rankiniu būdu atliktos skaitiklio registracijos patenka į numatytą intervalą. Tikrinimas pagrįstas esamų skaitiklio registracijų tiesiniu sumažėjimu.
10. Lauke **Tipas** pasirinkite pranešimo tipą (informacija, įspėjimas, klaida), kuris bus rodomas, jei rankiniu būdu atliekamų skaitiklio registravimų metu atsiranda nuokrypių už apibrėžto intervalo.
11. „FastTab“ **Turto tipai** įtraukite turto tipus, kurie turėtų galėti naudoti skaitiklį.
12. „FastTab“ **Susijusio turto skaitikliai** įtraukite skaitiklį, kuris bus automatiškai atnaujinamas atnaujinus šį skaitiklį.


>[!NOTE]
>Susijęs skaitiklis automatiškai atnaujinamas tik tuo atveju, jei skaitiklio nustatymuose susijęs skaitiklis yra turto tipo. Pavyzdžiui, skaitiklį galima nustatyti „Gamybos valandoms“ ir įtraukti turto tipą „Sunkvežimio variklis“. Kai šis skaitiklis atnaujinamas, susijęs skaitiklis „Alyva“ taip pat atnaujinamas pagal tas pačias skaitiklio reikšmes. Nustatymai dalyje **Skaitikliai** apima nustatymus „Valandos“. Be to, skaitiklyje „Alyva“ turto tipas „Sunkvežimio variklis“ turi būti įtrauktas į „FastTab“ **Turto tipai**, kad būtų užtikrintas skaitiklio ryšys. Žr. toliau esančias ekrano kopijas, kuriose pateiktas valandų ir alyvos skaitiklių nustatymo pavyzdys.

Kai turto tipai įtraukiami į skaitiklio tipą dalyje **Skaitikliai**, šis skaitiklis automatiškai įtraukiamas į turto tipus „FastTab“ **Skaitikliai**, dalyje [Turto tipai](../setup-for-objects/object-types.md).

![1 iliustracija.](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]