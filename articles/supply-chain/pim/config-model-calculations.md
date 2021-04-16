---
title: Produkto konfigūracijos modelio skaičiavimai
description: Šioje temoje aprašoma, kaip sukurti produkto konfigūracijos modulio atributų skaičiavimus
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829623"
---
# <a name="product-configuration-model-calculations"></a>Produkto konfigūracijos modelio skaičiavimai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti produkto konfigūracijos modulio atributų skaičiavimus.

## <a name="prerequisites"></a>Būtinieji komponentai

Skaičiavimai yra naudojami produkto konfigūracijos modelyje, siekiant apskaičiuoti produkto konfigūracijos vertes. Galėsite pradėti nustatyti skaičiavimus tik tuo atveju, jei egzistuos susijęs produkto konfigūracijos modelis. Konfigūracijos modelių ir susijusių užduočių nustatymo proceso apžvalgą rasite [Produkto konfigūracijos modelio nustatymas](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Skaičiavimo sukūrimas

Skaičiavimą sudaro išraiška ir tikslinis atributas. Daugiau informacijos rasite [Produktų konfigūracijos modelių skaičiavimų DUK](calculate-product-configuration-models.md).

Norėdami sukurti skaičiavimą esamam produkto modeliui, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Bendra \> Produkto konfigūracijos modeliai**.
1. Atidarykite produkto konfigūracijos modelį ir tada pasirinkite **Redaguoti**.
1. „FastTab“ **Skaičiavimai** pasirinkite **Įtraukti** norėdami įtraukti skaičiavimą ir tada nustatykite šiuos laukus:

    - **Pavadinimas** – Įveskite skaičiavimo pavadinimą.
    - **Aprašas** – Įveskite skaičiavimo aprašą.
    - **Tikslinis atributas** – Pasirinkite atributą, kuriam atliekate skaičiavimą.

1. Pasirinkite **Redaguoti išraišką**.
1. Dialogo lange **Įvesti skaičiavimą** į išraišką įtraukite reikiamus atributus, operatorius ir reikšmes. Daugiau informacijos apie tai, kaip dirbti su šiais elementais rasite [Išraiškos ir lentelių apribojimai produkto konfigūracijos modeliuose](expression-constraints-table-constraints-product-configuration-models.md).
1. Kai išraiška bus parengta, pasirinkite **Gerai**.

## <a name="calculation-examples"></a>Skaičiavimo pavyzdžiai

Šiame skyriuje pateikiami keli pavyzdžiai, kaip veikia skaičiavimai.

### <a name="example-1"></a>1 pavyzdys

Tikslinis atributas yra Bulio logika, o skaičiavime naudojama ši sąlyginė išraiška:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Išraiška pateikia tikslinio atributo reikšmę *Teisinga*, jei „`decimalAttribute2`” yra lygus arba didesnis nei `decimalAttribute1`. Kitu atveju išraiška grąžina Bulio logikos reikšmę *Klaidinga*.

### <a name="example-2"></a>2 pavyzdys

Šiame pavyzdyje teksto atributas „`textFixedList`” naudojamas kaip tikslo atributas. Šį atributą sudaro toliau pateiktas fiksuotas sąrašas.

| Reikšmė | Sprendimo priemonės reikšmė |
|---|---|
| „A” | „1a” |
| „B” | „2b” |
| „C” | „2c” |

Toliau pateiktoje ekrano kopijoje parodyta, kaip šio atributo parametrai gali atrodyti jūsų sistemoje.

![Atributo tipo parametrai 2 pavyzdžiui](media/model-calculations-example2.png "Atributo tipo parametrai 2 pavyzdžiui")

Atributas yra naudojamas šiame sąlyginiame sakinyje:

`If[integerAttribute < 150, 0, 2]`

Jei „`integerAttribute`” vertė yra mažesnė nei 150, šis sakinys grąžina pirmo įrašo fiksuotame sąraše tekstinę reikšmę *„A”*. Kitu atveju grąžinama trečio įrašo fiksuotame sąraše tekstinė reikšmė *„C”*.

> [!NOTE]
> Fiksuotas sąrašas yra nulinio išvardijimo („enum”) atitikmuo ir jo reikšmės pasiekiamos naudojant atitinkamą sveikojo skaičiaus vertę. Todėl pirmoji fiksuota sąrašo reikšmė (*„A”*) sutapatinama *su 0*, o antroji reikšme (*„B”*) sutapatinama *su 1*, ir trečioji vertė (*„C”*) sutapatinama *su 2*.

### <a name="example-3"></a>3 pavyzdys

Šiame pavyzdyje naudojamas tikslinis atributas „`textFixedList`” iš ankstesnio pavyzdžio. Taip pat naudojamas kitas teksto atributas, „`textAttribute`”, kuriame yra šis fiksuotas sąrašas.

| Reikšmė | Sprendimo priemonės reikšmė |
|---|---|
| „AA” | „1aa” |
| „BB” | „2bb” |

Toliau pateiktoje ekrano kopijoje parodyta, kaip šio atributo parametrai gali atrodyti jūsų sistemoje.

![Atributo tipo parametrai 3 pavyzdžiui](media/model-calculations-example3.png "Atributo tipo parametrai 3 pavyzdžiui")

„`textFixedList`” atributo reikšmė apskaičiuojama naudojant šį sąlyginį sakinį:

`If[textAttribute == "1aa", 0, 2]`

Jei „`textAttribute`” reikšmė turi sprendimo priemonės reikšmę, lygią *„1aa”*, ši išraiška grąžina pirmo įrašo fiksuotame sąraše „`textFixedList`” tekstinę reikšmę *„A”*. Kitu atveju grąžinama trečio įrašo fiksuotame sąraše „`textFixedList`” tekstinė reikšmė *„C”*.

> [!NOTE]
> - Sąlyginis sakinys turi naudoti atributo sprendimo priemonės reikšmę.
> - Skaičiavimuose galima naudoti tik fiksuoto sąrašo teksto atributus.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Produktų konfigūracijos modelių skaičiavimų DUK](calculate-product-configuration-models.md)
- [Išraiškos apribojimo įtraukimas į produkto konfigūracijos modelį](tasks/add-expression-constraint-product-configuration-model.md)
- [Produkto konfigūracijos modelių apžvalga](product-configuration-models.md)
