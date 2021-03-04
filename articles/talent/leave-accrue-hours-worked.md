---
title: Nedarbo laiko kaupimas pagal dirbtas valandas
description: Šioje temoje aprašoma, kaip galima konfigūruoti atostogų planus, kad būtų galima kaupti laiko nedarbo laiką pagal dirbtas valandas.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462021"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Nedarbo laiko kaupimas pagal dirbtas valandas

## <a name="overview"></a>Apžvalga

Organizacijos, kuriose esama už valandinį įkainį dirbančių darbuotojų, nedarbo laiką gali skirti pagal dirbtas valandas, o ne pagal pareigų ėjimo organizacijoje trukmę. Duomenys apie dirbtas valandas paprastai saugomi laiko ir lankomumo sistemoje. 

## <a name="leave-plans"></a>Atostogų planai

Atostogų plane kaupimo tipas gali būti darbo mėnesiai arba darbo valandos. Pasirinkus darbo valandas, yra du kaupimui naudojamų valandų tipai: įprastinės valandos ir viršvalandžiai.

Norėdami nustatyti atostogų planą, kuriame būtų naudojamos darbo valandos, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Atostogų ir neatvykimų planai** spustelėkite **Kurti naują planą**.
2. Įveskite savo atostogų plano pavadinimą.
3. Pasirinkite plano kaupimo dažnį.
5. Pasirinkite plano pradžios datą.
6. Pasirinkite kaupimo laikotarpio pagrindą ir konkretaus darbuotojo datą (jei taikoma).
7. Pasirinkite kaupimo plano kaupimo tipą **Dirbtos valandos**.
8. Pasirinkite kaupimui naudojamų valandų tipą.
9. Įveskite dirbtų valandų skaičių ir susietą kaupimo sumą, minimalų balansą ir didžiausią perkėlimą arba subsidijos sumą.

Atliekant kaupimo pagal dirbtas valandas planų apdorojimą, norint nustatyti kaupiamas valandas, naudojamas kaupimo dažnis kartu su kaupimo laikotarpio pagrindu.

## <a name="annual-accrual-frequency"></a>Metinis kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Mėnesio kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Pusės mėnesio kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Savaitės kaupimo dažnis

| Kaupimo skyrimo data    | Dirbtų valandų pakopa    | Kaupimo suma        | Dirbtų valandų datos   | Faktinės dirbtos valandos| Premija               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Darbuotojui priskirti atostogų planai

Darbuotojui priskirtuose atostogų planuose rodomas planų pakopos pagrindas ir valandų tipas, kai dirbtos valandos nurodomos kaip kaupimo tipas. Aktyviuose planuose taip pat rodomos faktinės kaupimo laikotarpiais nuo dabartinės datos dirbtos valandos. 

## <a name="loading-data"></a>Įkeliami duomenys

Faktinės valandos gali būti importuojamos duomenų valdyme naudojant atostogų ir nebuvimo darbe valandų skaičiaus objektą. Jei naudojate darbo laiko kalendorius, importavimas patikrins, ar įprastinių dirbtų valandų skaičius neviršija kalendoriuje suplanuotų dienos valandų skaičiaus. Importavimas taip pat patikrina, ar nurodytos dienos dirbtų valandų skaičius ne didesnis negu 24 valandos. 

Norint importuoti atostogų kaupimo procese naudojamas faktines valandas, reikalinga toliau nurodyta informacija.

+ Darbuotojo numeris 
+ Darbo dienos data
+ Tipas
+ Valandos

Viena data gali turėti tik po vieną kiekvieno iš visų su ja susietų tipų pavyzdį.

| DARBUOTOJO NUMERIS       | DARBO DIENOS DATA           | TIPAS                  | VALANDOS                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Reguliarus               | 8                    |       
| 000337                | 8/7/2018             | Reguliarus               | 8                    |
| 000337                | 8/7/2018             | Viršvalandžiai              | 3                    |
| 000337                | 8/8/2018             | Reguliarus               | 8                    |
| 000337                | 8/7/2018             | Reguliarus               | 8                    |
| 000337                | 8/9/2018             | Reguliarus               | 8                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]