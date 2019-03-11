---
title: Kurti gamybos užsakymus
description: Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę. Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data. Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "324634"
---
# <a name="create-production-orders"></a>Kurti gamybos užsakymus

[!include [banner](../includes/banner.md)]

Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę. Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data. Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę.

Gamybos užsakymas pereina gamybos ciklo etapus. Kai užsakymas sukurtas, jam priskiriama būsena **Sukurtas**. Kai užsakymas baigtas, jam priskiriama būsena **Baigtas**. Parametro nuostata kiekviename etape leidžia naudotojui konfigūruoti kiekvieną veiksmą. Nuostatą galima nustatyti vienam naudotojui arba visiems naudotojams.

Gamybos komplektavimo specifikacija ir gamybos maršrutas yra pagrindiniai gamybos užsakymo objektai. Jie į gamybos užsakymą kopijuojami pagal pasirinktą prekę ir kiekį, kurį ketinama gaminti. Prieš pradedant gamybos užsakymą, galima redaguoti gamybos komplektavimo specifikaciją ir maršrutą.

Gamybos užsakymą galima kurti pagal toliau pateiktus scenarijus.

-   Sukurtas vykdant bendrąjį planavimą pagal medžiagų poreikį.
-   Sukurtas tiesiai iš pardavimo užsakymo eilutės arba sukūrus ir įvertinus aukštesnio lygio gamybos užsakymą (iškviestas tiekimas).
-   Sukurtas rankiniu būdu.




