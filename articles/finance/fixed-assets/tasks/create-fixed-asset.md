---
title: Ilgalaikių išteklių kūrimas
description: Šiame straipsnyje paaiškinama, kaip kurti naują ilgalaikio turto įrašą iš ilgalaikio turto sąrašo puslapio.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00c72081d20015737aa027cee9474a54e498cef4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868495"
---
# <a name="create-a-fixed-asset"></a>Ilgalaikių išteklių kūrimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip kurti naują ilgalaikio turto įrašą iš ilgalaikio **turto** sąrašo puslapio.

Sistema priskiria turto numerį, pagrįstą numeracija, priskirta ilgalaikio turto grupei. Jei naudojate ilgalaikio turto šabloną turto importavimo naudojant „Microsoft Excel” papildinį metu arba jei naudojate kitą importavimo užduotį, sistema automatiškai sukuria ilgalaikio turto įrašus ir padidina turto numerį.

Norėdami rankiniu būdu sukurti turto įrašą, atlikite toliau pateiktus veiksmus.

1. Eikite į **Naršymo sritis \> Moduliai \> Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
2. **Veiksmų srityje** pasirinkite **Naujas**.
3. Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę. Laukas **Numeris** bus numatytasis, jei įjungėte **Automatiškai sunumeruotas ilgalaikio turto funkcionalumas** parinktyse **Ilgalaikio turto parametrai** ir **Ilgalaikio turto grupė**. Jei neįgalinote, turite įvesti unikalų numerį, kad identifikuotumėte ilgalaikį turtą.
4. Lauke **Pavadinimas** įveskite reikšmę. Įveskite papildomą šio turto informaciją, kurios reikia jūsų verslui.
5. **Veiksmų srityje** pasirinkite **Knygos**.
6. Lauke **Įsigijimo data** įveskite datą.
7. Lauke **Įsigijimo kaina** įveskite skaičių.

    - Įveskite papildomą šios knygos informaciją, kurios reikia jūsų verslui.
    - Įveskite papildomą likusių knygų informaciją, kurios reikia jūsų verslui.

8. Uždarykite puslapį.

Taip pat galite importuoti ilgalaikį turtą naudodami „Excel” papildinį arba vykdydami importavimo užduotį iš darbo srities **Duomenų valdymas**. Prieš paleisdami importavimą, įveskite reikiamų šablono laukų vertes.

Jei nenurodėte ilgalaikio turto numerio „Excel” papildinio šablone arba duomenų valdyme, sistema sukuria kiekvieno importuoto turto ilgalaikio turto numerį ir automatiškai padidina kiekvieno numeraciją. Tačiau, jei importuojate turtą ir nurodote turto numerius šablone, sistema automatiškai **nepadidina** numeracijos. Tokiu atveju administratoriui gali tekti rankiniu būdu atnaujinti numeraciją. Jei nurodėte ilgalaikio turto numerį „Excel” papildinio šablone, sistema naudoja nurodytą ilgalaikio turto numerį ir padidina numeraciją.

> [!NOTE]                                                                                                         
> Užregistravus nusidėvėjimą, laukai **Atiduota eksploatuoti** ir **Nusidėvėjimo vykdymo data** bus užrakinti puslapyje **Knyga**. Be to, nė vienas laukas nebus atnaujintas iš duomenų objekto.

> [!WARNING]
> Ilgalaikio turto įrašas nebus panaikintas, jei operacijos buvo užregistruotos susijusioje knygoje arba jei naujai sukurtas ilgalaikis turtas yra įvedamas į žurnalo eilutę, bet neužregistruojamas. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
