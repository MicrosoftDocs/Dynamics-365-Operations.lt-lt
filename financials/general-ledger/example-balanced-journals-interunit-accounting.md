---
title: "Subalansuota interunit apskaitos žurnalai"
description: "Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8b6fda79222905b0df211a0b944aca9e4dc76850
ms.lasthandoff: 03/31/2017


---

# <a name="balanced-journals-for-interunit-accounting"></a>Subalansuota interunit apskaitos žurnalai

Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija. 

Jei apskaitos įrašai nesubalansuoti finansinės dimensijos reikšmių lygiu, papildomi sąskaitos įrašai yra sukuriami automatiškai, kad būtų subalansuotas žurnalas. Šiuose sąskaitos įrašuose siekiant nustatyti pagrindinę sąskaitą naudojami puslapyje **Automatinių operacijų sąskaitos** esantys registravimo tipai **Susiję vienetai – debetas** ir** Susiję vienetai – kreditas**. Pavyzdžiui, kaip balansavimo finansinė dimensija pažymėtas Filialas, kuris yra antrasis DK sąskaitos segmentas, ir netrukus bus sukurti kiti apskaitos įrašai.

|                      |           |
|----------------------|-----------|
| 6100-JEP-OU\_256 | 100,00 DR |
| 6100-NY-OU\_249  | 100,00 DR |
| 2100 – MSP-OU\_256 | 200,00 CR |

Šiuo atveju nustatomi šie balansai:

-   Filialas MSP = 100,00 CR
-   Filialas NY = 100,00 DR

Taigi toliau nurodyti apskaitos įrašai sukuriami automatiškai, siekiant subalansuoti žurnalą finansinių dimensijų reikšmių lygiu.

|                                   |           |
|-----------------------------------|-----------|
| (Interunit debeto) – MSP-OU\_256 | 100,00 DR |
| (Interunit kreditas)-NY-OU\_249 | 100,00 CR |




