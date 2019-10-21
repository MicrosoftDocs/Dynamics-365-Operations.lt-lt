---
title: Nusidėvėjimo poveikis su atšaukimais
description: Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187365"
---
# <a name="depreciation-effects-with-reversals"></a>Nusidėvėjimo poveikis su atšaukimais

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aptartos galimos ilgalaikio turto operacijos atšaukimo pasekmės. 

Galite atšaukti ilgalaikio turto operacijas ir su ilgalaikiu turtu susietas operacijas. Atšauktą operaciją taip pat galite anuliuoti. 

Atšaukite arba anuliuokite galite operaciją, kuri nebuvo paskutinė operacija, registruota turto knygoje. Pirmiausia turėtumėte nustatyti, ar po operacijos, kurią atšaukiate, buvo užregistruota kokių nusidėvėjimo operacijų. Taip yra todėl, nes, atšaukiant operaciją, nusidėvėjimas neperskaičiuojamas. Todėl po atšaukimo nusidėvėjimas dažnai pervertinamas ar nuvertinamas, kaip parodyta pavyzdžiuose. 

Kad užtikrintumėte, kad, atšaukiant operaciją, nusidėvėjimas teisingas, netęskite atšaukimo, jeigu gaunate pranešimą, kad nusidėvėjimas nebus skaičiuojamas iš naujo. Geriau pirmiausia atšaukite nusidėvėjimo operaciją, kuri užregistruota po operacijos, kurią bandote atšaukti, tada tęskite atšaukimą. Nebūsite įspėti apie nusidėvėjimo perskaičiavimus ir galėsite tęsti atšaukimą. 

Toliau pateiktuose pavyzdžiuose rodomi skaičiavimai, kurie atliekami, jei tęsiate nepaisydami pranešimo ir pirmiausia neatšaukę nusidėvėjimo operacijų.

## <a name="example-1-depreciation-is-overstated"></a> 1 pavyzdys: nusidėvėjimas pervertintas
Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių). Šiame pavyzdyje nusidėvėjimas pervertintas.
#### <a name="asset-transaction-history"></a>Turto operacijų retrospektyva

| Data       | Operacijos tipas                                                          | Suma                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| Sausio 1  | Įsigijimas                                                               | 59 000,00                                 |
| Sausio 1  | Įsigijimo koregavimas                                                    | 1000,00                                  |
| Sausio 31 | Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui) | 1 000,00Skaičiavimas: balansinė vertė (59 000 + 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60) |

#### <a name="reversal-action"></a>Atšaukimo veiksmai

| Data      | Operacijos tipas                | Suma    |
|-----------|---------------------------------|-----------|
| Sausio 1 | Įsigijimo derinimo atšaukimas | -1000,00 |

#### <a name="depreciation-effect"></a>Nusidėvėjimo efektas

| Data        | Operacijos tipas        | Suma                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| Vasario 28 | Nusidėvėjimas (pasiūlymas) | 983,05Skaičiavimas: balansinė vertė (59 000 – 1 000 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59) |

Nusidėvėjimas parvertintas 16,95 (1000–983,05).

## <a name="example-2-depreciation-is-understated"></a> 2 pavyzdys: Nusidėvėjimas nuvertintas
Turtas nustatytas su 5 metų naudojimu ir tiesiogiai proporcingu nusidėvėjimu (60 nusidėvėjimo laikotarpių). Šiame pavyzdyje nusidėvėjimas nuvertintas.
#### <a name="asset-transaction-history"></a>Turto operacijų retrospektyva

| Data       | Operacijos tipas                                                          | Suma                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| Sausio 1  | Įsigijimas                                                               | 59 000,00                                   |
| Sausio 1  | Vertės mažinimas                                                     | 1000,00                                    |
| Sausio 31 | Nusidėvėjimas (sukurtas naudojant pasiūlymą vienam nusidėvėjimo laikotarpiui) | 966,67Skaičiavimas: balansinė vertė (59 000 – 1 000) / likusių nusidėvėjimo laikotarpių skaičius (60) |

#### <a name="reversal-action"></a>Atšaukimo veiksmai

| Data      | Operacijos tipas               | Suma    |
|-----------|--------------------------------|-----------|
| Sausio 1 | Vertės mažinimo atšaukimas | -1000,00 |

#### <a name="depreciation-effect"></a>Nusidėvėjimo efektas

| Data        | Operacijos tipas        | Suma                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| Vasario 28 | Nusidėvėjimas (pasiūlymas) | 983,62Skaičiavimas: balansinė vertė (59 000 – 966,67 nusidėvėjimas) / likusių nusidėvėjimo laikotarpių skaičius (59) |

Nusidėvėjimas nuvertintas 16,95 (983,62–966,67).



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Ilgalaikio turto nusidėvėjimas](fixed-asset-depreciation.md)


