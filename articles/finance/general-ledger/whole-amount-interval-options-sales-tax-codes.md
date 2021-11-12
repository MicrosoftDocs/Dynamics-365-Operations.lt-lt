---
title: PVM kodų skaičiavimo parinktys Visa suma ir Intervalas
description: Šiame straipsnyje paaiškinamos PVM kodų lauko Skaičiavimo būdas parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.
author: kailiang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44c4ce480de470b623f6faeff5a763bfcb05aecc
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726851"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a>PVM kodų skaičiavimo parinktys Visa suma ir Intervalas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamos PVM kodų **Skaičiavimo būdas** lauko parinktys ir tai, kaip skaičiuojamas intervalų ir visų sumų PVM.

Galite nustatyti, kad PVM kodas būtų skaičiuojamas pagal visą sumą arba intervalo sumą. **PVM kodų** puslapyje naudokite **Skaičiavimo metodas** lauką **Skaičiavimas** FastTab skirtuke, kad pasirinktumėte pardavimo PVM kodo skaičiavimo metodą.
- Visa suma – mokesčio tarifas taikomas visai apmokestinamai sumai.
- Intervalas – apmokestinama suma skirstoma į dalis, kiekviena iš jų patenka į intervalą, kuris turi tam tikrą PVM tarifą. Sumos dalis, kuri patenka į tam tikrą intervalą, apmokestinama pagal to intervalo mokesčių tarifą. PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.
  > [!NOTE]                                                                                                                              
  > Parinktis Intervalas galima tik puslapio DK parametrai srities PVM lauke Skaičiavimo metodas pasirinkus Eilutė. 

Intervalai nustatomi puslapyje PVM kodo reikšmės įvedant mokesčio tarifo žemiausią ir aukščiausią ribines sumas. Siekiant apskaičiuoti visų apmokestinamų sumų mokesčius (nepaisant to, koks pasirinktas skaičiavimo metodas) intervalai turi atitikti šiuos reikalavimus:
-   Mažiausia primojo intervalo turi būti riba – nulis.
-   Paskutinio intervalo aukščiausia riba turi būti nulis, tai reiškia begalybę.
-   Aukščiausia intervalo riba turi būti žemiausia kito intervalo riba.

Jei suma yra aukščiausia ankstesnio intervalo riba ir žemiausia kito intervalo riba, tai sumai bus taikomas pirmojo intervalo PVM tarifas. Jei suma nepatenka į intervalus, kuriuos nustato apatinės ir viršutinės ribos, taikomas PVM tarifas yra nulis.

## <a name="example-whole-amount-method-of-calculation"></a>Pavyzdys: bendros sumos skaičiavimo metodas
Puslapyje PVM kodų vertės PVM tarifai nustatomi šiais intervalais:

| Minimali riba     | Aukščiausia riba     | Mokesčio tarifas     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

PVM skaičiuojamas visai apmokestinamai sumai.

| Apmokestinama suma (kaina) | Skaičiavimas    | PVM |
|------------------------|----------------|-----------|
| 35,00                  | 35,00 \* 0,30  | 10,50     |
| 50,00                  | 50,00 \* 0,30  | 15,00     |
| 85,00                  | 85,00 \* 0,20  | 17,00     |
| 305,00                 | 305,00 \* 0,10 | 30,50     |

## <a name="example-interval-method-of-calculation"></a> Pavyzdys: intervalinis skaičiavimo metodas
Puslapyje Reikšmės PVM tarifai yra nustatomi šiais intervalais:

| Minimali riba     | Aukščiausia riba     | Mokesčio tarifas     |
|-------------------|-------------------|--------------|
| 0,00              | 50,00             | 30 %          |
| 50,00             | 100,00            | 20 %          |
| 100,00            | 0,00              | 10 %          |

PVM yra mokesčių sumų, kurios apskaičiuotos kiekvienam sumos intervalui, suma.

| Apmokestinama suma (kaina) | Skaičiavimas                                                               | PVM |
|------------------------|---------------------------------------------------------------------------|-----------|
| 35,00                  | 35,00 \* 0,30                                                             | 10,50     |
| 50,00                  | 50,00 \* 0,30                                                             | 15,00     |
| 85,00                  | (50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)                          | 22,00     |
| 305,00                 | (50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50) | 45.50     |



Daugiau informacijos žr. [PVM tarifų nustatymas pagal bazinės ribos ir skaičiavimo metodus](marginal-base-field.md).







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
