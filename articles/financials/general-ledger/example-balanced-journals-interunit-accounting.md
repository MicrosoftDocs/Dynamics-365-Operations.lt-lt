---
title: "Susijusių vienetų apskaitos subalansuoti žurnalai"
description: "Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija."
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5b1d788ebd5617a1d3f1c8ca36f5ae3c29b534c5
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Susijusių vienetų apskaitos subalansuoti žurnalai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija. 

Jei apskaitos įrašai nesubalansuoti finansinės dimensijos reikšmių lygiu, papildomi sąskaitos įrašai yra sukuriami automatiškai, kad būtų subalansuotas žurnalas. Šiuose sąskaitos įrašuose siekiant nustatyti pagrindinę sąskaitą naudojami puslapyje **Automatinių operacijų sąskaitos** esantys registravimo tipai **Susiję vienetai – debetas** ir**Susiję vienetai – kreditas**. Pavyzdžiui, kaip balansavimo finansinė dimensija pažymėtas Verslo struktūros vienetas, kuris yra antrasis DK sąskaitos segmentas, ir netrukus bus sukurti kiti apskaitos įrašai.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Šiuo atveju nustatomi šie balansai:

-   Verslo vieneto kodas MSP = 100,00 CR
-   Verslo vieneto kodas NY = 100,00 DR

Taigi toliau nurodyti apskaitos įrašai sukuriami automatiškai, siekiant subalansuoti žurnalą finansinių dimensijų reikšmių lygiu.

|                                   |           |
|-----------------------------------|-----------|
| (Susiję vienetai – debetas) – MSP – OU\_256 | 100,00 DR |
| (Susiję vienetai – kreditas) – NY – OU\_249 | 100,00 CR |






