---
title: "Visa suma ir PVM kodų intervalo skaičiavimo parinktys"
description: "Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bab0f6ca21f4216b70cccf24f5781e0dbf48b7f8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>Visa suma ir PVM kodų intervalo skaičiavimo parinktys

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.

Galite nustatyti, kad PVM kodas būtų skaičiuojamas pagal visą sumą arba intervalo sumą. PVM kodų puslapyje „FastTab“ skirtuko Skaičiavimas lauke Skaičiavimo metodas pasirinkite, kaip skaičiuoti PVM kodą.
-   Visa suma – mokesčio tarifas taikomas visai apmokestinamai sumai.
-   Intervalas – apmokestinama suma skirstoma į dalis, kiekviena iš jų patenka į intervalą, kuris turi tam tikrą PVM tarifą. Sumos dalis, kuri patenka į tam tikrą intervalą, apmokestinama pagal to intervalo mokesčių tarifą. PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.
> [!NOTE]                                                                                                                              
> Parinktis Intervalas galima tik puslapio DK parametrai srities PVM lauke Skaičiavimo metodas pasirinkus Eilutė. 

Intervalai nustatomi puslapyje PVM kodo reikšmės įvedant mokesčio tarifo žemiausią ir aukščiausią ribines sumas. Siekiant apskaičiuoti visų apmokestinamų sumų mokesčius (nepaisant to, koks pasirinktas skaičiavimo metodas) intervalai turi atitikti šiuos reikalavimus:
-   Mažiausia primojo intervalo turi būti riba – nulis.
-   Paskutinio intervalo aukščiausia riba turi būti nulis, tai reiškia begalybę.
-   Aukščiausia intervalo riba turi būti žemiausia kito intervalo riba.

Jei suma yra aukščiausia ankstesnio intervalo riba ir žemiausia kito intervalo riba, tai sumai bus taikomas pirmojo intervalo PVM tarifas. Jei suma nepatenka į intervalus, kuriuos nustato apatinės ir viršutinės ribos, taikomas PVM tarifas yra nulis.

## <a name="example-whole-amount-method-of-calculation"></a>Pavyzdys: bendros sumos skaičiavimo metodas
Puslapyje PVM kodų vertės PVM tarifai nustatomi šiais intervalais:
|                   |                   |              |
|-------------------|-------------------|--------------|
| **Minimali riba** | **Aukščiausia riba** | **Mokesčio tarifas** |
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

PVM skaičiuojamas visai apmokestinamai sumai.

| Apmokestinama suma (kaina) | Skaičiavimas    | PVM |
|------------------------|----------------|-----------|
| 35,00                  | {35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a> Pavyzdys: intervalinis skaičiavimo metodas
Puslapyje Reikšmės PVM tarifai yra nustatomi šiais intervalais:

|                   |                   |              |
|-------------------|-------------------|--------------|
| **Minimali riba** | **Aukščiausia riba** | **Mokesčio tarifas** |
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.

| Apmokestinama suma (kaina) | Skaičiavimas                                                               | PVM |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45,50     |

 

Daugiau informacijos žr. [PVM tarifų nustatymas pagal Bazinės ribos ir Skaičiavimo metodo laukus](marginal-base-field.md).






