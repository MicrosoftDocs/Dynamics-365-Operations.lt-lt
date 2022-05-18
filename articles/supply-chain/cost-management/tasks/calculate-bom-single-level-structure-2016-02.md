---
title: Apskaičiuoti KS naudojant vieno lygio struktūrą (2016 m. vasario mėn.)
description: Šioje procedūroje nurodoma, kaip apskaičiuoti galutinio produkto savikainą naudojant vieno lygio išskleidimą, paremtą įkainojimo lapu.
author: JennySong-SH
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a52542f6c93897519187313c026a4598e41cc362
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673248"
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