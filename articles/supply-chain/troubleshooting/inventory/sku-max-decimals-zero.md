---
title: Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0
description: 'Kai bandote užregistruoti atsargų operaciją arba atsargų rezervavimą, gaunate tokį klaidos pranešimą: „Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0“.'
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477131"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0


## <a name="symptoms"></a>Požymiai

Kai bandote užregistruoti atsargų operaciją ar atsargų rezervavimą, gaunate tokį klaidos pranešimą:

> Didžiausias atsargų saugojimo vieneto dešimtainių dalių skaičius yra 0.

Ši problema kyla tada, kai atsargų operacijos kiekis nurodomas kaip dešimtainė vertė, kuri yra mažesnė už lauke palaikomą tikslumo lygį. Pavyzdžiui, nurodytas atsargų operacijos *0,5* kiekis, bet tik sveikųjų skaičių kiekiai yra palaikomi. Todėl vertė turi būti *1* vietoje *0,5*.

## <a name="resolution"></a>Sprendimas

1. Paleiskite šį scenarijų „SQL Server” programoje, kad suapvalintumėte kiekius atsargų operacijose. Šis scenarijus pataisys lentelės **inventTrans** vertes.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Paleiskite turimo vientisumo patikrą, kai **taisyti klaidą** parinktis yra įjungta. Šis patikrinimas ištaisys vertes lentelėje **inventSum**.

> [!IMPORTANT]
> Itin rekomenduojame, kad atidžiai redaguotumėte scenarijų, kaip to reikalaujama jūsų aplinkoje, atliktumėte testavimą testavimo aplinkoje ir patikrintumėte rezultatų duomenis prieš paleisdami scenarijų gamybos aplinkoje.
