---
title: "Susijusių vienetų apskaitos subalansuoti žurnalai"
description: "Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Susijusių vienetų apskaitos subalansuoti žurnalai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija. 

Jei apskaitos įrašai nesubalansuoti finansinės dimensijos reikšmių lygiu, papildomi sąskaitos įrašai yra sukuriami automatiškai, kad būtų subalansuotas žurnalas. Šiuose sąskaitos įrašuose siekiant nustatyti pagrindinę sąskaitą naudojami puslapyje **Automatinių operacijų sąskaitos** esantys registravimo tipai **Susiję vienetai – debetas** ir**Susiję vienetai – kreditas**. Pavyzdžiui, kaip balansavimo finansinė dimensija pažymėtas Filialas, kuris yra antrasis DK sąskaitos segmentas, ir netrukus bus sukurti kiti apskaitos įrašai.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Šiuo atveju nustatomi šie balansai:

-   Filialas MSP = 100,00 CR
-   Filialas NY = 100,00 DR

Taigi toliau nurodyti apskaitos įrašai sukuriami automatiškai, siekiant subalansuoti žurnalą finansinių dimensijų reikšmių lygiu.

|                                   |           |
|-----------------------------------|-----------|
| (Susiję vienetai – debetas) – MSP – OU\_256 | 100,00 DR |
| (Susiję vienetai – kreditas) – NY – OU\_249 | 100,00 CR |






