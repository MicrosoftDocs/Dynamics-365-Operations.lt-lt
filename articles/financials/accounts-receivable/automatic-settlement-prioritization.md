---
title: Automatinis sudengimas ir prioritetų nustatymas
description: Šioje temoje aprašoma, kaip sudengiamos operacijos, jei puslapyje Gautinų sumų parametrai pasirenkate Automatinis sudengimas. Jame taip pat paaiškinama, kaip automatinį sudengimą galima naudoti kartu su mokėjimo prioritetu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 775ce10cdba5e38fbb5fc058c6df297143229f79
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "318976"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatinis sudengimas ir prioritetų nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sudengiamos operacijos, jei puslapyje Gautinų sumų parametrai pasirenkate Automatinis sudengimas. Jame taip pat paaiškinama, kaip automatinį sudengimą galima naudoti kartu su mokėjimo prioritetu.

Sudengti mokėjimus su sąskaitomis faktūromis ir kitomis operacijomis galima dviem būdais. Galite rankiniu būdu pasirinkti norimas sudengti operacijas arba „Microsoft Dynamics 365 for Finance and Operations“ gali automatiškai parinkti operacijas naudodama automatinio sudengimo funkciją. Be to, galite tinkinti automatinių sudengimų taikymo būdą naudodami parinktį **Nustatyti sudengimo prioritetą**. Visos šios parinktys įeina į sudengimo parametrus, kurie nustatomi puslapyje **Gautinų sumų parametrai**. Būdas, kuriuo operacijos yra automatiškai sudengiamos gali skirtis, nes jis priklauso nuo metodo, kurį naudojate automatiniam sudengimui atlikti. Galimi šie metodai:

-   Vartotojo nustatytas sudengimo prioritetas
-   Numatytasis automatinis sudengimas

Toliau pateikiamuose skyriuose aprašoma, kaip operacijos sudengiamos naudojant atskirus metodus.

## <a name="example-transactions"></a>Operacijų pavyzdys
Toliau šiame straipsnyje pateikti sudengimų pavyzdžiai yra paremti toliau pateiktomis operacijomis. Visos operacijos yra 2050 kliento.

| Operacija   | Data        | Suma | Mokėjimo nuolaidos sąlygos | Mokėjimo nuolaidos data | Komentarai                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 sąskaita faktūra     | Rugpjūčio 15 d.   | 100,00 | 2 %14, grynoji 30        | Rugpjūčio 29 d.          |                                                                                                                                                                                               |
| 2 sąskaita faktūra     | Rugsėjo 1 d. | 250,00 | 2 %14, grynoji 30        | Rugsėjo 15 d.       |                                                                                                                                                                                               |
| 3 sąskaita faktūra     | Spalio 15 d.  | 500,00 | 2 % 14 / grynoji 30        | Spalio 29 d.         |                                                                                                                                                                                               |
| Delspinigių pažyma | Spalio 15 d.  | 7,00   |                     |                    | Ši delspinigių pažyma yra 1 sąskaitai faktūrai ir 2 sąskaitai faktūrai. Suma yra apskaičiuojama kaip 2 procentai palūkanų nuo sumų, nuo kurių termino praėjo 30 ar daugiau dienų. Pavyzdys: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Vartotojo nustatytas sudengimo prioritetas
Jei parametrą **Naudoti prioritetą automatiniams sudengimams atlikti** nustatysite į **Taip** puslapyje **Gautinų sumų parametrai**, sudengimo prioritetas, kurį nustatėte puslapyje **Sudengimo prioritetas**, bus naudojamas, kai bus pasirinktos operacijos automatiniams sudengimams atlikti. Pavyzdžiui, nustatomas toks sudengimo prioritetas:

1.  Operacijos tipas
    -   Mokėjimo mokesčiai
    -   Priminimo laiškai
    -   Delspinigių pažymos
    -   SF

2.  Operacijos data didėjimo tvarka
3.  Kvitas

Jei spalio 25 d. registruojate 700,00 mokėjimą, šis mokėjimas bus sudengtas su operacijomis toliau nurodyta tvarka.

| Kvitas       | Data       | PVM sąskaita faktūra | Suma operacijos valiuta | Sudengtina suma | Likutis | Valiuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Delspinigių pažyma | 2015-10-15 |         | 7,00                           | 7,00             | 0,00    | USD      |
| 1 sąskaita faktūra     | 2015-08-15  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| 2 sąskaita faktūra     | 2015-09-01   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| 3 sąskaita faktūra     | 2015-10-15 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Numatytasis automatinis sudengimas
Jei nėra jokio vartotojo nustatyto sudengimo prioriteto, automatiškai pasirenkamos sudengimo operacijos pagal mokėjimo terminą. Sudengtų operacijų valiuta turi būti tokia pat kaip operacijos, kurią jos sudengia. Jei spalio 25 d. registruojate 700,00 mokėjimą, pasirenkamos toliau nurodytos sudengimo operacijos.

| Kvitas       | Data       | PVM sąskaita faktūra | Suma operacijos valiuta | Sudengtina suma | Likutis | Valiuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| 1 sąskaita faktūra     | 2015-08-15  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| 2 sąskaita faktūra     | 2015-09-01   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| 3 sąskaita faktūra     | 2015-10-15 |         | 500,00                         | 350,00           | 150,00  | USD      |
| Delspinigių pažyma | 2015-10-15 |         | 7,00                           | 0,00             | 0,00    | USD      |





