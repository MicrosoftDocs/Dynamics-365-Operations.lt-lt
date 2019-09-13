---
title: Darbo užsakymų tipai
description: Šioje temoje aiškinami darbo užsakymų tipai modulyje „Turto valdymas”.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 57120b51c069e49697f8ec4357265974a0d3afb4
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874583"
---
# <a name="work-order-types"></a>Darbo užsakymų tipai

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Darbo užsakymų tipai naudojami siekiant suskirstyti darbo užsakymus į kategorijas. Pavyzdžiui, galite turėti darbo užsakymų, susijusių su prevencine arba taisomąja priežiūra.

Pagal darbo užsakymo tipą apibrėžiama sąsaja su darbo užsakymo ciklo modeliu. Pagal darbo užsakymo ciklo modelį apibrėžiamos darbo užsakymo ciklo būsenos, kurios gali būti nustatytos darbo užsakyme. (Darbo užsakymo ciklo būsenų pavyzdžiai, be kita ko, yra **Sukurtas**, **Vykdomas** ir **Užbaigtas**.)

Daugiau informacijos apie darbo užsakymo ciklo būsenas ir projekto etapus žr. [Darbo užsakymo ciklo būsenos](work-order-lifecycle-states.md).

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Darbo užsakymų tipai**.
2. Norėdami sukurti darbo užsakymo tipą, pasirinkite **Naujas**.
3. Lauke **Darbo užsakymo tipas** įveskite darbo užsakymo tipo ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.
5. Lauke **Darbo užsakymo ciklo modelis** pasirinkite ciklo modelį.
5. Parinktyje **Vienas priežiūros darbuotojas** pasirinkite **Taip**, jeigu visos su šio tipo darbo užsakymu susijusios darbo užsakymo užduotys turėtų būti paskirtos tam pačiam priežiūros darbuotojui.
6. Lauke **Išlaidų tipas** tinkamai pasirinkite **Taisomosios**, **Prevencinės** arba **Investicinės**. Visoms darbo užsakyme nurodytoms darbo užsakymo užduotims turi būti nustatytas toks pat išlaidų tipas.
7. Atitinkamose skyriaus **Privaloma** parinktyse pažymėkite **Taip**, kad patikslintumėte, kuri su gedimais arba prižiūrimo turto prastova susijusi informacija įtraukta į šio tipo darbo užsakymą.

    > [!NOTE]
    > Parinktys skyriuje **Privaloma** yra susijusios su „FastTab” **Tikrinti** parinktimis puslapyje **Darbo užsakymo ciklo būsenos** (**Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Ciklo būsenos**).

8. Pasirinkite **Įrašyti**.

![1 pav.](media/16-setup-for-work-orders.png)
