---
title: "Automatinis sudengimas ir prioritetų nustatymo srityse"
description: "Šiame straipsnyje aprašoma, kaip sudengiamos operacijos, jei puslapyje Gautinų sumų parametrai pasirenkate Automatinis sudengimas. Jame taip pat paaiškinama, kaip automatinį sudengimą galima naudoti kartu su mokėjimo prioritetu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Automatinis sudengimas ir prioritetų nustatymo srityse

Šiame straipsnyje aprašoma, kaip sudengiamos operacijos, jei puslapyje Gautinų sumų parametrai pasirenkate Automatinis sudengimas. Jame taip pat paaiškinama, kaip automatinį sudengimą galima naudoti kartu su mokėjimo prioritetu.

Sudengti mokėjimus su sąskaitomis faktūromis ir kitomis operacijomis galima dviem būdais. Galite rankiniu būdu pasirinkti operacijų atsiskaityti arba Microsoft Dynamics 365 operacijoms automatiškai pasirinkti operacijas naudodami automatinio atsiskaitymo funkciją. Be to, galite tinkinti automatinių sudengimų taikymo būdą naudodami parinktį **Nustatyti sudengimo prioritetą**. Visi šie variantai yra dalis sprendimo parametrų, kurie nustatomi pagal **sudaro gautinų sumų parametrai** puslapis. Būdas, kuriuo operacijos yra automatiškai sudengiamos gali skirtis, nes jis priklauso nuo metodo, kurį naudojate automatiniam sudengimui atlikti. Galimi šie metodai:

-   Vartotojo nustatytas sudengimo prioritetas
-   Numatytasis automatinis sudengimas

Toliau pateikiamuose skyriuose aprašoma, kaip operacijos sudengiamos naudojant atskirus metodus.

## <a name="example-transactions"></a>Operacijų pavyzdys
Toliau šiame straipsnyje pateikti sudengimų pavyzdžiai yra paremti toliau pateiktomis operacijomis. Visos operacijos yra 2050 kliento.

| Operacija   | Data        | Suma | Mokėjimo nuolaidos sąlygos | Mokėjimo nuolaidos data | Komentarai                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 sąskaita faktūra     | Rugpjūčio 15 d.   | 100,00 | 2 % 14, grynoji 30        | Rugpjūčio 29 d.          |                                                                                                                                                                                               |
| 2 sąskaita faktūra     | Rugsėjo 1 d. | 250,00 | 2 % 14, grynoji 30        | Rugsėjo 15 d.       |                                                                                                                                                                                               |
| 3 sąskaita faktūra     | Spalio 15 d.  | 500,00 | 2 % 14 / grynoji 30        | Spalio 29 d.         |                                                                                                                                                                                               |
| Delspinigių pažyma | Spalio 15 d.  | 7,00   |                     |                    | Ši palūkanų pažyma yra SF 1 ir 2 sąskaitos faktūros. Suma apskaičiuojama kaip 2 procentai palūkanų sumas, kurios yra 30 ar daugiau dienų pradelstos. Pavyzdys: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Vartotojo sukurto sprendimo prioriteto
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




