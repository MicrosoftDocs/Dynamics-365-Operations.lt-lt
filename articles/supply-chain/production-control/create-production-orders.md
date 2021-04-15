---
title: Gamybos užsakymo ciklo apžvalga
description: Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę. Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data. Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę.
author: johanhoffmann
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df773cf13b8ccd9ee4f861955b1a4321af38a150
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811803"
---
# <a name="production-order-lifecycle-overview"></a>Gamybos užsakymo ciklo apžvalga

[!include [banner](../includes/banner.md)]

Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę. Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data. Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę.

Gamybos užsakymas pereina gamybos ciklo etapus. Kai užsakymas sukurtas, jam priskiriama būsena **Sukurtas**. Kai užsakymas baigtas, jam priskiriama būsena **Baigtas**. Parametro nuostata kiekviename etape leidžia naudotojui konfigūruoti kiekvieną veiksmą. Nuostatą galima nustatyti vienam naudotojui arba visiems naudotojams.

Gamybos komplektavimo specifikacija ir gamybos maršrutas yra pagrindiniai gamybos užsakymo objektai. Jie į gamybos užsakymą kopijuojami pagal pasirinktą prekę ir kiekį, kurį ketinama gaminti. Prieš pradedant gamybos užsakymą, galima redaguoti gamybos komplektavimo specifikaciją ir maršrutą.

Gamybos užsakymą galima kurti pagal toliau pateiktus scenarijus.

-   Sukurtas vykdant bendrąjį planavimą pagal medžiagų poreikį.
-   Sukurtas tiesiai iš pardavimo užsakymo eilutės arba sukūrus ir įvertinus aukštesnio lygio gamybos užsakymą (iškviestas tiekimas).
-   Sukurtas rankiniu būdu.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]