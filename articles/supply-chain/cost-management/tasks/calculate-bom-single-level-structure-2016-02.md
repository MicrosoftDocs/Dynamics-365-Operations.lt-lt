---
title: Apskaičiuoti KS naudojant vieno lygio struktūrą (2016 m. vasario mėn.)
description: Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant vieno lygio išskleidimą, paremtą įkainojimo lapu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013eddf1ba8e8cab3c87cb1f063d9bf886b0f833
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821398"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Apskaičiuoti KS naudojant vieno lygio struktūrą (2016 m. vasario mėn.)

[!include [banner](../../includes/banner.md)]

Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant vieno lygio išskleidimą, paremtą įkainojimo lapu. Tai šeštoji KS skaičiavimo sekų užduotis. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.

1. Eikite į Išleisti produktai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite produktą BOM_1.  
3. Veiksmų srityje spustelėkite Valdyti išlaidas.
4. Spustelėkite Prekės kaina.
5. Spustelėkite Skaičiuoti prekės savikainą.
    * Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.  
6. Lauke Įkainojimo versija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Norėdami pademonstruoti, pasirinkite 10. Tai ta pati įkainojimo versija, naudojama savikainai į komponentus įtraukti.  
7. Spustelėkite GERAI.
8. Spustelėkite Peržiūrėti skaičiavimo informaciją.
    * Gali reikėti spustelėti elipsės mygtuką (...), kad šią parinktį matytumėte viršutiniame meniu.    Čia yra išlaidų sudėtis: * 10 išvesta iš ITEM_A, 10 iš ITEM_B, 10 iš BOM_2. Šiuo atveju nėra išsamios informacijos apie BOM_2, nes jis nebuvo apskaičiuotas – tik įvesta BOM_2 standartinės savikainos reikšmė 10.  * 7 išvedamas iš nustatymo laiko, kuris yra pastovios išlaidos, o papildomas 7 išvedamas iš apdorojimo laiko operacijos (Apdoroti).  * Taip pat yra kitų sumų, sutampančių su netiesioginėmis išlaidomis.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]