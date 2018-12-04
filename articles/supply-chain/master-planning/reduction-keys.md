---
title: "Mažinimo raktai"
description: "Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą. Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus. Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4b7f4ebd635e02f3cfc6d0f620dad30e6b1a98a2
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="reduction-keys"></a>Mažinimo raktai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami pavyzdžiai, kuriais rodoma, kaip nustatyti mažinimo raktą. Jame pateikiama informacija apie įvairius mažinimo rakto parametrus ir kiekvieno iš jų rezultatus. Naudodami mažinimo raktą, galite apibrėžti, kaip sumažinti prognozės poreikius.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>1 pavyzdys: procentas – mažinimo rakto prognozės mažinimo principas
---------------------------------------------------------------

Šiame pavyzdyje parodoma, kaip mažinimo raktas sumažina poreikio prognozės poreikius pagal procentines dalis ir laikotarpius, kuriuos nurodo mažinimo raktas.

1. Puslapyje **Mažinimo raktai** nustatykite toliau nurodytas eilutes.

   | Grąža | Vienetas  | Procentas |
   |--------|-------|---------|
   |   1    | Mėnuo |   100   |
   |   2    | Mėnuo |   75    |
   |   3    | Mėnuo |   50    |
   |   4    | Mėnuo |   25    |


2. Susiekite mažinimo raktą su prekės draudimo grupe.
3. Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Procentas – mažinimo raktas**.
4. Sukurkite 1 000 vienetų per mėnesį poreikio prognozę.

Jei prognozės planavimą paleisite sausio 1 d., poreikio prognozės poreikiai bus naudojami atsižvelgiant į procentus, nustatytus puslapyje **Mažinimo raktai**. Toliau nurodyti poreikio kiekiai perkeliami į bendrąjį planą.

| Mėnuo                | Reikalingas vienetų kiekis |
|----------------------|---------------------------|
| sausio              | 0                         |
| Vasaris             | 250                       |
| Kovas                | 500                       |
| Balandžio                | 750                       |
| Gegužė–gruodis | 1000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>2 pavyzdys: operacijų mažinimo rakto prognozės mažinimo principas
Šiame pavyzdyje parodoma, kaip faktiniai užsakymai, vykdomi per laikotarpius, kuriuos nurodo mažinimo raktas, sumažina poreikio prognozės poreikius.

-   Puslapio **Bendrieji planai** lauke **Mažinimo principas** pasirinkite **Operacijos – mažinimo raktas**.

Sausio 1 d. yra toliau nurodyti pardavimo užsakymai.

| Mėnuo    | Užsakytų vienetų kiekis |
|----------|--------------------------|
| sausio  | 956                      |
| Vasaris | 1 176                    |
| Kovas    | 451                      |
| Balandis    | 119                      |

Jei naudojate tą pačią 1 000 vienetų per mėnesį poreikio prognozę, į bendrąjį planą perkeliami toliau nurodyti poreikio kiekiai.

| Mėnuo                | Reikalingas vienetų kiekis |
|----------------------|---------------------------|
| sausio              | 44                        |
| Vasaris             | 0                         |
| Kovas                | 549                       |
| Balandžio                | 881                       |
| Gegužė–gruodis | 1000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>3 pavyzdys: operacijų dinaminio laikotarpio prognozės mažinimo principas
Dažniausiai sistemos yra nustatomos taip, kad operacijos sumažintų poreikio prognozę per tam tikrus prognozės laikotarpius: savaites, mėnesius ir t. t. Šie laikotarpiai yra nustatomi mažinimo rakte. Tačiau laiko tarpas tarp dviejų poreikio prognozės eilučių taip pat gali *nurodyti* laikotarpį.

1. Kurkite toliau nurodytų datų ir kiekių poreikio prognozę.

   | Data       | Poreikio prognozė |
   |------------|-----------------|
   | Sausio 1  | 1000           |
   | Sausio 5 d.  | 500             |
   | Sausio 12 d. | 1000           |

   Šioje prognozėje nėra aiškaus laikotarpio tarp prognozės datų: tarp pirmosios ir antrosios datų yra keturių dienų laikotarpis, o tarp antrosios ir trečiosios datų yra septynių dienų laikotarpis. Šie įvairūs laikotarpiai yra dinaminiai laikotarpiai.
2. Kurkite pardavimo užsakymo eilutes, kaip nurodyta toliau.
   | Data                             | Pardavimo užsakymo kiekis |
   |----------------------------------|----------------------|
   | Ankstesnių metų gruodžio 15 d. | 500                  |
   | Sausio 3 d.                        | 100                  |
   | Sausio 10 d.                       | 200                  |

Prognozė bus sumažinama, kaip parodyta toliau.

-   Pirmasis pardavimo užsakymas nepatenka į jokį laikotarpį, todėl jis nesumažins jokios prognozės.
-   Antrasis pardavimo užsakymas yra tarp sausio 1 d. ir sausio 5 d., todėl jis sumažins sausio 1 d. prognozę 100.
-   Trečiasis pardavimo užsakymas yra tarp sausio 5 d. ir sausio 12 d., todėl jis sumažins sausio 5 d. prognozę 200.

Prognozei įvykdyti bus sukurtas toliau nurodytas suplanuotas užsakymas.

| Poreikio prognozės data | Sumažintas kiekis |
|----------------------|------------------|
| Sausio 1            | 900              |
| Sausio 5 d.            | 300              |
| Sausio 12 d.           | 1000            |

Toliau pateikiama sumažinimo **Operacijos – dinaminis laikotarpis** suvestinė.

-   Prognozės poreikius sumažina faktinės užsakymo operacijos, vykdomos dinaminio laikotarpio metu. Dinaminis laikotarpis apima dabartinės prognozės datas ir baigiasi, kai prasideda kita prognozė.
-   Naudojant šį metodą mažinimo raktas nėra reikalingas.
-   Naudojant šią parinktį, įvyksta toliau pateikti scenarijai.
    -   Jei prognozė sumažinama iki galo, dabartinės prognozės poreikiai tampa 0 (nulis).
    -   Jei nėra ateities prognozės, mažinami poreikiai iš paskutinį kartą įvestos prognozės.
    -   Laiko ribos įtraukiamos skaičiuojant prognozės mažinimą.
    -   Teigiamos dienos įtraukiamos skaičiuojant prognozės mažinimą.
    -   Jei faktinės užsakymo operacijos yra didesnės nei prognozuoti poreikiai, likusios operacijos nėra perduodamos į kitą prognozės laikotarpį.


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Bendrieji planai](master-plans.md)




